Ubunto faz parte da família Debian, o comando usado é apt

<span style="color:yellow">Comandos apt</span>


```bash
sudo apt update
```
* Instala e atualiza pacotes/programas
* Localiza todos os pacotes a serem atualizados
* sudo vem de super usuário
* pedi senha(senha não aparece no terminal)
****

```bash
apt list nomePacote
```
*  Descobre se o pacote está instalado ou não e sua versão
****


```bash
sudo apt update
```
* Localiza todos os pacotes a serem instalados
****


```bash
apt search nomePacote
```
* Pesquisa sobre o pacote
****


```bash
sudo apt install nomePacote
```
* Instala p pacote escolhido
****


```bash
sudo apt remove nomePacote
```
* remove o pacote escolhido
****

<span style="color:yellow">Comando dpkg</span>

```bash
sudo dpkg -i nomeArquivo
```
* Instala p pacote escolhido que está em uma pasta fora do repositório, fora dos pacotes padrões, como o chrome.