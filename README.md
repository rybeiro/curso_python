# Curso Python | IDE Jupyter
Esse repositório ficará registrado os principais recursos utilizados nesse curso para consultas futuras.

No arquivo Dockerfile utilizamos a imagem minima do Jupyter. Existem outras imagens mais completas que podem ser encontradas em [Docker Hub - Jupyter](https://hub.docker.com/search?q=jupyter&type=image)

# Curso Python
- Linguagem de alto nível
> Blocos de código em Python devem ter dois pontos (:) e o conteúdo do bloco deve estar identado.
## Comandos Utilitários
#### ***dir()*** | exibe todos os tipos de atributos e funções/métodos de um tipo de dado ou variável.

Exemplo:
```
dir("Fabio")
````

#### ***help()*** | exibe a documetação de como utilizar os atributos/propriedades e funções/métodos disponíveis.

Exemplo:
```
help("Fabio".lower)
```

### ***type()*** | exibe o tipo de dado de uma variável.

Exemplo:
```
type(7.0)
```

## Operadores aritméticos
Subtração: 7 - 4 = 3

Adição: 7 + 4 = 11

Multiplicação: 7 * 4 = 28

Divisão: 7 / 4 = 1.75 # Aqui o resultado é um Float e se precisar do resultado em Inteiro deveira fazer *casting*. Mas o Python nós dá a solução Pythonica.

Módulo: 7 % 4 = 3

**Formas Phytonicas:**

Divisão Phytônica: 7 // 4 = 1

Exponenciação: 3 ** 3 = 9

**Dica:**

1000000000 | 1bi | Escrever números de forma mais legível de forma Phytonica: 1_000_000_000 o resultado final será o mesmo.

## Tipos de dados
Integer => 7

Float   => 7.0

Complex => 7j (basta adicionar o **j** ao lado do número)

Boolean => True | False

String  => Texto

None => Sem tipo definido


# Estrutura condicional
**if | elif | else**
```
if idade < 16:
    exit()
elif idade < 18:
    "Acesso limitado"
else
    "Acesso total"
```
```
# esse exemplo é o in_array do PHP
if 7 in range(10):
    print("encontrado")
else:
    print("Não encontrado")
```
# Operadores lógicos
## Operadores binários
**and | or | is**
```
if ativo and logado:
    "Bem vindo"
elif ativo or logado:
    "Acesso negado"

if ativo is True:
    "Acesso autorizado"
```
## Operadores unários
**not**
```
if not ativo:
    "Acesso negado"
```

# Estrutura de repetição
**loop for**
```
for coluna in tabela:
    print(coluna)

```
**loop while**
```
num = 1
while num < 10:
    print(num)
    num = num + 1

```

# Collections | Coleções
**lista / list()** vetor/matriz são a mesma coisa que *array*. Em Python é dinâmico e podem receber qualquer tipo de dado como valor.

```lista = [] ou lista = list()```

```lista = list(range(10))```

Adicionar 1:1 elemento na lista => lista.append()

Adicinar 1:N elementos na lista => lista.extend([])

Adicionar 1:1 elemento em uma posição especifica da lista => lista.insert(posicao, valor)

Inverter a ordem => lista.reverse()

Inverter a ordem => lista[::-1]

Ordernar a lista => lista.sort()

Copiar uma lista => lista.copy()

Tamanho de uma lista => len(lista)

Remover último elemento da lista => lista.pop() # Remove e retorna o elemento removido.

Remover elemento pela posição => lista.pop(2) # Se não houver o índice informado dá error

Limpar a lista => lista.clear()

Criar lista com indice => list(enumerate(range(inicio,fim)))

Encontrar o índice através do valor => lista.index(valor) # retorna a primeira ocorrencia # Se não existe gerar error

Encontrar o índice através do valor e posição => lista.index(valor, posicao)

Encontrar o índice através do valor e intervalo (posição) => lista.index(valor, pos_ini, pos_fim)

Utilizando o *slicing* na lista => ```lista[inicio:fim:passo]```

Retornar a partir de uma posição inicial => ```lista[1:]```

Retornar até uma determinada posição fim => ```lista[:3]```

Retornar dos elementos => ```lista[::]```

Retornar Soma, Máximo, Mínimo, Tamanho | Para isso a lista deve se do tipo *integer ou float*

sum(lista) | max(lista) | min(lista) | len(lista)

Desempacotamento de lista => ```lista[1,2,3] / num1, num2, num3 = lista```

Copiando uma lista para outra Métodos *Shallow copy e Deep copy*

*Deep copy* => Cria uma nova instância

```lista[1,2,3]```

```nova_lista = lista.copy()```

```nova_lista.append(4)```

```print(lista)```

```print(nova_lista)```

*Shallow copy* => utiliza a mesma instância e a alteração afeta as duas variáveis.

**tupla / tuple()** Diferente de lista são imutáveis e é representada por (). Tuplas são definidas a partir da vírgula.

```tupla = (4,) | tupla = (1,2) | tupla = 1, | tupla = 1,2```

Também podemos aplicar a Soma, Máximo, Mínimo e Tamanho nas tuplas igualmente às listas.

> Na tupla não temos problema de *Shallow copy* na atribuição.

Acessar elemento da tupla

**Dicionário/Mapa** Em alguma linguagens são conhecida com Mapas.
- Dicionário/Mapa são coleções do tipo *chave/valor* e são representadas por {'chave':'valor'}.

Criar dicionário =>
- Mais comum: dicionario = {'br': 'Brasil', 'en': 'Estados unidos'}
- Menos comum: dicionario = dict(br='Brasil', en='Estados unidos')

Acessar o elemento do dicionário
- Forma recomendada porque se a chave não existir retorna None: ```dicionario.get('br')```
- Forma não recomendada porque se a chave não existir retorna um *error* ```dicionario['br']```
- Setando valor padrão se retornar None: ```dicionario.get('ru', 'Não encontrado')
- Verificar se existe uma chave em um dicionário: ```'br' in dicionario```
- Podemos utilizar qualquer tipo de dado: ```string, integer, float, boolean, list, tuple``` como chave no dicionário.

Adicionar ou atualizar elementos no dicionário
- Atribuição mais comum: ```dicionario['ru'] = 'Russia'```
- Outra forma de atribuição: ```dicionario.update({'ru': 'Russia'})```

Remover
- Forma 1 ```dicionario.pop(chave)``` retornar o valor
- Forma 2 ```del dicionario['chave']``` não retornar

Métodos
- {}.clear() Limpar o dicionario ```dicionario.clear()``` Zera o dicionário
- {}.copy() Cópia com *Deep copy* ```novo = dicionario.copy()``` copia para uma nova instância
- Cópia com *Shallow copy* ```novo = dicionario```copia e aponta para mesma instância
- {}.keys ```dicionario.keys()``` retorna um dicionário de chaves.
- {}.values ```dicionario.values()``` retorna um dicionário de valores.
- {}.items ```dicionario.items()``` retorna uma lista contendo uma tupla

Formas para criar um dicionário com o método fromkeys()
- {}.fromkeys() - Forma 1: ```usuario = {}.fromkeys('a', 'b')``` *output: {'a': 'b'}*
- {}.fromkeys() - Forma 2: ```usuario = {}.fromkeys(['nome', 'sobrenome', 'email', 'profile'], 'desconhecido')``` *output: {'nome': 'desconhecido', 'sobrenome': 'desconhecido', 'email': 'desconhecido'}*
- {}.fromkeys() - Forma 3: ```usuario = {}.fromkeys('teste', 'João')``` *output: {'t': 'João', 'e': 'João', 's': 'João'* Repare que não repetiu a chave te. *Vide nota*.

> Para iteirar em um dicionário utilizar o formato Phytônico

```
meses = {'jan': 1, 'fev': '2', 'mar': 3}
for mes in meses.keys():
    print(mes)

for mes in meses.values():
    print(mes)
```
> Em dicionário não aceitam chaves duplicadas. Se passar uma chave existente o valor será atualizado.


**Conjunto** É uma referência a Teoria dos Conjuntos da Matemática.
- Em Python **conjuntos** são *Sets*
- Sets (conjuntos) são representados por {} e diferentemente do *dict* só possue valor.

Definindo um Set (conjunto)
- Mais comum, Forma 1: ```conjunto = {1,2,3,4,3,2,1}
- Menos usual, Forma 2: ```conjunto = set({1,2,3,4,4,2,3,})``` definimos com valores repetidos.

Adicionar elemento
- {}.add() ```conjunto.add(7)```

Remover elemento
- {}.remove() Forma 1: ```conjunto.remove(7)``` Se não existir o valor gera um *error*
- {}.discard() Forma 2: ```conjunto.discard(7)```Se não existir nenhum *error* é gerado

Copiar
- {}.copy *Deep copy* ```novo = conjunto.copy()``` Copia e aponta para um nova instância
- *Shallow copy ``` novo = conjunto``` copia e aponta para mesma instância
- {}.clear() - Limpar conjunto ```conjunto.clear()```

Teoria dos Conjuntos |
- alunos_python={'Fabio', 'Maria', 'Jose', 'Joaquina'}
- alunos_php={'Fabio', 'Maria', 'Patricia', 'Laura'}
- {}.union({}) - União - Forma 1: ```alunos_php.union(alunos_python)``` recomendado para legibilidade
- {} | {} - União - Forma 2: ```alunos_php | alunos_python```
- {}.intersection({}) - Intersecção - Forma 1: ``````alunos_php.intersection(alunos_python)```
- {} & {} - Intersecção - Forma 2: ``````alunos_php & alunos_python```
- {}.difference({}) - Intersecção - Forma 1: ``````alunos_php.difference(alunos_python)```

> Sets (conjuntos) não aceitam valores duplicados. Não possuem valores ordenados. Não são acessados via índice.
> Utilidade do Set converter list(), tuple() em set para remover repetições.

# *Collections* | High Performance Container Datetypes
Tipos de dados de container de alta performance.

### Módulo *Couter* | Contador
Recebe um iterável como parâmetro e cria um objeto *Collection Couter* parecido com um dicionário (chave/valor) sendo a **chave** será o elemento do iterável e o **valor** a quantidade de ocorrências desse elemento.

- Uso => temos que importar: ```from collections import Counter```
- Exemplo:
```
from collections import Counter
lista = [1,2,3,1,2,3,1,2,3,4,5,4,5,4,6,78,8,54,3,22,4,4,5,3,2,24,3]
counter = Counter(lista)
print(counter)
```

### Módulo *Default Dict*
É o dicionário de alta performance. Na criação desse dicionário é necessário indicar um valor *default* e caso seja consultado uma chave inexistente, será criada a chave com valor default, para isso utilizaremos *lambda*.

- Uso => temos que importar: ```from collections import defaultdict```
- Exemplo:
```
from collections import defaultdict
dicionario = defaultdict(lambda: 0)
dicionario['curso'] = 'PHP'
print(dicionario)
dicionario['outro']
print(dicionario)
```

### Módulo *Ordered Dict*
Esse dicionário garante a ordem de inserção dos elementos, diferentemente do dicionário comum.

- Uso => temos que importar ```from collections import OrderedDict```
- Exemplo que demostra a diferença entre o dicionário comum e o Ordered Dict:

**Dicionario comum**

```dict = {'a': 1, 'b': 2}```

```dict2 = {'b': 1, 'a': 2}```

```print(dict == dict2) # Output True porque a ordem dos elementos não importam.```

**Ordered Dict**

```from collections import OrderedDict```

```odict = OrderedDict({'a': 1, 'b': 2})```

```odict2 = OrderedDict({'b': 1, '1': 2})```

```print(dict == dict2) # Output False porque a ordem dos elementos importam.```

### Módulo *Named Tuple*
São tuplas onde podemos definir nomes para os índices.

- Uso => temos que importar ```from collections import namedtuple```
- Formas de declarar, todas produzem o mesmo resultado
    - Forma 1: ```cachorro = namedtuple('cachorro', 'idade raca nome')
    - Forma 2: ```cachorro = namedtuple('cachorro', 'idade, raca, nome')
    - Forma 3: ```cachorro = namedtuple('cachorro', ['idade', 'raca', 'nome'])

```
from collection import namedtuple
cachorro = namedtuple('cachorro', ['idade', 'raca', 'nome'])
tor = cachorro(idade=2, raca='Chow-Chow', nome='tor')
print(tor)
```

- Formas de acesso
    - Forma 1, pelo índice: ```print(tor[0]) ```
    - Forma 2, pela chave: ```print(tor.raca)```

### Módulo *Deque*
Seria uma lista de alta performance. A diferença é que podemos inserir ou remover elementos no Inicio/Fim da lista.

- Uso => temos que importar: ``` from collections import deque```
- Adicionando no inicio: ```lista.appendleft(elemento)
- Adcionando no fim: ```lista.append(elemento)```
- Removendo do inicio: ```lista.popleft()```
- Removendo do fim: ```lista.pop()```
- Para mais métodos consulte o utilitário de ajuda.

# Funções
São pequenos trechos de códigos que realizam tarefas especificas e bem definidas. Funções podem ou não receber parâmentros de entrada e retornar ou não dados.

- Existem função pre-definidas pela linguagem, exemplo: ```print()```
- Uma função é definida a partir da palavra reservada *def*.
- Nome de função deve ser definida com letras minúsculas. ```def nomefuncao():```
- Nome composto deve-se separar por underline (*Snake case*). ```def nome_funcao():```
- Bloco da função ou corpo da função deve ficar identado.
- Usando a função ou executando a função: ```nome_funcao()```
- Para retornar dados em uma função utilizamos a palavra *return*
- *return* finaliza a execução da função.
- Funções com parâmetros de entrada obrigatório. ```def funcao(numero)```
    - **Parâmetro** são variáveis declaradas na definição de uma função
    - **Argumentos** são dados passados na chamada da função
- Função com parâmetros de entrada padrão *default paramters*. ```def exponencial(numero, potencia=2):```
- OBS: Parâmetros com valor padrão DEVEM ser informados no final da declaração
    - ERROR: ```def exponencial(numero=2, potencia):```
    - CORRETO: ```def exponecial(numero, potencia=2):```

# Escopo de variáveis
Variáveis locais é predominante às globais dentro do bloco da função.
- Variáveis globais, são declaradas FORA das funções e são acessíveis em qualquer lugar do programa.
- Variáveis locais, são declaradas DENTRO das funções e só podem ser utilizadas dentro do bloco (escopo) da função.
- Para utilizar uma variável global com mesmo nome de uma variável local é necessário informar ao Python utilizando a palavra reservada **global** antes da variável global.

Exemplos:
> USO ERRADO de variáveis globais com mesmo nome de variável local
```
total = 0

def incrementa():
    total = total + 1
    return total
```

> USO CORRETO de variáveis globais com mesmo nome de variável local
```
total = 0

def incrementa():
    global total
    total = total + 1
    return total
```

> **ATENÇÃO EVITE O USO DE VARIÁVEIS GLOBAIS**

# Princípios
- DRY - Don't Repeat yourself (Não repita seu código ou não repita você mesmo).

# Informações úteis
- Concatenação utizar o símbolo +
- range(1,10) -> utilizado para gerar sequência númerica.

Exemplos:
- ```range(valor_final)```
- ```range(inicio, fim)```
- range(inicio, fim, passo) O passo é o valor de incremento ou decremento.
- enumerate() -> Retorna (index, value)
- Separa a string pelo espaço como default => string.split()
- Para definir o caracter => string.split(';')
- Juntando elementos com separador => "-".join(lista)
- Usando o método *count* para contar valores iguais => lista[1,2,3,4,1,2,2] ```lista.count(2)```
- Encontrar as n ocorrência ```{}.most_common(n)```
