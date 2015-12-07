---
title: 'Testes de fim de semana &#8211; parte 1: GnomeDo'
author: Rodrigo Carvalho
layout: post
permalink: /testes-de-fim-de-semana-parte-1-gnomedo/
comments: true
categories:
  - Dicas
tags:
  - linux
  - software livre
---
Os dias úteis são sempre complicados para tirarmos um tempinho para diversão, como testar &#8220;programinhas&#8221; no computador. Este fim de semana testei dois programas (para Linux, claro) que estou com vontade de testar à muito tempo e abaixo falarei sobre o primeiro deles: o <a href="https://wiki.ubuntu.com/GnomeDo" target="_blank">GnomeDo</a>.

Tenho muito ouvido falar da ferramenta GnomeDo, que promete agilizar qualquer tarefa que quisermos realizar ao computador. A instalação no Ubuntu Hardy é muito fácil, já que ele está no repositório, mas o repositório tem poucos plugins e não cheguei a instalar nenhuma outro manualmente, apesar do processo parecer simples.

Instalado, vamos utilizá-lo e, para tal, é preciso deixá-lo rodando em &#8220;background&#8221; com o comando:

> <pre>gnome-do --quiet</pre>

Desta forma, basta utilizar o atalho &#8220;super + espaço&#8221; (onde super é o botão Windows do teclado) que a tela do GnomeDo aparecerá. Ao começar a digitar, ele vai tentando adivinhar progressivamente a tarefa que se deseja realizar. É realmente muito fácil de se usar e traz uma praticidade muito grande! Quer ouvir música? Para que utilizar o mouse e procurar o reprodutor no menu &#8220;Sons&#8221;? &#8220;Super + espaço&#8221; seguido de &#8220;música&#8221; já resolve o problema! Claro que para ser mais prático, o ideal é adicioná-lo aos programa que iniciam junto com a sessão, para ele já ficar disponível após o boot.

<p style="text-align:center;">
  <a href="http://rcarvalho.files.wordpress.com/2008/05/gnomedo.png"><img class="size-medium wp-image-9" src="http://rcarvalho.files.wordpress.com/2008/05/gnomedo.png?w=300" alt="GnomeDo em ação (prestes a buscar no Wikipedia pela minha banda favorita!)" width="300" height="187" /></a>
</p>

Ok, nem tudo são flores. Um problema que encontrei é que nem sempre o que se deseja fazer está escrito da forma como desejamos. Por exemplo, se desejar encontrar um arquivo através do Tracker (software de busca &#8220;full-text&#8221; rápida e indexação de arquivos, equivalente ao Google Desktop ou ao Beagle), o mais lógico seria escrever &#8220;encontrar&#8221;, &#8220;buscar&#8221; ou até &#8220;search&#8221;, mas nada disso funciona. Para abrir a janela do tracker deve-se escrever &#8220;tracker&#8221; ou &#8220;pesquisa&#8221; e colocar a seta para baixo para selecioná-lo, pois a opção que aparece da primeira vez é a ferramenta de configuração. Pelo menos ele é inteligente e da próxima vez que se digita &#8220;pesquisa&#8221;, ele já o coloca como primeira opção.

Resumo, o GnomeDo é muito útil e agiliza muito as tarefas do dia-a-dia. Gostei muito do atalho &#8220;super + espaço&#8221; e da sua forma de uso. Mas uma sugestão que darei ao desenvolvedor é possibilitar o uso de lista de sinônimos e não apenas a busca pelo nome que os programa estão escrito no menu.

A [parte 2][1] já está escrita e já pode ser lida; fala sobre o AWN. Abraço!

 [1]: http://rcarvalho.wordpress.com/2008/05/06/testes-de-fim-de-semana-parte-2-awn/
