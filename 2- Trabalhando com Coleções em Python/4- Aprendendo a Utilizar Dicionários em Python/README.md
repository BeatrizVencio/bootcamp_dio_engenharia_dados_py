# Aprendendo a Utilizar Dicionários em Python

### Aula 1 - Dicionários: Criação e acesso aos dados

Nesta aula, exploramos o conceito de dicionários em Python, aprendendo como criá-los, inserir dados e acessar informações.

**O que são dicionários?**

- Dicionários são estruturas de dados que armazenam dados em pares chave-valor.
- As chaves são únicas, permitindo a organização e o acesso rápido aos dados.
- Dicionários são mutáveis: Você pode modificar os valores associados às chaves depois de criar o dicionário.

**Criando dicionários em Python:**

- Use chaves `{}` para delimitar os pares chave-valor.
- Separe os pares por vírgulas.
- A chave deve ser um objeto imutável (string, número, tupla) e o valor pode ser qualquer tipo de dado.
- Você pode criar dicionários vazios ou inicializá-los com dados.

**Exemplos:**

```python
# Dicionário com informações de uma pessoa
pessoa = {"nome": "Guilherme", "idade": 28}

# Criando dicionário vazio
pessoa = {}

# Dicionário com diferentes tipos de dados
carro = {"marca": "Ferrari", "modelo": "F8", "ano": 2018}

```

**Acessando elementos de um dicionário:**

- Use colchetes `[]` com a chave desejada para acessar o valor associado.

**Exemplos:**

```python
pessoa = {"nome": "Guilherme", "idade": 28}

# Acessando o valor da chave "nome"
print(pessoa["nome"])
>>> Guilherme

# Acessando o valor da chave "idade"
print(pessoa["idade"])
>>> 28

# Acessando um valor que não existe, gera erro
print(pessoa["profissão"])
>>> KeyError: 'profissão'

```

**Dicionários aninhados:**

- Você pode criar dicionários que armazenam outros dicionários, formando estruturas complexas.
- Para acessar elementos em dicionários aninhados, use dois ou mais colchetes `[]`.

**Exemplo:**

```python
contatos = {
    "guilherme": {"email": "guilherme@email.com", "telefone": "3333-2221"},
    "giovana": {"email": "giovana@email.com", "telefone": "3443-2121"},
    "chappie": {"email": "chappie@email.com", "telefone": "3344-9871"}
}

# Acessando o telefone de Giovana
print(contatos["giovana"]["telefone"])
>>> 3443-2121

```

### Aula 2 - Métodos da classe dict

A segunda aula nos apresenta métodos úteis da classe `dict` para manipular e transformar dicionários de forma eficiente.

**Compreendendo Métodos:**

- **Métodos** são funções que pertencem a um objeto (nesse caso, um objeto do tipo `dict`).
- Acessamos métodos usando o ponto (`.`) após o nome do dicionário, seguido do nome do método e parênteses.
- Métodos podem modificar o dicionário original, ou retornar uma nova lista, dependendo do método.

**Métodos da Classe `dict`:**

1. **`clear()`:** Remove todos os itens do dicionário.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    contatos.clear()
    print(contatos)
    >>> {}
    
    ```
    
2. **`copy()`:** Cria uma cópia independente do dicionário original.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    copia_contatos = contatos.copy()
    copia_contatos["chappie"] = "3344-9871"
    print(contatos)
    >>> {"guilherme": "3333-2221", "giovana": "3443-2121"}
    print(copia_contatos)
    >>> {"guilherme": "3333-2221", "giovana": "3443-2121", "chappie": "3344-9871"}
    
    ```
    
3. **`fromkeys(iterável, valor)`:** Cria um novo dicionário com chaves a partir de um iterável, usando um valor padrão para cada chave.
    
    ```python
    chaves = ["nome", "telefone"]
    novo_dicionario = dict.fromkeys(chaves, "vazio")
    print(novo_dicionario)
    >>> {'nome': 'vazio', 'telefone': 'vazio'}
    
    ```
    
4. **`get(chave, valor_padrão)`:** Retorna o valor associado à chave, ou `None` se a chave não existir.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    print(contatos.get("guilherme"))
    >>> 3333-2221
    print(contatos.get("joao", "não encontrado"))
    >>> não encontrado
    
    ```
    
5. **`items()`:** Retorna um iterável de tuplas, onde cada tupla contém uma chave e seu valor.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    for chave, valor in contatos.items():
        print(f"Chave: {chave}, Valor: {valor}")
    
    ```
    
6. **`keys()`:** Retorna uma lista contendo as chaves do dicionário.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    print(contatos.keys())
    >>> dict_keys(['guilherme', 'giovana'])
    
    ```
    
7. **`pop(chave, valor_padrão)`:** Remove o item associado à chave e retorna seu valor.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    valor_removido = contatos.pop("guilherme")
    print(valor_removido)
    >>> 3333-2221
    print(contatos)
    >>> {"giovana": "3443-2121"}
    
    ```
    
8. **`popitem()`:** Remove e retorna um par chave-valor aleatório do dicionário.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    chave, valor = contatos.popitem()
    print(chave, valor)
    >>> ('giovana', '3443-2121')
    print(contatos)
    >>> {'guilherme': '3333-2221'}
    
    ```
    
9. **`setdefault(chave, valor_padrão)`:** Retorna o valor associado à chave, ou insere a chave com o valor padrão se a chave não existir.
    
    ```python
    contatos = {"guilherme": "3333-2221"}
    print(contatos.setdefault("guilherme", "3333-2221"))
    >>> 3333-2221
    print(contatos.setdefault("joao", "3443-2121"))
    >>> 3443-2121
    print(contatos)
    >>> {'guilherme': '3333-2221', 'joao': '3443-2121'}
    
    ```
    
10. **`update(dicionário)`:** Atualiza o dicionário com os pares chave-valor do dicionário fornecido.
    
    ```python
    contatos = {"guilherme": "3333-2221"}
    novos_contatos = {"joao": "3443-2121", "chappie": "3344-9871"}
    contatos.update(novos_contatos)
    print(contatos)
    >>> {'guilherme': '3333-2221', 'joao': '3443-2121', 'chappie': '3344-9871'}
    
    ```
    
11. **`values()`:** Retorna uma lista contendo os valores do dicionário.
    
    ```python
    contatos = {"guilherme": "3333-2221", "giovana": "3443-2121"}
    print(contatos.values())
    >>> dict_values(['3333-2221', '3443-2121'])
    
    ```
    

### Materiais Complementares

[Dicionários.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/2a84cc9b-52fb-4428-8587-f5fc930b8285/Dicionrios.pdf)