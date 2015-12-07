---
title: 'Software (livre) é Conhecimento (livre) &#8211; parte 1'
author: Rodrigo Carvalho
excerpt: Este artigo procura mostrar uma nova visão às pessoas de como elas enxergam o software. Software também é conhecimento e, como tal, deve ser livre para propiciar o desenvolvimento da humanidade.
layout: post
permalink: /software-livre-e-conhecimento-livre-parte-1/
comments: true
categories:
  - Liberdade
tags:
  - conhecimento livre
  - software livre
---
<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } -->Antes de mais nada, devo dizer que este artigo é uma preparação para a apresentação que irei fazer no 

<a href="http://gnugraf.org" target="_blank">II GNUGRAF</a> e é baseado na excelente palestra do professor Eurico Zimbres, da faculdade de Geologia da UERJ, grande ativista do software livre no Rio de Janeiro. Então segue o artigo e espero seus comentários a respeito, para que a palestra fique mais rica.

**O que é software?**

<p style="font-weight:normal;">
  Quando alguém fala em <em>software</em>, qual a primeira coisa que lhe vem a mente? A grande maioria das pessoas pensará em <span style="text-decoration:none;"><strong>algo útil</strong></span> para executar uma tarefa no computador. Desenvolvedores de software, poderão pensar também em como ele foi feito – no seu <strong><a href="http://pt.wikipedia.org/wiki/C%C3%B3digo_fonte">código-fonte</a></strong>. Vejamos então a definição provida pela Wikipédia:
</p>

> <p style="font-weight:normal;">
>   <em><strong>Software</strong></em> ou <strong>logiciário</strong> é uma sequência de instruções a serem seguidas e/ou executadas, na manipulação, redirecionamento ou modificação de um dado/informação ou acontecimento.
> </p>

Resumindo de uma forma bem simples, software é como se fosse uma “receita de bolo” escrito de forma que o computador entenda. Assim, o resultado final (o “algo útil” citado anteriormente) seria exatamente o “bolo” feito pelo computador. Veja um exemplo de programa escrito na linguagem C:

<pre style="font-weight:normal;padding-left:60px;">#include &lt;stdio.h&gt;
int main(void)
{
    int count;
    for(count=1;count&lt;=500;count++)
        printf("Conhecimento tem que ser livre!");
    return 0;
}</pre>

<p style="font-weight:normal;">
  Para você que não entende a linguagem, este programa escreve na tela do computador 500 vezes a frase &#8220;Conhecimento tem que ser livre!&#8221;. Melhor dizendo, este programa é uma &#8220;receita&#8221; que, ao ser lida pelo computador, diz a ele como escrever a frase 500 vezes. Obviamente, esta não é a única forma de se fazer isso! Você pode escrever em outra linguagem que o programador tenha mais fluência ou adicionar mais tempero (escrever o texto colorido) ou ainda gastando mais ingredientes (gastando mais memória para fazer a mesma coisa).
</p>

Agora vamos fazer uma pequena brincadeira &#8211; leia o seguinte texto, escrito em Alemão:

> Meiner lieber Seele, der vergangen is  
> So frueh aus dieses Leben, unzufrieden,  
> Ruehe in den Himmel ewig  
> Und lebe Ich hier auf dieser Erde immer traurig

<p style="font-weight:normal;">
  Se você é fluente em Alemão tanto quanto é na linguagem C, então a dúvida foi a mesma :) . Mas, se traduzirmos o texto para o português:
</p>

> Alma minha gentil, que te partiste  
> Tão cedo desta vida descontente,  
> Repousa lá no Céu eternamente,  
> E viva eu cá na terra sempre triste.  
> *Luís de Camões*

<p style="font-weight:normal;">
  Assim como a literatura, software e receitas de bolo são expressões de conhecimento. Uma receita de bolo foi feita com o conhecimento gerado de uma pessoa entendida sobre fabricação de bolos. Por isso, quando você vai à casa de um amigo e come um delicioso bolo feito por ele, você prontamente já pede a receita, afinal, com ela em mãos, você poderá fazê-lo e adaptá-lo ao seu gosto, deixando-o ainda melhor. Para o software é a mesma coisa! Desta forma, chegamos à nossa primeira conclusão:
</p>

<p style="font-weight:normal;padding-left:30px;">
  <strong>&#8220;Software é conhecimento!&#8221;</strong>
</p>

Nosso programa exemplo foi bastante simples, mas imagine a quantidade de conhecimento que existe num software como o <a href="http://www.gimp.org/" target="_blank">GIMP</a>, o [Inkscape][1], o [Ardour][2] e tantos outros!  O problema é que, infelizmente, o código-fonte de vários softwares não está disponível, restringindo todo o conhecimento a um pequeno grupo de pessoas. Para resolver esta situação que foi criado o software livre, mas isso será o assunto da [segunda parte do artigo][3]. Não deixe de ler!

 [1]: http://www.inkscape.org/
 [2]: http://ardour.org/
 [3]: http://www.rodrigocarvalho.blog.br/software-livre-e-conhecimento-livre-parte-2/
