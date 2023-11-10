### FILELIST
- UM OBJETO DENTRO DO OBJETO QUE PODE TER VÁRIOS ARQUIVOS
- Basicamente faz upload de arquivos do pc
![[Pasted image 20231109214606.png|400]]
```JS
function arquivo = document.getElementById('arquivo').files;
console.log(arquivo);
```
- para selecionar múltiplos arquivos do pc:
![[Pasted image 20231109215135.png|500]]
![[Pasted image 20231109215407.png|500]]
- Para trabalhar com um único arquivo acrescente ``filer[0];
```js
function arquivo = document.getElementById('arquivo').files[0];
console.log(arquivo);
```
- Para um único arquivo aparece agora o objeto ``file
![[Pasted image 20231109215807.png|400]]
- Aparece alguns itens neste file importante
- Nome de arquivo, ultimo arquivo modificado, name, tipo de aquivo, tamanho, etc
