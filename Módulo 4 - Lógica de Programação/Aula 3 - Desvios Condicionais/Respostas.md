# Dicas:
### Para tester, crie normalmente seu projeto e cole os codigos apenas dentro da função main.
### Verifique o código sempre com os slides para conseguir abstrair o significado. 
### Caso esteja usando o Visual Studio Community, utiline o comando Console.ReadLine() no final do código. Se for o VS Code não há necessidade.

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
### Leia um número real. Se o numero for positivo imprima a raiz quadrada. Do contrário,  imprima o número ao quadrado. 
#### Use Math.Sqrt() para a raiz quadrada.
#### Use Math.Pow() para o número ao quadrado.

```C#
            //Declaração das Variáveis
            float numero = 0;

            //Entrada de Dados
            Console.Write("Digite um número: ");
            numero = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out numero);

            //Processamento e Saída de Dados
            if(numero > 0)
            {
                float raiz = (float)Math.Sqrt(numero) //O float entre parentese se chama Cast, ele serve para converter o valor do Math.Sqrt() que é em double para float.
                Console.WriteLine($"Como o número {numero} é positivo, sua raiz quadrada é {raiz}");
            }
            else if(numero <> 0)
            {
                float quadrado = (float)Math.Pow(numero, 2) //O float entre parentese se chama Cast, ele serve para converter o valor do Math.Sqrt() que é em double para float.
                Console.WriteLine($"Como o número {numero} é negativo, seu quadrada é {quadrado}");
            }
            
````

# Questão 4:
### A Secretaria de Meio Ambiente que controla o índice de poluição mantém 3 grupos de indústrias que são altamente poluentes do meio ambiente. 
#### O índice de poluição aceitável varia de 0,05 até 0,3. Se o índice sobe para 0,3 as indústrias do 1º grupo são intimadas a suspenderem suas atividades, se o índice crescer para 0,4 as indústrias do 1º e 2º grupo são intimadas a suspenderem suas atividades, se o índice atingir 0,5 todos os grupos devem ser notificados a paralisarem suas atividades. Faça um algoritmo que leia o índice de poluição medido e emita a notificação adequada aos diferentes grupos de empresas.

```C#
            //Declaração das Variáveis
            float indicePoluicao = 0.0f;
            
            //Entrada de Dados
            Console.Write("Qual o índice de poluição:  ");
            indicePoluicao = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out indicePoluicao);

            //Processamento e Saída de Dados
            if(indicePoluicao < 0.05f)
            {
                Console.WriteLine($"Índice de Poluição: {indicePoluicao}. Abaixo do esperado.");
            }
            else if(indicePoluicao >= 0.05f && indicePoluicao < 0.3f)
            {
                Console.WriteLine($"Índice de Poluição: {indicePoluicao}. Faixa normal de trabalho.");
            }
            else if(indicePoluicao >= 0.3f && indicePoluicao > 0.4f)
            {
                Console.WriteLine($"Índice de Poluição: {indicePoluicao}. Acima do esperado. Notificação de Alerta para o Grupo 1.");
            }
            else if(indicePoluicao >= 0.4f && indicePoluicao > 0.5f)
            {
                Console.WriteLine($"Índice de Poluição: {indicePoluicao}. Acima do esperado. Notificação de Alerta para os Grupos 1 e 2.");
            }
            else if(indicePoluicao >= 0.5f)
            {
                Console.WriteLine($"Índice de Poluição: {indicePoluicao}. Acima do esperado. Notificação de Alerta para todos Grupos.");
            }
````

# Questão 5: 
### Ler o nome de 2 times e o número de gols marcados na partida (para cada time). E no final escrever o nome do vencedor. Caso não haja vencedor deverá ser impressa a palavra EMPATE.

