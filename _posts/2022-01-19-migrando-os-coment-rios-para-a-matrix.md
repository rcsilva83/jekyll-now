---
author: Rodrigo Carvalho
layout: post
comments: true
published: false
title: Migrando os comentários para a Matrix
categories:
  - Tecnologia
  - Privacidade
tags:
  - disqus
  - cactus-comments
  - matrix
---
![Disqus para Cactus.png]({{site.baseurl}}/images/Disqus para Cactus.png)
<sup><sub>Crédito: ![matrix](https://live.staticflickr.com/3070/2564208746_df3c98169e_b.jpg)["matrix"](https://www.flickr.com/photos/21936312@N08/2564208746) by [Gamaliel E. M.](https://www.flickr.com/photos/21936312@N08) is licensed under [CC BY-NC 2.0](https://creativecommons.org/licenses/by-nc/2.0/?ref=openverse&atype=html)[![](https://search.creativecommons.org/static/img/cc_icon.svg?image_id=ef2a8579-e8fb-4f90-81e8-b2a408fbea72)![](https://search.creativecommons.org/static/img/cc-by_icon.svg)![](https://search.creativecommons.org/static/img/cc-nc_icon.svg)](https://creativecommons.org/licenses/by-nc/2.0/?ref=openverse&atype=html)</sub></sup>

Na [última postagem](medidas-de-privacidade-que-nao-vao-dificultar-sua-vida) do blog, comecei uma série sobre privacidade online. No entanto, após publicar o texto, percebi algo bastante incoerente com aquele tema: o blog usava o [Disqus](https://disqus.com/) como sistema de comentários! Enquanto este sistema é muito popular e fácil de se usar, ele rastreia seus usuários. Sendo assim, precisava encontrar alguma alternativa a ele.

<!-- more -->

Encontrei uma lista muito legal de [opções de sistemas de comentários para sites estáticos](https://cloudcannon.com/community/jamstack-ecosystem/commenting/) (que é o caso deste) e foquei em 4 características:
1. Centrado em privacidade
1. Opção _hosted_, ou seja, não exigisse que eu tivesse que manter uma instalação da ferramenta num servidor
1. Gratuito para pouca demanda
1. Preferenciamente [_open source_](https://pt.wikipedia.org/wiki/C%C3%B3digo_aberto)

Após filtrar por estas características, reduzi a lista para 2 opções: [Cactus](https://cactus.chat/) e [Cusdis](https://cusdis.com/). Acabei ficando com a primeira, que oferece  uma solução menos acoplada por ser baseada na [Matrix](https://matrix.org/).

A Matrix é uma rede aberta para comunicação descentralizada, totalmente baseada em padrões abertos e uma das peças mais importantes do movimento de [descentralização da web](https://pt.wikipedia.org/wiki/Descentraliza%C3%A7%C3%A3o_da_Web). Este movimento também tem muita relação com privacidade online, pois objetiva a eliminação dos grandes silos de informação, como Google, Facebook entre outros. Se o assunto descentralização da web te interessou, recomendo a newsletter [Redecentralize Digest](https://redecentralize.org/redigest/).

Sendo assim, a escolha do Cactus me pareceu a mais interessante e sua configuração foi muito simples e rápida. Você já pode testar agora a nova sessão de comentários e, desta forma, se sentir como [Neo](https://duckduckgo.com/?q=neo+matrix&atb=v211-1&iax=images&ia=images) navegando pela Matrix ;)


