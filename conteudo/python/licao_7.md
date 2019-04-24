# Lição 7: Tipos com valores verdadeiros e falsos
Python considera todos os tipos como verdadeiros em operações lógicas, exceto:

* Constantes definidas para serem falsas: `None`, `False`;
* `0` de qualquer tipo numérico;
* Sequências e coleções vazias: `''`, `()`, `[]`, `{}`, `set()`, `range(0)`;
* Objetos com os métodos `__bool__()` ou `__len__()` retornarem, respectivamente, `False` ou `0`.

###### Referências
1. Python 3 docs: [docs.python.org](https://docs.python.org/3/library/stdtypes.html#truth-value-testing)
