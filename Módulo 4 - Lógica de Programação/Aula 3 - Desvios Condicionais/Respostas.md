# Dicas:
### Para tester, crie normalmente seu projeto e cole os codigos apenas dentro da função main.
### Verifique o código sempre com os slides para conseguir abstrair o significado. 

# Questão 1: 
### Solicite um número ao usuário e mostre se o número é positivo ou negativo. Se o numero for positivo mostre se ele é impar ou par.
```C#
            //Declaração das Variáveis
           float numero = 0;

            //Entrada de Dados
            Console.Write("Digite um número: ");
            numero = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out numero);

            //Processamento e Saída de Dados
            if(numero % 2 == 0)
            {
                Console.WriteLine($"O número {numero} é PAR");
            }
            else
            {
                Console.WriteLine($"O número {numero} é IMPAR");
            }
            
```

# Questão 2:
### A cancela de um estabelecimento, em momento de pandemia, funciona dependendo da temperatura aferida e registrada pelo recepcionista do local. É preciso criar um algoritmo para liberar ou não a cancela dependendo da temperatura corporal. Com um medidor o recepcionista irá aferir e registrar no sistema e o algoritmo deverá liberar caso a temperatura seja <= 37 e não liberar caso a temperatura seja maior que 37º. A cancela só recebe True ou False (True para liberar e False para bloquear)

```C#
            //Declaração das Variáveis
            float temp = 0;
            bool liberar = false;

            //Entrada de Dados
            Console.Write("Qual a temperatura: ");
            temp = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out temp);

            //Processamento e Saídade Dados
            if(temp <= 37)
            {
                liberar = true;
                Console.WriteLine($"Cancela Liberada!");
            }
           else
           {
                liberar = false;
                Console.WriteLine($"Cancela Bloqueada!");
           }
````


# Questão 3:
### Leia um número real. Se o numero for positivo imprima a raiz quadrada. Do contrario,  imprima o numero ao quadrado. 
Use Math.Sqrt() para a raiz quadrada.
Use Math.Pow() para o numero ao quadrado.

```C#
            //Declaração das Variáveis
            float retangulo = 0.0f;
            float largura = 0.0f;
            float comprimento = 0.0f;

            //Entrada de Dados
            Console.Write("Qual a largura do retângulo em metros: ");
            largura = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out largura);

            Console.Write("Qual o comprimento do retângulo em metros: ");
            comprimento = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out comprimento);

            //Processamento de Dados
            retangulo = largura * comprimento;

            //Saída de Dados
            Console.WriteLine($"A área desse retângulo é {retangulo} metros quadrados");
````

# Questão 4:
### Escreva um algoritmo para ler o número total de eleitores de um município, o número de votos brancos, nulos e válidos. Calcular e escrever o percentual que cada um representa em relação ao total de eleitores.
### Dica: O total de eleitores será a soma de todos os votos

```C#
//Declaração das Variáveis
            int totalEleitores = 0;
            int totalValidos = 0;
            int totalNulos = 0;
            int totalBrancos = 0;

            float percValidos = 0.0f;
            float percNulos = 0.0f;
            float percBrancos = 0.0f;

            //Entrada de Dados
            Console.Write("Qual o total de votos válidos:  ");
            totalValidos = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out totalValidos);

            Console.Write("Qual o total de votos nulos:  ");
            totalNulos = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out totalNulos);

            Console.Write("Qual o total de votos brancos:  ");
            totalBrancos = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out totalBrancos);

            //Processamento de Dados
            totalEleitores = totalValidos + totalNulos + totalBrancos;
            percValidos = totalValidos / totalEleitores;
            percNulos = totalNulos / totalEleitores;
            percBrancos = totalBrancos / totalEleitores;

            //Saída de Dados
            Console.WriteLine($"O total de eleitores dessa cidade foi de {totalEleitores.ToString("0.00")} de eleitores");
            Console.WriteLine($"O percentual de votos validos foi {percValidos.ToString("0.00")} %");
            Console.WriteLine($"O percentual de votos nulos foi {percNulos.ToString("0.00")} %");
            Console.WriteLine($"O percentual de votos brancos foi {percBrancos.ToString("0.00")} %");
            //.ToString("0.00") serve para manilupar para 2 casas decimais.
````

# Questão 5: 
### Escreva um algoritmo que armazene o valor 10 em uma variável A e o valor 20 em uma variável B. A seguir (utilizando apenas atribuições entre variáveis) troque os seus conteúdos fazendo com que o valor que está em A passe para B e vice-versa. Ao final, escrever os valores que ficaram armazenados nas variáveis.

```C#
            //Entrada de Dados
            int A = 10;
            int B = 20;
            int C = 0;
            int D = 0;

            //Processamento de Dados
            C = A;
            D = B;
            A = D;
            B = C;

            //Saída de Dados
            Console.WriteLine($"Antes A tinha o valor {C}. Agora tem o valor {A}");
            Console.WriteLine($"Antes B tinha o valor {D}. Agora tem o valor {B}")

```

# Questão 6:
### O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos (aplicados ao custo de fábrica). Supondo que o percentual do distribuidor seja de 28% e os impostos de 45%, escreva um algoritmo para ler o custo de fábrica de um carro, calcular e mostrar o custo final ao consumidor.

```C#
            //Declaração das Variáveis
            float carroNovo = 0.0f;
            float custoFabrica = 0.0f;
            float percDistribuidor = 0.28f;
            float impostos = 0.45f;

            //Entrada de Dados
            Console.Write("Qual foi o custo para fabricar o carro R$: ");
            custoFabrica = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out custoFabrica);

            //Processamento de Dados
            carroNovo = custoFabrica * impostos + custoFabrica * percDistribuidor + custoFabrica;

            //Saída de Dados
            Console.WriteLine($"O valor do novo carro é de R$ {carroNovo.ToString("0.00")}");

```
