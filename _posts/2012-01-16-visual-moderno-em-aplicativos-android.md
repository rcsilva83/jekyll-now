---
title: Visual moderno em aplicativos Android
author: Rodrigo Carvalho
layout: post
permalink: /visual-moderno-em-aplicativos-android/
Views:
  - 152
comments: true
categories:
  - Tecnologia
tags:
  - actionbar
  - actionbarsherlock
  - android
  - compatibility library
  - design
  - greendroid
  - ui
---
Quando foi lançada, a versão 3.0 do sistema Android trouxe um visual totalmente remodelado e com diversos conceitos de interface diferentes. Desde então, a Google vem modificando a API adicionando novos padrões de UI (interface de usuário), com o objetivo de tornar os aplicativos desenvolvidos na plataforma mais intuitivos.

No início, apenas os aparelhos com versões do sistema a partir da 3.0 tinha acesso a estas novas APIs, trazendo um grande problema de fragmentação. Afinal, como tirar proveito destas melhorias se a grande maioria dos aparelhos no mercado ainda estão trabalhando com Android 2.x? Foi então lançada a <a title="Android Compatibility Library" href="http://developer.android.com/sdk/compatibility-library.html" target="_blank">Compatibility Library</a>, para possibilitar embarcar estas APIs mais recentes junto com as aplicações, possibilitando seu acesso mesmo nas versões mais antigas do sistema.

Esta semana a Google deu mais um passo na direção certa e lançou o <a title="Site do Android UI Design Guidelines" href="http://developer.android.com/design/index.html" target="_blank">Android UI Design Guidelines</a>. Leitura obrigatória para quem está desenvolvendo para a plataforma, explica todos os conceitos de interface utilizados e tudo o que você deve e não fazer ao desenvolver aplicativos.

**O problema do ActionBar**

Sabemos que devemos seguir o guia e utilizar as APIs de compatibilidade para poder seguí-lo, no entanto uma peça chave da interface de um aplicativo Android ficou estranhamente de fora do Compatibility Library: o <a title="Padrão de UI ActionBar" href="http://developer.android.com/design/patterns/actionbar.html" target="_blank">ActionBar</a>.

Uma opção seria implementar por conta própria, o que não é muito produtivo. Outra seria copiar o código de um aplicativo como o do <a title="Site do aplicativo do Google I/O" href="http://code.google.com/p/iosched/" target="_blank">Google I/O</a> (o que parece ser a recomendação), mas fazer &#8220;copy-and-paste&#8221; não é uma das técnicas de programação mais inteligentes.

A melhor opção então é procurar bibliotecas de terceiros para incorporar no aplicativo. Inicialmente conheci o <a title="Site do GreenDroid" href="http://greendroid.cyrilmottier.com/" target="_blank">GreenDroid</a>, que é utilizado no <a title="Aplicativo do Ubuntu One para Android" href="https://market.android.com/details?id=com.ubuntuone.android.files&hl=pt_BR" target="_blank">aplicativo do Ubuntu One</a> e, além da ActionBar, tem vários outros recursos. Mas a opção que escolhi foi o <a title="Site do ActionBarSherlock" href="http://actionbarsherlock.com" target="_blank">ActionBarSherlock</a>.

O ActionBarSherlock tem a vantagem de tentar ser um superconjunto da Compatibility Library, ou seja, ele já contém tudo desta API e mais a ActionBar. Melhor de tudo, se a versão do Android no aparelho é recente, ele utiliza a ActionBar nativa. Seu uso é muito simples e irei utilizar no meu novo projeto: o <a title="Aplicativo para Android da Revista Espírito Livre" href="https://github.com/espiritolivre/Espirito-Livre-Para-Android" target="_blank">aplicativo para Android da Revista Espírito Livre</a>.

**Mais fontes de estudo**

Com o problema do ActionBar resolvido, você pode começar a desenvolver seus aplicativos Android utilizando todo o potencial da plataforma e, ainda assim, mantendo a compatibilidade com até a versão 1.6 do sistema.

Um site bem legal que conheci nas minhas buscas (onde conheci do ActionBarSherlock) é o <a title="Site Androi UI Design Patterns" href="http://www.androiduipatterns.com/" target="_blank">Android UI Design Patterns</a>. Ele contém diversos artigos explicativos dos padrões de interface para Android, dicas de implementação e muito mais.

Outra dica boa é o site <a title="Android Assets Studio" href="http://android-ui-utils.googlecode.com/hg/asset-studio/dist/index.html" target="_blank">Android Assets Studio</a>, que é uma mão na roda para criação de ícones para seu aplicativo. Eu que não sou nenhum artista gráfico, consegui criar ícones simples porém bonitos com apenas alguns cliques.

Espero que as dicas acima os ajudem a desenvolver aplicativos com excelente visual e consistente com a plataforma Android. Caso tenham alguma outra dica, compartilhem nos comentários!
