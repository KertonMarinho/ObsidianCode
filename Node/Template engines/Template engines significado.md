(motores de Templates)
- É uma ferramenta que ajuda a criar e renderizar páginas da web dinâmicas.
- Ela permite que você combine dados (como informações de um banco de dados) com um modelo ou template HTML predefinido para gerar páginas da web completas de forma programática.
---
- As template engines em Node.js são particularmente úteis quando você está construindo aplicativos da web que precisam exibir informações dinâmicas aos usuários, como blogs, sites de comércio eletrônico, fóruns, etc. Em vez de escrever manualmente HTML com todos os dados incorporados, você pode usar uma template engine para inserir automaticamente os dados nos lugares certos do modelo.

Alguns exemplos populares de template engines em Node.js incluem:

1. **EJS (Embedded JavaScript)**: EJS permite que você insira código JavaScript diretamente em seu HTML, tornando-o mais flexível e poderoso.
    
2. **Handlebars**: Handlebars é uma template engine que usa uma sintaxe simples com chaves duplas {{}} para inserir variáveis e expressões em seu modelo.
    
3. **Pug (anteriormente conhecido como Jade)**: Pug é uma template engine que utiliza uma sintaxe de indentação significativa, o que a torna mais compacta e legível.
    
4. **Nunjucks**: Esta template engine é inspirada na linguagem de templates do Jinja2 (usada em Python) e é muito poderosa e flexível.
    
5. [[mustache (instalação)]]: Mustache é uma template engine minimalista que está disponível em várias linguagens de programação, incluindo JavaScript. É conhecida por sua simplicidade e portabilidade.
6. **Edge** 
	- Adonis utiliza este template

Quando você escolhe uma template engine para o seu projeto Node.js, geralmente instala o pacote correspondente usando o gerenciador de pacotes npm (Node Package Manager) e, em seguida, configura-o para renderizar os modelos HTML conforme necessário em suas rotas e controladores.



		você não precisa configurar sempre tudo na mão se não quiser, o próprio express tem um gerador de projeto express que você pode usar para não precisar ficar fazendo tudo na mão, se te interessar aqui o link da doc: https://expressjs.com/en/starter/generator.html


