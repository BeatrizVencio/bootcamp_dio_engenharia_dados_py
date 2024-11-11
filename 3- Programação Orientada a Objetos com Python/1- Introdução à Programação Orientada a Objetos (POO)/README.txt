# Introdução à Programação Orientada a Objetos (POO) com Python

### Aula 1 - O que é Orientação a Objetos (OO)?

Nesta aula, exploramos o conceito de Orientação a Objetos (OO), uma das formas mais populares de organizar código, especialmente para projetos grandes e complexos.

**Paradigmas de Programação:**

- Um paradigma de programação é um estilo de programação, uma forma de organizar código.
- Exemplos de paradigmas:
    - Imperativo/Procedural: Foca em sequências de instruções.
    - Funcional: Utiliza funções como blocos de código independentes.
    - Orientado a Eventos: Baseado em eventos que disparam ações.
    - Orientado a Objetos (OO): O foco é em objetos, que representam entidades do mundo real com propriedades e ações.

**Programação Orientada a Objetos (OO):**

- **Objetivo:** Estrutura o código em torno de **objetos**, abstraindo problemas do mundo real.
- **Principais Conceitos:**
    - **Classe:** Um modelo ou blueprint para criar objetos. Define suas propriedades e métodos.
    - **Objeto:** Uma instância de uma classe. Possui seus próprios valores para as propriedades e pode executar os métodos da classe.

**Benefícios da OO:**

- **Reutilização:** Classes podem ser reutilizadas em diferentes partes do código.
- **Modularidade:** O código fica mais organizado e fácil de manter.
- **Extensibilidade:** Facilita a adição de novas funcionalidades sem afetar o código existente.
- **Abstração:** Esconde detalhes complexos, tornando o código mais limpo e fácil de entender.

**Exemplo para ilustrar OO:**

- Imagine um programa que simula um supermercado.
- Você pode criar uma classe `Produto` com propriedades como `nome`, `preco`, `fabricante`, `data_validade`.
- Cada produto no supermercado seria um **objeto** da classe `Produto`, com seus próprios valores para essas propriedades.

### Aula 2 - Os conceitos de Classes e Objetos

Vamos continuar desvendando o mundo da programação orientada a objetos (POO) em Python, aprofundando os conceitos de classes e objetos.

**Classe:**

- Uma classe é como um molde ou um blueprint que define as características (atributos) e os comportamentos (métodos) de um tipo específico de objeto.
- Imagine uma classe como um "modelo" para construir objetos do mesmo tipo.

**Objeto:**

- Um objeto é uma instância de uma classe.
- Ele possui seus próprios valores para os atributos definidos na classe e pode executar os métodos da classe.
- É o "exemplar" da classe, com os dados e as ações configuradas.

**Exemplo:**

```python
class Cachorro:
    def __init__(self, nome, cor, acordado=True):
        self.nome = nome
        self.cor = cor
        self.acordado = acordado

    def latir(self):
        print("Auau!")

    def dormir(self):
        self.acordado = False
        print("Zzzzzz...")

```

- Criamos uma classe `Cachorro` que define as características (nome, cor, estado de vigília) e os comportamentos (latir, dormir) de um cachorro.
- Podemos criar objetos da classe `Cachorro`:
    
    ```python
    rex = Cachorro("Rex", "Marrom")
    luna = Cachorro("Luna", "Branco e Preto", acordado=False)
    
    ```
    
    - `rex` e `luna` são objetos da classe `Cachorro`, cada um com seus próprios nomes e cores. `rex` está acordado, enquanto `luna` está dormindo.

### Aula 3 - Criando seu primeiro Programa com POO

Nesta aula, aplicamos os conceitos de POO aprendidos em Python para criar um programa completo. O objetivo é simular um sistema de registro de vendas de bicicletas.

**O Desafio:**

- Um personagem chamado João tem uma bicicletaria e precisa registrar as vendas.
- O programa deve permitir que João informe a cor, modelo, ano e valor da bicicleta vendida.
- Uma bicicleta deve ter os comportamentos: buzinar, parar e correr.

**Construindo o Programa:**

