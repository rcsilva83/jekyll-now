---
title: 'WebM: Fim do impasse do HTML5?'
author: Rodrigo Carvalho
layout: post
permalink: /webm-fim-do-impasse-do-html5/
comments: true
categories:
  - Liberdade
  - Tecnologia
tags:
  - codec
  - google
  - html5
  - livre
  - mozilla
  - web2.0
  - webm
---
<p style="text-align: justify;">
  Eis que na semana que começou com a <a href="http://whiplash.net/materias/news_863/107949-dio.html?utm_source=feedburner&utm_medium=feed&utm_campaign=Feed%3A+feedburner%2FiSMr+%28WHIPLASH.NET+-+Rock+e+Heavy+Metal%29&utm_content=Google+Reader" target="_blank">perda de um grande ídolo</a>, temos uma ótima notícia: a Google <a href="http://br-linux.org/2010/webm-google-lanca-formato-de-video-aberto-para-web/" target="_blank">anuncia o lançamento</a> de um codec de vídeos livre para ser utilizado na web! Este é um grande passo na direção de uma web mais aberta, portável e acessível.
</p>

<p style="text-align: justify;">
  Se você está pensando &#8220;tá, mas e o que isto tem a ver comigo?&#8221;, a reposta simples é TUDO! Isto irá afetar todas as pessoas que acessa a internet atualmente (o que significa quase todas as pessoas do mundo) e irei explicar o porquê agora.
</p>

<p style="text-align: justify;">
  <strong>Web2.0 e o Flash Player<br /> </strong>
</p>

<p style="text-align: justify;">
  Algum tempo atrás, criaram uma palavrinha para denotar uma mudança brusca que estava acontecendo na Internet. As pessoas não estavam apenas acessando web sites quase estáticos apenas para obter informação. Agora elas estavam interagindo através de redes sociais, criando conteúdo em blogs e fotologs, distribuindo e assistindo vídeos e músicas etc. Era a chegada de uma nova era na grande rede: a web2.0.
</p>

<p style="text-align: justify;">
  Todo este movimento veio puxado por sites como Orkut (aqui no Brasil), Blogger, YouTube, Flickr, dentre outros. No caso particular do YouTube, não havia meios de executar vídeos diretamente pelo navegador, a não ser apelando para o uso de plugins. Eles então escolheram o Adobe Flash Player como plataforma de execução de vídeos via <a href="http://pt.wikipedia.org/wiki/Streaming" target="_blank"><em>streaming</em></a>.
</p>

<p style="text-align: justify;">
  O Flash Player está presente na web desde o seus primórdios. Mas com a web2.0 ele (antes restrito a <em>banners</em> em sites, pequenas animações ou àqueles pesados sites ricos em recursos gráficos e navegação precária) passou a ser peça fundamental para a distribuição de conteúdo multimídia. Mas isto se tornou um grande problema para o avanço da web por alguns motivos:
</p>

<ol style="text-align: justify;">
  <li>
    É proprietário e suas melhorias são dependentes da vontade da Adobe &#8211; alguns grupos tentaram criar implementações livres do plugin, mas elas nunca chegaram ao ponto de poderem substituir o original;
  </li>
  <li>
    Sites como YouTube não funcionavam bem em plataformas pouco suportadas pelo software (como Linux antigamente) e ninguém podia melhorar isto além da Adobe (problema acima);
  </li>
  <li>
    Aparelhos móveis, como smartphones, tiveram têm problemas para suportar a tecnologia e com o consumo de bateria (Steve Jobs, da Apple, <a href="http://meiobit.com/65338/steve-jobs-decreta-o-fim-do-flash/" target="_blank">falou sobre isto há pouco tempo</a>);
  </li>
  <li>
    Problemas comerciais com empresas que não querem ficar dependentes da Adobe (Steve Jobs também falou sobre isto).
  </li>
</ol>

<p style="text-align: justify;">
  <strong>HTML5 e o impasse</strong>
</p>

