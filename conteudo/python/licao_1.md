# Lição 1: Tipos de dados
Python é uma linguagem que possui **tipagem dinâmica e forte**. Ela possui `tipo dinâmico` porque a mesma variável pode
assumir valores de tipos diferentes em tempo de execução:

**Exemplo:**
```python
>>> variavel = 1      # Inteiro
>>> variavel = '1'    # String
>>> variavel = False  # Booleano
```

Ela é fortemente tipada porque operações são realizadas somente entre tipos compatíveis, ou seja, não é realizado
conversões implícitas entre tipos de dados diferentes e incompatíveis.

**Exemplo:**
```python
>>> '1' + 2
Traceback (most recent call last):
  File "<input>", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'str' and 'int'
>>> 5 + 3
7
>>> '5' + '3' + 'a'
'53a'
```

Para a operação de multiplicação, pode-se dizer que há um caso especial onde é possível multiplicar uma string com um
inteiro qualquer. O resultado do processo será uma nova string repetida N vezes.

**Exemplo:**
```python
>>> '5' * 3
'555'
>>> 'a' * 2
'aa'
```

### Tipos Básicos
Os tipos básicos mais difundidos da linguagem são:

* Numérico: `int` e `float`
    * `int`: Número inteiro;
    * `float`: Número real, com ponto flutuante.
* Caracteres: `str`
    * `str`: Sequência imutável de caracteres.
* Booleano (Verdadeiro ou Falso): `bool`
    * `bool`: True ou False
* Coleção de dados: `list` e `tuple`
    * `list`: Coleção mutável  de dados de qualquer tipo, seja string, inteiro, booleano ou qualquer outro tipo.
    
        **Exemplo**
        ```python
        >>> a = [2, 'a', False, None, -5.3]
        >>> a
        [2, 'a', False, None, -5.3]
        >>> a[0] = 4
        >>> a
        [4, 'a', False, None, -5.3]
        ```
    * `tuple`: Coleção imutável  de dados de qualquer tipo. Isso quer dizer que, uma vez definido seus valores, não será 
    possível modificá-los
        
        **Exemplo**
        ```python
        >>> a = (2, 1, 3, 3)
        >>> a
        (2, 1, 3, 3)
        >>> a[0] = 5
        Traceback (most recent call last):
          File "<input>", line 1, in <module>
        TypeError: 'tuple' object does not support item assignment
        ```
* Conjuntos: `set`
    * `set`: Lista de valores arbitrários de valores únicos. Nesse tipo de dado é possível aplicar operações de 
    conjuntos matemáticos, tal como, união, interseção e diferença. Um conjuto (`set`), pode ser criado a partir de
    sequências como `list`, `tuple` e `str`.
        
        **Exemplos**
        ```python
        >>> set([1, 1, 2, 3]) # Criando com uma lista
        {1, 2, 3}
        >>> set((3, 1, 2, 2)) # Criando com uma tupla
        {1, 2, 3}
        >>> {4, 1, 1, 2, 2, 3} # Criando com chaves
        {1, 2, 3, 4}
        >>> set('bbacc') # Criando com uma string
        {'a', 'b', 'c'}
        ```
 
* Mapeamento de dados: `dict`
    * `dict`: Mapeamento de dados que cria um par de chave/valor não ordenado. A chave pode ter quase qualquer tipo de 
    valor, de tipos que possa-se criar um código hash (código numérico e único que identifica um objeto). Para o valor,
    não há restrição de tipos, pode ser qualquer coisa.
        
        **Exemplos**
        ```python
        >>> {'chave_1': 'valor X', 'chave_n': 'valor Y'}
        {'chave_1': 'valor X', 'chave_n': 'valor Y'}
        >>> {True: 123}
        {True: 123}
        >>> {None: {1, 1, 4, 2}}
        {None: {1, 2, 4}}
        >>> {(1, 'x'): '432'}
        {(1, 'x'): '432'}
        >>> {[3, 3]: 'teste'}
        Traceback (most recent call last):
          File "<input>", line 1, in <module>
        TypeError: unhashable type: 'list'
        >>> {(1, ['a']): '432'}
        Traceback (most recent call last):
          File "<input>", line 1, in <module>
        TypeError: unhashable type: 'list'
        ```
    
###### Referências
1. [Docs Python.org: "Built-in Types"](https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex)
2. [Tutorial Point: "Python 3 - Variable Types"](https://www.tutorialspoint.com/python3/python_variable_types.htm)
3. [Techopedia: "Hash Code"](https://www.techopedia.com/definition/25432/hash-code)
4. [Real Python: "The Ultimate Guide to Python Type Checking"](https://realpython.com/python-type-checking/)
