- Torna o TS mais específico
- Todo elemento é  htmlelement mas  dentro dele tem tipos e propriedades diferentes o assertions é para corrigir isso
- assistência dada ao TP para ele entender mais espicificamente que elemento é aquele ou como funcionar aquele elemento
```js
let idadefield = document.getElementById('iade') as HTMLInputElement;
//...
console.log(idadefield.value);
```
---

#Chagpt
Em TypeScript, os type assertions (ou "type casts") são uma maneira de indicar ao compilador que você tem conhecimento sobre o tipo de uma variável mais do que ele pode inferir por si só. Isso é útil em situações onde você sabe que um tipo específico é aplicável, mesmo que o TypeScript não possa deduzi-lo automaticamente.

Existem duas maneiras principais de fazer type assertions em TypeScript: "angle-bracket" (`< >`) e `as`.

### Angle-bracket syntax:

```typescript
let valor: any = "Isso é uma string";
let tamanhoString: number = (<string>valor).length;
```

### `as` syntax:

```typescript
let valor: any = "Isso é uma string";
let tamanhoString: number = (valor as string).length;
```

Ambas as formas atuam de maneira semelhante, permitindo que você indique ao TypeScript que o tipo da variável é aquele que você está especificando.

É importante notar que type assertions não fazem nenhuma mudança real nos dados em tempo de execução. Eles são apenas uma ferramenta para ajudar o compilador a entender e validar o código.

No entanto, usar type assertions pode ser arriscado se usado incorretamente, pois você está dizendo ao TypeScript para tratar uma variável de uma maneira que pode não ser verdadeira em tempo de execução. Isso pode levar a erros se o tipo que você está especificando não for realmente o correto.

Se possível, é uma boa prática evitar type assertions e optar por outras abordagens mais seguras, como tipagem explícita ou verificação de tipos condicional para garantir a segurança do tipo durante a execução do código.