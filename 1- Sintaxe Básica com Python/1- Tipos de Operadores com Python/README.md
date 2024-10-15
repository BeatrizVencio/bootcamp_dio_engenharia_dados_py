# Tipos de Operadores com Python

### Aula 1 - Operadores aritméticos

A primeira aula mergulha no mundo dos operadores aritméticos, os blocos de construção para realizar cálculos matemáticos dentro de seus programas Python.

**Conceitos chave:**

- **Operadores básicos:** Adição, subtração, multiplicação, divisão, divisão inteira (retorna apenas a parte inteira da divisão) e módulo (calcula o resto da divisão).
- **Precedência de operadores:** A ordem de execução das operações é definida pela precedência. Parênteses são utilizados para forçar uma determinada ordem de execução.
- **Exemplos:**
    
    ```python
    # Adição
    print(2 + 1)
    >>> 3
    
    # Subtração
    print(10 - 2)
    >>> 8
    
    # Multiplicação
    print(4 * 3)
    >>> 12
    
    # Divisão
    print(12 / 3)
    >>> 4.0
    
    # Divisão inteira
    print(12 // 2)
    >>> 6
    
    # Módulo
    print(10 % 3)
    >>> 1
    
    # Exponenciação
    print(2 ** 3)
    >>> 8
    
    # Utilizando parênteses para forçar a ordem
    print(10 - (5 * 2))
    >>> 0
    
    ```
    
- **Utilização:** Os operadores aritméticos são essenciais para realizar cálculos em Python.

### Aula 2 - Operadores de comparação

A segunda aula introduz os operadores de comparação, ferramentas que permitem ao seu código tomar decisões com base em comparações entre valores.

**Conceitos chave:**

- **Operadores básicos:** Igualdade (==), Diferença (!=), Maior que (>), Menor que (<), Maior ou igual (>=) e Menor ou igual (<=).
- **Retorna valores booleanos:** As comparações resultam em `True` (verdadeiro) ou `False` (falso), que são importantes para controlar o fluxo do programa.
- **Utilização:** Utilizados em estruturas condicionais (`if`, `elif`, `else`) para direcionar o fluxo do código com base em comparações.
- **Exemplos:**
    
    ```python
    # Igualdade
    print(5 == 5)
    >>> True
    
    # Diferença
    print(5 != 5)
    >>> False
    
    # Maior que
    print(10 > 5)
    >>> True
    
    # Menor que
    print(5 < 10)
    >>> True
    
    # Maior ou igual
    print(10 >= 10)
    >>> True
    
    # Menor ou igual
    print(5 <= 5)
    >>> True
    
    ```
    

### Aula 3 - Operadores de atribuição

Esta aula nos apresenta aos **operadores de atribuição**, ferramentas essenciais para manipular variáveis e realizar cálculos de forma eficiente.

**O que são operadores de atribuição?**
Eles são símbolos especiais que permitem atribuir um valor a uma variável ou modificar o valor atual de uma variável de forma concisa.

**Operadores de atribuição e seus usos:**

- **`=` (Atribuição simples):** O operador mais básico, usado para definir o valor inicial de uma variável.
    
    ```python
    # Atribuição simples
    saldo = 500
    print(saldo)
    >>> 500
    ```
    
- **`+=` (Atribuição com adição):** Soma um valor à variável atual e atualiza o valor da variável.
    
    ```python
    # Atribuição com adição
    saldo += 200 
    print(saldo)
    >>> 700
    ```
    
- **`-=` (Atribuição com subtração):** Subtrai um valor da variável atual e atualiza o valor da variável.
    
    ```python
    # Atribuição com subtração
    saldo -= 100
    print(saldo)
    >>> 600
    ```
    
- `*=` **(Atribuição com multiplicação):** Multiplica um valor pela variável atual e atualiza o valor da variável.
    
    ```python
    # Atribuição com multiplicação
    saldo *= 2
    print(saldo)
    >>> 1200
    ```
    
