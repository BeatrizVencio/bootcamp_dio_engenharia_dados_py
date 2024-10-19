# Explorando Conjuntos em Python

### Aula 1 - Conjuntos

Esta aula nos apresenta o conceito de **conjuntos** em Python, explorando suas características únicas e como usá-los para trabalhar com coleções de elementos distintos.

**O que são Conjuntos?**

- **Conjuntos** (sets) são coleções desordenadas de elementos que não podem conter valores duplicados.
- Usados para representar conjuntos matemáticos ou para remover itens duplicados de um iterável.
- São representados por chaves `{}`.

**Por que usar Conjuntos?**

- **Elementos Únicos:** Garante que cada elemento em um conjunto seja único, eliminando duplicações automaticamente.
- **Operações de Conjuntos:** Python fornece operações eficientes para conjuntos, como união, interseção e diferença.
- **Teste de Pertinência:** Verifica se um elemento está presente em um conjunto de forma eficiente usando `in`.

**Criando Conjuntos em Python:**

- Use chaves `{}` para delimitar os elementos do conjunto.
- Separe os elementos por vírgulas.
- Você pode criar conjuntos vazios ou inicializá-los com dados.

**Exemplos:**

```python
# Conjunto de números
numeros = {1, 2, 3, 1, 4, 2, 5}
print(numeros)
>>> {1, 2, 3, 4, 5} # Note que os duplicados foram removidos

# Conjunto de letras
letras = {"a", "b", "a", "c", "x", "i"}
print(letras)
>>> {"a", "b", "c", "i", "x"}

# Criando um conjunto a partir de uma lista
carros = ["gol", "celta", "palio", "gol", "celta"]
conjunto_carros = set(carros)
print(conjunto_carros)
>>> {"gol", "celta", "palio"}

```

**Acessando elementos de um conjunto:**

- Conjuntos **não são indexados** e não suportam acesso direto por índices, como listas ou tuplas.
- Para acessar os elementos, você geralmente precisa iterar sobre eles, usando um laço `for`.
- **`list(conjunto)`:** Se você precisa acessar os elementos de um conjunto em uma ordem específica, você pode convertê-lo para uma lista usando a função `list()`.

**Operações com Conjuntos:**

- **União (`|` ou `.union()`):** Combina dois conjuntos, incluindo todos os elementos de ambos.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {3, 4, 5}
    uniao = conjunto_a | conjunto_b
    print(uniao)
    >>> {1, 2, 3, 4, 5}
    
    ```
    
- **Interseção (`&` ou `.intersection()`):** Retorna os elementos que estão presentes em ambos os conjuntos.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {2, 3, 4}
    intersecao = conjunto_a & conjunto_b
    print(intersecao)
    >>> {2, 3}
    
    ```
    
- **Diferença (`` ou `.difference()`):** Retorna os elementos que estão presentes no primeiro conjunto, mas não no segundo.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {2, 3, 4}
    diferenca = conjunto_a - conjunto_b
    print(diferenca)
    >>> {1}
    
    ```
    
- **Diferença Simétrica (`^` ou `.symmetric_difference()`):** Retorna os elementos que estão presentes em um conjunto, mas não em ambos.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {2, 3, 4}
    diferenca_simetrica = conjunto_a ^ conjunto_b
    print(diferenca_simetrica)
    >>> {1, 4}
    
    ```
    
- **Subconjunto (`<=` ou `.issubset()`):** Verifica se todos os elementos de um conjunto estão presentes em outro conjunto.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {1, 2, 3, 4, 5}
    print(conjunto_a <= conjunto_b)
    >>> True
    
    ```
    
- **Superconjunto (`>=` ou `.issuperset()`):** Verifica se um conjunto contém todos os elementos de outro conjunto.
    
    ```python
    conjunto_a = {1, 2, 3, 4, 5}
    conjunto_b = {1, 2, 3}
    print(conjunto_a >= conjunto_b)
    >>> True
    
    ```
    
- **Disjunto (`isdisjoint()`):** Verifica se dois conjuntos não possuem elementos em comum.
    
    ```python
    conjunto_a = {1, 2, 3}
    conjunto_b = {4, 5, 6}
    print(conjunto_a.isdisjoint(conjunto_b))
    >>> True
    
    ```
    

### Materiais Complementares

[Conjuntos.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/cd0c608e-d7f4-4e01-93d8-29b8059a7381/Conjuntos.pdf)