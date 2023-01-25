# Questão 1: 
### Crie um algoritmo para calcular o IMC do usuário. Formula: IMC = peso / altura²
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

# Questão 2:
### Transformar uma temperatura de Fahrenheit para Celsius.
### TC = (TF - 32) / 1,8
### TC: Temperatura em Celsius.
### TF: Temperatura em Fahrenheit.

```Portugol
programa
{
	//Declaração das Variáveis
	real TC
	real TF

	funcao inicio()
	{
		//Entrada de dados
		escreva("Qual a temperatura em Fahrenheit: ")
		leia(TF)
		
		//Processamento de Dados
		TC = (TF - 32) / 1.8

		//Saída de Dados
		escreva("A temperatura " + TF + " °F" + "em Celsius é " + TC + "°C")
	}
}

````
