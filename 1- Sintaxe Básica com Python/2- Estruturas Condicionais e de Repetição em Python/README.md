# Estruturas Condicionais e de Repetição em Python

### Aula 1 - Indentação e blocos

Nesta aula, desvendamos a importância da **indentação** e como ela define a estrutura dos **blocos de comandos** em Python.

**Mais que um capricho, uma regra:**

- **Definindo blocos:** Em Python, a indentação (espaços no início de uma linha de código) não é apenas um capricho estético, mas sim uma regra gramatical que define os blocos de comandos.
- **Evitando chaves:** Diferente de linguagens como Java e C, o Python não usa chaves `{}` para delimitar blocos. A indentação é a única forma de indicar ao interpretador o início e o fim de um bloco.
- **Consistência é crucial:** A indentação deve ser consistente em todo o código. Use o mesmo número de espaços para cada nível de indentação.

**Por que a indentação é importante?**

- **Legibilidade:** Torna o código mais fácil de ler e entender.
- **Organização:** Define a estrutura do código, facilitando a manutenção e a identificação de diferentes blocos de comandos.
- **Prevenção de erros:** O interpretador Python se baseia na indentação para executar o código corretamente. Erros de indentação levam a erros de sintaxe.

**Exemplos:**

```python
# Código com indentação CORRETA
if saldo >= valor:
    print("Valor sacado!")
    saldo -= valor
    print("Seu novo saldo é:", saldo)
else:
    print("Saldo insuficiente!")

# Código com indentação INCORRETA
if saldo >= valor:
    print("Valor sacado!")
saldo -= valor
    print("Seu novo saldo é:", saldo)
else:
    print("Saldo insuficiente!")

```

### Aula 2 - Estruturas condicionais

Esta aula nos ensina a usar **estruturas condicionais**, construções fundamentais para criar programas que tomam decisões e executam diferentes ações com base em condições lógicas.

**Tipos de estruturas condicionais:**

1. **`if` (Se):** Executa um bloco de código apenas se uma condição for verdadeira.
    
    ```python
    idade = 20
    if idade >= 18:
        print("Você é maior de idade!")
    
    ```
    
2. **`if-else` (Se-Senão):** Executa um bloco de código se a condição for verdadeira e outro bloco se for falsa.
    
    ```python
    idade = 16
    if idade >= 18:
        print("Você é maior de idade!")
    else:
        print("Você é menor de idade!")
    
    ```
    
3. **`if-elif-else` (Se-Senão Se-Senão):** Permite testar várias condições em sequência, executando o bloco correspondente à primeira condição verdadeira.
    
    ```python
    nota = 7.5
    if nota >= 9:
        print("Excelente!")
    elif nota >= 7:
        print("Bom!")
    else:
        print("Precisa melhorar.")
    
    ```
    

**Utilizando estruturas condicionais para:**

- **Controlar o fluxo de execução:** Decidir quais comandos executar com base em condições.
- **Criar programas interativos:** Permitir que o usuário escolha diferentes ações com base em suas escolhas.
- **Validar dados de entrada:** Verificar se os dados inseridos pelo usuário são válidos.

### Aula 3 - Estruturas de Repetição

Esta aula nos apresenta as **estruturas de repetição**, ferramentas poderosas que automatizam tarefas repetitivas e simplificam a escrita de código.

**Tipos de Estruturas de Repetição:**

1. **`for` (Para):** Itera sobre os elementos de uma sequência (listas, strings, tuplas, etc.), executando um bloco de código para cada elemento.
    
    ```python
    frutas = ["maçã", "banana", "uva"]
    for fruta in frutas:
        print("Eu gosto de", fruta)
    
    ```
    
2. **`while` (Enquanto):** Executa um bloco de código **enquanto** uma condição for verdadeira.
    
    ```python
    contador = 1
    while contador <= 5:
        print(contador)
        contador += 1
    
    ```
    
3. **`break` (Interromper):** Interrompe a execução de um laço de repetição (for ou while).
    
    ```python
    números = [1, 2, 3, 4, 5]
    for número in números:
        if número == 3:
            break
        print(número)
    
    ```
    

**Utilizando Estruturas de Repetição para:**

- **Automatizar tarefas repetitivas:** Evite escrever o mesmo código várias vezes.
- **Processar grandes quantidades de dados:** Itera sobre listas e outras sequências para realizar operações em cada elemento.
- **Criar loops infinitos:** Use `while True` para criar um loop que continua executando indefinidamente.
- **Controlar o fluxo de execução:** Use `break` para interromper a execução de um loop em determinadas condições.

### Materiais Complementares

[1- Indentação e blocos.pdf](https://github.com/BeatrizVencio/bootcamp_dio_engenharia_dados_py/blob/main/1-%20Sintaxe%20Básica%20com%20Python/2-%20Estruturas%20Condicionais%20e%20de%20Repetição%20em%20Python/Materiais%20Complementares/1-%20Indentação%20e%20blocos.pdf)

[2- Estruturas condicionais.pdf](https://github.com/BeatrizVencio/bootcamp_dio_engenharia_dados_py/blob/main/1-%20Sintaxe%20Básica%20com%20Python/2-%20Estruturas%20Condicionais%20e%20de%20Repetição%20em%20Python/Materiais%20Complementares/2-%20Estruturas%20condicionais.pdf)

[3- Estruturas de repetição.pdf](https://github.com/BeatrizVencio/bootcamp_dio_engenharia_dados_py/blob/main/1-%20Sintaxe%20Básica%20com%20Python/2-%20Estruturas%20Condicionais%20e%20de%20Repetição%20em%20Python/Materiais%20Complementares/3-%20Estruturas%20de%20repetição.pdf)
