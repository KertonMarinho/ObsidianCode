
- Em poucas palavras, Big O é uma forma de classificar quanto a sua função ou algoritmo é escalável.

- Isso nos ajuda a determinar qual será o comportamento do nosso algoritmo no **PIOR** dos casos ou quanto tempo ele levará para ser completado baseado nos seus valores de entrada.

- Ou seja, qual será a performance do seu código se o número de valores de entrada aumentar? Constante? Linear? Exponencial? Veremos logo abaixo.

- O tempo de execução do algoritmo é constante, independente da carga de dados que aparece.
---
## <span style="color:yellow">Big o : Extraindo métrica</span>

$$T = an  + b$$
T = complexidade de tempo
n = tamanho de array
a = constante, quanto tempo leva para calcular o código
b = todas variáveis
#### Como calcular o big O
1. Encontre o item que aumenta mais rapidamente
2. remova os coeficientes (b),eles são tão pequenas que ela passa ha Não ser mensuráveis
<span style="color:orange">Exemplo:</span>
```python
def find-sum(my_array):
	sum = 0 # Constante(b), leva o mesmo tempo para excultar
	for item in my_array 
		sum =+ item
	return sum #constante
```
- Quantos mais elementos deste dados de entrada, maior o número  de execuções que vão acontecer aqui:
```python
for item in my_array 
		sum =+ item
```
- calculando o Big (0)
$$ t= an$$
$$ t=1n $$
$$t = an =O(n)$$
$$t = O(n)$$
n= números de elementos que tem dentro do Array
- Crescimento Linear
- Quanto mais elementos, maior o número de execução
- Consumo de memoria é constante, independentemente de dados
---
## <span style="color:yellow">Big (o)  -  Tempo constante - O (1)</span>
- Quando o algoritmo executar sempre no mesmo tempo, independente da quantidade de dados que receber.
- Quando executara algum tipo de código independente o que aconteça ele sempre terá o mesmo tempo.
```python
exemplo
def example_1();
	print('Hello')
#exemplo 2
def example_2(n):
	return n
```
- Quando não tem dados de entradas ou conjunto de extrusões não esteja manipulando nenhum dado que veio de outra função ou da mesma função normalmente é um tempo constante.
```python
def example_4():
	my_queue.queue()
	my_queue.put(1)
	
```
---
## <span style="color:yellow">Big (o)  -  Tempo Linear - O (n)</span>
- Quando o tempo de algoritmo é dependente do valor de n(dados de entrada)
```python
def print_itens(my_array):
	for itemn in my_array:
		print(item)
```
<span style="color:orange">Exemplo</span>
![[Pasted image 20231021080815.png|500]]
<span style="color:orange">Exemplo 2</span>
```python
def find_sum(my_array):
	sum = 0
	for item in my_array:
		sum += item
	return sum
```
>[!warning]
>A busca linear, também chamada de busca burra, aumenta o tempo de execução de acordo com o número de elementos de um array.  
>Se o array tem de zero a 100 elementos , o algoritmo vai verificar item por item até achar o número escolhido. ser for 1 milhão de elementos da mesma forma.
---

---
## <span style="color:yellow">Big (o)  -  Tempo Logarítmo - O (log n)</span>
- Quando o algoritmo reduz  o tamanho de entrada a cada iteração
- Um algoritmo tem tempo logarítmico quando ele reduz o tamanho dos dados de entrada a cada iteração. Desta forma, ele não precisa olhar todos os dados de entrada para concluir sua tarefa.
- - A cada execução do algoritmo ele está separando os dados, cortando eles pela metade e fazendo uma busca que tem ser feito.
![[Pasted image 20231126223909.png]]
-  Ele corta pela metade, executa, corta pela metade novamente, executa...sucessivamente(ex: ave binária)
- Sempre lembra que Log de n vc corta os elementos pela metade e vai fazendo as interações.
--- 
## <span style="color:yellow">Tempo quadrático O (2^n)</span>
- Quando o Algoritmo tem a necessidade  de executar uma operação linear para cada valor dentro dos dados de entrada.
- O algoritmo é considerado com complexidade quadrática quando tem a necessidade de perormar uma operação de tempo linear para cada valor dentro dos dados de entrada. Dica: Normalmente, quando tem um "for" dentro de outro.
- ![[Pasted image 20231126224709.png]]
- Três listras seriam (n^3), o conceito é o mesmo.
- Quando temos uma interação dentro da outra teremos esse padrão
- É bastante lento, muito usados em arrays e força bruta
- --
## <span style="color:yellow">Tempo exponencial - O (2<sup>n</sup>)</span>
- Quando p algoritmo de tamanho n recursivamente com dois sub-problemas de tamanho n-1
- Um algoritmo é considerado com tempo exponencial quando o crescimento do tempo dobra para cada item adicionado aos dados de entrada. 
- Este tipo de complexidade é muito vista em algoritmos de força bruta.
![[Pasted image 20231127232102.png]]
>[!warning]
> Recursividade, em uma explicação simples, é quando um método/função faz uma chamada de si mesmo. No exemplo acima, perceba qua a função fibonacci chama a ela mesma no corpo do seu algoritmo