```python
class Bicicleta: # Define a classe "Bicicleta" 
    def __init__(self, cor, modelo, ano, valor): # Método que inicializa o objeto
        self.cor = cor # Atribui o valor de "cor" ao atributo "cor" 
        self.modelo = modelo # Atribui o valor de "modelo" ao atributo "modelo" 
        self.ano = ano # Atribui o valor de "ano" ao atributo "ano" 
        self.valor = valor # Atribui o valor de "valor" ao atributo "valor" 

    def buzinar(self): # Define o método "buzinar"
        print("Plim-plim...") 

    def parar(self): # Define o método "parar"
        print("Bicicleta parada!") 

    def correr(self): # Define o método "correr"
        print("Bicicleta correndo...") 

    def __str__(self): # Define o método "__str__" - usado para representar o objeto como uma string
        return f"Bicicleta {self.cor}, {self.modelo}, {self.ano}, {self.valor}" # Retorna uma string com informações da bicicleta

# Criando objetos de bicicleta
b1 = Bicicleta("Vermelha", "Caloi", 2022, 600) # Cria um objeto de bicicleta chamado "b1" com dados específicos
b2 = Bicicleta("Verde", "Monark", 2008, 189) # Cria um objeto de bicicleta chamado "b2" com dados específicos

# Testando os objetos e seus métodos
print(b1) 
>>> Bicicleta Vermelha, Caloi, 2022, 600

b1.buzinar() # Chama o método "buzinar" do objeto "b1"
>>> Plim-plim...

b1.correr() # Chama o método "correr" do objeto "b1"
>>> Bicicleta correndo...

b1.parar() # Chama o método "parar" do objeto "b1"
>>> Bicicleta parada!

print(b1.cor) # Imprime o valor do atributo "cor" do objeto "b1"
>>> Vermelha

print(b2) # Imprime as informações da bicicleta "b2"
>>> Bicicleta Amarela, Monark, 2008, 300

b2.buzinar() # Chama o método "buzinar" do objeto "b2"
>>> Plim-plim...

b2.correr() # Chama o método "correr" do objeto "b2"
>>> Bicicleta correndo...

b2.parar() # Chama o método "parar" do objeto "b2"
>>> Bicicleta parada!

print(b2.cor) # Imprime o valor do atributo "cor" do objeto "b2"
>>> Amarela

```

**Pontos Chave:**

- **Classe:** `Bicicleta` define o modelo geral para criar bicicletas.
- **Objeto:** `b1` e `b2` são bicicletas individuais com seus próprios atributos.
- **Atributos:** `cor`, `modelo`, `ano`, `valor` e `marcha` são as características de cada bicicleta.
- **Métodos:** `buzinar`, `parar`, `correr`, `trocar_marcha` e `__str__` são as ações que as bicicletas podem realizar.
- **`self`:** Refere-se à instância do objeto dentro dos métodos.
- **`__str__`:** Define como o objeto é apresentado como string.

### Aula 4 - Construtores e Destrutores

Nesta aula, exploramos os métodos especiais `__init__` (construtor) e `__del__` (destrutor) em Python, que são utilizados para gerenciar o ciclo de vida de objetos.

**Construtor (`__init__`)**

- **Objetivo:** Inicializar o estado de um objeto quando ele é criado.
- **Execução:** O construtor é chamado automaticamente quando você cria uma nova instância da classe.
- **Parâmetros:** O primeiro parâmetro de um construtor é sempre `self`, que representa a própria instância do objeto. Os demais parâmetros podem ser usados para definir os atributos do objeto.

**Exemplo:**

```python
class Cachorro:
    def __init__(self, nome, cor, acordado=True): # Construtor da classe
        self.nome = nome
        self.cor = cor
        self.acordado = acordado

    def latir(self):
        print("Auau!")

    def dormir(self):
        self.acordado = False
        print("Zzzzzz...")

```

**Destrutor (`__del__`)**

- **Objetivo:** Realizar alguma ação antes que um objeto seja destruído da memória.
- **Execução:** Chamado automaticamente quando o interpretador Python decide que um objeto não é mais necessário.
- **Utilização em Python:** Em Python, o uso de destrutores é menos frequente do que em outras linguagens, como C++, pois o gerenciamento de memória (garbage collection) é feito automaticamente. Destrutores podem ser úteis para tarefas como fechar arquivos ou liberar recursos.

**Exemplo:**

```python
class Cachorro:
    def __init__(self, nome, cor, acordado=True):
        self.nome = nome
        self.cor = cor
        self.acordado = acordado

    def latir(self):
        print("Auau!")

    def dormir(self):
        self.acordado = False
        print("Zzzzzz...")

    def __del__(self): # Destrutor da classe
        print("Destruindo a instância...")

```

- Neste exemplo, ao criar um objeto `Cachorro` e, posteriormente, removê-lo da memória, o destrutor será chamado, exibindo a mensagem "Destruindo a instância...".

### Materiais Complementares

[Programação Orientada a Objetos Com Python.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/5d3855c3-2a3f-4d06-8233-dc33a528722a/Programao_Orientada_a_Objetos_Com_Python.pdf)