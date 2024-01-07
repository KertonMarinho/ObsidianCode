O **nodemon** é uma ferramenta que ajuda no desenvolvimento de aplicativos baseados em **Node.js**. Ele monitora o diretório do aplicativo e reinicia automaticamente o servidor Node.js quando detecta alterações nos arquivos do diretório. [O nodemon é um substituto para o comando `node` e não requer nenhuma alteração adicional no código ou no método de desenvolvimento](https://www.npmjs.com/package/nodemon) [1](https://www.npmjs.com/package/nodemon).

# Para instalar:
```shell
npm install -g nodemon
```
- agora em vez de der o comando node dist/index.js,
- vc pode dar o comando nodemon dist/index.js
![[Pasted image 20231003222620.png]]

- agora ele fica monitorando, e responde automaticamente
- 
![[Pasted image 20231003222811.png]]
- agora ele monitora e atualiza a página automaticamente
---
# Usando o Nodemon com Typescript
## Instalando a biblioteca TS Node

````shell
npm install -g ts-node
````
- pode cancelar o Nodemon de monitorar em tempo real
- pode até tirar a pasta ``dist``
- A partir de agora em vez de rodar o comando node ele vai rodar o comando ts-node

---
# Para rodar o log do node no terminal
```shell
ts-node src/index.ts
```
# Para rodar o nodemon(ele monitorar e executar, substituindo outros comandos)
```js
nodemon src/index.ts
```


## Criando um script para rodar ts-node
1. no arquivo ``package.jason`` 
2. Em scripts
3. Pode tirar ``watch-ts`` 
![[Pasted image 20231004211941.png|500]] 
4. Substitua o ``start`` pelo 
```json
"start-dev":"nodemon src/index.ts"
```
6. Para rodar no terminal o script:
```shell
npm run start-dev
```

