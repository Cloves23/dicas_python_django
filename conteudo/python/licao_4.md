# Lição 4: Operadores de comparação
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
1. [Docs Python.org: "Built-in Types"](https://docs.python.org/3/library/stdtypes.html#comparisons)
