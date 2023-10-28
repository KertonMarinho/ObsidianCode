## <span style="color:orange">Processos</span>
Todos os programas em execução podem ser chamados de processos e são identificados por um número chamado PID (process identification)

* Os processos podem estar em três estados diferentes: em foreground (primeiro plano), em background (segundo plano) ou suspensos
	   <span style="color:green">Foreground</span>
   Os processos em foreground costumam segurar o controle do terminal até encerrarem
	<span style="color:green">background</span>
   Podemos mandar o processo para background para não deter o controle do terminal
****
## <span style="color:orange">Comando ps</span>
* Retorna uma lista dos processos em execução
* Sintaxe:
```bash
ps [opções]
```
* **-a** (todos os processos no sistema)
* **-x** (lista todos os processos pertencentes ao usuário)
* **-u** (mostra o nome de usuário que iniciou o processo e hora em que o processo foi iniciado)
****
## <span style="color:aquamarine">Comando top</span>
* Mostra os programas em execução ativos, parados, uso de CPU, memória RAM, Swap etc.
* Continua em execução mostrando continuamente os processos que estão rodando em seu computador e os recursos utilizados por eles

```bash
top [opções]
```
****
## <span style="color:green">Comando jobs</span>
* O comando jobs mostra os processos que estão parados ou rodando em segundo plano
* Processos em segundo plano são iniciados usando o símbolo "&" no final da linha de comando

```bash
jobs [opções]
```
****
## <span style="color:red">Comandos fg e bg</span>
* Coloca um processo em<span style="color:yellow"> foreground(fg)</span>

```bash
fg [número]
```
* Coloca um processo ##</span>

```bash
bg [número]
```
****
## <span style="color:brown">Comando kill</span>
* Encerra um processo em execução
- principais parâmetros utilizados:
	- -l: lista os sinais que podem ser enviados para os processos; 
	- -s: envia o sinal SIG para o processo; e 
	- -9: envia o sinal de interrupção SIGKILL, que é usado para forçar o encerramento de um processo.
```bash
kill [opções][sinal][número]
```








