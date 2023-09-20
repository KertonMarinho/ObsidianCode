<span style="color:yellow">></sapn>
Redireciona a saída padrão de um comando/script para algum dispositivo ou arquivo em vez do dispositivo de saída padrão (tela)
<span style="color:yellow">>></span>
Redireciona a saída padrão de um comando/script para algum dispositivo ou arquivo em vez do dispositivo de saída padrão (tela) 
* A diferença entre este redirecionamento duplo e o simples é se caso for usado com arquivos, adiciona a saída do comando ao final do arquivo existente em vez de substituir seu conteúdo
<
Direciona a entrada padrão (teclado) de arquivo/dispositivo para um comando 
* Este comando faz o contrário do anterior, ele envia dados ao comando
<<
Direciona a entrada padrão (teclado) de arquivo/dispositivo para um comando 
* Este comando faz o contrário do anterior, ele envia dados ao comando
****
<mark style="background: #ABF7F7A6;">Exemplo:</mark>
![[Pasted image 20230914214550.png]]
<sup>comando top</sup>
Joga a saída do top(Lista o processo do sistema e fica atualizando eles) em um arquivo.

```shell
top > Saida.txt
```
* resultado de saída nós temos resultado do top
* se for >> ele não apagar o que tinha antes(> subscreve o arquivo)
****
<mark style="background: #D2B3FFA6;">Exempla 2:</mark>
Pega o arquivo saida.txt como entrada do comando sort (ordena em ordem alfabética) e redireciona com seta invertida <.
```shell
sort < saida.txt
```
* * * *
<span style="color:turquoise">pipe |</span>
É possível encadear comandos Linux utilizando o sinal de pipe
* Assim, a saída de um comando é a entrada do próximo
<mark style="background: #ABF7F7A6;">Exemplo:</mark>
* comando Ls
![[Pasted image 20230914220635.png]]
* Com pipe o vc pode encadear comados

```shell
ls | sort
```
* resultado de saída, o pipe gerou uma sáida e pegou o resultado como próximo comando que é o sort
![[Pasted image 20230914221035.png]]
* pode encandeando quantos comandos quiser
****
<span style="color:turquoise">tree</span>
* Envia simultaneamente a saída do comando para um arquivo e para a tela
* Sintaxe:

```shell
comando | tree [arquivo]
```
