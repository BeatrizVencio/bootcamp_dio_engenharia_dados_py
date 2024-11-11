# Aprendendo o Conceito de Herança com Python

### Aula 1 - Herança em POO

Nesta aula, mergulhamos no conceito de **herança**, uma das ferramentas mais poderosas da programação orientada a objetos (POO).

**O que é Herança?**

- A herança é um mecanismo que permite que uma classe (chamada de **classe filha** ou **subclasse**) herde os atributos e métodos de outra classe (chamada de **classe pai** ou **superclasse**).
- A classe filha "estende" a classe pai, adicionando suas próprias características e comportamentos ou modificando os herdados.
- O objetivo da herança é evitar repetição de código e promover reutilização.

**Exemplo para ilustrar a Herança:**

- Imagine que você tem uma classe `Animal` que define atributos básicos de um animal, como `nome`, `especie` e `idade`.
- Agora, você quer criar uma classe `Cachorro` que herda da classe `Animal`.
- A classe `Cachorro` terá os atributos herdados de `Animal` (nome, espécie, idade) e pode adicionar um atributo próprio, como `raca`.
- Além disso, `Cachorro` pode ter um novo método, como `latir`.

**Benefícios da Herança:**

- **Reutilização:** Evita a reescrita do código da classe pai na classe filha.
- **Organização:** Promove a organização do código em uma hierarquia de classes.
- **Extensibilidade:** Facilita a criação de novas classes complexas com base em classes existentes.
- **Polimorfismo:** Permite que objetos de diferentes classes sejam tratados de forma similar.

### Aula 2 - Conceituando Herança Simples e Herança Múltipla

Nesta aula, exploramos os dois tipos principais de herança em Python: **Herança Simples** e **Herança Múltipla**.

**Herança Simples:**

- Uma classe filha herda atributos e métodos de **apenas uma** classe pai.
- É a forma mais comum de herança, representando relações simples entre classes.

**Exemplo:**

```python
class Animal:
    def __init__(self, nome, especie, idade):
        self.nome = nome
        self.especie = especie
        self.idade = idade

    def emitir_som(self):
        print("Som de animal genérico...")

class Cachorro(Animal): # Herança simples: Cachorro herda de Animal
    def __init__(self, nome, especie, idade, raca):
        super().__init__(nome, especie, idade) # Chama o construtor da classe pai (Animal)
        self.raca = raca

    def latir(self):
        print("Auau!")

```

**Herança Múltipla:**

- Uma classe filha herda atributos e métodos de **várias** classes pai.
- Python permite herança múltipla, mas exige cuidado para evitar conflitos entre atributos e métodos herdados.

**Exemplo:**

```python
class Animal:
    def __init__(self, nome, especie, idade):
        self.nome = nome
        self.especie = especie
        self.idade = idade

    def emitir_som(self):
        print("Som de animal genérico...")

class Voador:
    def voar(self):
        print("Voando...")

class Pássaro(Animal, Voador): # Herança múltipla: Pássaro herda de Animal e Voador
    def __init__(self, nome, especie, idade, cor_pena):
        super().__init__(nome, especie, idade)
        self.cor_pena = cor_pena

    def cantar(self):
        print("Piu-piu...")

```

### Aula 3 - Herança Simples

Nesta aula, vamos explorar a **Herança Simples**, uma das formas mais comuns de usar herança em Python.

**Relembrando:**

- Herança é um conceito que permite que uma classe filha herde atributos e métodos de uma classe pai (superclasse).
- Na Herança Simples, a classe filha herda de apenas uma classe pai.

**Sintaxe da Herança Simples:**

```python
class ClasseFilha(ClassePai):
    # Código da classe filha
    pass # A palavra-chave "pass" indica que não há código a ser executado

```

**Exemplo:**

Imagine um sistema de transporte com veículos. Podemos ter uma classe pai "Veículo" e classes filhas, como "Carro", "Moto" e "Caminhão".

