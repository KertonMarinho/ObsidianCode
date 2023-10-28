Ubunto faz parte da família Debian, o comando usado é apt

# <span style="color:yellow">Comandos apt</span>

```bash
sudo apt update
```
* Instala e atualiza pacotes/programas
* Localiza todos os pacotes a serem atualizados
* sudo vem de super usuário
* pedi senha(senha não aparece no terminal)
* Os principais parâmetros incluem:
	*  <u>update</u>: atualiza a lista de pacotes disponíveis; 
	*  <u>upgrade</u>: atualiza os pacotes já instalados para sua versão mais recente; 
	*  <u>install</u>: instala um pacote; 
	*  <u>remove</u>: remove um pacote; 
	*  <u>list</u>: descobre se o pacote está instalado ou não, e qual a sua versão; e 
	*  <u>search</u>: procura por um pacote no repositório.
****
*  Descobre se o pacote está instalado ou não e sua versão
```bash
apt list nomePacote
```

* Localiza todos os pacotes a serem instalados
```bash
sudo apt update
```

* Pesquisa sobre o pacote
```bash
apt search nomePacote
```

* Instala p pacote escolhido
```bash
sudo apt install nomePacote
```

* remove o pacote escolhido
```bash
sudo apt remove nomePacote
```

****

# <span style="color:yellow">Comando dpkg</span>

``dpkg [opções] nome_do_pacote
```bash
sudo dpkg -i nomeArquivo
```
- O comando dpkg é um gerenciador de pacotes para sistemas operacionais baseados em Debian, como o Ubuntu. 
- É útil para instalar pacotes fora do repositório padrão do sistema. 
- O próprio Google Chrome é um exemplo que precisa ser instalado dessa maneira.
- Alguns dos principais parâmetros são:
	- <u>-i (instalar)</u>: instala um pacote específico; 
	- <u> -r (remover)</u>: remove um pacote específico; 
	- <u>-l (listar)</u>: lista todos os pacotes instalados; e 
	- <u>-S (buscar)</u>: busca por um pacote específico