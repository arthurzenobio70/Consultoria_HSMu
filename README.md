# Consultoria_HSMu
var entrevistados = 0;
var menosDe10 = [];
var entre10e15 = [];
var maisDe15 = [];

var pergunta = prompt('Deseja participar da pesquisa?');

while(pergunta == 'sim' || pergunta == 'desejo' || pergunta == 'Sim'){
	entrevistados ++;
	var vezes = prompt('Quantas vezes você utilizou o Restaurante Universitário neste mês?');
	if (vezes < 10){
		menosDe10.push(vezes);
	} else if(vezes >=10 && vezes <=15){
		entre10e15.push(vezes);
	} else{
		maisDe15.push(vezes);
	}
	alert('Obrigada pelas respostas!');	
	pergunta = prompt('Deseja participar da pesquisa?');
}

var porcMenos10 = (entrevistados * menosDe10.length)/ 100;
var porc10 = (porcMenos10*100).toFixed(2);
var porcEntre10e15 = (entrevistados * entre10e15.length)/ 100;
var porc10e15 = (porcEntre10e15*100).toFixed(2);
var porcMais15 = (entrevistados * maisDe15.length)/ 100;
var porc15 = (porcMais15*100).toFixed(2);
document.write("A quantidade de alunos entrevistados foi de: "+ entrevistados + ' alunos.');
document.write("<br> O percentual de alunos que utilizaram menos de 10 vezes o restaurante é: " + porc10 + '%.');
document.write("<br> O percentual de alunos que utilizaram entre 10 e 15 vezes é: " + porc10e15 + '%.');
document.write("<br> O percentual de alunos que utilizaram o restaurante acima de 15 vezes é: " + porc15 + '%.');
