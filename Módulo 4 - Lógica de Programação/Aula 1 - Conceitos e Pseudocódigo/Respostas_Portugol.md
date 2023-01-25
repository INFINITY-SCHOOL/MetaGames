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


# Questão 3:
### Escreva um algoritmo para ler as dimensões de um retângulo (largura e comprimento), calcular e escrever a área do retângulo.
### retangulo = largura * comprimento

```Portugol
programa
{
	//Declaração das Variáveis
	real retangulo
	real largura
	real comprimeto

	funcao inicio()
	{
		//Entrada de dados
		escreva("Qual a largura do retângulo em metros: ")
		leia(largura)
		
		escreva("Qual o comprimeto do retângulo metros: ")
		leia(comprimeto)
		
		//Processamento de Dados
		retangulo = largura * comprimeto

		//Saída de Dados
		escreva("A área desse retângulo é " + retangulo + "metros quadrados")
	}
}
````

# Questão 4:
### Escreva um algoritmo para ler o número total de eleitores de um município, o número de votos brancos, nulos e válidos. Calcular e escrever o percentual que cada um representa em relação ao total de eleitores.
### Dica: O total de eleitores será a soma de todos os votos

```Portugol
programa
{
	//Declaração das Variáveis
	inteiro totalEleitores
	inteiro totalValidos
	inteiro totalNulos
	inteiro totalBrancos

	real percValidos
	real percNulos
	real percBrancos

	funcao inicio()
	{
		//Entrada de dados
		escreva("Qual o total de votos válidos: ")
		leia(totalValidos)
		
		escreva("Qual o total de votos nulos: ")
		leia(totalNulos)

		escreva("Qual o total de votos brancos: ")
		leia(totalBrancos)
		
		//Processamento de Dados
		totalEleitores = totalValidos + totalNulos + totalBrancos
		percValidos = totalValidos / totalEleitores
		percNulos = totalNulos / totalEleitores
		percBrancos = totalBrancos / totalEleitores

		//Saída de Dados
		escreva("O total de eleitores dessa cidade foi de : " + totalEleitores + " de eleitores \n")
		escreva("O percentual de votos validos foi : " + percValidos + "% \n")
		escreva("O percentual de votos nulos foi : " + percNulos + "% \n")
		escreva("O percentual de votos brancos foi : " + percBrancos + "% \n")
		
	}
}
````

# Questão 5: 
### Escreva um algoritmo que armazene o valor 10 em uma variável A e o valor 20 em uma variável B. A seguir (utilizando apenas atribuições entre variáveis) troque os seus conteúdos fazendo com que o valor que está em A passe para B e vice-versa. Ao final, escrever os valores que ficaram armazenados nas variáveis.

```Portugol
programa
{
	//Declaração das Variáveis
	funcao inicio()
	{
		//Entrada de dados
		inteiro A = 10
		inteiro B = 20
		inteiro C
		inteiro D
		
		//Processamento de Dados
		C = A
		D = B
		A = D
		B = C

		//Saída de Dados
		escreva("Antes A tinha o valor " + C + ". Agora tem o valor" + A + "\n")
		escreva("Antes B tinha o valor " + D + ". Agora tem o valor" + B + "\n")
	}
}

```

# Questão 6:
### O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos (aplicados ao custo de fábrica). Supondo que o percentual do distribuidor seja de 28% e os impostos de 45%, escreva um algoritmo para ler o custo de fábrica de um carro, calcular e mostrar o custo final ao consumidor.

```Portugol
programa
{
	//Declaração das Variáveis
	real carroNovo
	real custoFabrica
	real percDistribuidor = 0.28
	real impostos = 0.45

	funcao inicio()
	{
		//Entrada de dados
		escreva("Qual foi o custo para fabricar o carro R$: ")
		leia(custoFabrica)
		
		//Processamento de Dados
		carroNovo = custoFabrica + custoFabrica * percDistribuidor + custoFabrica * impostos

		//Saída de Dados
		escreva("O valor do novo carro é de R$" + carroNovo)
		
	}
}

```
