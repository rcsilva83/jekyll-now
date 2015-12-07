---
title: Configurando PulseAudio com Jack no Ubuntu 10.04
author: Rodrigo Carvalho
layout: post
permalink: /configurando-pulseaudio-com-jack-no-ubuntu-10-04/
Views:
  - 87
comments: true
categories:
  - Dicas
  - Música
tags:
  - jack
  - linux
  - pulseaudio
  - ubuntu
---
Aqui no blog estão faltando artigos a respeito de música (afinal, o subtítulo dele diz que este é um dos assuntos) e estou pretendendo mudar isto. Estou preparando um artigo legal que espero publicar em breve, mas, por hora, vou publicar uma dica rápida e útil para quem trabalha ou pretende trabalhar com música no Linux: que é a integração do <a href="http://pt.wikipedia.org/wiki/JACK_Audio_Connection_Kit" target="_blank">Jack</a> com o <a href="http://pt.wikipedia.org/wiki/PulseAudio" target="_blank">PulseAudio</a>, que é padrão em diversas distribuições.

Para quem não conhece, o Jack é um servidor de áudio para Linux e MacOS X sensacional, desenvolvido para trabalho profissional de edição e produção de áudio. Ele provê baxíssima latência e funciona como uma mesa de som virtual, permitindo que você faça vários programas isolados trabalharem em conjunto de forma fácil. O problema é que, quando ele está rodando, todos os seus softwares que utilizam o PulseAudio param de emitir som. Isto atrapalha muito, pois às vezes estamos gravando alguma coisa e queremos ouvir uma MP3 no programa padrão do computador ou assistir um vídeo no YouTube e não isto não será possível até que o Jack seja encerrado. É para resolver este problema que existe o pacote &#8220;pulseaudio-module-jack&#8221;, fazendo com que o PulSeAudio repasse para o Jack o audio, acabando com este inconveniente!

Já existem alguns tutoriais na Internet explicando isto, mas nenhum funcionou 100% para mim. Então segue o que fiz para funcionar no meu computador:

**1) Instalando o pulseaudio-module-jack**

Pode utilizar Ubuntu Software Center (se preferir a interface gráfica) ou copiar e colar o comando abaixo no Terminal:

<p style="padding-left: 30px;">
  <code>sudo apt-get install  pulseaudio-module-jack</code>
</p>

**2) Copiando configurações padrão do PulseAudio**

Utilize o comando abaixo para copiar o arquivo de configurações padrão do PulseAudio para o seu diretório de usuário:

<p style="padding-left: 30px;">
  <code>cp /etc/pulse/default.pa ~/.pulse/pulsejack.pa</code>
</p>

**3) Configurando o PulseAudio para usar o Jack**

Abra o arquivo criado no passo anterior no seu editor de texto favorito (eu gosto do Gedit) e modifique as seguintes linhas:

<p style="padding-left: 30px;">
  <code>### Load audio drivers statically (it is probably better to not load&lt;br />
### these drivers manually, but instead use module-hal-detect --&lt;br />
### see below -- for doing this automatically)&lt;br />
#load-module module-alsa-sink&lt;br />
#load-module module-alsa-source device=hw:1,0&lt;br />
#load-module module-oss device="/dev/dsp" sink_name=output source_name=input&lt;br />
#load-module module-oss-mmap device="/dev/dsp" sink_name=output source_name=input&lt;br />
#load-module module-null-sink&lt;br />
#load-module module-pipe-sink</code>
</p>

` `

<p style="padding-left: 30px;">
  <code>### Automatically load driver modules depending on the hardware available&lt;br />
.ifexists module-hal-detect.so&lt;br />
load-module module-hal-detect&lt;br />
.else&lt;br />
### Alternatively use the static hardware detection module (for systems that&lt;br />
### lack HAL support)&lt;br />
load-module module-detect&lt;br />
.endif</code>
</p>

para que fiquem assim:

<p style="padding-left: 30px;">
  <code>### Load audio drivers statically (it is probably better to not load&lt;br />
### these drivers manually, but instead use module-hal-detect --&lt;br />
### see below -- for doing this automatically)&lt;br />
#load-module module-alsa-sink&lt;br />
#load-module module-alsa-source device=hw:1,0&lt;br />
#load-module module-oss device="/dev/dsp" sink_name=output source_name=input&lt;br />
#load-module module-oss-mmap device="/dev/dsp" sink_name=output source_name=input&lt;br />
#load-module module-null-sink&lt;br />
#load-module module-pipe-sink&lt;br />
load-module module-jack-source&lt;br />
load-module module-jack-sink</code>
</p>

` `

<p style="padding-left: 30px;">
  <code>### Automatically load driver modules depending on the hardware available&lt;br />
#.ifexists module-hal-detect.so&lt;br />
#load-module module-hal-detect&lt;br />
#.else&lt;br />
### Alternatively use the static hardware detection module (for systems that&lt;br />
### lack HAL support)&lt;br />
#load-module module-detect&lt;br />
#.endif</code>
</p>

**4) Parando o PulseAudio e fazer com que ele não inicie automaticamente**

A configuração padrão do PulseAudio no Ubuntu faz com que ele inicie automaticamente caso ele seja fechado. No nosso caso este não é o comportamento desejado, pois o Jack tem que pará-lo para reiniciá-lo com as configurações feitas no passo anterior. Então rode o comando abaixo para reconfigurar o PulseAudio:

<p style="padding-left: 30px;">
  <code>echo "autospawn = no" &gt; ~/.pulse/client.conf</code>
</p>

**5) Configure o Jack**

Agora só basta dizer para o Jack reiniciar o PulseAudio com as novas configurações quando ele estiver ativo e voltar para o comportamento padrão com ele estiver inativo. Para fazer isto, abra o Jack Control, entre em &#8220;Settings&#8230;&#8221; e vá para a aba &#8220;Options&#8221;. Nesta aba, mude as configurações para as seguintes:

<p style="text-align: center;">
  <a href="/wp-content/uploads/2010/07/Captura_de_tela-Setup-JACK-Audio-Connection-Kit.png"><img class="size-medium wp-image-439  aligncenter" title="Captura_de_tela-Setup - JACK Audio Connection Kit" src="/wp-content/uploads/2010/07/Captura_de_tela-Setup-JACK-Audio-Connection-Kit-300x246.png" alt="Configurações do Jack" width="300" height="246" /></a>
</p>

Pronto, agora nunca mais perderá o som dos aplicativos padrão depois de iniciar o Jack para trabalhar com áudio!

***Créditos:*** Este tutorial foi feito baseado <a href="http://sync-signal.com/2009/12/configuring-jack-and-pulseaudio-on-ubuntu-9-10/" target="_blank">neste</a> que foi encontrado através <a href="http://flavioschiavoni.blogspot.com/2010/05/jack-e-pulse.html" target="_blank">deste</a>.
