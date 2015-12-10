---
published: true
layout: post
title: Facilitando o uso do Github Pages
categories: 
  - Dicas
  - Tecnologia
tags: 
  - wordpress
  - octopress
  - jekyll
  - "github-pages"
date: "2015-12-09 21:29:00 -0300"
---


Há pouco mais de 1 ano resolvi migrar o meu blog do [Wordpress](https://wordpress.org/) para o [Octopress](http://octopress.org/). Estava muito satisfeito com o Wordpress, mas achava que não fazia mais sentido eu pagar uma hospedagem para o blog. O Octopress me possibilitou o uso da hospedagem gratuita do [Github Pages](https://pages.github.com/) (mantendo o meu domínio) além de outros benefícios como:

1. Reduziu drasticamente o tempo de carregamento das páginas;

2. Agora quase nunca o blog fica fora do ar;

3. Sistema de templates muito mais simples, facilitando ajustes no tema visual;

4. Maior segurança, eliminando a preocupação de manter o sistema constantemente atualizado;

<!-- more -->

Mas, é claro, nem tudo são flores e eu já sabia disso. O Wordpress é muito fácil de usar e o Octopress acaba sendo um pouco burocrático na hora de escrever um novo post. Não é à toa que tenho escrito muito menos nos últimos tempos! Para escrever um novo post no Octopress deve-se criar um arquivo formatado em Markdown no computador onde está o "código-fonte" do blog e as ferramentas de geração do Octopress configuradas (Ruby com algumas gems). De cara, já perdemos a edição visual (que pode ser suprida por editores Markdown), mas o pior é não poder mais escrever pela web de qualquer computador.

### Simplificando

Depois de algum tempo descontente com esta situção, conheci algumas ferramentas que me pareceram muito interessantes:

1. [Jekyll Now](http://www.jekyllnow.com/)

2. [Prose.io](http://prose.io/)

O Jekyll Now é um projeto que facilita a configuração inicial de sites Jekyll a serem hospedados no Github Pages: é só dar um "fork" e começar a usar. Como o Github Pages suporta o Jekyll nativamente, é possível utilizar a própria interface do Github para escrever posts de qualquer lugar. E o Jekyll Now ainda trás suporte a Google Analytics e ao Disqus sem o uso de plugins, já que eles não são suportados pela hospedagem do Github. 

Já o Pose.io é uma interface de escrita de texto integrada ao Github. Com ele, é possível ter uma experiência bem próxima do que eu tinha no Wordpress, escrevendo posts diretamente no repositório Github do meu blog!

### Migração

Como o Octopress é feito sobre o Jekyll, a migração é muito simples. Basicamente tive que alterar os arquivos de configuração do Jekyll e copiar os arquivos Markdown de posts e páginas do antigo blog para o novo. Pronto! O blog já estava pronto para ir para o ar!

Ainda é muito cedo para dizer que esta configuração está ideal, mas a experiência de escrever este post já foi muito melhor! 

PS: Quem acompanha este blog via feed RSS ou e-mail, deve ter reparado um problema. Na tansição de uma plataforma para outra (isso também aconteceu quando migrei do Wordpress) o feed foi todo refeito e os leitores de RSS reconheceram todos os posts como novos. Peço desculpas pelo inconveniente e espero que isto não aconteça novamente :)
