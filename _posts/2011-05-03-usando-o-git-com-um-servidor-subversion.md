---
title: Usando o Git com um servidor Subversion
author: Rodrigo Carvalho
layout: post
permalink: /usando-o-git-com-um-servidor-subversion/
Views:
  - 18
comments: true
categories:
  - Tecnologia
tags:
  - console2
  - cygwin
  - git
  - git-svn
  - svn
---
No meu [último artigo][1], dei uma dica de como aprender de forma rápida a usar o maravilhoso sistema de controle de versão (SCM) <a title="Git" href="http://pt.wikipedia.org/wiki/Git" target="_blank">Git</a>. Mas o fato é que atualmente o <a title="Subversion" href="http://pt.wikipedia.org/wiki/Subversion" target="_blank">Subversion</a> (ou SVN) ainda é o SCM mais utilizado no mundo e muitas empresas ainda não migraram para o Git. Mas nem por isso você precisa se desanimar, pois, se quiser, você pode utilizar o Git hoje <span style="text-decoration: line-through;">sem ninguém saber</span> com um servidor Subversion!

O próprio Git fornece uma ferramenta milagrosa chamada &#8220;git-svn&#8221;. O que o git-svn faz é o seguinte:

*   Clona um repositório Subversion para sua máquina, como faria o Git para qualquer repositório remoto;
*   Recupera os branches e tags do Subversion e configura no Git local;
*   Faz um &#8220;fetch&#8221; das modificações do repositório Subversion com o repositório Git;
*   Faz o &#8220;push&#8221; das modificações locais para repositório Subversion;

Resumidamente, o git-svn faz com o Subversion tudo o que o Git puro faria com um repositório remoto. No entanto, os comandos são um pouco diferentes, mas a documentação pode ser encontrada no <a title="&quot;Man page&quot; do git-svn" href="http://www.kernel.org/pub/software/scm/git/docs/git-svn.html" target="_blank">&#8220;man page&#8221; do git-svn</a>. Infelizmente a documentação ainda está um pouco aquém do esperado, mas a seguir vou dar algumas dicas de resolução de problemas pelos quais passei.

**Problema 1: Git não consegue clonar o repositório SVN**

O primeiro problema pelo qual eu passei foi um erro ao rodar o comando &#8220;git svn clone&#8221;. O problema é que o histórico do meu projeto no Subversion estava muito grande e o servidor não deu conta do processamento feito pelo git-svn. A solução é não clonar todo o histórico do repositório utilizando o parâmetro &#8220;-r&#8221;. Um exemplo seria:

<pre>git svn clone -r 3000:HEAD http://rodrigocarvalho.blog.br/svn/
</pre>

Neste exemplo, utilizamos o parâmetro &#8220;-r&#8221; para clonar o histórico a partir da revisão 3000 do SVN até a útima revisão (HEAD). Não existe uma fórmula para escolher a revisão inicial, sendo que consegui encontrar um valor que funcionou para mim na tentativa e erro.

**Problema 2: Os branches do SVN não foram para o Git**

Após feito o clone, você poderá se dar falta dos branches que tinha no SVN. Caso a estrutura do seu repositório Subversion seja a padrão (trunk, branches, tags), simplesmente utilize o parâmetro &#8220;-s&#8221;. O exemplo acima ficaria assim:

<pre>git svn clone -s -r 3000:HEAD http://rodrigocarvalho.blog.br/svn/</pre>

Desta forma ele vai criar no Git os branches que existiam no seu repositório SVN.

No entanto, se a estrutura do seu repositório não for a padrão, você terá que utilizar os parâmentros &#8220;&#8211;trunk&#8221; ou &#8220;-T&#8221;, &#8220;&#8211;tags&#8221; ou &#8220;-t&#8221; e &#8220;&#8211;branches&#8221; ou &#8220;-b&#8221;. Um exemplo seria:

<pre>git svn clone --trunk=trunk/projetox --tags=tags/projetox \
   --branches=branches/projetox -r 3000:HEAD http://rodrigocarvalho.blog.br/svn/</pre>

**Bonus****: Git no Windows**

Normalmente, as pessoas trabalham com Git pela linha de comando mesmo. Se você utilizar um sistema UNIX (Linux, OSX, *BSD), você terá à sua disposição o bash, que é uma excelente ferramenta modo texto. Adicione o pacote &#8220;bash-completion&#8221;, aí que o bash vai te facilitar ainda mais a vida!

Infelimente, sou obrigado a trabalhar todos os dias na empresa com no Windows, sistema operacional que tem um console textual muito fraco e que ele não te ajuda em nada&#8230; Mas é para isto que existe o <a title="Cygwin" href="http://www.cygwin.com/" target="_blank">cygwin</a>, que emula um ambiente UNIX no Windows! Portanto, ao utilizar Git no Windows, eu recomendo fortemente o uso do Cygwin.

Sua instalação é muito tranquila e pode ser feita mesmo em computadores onde não se tenha permissões de administrador. É só escolher uma pasta de instalação (uma onde se tenha permissão de escrita, por favor), esperar ele baixar a lista de pacotes disponíveis da Internet (sim, igualzinho ao apt, yum etc \o/) e selecionar para instalar todas as ferramentas que considerar úteis. No nosso caso, você vai querer selecionar pelo menos estas:

1.  &#8220;git&#8221;;
2.  &#8220;git-completion&#8221; (que é o pacote do bash-completion para os comandos do Git);
3.  &#8220;git-svn&#8221;.

Espere a instalação baixar tudo que terá um ambiente Git montado no Windows!

Para deixar ainda melhor, eu recomendo o uso da ferramenta <a title="Console2" href="http://sourceforge.net/projects/console/" target="_blank">Console2</a> que é melhor do que a janela de linha de comando do Windows, pois oferece abas e possibilidade de redimencionar a janela. Sua instalação também é muito fácil e, após instalado, você deve configurar para ele rodar o Cygwin ao invés do terminal do Windows. Para fazê-lo, vá em &#8220;Edit&#8221; -> &#8220;Settings&#8221;.  No campo &#8220;Shell&#8221; da aba &#8220;Console&#8221; escreva:

<pre>&lt;pasta_do_cygwin&gt;\bin\bash.exe --login -i</pre>

Onde &#8220;<pasta\_do\_cywin>&#8221; deve ser substituído pelo caminho onde você instalou o Cygwin.

Pronto você terá um ambiente Git muito mais produtivo do que antes!

 [1]: aprenda-git-e-github-de-forma-rapida
