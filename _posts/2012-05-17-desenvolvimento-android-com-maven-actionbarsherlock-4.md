---
title: Desenvolvimento Android com Maven + ActionBarSherlock 4
author: Rodrigo Carvalho
layout: post
permalink: /desenvolvimento-android-com-maven-actionbarsherlock-4/
Views:
  - 188
comments: true
categories:
  - Dicas
  - Tecnologia
tags:
  - actionbarsherlock
  - android
  - android-maven-plugin
  - m2e-android
  - maven
---
Estes últimos dias, estou tentando retomar o projeto do aplicativo da <a title="Aplicativo da Espirito Livre para Android" href="https://github.com/espiritolivre/Espirito-Livre-Para-Android" target="_blank">Revista Espírito Livre para Android</a>. A primeira versão que desenvolvi foi bem simples, mas serviu para me dar uma boa visão sobre os rumos da plataforma e me incentivou a estudar bastante. Com isso, vi que dava para melhorar o aplicativo em vários pontos e que a melhor opção seria começar uma nova versão do zero.

Uma das minhas ideias para esta nova versão era começar a utilizar o <a title="Apache Maven" href="http://pt.wikipedia.org/wiki/Apache_Maven" target="_blank">Maven</a> para gerenciar as dependências do aplicativo. Quem conhece a ferramenta, sabe que ela oferece diversos benefícios como, por exemplo, o build independente de IDE e eliminar a necessidade de versionar os binários das APIs dependentes.

**Maven no Android**

Comecei a pesquisar e encontrei o <a title="Página do android-maven-plugin" href="http://code.google.com/p/maven-android-plugin/" target="_blank">android-maven-plugin</a>. Este plugin adiciona ao ciclo de vida do Maven as especificidades da compilação de um projeto Android.

Além disso, existem <a title="Arquétipos Maven" href="http://stand.spree.de/wiki_details_maven_archetypes" target="_blank">arquétipos</a> (*archetypes*) que criam a estrutura de diretórios e arquivos básicos de qualquer projeto Android, além de já incluir no pom.xml o android-maven-plugin configurado com a versão desejada do Android. O arquétipo que mais me interessou foi o &#8220;android-release&#8221; que, além do projeto principal, cria um projeto de testes e configura o projeto para gerar um pacote para distribuição.

**Maven + Android + Eclipse**

Com o projeto Maven pronto, já dá para compilar e gerar um pacote da aplicação pela linha de comando. No entanto, apesar do Eclipse (a partir da versão 3.7 &#8220;Indigo&#8221;) suportar projetos Maven nativamente, ao tentar importar o projeto, ele apresentará um erro.

Assim como Maven precisa de um plugin para lidar com as especificidades da compilação para Android, o Eclipse também precisa. O <a title="Site do plugin ADT" href="https://developer.android.com/sdk/eclipse-adt.html" target="_blank">ADT</a> por si só não consegue lidar com o projeto, pois ele não espera um projeto no formato Maven.

Mas para configurar é muito fácil. Considerando que está utilizando a versão 3.7, você deverá utilizar o plugin <a title="Site do m2e-android" href="http://rgladwell.github.com/m2e-android/" target="_blank">m2e-android</a>. Para instalá-lo é bem simples e está explicado em sua página.

***Atenção:** Não confundir este com o &#8220;m2eclipse-android-integration&#8221;, que é a versão antiga do m2e-android. Parece bobeira, mas eu bati muito a cabeça com isso!*

**ActionBarSherlock 4**

Superados os problemas do Maven e sua integração com o Eclipse, chegou a hora de incluir no projeto o <a title="Site do ActionBarSherlock" href="http://actionbarsherlock.com/" target="_blank">ActionBarSherlock</a>, componente que já mencionei <a title="Visual moderno em aplicativos Android" href="/visual-moderno-em-aplicativos-android/" target="_blank">num post anterior</a>. Como estava desenvolvendo uma versão nova do aplicativo, também decidi atualizar a biblioteca para a versão 4.0. No entanto, ao incluí-la no projeto, tive um erro.

Infelizmente, documentação não é o forte do componente e, depois de bater muito a cabeça, descobri que a versão nova exige que a compilação seja feita para Android 4 (e não para Android 3, como a versão antiga). Sendo assim, você deve configurar seu projeto para o *API level* 15 e a versão do Android 4.0.1.2.

Além disso, tentei rodar a aplicação num emulador rodando Android 1.6 (versão mínima compatível na versão 3.0) e tive outro erro. Também depois de perder algum tempo, descobri que a versão agora só suportava versões do Android a partir da 2.1.

**Conclusão**

Apesar destes problemas, vale muito a pena utilizar o Maven nos projetos. Eu bati muito a cabeça, mas espero que este artigo te ajude a evitar estes problemas e que consiga utilizar a ferramenta muito mais tranquilamente.

Uma última dica para quem utiliza o ActionBarSherlock, é utilizar o arquétipo Maven para gerar o projeto e, durante a geração, escolher a *API level* 15. Você deve tomar cuidado que o padrão é a *API level* 10, mas você pode negar esta escolha e forçar a versão desejada.

Por fim, torço muito para que o ambiente Maven para Android seja cada vez mais utilizado e fique cada vez mais estável e fácil de usar.