```python
class Veiculo:
    def __init__(self, cor, placa, numero_rodas):
        self.cor = cor
        self.placa = placa
        self.numero_rodas = numero_rodas

    def ligar_motor(self):
        print("Ligando o motor...")

class Motocicleta(Veiculo):
    def __init__(self, cor, placa, numero_rodas, tipo_motor="a gasolina"):
        super().__init__(cor, placa, numero_rodas)
        self.tipo_motor = tipo_motor

    def fazer_manobra(self):
        print("Manobrando a motocicleta...")

class Carro(Veiculo):
    def __init__(self, cor, placa, numero_rodas, nome_modelo):
        super().__init__(cor, placa, numero_rodas)
        self.nome_modelo = nome_modelo

    def acelerar(self):
        print("Carro acelerando...")

class Caminhao(Veiculo):
    def __init__(self, cor, placa, numero_rodas, carga_maxima):
        super().__init__(cor, placa, numero_rodas)
        self.carga_maxima = carga_maxima
        self.esta_carregado = False

    def carregar(self):
        self.esta_carregado = True
        print("Carga carregada!")

    def descarregar(self):
        self.esta_carregado = False
        print(f"{'Sim' if self.esta_carregado else 'Não'} carregado")

# Criando objetos de diferentes tipos de veículos
moto = Motocicleta("Preta", "ABC-1234", 2)
carro = Carro("Branco", "XYZ-4321", 4, "Gol")
caminhao = Caminhao("Azul", "KLM-9876", 6, 10000)

# Testando as classes
moto.ligar_motor()
>>> Ligando o motor...

moto.fazer_manobra()
>>> Manobrando a motocicleta...

carro.ligar_motor()
>>> Ligando o motor...

carro.acelerar()
>>> Carro acelerando...

caminhao.ligar_motor()
>>> Ligando o motor...

caminhao.carregar()
>>> Carga carregada!

caminhao.descarregar()
>>> Sim carregado

```

**Pontos Chave:**

- **`super().__init__(...)`:** Chama o construtor da classe pai para inicializar os atributos herdados.
- **`Veiculo`:** A classe pai define características comuns a todos os veículos.
- **`Motocicleta`, `Carro`, `Caminhao`:** Classes filhas herdam de `Veiculo` e adicionam atributos e métodos específicos.

### Aula 4 - Herança Múltipla

Nesta aula, exploramos a **Herança Múltipla**, uma funcionalidade poderosa do Python que permite que uma classe filha herde atributos e métodos de **várias** classes pai.

**Conceito:**

- A Herança Múltipla permite criar classes que combinam características de diferentes tipos, simulando situações complexas do mundo real.
- A classe filha herda os atributos e métodos de todas as classes pai, criando um objeto com múltiplas funcionalidades.

**Exemplo:**

Imagine um sistema de animais que pode ter animais terrestres e animais que voam.

```python
class Animal:
    def __init__(self, nome, especie, patas):
        self.nome = nome
        self.especie = especie
        self.patas = patas

    def emitir_som(self):
        print("Som de animal genérico...")

class Mamifero(Animal):
    def __init__(self, nome, especie, patas, cor_pelo):
        super().__init__(nome, especie, patas)
        self.cor_pelo = cor_pelo

    def amamentar(self):
        print("Amamentando...")

class Ave(Animal):
    def __init__(self, nome, especie, patas, envergadura_asas):
        super().__init__(nome, especie, patas)
        self.envergadura_asas = envergadura_asas

    def voar(self):
        print("Voando...")

class Cachorro(Mamifero): # Herda de Mamifero
    def __init__(self, nome, especie, patas, cor_pelo, raca):
        super().__init__(nome, especie, patas, cor_pelo)
        self.raca = raca

    def latir(self):
        print("Auau!")

class Gato(Mamifero): # Herda de Mamifero
    def __init__(self, nome, especie, patas, cor_pelo, cor_olhos):
        super().__init__(nome, especie, patas, cor_pelo)
        self.cor_olhos = cor_olhos

    def miar(self):
        print("Miau...")

class Avestruz(Ave): # Herda de Ave
    def __init__(self, nome, especie, patas, envergadura_asas, cor_penagem):
        super().__init__(nome, especie, patas, envergadura_asas)
        self.cor_penagem = cor_penagem

    def correr_rapido(self):
        print("Correndo velozmente...")

```
