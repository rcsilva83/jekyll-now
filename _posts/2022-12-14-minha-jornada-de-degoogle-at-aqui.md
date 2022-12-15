---
author: Rodrigo Carvalho
layout: post
comments: true
published: true
title: Minha jornada de "degoogle" até aqui
categories:
  - Tecnologia
tags:
  - nextcloud
  - cloudron
  - onlyoffice
  - ente
  - linode
  - onetsolutions
  - scaleway
  - privacidade
  - privacy
---
Há muito tempo estou insatisfeito com a forma como a Google trata as informações de seus usuários. Fui usuário dos seus produtos gratuitos por anos, mas, com o passar do tempo, fui ficando mais consciente de como o modelo de negócios de "pague com seus dados" é danoso e busquei alternativas. Foram anos até concretizar a migração que vou narrar a seguir que contempla o seguinte:

1. Google Search -> [DuckDuckGo](https://duckduckgo.com/) e [Startpage](https://www.startpage.com/)
1. Gmail -> [Cloudron](https://www.cloudron.io/) (servidor) + [SOGo](https://www.sogo.nu/) (webmail)
1. Google Calendar -> [SOGo](https://www.sogo.nu/)
1. Google Drive -> [Nextcloud](https://nextcloud.com/)
1. Google Docs -> [Nextcloud](https://nextcloud.com/) + [OnlyOffice](https://www.onlyoffice.com/pt/office-for-nextcloud.aspx)
1. Google Photos -> [Ente](https://ente.io/)

Migrar o buscador é fácil, então, como o assunto é longo, vamos focar nos demais. Desde já adianto que tratarei cada ponto sem grandes explicações para deixar o texto o mais curto possível. Se desejar que eu detalhe um pouco mais alguma coisa, peça nos comentários que eu respondo ou faço um outro post.

<!-- more -->

## Com tudo para o Nextcloud!

Minha primeira tentativa de migração foi apostando todas as fichas no Nextcloud. Escolhi um [provedor](https://nextcloud.com/sign-up/) que achei ter um bom custo-benefício ([Cloudamo](https://cloudamo.com/)) e comecei a migrar tudo para lá. Em pouco tempo vi que o Nextcloud não atenderia todas as minhas necessidades de forma satisfatória, principalmente na parte de e-mail. 

1. ele não oferece um servidor de e-mail, somente um webmail;
1. o webmail é bem fraco e com um layout que não prioriza o conteúdo;
1. a busca do Nextcloud é bastante ruim para apresentar resultados de e-mail;
1. e ainda encontrei alguns bugs bem chatos na importação do Google e outros.

Para completar, servidor no Cloudamo era bem lento... Se eu quisesse um servidor mais rápido, o custo seria bem alto para uma solução que já não estava me atendendo bem.

## Vamos de Mailbox.org

Após a decepção com o Nextcloud, tentei a [Mailbox.org](https://mailbox.org/en/). Ali eu já passei a ter um servidor de e-mail, podendo migrar meus e-mails do Gmail e ter um endereço `@rodsilva.com`. O webmail, apesar de simples, era bem melhor que o do Nextcloud. No entanto, a interface ainda era um pouco lenta, o gestor de tarefas tinha uma interface muito ruim e, o principal, o editor de documentos estava corrompendo meus arquivos após editá-los!

## Uma nova chance para o Nextcloud com Linode e Yunohost

Comecei a ver alguns [vídeos no Youtube](https://www.youtube.com/watch?v=FGS-VL6MgLo) patrocinados pela [Linode](https://www.linode.com/) e como seus servidores poderiam ser usados para hospedar um serviço Nextcloud. Resolvi usar um cupom de 100 dólares para testar e descobri o Cloudron na lista de aplicações com instalador pronto. Pesquisei por uma alternativa open source e encontrei o [Yunohost](https://yunohost.org/). 

O Yunohost é um projeto muito legal que usei um tempo, mas não deu muito certo. Eles evitam usar soluções de contêineres (como [Docker](https://pt.wikipedia.org/wiki/Docker_(software))), mas isso acaba impactando no processo de atualização das aplicações instaladas. Para dar um exemplo, uma versão nova do Nextcloud precisava de uma atualização do PHP. Para atualizá-lo, seria necessária a atualização do PHP do sistema todo, deixando todo o processo muito delicado e, por consequência, demorado.

Além disso, vi que eles não têm um modelo de negócios que possa sustentar de forma segura desenvolvedores em tempo integral - dependerem totalmente de doações. Isso me deixou inseguro em confiar toda minha vida digital com o software deles.

## Sai Yunohost, entra Cloudron

De qualquer forma, a solução de um servidor na Linode ainda parecia boa e fui tentar o Cloudron. Em pouco tempo consegui montar meu servidor e tive confiança de mandar tudo para lá. O ponto negativo do Cloudron é que eu acho a assinatura deles um pouco cara (mais cara que o próprio servidor). Gostaria de contribuir financeiramente com o desenvolvimento do software, mas acabei optando pela versão gratuita com limite de 2 aplicações instaladas. Num contexto onde estava usando o servidor mais simples da Linode, não conseguiria rodar muitas aplicações de qualquer forma.

O Cloudron tem um servidor de e-mails e, com o Nextcloud instalado, a segunda aplicação teria que ser um webmail. Inicialmente escolhi o [Roundcube](https://roundcube.net/), mas, após um tempo, migrei para o SOGo para ter integração do e-mail com a agenda.

## Sai Linode, entra OnetSolutions e Scaleway.

Após a instalação do SOGo, que é mais pesado que o Roundcube, meu servidor da Linode começou a ficar instável por falta de memória. Como a próxima opção de servidor na Linode custaria do dobro do preço, fui pesquisar alternativas. Encontrei o site [VPSBenchmarks](https://www.vpsbenchmarks.com/) e nele encontrei a [OnetSolutions](https://onetsolutions.net/en/vps-server), que oferece um servidor com configuração melhor e mais barato que a Linode, e a [Scaleway](https://www.scaleway.com/en/), que oferece um serviço do [object storage](https://www.ibm.com/br-pt/cloud/learn/what-is-object-storage) praticamente gratuito até um limite de uso e era perfeito para armazenar os backups diários do servidor.

## Para fotos: Ente

No entanto, o Nextcloud estava me decepcionando em outro ponto: trabalhar com fotos não se mostrou viável. Inicialmente o Nextcloud caiu muitas vezes durante o processo de upload inicial, pelo alto volume de arquivos. Passada esta etapa, o acesso às fotos era muito lento e muitas vezes simplesmente não conseguia visualizar as que queria. Além disso, a interface e funcionalidade do Nextcloud para este uso também não são das melhores e o aplicativo para Android apresentou bugs para detectar novas fotos e enviar para o servidor.

Neste ponto, vi que seria melhor atendido por serviço especializado em armazenamento de fotos e decidi pelo Ente. Estou usando há poucos dias, já estou encontrando alguns bugs no upload inicial, mas a experiência geral está bem melhor que no Nextcloud. A equipe é solícita quanto aos bugs reportados, enquanto no Nextcloud o comum era que os bugs que reportei ficassem praticamente sem resposta.

## Essa história ainda não chegou ao fim

É bem possível que eu mude algumas coisas na minha configuração atual e ainda exitem outros serviços do Google a abandonar (GMS do Android, Waze, Google Maps, Youtube...), mas espero que o relato da minha jornada até aqui inspire e ajude outras pessoas que desejam fazer o mesmo.

Teve algum ponto que gostaria de saber mais detalhes? Peça nos comentários!