- **`/=` (Atribuição com divisão):** Divide a variável atual por um valor e atualiza o valor da variável.
    
    ```python
    # Atribuição com divisão
    saldo /= 5
    print(saldo)
    >>> 240.0
    ```
    
- **`//=` (Atribuição com divisão inteira):** Realiza uma divisão inteira da variável atual por um valor e atualiza o valor da variável.
    
    ```python
    # Atribuição com divisão inteira
    saldo //= 2
    print(saldo)
    >>> 120
    ```
    
- **`%=` (Atribuição com módulo):** Calcula o módulo da variável atual por um valor e atualiza o valor da variável.
    
    ```python
    # Atribuição com módulo
    saldo %= 10
    print(saldo)
    >>> 0
    ```
    
- `**=` **(Atribuição com exponenciação):** Eleva a variável atual a um valor e atualiza o valor da variável.
    
    ```python
    # Atribuição com exponenciação
    saldo **= 2
    print(saldo)
    >>> 0
    ```
    

**Benefícios dos operadores de atribuição:**

- **Concisão:** Tornam o código mais limpo e eficiente, evitando a repetição de nomes de variáveis.
- **Legibilidade:** Facilitam a compreensão de como os valores de variáveis estão sendo modificados.
- **Eficiência:** Em alguns casos, podem ser mais eficientes do que operações tradicionais, especialmente em loops onde a variável está sendo modificada repetidamente.

### Aula 4 - Operadores Lógicos

Nesta aula, aprendemos a usar **operadores lógicos** para criar expressões lógicas complexas e controlar o fluxo de execução de nossos programas Python.

**O que são operadores lógicos?**
Eles nos permitem combinar múltiplas condições (expressões que resultam em `True` ou `False`) para tomar decisões mais complexas.

**Tipos de operadores lógicos:**

- **`and` (E lógico):** Retorna `True` se **ambas** as condições forem verdadeiras.
    
    ```python
    idade = 20
    tem_carteira = True
    pode_dirigir = idade >= 18 and tem_carteira
    print(pode_dirigir)
    >>> True
    
    ```
    
- **`or` (Ou lógico):** Retorna `True` se **pelo menos uma** das condições for verdadeira.
    
    ```python
    tem_dinheiro = False
    tem_cartao = True
    pode_comprar = tem_dinheiro or tem_cartao
    print(pode_comprar)
    >>> True
    
    ```
    
- **`not` (Negação lógica):** Inverte o valor lógico de uma condição.
    
    ```python
    pode_entrar = False
    pode_entrar = not pode_entrar
    print(pode_entrar)
    >>> True
    
    ```
    

**Precedência dos operadores lógicos:**

- `not` é executado antes de `and`.
- `and` é executado antes de `or`.
- Parênteses podem ser usados para forçar a ordem de execução.

**Exemplos:**

```python
# Usando "and" para verificar se um número está dentro de um intervalo
numero = 15
if numero > 10 and numero < 20:
    print("O número está entre 10 e 20.")
else:
    print("O número não está entre 10 e 20.")

# Usando "not" e "and" para verificar a elegibilidade para um empréstimo
idade = 25
tem_score = True
tem_renda = True
if idade >= 18 and tem_score and tem_renda:
    print("Empréstimo aprovado!")
else:
    print("Empréstimo negado.")

```

**Utilize os operadores lógicos para:**

- Verificar se múltiplas condições são verdadeiras ao mesmo tempo.
- Criar decisões mais complexas em seus programas.
- Controlar o fluxo de execução de seus programas.

### Aula 5 - Operadores de identidade

Esta aula nos apresenta aos **operadores de identidade**, ferramentas que nos permitem comparar se duas variáveis **referenciam o mesmo objeto na memória**, e não apenas se seus valores são iguais.

**O que são operadores de identidade?**

