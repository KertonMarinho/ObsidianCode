# Web Scraping
- Acesse o HTML da página da web e extrair informações/dados úteis dela. Essa técnica é chamada da web scraping ou web harvesting ou web extraction
- Web scraping é um termo usado para descrever o uso de um programa ou algoritmo para extrair e processar grandes quantidades de dados da web
- Web scraping extrai dados automaticamente e os apresenta em um formato que você pode facilmente entender.
![[Pasted image 20240912200040.png|450]]
---
## <span style="color:yellow">O que é o robots.txt</span>
É instruit os robôs da web sobre como rastrear páginas em um site
- O arquivo robots.txs faz parte do protocolo de exclusão de roboôs(rep), um grupo de padrões da web  que regulam como os robôs rastreiam a web, acessam e indexam contéudo para servir esse conteúdo para os usuários.
- Para acessar este arquivo troque o domain_name pelo nome do site:
http://_domain_name/robots.tx
---
## <span style="color:#8A2BE2">Beautifull Soup</span>
- É uma biblioteca python para extrair dados de arquivos HTML e XML
- Você pode usá-lo para extrair tabelas, listas, parágrafos e também pode colocar filtros para extrair informações de páginas da web.
- O Beatiful Soup 4 é mais rápido, tem mais recursos e funciona com analisadores de terceiros como lxml e html5lib

### Passos para usar:
1.  Para instalar:
``` shell
pip install beautifulsoup4
```
biblioteca beautufull soup:
www.crummy.com/software/BeautifulSoup/bs4/doc/
- Para instalar versão usada no curso:
```
pip install beautifulsoup4==4.11.1
```
2. entre na pasta do arquivo que vai ser usado:

```shell
"C:\Users\kerto\Area Work\Curso Udemy Python\arquivos"
```

3.  Importar para o Python o beatifullsoup4 na pasta do projeto:
```shell
python
from bs4 import BeautifulSoup 
```

4.  Pelo terminal carrega o arquivo:
```shell
html_file = open("generic_simple.html", mode="r", encoding="utf-8")
```
- Para ver o arquivo no htm_file:
```shell
html_file
```
![[Pasted image 20240922211009.png]]
- Cria a vriável soup e utiliza o beautifulSoup e colocque o html_file dentro da variável:
```shell
soup = BeautifulSoup(html_file)
```
- para ver o que tem dentro do soup:
```shell
soup
```
- mostra  todas as listas de funçoes e atributos 
```shell
print(dir(soup))
```
![[Pasted image 20240922211741.png|500]]

- também pode ver a função Help do Python passando soup
```shell
print(help(soup))
# para sair apert Q
```
![[Pasted image 20240922211826.png]]
- Para exiber com mais detalhes o html:
```shell
soup.prettify()
```
![[Pasted image 20240922212120.png]]
- Para pegar o só o texto sem as tags:
```shell
soup.get_text()
```
![[Pasted image 20240922212322.png]]
-  Voce pode dar um replace para tirar o /n(entre outros):

```shell
soup.get_text().replace("\n", " ")
```
![[Pasted image 20240922213714.png]]
- pegar qualquer elemento ``soup.<elemento>

```shell
soup.title
# se tiver mais de um ele pega o primeiro que achar
```
- pega o tem dentro da tag

```shell
soup.title.string
```
- mostra o nome da tag
```shell
soup.title.name
```
- vc pode pegar o está o pai dela(dentro onde ela está)
```shell
soup.title.parent
```
- pega os filhos dessa tag
```shell
list(sopu.div.children)
```
- pega as tags  que está dentro utilizando for:
```shell
for i in list(souo.div.chlidren):
print(i.name)
```
- para pegar o href
```shell
soup.a["href"]
```
#### um jeito mais utilizado
```shell
soup.find("div")
```
- find com filtro
```shell
soup.find("DIV", ID="IMP_SRTILCE_id")
```
- Pegar tudo que contem na div utilizando class:
```shell
sopu.find("div", class_="article")
# não esqueca do (_) para pegar tudo que tiver a palavra escolhida
```
- Pegar todas as divs que tiverem uma palavra:
```shell
soup.find_all("div",class="article")
```
- Navegando entre os elementos:
```shell
soup.find_all("div",class="article")[3].b.string
```
- pegar todos os links de uma página:
```shell
soup.find_all("a")
```
- descobrir quantos links existe
```shell
len(sopu.find_all("a"))
```
- mostrar de uam forma organizada com for
![[Pasted image 20240922223305.png]]

---
# Web Scraping - conceitos essenciais(aula 14)

