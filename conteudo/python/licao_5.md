# Lição 5: Operadores lógicos `and`, `or` e `not`
A lista de operadores booleanos abaixo está ordenada por ordem de prioridade ascendente:

| Operação | Teste Lógico
|----------|-------------------------------------------
|`x or y`  |Se `x` é falso, então `y`, senão `x`
|`x and y` |Se `x` é falso, então `x`, senão `y`
|`not x`   |Se `x` é false, então `True`, senão `False`

1. Ao executar o operador `or`, o valor seguinte será avaliado somente se o primeiro valor for Falso;
2. Para o operador `and`, o valor seguinte será avaliado se o primeiro for verdadeiro.

É possível utilizar esses operadores lógicos como se fossem condicionais pra definir valores em variáveis.

**Exemplo:**
```python
a = 4

# Atribuição com "if"
if a:
    b = a * 5
else:
    b = a

# Atrubuição com operador lógico "and"
b = a and a*5
# Resultado: 20

a = 0
b = a and a*5
# Resultado: 0
```

Para o operador `and`, se todos os valores forem verdadeiros, o valor retornado será o último valor. 
Caso haja algum falso, o primeiro valor falso será retornado.

**Exemplo:**  
```python
a = 1 and 2 and 3
# Resultado: 3

a =  True and False and 5
# Resultado: False

a = 6 and -1 and 0
# Resultado: 0
```

Para o operador "or", o valor assumido será o primeiro verdadeiro ou, se tudo for falso, o último valor falso. 

```python
print(1 or 3 or 0) # Resultado: 1
print(0 or 5 or 9) # Resultado 5
```

##### Excercício
1. Sem utilizar `if-elif-else`, faça com que a variável `saida` tenha seu valor definido baseado nas seguintes regras:
    * Se `entrada == "[*]"`, então `saida = "[{pos}]"`;
    * Se `entrada.starswith("[")`, então `saida = entrada`;
    * Caso contrário, `saida = entrada * 3`.

###### Referências
1. [Docs Python.org: "Built-in Types"](https://docs.python.org/3/library/stdtypes.html#boolean-operations-and-or-not)
