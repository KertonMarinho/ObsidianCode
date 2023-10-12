
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
- Quantos mais elementos deste dados de entrada, maior o número  de excuções que vão acontecer aqui:
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
