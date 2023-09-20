****<span style="color: orange">Comando LS</span>
* Lista o conteúdo de um diretório
* Sintaxe:
```bash
ls[opcoes][arquivo]
```
* **-A** (inclui os arquivos com o nome iniciado com '.' na listagem - arquivos ocultos)
* **-R** (lista recursivamente os diretórios encontrados)
* **-d** (Lista nomes de diretórios como arquivo, preferencialmente no lugar de seus conteúdos)
* **-L** (LS mais detalhado)

<span style="color:blue">Comando CD</span>
* Muda o diretório corrente para "dir"
* Sintaxe:

```bash
cd [l|P][dir]
```
* **~** (vai direto para  a home do usuário)
* **..** (retorna o diretório anterior)
* **-L** (segue links simbólicos)
* **-P** (usa a estrutura física de diretório em vez de seguir links simbólicos)

<span style="color:aquamarine">Comando mkdir</span>
* Cria diretórios
* Sintaxe:

```bash
mkdir[opções] diretórios...
```
* **-P** (cria os diretórios -pai de um caminho, caso eles não existam ainda)
* **-m** (indica o modo - permissões de um diretório no momento de usa criação)

<span style="color: brown">Comando rmdir</span>
* Remove diretórios vazios
* Sintaxe:

```bash
rmdir [opcoes] diretórios...
```

<span style="color:salmon">Comando rm</span>
* remove diretórios e os arquivos
* Sintaxe:

```bash
rm [opções] diretórios
```
* **-r** (apaga o conteúdo dos diretórios de forma recursiva, tudo que tiver dentro dele)
* **-R** (igual a -r)
* **i** (questiona se cada arquivo será apagado. Se a resposta for negativa, o arquivo é preservado)

<span style="color: violet">Comando CD</span>
* Mostra o caminho de diretórios em que você está


