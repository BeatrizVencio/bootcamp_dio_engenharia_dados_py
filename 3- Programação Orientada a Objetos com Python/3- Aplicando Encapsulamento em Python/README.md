# Aprendendo o Conceito de Herança com Python

### Aula 1 - O que é Encapsulamento?

Nesta aula, o instrutor explica o conceito de **encapsulamento**, um dos pilares da programação orientada a objetos (POO), mostrando como ele garante a segurança e integridade dos dados de uma classe.

**O que é Encapsulamento?**

- O encapsulamento é uma técnica que envolve agrupar dados (atributos) e métodos (ações) de uma classe e controlar o acesso a esses dados.
- Ele impede que o código externo modifique os dados diretamente, garantindo que a estrutura da classe seja mantida e evitando alterações acidentais.

**Exemplo:**

Imagine uma classe `Conta` que representa uma conta bancária. Ela possui um atributo privado `saldo`, que armazena o saldo da conta. Para modificar o saldo, a classe oferece métodos públicos:

- `depositar(valor)`: Adiciona dinheiro ao saldo.
- `sacar(valor)`: Remove dinheiro do saldo.

**Como o Encapsulamento Funciona:**

- A classe `Conta` controla o acesso ao `saldo` através de seus métodos, garantindo que o saldo seja modificado de forma segura e controlada.
- O usuário da classe não precisa se preocupar com a implementação interna dos métodos, apenas com o que eles fazem.

**Vantagens do Encapsulamento:**

- **Segurança:** Impedir modificações diretas aos atributos da classe garante que a integridade dos dados seja mantida.
- **Manutenção:** Facilita a modificação do código interno da classe sem afetar o código externo que usa a classe.
- **Modularidade:** Permite criar classes independentes e reutilizáveis.

### Aula 2 - Recursos públicos e privados

Nesta aula, o instrutor aprofunda a explicação sobre recursos públicos e privados em Python, mostrando como eles se aplicam ao encapsulamento e como usar convenções de nomenclatura para diferenciá-los.

**Recursos Públicos:**

- Em Python, todos os atributos e métodos de uma classe são considerados públicos por padrão.
- Isso significa que qualquer código pode acessá-los e modificá-los diretamente, sem restrições.

**Recursos Privados:**

- Para tornar um atributo ou método privado, use um *underline* (`_`) antes de seu nome.
- O interpretador Python não impede o acesso a recursos privados, mas é uma convenção que sinaliza que esses recursos **não devem ser usados diretamente** por código externo.

**Exemplo:**

```python
class Pessoa:
    def __init__(self, nome, _idade):  # _idade é um atributo privado
        self.nome = nome
        self._idade = _idade

    def apresentar(self):
        print(f"Olá, meu nome é {self.nome}.")
        print(f"Tenho {self._idade} anos.")

    def get_idade(self): # Método para acessar a idade
        return self._idade

    def set_idade(self, nova_idade): # Método para modificar a idade
        if nova_idade >= 0:
            self._idade = nova_idade
        else:
            print("Idade inválida!")

# Criando objeto
pessoa1 = Pessoa("Beatriz", 21)
pessoa1.apresentar()
>>> Olá, meu nome é Beatriz.
>>> Tenho 21anos.

# Acessando o atributo privado diretamente (não recomendado)
print(pessoa1._idade)
>>> 21

# Acessando o atributo usando o método público
print(pessoa1.get_idade())
>>> 21

# Modificando o atributo usando o método público
pessoa1.set_idade(21)
>>> Olá, meu nome é Beatriz.
>>> Tenho 21 anos.

```

**Observações:**

- É importante respeitar a convenção do *underline* para que outros programadores entendam que o atributo ou método é privado e não deve ser usado diretamente.
- Embora o interpretador Python não impeça o acesso, é fundamental usar métodos públicos para interagir com recursos privados, garantindo a integridade e a manutenção do código.

O encapsulamento é uma prática crucial em POO, que promove a organização, segurança e manutenção de código. Experimente usar recursos públicos e privados para gerenciar o acesso a dados e métodos em suas classes.

### Aula 3 - Propriedades

Agora, vamos conhecer o conceito de **"propriedades"**, uma forma mais elegante e controlada de trabalhar com atributos em classes.

**Por que usar propriedades?**

- **Encapsulamento:** Permite controlar o acesso aos atributos da classe, garantindo que as modificações ocorram de maneira segura.
- **Validação de Dados:** Pode aplicar validação para garantir que os atributos recebam valores adequados.
- **Flexibilidade:** Simplifica a modificação da implementação interna da classe sem afetar o código externo.

**Criando Propriedades em Python:**

- Utilize o decorador `@property` para definir o *getter*, que é usado para **ler o valor** de um atributo.
- Utilize o decorador `@atributo.setter` para definir o *setter*, que é usado para **modificar o valor** de um atributo.

**Exemplo:**

```python
class Pessoa:
    def __init__(self, nome, _idade):
        self._nome = nome
        self._idade = _idade

    @property # Getter para o atributo "nome"
    def nome(self):
        return self._nome.title() # Retorna o nome com a primeira letra em maiúscula

    @nome.setter # Setter para o atributo "nome"
    def nome(self, novo_nome):
        if novo_nome.isalpha():
            self._nome = novo_nome
        else:
            print("Nome inválido!")

    @property # Getter para o atributo "idade"
    def idade(self):
        return self._idade

    @idade.setter # Setter para o atributo "idade"
    def idade(self, nova_idade):
        if nova_idade >= 0:
            self._idade = nova_idade
        else:
            print("Idade inválida!")

```

**Como Usar Propriedades:**

```python
pessoa1 = Pessoa("Beatriz", 21)
print(pessoa1.nome) # Acessando o nome (getter)
>>> Beatriz

pessoa1.nome = "joao" # Modificando o nome (setter)
>>> Olá, meu nome é João.
>>> Tenho 21 anos.

pessoa1.idade = 30 # Modificando a idade (setter)
>>> Olá, meu nome é João.
>>> Tenho 30 anos.

pessoa1.idade = -10 # Tentando atribuir uma idade inválida
>>> Idade inválida!

```

**Observações:**

- **`_nome` e `_idade` são os atributos privados.** O código externo não deve acessá-los diretamente.
- **`nome` e `idade` são as propriedades.** Elas permitem acessar e modificar os atributos de forma controlada.
- **`getter`:** O método `nome` (ou `idade`) é chamado quando você acessa a propriedade.
- **`setter`:** O método `nome` (ou `idade`) é chamado quando você atribui um novo valor à propriedade.

Usando propriedades, você garante que os atributos de suas classes sejam manipulados de forma segura e organizada.