```C#
            //Declaração das Variáveis
            string time1 = "";
            string time2 = "";
            int gols1 = 0;
            int gols2 = 0;

            //Entrada de Dado
             //Entrada de Dados
            Console.Write("Qual o time 1:  ");
            time1 = Console.ReadLine();
            Console.Write("Qual o time 2:  ");
            time2 = Console.ReadLine();

            Console.Write($"Quantos gols o time {time1} marcou: ");
            gols1 = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out gols1);
            Console.Write($"Quantos gols o time {time2} marcou: ");
            gols2 = int.Parse(Console.ReadLine());
            //ou esse
            //int.TryParse(Console.ReadLine(), out gols2);

            //Processamento de Dados

            if(gols1 > gols2)
            {
                Console.WriteLine($"Time {time1} venceu.");
            }
            if(gols1 < gols2)
            {
                Console.WriteLine($"Time {time2} venceu.");
            }
            else
            {
                Console.WriteLine($"EMPATE.");
            }

```

# Questão 6:
### Desenvolva um algoritmo que solicite o preço de três produtos e informe qual produto deve ser comprado, sabendo que a decisão é sempre pelo mais barato.

```C#
            //Declaração das Variáveis
            float prod1 = 0;
            float prod2 = 0;
            float prod3 = 0;

            //Entrada de Dados
            Console.Write("Qual o preço do primeiro produto? R$: ");
            prod1 = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out prod1);
            Console.Write("Qual o preço do segundo produto? R$: ");
            prod2 = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out prod2);
            Console.Write("Qual o preço do terceiro produto? R$: ");
            prod3 = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out prod3);

            //Processamento e Saída de Dados
            if(prod1 > prod2 > prod3)
            {
                Console.WriteLine($"Compre o produto 3.");
            }
            else if(prod3 > prod1 > prod2)
            {
                Console.WriteLine($"Compre o produto 2.");
            }
            else if(prod2 > prod3 > prod1)
            {
                Console.WriteLine($"Compre o produto 1.");
            }
            
```
# Questão 7:
### Uma empresa quer verificar se um empregado está qualificado para a aposentadoria ou não. Para isso tem que se ter um dos seguintes requisitos:
#### 1) Ter no mínimo 65 anos de idade. 
#### 2) Ter trabalhado no mínimo 30 anos. 
#### 3) Ter no mínimo 60 anos e ter trabalhado no mínimo 25 anos. 

### Faça um algoritmo que leia: o número do empregado (código), o ano de seu nascimento e o ano de seu ingresso na empresa. O programa deverá escrever a idade e o tempo de trabalho do empregado e a mensagem 'Requerer aposentadoria' ou 'Não requerer'.
### Use: DateTime.Now.Year, para pegar o valor do ano atual.

```C#
            //Declaração das Variáveis
            int codigo = 0;
            int anoNascimento = 0;
            int anoContratacao = 0;
            int idade = 0;
            int tempoTrabalhado = 0;

            //Entrada de Dados
            Console.Write("Qual o número do empregado (código): ");
            codigo = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out codigo);
            Console.Write("Qual o ano de seu nascimento: ");
            anoNascimento = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out anoNascimento);
            Console.Write("Qual o ano de seu ingresso na empresa: ");
            anoContratacao = float.Parse(Console.ReadLine());
            //ou esse
            //float.TryParse(Console.ReadLine(), out anoContratacao);

            //Processamento Dados 
            
            idade =  DateTime.Now.Year - anoNascimento;
            tempoTrabalhado = DateTime.Now.Year - anoContratacao;

            //Saída de Dados
            if(idade >= 65 || tempoTrabalhado >= 30 || (idade >= 60 && tempoTrabalhado >= 25))
            {
                Console.WriteLine($"Idade: {idade}. Tempo trabalhado: {tempoTrabalhado}. Requerer aposentadoria.");
            }
            else 
            {
                Console.WriteLine($"Idade: {idade}. Tempo trabalhado: {tempoTrabalhado}. Não requerer.");
            }
            
            
```