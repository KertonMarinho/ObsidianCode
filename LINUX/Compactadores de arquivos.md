<span style="color:blue">TIPOS</span>
* <span style="color:orange">.gz</span>  compactadores pelo gzip
* <span style="color:orange">.bzip2</span>
* <span style="color:orange">.tar.gz</span> Compactadores pelo gzip no utilitário tar (tar é um arquivador, vc arquiva primeiro depois vc compacta co, gzip)

<span style="color:aquamarine">Tar</span>
*  O tar é um arquivador(ele junta arquivos e não compacta)
* Pode ser usado em conjunto com o gzip para compactar e arquivar
* Sintaxe:

```bash
tar [opções][arquivo-destino][arquivo-origem]
```

<span style="color:turquoise">Comandos</span>
* <span style="color:orange">-c</span> (cria um novo arquivo)
* *<span style="color:orange">-x</span> (extrai arquivos de um arquivo compactado)
* *<span style="color:orange">-j</span> (filtra o arquivo compactado  por meio do bzip2)
* *<span style="color:orange">-z</span> (filtro o arquivo compactado através do gzip)
* *<span style="color:orange">-t</span> (lista o conteúdo do arquivo compactado)
* *<span style="color:orange">-f</span> (usa o arquivo especificado para gravação)
* exemplo:
	![[Pasted image 20230913222617.png]]
		<sub>ele cria e grava(-cf) e compacta todos os arquivos aula(2 e 3)</sub>
	




			 
