Existem para proteger o sistema e arquivos de acessos indevidos de pessoas ou programas não autorizados
#dono
É quem criou arquivo ou diretório. É o mesmo nome do usuário que estiver logado no sistema
A identificação do dono também é chamada de user id (UID)
#grupo
Permite que vários usuários diferentes tenham acesso a um mesmo arquivo A identificação do grupo é chamada de group id (GID)

<span style="color:yellow">Tipos de permissões de acesso</span>
* <span style="color:red">r</span> - permissão de leitura para arquivos. Para diretórios, permite listar seu conteúdo (com comando Ls, por exemplo)
* <span style="color:red">w</span> - permissão de escrita para arquivos. Para diretórios, permite a gravação de arquivos ou outros diretórios dentro dele
* Um arquivo/diretório só pode ser apagado se tiver permissão de escrita
* <span style="color:red">x</span> - permite executar um arquivo (caso seja um programa executável). Para diretórios, permite que seja acessado através do comando cd


```bash
-rwxr-xr-- kertoon users nomeArquivo
```
* <span style="color:orange">1° caractere </span>1° caractere – diz o tipo do arquivo. 
    * "d" é um diretório; 
    * "l“, um link a um arquivo no sistema; 
    * "-" é um arquivo comum
* <span style="color:orange">(2-4)° caractere </span>  permissões do dono do arquivo (kerton)
* <span style="color:orange">(5-7)° caractere </span>  permissões do grupo do arquivo (users)
	* traço(-) significa que não pode fazer escrita
*  <span style="color:orange">(8-10)° caractere </span> permissões de outros usuários ao arquivo
	* pode abrir o arquivo
	* não pode escrever
	* não pode excutar

# <span style="color:turquoise">Comando chmod</span>  
Modifica as permissões de um arquivo ou diretório
* Sintaxe:

```bash
chmod [opções][permissões][diretório/arquivo]
```


![pictures](chmod.png)

<span style="color:orange">Exemplo:</span>

![[Pasted image 20230914205655.png]]
* Primeiro caractere <mark style="background: #CACFD9A6;">d</mark> significa diretório.
* Primeiro caractere <mark style="background: #FF5582A6;">  - </mark> significa arquivo.
Mudar permissão:
```shell
chmod o+w aula.txt

```