<p style="text-align: justify;">
  Foi então que a <a href="http://pt.wikipedia.org/wiki/W3C" target="_blank">W3C</a>, consórcio de empresas que criam e mantém os padrões abertos que todos seguem (menos a Microsoft no Internet Explorer&#8230;) para que a web seja aberta e interoperável, percebeu que era hora dos padrões evoluírem para acompanhar toda esta mudança. O carro chefe desta mudança seria a atualização do principal padrão utilizado para criar websites: o <a href="http://pt.wikipedia.org/wiki/HTML" target="_blank">HTML</a>. Com a versão 5, o sites poderiam utilizar vários recursos avançados, como por exemplo execução de áudio e vídeo, direto no navegador sem depender de plugins externos (<a href="http://idgnow.uol.com.br/internet/2009/06/16/html-5-conheca-a-linguagem-que-vai-revolucionar-sua-navegacao-na-web/" target="_blank">saiba mais sobre HTML5</a>).
</p>

<p style="text-align: justify;">
  Tudo estava muito bom até que se chegou na discussão do <a href="http://pt.wikipedia.org/wiki/Codec" target="_blank">codec</a> de vídeo a ser padronizado. De um lado Ogg Theora: livre e gratuito para qualquer tipo de uso, mas pouco difundido e com possíveis problemas de patentes. Do outro o H.264: proprietário e pago, mas amplamente utilizado (inclusive dentro do Flash), suportado por hardware (o que torna mais rápido e com baixo consumo de recursos) e tecnicamente (ou teoricamente) melhor. Empresas proprietárias, como Microsoft e Apple, defendendo o H.264. Empresas e fundações pró-software livre, como Mozilla e FSF, defendendo o Theora. Google em cima do muro suportando ambos no seu navegador Chrome.
</p>

<p style="text-align: justify;">
  Então a FSF teve uma ótima ideia e publicou uma <a href="http://www.fsf.org/blogs/community/google-free-on2-vp8-for-youtube/" target="_blank">carta aberta</a> à Google, pedindo que ela abrisse o código do VP8: um codec que, após uma aquisição, havia se tornado de sua propriedade. Este seria um candidato perfeito para acabar com a discussão já que ele não teria problemas de patentes e seria tecnicamente melhor que o H.264.
</p>

<p style="text-align: justify;">
  <strong>WebM: em rumo à &#8220;<em>open web</em>&#8221;<br /> </strong>
</p>

<p style="text-align: justify;">
  Chegamos no presente e no anúncio do qual mencionei no início do post. O WebM utiliza para codificação de vídeo justamente o VP8 (conforme pedido pela FSF) e realmente acho que o impasse dos codecs chegará ao fim, já que a Microsoft já <a href="http://info.abril.com.br/noticias/tecnologia-pessoal/microsoft-deve-suportar-webm-do-google-20052010-6.shl" target="_blank">anunciou</a> que suportará o WebM e acho que a Apple não vai muito à frente sozinha.
</p>

<p style="text-align: justify;">
  Espero que eu tenha conseguido mostrar como este anúncio é um grande passo na direção certa e como isto abrirá as portas para uma web com vídeo de alta qualidade, alto desempenho e utilizando padrões totalmente abertos, sem restrições de uso etc.
</p>

<p style="text-align: justify;">
  <em><strong>PS:</strong> Você pode fazer sua parte em favor de uma web mais aberta utilizando navegadores que sejam aderentes aos padrões internacionais da W3C, como o <a href="http://www.mozilla.com/pt-BR/firefox/" target="_blank">Firefox</a>, <a href="http://www.google.com/chrome" target="_blank">Google Chrome</a>, <a href="http://www.opera.com/" target="_blank">Opera</a> e <a href="http://www.apple.com/safari/" target="_blank">Safari</a>. Dizem que o Internet Explorer 8 está totalmente aderente, mas não tenho certeza (o IE6 e 7 com certeza não são). De qualquer modo eu recomendo o Firefox ou o Chrome, por serem softwares livres.</em>
</p>
