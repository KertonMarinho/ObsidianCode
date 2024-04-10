- É um conjunto de objetos que permitem a interação entre javascript e o navegador.
- Ele fornecer acesso às características do navegador, como janelas, históricos, cookies e muito mais
## <span style="color:yellow">Objeto Window</span>
- O objeto de nível mais elevado do BOM é o window. Representa uma janela aberta do navegador
### closed
- A propriedade closed retorna o valor booleano true se a janela estiver fechada e false se estiver aberta
![[Pasted image 20240318211347.png]]
### History
- O objeto history contém as URLs visitadas pelo usuário(na janela do navegador)
![[Pasted image 20240318211728.png]]
![[Pasted image 20240318211808.png]]
![[Pasted image 20240318211846.png]]

### OPEN
- O método open() abre uma nova janela. Abrir janelas sem o consentimento do usuário deve ser evitado
![[Pasted image 20240318212037.png]]

### CLOSE
- O método close() fecha uma janela
![[Pasted image 20240318212242.png]]

### ONLOAD
O evento onload() ocorre quando uma página termina de ser carregada
![[Pasted image 20240318212422.png]]
