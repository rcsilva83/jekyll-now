---
published: false
---

## Facilitando o uso do Github Pages

Há pouco mais de 1 ano resolvi migrar o meu blog do Wordpress para o Octopress. Estava muito satisfeito com o Wordpress, mas não achava que fazia mais sentido eu pagar uma hospedagem para o blog. O Octopress me possibilitou o usoda hospedagem gratuita do Github Pages além de outros benefícios como:
1. Reduziu drásticamente o tempo de carregamento das páginas;
2. Sistema de templates muito mais simples, facilitando ajustes no tema visual;
3. Maior segurança, eliminando a preocupação de manter o sistema constantemente atualizado;

Mas, é claro, que nem tudo são flores e eu já sabia disso. O uso do Wordpress é muito mais fácil e o Octopress acaba sendo um pouco burocrático na hora de escrever um novo post. Não é à toa que tenho escrito muito menos nos últimos tempos! Para escrever um novo post no Octopress deve-se criar um arquivo formatado em Markdown no computador onde está o "código-fonte" do blog e as ferramentas de geração do Octopress configuradas (Ruby com algumas gems). De cara, já perdemos a edição visual (que pode ser suprida por editores Markdown), mas o pior é não poder mais escrever pela web de qualquer computador.

### Simplificando

Depois de algum tempo descontente com esta situção, conheci algumas ferramentas que me pareceram muito interessantes:
1. Jekyll Now
2. Prose.io

O Jekyll Now é um projeto que facilita a configuração inicial de sites Jekyll a serem hospedados no Github Pages: é só dar um "fork" e começar a usar. Como o Github Pages suporta o Jekyll nativamente, é possível utilizar a própria interface do Github para escrever posts de qualquer lugar. E o Jekyll Now ainda trás suporte a Google Analytics e ao Disqus sem o uso de plugins, o que não é suportado pela hospedagem do Github. 

Já o Pose.io é uma interface de escrita de texto integrada ao Github. Com ele, é possível ter uma experiência bem próxima do que eu tinha no Wordpress, escrevendo posts diretamente no repositório Github do meu blog!

### Migração

A migração do Octopress para o Jekyll é bastante simples, já que o Octopress é feito sobre o Jekyll. Tive que basicamente alterar os arquivos de configuração do Jekyll e copiar os arquivos Markdown de posts e páginas do antigo blog para o novo. Pronto! O blog já estava pronto para ir para o ar!

