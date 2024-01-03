![[Pasted image 20240102221044.png|410]]
![[Pasted image 20240102221134.png|400]]


```js
const inputTarefa = document.querySelector('.input-tarefa');
const btnTarefa = document.querySelector('.btn-tarefa');
const btUrgencia = document.querySelector('.btn-Urgencia');
const tarefas = document.querySelector('.tarefas');

//essa função é unicamente para criar i li
function criaLi() { 
	const li = document.createElement('li');
	return li;
}
//quando precionar enter a lista é criada
inputTarefa.addEventListener('keypress', function(e) { 
	if (e.keyCode === 13) {
	if (!inputTarefa.value) return; //se input tiver um valor cria a terafa, vazio retorna. 
		criaTarefa(inputTarefa.value);
	}
});
//limpa input e adcionado input e volta parra ser digitado,com essa funcção vc não precisa sair do campo parra adcionar nova  tarefa
function limpaInput() { 
	inputTarefa.value = '';//limpa o valor que tiver no input
	inputTarefa.focus();  //coloca um cursor e fica piscando
}
function criaBotaoApagar(li) {  //li: local aonde vai ser adicionado o botão
	li.innerText += ' ';  //adciona um espaço entre o texto e o botão
	const botaoApagar = document.createElement('button');
	botaoApagar.innerText = 'Apagar'; //texto que aparece no botão

  // botaoApagar.classList.add('apagar');
	botaoApagar.setAttribute('class', 'apagar');//seta o atributo(class) e adciona class apagar
	botaoApagar.setAttribute('title', 'Apagar esta tarefa');//aparece o texto(apagar essa tarefa)quando passa o mouse
	li.appendChild(botaoApagar);
};

btUrgencia.addEventListener('click', function() {
	const li = document.querySelector('li:last-child'); // pega a última li criada
	li.classList.toggle('vermelho'); // adiciona ou remove a classe "vermelho"
});

function criaTarefa(textoInput) {
	const li = criaLi(); //esse const li pega a li que esta na outra função(criaLI)
	li.innerText = textoInput;
	tarefas.appendChild(li);//coloca o Li na class tarefa
	limpaInput();
	criaBotaoApagar(li);
	salvarTarefas();
}
//function btnColor(){
//  return document.querySelector('li').style.color ='#ff0000';
btnTarefa.addEventListener('click', function() {
	if (!inputTarefa.value) return; //hífen com uma linha só não precisa de chaves
	criaTarefa(inputTarefa.value); //joga o texto(input.tarefa)para outra função(criaTarefa)
});
//apaga o lelmentyo da  lista
document.addEventListener('click', function(e) {  //apaga o lelmentyo da  lista
	const el = e.target; //pega o elemento que está sendo crickado

	if (el.classList.contains('apagar')) {
		el.parentElement.remove(); //remove o pai do botão(no caso o li)
		salvarTarefas();//salva as tarefas para remove do localStorage
	}
});
function salvarTarefas() {
	const liTarefas = tarefas.querySelectorAll('li'); //ver quando de tarefas tem(li)
	const listaDeTarefas = [];

   for (let tarefa of liTarefas) {
		let tarefaTexto = tarefa.innerText;//pega o texto da tarefa
		tarefaTexto = tarefaTexto.replace('Apagar', '').trim();//para que não apareeça a palavra apagar do botão  no array o replace irá substituir por nada.  //função trim remove espaços sobrandos

    listaDeTarefas.push(tarefaTexto);//pega o texto tarefa texto e adiciona em lista de tarefas
	}
//converte array em json string
  const tarefasJSON = JSON.stringify(listaDeTarefas);//converte array em json string
//localStorage:local onde pode quardar coisas no navegador,mini base da dados.

//primeiro paramêtro nome do local que vai salva(renomeia),segundo parâmetros tarefas o que vai salvar(neste cao tarefasJson)
  localStorage.setItem('tarefas', tarefasJSON);//terfas:nome que será recuperar a lista
}
//obter as terafas salvas no locastorage:
function adicionaTarefasSalvas() { //recupeaas as tarefas logo depois que o navegador se aberto
	const tarefas = localStorage.getItem('tarefas');//obten os item pelos nomes que vc setou as tarefas
	const listaDeTarefas = JSON.parse(tarefas);//converte as tarefas em array de volta
	for(let tarefa of listaDeTarefas) { //cria as tarefas com o que foi salva no storage
		criaTarefa(tarefa);
	}
}
adicionaTarefasSalvas();
```

>[!Local storage]
>Local do LocalSotrage no console do navegador
>console->aplication->LocalStorage->site aberto->aonde está a lista


