# Manipulando Strings com Python

### Aula 1 - Conhecendo métodos úteis da classe string

Nesta aula, mergulhamos no mundo das strings em Python, explorando métodos essenciais para manipular e transformar textos.

**Introdução à Classe String:**

- A classe `string` em Python é poderosa e versátil, permitindo trabalhar com sequências de caracteres de forma eficiente.

**Métodos Úteis para Manipular Strings:**

- **`upper()`:** Converte a string para maiúsculas.
    
    ```python
    nome = "guilherme"
    print(nome.upper())
    >>> GUILHERME
    
    ```
    
- **`lower()`:** Converte a string para minúsculas.
    
    ```python
    nome = "GUILHERME"
    print(nome.lower())
    >>> guilherme
    
    ```
    
- **`title()`:** Capitaliza a primeira letra de cada palavra na string.
    
    ```python
    nome = "guilherme arthur"
    print(nome.title())
    >>> Guilherme Arthur
    
    ```
    
- **`strip()`:** Remove espaços em branco no início e no fim da string.
    
    ```python
    texto = "  Olá mundo!   "
    print(texto.strip())
    >>> Olá mundo!
    
    ```
    
- **`lstrip()`:** Remove espaços em branco do início da string.
    
    ```python
    texto = "  Olá mundo!   "
    print(texto.lstrip())
    >>> Olá mundo!
    
    ```
    
- **`rstrip()`:** Remove espaços em branco do fim da string.
    
    ```python
    texto = "  Olá mundo!   "
    print(texto.rstrip())
    >>>   Olá mundo!
    
    ```
    
- **`center(largura, caractere)`:** Centraliza a string em uma determinada largura, preenchendo com o caractere especificado.
    
    ```python
    texto = "Python"
    print(texto.center(10, '#'))
    >>> ###Python###
    
    ```
    

### Aula 2 - Interpolação de variáveis

Esta aula explora a **interpolação de variáveis**, uma técnica fundamental para inserir valores de variáveis dentro de strings, criando mensagens dinâmicas e personalizadas.

**Formas de Interpolar Variáveis em Python:**

1. **`%` (Estilo antigo):** Uma forma mais tradicional, mas menos recomendada atualmente.
    
    ```python
    nome = "Guilherme"
    idade = 28
    print("Olá, me chamo %s. Eu tenho %d anos de idade." % (nome, idade))
    >>> Olá, me chamo Guilherme. Eu tenho 28 anos de idade.
    
    ```
    
2. **`format()`:** Oferece mais flexibilidade e controle sobre a formatação.
    
    ```python
    nome = "Guilherme"
    idade = 28
    print("Olá, me chamo {}. Eu tenho {} anos de idade.".format(nome, idade))
    >>> Olá, me chamo Guilherme. Eu tenho 28 anos de idade.
    
    ```
    
3. **`f-string`:** A forma mais moderna e recomendada, proporcionando concisão e legibilidade.
    
    ```python
    nome = "Guilherme"
    idade = 28
    print(f"Olá, me chamo {nome}. Eu tenho {idade} anos de idade.")
    >>> Olá, me chamo Guilherme. Eu tenho 28 anos de idade.
    
    ```
    

**Entendendo as Diferenças:**

- **`%`:** Usa marcadores de posição (como `%s` para strings e `%d` para números inteiros) e um tupla com os valores a serem substituídos.
- **`format()`:** Utiliza chaves `{}` como marcadores de posição e um método `format()` para inserir valores.
- **`f-string`:** Incorpora variáveis diretamente dentro das strings, delimitadas por chaves `{}`.

**Vantagens do `f-string`:**

- **Concisão:** Código mais limpo e fácil de ler.
- **Flexibilidade:** Permite formatação mais complexa usando expressões dentro das chaves.
- **Eficiência:** Geralmente é mais rápido que outros métodos de interpolação.

### Aula 3 - Fatiamento de string

Agora vamos para o **fatiamento de strings**, uma técnica poderosa para extrair partes específicas de uma string, como caracteres individuais ou substrings, e também para inverter strings.

**Entendendo o Fatiamento:**

- A sintaxe do fatiamento é `[inicio:fim:passo]`.
- **`inicio`:** Índice do primeiro caractere a ser incluído (opcional, se não informado, inicia no 0).
- **`fim`:** Índice do último caractere a ser incluído (opcional, se não informado, vai até o fim).
- **`passo`:** Indica de quantos em quantos caracteres o fatiamento deve ser feito (opcional, se não informado, é 1).

**Exemplos:**

```python
nome = "Beatriz Vencio Moreira Nascimento"

# Acessando um caractere específico (indice 0)
print(nome[0])
>>> B

# Extraindo uma substring (do índice 0 até o índice 9, excluindo o 9)
print(nome[0:10])
>>> Beatriz Ve

# Extraindo uma substring (do índice 10 até o fim, excluindo o 10)
print(nome[10:])
>>> ncio Moreira Nascimento

# Extraindo uma substring (do índice 10 até o índice 15, de 2 em 2)
print(nome[10:16:2])
>>> ni

# Invertendo a string
print(nome[::-1])
>>> otnemicsaN arieroM oicneV zirtaeB

```

### Aula 4 - Strings múltiplas linhas

Veremos como vamos lidar com **strings que ocupam várias linhas** em Python, facilitando a criação de textos mais extensos e formatados.

**Criando Strings Multi-Linhas:**

- **Triplas Aspas:** Use três aspas simples (`'''`) ou três aspas duplas (`"""`) para delimitar uma string que pode se estender por várias linhas.
    
    ```python
    mensagem = """Olá, meu nome é Beatriz,
    Eu estou aprendendo Python!
    Essa mensagem tem diferentes recuos.
    """
    print(mensagem)
    
    ```
    

**Exemplo Completo com Strings Triplas e Interpolação:**

```python
nome_usuario = "Beatriz"

menu = f"""
    ============= MENU =============

    1 - Depositar
    2 - Sacar
    0 - Sair

    ================================

    Bem-vindo ao sistema, {nome_usuario}!
    Obrigado por usar nosso sistema!!!!
"""

print(menu)

```

**Observações:**

- Todos os espaços em branco dentro das aspas triplas são incluídos na string.
- A indentação dentro do bloco de aspas triplas **não** influencia a estrutura do código.
- Você pode usar aspas triplas para escrever textos grandes, poemas, códigos HTML ou qualquer outro tipo de texto que precise ocupar várias linhas.

### Materiais Complementares

[String e fatiamento.pdf](https://github.com/BeatrizVencio/bootcamp_dio_engenharia_dados_py/blob/main/1-%20Sintaxe%20Básica%20com%20Python/3-%20Manipulando%20Strings%20com%20Python/Materiais%20Complementares/String%20e%20fatiamento.pdf)
