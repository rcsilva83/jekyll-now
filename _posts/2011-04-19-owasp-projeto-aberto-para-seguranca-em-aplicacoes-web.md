---
title: 'OWASP: Projeto Aberto para segurança em aplicações web'
author: Rodrigo Carvalho
layout: post
permalink: /owasp-projeto-aberto-para-seguranca-em-aplicacoes-web/
Views:
  - 105
comments: true
categories:
  - Liberdade
  - Tecnologia
tags:
  - antisamy
  - appsec
  - owasp
  - projeto
  - segurança
  - top 10
  - web
  - webgoat
  - webscarab
---
***Este artigo foi publicado na <a title="Edição 24 da Revista Espírito Livre" href="http://www.revista.espiritolivre.org/?p=921" target="_blank">edição 24</a> da <a title="Revista Espírito Livre" href="http://www.revista.espiritolivre.org/" target="_blank">Revista Espírito Livre</a>.***

*** ***A [OWASP][1] (Open Web Application Security Project ou Projeto Aberto de Segurança em Aplicações Web) é uma organização mundial sem fins lucrativos focada em melhorar a segurança de softwares, em especial os softwares baseados na web. Sua missão é fazer com que a segurança das aplicações seja visível, de forma que pessoas e organizações possam fazer decisões conscientes a respeito dos verdadeiros riscos de segurança das aplicações.

Todos são livres para participar da organização e de sua comunidade, e esta caraterística atraiu a atenção de diversas empresas, tanto as que trabalham com software livre, como a Fundação Mozilla, quanto as empresas comerciais e proprietárias, como Microsoft, Adobe e Oracle. Além disso, diversas universidades americanas são membros da organização.

Outra característica é que ela tenta se organizar de uma maneira descentralizada através dos chamados “capítulos locais”. Estes “capítulos” são grupos locais formado por pessoas interessadas em ajudar a OWASP a atingir seus objetivos fomentando localmente os princípios e boas práticas pregadas pela organização. O Brasil atualmente conta com dois capítulos: Brasília e São Paulo. Adicionalmente, como forma de divulgação, são promovidos diversos eventos no mundo todo, inclusive no Brasil que, em 2010, teve sua segunda edição do [OWASP AppSec][2].

Para alcançar seu objetivo, a OWASP desenvolve diversos projetos, tanto de software quanto de documentação, e todos eles são licenciados sob licensas livres, tornando o acesso a eles muito fácil e democrático. A seguir detalharei melhor alguns dos principais projetos.

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		H2 { margin-bottom: 0.21cm } 		H2.western { font-family: "Arial", sans-serif; font-size: 14pt; font-style: italic } 		H2.cjk { font-size: 14pt; font-style: italic } 		H2.ctl { font-family: "Lohit Hindi"; font-size: 14pt; font-style: italic } -->

## Top 10

O Top 10 é uma lista dos 10 ataques a segurança de aplicações web mais críticos existentes. Este é, provavelmente, o projeto mais famoso da OWASP e é atualizado frequentemente, sendo que a última versão é deste ano (2010) com a seguinte lista de ataques:

