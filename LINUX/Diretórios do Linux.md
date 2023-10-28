## <span style="color:#FFB8EBA6;">Diretório bin </span> 
* Binaries(binários)
* Onde encontra-se os binários(executáveis) de diversos programas
```shell
/bin
```
----
## <span style="color:#FF5582A6;">Diretório Boot </span>
* Contém os arquivos necessários para seu SO inicializar
* Contém o GRUB
```bash
/boot
```
----
## <span style="color: #FFB86CA6;">Diretório Dev </span>
- Representar dispositivos de hardware presentes no sistema
* Devices(dispositivos)
* Onde encontra-se os arquivos do seu hardware. Discos, sons, câmera e etc
* Para acessar a unidade de discos /dev/sda1 (o número final varia de acordo com a partição do disco)
* os arquivos de dispositivo no "/dev" são usados por vários programas de sistema para a realização de tarefas, como montar partições de disco ou acessar dispositivos de rede
```bash
/dev
```
----
## <span style="color: #FFF3A3A6;">Diretório ETC </span>
 - Usado para armazenar arquivos de configuração do sistema e de programas instalados no sistema
* Et cetera
* Mantém as config. gerais do sistemas para todos os usuários.
* O diretório "/etc" é acessado frequentemente por administradores de
sistema, para a realização de tarefas como configurar serviços de rede, adicionar ou remover usuários, ou ainda alterar configurações de programas instalados.
```bash
/etc
```
---
## <span style="color:  #BBFABBA6;">Diretório Home </span>
* Equivalente ao usuário(user) do windows
* Mantém os arquivos(como musica, documentos, etc...) e config dos usuários do sistemas
```bash
/home
```
---
## <span style="color: #ABF7F7A6;">Diretório root </span>
* Mantém os arquivos e config do root do sistema(administrador)
```bash
/root
```
----
## <span style="color:  #ADCCFFA6;">Diretório Lib </span>
 Library (biblioteca)
* Mantém bibliotecas usadas por softwares
* Similar a DLL do windows
```bash
/lib
```
---
## <span style="color: #D2B3FFA6;">Diretório Media e MNT</span>
* diretório usado para montar dispositivos externos, como discos rígidos externos ou dispositivos de mídia removíveis.
```bash
/media
```

* usado para montar dispositivos de armazenamento temporários
```bash
/mnt
```
---

## <span style="color:  #CACFD9A6;">Diretório  OPT </span>
- optional
* Diretório usado por alguns fabricantes para instalar seus softwares
* O Google Chrome usa está pasta

```bash
opt
```
---
# <span style="color: #FFB86CA6;">Outros diretórios</span>

```bash
/proc
```
* Mantém arquivos sobre o sistemas e seus processos

```bash
/run
```
* Armazena informações e logs de serviços que rodaram

```bash
/sbin
```
* Semelhante ao bin, mas são binários que só podem ser acessados pelo root

```bash
/temp
```
* Diretórios de arquivos temporários de cada sessão

```bash
/usr
```
* Já foi a pasta de usuários
* Hoje, mantém arquivos de programas para usuários

```bash
/var
```
* Arquivos como logs do sistemas, backup, ou seja, arquivos de tamanhos variáveis e que tendem a crescer de tamanho