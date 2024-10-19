# Trabalhando com Listas em Python

### Aula 1 - Listas: Criação e acesso aos dados

Nesta aula, vimos os conceito de **listas** em Python e nos ensina como criar e acessar os dados que elas armazenam.

**O que são listas?**

- Listas são estruturas de dados que permitem armazenar sequencias de elementos.
- Cada elemento de uma lista pode ser de um tipo de dado diferente, inclusive listas aninhadas, possibilitando criar estruturas bidimensionais, como tabelas.
- Listas são mutáveis: Você pode alterar os valores de seus elementos depois de criá-las.

**Criando listas em Python:**

- Use colchetes (`[]`) para delimitar os elementos da lista.
- Separe os elementos por vírgulas.
- Você pode criar listas vazias ou inicializá-las com dados.

**Exemplos:**

```python
# Lista de frutas
frutas = ["laranja", "maçã", "uva"]

# Lista vazia
frutas = []

# Lista de números
numeros = [1, 2, 3, 4, 5]

# Lista de diferentes tipos
carro = ["Ferrari", "F8", 420000, 2018, "São Paulo", True]

```

**Acessando elementos de uma lista:**

- Listas são indexadas, começando do índice 0.
- Use colchetes (`[]`) com o índice do elemento desejado para acessá-lo.

**Exemplos:**

```python
frutas = ["laranja", "maçã", "uva"]

# Acessando o primeiro elemento
print(frutas[0])
>>> laranja

# Acessando o último elemento
print(frutas[-1])
>>> uva

# Acessando o segundo elemento
print(frutas[1])
>>> maçã

```

**Indicações Negativas:**

- Uma forma de acessar elementos a partir do fim da lista é usando índices negativos, em que -1 se refere ao último elemento, -2 ao penúltimo, e assim por diante.

**Listas aninhadas:**

- Você pode criar listas que armazenam outras listas, formando estruturas multidimensionais.
- Para acessar elementos em listas aninhadas, use dois índices.

**Exemplo:**

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Acessando o elemento na linha 1 e coluna 2
print(matriz[1][2])
>>> 6

```

### Aula 2 - Métodos da classe list

A segunda aula da série "Listas em Python" mergulha nos métodos que a classe `list` oferece, ferramentas para manipular e transformar listas de forma eficiente.

**Compreendendo Métodos:**

- **Métodos** são funções que pertencem a um objeto (nesse caso, um objeto do tipo `list`).
- Acessamos métodos usando o ponto (`.`) após o nome da lista, seguido do nome do método e parênteses.
- Métodos podem modificar a lista original, ou retornar uma nova lista, dependendo do método.

**Métodos da Classe `list`:**

1. **`append(elemento)`:** Adiciona um elemento ao final da lista.
    
    ```python
    frutas = ["maçã", "banana"]
    frutas.append("uva")
    print(frutas)
    >>> ["maçã", "banana", "uva"]
    
    ```
    
2. **`clear()`:** Remove todos os elementos da lista.
    
    ```python
    frutas = ["maçã", "banana", "uva"]
    frutas.clear()
    print(frutas)
    >>> []
    
    ```
    
3. **`copy()`:** Cria uma cópia independente da lista original.
    
    ```python
    frutas = ["maçã", "banana", "uva"]
    copia_frutas = frutas.copy()
    copia_frutas.append("morango")
    print(frutas)
    >>> ["maçã", "banana", "uva"]
    print(copia_frutas)
    >>> ["maçã", "banana", "uva", "morango"]
    
    ```
    
4. **`count(elemento)`:** Conta quantas vezes um elemento aparece na lista.
    
    ```python
    cores = ["vermelho", "azul", "verde", "azul"]
    print(cores.count("azul"))
    >>> 2
    
    ```
    
5. **`extend(iterável)`:** Adiciona todos os elementos de um iterável (como outra lista, string, tupla, etc.) ao final da lista atual.
    
    ```python
    linguagens = ["python", "js", "c"]
    linguagens.extend(["java", "csharp"])
    print(linguagens)
    >>> ["python", "js", "c", "java", "csharp"]
    
    ```
    
6. **`index(elemento)`:** Retorna o índice da primeira ocorrência de um elemento na lista.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    print(linguagens.index("java"))
    >>> 3
    
    ```
    
7. **`insert(índice, elemento)`:** Insere um elemento em uma posição específica na lista.
    
    ```python
    frutas = ["maçã", "uva"]
    frutas.insert(1, "banana")
    print(frutas)
    >>> ["maçã", "banana", "uva"]
    
    ```
    
8. **`pop()`:** Remove e retorna o último elemento da lista. Se um índice for fornecido, remove e retorna o elemento nesse índice.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    ultimo_elemento = linguagens.pop()
    print(ultimo_elemento)
    >>> csharp
    print(linguagens)
    >>> ["python", "js", "c", "java"]
    
    ```
    
9. **`remove(elemento)`:** Remove a primeira ocorrência de um elemento da lista.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    linguagens.remove("c")
    print(linguagens)
    >>> ["python", "js", "java", "csharp"]
    
    ```
    
10. **`reverse()`:** Inverte a ordem dos elementos da lista.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    linguagens.reverse()
    print(linguagens)
    >>> ["csharp", "java", "c", "js", "python"]
    
    ```
    
11. **`sort()`:** Ordena a lista em ordem crescente (alfabética para strings, numérica para números) e modifica a lista original.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    linguagens.sort()
    print(linguagens)
    >>> ["c", "csharp", "java", "js", "python"]
    
    ```
    
12. **`sorted(iterável)`:**  Retorna uma nova lista ordenada, não modificando o iterável original.
    
    ```python
    linguagens = ["python", "js", "c", "java", "csharp"]
    lista_ordenada = sorted(linguagens)
    print(linguagens)     
    >>> ["python", "js", "c", "java", "csharp"]
    
    print(lista_ordenada)
    >>> ["c", "csharp", "java", "js", "python"]
    ```
    

### Materiais Complementares

[Listas.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/40043bc3-214c-4bd4-985f-97c9110b08d2/Listas.pdf)