---
published: true
layout: post
date: '2016-09-16 18:05:00 -0300'
comments: true
categories:
  - Dicas
tags:
  - livro
  - colaborativo
  - gitbook
  - widbook
  - wikibooks
---
Recentemente eu tive a necessidade de escrever uma apostila sobre teoria de ritmo. À princípio, apenas criei um documento texto no meu computador e fui escrevendo aos poucos. Mas, num determinado momento, pensei que este material teria mais utilidade disponível na internet (sob uma licensa livre) do que esquecido no meu HD. Então pesquisei alguns sites para eu publicar minha apostila online e selecionei alguns candidatos.

<!-- more -->

#### [Wikilivros](https://pt.wikibooks.org/)

O Wikilivros (ou Wikibooks, no original) é um braço da famosa Wikipédia, mas com o conteúdo organizado em formato de livros. Já existe um [livro de teoria musical](https://pt.wikibooks.org/wiki/Teoria_musical) incompleto (e aparentemente abandonado) e poderia tentar terminá-lo. No entanto, meu objetivo era bem mais simples do que criar um livro e já tinha um conteúdo já escrito numa estrutura totalmente diferente.

#### [Widbook](https://www.widbook.com/)

Um site um pouco mais adequado às minhas necessidades é o Widbook. É uma rede social para escrever e compartilhar livros digitais, oferecendo um ambiente colaborativo para leitura e escrita. No entanto, não existe nenhuma forma de disponibilizar o livro para download, o que era um requisito para mim. Aliás, pior do que isso: não existe nenhuma forma de você baixar o seu próprio livro! Ou seja, escreveu no Widbook, fica para sempre lá.

O Widbook parece ter um uso bastante amigável e possui alguns recursos interessantes (como recebimento de doações), mas para mim não faziam tanto sentido.

#### [Gitbook](https://www.gitbook.com/)

Finalmente encontrei (através de uma dica da [Espírito Livre](http://www.revista.espiritolivre.org/gitbook-uma-forma-simples-de-criar-livros-digitais/)) o Gitbook. Ele também oferece um ambiente colaborativo para leitura e escrita de livros digitais, mas, diferente do Widbook, converte o livro para diversos formatos (PDF, Kindle e ePub) que podem ser baixados, além de poder ser visualizado pela web.

Também não existe o problema do livro ficar preso dentro da plataforma. O Gitbook utiliza para guardar os livros um formato aberto ([Markdown](https://pt.wikipedia.org/wiki/Markdown)) e os salva num repositório [Git](https://pt.wikipedia.org/wiki/Git). Além da facilidade de acesso para poder ter uma cópia dos meus próprios livros, eu consigo editá-los mesmo se o Gitbook acabar algum dia.

### Gitbook na prática

![gitbook.png](/images/gitbook.png)

Comecei importando o documento texto que já tinha escrito antes e precisei de um tempo formatar o conteúdo para o Gitbook. Para editar, é possível utilizar o próprio site, mas ele oferece um aplicativo desktop que possui mais funções.

Uma das funcionalidade que achei mais interessantes é o uso de plugins e ele possui um [repositório](https://plugins.gitbook.com/) repleto deles! No meu caso, eu precisava adicionar partituras musicais na minha apostila, das quais poderia utilizar com imagens, mas seria um pouco trabalhoso. Então preferi [utilizar um plugin](https://plugins.gitbook.com/plugin/abc2svg) para gerar as partituras para mim.

Algo que pode ser interessante para os usuários mais técnicos, é a opção de colocar os "arquivos fonte" do livro num repositório no Github e abrir mais possibilidades de colaboração (issues, pull requests etc). Se você nem faz ideia do que seja Github, não se preocupe que o Gitbook utiliza por padrão um repositório próprio que você não precisa configurar.

No entanto, nem tudo são flores. O editor de texto visual se mostrou um tanto problemático, desformatando o texto diversas vezes após salvar o trabalho. Em determinados momentos, eu simplesmente desisti do editor visual e trabalhei direto com o código Markdown mesmo. Isso pode ser uma barreira para quem não tiver conhecimento técnico.

Além disso, se você utilizar um plugin numa determinada página do livro, necessariamente terá trabalhar direto com o Markdown nesta página, perdendo a facilidade do editor visual. Mas o que realmente achei inconveniente no uso de plugins é não ser possível visualizar o resultado do plugin através do editor. Ou seja, no meu caso, não era possível ver a partitura desenhada antes de enviar as atualizações para o Gitbook e gerar a nova versão do livro.

### Conclusão

Apesar dos problemas, o Gitbook se mostrou uma ferramenta muito poderosa e que atendeu muito bem às minhas necessidades. Para um usuário não técnico, acredito que ele não seja muito adequado, mas para mim, que sou desenvolvedor de software, trabalhar com Markdown não é um problema e as possibilidades que os plugins trazem são enormes!

Por fim, só me resta deixar o [link para o meu usuário no Gitbook](https://www.gitbook.com/@rcsilva83/) para você poder ver como minha singela apostila está ficando. Ainda pretendo reorganizar o conteúdo, melhorar alguns exemplos e testar alguns para escrever exercícios e incorporar música e vídeo.
