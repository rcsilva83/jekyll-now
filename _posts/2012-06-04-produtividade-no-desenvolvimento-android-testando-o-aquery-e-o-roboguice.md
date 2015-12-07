---
title: 'Produtividade no desenvolvimento Android: testando o AQuery e o RoboGuice'
author: Rodrigo Carvalho
layout: post
permalink: /produtividade-no-desenvolvimento-android-testando-o-aquery-e-o-roboguice/
Views:
  - 155
comments: true
categories:
  - Tecnologia
tags:
  - android
  - aquery
  - comparativo
  - guice
  - ioc
  - roboguice
---
Como último estágio antes da retomada do desenvolvimento da nova versão do <a title="Repositório do aplicativo para Android da Revista Espírito Livre" href="https://github.com/espiritolivre/Espirito-Livre-Para-Android" target="_blank">aplicativo da Revista Espírito Livre</a>, resolvi testar dois frameworks que prometem mais produtividade e código mais limpo para suas aplicações Android. O objetivo dos testes é escolher um deles para utilizar na próxima versão do aplicativo.

O primeiro será o <a title="Site do AQuery" href="http://code.google.com/p/android-query/" target="_blank">AQuery</a>, componente que provê uma API ao estilo do framework Javascript <a>JQuery</a>, tornando o código mais compacto e expressivo.

O segundo será o <a title="Site do RoboGuice" href="http://code.google.com/p/roboguice/" target="_blank">RoboGuice</a>, uma extensão do framework Java de <a title="Inversão de controle na Wikipédia" href="http://pt.wikipedia.org/wiki/Invers%C3%A3o_de_controle" target="_blank">IOC</a> <a title="Site do Google Guice" href="http://code.google.com/p/google-guice/" target="_blank">Google Guice</a> com funcionalidades específicas para o mundo Android.

Para os testes, utilizarei a primeira versão do aplicativo da REL. Segue um trecho de código do aplicativo original para servir como comparativo:

<script src="https://gist.github.com/rcsilva83/2847729.js"></script>

**AQuery**

Antes de tecer qualquer comentário, segue abaixo como ficou o código original portado para o AQuery:

<script src="https://gist.github.com/rcsilva83/2847655.js"></script>

*Pontos positivos*

*   Conforme prometido, o código ficou realmente mais compacto e expressivo. É possível fazer muitas configurações num mesmo objeto com apenas 1 linha de código sem perder a legibilidade.
*   O uso de <a title="Interface fluente na Wikipédia (em inglês)" href="http://en.wikipedia.org/wiki/Fluent_interface" target="_blank">interface fluente</a> é muito positivo e grande responsável pelo código enxuto e limpo.
*   Pelo que vi na documentação, o tratamento de XML e Json parece bastante poderoso, apesar de não ter utilizado.

*Pontos negativos*

*   O componente ainda é um pouco limitado no que se refere a abrangência das funcionalidades do Android e, basicamente, se limita a configurar componentes visuais.
*   O uso do AQuery em apenas algumas partes do código, o torna despadronizado e estranho, pois uma parte fica com cara de Java e outra não. O ponto acima torna este problema mais evidente, pois o uso da API é pequeno em relação ao restante do código.
*   Comparado ao RoboGuice, ele não é tão maduro, pois é uma biblioteca mais jovem e ainda nem atingiu sua versão 1.0. Apesar do fato de não ter chegado na versão 1.0 não significar que o componente tem muitos *bugs*, é comum ocorrerem quebras de API antes do lançamento desta versão.

**RoboGuice**

Vamos partir agora para o teste do RoboGuice. Veja como o código original ficou com a utilização do framework:

<script src="https://gist.github.com/rcsilva83/2847682.js"></script>

*Pontos positivos*

*   O código de interface gráfica fica um pouco mais limpo, mas não muito.
*   Ele é um framework de injeção de dependências completo para sua aplicação móvel! Não cabe a este artigo falar das vantagens disso, mas traz grandes possibilidades de melhorar o código.
*   Possui diversas funcionalidades (nem todas foram exploradas no teste), sendo algumas que mais me chamaram atenção:
*   Injeção de todo o tipo de objetos do Android, além dos componentes de interface, como Activity, Context e Application;
*   Processamento de tarefas assíncronas (AsyncTask);
*   API de logging melhorada;

*   Parece ser uma API madura, além de se basear no Guice que é bastante maduro.

*Pontos negativos*

*   A documentação da versão atual (2.0) está muito pobre ainda. Documentação completa só para a versão 1.1.
*   Algo que nem é muito relevante é a certa complexidade para conjugar seu uso com o <a title="Site do ActionBarSherlock" href="http://actionbarsherlock.com/" target="_blank">ActionBarSherlock</a>. O problema é que ambos exigem que suas Activity&#8217;s estendam suas próprias classes, mas Java não tem herança múltipla para poder herdar de ambas. Mas isto foi fácil de solucionar, pois já existe <a title="API para conjugar o RoboGuice com o AactionBarSherlock" href="https://github.com/rtyley/roboguice-sherlock" target="_blank">código pronto</a> para resolver o problema.

**Conclusão**

Avaliadas as duas opções, decidi por utilizar o RoboGuice em meus futuros projetos. Ele é bastante poderoso e trará grandes vantagens para a qualidade do código e para a produtividade no desenvolvimento. O que eu fiquei mais impressionado com o framework foi a quantidade de recursos úteis que ele dispõe.

Não explorei a fundo tudo o que o RoboGuice poderia me proporcionar, pois exigiria uma refatoração completa de uma aplicação que será jogada fora. Isto não significa que o RoboGuice seja intrusivo no código, mas porque ele reforça boas práticas de programação.

Se você discordou de alguma avaliação minha ou tem alguma coisa a acrescentar, utilize a sessão de comentários logo abaixo para compartilhar comigo!

Veja também:

*   <a title="Visual moderno em aplicativos Android" href="/visual-moderno-em-aplicativos-android/" target="_blank">Visual moderno em aplicativos Android</a>
*   <a title="Desenvolvimento Android com Maven + ActionBarSherlock 4" href="/desenvolvimento-android-com-maven-actionbarsherlock-4/" target="_blank">Desenvolvimento Android com Maven + ActionBarSherlock 4</a>
