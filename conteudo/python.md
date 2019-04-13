# Conteúdos de Python

### Lição 1
Python considera todos os tipos como verdadeiros em operações lógicas, exceto:

* Constantes definidas para serem falsas: `None`, `False`;
* `0` de qualquer tipo numérico;
* Sequências e coleções vazias: `''`, `()`, `[]`, `{}`, `set()`, `range(0)`;
* Objetos com os métodos `__bool__()` ou `__len__()` retornarem, respectivamente, `False` ou `0`.

###### Referências
1. Python 3 docs: [docs.python.org](https://docs.python.org/3/library/stdtypes.html#truth-value-testing)

---

### Lição 2
Python possui 8 operadores de comparação que são listados abaixo:

|Operação | Significado                 | Método
|---------|-----------------------------|------------------
|< 	      | menor que                   | `__lt__()`
|<=       | menor ou igua à             | `__le__()`
|> 	      | maior que                   | `__gt__()`
|>=       | maior ou igual à            | `__ge__()`
|==       | igual                       | `__eq__()`
|!=       | diferente                   | `__eq__()`
|is       | identidade do objeto        | Não personalizável
|is not   | nega a identidade do objeto | Não personalizável

**ATENÇÃO**: O operador `is` verifica se duas variáveis aponta exatamente para o mesmo objeto em memória, não se seus
valores são iguais.

**Exemplo:**
```python
a = 1
b = 1
print(a == b, a is b) # Resultado: True, True

a = [1]
b = [1]
print(a == b, a is b) # Resultado: True, False
```

###### Referências
1. Python 3 docs: [docs.python.org](https://docs.python.org/3/library/stdtypes.html#comparisons)

---

### Lição 3
É possível utilizar operadores lógicos (`and`, `or`) como se fossem condicionais pra definir valores em variáveis.

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
