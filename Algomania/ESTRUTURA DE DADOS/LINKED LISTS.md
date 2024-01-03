# <span style="color:yellow">Linked Lists(listas linkadas)</span>
- Muita utilizada para guarda estruturas mais dinâmicas.
- Guarda uma lista de elementos, onde cada elemento está ligado ao próximo elemento dele
- Existe alguns tipos de listas linkadas
- Uma lista linkada é um conjunto de dados que são interligados, os elementos não são guardados em uma área de memória contínua como um array. Cada nó da lista aponta para o próximo e o anterior, se for uma lista duplamente linkada. 

### <span style="color:purple">Lista linkada dupla</span>
- Neste cada elemento está ligado com o próximo elemento e tem um ponteiro para o anterior
- ``node=nó``
- ``HEAD= a cabeça, o primeiro nó``
- ``TAIL= o ultímo nó``
- o prev (ponteiro) do ``HEAD`` vai ser ``NULL``
- o NEXT do ``tail`` vai ser ``NULL``
![[Pasted image 20240102231451.png|600]]

- Em JavaScript, uma linked list é uma estrutura de dados composta por nós, onde cada nó contém um valor e uma referência para o próximo nó na sequência. Não há uma implementação nativa de linked list em JavaScript como em algumas outras linguagens, mas é possível criar uma usando objetos ou classes.

Por exemplo, podemos criar um nó:

```javascript
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}
```

E então, criar a estrutura da linked list:

```javascript
class LinkedList {
  constructor() {
    this.head = null;
    this.tail = null;
  }

  addToTail(value) {
    const newNode = new Node(value);// Aqui, um novo nó é criado utilizando a classe `Node` que foi definida anteriormente. Este novo nó recebe o valor passado como parâmetro para a função `addToTail`
   //Este bloco de código verifica se a lista está vazia ou não. Se `this.head` for `null` (ou seja, se a lista estiver vazia), isso significa que o novo nó será tanto o início quanto o fim da lista:
	if (!this.head) {//Se a lista estiver vazia, neste caso, o novo nó será o primeiro nó da lista, então...
      this.head = newNode;//..então `this.head` (referência para o primeiro nó) é configurado para apontar para o novo nó
      this.tail = newNode;//: Além disso, como a lista está vazia, o novo nó também será o último nó da lista, então `this.tail` (referência para o último nó) é configurado para apontar para o novo nó.
    } else { //Se a lista não estiver vazia (`else`):
      this.tail.next = newNode;//Aqui, o próximo nó do atual último nó (que está representado por `this.tail`) é configurado para apontar para o novo nó, ou seja, o novo nó é adicionado após o último nó existente na lista.
      this.tail = newNode;//: Após adicionar o novo nó após o atual último nó, atualizamos `this.tail` para que aponte para o novo nó, tornando-o o novo último nó da lista.
    }
  }

  removeFromHead() {
    if (!this.head) return null; //Verifica se a lista está vazia. Se não houver nenhum nó (`this.head` é `null`), retorna `null` indicando que a lista está vazia e não há nada para remover.

    const removedNode = this.head; //: Se houver pelo menos um nó na lista, armazena uma referência para o nó no início da lista em `removedNode`.
    this.head = this.head.next; //Atualiza `this.head` para apontar para o próximo nó da lista, removendo assim o nó que estava no início. Isso basicamente corta o primeiro nó da lista e move a cabeça da lista para o próximo nó.
    

    if (!this.head) { 
      this.tail = null;
    } //Se depois de remover o nó a lista ficar vazia, ou seja, se `this.head` se tornar `null` (porque não há mais nenhum nó na lista), então `this.tail` também é definido como `null`, indicando que a lista não tem mais nenhum nó:

    return removedNode.value; //Retorna o valor do nó removido do início da lista
  }

  search(value) {
    let currentNode = this.head;//Começa a busca a partir do primeiro nó da lista
    while (currentNode) {//: Executa um loop enquanto `currentNode` não for `null`, percorrendo todos os nós da lista.
      if (currentNode.value === value) {//Se o valor do nó atual (`currentNode.value`) for igual ao valor passado como parâmetro (`value`), significa que encontramos o valor na lista, então retorna `true`
        return true;
      }
      currentNode = currentNode.next;//Avança para o próximo nó na lista para continuar a busca.
    }
    return false;//Se o loop terminar sem encontrar o valor, isto é, quando `currentNode` se torna `null`, o método retorna `false`, indicando que o valor não está na lista
  }
}
```

Com esta estrutura, você pode adicionar elementos ao final da lista usando `addToTail`, remover elementos do início usando `removeFromHead` e buscar elementos usando `search`. Por exemplo:

```javascript
const myList = new LinkedList();
myList.addToTail(10);
myList.addToTail(20);
myList.addToTail(30);

console.log(myList.search(20)); // Saída: true
console.log(myList.removeFromHead()); // Saída: 10
```

Essa é uma implementação básica de uma linked list em JavaScript. Ela pode ser expandida com mais métodos, como inserção em posições específicas, remoção por valor, entre outros.