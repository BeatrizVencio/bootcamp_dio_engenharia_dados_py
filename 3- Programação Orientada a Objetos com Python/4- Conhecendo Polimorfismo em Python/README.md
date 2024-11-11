# Conhecendo Polimorfismo em Python

### Aula 1 - O que é Polimorfismo?

A aula 1 sobre polimorfismo em Python introduz esse conceito fundamental, que é uma das características da programação orientada a objetos (POO), permitindo que o mesmo código funcione com diferentes tipos de objetos.

**O que é Polimorfismo?**

- A palavra "polimorfismo" significa ter muitas formas.
- Na programação, o polimorfismo significa que você pode usar o mesmo nome de função (com assinaturas diferentes), mas ela se comporta de maneiras diferentes dependendo do tipo de dados que você está passando.

**Exemplo:**

Imagine a função `len()` em Python, que calcula o tamanho de um objeto. Ela funciona com strings, listas e tuplas:

```python
texto = "Python"
lista = [1, 2, 3, 4]
tupla = (1, 2, 3)

print(len(texto)) # Saída: 6
print(len(lista))  # Saída: 4
print(len(tupla))  # Saída: 3

```

- A função `len()` tem o mesmo nome, mas se adapta ao tipo de objeto que recebe:
    - String: Conta o número de caracteres.
    - Lista: Conta o número de elementos.
    - Tupla: Conta o número de elementos.

**Próximos Passos:**

- **Polimorfismo com Herança:** Explore como a herança em Python facilita a implementação do polimorfismo.

Com o conhecimento de polimorfismo, poderemos escrever o código mais flexível, reutilizável e fácil de entender.

### Aula 2 - Polimorfismo com Herança

Nesta aula, é demonstrado como o polimorfismo se integra à herança em Python, criando um sistema onde a mesma função pode ser utilizada com diferentes tipos de objetos, desde que compartilhem um método em comum.

**Polimorfismo na Herança:**

- A chave do polimorfismo com herança está na **sobreposição de métodos**, ou seja, redefinir um método herdado da classe pai na classe filha.
- Mesmo com diferentes implementações, o nome do método se mantém, permitindo usar o mesmo código para diferentes tipos de objetos.

**Exemplo:**

- Cria uma classe base `Passaro` com um método `voar()`.
- As classes filhas `Pardal` e `Avestruz` herdam de `Passaro`, mas redefinem o método `voar()` para representar comportamentos específicos.

```python
class Passaro:
    def __init__(self):
        pass

    def voar(self):
        print("Passaro voa!")

class Pardal(Passaro):
    def __init__(self):
        pass

    def voar(self):
        print("Pardal voa")

class Avestruz(Passaro):
    def __init__(self):
        pass

    def voar(self):
        print("Avestruz não voa!")

# Função polimórfica
def plano_de_voo(passaro):
    passaro.voar()

# Criando objetos
pardal = Pardal()
avestruz = Avestruz()

# Usando a função polimórfica
plano_de_voo(pardal)
>>> Pardal voa
plano_de_voo(avestruz)
>>> Avestruz não voa!

```

**Observações:**

- A função `plano_de_voo()` recebe um objeto do tipo `Passaro` como parâmetro e chama o método `voar()`.
- A função `plano_de_voo()` não precisa saber qual tipo específico de pássaro está sendo passado.
- O polimorfismo faz com que o método correto `voar()` seja executado, de acordo com a classe do objeto.
