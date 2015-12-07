---
title: A abertura do Android
author: Rodrigo Carvalho
layout: post
permalink: /a-abertura-do-android/
comments: true
Views:
  - 1
categories:
  - Liberdade
  - Tecnologia
tags:
  - android
  - aosp
  - bazar
  - catedral
---
Como já comentei no artigo &#8220;<a title="O sucesso do Android" href="o-sucesso-do-android/" target="_blank">O sucesso do Android</a>&#8220;, uma das maiores críticas ao sistema do robô verde é a falta de abertura no seu desenvolvimento por parte da Google. O que acontece é que a empresa desenvolve o sistema a portas fechadas e, após o lançamento de uma nova versão, ela &#8220;joga&#8221; o código nos repositórios públicos do <a title="Android Open Source Project" href="http://source.android.com/" target="_blank">Android Open Source Project</a> (AOSP). Apesar de ser um defensor do software livre e concordar que a política de desenvolvimento do Android não é das mais abertas, sou obrigado a discordar de grande parte dessas críticas.

**Long live to true open source**

Em outubro do ano passado, <a title="Joe Hewitt" href="http://en.wikipedia.org/wiki/Joe_Hewitt_(programmer)" target="_blank">Joe Hewitt</a>, um conhecido desenvolvedor *open source* e usuário de iPhone, <a href="http://www.euandroid.com.br/noticia/2010/10/famoso-desenvolvedor-joe-hewitt-software-livre-questiona-apple-e-google/" target="_blank">fez críticas ao Google</a> dizendo que o Android não é diferente do iOS em termos de abertura. Ele compara seu modelo de desenvolvimento com o do <a title="Firefox" href="http://getfirefox.com" target="_blank">Firefox</a> e do <a title="Linux" href="http://pt.wikipedia.org/wiki/Linux" target="_blank">Linux</a>, como estes sendo verdadeiros softwares livres. No entanto, é muito estranho para mim uma pessoa como o Joe falar tamanha bobeira, parecendo, inclusive, que ele está desesperadamente procurando uma justificativa para utilizar o iPhone ao invés de um smartphone com Android.

Um texto bastante conhecido para qualquer pessoa interessada em software livre (e leitura obrigatória para qualquer geek ou hacker) é o &#8220;<a title="The Cathedral and The Bazaar" href="http://www.catb.org/~esr/writings/cathedral-bazaar/cathedral-bazaar/" target="_blank">The Cathedral and The Bazaar</a>&#8220;, escrito por <a title="Eric Raymond" href="http://pt.wikipedia.org/wiki/Eric_Steven_Raymond" target="_blank">Eric Raymond</a>, que descreve duas formas de desenvolver um software. Uma delas ele compara com uma catedral, onde o software é desenvolvido por um grupo fechado de pessoas, sem muito barulho. Outra forma ele compara com um bazar, onde o desenvolvimento é feito de forma mais pública e que está aberta para qualquer um contribuir. Podemos ver claramente que desenvolvimento do Android se encaixa na primeira e que, apesar deste modelo ser mais comum no desenvolvimento de softwares proprietários, ele já foi utilizadoem softwares livres, como o <a title="Emacs" href="http://pt.wikipedia.org/wiki/Emacs" target="_blank">Emacs</a>, desenvolvido pelo próprio fundador do movimento do software livre, <a title="Richard Stallman" href="http://pt.wikipedia.org/wiki/Richard_Matthew_Stallman" target="_blank">Richard Stallman</a>. Será que realmente o Android não pode ser considerado software livre por ser desenvolvido a portas fechadas?

Além disso, como fazer uma comparação ao iOS? Graças à abertura do código do Android, o meu <a title="HTC Magic" href="http://pt.wikipedia.org/wiki/HTC_Magic" target="_blank">HTC Magic</a> está sempre atualizado com a última versão do sistema. Aliás, graças à abertura do código, é possível <a title="iDroid" href="http://www.idroidproject.org/" target="_blank">rodar o sistema do Google num iPhone</a> :) É possível o contrário? Sem o código em mãos, absolutamente não.

**Por que catedral?**

No texto, Eric Raymond fala muito sobre um projeto muito bem sucedido e atribui este sucesso ao modelo &#8220;bazar&#8221;: o Linux. Se este modelo é tão bom, porque o Google optou pelo &#8220;catedral&#8221;? A <a title="FAQ AOSP" href="http://source.android.com/faqs.html#aosp" target="_blank">resposta oficial</a> é esta:

> Why are parts of Android developed in private?
> 
> It typically takes over a year to bring a device to market, but of course device manufacturers want to ship the latest software they can. Developers, meanwhile, don&#8217;t want to have to constantly track new versions of the platform when writing apps. Both groups experience a tension between shipping products, and not wanting to fall behind.
> 
> To address this, some parts of the next version of Android including the core platform APIs are developed in a private branch. These APIs constitute the next version of Android. Our aim is to focus attention on the current stable version of the Android source code, while we create the next version of the platform as driven by flagship Android devices. This allows developers and OEMs to focus on a single version without having to track unfinished future work just to keep up. Other parts of the Android system that aren&#8217;t related to application compatibility are developed in the open, however. It&#8217;s our intention to move more of these parts to open development over time.

Na lista de discussão <a title="Lista Android Brasil" href="http://groups.google.com/group/androidbrasil" target="_blank">Android Brasil</a>, houve uma <a title="Discussão sobre o AOSP" href="http://groups.google.com/group/androidbrasil/browse_thread/thread/3789721c31272fdf?hl=pt-BR#" target="_blank">discussão</a> sobre este texto e minha opinião é a mesma de diversas pessoas da lista: no mercado móvel há uma concorrência muito acirrada e as empresas que investem no Android querem ter uma vantagem competitiva em relação às suas concorrentes. Talvez este tenha sido, inclusive, o motivo do sucesso do sistema e um dos motivos do fracasso de tantos outros sistemas abertos que tentaram entrar neste mercado.

**Futuro**

Como o próprio Google disse em sua nota oficial, eles querem que cada vez mais o sistema seja desenvolvido de forma aberta e tudo dependerá de como o mercado irá se comportar. O recente <a title="Notícia sobre a retenção do código da versão 3.0" href="http://br-linux.org/2011/contra-ma-ajambracao-google-pretende-reter-por-enquanto-o-codigo-fonte-do-android-3-0/" target="_blank">anúncio da retenção do código da versão 3.0</a> por mais tempo do que o normal foi um prato cheio para os alarmistas, mas ainda não vi motivos para que ela mantenha esta versão fechada para sempre. O Android sempre teve seu código disponibilizado e isto é um dos principais motivos para o seu sucesso &#8211; mudar esta política agora seria um tiro no pé.

Desta forma, acho que estamos caminhando para um futuro cada vez mais aberto para o Android. Eu, como usuário do sistema, torço muito para que isto aconteça, pois os projetos desenvolvidos em forma de &#8220;bazar&#8221; costumam ter uma evolução muito mais rápida, com muito mais inovações e menos bugs, como aconteceu com o Linux.
