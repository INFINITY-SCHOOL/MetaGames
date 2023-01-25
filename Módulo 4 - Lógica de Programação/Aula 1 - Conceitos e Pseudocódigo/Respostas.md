# Questão 1: Crie um algoritmo para calcular o IMC do usuário. Formula: IMC = peso / altura²
```Portugol
programa
{
//Declaração das Variáveis
	real imc
	real peso
	real altura
	funcao inicio()
	{
	//Entrada de dados
		escreva("Qual a sua altura: ")
		leia(altura)
		escreva("Qual seu peso: ")
		leia(peso)

  //Processamento de Dados
	  imc = peso / (altura * altura)

   //Saída de Dados
	   escreva("Seu IMC é de " + imc)
  }
}
```
