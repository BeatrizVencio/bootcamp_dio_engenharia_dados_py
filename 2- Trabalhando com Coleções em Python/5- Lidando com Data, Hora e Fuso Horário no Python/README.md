# Lidando com Data, Hora e Fuso Horário no Python

### Aula 1 - Trabalhando com objetos date, datetime e time

Nesta aula, aprendemos a manipular datas e horas em Python utilizando o módulo `datetime`.

**Importando o Módulo `datetime`:**

```python
import datetime
```

**Objeto `date`:**

- Representa uma data (ano, mês, dia).
- Para criar um objeto `date`, use o construtor `date(ano, mês, dia)`.

```python
hoje = datetime.date(2023, 7, 19)
print(hoje) # Saída: 2023-07-19
```

**Objeto `datetime`:**

- Representa uma data e hora (ano, mês, dia, hora, minuto, segundo, microsegundo).
- Para criar um objeto `datetime`, use o construtor `datetime(ano, mês, dia, hora, minuto, segundo, microsegundo)`.

```python
agora = datetime.datetime(2023, 7, 19, 18, 39, 20)
print(agora) # Saída: 2023-07-19 18:39:20

```

**Objeto `time`:**

- Representa um horário (hora, minuto, segundo, microsegundo).
- Para criar um objeto `time`, use o construtor `time(hora, minuto, segundo, microsegundo)`.

```python
horario = datetime.time(18, 39, 20)
print(horario) # Saída: 18:39:20
```

**Métodos Úteis:**

- **`date.today()`:** Retorna a data atual.
- **`datetime.now()`:** Retorna a data e hora atuais.

**Exemplos:**

```python
hoje = datetime.date.today()
print(hoje) # Saída: 2023-07-19 (a data atual no momento da execução)

agora = datetime.datetime.now()
print(agora) # Saída: 2023-07-19 18:39:20 (a data e hora atuais no momento da execução)
```

### Aula 2 - Manipulando datas com timedelta

Nesta aula, aprendemos a usar o objeto `timedelta` para realizar cálculos com datas, como adicionar ou subtrair períodos de tempo.

**Importando o Módulo `datetime`:**

```python
import datetime
```

**Objeto `timedelta`:**

- Representa um intervalo de tempo.
- Para criar um objeto `timedelta`, use o construtor `timedelta(dias, segundos, microsegundos, milissegundos, minutos, horas, semanas)`.

```python
uma_semana = datetime.timedelta(weeks=1)
print(uma_semana) # Saída: 7 days, 0:00:00
```

**Operações com `timedelta`:**

- **Adição:** Some um objeto `timedelta` a um objeto `date` ou `datetime` para adicionar tempo.
- **Subtração:** Subtraia um objeto `timedelta` de um objeto `date` ou `datetime` para subtrair tempo.
- **Comparação:** Compare objetos `timedelta` usando operadores como `>`, `<`, `==`, etc.

```python
hoje = datetime.date.today()
print(hoje) # Saída: 2023-07-19 (a data atual no momento da execução)

uma_semana = datetime.timedelta(weeks=1)
daqui_uma_semana = hoje + uma_semana
print(daqui_uma_semana) # Saída: 2023-07-26

ontem = hoje - datetime.timedelta(days=1)
print(ontem) # Saída: 2023-07-18

# Verificando a diferença entre duas datas
data1 = datetime.date(2023, 7, 10)
data2 = datetime.date(2023, 7, 19)
diferenca = data2 - data1
print(diferenca) # Saída: 9 days, 0:00:00
```

### Aula 3 - Formatando e convertendo datas com strftime e strptime

Nesta aula, aprendemos a formatar datas e horas em Python de acordo com padrões personalizados, utilizando os métodos `strftime` e `strptime`.

**Método `strftime`:**

- Formato **"string format time"**: Converte um objeto `datetime` (ou `date` ou `time`) para uma string formatada de acordo com um código de formatação.
- Utiliza códigos especiais (como "%Y" para ano, "%m" para mês, "%d" para dia, "%H" para hora, etc.) para indicar o formato desejado.

```python
import datetime

data_e_hora = datetime.datetime(2023, 7, 19, 13, 45, 58)

# Formatando a data e hora para "Dia/Mês/Ano Hora:Minuto:Segundo"
data_formatada = data_e_hora.strftime("%d/%m/%Y %H:%M:%S")
print(data_formatada) # Saída: 19/07/2023 13:45:58
```

**Método `strptime`:**

- Formato **"string parse time"**: Converte uma string formatada para um objeto `datetime`.
- Usa o mesmo código de formatação usado em `strftime`, mas para **analisar** a string e criar um objeto `datetime`.

```python
import datetime

data_string = "20/07/2023 13:45:58"

# Convertendo a string para um objeto datetime
data_convertida = datetime.datetime.strptime(data_string, "%d/%m/%Y %H:%M:%S")
print(data_convertida) # Saída: 2023-07-20 13:45:58
```

**Compreendendo Códigos de Formatação:**

- Uma tabela completa com os códigos de formatação para `strftime` e `strptime` está disponível na documentação oficial do Python: https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior

### Aula 4 - Trabalhando com timezone

Nesta aula, aprendemos a lidar com fusos horários (timezones) em Python.

**Importando os Módulos Necessários:**

```python
from datetime import datetime, timedelta, timezone
```

**Criando um objeto `datetime` com `timezone`:**

- Para definir um fuso horário, use o método `timezone(nome_do_fuso)`.
- Use o método `now()` para obter a data e hora atuais nesse fuso horário.

**Exemplo:**

```python
data_e_hora_sp = datetime.datetime.now(timezone('America/Sao_Paulo'))
print(data_e_hora_sp) # Saída: 2023-07-19 15:23:45.196001-03:00 (data e hora em São Paulo)

data_e_hora_oslo = datetime.datetime.now(timezone('Europe/Oslo'))
print(data_e_hora_oslo) # Saída: 2023-07-19 19:23:45.196001+02:00 (data e hora em Oslo)
```

**Convertendo entre Timezones:**

- Utilize o método `astimezone()` para converter um objeto `datetime` para outro fuso horário.

**Exemplo:**

```python
data_e_hora_sp = datetime.datetime.now(timezone('America/Sao_Paulo'))
print(data_e_hora_sp) # Saída: 2023-07-19 15:23:45.196001-03:00 (data e hora em São Paulo)

data_e_hora_utc = data_e_hora_sp.astimezone(timezone('UTC'))
print(data_e_hora_utc) # Saída: 2023-07-19 18:23:45.196001+00:00 (data e hora em UTC)
```

### Materiais Complementares

[data e hora.pptx](https://prod-files-secure.s3.us-west-2.amazonaws.com/5f9b2a52-e80e-40bf-9263-c2b21d7b302c/80f574e2-727e-4bf9-8eda-f19bdee32938/data_e_hora.pptx)