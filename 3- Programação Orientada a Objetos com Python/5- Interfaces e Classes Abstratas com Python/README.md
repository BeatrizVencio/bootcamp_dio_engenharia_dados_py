# Interfaces e Classes Abstratas com Python

### Aula 1 - Variáveis de classe e Variáveis de instância

Nesta aula, exploramos os tipos de variáveis em POO em Python: variáveis de classe e variáveis de instância.

**Variáveis de Classe:**

- **Definidas dentro da classe:** São declaradas dentro da classe, mas fora de qualquer método.
- **Compartilhadas por todos os objetos da classe:** O valor da variável de classe é o mesmo para todos os objetos.
- **Modificadas diretamente pela classe:** Se você alterar o valor da variável de classe em um objeto, a alteração será refletida em todos os objetos da classe.

**Variáveis de Instância:**

- **Definidas no construtor:** São declaradas dentro do construtor (`__init__`) da classe.
- **Únicas para cada objeto:** Cada objeto possui sua própria cópia da variável de instância, com valores que podem ser diferentes.
- **Modificadas através de objetos:** Você precisa acessar um objeto específico para modificar sua variável de instância.

**Exemplo:**

```python
class Estudante:
    # Variável de classe
    escola = "DIO"

    def __init__(self, nome, matricula): # Construtor
        # Variável de instância
        self.nome = nome
        self.matricula = matricula

    def __str__(self):
        return f"{self.nome} ({self.matricula}) - {Estudante.escola}"

# Criando objetos
bia= Estudante("Beatriz", 58451)
gio = Estudante("Giovanna", 17323)

# Acessando variáveis
print(bia.nome)
>>> Beatriz
print(gio.matricula)
>>> 17323
print(bia.escola)
>>> DIO
print(gio.escola)
>>> DIO

# Modificando variáveis
Estudante.escola = "Python"
print(bia.escola)
>>> Python
print(gio.escola)
>>> Python

```

**Próximos Passos:**

- **Métodos de Classe e Métodos de Instância:** Aprenda a diferenciar e usar métodos de classe e métodos de instância.
- **Herança:** Explore como criar novas classes que herdam características de classes existentes.
- **Encapsulamento:** Entenda como esconder os detalhes internos de uma classe para controlar o acesso aos seus atributos e métodos.

### Aula 2 - Métodos de classe e Métodos estático

A aula 2 da série sobre POO em Python se concentra em dois tipos específicos de métodos em classes: **métodos de classe** e **métodos estáticos**.

**Métodos de Classe:**

- **Ligados à classe:** São métodos que pertencem à classe e não a um objeto específico.
- **Acessam o estado da classe:** Podem acessar e modificar variáveis de classe.
- **Primeiro parâmetro é `cls`:** O primeiro parâmetro de um método de classe é normalmente `cls` (pode ser qualquer nome, mas a convenção é `cls`), que representa a própria classe.

**Sintaxe:**

```python
class Classe:
    def metodo_de_classe(cls):
        # código do método de classe
        pass

```

**Exemplo:**

```python
class Pessoa:
    contador_pessoas = 0  # Variável de classe

    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade
        Pessoa.contador_pessoas += 1  # Incrementa o contador ao criar um objeto

    @classmethod  # Decoração para definir um método de classe
    def gerar_relatorio(cls):
        print(f"Total de pessoas: {cls.contador_pessoas}")

# Criando objetos
pessoa1 = Pessoa("Guilherme", 28)
pessoa2 = Pessoa("Giovanna", 25)

# Chamando o método de classe
Pessoa.gerar_relatorio() # Saída: Total de pessoas: 2

```

**Métodos Estáticos:**

- **Não estão ligados a instâncias ou classe:** São métodos que não operam sobre o estado da classe ou de um objeto.
- **Não recebem `self` ou `cls`:** São usados como funções regulares, mas dentro do escopo da classe.

**Sintaxe:**

```python
class Classe:
    @staticmethod
    def metodo_estatico():
        # código do método estático
        pass

```

**Exemplo:**

```python
class Matematica:
    @staticmethod
    def somar(x, y):
        return x + y

resultado = Matematica.somar(5, 3)
print(resultado) # Saída: 8

```

**Quando usar cada tipo de método:**