- **`is`:** Retorna `True` se duas variáveis referenciam o mesmo objeto na memória.
- **`is not`:** Retorna `True` se duas variáveis **não** referenciam o mesmo objeto na memória.

**Quando usar operadores de identidade?**

- **Quando a localização na memória é crucial:** É útil para verificar se duas variáveis estão realmente apontando para o mesmo objeto, e não apenas para um objeto com o mesmo valor.
- **Comparando objetos mutáveis:** Para objetos mutáveis (como listas e dicionários), `is` e `is not` são relevantes, já que a modificação de um objeto afeta todos os seus referenciais.

**Exemplos:**

```python
curso = "Curso de Python"
nome_curso = curso
saldo = 200
limite = 200

# Verificando a identidade de variáveis que referenciam o mesmo objeto
print(curso is nome_curso)  # True - ambas referenciam o mesmo objeto
print(curso is not nome_curso) # False

# Verificando a identidade de variáveis com o mesmo valor, mas objetos diferentes
print(saldo is limite) # True - no caso de inteiros, pode ser True ou False, depende da implementação do Python
print(saldo is not limite) # False

```

**Observações:**

- No caso de números inteiros (como `saldo` e `limite` no exemplo acima), o Python pode reutilizar o mesmo objeto na memória para representar o mesmo valor. Isso significa que `saldo is limite` pode resultar em `True` ou `False`, dependendo da implementação do Python.
- Para objetos mutáveis, a comparação de identidade é crucial, pois a modificação de um objeto afeta todos os seus referenciais.

### Aula 6 - Operadores de associação

Agora vamos aos **operadores de associação**, ferramentas que nos permitem verificar se um objeto está presente em uma sequência, como listas e strings.

**O que são operadores de associação?**

- **`in`:** Retorna `True` se o objeto está presente na sequência.
- **`not in`:** Retorna `True` se o objeto **não** está presente na sequência.

**Quando usar operadores de associação?**

- **Procurando elementos em sequências:** São ideais para verificar a presença de um elemento em listas, strings, tuplas e conjuntos (sets).
- **Construindo condições:** Usados em estruturas condicionais (`if`, `elif`, `else`) para tomar decisões com base na presença ou ausência de elementos em sequências.

**Exemplos:**

```python
curso = "Curso de Python"
frutas = ["laranja", "uva", "limão"]
saques = [1500, 100]

# Verificando se "Python" está na string "curso"
print("Python" in curso)
>>> True

# Verificando se "maçã" não está na lista de "frutas"
print("maçã" not in frutas)
>>> True

# Verificando se 200 está na lista de "saques"
print(200 in saques)
>>> False

```

**Utilize os operadores de associação para:**

- Verificar se um elemento específico está presente em uma sequência.
- Construir condições para tomar decisões, por exemplo, em um sistema de estoque para verificar a disponibilidade de um item.
- Validar dados de entrada, por exemplo, em um formulário para verificar se um valor está dentro de um conjunto de valores válidos.

### Materiais Complementares

[1- Operadores aritméticos.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/48160b16-2519-4524-9008-fea4aa4c418d/1-_Operadores_aritmticos.pdf)

[2- Operadores de comparação.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/d9947e81-dc3d-4dce-9f68-18c98b9d6717/2-_Operadores_de_comparao.pdf)

[3- Operadores de atribuição.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/e8007349-8121-4425-b0b6-90aed05cd802/3-_Operadores_de_atribuio.pdf)

[4- Operadores lógicos.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/cadb3157-cc97-4b8c-849a-4089449f4873/4-_Operadores_lgicos.pdf)

[5- Operadores de identidade.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/7cb945c1-8e93-4596-8758-3e9fa2a3866e/5-_Operadores_de_identidade.pdf)

[6- Operadores de associação.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/0eff47c1-a86a-4dd8-90fd-6b8f6ed9d525/6-_Operadores_de_associao.pdf)