1.  **Injeção:** ocorre quando um dado não confiável é enviado a um interpretador como parte de um comando ou consulta. O tipo de injeção mais famoso é o *SQL Injection* que permite que o atacante execute quaisquer comandos SQL no banco de dados da aplicação vulnerável.
2.  **Cross-site Scripting (XSS):** ocorre quando uma aplicação obtém um dado não confiável e envia para um navegador web sem correta validação e escapamento. Permite que um atacante execute quaisquer scripts (normalmente Javascript) no navegador da vítima.
3.  **Autenticação e gerenciamento de sessão quebrados:** ocorre quando a autenticação e o gerenciamento de sessão da aplicação não são feitos de forma correta, permitindo que o atacante comprometa senhas, chaves, sessões web, assumindo a identidade da vítima.
4.  **Referência direta insegura a objeto:** ocorre quando o desenvolvedor expõe uma referência a um objeto interno, como um arquivo, diretório ou chave de banco de dados. Sem uma checagem de controle de acesso ou outra proteção, atacantes podem manipular estas referências para acessar dados não autorizados, como arquivos confidenciais.
5.  **Cross-site Request Forgery (CSRF):** força o navegador web da vítima logada numa aplicação a enviar um *request* forjado, incluindo o *cookie* de sessão da vítima e qualquer outra informação de autenticação incluída automaticamente, para uma aplicação vulnerável. Isto permite que o atacante force o navegador da vítima a gerar *requests *que a aplicação vulnerável pensa que são vegítimos.
6.  **Problema com configurações de segurança:** boa segurança requer ter uma configuração de segurança bem definida e implantada para a aplicação, *frameworks*, servidor de aplicação, servidor web, servidor de banco de dados e plataforma. Todas estas configurações devem ser definidas, implementadas e mantidas quando não são liberadas com configurações padrão seguras. Isto inclui manter todo o software atualizado, incluindo todas as bibliotecas utilizadas pelas aplicações.
7.  **Armazenamento criptográfico inseguro:** ocorre quando a aplicação protege incorretamente seus dados sensíveis (como números de cartões de crédito e credenciais de autenticação) com criptografia ou *hash *adequados. Os atacantes podem roubar ou modificar estes dados para conduzir roubo de identidade, fraude de cartão de crédito ou outros crimes.
8.  **Falha ao restringir acesso a URL:** ocorre quando a aplicação restringe o acesso a uma página reservada apenas pela interface, ou seja, não exibindo os *links *para ela. Um atacante pode obter o link para esta página e acessá-la diretamente.
9.  **Proteção em nível de transporte insuficiente:** ocorre quando uma aplicação falha ao autenticar, encriptar e proteger a confidencialidade e integridade do tráfego de rede sensível. Isto pode acontecer com o uso de algorítmos de criptografia fracos, usam certificados digitais expirados ou inválidos ou não os usam corretamente.
10. ***Redirects *****e *****forwards *****não validados:** ocorre quando uma aplicação redireciona ou encaminha um usuário a outras páginas ou sites e usam dados não confiáveis para determinar a página de destino. Sem validação apropriada, atacantes podem redirecionar vítimas para sites de *phishing *ou *malware *ou usam *forwards *para acessar páginas não autorizadas.

Além de ser um poderoso documento de conscientização, para cada uma das vulnerabilidades listadas são ensinadas formas de evitar que sua aplicação fique vulnerável. Vale muito a pena ler as explicações mais aprofundadas de cada vulnerabilidade e, principalmente, nas formas de prevenção.

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		H2 { margin-bottom: 0.21cm } 		H2.western { font-family: "Arial", sans-serif; font-size: 14pt; font-style: italic } 		H2.cjk { font-size: 14pt; font-style: italic } 		H2.ctl { font-family: "Lohit Hindi"; font-size: 14pt; font-style: italic } -->

## WebGoat

O WebGoat é uma aplicação web feita em Java com diversas falhas de segurança feita para ensinar lições de segurança em aplicações web. Em cada lição, o usuário deve demonstrar que entende um problema de segurança explorando a vulnerabilidade do WebGoat. Por exemplo, uma das lições o usuário precisa fazer um ataque de *SQL Injection *para roubar números falsos de cartões de crédito. A aplicação é um ambiente de aprendizado realístico e provê aos usuários dicas e código que explicam cada lição.

[<img class="aligncenter size-medium wp-image-572" title="webgoat" src="/wp-content/uploads/2011/04/webgoat-300x252.png" alt="" width="300" height="252" />][3]

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		H2 { margin-bottom: 0.21cm } 		H2.western { font-family: "Arial", sans-serif; font-size: 14pt; font-style: italic } 		H2.cjk { font-size: 14pt; font-style: italic } 		H2.ctl { font-family: "Lohit Hindi"; font-size: 14pt; font-style: italic } -->

## WebScarab

O WebScarab é um aplicativo desktop feito em Java (portanto é multiplataforma) utilizado como um proxy web. Após configurar seu navegador para utilizar a porta aberta pelo WebScarab como proxy HTTP, você pode utilizá-lo para analisar todo o tráfego entre o navegador e a aplicação que está sendo acessada, bem como alterar o conteúdo do *request* enviado originalmente. Assim, ele pode ser utilizado para identificar falhas de segurança em sua aplicação web sem alterar a interface de usuário da mesma.

