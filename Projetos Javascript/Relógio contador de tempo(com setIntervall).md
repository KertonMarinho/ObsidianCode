![[Pasted image 20240102103853.png|400]]
![[Pasted image 20240102105134.png|400]]


```js
function relogio() {
//função que aumenta de um segundo e retorna a data acrescido este segundos:
  function criaHoraDosSegundos(segundos) { 
    //js recebe em milésimos de segundos e a função está em segundos,para contornar  multiplica por 1000:
    const data = new Date(segundos * 1000); 
    return data.toLocaleTimeString('pt-BR', { //toLOcaleTiomeString: formatação que ja vem pronto no js

	hour12: false, //retira pm/am do relógio
	timeZone: 'UTC' //time zone(não considera a data,somente a hora,zerando a data e hora)como se fosse 1/1/1970 data incial do js(pode ser também GMT),tornado o relogio zerado 00:00:00.

    });}
const relogio = document.querySelector('.relogio');
let segundos = 0; //variável que mantém os segundos
let timer;

function iniciaRelogio() {  
    timer = setInterval(function() { //timer recebe e  atualização
//segundos é vizinha desta função, então não precisa usar uma variável e let
      segundos++;  //setInterval a cada um segundo será somado mais um

      relogio.innerHTML = criaHoraDosSegundos(segundos); //atualiza o innerHtml do relogio,tem que passar a um função se não ele não formatar os segundos

    }, 1000);}
    
document.addEventListener('click', function(e) {

    const el = e.target;//e.target :qual elemento está sendo clicado

   if (el.classList.contains('zerar')) {
//limpa sempr pE que dois time fuca brigando pelo milísegundos:
      clearInterval(timer); 
		relogio.innerHTML = '00:00:00';
		relogio.classList.remove('pausado'); //remove a classe pausado (relogio fica vermelho)
		segundos = 0; //volta a ser zero
		 }

   if (el.classList.contains('iniciar')) {
		relogio.classList.remove('pausado'); //remove a classe pausado(relogio fica vermelho)
		clearInterval(timer);
		iniciaRelogio();
		}
	if (el.classList.contains('pausar')) {
		clearInterval(timer);
		relogio.classList.add('pausado'); ///adciona a classe pausado
		}
	});
}
relogio();
```