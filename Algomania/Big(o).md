
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
tudo certo com a automçao