[<img class="aligncenter size-medium wp-image-573" title="webscarab" src="/wp-content/uploads/2011/04/webscarab-300x133.png" alt="" width="300" height="133" />][4]

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		H2 { margin-bottom: 0.21cm } 		H2.western { font-family: "Arial", sans-serif; font-size: 14pt; font-style: italic } 		H2.cjk { font-size: 14pt; font-style: italic } 		H2.ctl { font-family: "Lohit Hindi"; font-size: 14pt; font-style: italic } -->

## ESAPI

A ESAPI é uma API de controle de segurança que torna fácil aos desenvolvedores escreverem aplicações com baixo risco. Disponível para as plataformas como Java, .NET, Python e PHP, a ESAPI tem o seguinte design básico para todas as implementações:

*   Ter um conjunto de interfaces de controle de segurança;
*   Ter uma implementação de referência para cada controle;
*   Poder, opcionalmente, utilizar sua própria implementação para cada controle;

O diagrama abaixo mostra todos os módulos os controles contemplados pela ESAPI.

[<img class="aligncenter size-medium wp-image-574" title="esapi" src="/wp-content/uploads/2011/04/esapi-300x155.png" alt="" width="300" height="155" />][5]

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		H2 { margin-bottom: 0.21cm } 		H2.western { font-family: "Arial", sans-serif; font-size: 14pt; font-style: italic } 		H2.cjk { font-size: 14pt; font-style: italic } 		H2.ctl { font-family: "Lohit Hindi"; font-size: 14pt; font-style: italic } -->

## AntiSamy

O AntiSamy é uma API utilizada para evitar que código HTML e CSS malicioso afete sua aplicação e evitando, assim, um ataque de XSS. A API faz isso fazendo uma validação do HTML/CSS recebido do cliente e o valida através de uma *whitelist*, que é uma lista de elementos HTML/CSS seguros de serem aceitos pela aplicação. Ele tem suporte a mensagens de erro amigáveis e suas políticas de validação podem ser personalizadas.

## Guias

Além de software, a OWASP elabora uma rica documentação sobre o assunto e uma parte desta documentação é composta por três importantes guias:

1.  **Guia de desenvolvimento:** provê um guia prático com exemplos de código em Java, .NET e PHP, cobrindo um extenso leque de problemas de segurança;
2.  **Guia de revisão de código: **objetiva guiar o revisor de código na busca por vulnerabilidades da aplicação;
3.  **Guia de teste:** objetiva criar melhores práticas para testes de penetração em aplicações web;

## Conclusão

Como vimos ao longo deste artigo, a OWASP é uma organização bastante ativa e que desenvolve diversos projetos importantes para a melhoria na segurança das aplicações web. O melhor de tudo é que estes projetos são todos liberados sob licenças livres, que facilitam sua adoção e implantação inclusive em empresas.

Além disso, por sua natureza aberta, qualquer pessoa é livre para virar um contribuidor de melhorias e correções para os produtos. Existem projetos muito interessantes ainda em desenvolvimento e que podem ser um local divertido para aprender novas tecnologias e contribuir com o software livre.

Que fique claro, no entanto, que o que eu apresentei foi apenas uma pequena parte do que a OWASP desenvolve. Recomendo fortemente a todos os desenvolvedores de aplicações web que naveguem pelo site e descubram tudo que ela tem a oferecer.

**Referências:**

<!-- 		@page { margin: 2cm } 		P { margin-bottom: 0.21cm } 		A:link { so-language: zxx } -->

*   **Site da OWASP:** [http://www.owasp.org][6]
*   **OWASP AppSec Brasil 2010:** [http://www.owasp.org/index.php/AppSec\_Brasil\_2010_(pt-br)][2]

**Créditos:** Grande parte do conteúdo do artigo foi baseado no material do próprio site da OWASP.

&nbsp;

 [1]: http://owasp.org/
 [2]: http://www.owasp.org/index.php/AppSec_Brasil_2010_(pt-br)
 [3]: http://www.rodrigocarvalho.blog.br/wp-content/uploads/2011/04/webgoat.png
 [4]: http://www.rodrigocarvalho.blog.br/wp-content/uploads/2011/04/webscarab.png
 [5]: http://www.rodrigocarvalho.blog.br/wp-content/uploads/2011/04/esapi.png
 [6]: http://www.owasp.org/
