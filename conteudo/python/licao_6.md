# Lição 6: Estrutura condicional - Declaração `if-elif-else`
Em Python, uma estrutura condicional pode ser composta de três partes:

1. Declarar apenas o `if` permite avaliar uma expressão e executar uma ação caso o valor avaliado seja verdadeiro;

    **Exemplo**
    ```python
    a = 10
    if a >= 10:
       print('O valor de "a" é:', a)
    ```

2. O `if-else` cria uma estrutura em que uma ação **X** é executada se uma condição for verdadeira ou executa uma ação
**Y** caso seja falsa;

    **Exemplo**
    ```python
    a = 10
    if a < 10:
       print('O valor de "a" é:', a)
    else:
       print('Valor impresso')
    ```

3. A estrutura `if-elif` é capaz de avaliar N condicionais e executar a primeira condição verdadeira;
    
    **Exemplo**
    ```python
    a = 10
    if a < 10:
       print('O valor de "a" é:', a)
    elif a == 10:
       print('Valor desejado impresso.')
    elif condicao_n:
       # Ação X
    # ...
    ```

4. Por fim, o `if-elif-else` é capaz de avalia N expressões, executar a ação da primeira que for verdadeira ou executar
executar a ação do `else` caso todas as expressões sejam falsas;

    **Exemplo**
    ```python
    a = 10
    if a < 10:
       print('O valor de "a" é:', a)
    elif a > 10:
       print('Não é esse valor')
    elif a != 10:
       print('Ainda não quero esse valor!')
    else:
       print('Essa ação será executada')
    ```

**Obs.:** É necessário conhecer os operadores de comparação mostrados na [Lição 4](licao_4.md).

##### Exercícios
1. Faça um programa que receba uma pontuação informada pelo usuário e imprima na tela uma mensagem de acordo com as
seguintes regras:
    1. Se a pontuação for igual a 10, imprima: `'Pontuação perfeita, parabéns!'`;
    2. Se for maior ou igual a 8.5 e menor que 10, imprima: `'É uma ótima pontuação, mas precisa melhorar.'`;
    3. Se for maior ou igual a 7 e menor que 8.5, imprima: `'Cuidado, essa pontuação não está boa!'`;
    4. Se for maior ou igual a 0 e menor que 7, imprima: `'Essa pontuação está muito ruim. Medidas extremas necessárias.'`
    5. Caso não esteja dentro do intervalo entre 0 e 10, imprima: `'Xiii, valor fora do intervalo!'`

2. Faça um programa para o cálculo de uma folha de pagamento, sabendo que os descontos são do Imposto de Renda, que 
depende do salário bruto (conforme tabela abaixo) e 3% para o Sindicato e que o FGTS corresponde a 11% do Salário Bruto,
 mas não é descontado (é a empresa que deposita). O Salário Líquido corresponde ao Salário Bruto menos os descontos. O
 programa deverá pedir ao usuário o valor da sua hora e a quantidade de horas trabalhadas no mês.
    
    Desconto do IR:
    2. Salário Bruto até 900 (inclusive) - isento
    3. Salário Bruto até 1500 (inclusive) - desconto de 5%
    4. Salário Bruto até 2500 (inclusive) - desconto de 10%
    5. Salário Bruto acima de 2500 - desconto de 20% Imprima na tela as informações, dispostas conforme o exemplo
    abaixo. No exemplo o valor da hora é 5 e a quantidade de hora é 220. 
    ```
    Salário Bruto: (5 * 220)        : R$ 1100,00
    (-) IR (5%)                     : R$   55,00
    (-) INSS ( 10%)                 : R$  110,00
    FGTS (11%)                      : R$  121,00
    Total de descontos              : R$  165,00
    Salário Liquido                 : R$  935,00
    ```

###### Referências
1. [Docs Python.org: "More Control Flow Tools"](https://docs.python.org/3/tutorial/controlflow.html#if-statements)
2. [DevMedia: "Python: Estrutura condicional if-else"](https://www.devmedia.com.br/python-estrutura-condicional-if-else/38217)
3. [Python Brasil: "EstruturaDeDecisao"](https://wiki.python.org.br/EstruturaDeDecisao)
