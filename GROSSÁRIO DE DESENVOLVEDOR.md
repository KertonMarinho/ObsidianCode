***<span style="color:red">API (Aplication programming interface)</span>*
* Conjunto de rotinas e padrões de programação
* Objetivo: acessar aplicativos de software
* Plataformas baseadas na web
* Utilizada por programa/aplicação

<span style=color:orange>Framework</span>
* Conjunto de código de LP específica
* Auxilia no desenvolvimento web ou software
* Biblioteca de códigos con funções já prontas
* Arcabouço de códigos

<span style="color:green">IDE</span>
* Integra diversas funcionalidades para desenvolvimento em uma única interface gráfica
* Auxilia e agiliza o processo de desenvolvimento

<span style="color:pink">SDK</span>
* Composição: compilador, Debuger e Api
* Conjunto de ferramentas fornecidas por um fabricante para que se desenvolva para uma plataforma ou sistema específico

<span style="color:blue">serviços</span>
* processos de software
	* Monolíticos: roda em um único processo
	* Microsserviços: abordagem arquitetônica e organizacional de desnvolvimento de software na qual o software consiste em pequenos serviços independentes que se comunicam usando APIs bem definidas. São autônomos e especializados.

**<span style="color:turquoise">Soap (Service-oriented architecture_or Aplication_Protocol)</span>**
* Utiliza arquivos xml
* Protocolo de transporte: HTTP com

<span style="color:yellow">REST</span>
* Conjunto de restrições para criação de webservices
* Quando um serviço implementa esse padrão: Restfull
* Restfull utiliza Json

<span style="color:purple">Commit</span>
* envia alterações de determinado trecho do código
* Envia criação de uma nova versão dom projeto

<span style="color:brown">Versionamento</span>
* Atribuição de número de versão ao estado do projeto

<span style="color:grey">Snapshot</span>
* Cópia instantânea de um volume

<span style="color:salmon">Debug</span>
* debugging ou debugar
* depurar o programa
* Encontrar erros no programa e tentar resolvê-los

<span style="color:blue">Definição de Nuvem</span>
* Método de virtualização do sistema operacional
* Permite executar aplicativos isolados de recursos
* Simplificando: containers empacotam o código, as configurations e as Independence de um aplicativo em um único objetivo

<span style="color:pink">Computação de borda</span>
* Aproxima os equipamentos de onde os dados são gerados
* Evolução da computação em nuvem
* 1990, surgiu CDNs que armazena conteúdo próximo dos locais de entrega

<span style="color:green">Area STEM</span>
* Science, Technology, Engineering and Mathematics

<span style="color:purple">Fase de requisitos</span>
É o que determina a qualidade do software

<span style="color:turquoise">Aspectos da qualidade de software</span>
- [ ] Usabilidade(fácil de usar)
- [ ] Confiabilidade(envolve tolerância as falhas, o sistema é capaz de se recuperar após um,a falha )
- [ ] Funcionalidade
- [ ] manutenibilidade(é fácil de fazer modificações e correções)

<span style="color: yellow">Processos</span>
* ver [[Comandos de processos]] Linux

<span style="color:aquamarine">Repositório de gerenciamento de configuração</span>
* Ou sistema de controle de versão
* Ou VCS (Version control system)
* Gerenciamento várias versões no desenvolvimento do projeto
* Gestão inteligente e eficaz para organizar projeto
* acompanhamento de histórico de desenvolvimento
* Customização de determinada versão sem alterar o projeto principal
* Recuperação de versão anterior
* dois tipos de sistema de controle de versão
	* <span style="color:red">Centralizado</span>: composto por um único servidor central e várias estações de trabalho
	* <span style="color:red">Descentralizado</span>: (distribuído) possuem diversos repositórios autônomos e independente para cada desenvolvedor
	
![[Pasted image 20230915230359.png]]
****
<span style="color:aquamarine">Repositório de Reutilização</span>

![[Pasted image 20230915230712.png]]
****
<span style="color:aquamarine">Repositório de Ideias </span>
* um espaço no qual os desenvolvedores e futuros desenvolvedores  trocam informações e dicas sobre ferramentas, códigos e linguagens. A seguir, são listados alguns desses repositórios
	1. Oracle devoloper
	2. Cisco
	3. Cisco Netcad
	4. AWS (Amazon Web service)
	5. Mozzila
	6. Manual de python
	7. Site do java
	8. W3schools

<span style="color:aquamarine">Dogfoodin</span>
* "comer sua própria comida de cachorro"
* Gíria de Ti: desenvolvimento e utilização de seus próprios serviços
* Amazon sobre seus serviços(ela usa sua propria estrutura e aluga)
#DES/AULA3/TEMA4
***
<span style="color:salmon">Teste de software</span> 
* É um elemento de um tema mais amplo, muitas vezes conhecido como verificação e validação (V&V).
* <span style="color:yellow">Verificação</span> refere-se ao conjunto de tarefas que garantem que o software implemente corretamente uma função específica.
* <span style="color:yellow">Validação</span> refere-se ao conjunto de tarefas que asseguram que o software foi criado e pode ser rastreado segundo os requisitos do cliente. (Pressman, 2021, p. 373)

![[Pasted image 20230915234720.png]]
![[Pasted image 20230915235249.png]]
![[Pasted image 20230915235318.png]]
***
<span style="color:brown">Implemetação - deployment</span>
* Além das independências
	* Interpretadores
	* Compiladores
	* Pacotes
	* Extensões
	* Configuração do ambiente
	* Licenças  de outros software
	* Senhas de banco de dados

***
<span style="color:green">Contêiner</span>
* Pacote que contém um software e todas as dependências necessárias para que ele execute *
* Fornece facilidade de manuseio e economia de tempo, facilitando a implantação (deploy)
* Contêineres são um método de virtualização

---
## <span style="color:yellow">Middleware</span>
Middleware em Node.js e no contexto do Express refere-se a funções que têm acesso tanto ao objeto de solicitação (request object - req), ao objeto de resposta (response object - res) e à próxima função middleware no ciclo de solicitação-resposta da aplicação.

Eles são essenciais para manipular solicitações HTTP, executando várias funções intermediárias antes que a resposta final seja enviada de volta ao cliente. Os middlewares podem desempenhar uma variedade de funções, como:

1. **Manipulação de solicitação:** Podem modificar o objeto de solicitação (req), adicionando informações, validando dados, entre outros.
    
2. **Execução de código:** Realizam operações específicas antes de passar a solicitação para o próximo middleware na cadeia ou antes de enviar a resposta ao cliente.
    
3. **Controle de fluxo:** Podem decidir se uma solicitação deve continuar a ser processada ou ser interrompida com uma resposta específica.
    

Por exemplo, um middleware de registro de tempo pode registrar cada solicitação e a hora em que foi recebida. Outro middleware pode ser usado para autenticar usuários antes que eles possam acessar determinadas rotas. Eles podem ser incorporados na aplicação usando o método `app.use()` no Express, onde são chamados na ordem em que são declarados.

Os middlewares são uma parte poderosa da estrutura do Express, permitindo a criação de aplicativos flexíveis e modulares, onde várias funções podem ser adicionadas ou removidas facilmente para manipular as solicitações HTTP de acordo com as necessidades da aplicação.