- **Métodos de Classe:** Úteis para ações que envolvem o estado da classe, como criar objetos ou manipular variáveis de classe.
- **Métodos Estáticos:** Adequados para funções utilitárias que não precisam acessar o estado da classe ou objetos.

### Aula 3 - O que são Interfaces

Nesta aula, exploramos o conceito de interfaces e como implementá-las em Python com o módulo `abc`.

**O que são Interfaces?**

- **Definindo um contrato:** Interfaces definem o que uma classe deve fazer, mas não como fazê-lo.
- **Declarando métodos:** Contêm declarações de métodos, mas sem implementação.
- **Obrigando implementação:** Classes que implementam uma interface devem fornecer a implementação dos métodos declarados.

**Exemplo:**

```python
from abc import ABC, abstractmethod

class Forma(ABC):
    @abstractmethod  # Decoração para indicar um método abstrato
    def calcular_area(self):
        pass

class Quadrado(Forma):
    def __init__(self, lado):
        self.lado = lado

    def calcular_area(self):
        return self.lado * self.lado

class Circulo(Forma):
    def __init__(self, raio):
        self.raio = raio

    def calcular_area(self):
        return 3.14159 * self.raio * self.raio

# Criando objetos
quadrado = Quadrado(5)
circulo = Circulo(3)

# Calculando áreas
print(f"Área do quadrado: {quadrado.calcular_area()}")
print(f"Área do círculo: {circulo.calcular_area()}")

```

**Observações:**

- **`Forma`:** A classe base `Forma` define a interface, com o método abstrato `calcular_area`.
- **`Quadrado` e `Circulo`:** Classes que implementam a interface, fornecendo implementação para o método `calcular_area`.
- **`@abstractmethod`:** A decoração `@abstractmethod` indica que um método é abstrato.
- **`ABC`:** A classe base `ABC` (do módulo `abc`) indica que uma classe é abstrata e serve como base para interfaces.

**Vantagens das Interfaces:**

- **Reutilização:** Permite usar o mesmo código para diferentes tipos de objetos.
- **Flexibilidade:** Facilita a modificação da implementação de classes que implementam a interface.
- **Abstração:** Esconde detalhes de implementação, focando no que a classe deve fazer.

O uso de interfaces em Python ajuda a construir sistemas mais robustos, flexíveis e de fácil manutenção, utilizando o poder da programação orientada a objetos!

### Aula 4 - Classes Abstratas

Nesta aula, vimos as **classes abstratas**, que servem como modelos para outras classes e não podem ser instanciadas diretamente. Em Python, classes abstratas são implementadas utilizando o módulo `abc`.

**Classes Abstratas:**

- **Definindo um modelo:** Classes abstratas definem uma estrutura e comportamento, mas não uma implementação completa.
- **Métodos abstratos:** Contêm métodos abstratos que devem ser implementados por classes filhas.
- **Forçando implementação:** Classes que herdam de classes abstratas são obrigadas a implementar os métodos abstratos.

**Exemplo:**

```python
from abc import ABC, abstractmethod

class Veiculo(ABC):
    @abstractmethod
    def acelerar(self):
        pass

    @abstractmethod
    def frear(self):
        pass

class Carro(Veiculo):
    def __init__(self):
        pass

    def acelerar(self):
        print("Carro acelerando...")

    def frear(self):
        print("Carro freando...")

# Criando um objeto
carro = Carro()
carro.acelerar()
carro.frear()

```

**Observações:**

- **`Veiculo`:** A classe base `Veiculo` é abstrata, com métodos abstratos `acelerar` e `frear`.
- **`Carro`:** Uma classe filha que implementa a classe abstrata `Veiculo`, fornecendo a implementação para os métodos abstratos.
- **`@abstractmethod`:** A decoração `@abstractmethod` indica que um método é abstrato.
- **`ABC`:** A classe base `ABC` (do módulo `abc`) indica que uma classe é abstrata e serve como base para definir interfaces.

**Vantagens de Classes Abstratas:**

- **Abstração:** Esconde detalhes de implementação, focando no comportamento esperado.
- **Reutilização:** Define um modelo que pode ser adaptado por outras classes.
- **Modularidade:** Promove a organização e a manutenção do código.

Utilizar classes abstratas em Python é uma excelente prática para construir sistemas de software mais estruturados, robustos e flexíveis.
