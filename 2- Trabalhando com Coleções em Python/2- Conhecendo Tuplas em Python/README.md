# Conhecendo Tuplas em Python

### Aula 1 - Tuplas

Esta aula nos apresenta o conceito de **tuplas**, uma estrutura de dados em Python similar às listas, mas com uma diferença crucial: **tuplas são imutáveis**.

**O que são tuplas?**

- Tuplas são sequências ordenadas de elementos, como listas, mas com a restrição de que **não podem ser modificadas** depois de criadas.
- Podem conter elementos de tipos diferentes, inclusive tuplas aninhadas, permitindo a criação de estruturas bidimensionais.
- São representadas por parênteses `()`.

**Por que usar tuplas?**

- **Imutável:** Essa característica garante que os dados dentro da tupla permaneçam intactos, evitando modificações acidentais.
- **Segurança:** Útil para armazenar dados que não devem ser alterados, como configurações ou constantes.
- **Eficiência:** Em alguns casos, tuplas podem ser mais eficientes que listas, pois o Python pode otimizar seu armazenamento.

**Criando Tuplas em Python:**

- Use parênteses `()` para delimitar os elementos da tupla.
- Separe os elementos por vírgulas.
- Você pode criar tuplas vazias ou inicializá-las com dados.
- Uma tupla com um único elemento deve ter uma vírgula no final.

**Exemplos:**

```python
# Tupla de frutas
frutas = ("laranja", "pera", "uva")

# Tupla vazia
frutas = ()

# Tupla de números
numeros = (1, 2, 3, 4, 5)

# Tupla de diferentes tipos
carro = ("Ferrari", "F8", 420000, 2018, "São Paulo", True)

```

**Acessando elementos de uma tupla:**

- Tuplas são indexadas, começando do índice 0, como listas.
- Use colchetes `[]` com o índice do elemento desejado para acessá-lo.

**Exemplos:**

```python
frutas = ("laranja", "pera", "uva")

# Acessando o primeiro elemento
print(frutas[0])
>>> laranja

# Acessando o último elemento
print(frutas[-1])
>>> uva

# Acessando o segundo elemento
print(frutas[1])
>>> pera

```

**Tuplas aninhadas:**

- Você pode criar tuplas que armazenam outras tuplas, formando estruturas multidimensionais.
- Para acessar elementos em tuplas aninhadas, use dois índices.

**Exemplo:**

```python
matriz = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

# Acessando o elemento na linha 1 e coluna 2
print(matriz[1][2])
>>> 6

```

**Métodos Úteis da Classe `tuple`:**

- **`count(elemento)`:** Conta quantas vezes um elemento aparece na tupla.
    
    ```python
    cores = ("vermelho", "azul", "verde", "azul")
    print(cores.count("azul"))
    >>> 2
    
    ```
    
- **`index(elemento)`:** Retorna o índice da primeira ocorrência de um elemento na tupla.
    
    ```python
    linguagens = ("python", "js", "c", "java", "csharp")
    print(linguagens.index("java"))
    >>> 3
    
    ```
    

### Materiais Complementares

[Tuplas.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/f26d125f-a759-4711-9f4d-09bc7a7fa3d1/Tuplas.pdf)