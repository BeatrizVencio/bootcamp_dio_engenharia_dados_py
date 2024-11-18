# Dominando Funções Python

### Aula 1 - Funções Python – Parte 01

Esta aula nos introduz ao conceito de **funções em Python**,  explicando seus benefícios e como usá-las para organizar e reutilizar código.

**O que são Funções?**

- Uma função é um bloco de código que realiza uma tarefa específica e pode ser chamado por nome em diferentes partes do programa.
- Funções podem receber **parâmetros**, que são valores de entrada que podem ser usados para personalizar o comportamento da função.
- Funções podem **retornar** um valor, que representa o resultado da sua execução.

**Benefícios de Usar Funções:**

- **Reutilização:** Elimine a necessidade de escrever o mesmo código várias vezes.
- **Organização:** Divida programas complexos em partes menores e mais gerenciáveis.
- **Legibilidade:** Torne seu código mais fácil de ler e entender.
- **Modularidade:** Crie blocos de código independentes que podem ser testados e modificados individualmente.

**Sintaxe Básica de uma Função:**

```python
def nome_da_funcao(parametro1, parametro2, ...):
    # Bloco de código da função
    # ...
    return valor_de_retorno

```

**Exemplo Prático:**

```python
def exibir_mensagem(nome):
    print(f"Seja bem vindo, {nome}!")

exibir_mensagem("Beatriz")
>>> Seja bem vindo, Beatriz!

exibir_mensagem("João")
>>> Seja bem vindo, João!

```

**Conceitos-chave:**

- **Definindo uma função:** Use `def` seguido do nome da função, parênteses para os parâmetros (opcional) e dois pontos `:`.
- **Indentação:** O código dentro da função deve ser indentado, normalmente com quatro espaços.
- **Chamando uma função:** Use o nome da função seguido de parênteses, incluindo os argumentos se necessário.
- **`return`:** Use `return` para retornar um valor da função. Se nenhuma instrução `return` for usada, a função retorna `None`.
- **Argumentos Posicionais:** A ordem dos argumentos na chamada da função é importante, eles são associados aos parâmetros na definição da função em ordem.

**Argumentos Nomeados:**

- Você pode chamar funções usando argumentos nomeados, especificando o nome do parâmetro seguido de um sinal de igual (`=`) e o valor.
- Isso torna o código mais legível, especialmente quando a função possui muitos parâmetros.

**Exemplo com Argumentos Nomeados:**

```python
def exibir_mensagem(nome, saudacao="Seja bem vindo"):
    print(f"{saudacao}, {nome}!")

exibir_mensagem(nome="Beatriz", saudacao="Olá")
>>> Olá, Beatriz!

exibir_mensagem(saudacao="Bem-vindo", nome="João")
>>> Bem-vindo, João!

```

- **`args` e `*kwargs`:**
- **`args`:** Permite que uma função receba um número variável de argumentos posicionais. Esses argumentos serão armazenados em uma tupla.
- **`*kwargs`:** Permite que uma função receba um número variável de argumentos nomeados. Esses argumentos serão armazenados em um dicionário.

**Exemplo com `*args` e `**kwargs`:**

```python
def exibir_dados(*args, **kwargs):
    print("Argumentos posicionais:", args)
    print("Argumentos nomeados:", kwargs)

exibir_dados(1, 2, 3, nome="Beatriz", idade=21)
>>> Argumentos posicionais: (1, 2, 3)
>>> Argumentos nomeados: {'nome': 'Beatriz', 'idade': 21}

```

### Aula 2 - Funções Python – Parte 02

**Parâmetros Especiais:**

- **`args` e `*kwargs`:** Ferramentas para lidar com um número variável de argumentos, tornando funções mais flexíveis.
    - `args`: Captura argumentos posicionais em uma tupla.
    - `*kwargs`: Captura argumentos nomeados em um dicionário.
- **Passando Parâmetros por Posição, Nome ou Híbrido:** Python permite flexibilizar como você passa argumentos para funções, usando apenas a posição, apenas o nome, ou uma combinação de ambas.

**Escopo Local e Global:**

- **Escopo Local:** As variáveis criadas dentro de uma função são **locais** e apenas podem ser acessadas dentro dessa função.
- **Escopo Global:** Variáveis declaradas fora das funções são **globais** e podem ser acessadas por qualquer função.
- **`global`:** Use a palavra-chave `global` dentro de uma função para indicar que você deseja modificar uma variável global. **Evite usar `global` sempre que possível**, pois pode dificultar o debug e a manutenção do código.

**Objetos de Primeira Classe:**

- Em Python, tudo é um objeto, incluindo funções. Isso significa que funções podem ser:
    - **Atribuídas a variáveis:**
    
    ```python
    def soma(x, y):
        return x + y
    
    op_soma = soma
    resultado = op_soma(5, 3)
    
    ```
    
    - **Passadas como argumento para outras funções:**
    
    ```python
    def aplicar_funcao(funcao, a, b):
        return funcao(a, b)
    
    resultado = aplicar_funcao(soma, 5, 3)
    
    ```
    
    - **Retornadas por funções:**
    
    ```python
    def criar_funcao_soma(n):
        def somar(x):
            return x + n
        return somar
    
    somar_5 = criar_funcao_soma(5)
    resultado = somar_5(3)
    
    ```
    

### Materiais Complementares

[Funções.pdf](https://github.com/BeatrizVencio/bootcamp_dio_engenharia_dados_py/blob/main/1-%20Sintaxe%20Básica%20com%20Python/4-%20Dominando%20Funções%20com%20Python/Materiais%20Complementares/Funções.pdf)
