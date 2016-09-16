---
published: false
layout: post
date: '2016-07-19 23:00:00 -0300'
comments: true
categories:
  - Dicas
tags:
  - livro
  - colaborativo
  - gitbook
  - widbook
---
## Livros colaborativos com GitBook

Recentemente eu tive a necessidade de escrever uma apostila sobre teoria de ritmo. À princípio, apenas criei um documento texto que fui escrevendo aos poucos, mas, num determinado momento, pensei que este material teria mais utilidade disponível na internet (com uma licensa livre) do que esquecido no meu HD. Então pesquisei alguns sites candidatos para eu publicar minha apostila e selecionei alguns candidatos.

#### [Wikilivros](https://pt.wikibooks.org/)

O Wikilivros (ou Wikibooks, no original) é um braço da famosa Wikipédia, mas com o conteúdo organizado em formato de livros. Já existe um [livro de teoria musical](https://pt.wikibooks.org/wiki/Teoria_musical) incompleto (e aparentemente abandonado) e poderia tentar terminá-lo. No entanto, meu objetivo era bem mais simples e já tinha um conteúdo já escrito numa formatação totalmente diferente.

#### [Widbook](https://www.widbook.com/)

Um site um pouco mais adequado às minhas necessidades é o Widbook. Ele é uma rede social para escrever e compartilhar livros digitais, oferecendo um ambiente online para escrita. No entanto, {a única forma de colaboração dele é via comentários e} não existe nenhuma forma de disponibilidade o livro para download. Aliás, pior do que isso: não existe nenhuma forma de você baixar o seu próprio livro! Ou seja, escreveu no Widbook, não é possível tirar de lá. No entanto o Widbook possui alguns recursos interessantes, como recebimento de doações, que para mim não faziam muito sentido.

#### [Gitbook](https://www.gitbook.com/)

Finalmente encontrei (através de uma dica da [Espírito Livre](http://www.revista.espiritolivre.org/gitbook-uma-forma-simples-de-criar-livros-digitais/)) o Gitbook. Diferente do Widbook, um livro escrivo no Gitbook pode ser baixado em diversos formatos (PDF, Kindle e ePub), além de poder ser visualizado pela web. Também não existe o problema do livro ficar preso dentro da plataforma, pois el fica salvo num num formato aberto ([Markdown](https://pt.wikipedia.org/wiki/Markdown)) num repositório [Git](https://pt.wikipedia.org/wiki/Git). As formas de colaboração também são maiores, pois é possível fazer comentários dentro do próprio livro, fazer comentário gerais (chamados "discussões") e, para os mais técnicos, sempre é possível deixar o livro no [Github](https://pt.wikipedia.org/wiki/GitHub) e receber pull requests!

### Gitbook na prática

Comecei importando o documento texto que já tinha escrito antes para o Gitbook e precisei de um tempo formatar o conteúdo melhor. Para editar, é possível utilizar o próprio site, mas ele oferece um aplicativo desktop que possui mais funções.

Uma das funcionalidade que achei mais interessantes é o uso de plugins e ele possui um [repositório](https://plugins.gitbook.com/) repleto deles! No meu caso, eu precisava adicionar partituras musicais na minha apostila, das quais poderia utilizar com imagens, mas seria um pouco trabalhoso. Então preferi [utilizar um plugin](https://plugins.gitbook.com/plugin/abc2svg) para gerar as partituras para mim.

Algo que já tinha adiantado antes, e que pode ser interessante para os usuários mais técnicos, é a opção de colocar os "arquivos fonte" do livro num repositório no Github e abrir mais possibilidades de colaboração. Se você nem faz ideia do que seja Github, não se preocupe que o Gitbook utiliza por padrão um repositório dele próprio que você não precisa configurar nada.

No entanto, nem tudo são flores. O editor de texto visual se mostrou um tanto problemático, desformatando o texto diversas vezes após salvar o trabalho. Em determinados momentos, eu simplesmente desisti do editor visual e trabalhei direto com o código Markdown mesmo. Isso pode ser uma barreira para quem não tiver conhecimento técnico.

Além disso, se você utilizar um plugin numa determinada página do livro, necessariamente terá que abrir mão do editor de texto visual nesta página e trabalhar direto com o Markdown. Mas o que realmente achei inconveniente no uso de plugins é ser possível visualizar o resultado do plugin pelo editor, ou seja, no meu caso, não era possível a partitura antes de enviar as atualizações para o Gitbook e gerar a nova versão do livro.

### Conclusão

Apesar dos problemas, o Gitbook se mostrou uma ferramenta muito poderosa e que atendeu muito bem aos meus requisitos. Para um usuário não técnico, acredito que ele não seja muito adequado, mas para mim, que sou desenvolvedor de software, trabalhar com Markdown não é um problema. As possibilidades que os plugins trazem são enormes!

Por fim, só me resta deixar o [link para o meu usuário no Gitbook](https://www.gitbook.com/@rcsilva83/) para você poder ver como minha singela apostila está ficando. Ainda pretendo reorganizá-la de uma forma melhor, melhorar alguns exemplos e testar alguns para escrever exercícios e incorporar música e vídeo.
