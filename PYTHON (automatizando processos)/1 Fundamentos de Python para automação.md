# Python básico
## <span style="color:yellow">Concatenação</span> ``y = y + "world"
## <span style="color:yellow">Comparação</span>`` ==`` ``z == AA
## <span style="color:yellow">Resta da divião</span>`` % ``
## <span style="color:yellow">Operadores lógicos</span> ``and, or, not
---
## <span style="color:red">Receber uma entrada de usuário</span> 
```python
raw-input() #retorna uma string
```
## <span style="color:red">Impressão na tela</span>
```python
print
```
## <span style="color:red">A primeira atribuição em uma variável também é responsável pro cria-lá</span>
- Tipos de variável não precisa ser informado
- Python descobre o tipo de variável por conta
```python
x = 34 - 23
y = "hello"
```
## <span style="color:red">Para iniciar o Shell basta digitar o comando:</span>
```python
>python
```
## <span style="color:red">Quando o comando é inciado aparecerá três >(>>>) indicando que ele está ativo e pode receber comandos</span>
```python
>>> print "hello world"
```
## <span style="color:red">Whitespace</span>
- Importante p/ indentação e novas linhas
	- Use ``|`` para quando for para uma proxima linha prematuramente
- Em Python não há {}, isso é para definição de dicionário(dict)
- Blocos de código definidos por indentação!
---
## <span style="color: LimeGreen">Comentário por linha</span>  ``#``
## <span style="color: LimeGreen">Comentário por linha várias linhas </span>  ``"""palavra""""``
## <span style="color: LimeGreen">Fortemente tipada, não existe cast</span>
- Se quiser mudar o tipo, use uma função
```python
a = (int) 1.0 #erro!!!
a = int(1.0)
```
## <span style="color: LimeGreen">Não Possui comandos declarativos</span> 
```python
# Java
algo n = new algo();
## python
n = algo()
```
---
# <span style="color:#20B2AA">Tipos Básicos</span>
- Inteiros
- Inteiros longos
	- L ou l (convertidos automaticamente c/ precisão de inteiros 32 bits)
- Floats (ponto flutuante)
	``1.22 , 3.4e-10``
---
## *<span style="color: #1E90FF">Strings</span>
```python
"abc" ou 'abc'
```
## <span style="color:orange">Operadores de expressão de python e sua precedência</span>
[6. Expressões — Documentação Python 3.12.5](https://docs.python.org/pt-br/3/reference/expressions.html)
![[Pasted image 20240908222301.png]]

---
# <span style="color:violet">Comandos básicos</span> 
## <span style="color:#20B2AA">Dir(element)</span>
- Todos os atributos e metódos que estão associados a elemento
## <span style="color:#20B2AA">Type(element)</span>
- Descobre o tipo de objeto
## <span style="color:#20B2AA">Import</span>
- Importar módulos para uso no seu código
```python
import modulo
import modulo.algo
import modulo.algo as malg
from modulo import *
from modulo import algo
from modulo import algo.item as ait
```
---
# ATRIBUIÇÃO
-  Atribuição de uma variável em Python significa criar um rótulo para armazenar uma referência para algum objeto
	``Atribuição cria referência e não cópia
- Em Python a tipagem é dinâmica!
	- Declaração variáveis sem atribuí-las irá levantar um erro!
<span style="color:orange">Exemplo:</span>
```shell
>>> y
>>> traceback (most recent call last):
>>> file "<pyshell#16", line 1, in -toplevel- y
>>> NameErrror: name 'y' is not defined
>>> y = 3
>>> y
>>> 3
```
- Você pode inicializar várias variáveis de uma só vez!
```python
x = y = z =2.0
```
- Rótulos de variáveis são Case Sensitiva e não podem iniciar com números. Números, letras  e underscores são permitidos!
```python
bob bob_2 _bob _2_bob bob_2 BOB
```
- Palavras reservadas:
```
and, assert, break, class, continue, def, del, elif,else, except, exec, finally, for, from, global, if, import, in, is, lambda, not, or, pass, print, raise , return, try, while
```

![[Pasted image 20240911201000.png]]
- Tuplas não mutáveis diferente de listas
---
## Operador in
- retorna um booleano. Checa se um valor está em uma sequência
- 4 in li