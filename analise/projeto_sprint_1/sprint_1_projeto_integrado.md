[[TripleTen - DA]] 
<div>
Olá, Alexandre!

Meu nome é Luiz. Fico feliz em revisar seu projeto. Ao longo do texto farei algumas observações sobre melhorias no código e também farei comentários sobre suas percepções sobre o assunto. Estarei aberto a feedbacks e discussões sobre o tema.

**Peço que mantenha e não altere os comentários que eu fizer por aqui para que possamos nos localizar posteriormente, ok?**

Mais uma coisa, vamos utilizar um código de cores para você entender o meu feedback no seu notebook. Funciona assim:

<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Sucesso. Tudo foi feito corretamente.
</div>

<div class="alert alert-block alert-warning">
<b>Comentário do revisor: </b> <a class="tocSkip"></a>

Alerta não crítico, mas que pode ser corrigido para melhoria geral no seu código/análise.
</div>

<div class="alert alert-block alert-danger">

<b>Comentário do revisor: </b> <a class="tocSkip"></a>
    
Erro que precisa ser arrumado, caso contrário seu projeto **não** será aceito.
</div>

Você pode interagir comigo através dessa célula:
<div class="alert alert-block alert-info">
<b>Resposta do Aluno.</b> <a class="tocSkip"></a>
</div>

<div class="alert alert-block alert-success">
<b> Comentário geral do revisor</b> <a class="tocSkip"></a>

Obrigado por enviar o seu projeto e por chegar até aqui. Saber manipular corretamente as funções e operadores no python é muito relevante para uma carreira na área de dados.
    
<br>
    
Essa versão do seu trabalho ficou muito boa! Espero que as sugestões sejam relevantes para projetos futuros.
    
<br>
Te desejo uma jornada de muito sucesso e aprendizado.
    
<br>   
    
Qualquer dúvida, pode contar comigo.   
    
<br>  
    
**Até breve!**

</div>

Uma empresa de comércio eletrônico, Store 1, começou recentemente a coletar dados sobre seus clientes. O objetivo da Store 1 é entender melhor o comportamento dos clientes e tomar decisões baseadas em dados para melhorar experiência online deles.

Como parte da equipe analítica, sua primeira tarefa é avaliar a qualidade de uma amostra de dados coletados e preparar elas para análises futuras.

# Quiz

A Store 1 visa garantir a consistência na coleta de dados. Como parte desse esforço, a qualidade dos dados coletados sobre os usuários precisa ser avaliada. Foi pedido que você revise os dados coletados e proponha alterações. Abaixo, você verá dados sobre um determinado usuário. Revise os dados e identifique possíveis problemas.


```python
user_id = '32415'
user_name = ' mike_reed '
user_age = 32.0
fav_categories = ['ELECTRONICS', 'SPORT', 'BOOKS']
```

**Opções:**

1. O tipo de dados de `user_id` deve ser alterado de string para número inteiro (integer).
    
2. A variável `user_name` contém uma string com espaçamento desnecessário e um sublinhado entre o nome e o sobrenome.
    
3. O tipo de dados de `user_age` está incorreto.
    
4. A lista `fav_categories` contém strings em letras maiúsculas. Em vez disso, devemos converter os valores da lista para letras minúsculas.

Escreva na célula Markdown abaixo o número de opções que você identificou como problemas. Se você identificou vários problemas, separe o número por vírgulas. Por exemplo, se você acha que os números 1 e 3 estão incorretos, escreva 1, 3, e explique o motivo.

**Escreva sua resposta e explique seu raciocínio:**


**Resposta:**
1,2,3

**Explicação:**
1.  A variável `ser_id` deve ser transformada em um numero inteiro para a melhor consistência e manipulação dos tipos de dados que serão dispostos na mesma.
2.  Os espaçamentos na variável `use_name` devem ser retiradas para evitar possiveis futuros erros na manipulação de strings e os sublinhados **podem** ser substituidos por espaçamentos, pois são strings, para uma leitura facilitada.
3.  A variável `user_age` deve ser em número inteiro.
4.  Não é uma regra, porém, por motivo de consistência do código acima, é recomendado que a lista `fav_categories` tenha suas informações em minúsculas assim como as strings `user_name`.

<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Boa análise, mas leve em consideração que essas características podem mudar a depender do problema em questão.
</div>

# Tarefa 1

Vamos implementar as mudanças que identificamos. Primeiro, queremos corrigir os problemas com a variável `user_name`. Como verificamos, ela possui espaços desnecessários e um sublinhado como separador entre o nome e o sobrenome. Seu objetivo é remover os espaços e depois substituir o sublinhado por espaço.


```python
user_name = ' mike_reed '
user_name = user_name.strip() # retirando o espaço no começo e fim da string
user_name = user_name.replace('_',' ') #Substituindo o sublinhado por espaço

print(user_name)
```

    mike reed


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto! O estudante usou corretamente os métodos `strip()` e `replace()`.
</div>

# Tarefa 2

Em seguida, precisamos dividir o `user_name` atualizado em duas substrings para obter uma lista que contém dois valores: a string para o nome e a string para o sobrenome.


```python
user_name = 'mike reed'
name_split = user_name.split()

print(name_split)
```

    ['mike', 'reed']


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto! O método `split()` permite quebrar uma string em um delimitador. 
</div>

# Tarefa 3

Ótimo! Agora queremos trabalhar com a variável `user_age`. Como mencionamos antes, ela possui um tipo de dados incorretos. Vamos corrigir esse problema transformando o tipo de dados e imprimindo o resultado final.


```python
user_age = 32.0
user_age = int(user_age)

print(user_age)
```

    32


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto. O estudante converteu o tipo de dado do atributo "idade" para `int`.
</div>

# Tarefa 4

Como sabemos, os dados nem sempre são perfeitos. Temos que considerar cenários em que o valor de `user_age` não pode ser convertido em um número inteiro. Para evitar que nosso sistema falhe, devemos tomar medidas com antecedência.

Escreva um código que tenta converter a variável `user_age` em um número inteiro e atribua o valor transformado a `user_age_int`. Se a tentativa falhar, vamos exibir uma mensagem solicitando que o usuário forneça sua idade como um valor numérico com a mensagem: `Forneça sua idade como um valor numérico.`


```python
user_age = 'thirty two' # esta é a variável que armazena a idade como uma string.

# escreva um código que vai tentar transformar user_age em um número inteiro e, se falhar, vai imprimir a mensagem especificada
try:
    user_age_int = int(user_age)
except:
    print('Forneça sua idade como um valor numérico.')
```

    Forneça sua idade como um valor numérico.


<div class="alert alert-block alert-warning">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Aqui você poderia especificar qual tipo de exceção o seu código irá manipular. Adicione a exceção do tipo `ValueError` nesse caso.
    
Referência: https://www.w3schools.com/python/python_try_except.asp.
</div>

# Tarefa 5

Por fim, observe que todas as categorias de favoritos são armazenadas em letras maiúsculas. Para preencher uma nova lista chamada `fav_categories_low` com as mesmas categorias, mas em letras minúsculas, repita os valores na lista `fav_categories`, os modifique e anexe os novos valores à lista `fav_categories_low`. Como sempre, imprima o resultado final.


```python
fav_categories = ['ELECTRONICS', 'SPORT', 'BOOKS']
fav_categories_low = []

# escreva seu código aqui
fav_categories_low = [ categorie.lower() for categorie in fav_categories]
# não remova a instrução de impressão abaixo
print(fav_categories_low)
```

    ['electronics', 'sport', 'books']


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto. Bom trabalho usando `list comprehensions`!
</div>


# Tarefa 6

Conseguimos informações adicionais sobre os hábitos de consumo de nossos usuários, incluindo o valor gasto em cada uma de suas categorias favoritas. A administração está interessada nas seguintes métricas:

- Valor total gasto pelo usuário
- Valor mínimo gasto
- Valor máximo gasto

Vamos calcular e imprimir esses valores:


```python
fav_categories_low = ['electronics', 'sport', 'books']
spendings_per_category = [894, 213, 173]

total_amount = sum(spendings_per_category)
max_amount = max(spendings_per_category)
min_amount = min(spendings_per_category)

# não remova a instrução de impressão abaixo
print(total_amount)
print(max_amount)
print(min_amount)
```

    1280
    894
    173


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto. O estudante calculou corretamente o valor total, mínimo e máximo. 
</div>

# Tarefa 7

A empresa quer oferecer descontos aos seus clientes fiéis. Clientes que fizerem compras totalizando mais de $1.500 são considerados fiéis e vão receber um desconto.

Nosso objetivo é criar um ciclo `while` que verifique o valor total gasto e pare quando ele for atingido. Para simular novas compras, a variável `new_purchase` gera um número entre 30 e 80 em cada ciclo. Isso representa a quantidade de dinheiro gasto em uma nova compra, e é o que você precisa adicionar ao total.

Assim que o valor alvo for atingido e o ciclo `while` for encerrado, o valor final será impresso.


```python



from random import randint

total_amount_spent = 1280
target_amount = 1500 

while total_amount_spent < target_amount:
	new_purchase = randint(30, 80) # geramos um número aleatório de 30 a 80
	total_amount_spent += new_purchase
    
print(total_amount_spent)



```

    1506


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto!
</div>


# Tarefa 8

Agora temos todas as informações sobre um cliente da maneira que queremos. A administração de uma empresa nos pediu para encontrar uma maneira de resumir toda a informação sobre um usuário. Seu objetivo é criar uma string formatada que usa informações das variáveis ​​`user_id`, `user_name` e `user_age`.

Aqui está a string final que queremos criar: `Usuário 32415 chama-se mike e tem 32 anos.`


```python
user_id = '32415'
user_name = ['mike', 'reed']
user_age = 32

user_info = f"Usuário {user_id} chama-se {user_name[0]} e tem {user_age}."

# não remova a instrução de impressão abaixo
print(user_info)
```

    Usuário 32415 chama-se mike e tem 32.


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto. Bom trabalho usando `f-strings`!
</div>


Como você já deve saber, as empresas coletam e armazenam dados de uma maneira específica. A Store 1 deseja armazenar todas as informações sobre seus clientes em uma tabela.

| user_id | user_name | user_age | purchase_category | spending_per_category |
| --- | --- | --- | --- | --- |
| '32415' | 'mike', 'reed' | 32 | 'electronics', 'sport', 'books' | 894, 213, 173 |
| '31980' | 'kate', 'morgan' | 24 | 'clothes', 'shoes' | 439, 390 |

Em termos técnicos, uma tabela é simplesmente uma lista aninhada que possui uma sublista para cada usuário.

A Store 1 criou essa tabela para seus usuários. Ela está armazenada na variável `users`. Cada sublista contém o ID do usuário, nome e sobrenome, idade, categorias favoritas e o valor gasto em cada categoria.

# Tarefa 9

Para calcular a receita da empresa, siga estas etapas:

1. Use um ciclo `for` para iterar na lista `users`.
2. Extraia a lista de gastos de cada usuário e some os valores.
3. Atualize o valor da receita com o total de cada usuário.

Isso vai fornecer a receita total da empresa, que você vai imprimir no final.


```python


users = [
	  # este é o começo da primeira sublista
    ['32415', ['mike', 'reed'], 32, ['electronics', 'sport', 'books'],
        [894, 213, 173]
    ], # este é o fim da primeira sublista

    # este é o começo da segunda sublista
    ['31980', ['kate', 'morgan'], 24, ['clothes', 'shoes'],
        [439, 390]
    ] # este é o fim da segunda sublista
]

revenue = 0

for user in users:
	spendings_list = user[-1]
	total_spendings = sum(spendings_list)
	revenue += total_spendings

# não remova a instrução de impressão abaixo

print(revenue)

```

    2109


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto!
</div>


# Tarefa 10

Use um ciclo for para percorrer a lista de usuários que fornecemos e imprima os nomes dos clientes com menos de 30 anos.


```python
users = [
    ['32415', ['mike', 'reed'], 32, ['electronics', 'sport', 'books'],
     [894, 213, 173]],
    ['31980', ['kate', 'morgan'], 24, ['clothes', 'books'], [439,
     390]],
    ['32156', ['john', 'doe'], 37, ['electronics', 'home', 'food'],
     [459, 120, 99]],
    ['32761', ['samantha', 'smith'], 29, ['clothes', 'electronics',
     'beauty'], [299, 679, 85]],
    ['32984', ['david', 'white'], 41, ['books', 'home', 'sport'], [234,
     329, 243]],
    ['33001', ['emily', 'brown'], 26, ['beauty', 'home', 'food'], [213,
     659, 79]],
    ['33767', ['maria', 'garcia'], 33, ['clothes', 'food', 'beauty'],
     [499, 189, 63]],
    ['33912', ['jose', 'martinez'], 22, ['sport', 'electronics', 'home'
     ], [259, 549, 109]],
    ['34009', ['lisa', 'wilson'], 35, ['home', 'books', 'clothes'],
     [329, 189, 329]],
    ['34278', ['james', 'lee'], 28, ['beauty', 'clothes', 'electronics'
     ], [189, 299, 579]],
    ]

for user in users:
    if user[2] < 30:
        name_user = " ".join(user[1]) # Usei metodo "join" para facilitar leitura
        print(name_user)
```

    kate morgan
    samantha smith
    emily brown
    jose martinez
    james lee


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto. Bom trabalho com a formatação de saída da questão acima!
</div>


# Tarefa 11

Vamos juntar as tarefas 9 e 10 e imprimir os nomes de usuários com menos de 30 anos com gastos totais acima de 1.000 dólares.


```python
users = [
    ['32415', ['mike', 'reed'], 32, ['electronics', 'sport', 'books'],
     [894, 213, 173]],
    ['31980', ['kate', 'morgan'], 24, ['clothes', 'books'], [439,
     390]],
    ['32156', ['john', 'doe'], 37, ['electronics', 'home', 'food'],
     [459, 120, 99]],
    ['32761', ['samantha', 'smith'], 29, ['clothes', 'electronics',
     'beauty'], [299, 679, 85]],
    ['32984', ['david', 'white'], 41, ['books', 'home', 'sport'], [234,
     329, 243]],
    ['33001', ['emily', 'brown'], 26, ['beauty', 'home', 'food'], [213,
     659, 79]],
    ['33767', ['maria', 'garcia'], 33, ['clothes', 'food', 'beauty'],
     [499, 189, 63]],
    ['33912', ['jose', 'martinez'], 22, ['sport', 'electronics', 'home'
     ], [259, 549, 109]],
    ['34009', ['lisa', 'wilson'], 35, ['home', 'books', 'clothes'],
     [329, 189, 329]],
    ['34278', ['james', 'lee'], 28, ['beauty', 'clothes', 'electronics'
     ], [189, 299, 579]],
    ]


for user in users:
    if 30 > user[2] and sum(user[-1]) > 1000:
        name_user =  " ".join(user[1])
        print(name_user)
    # escreva seu código aqui
```

    samantha smith
    james lee


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto!
</div>


# Tarefa 12

Agora vamos imprimir o nome e a idade de todos os usuários que compraram roupas (clothes). Imprima o nome e a idade na mesma instrução de impressão.


```python


users = [
    ['32415', ['mike', 'reed'], 32, ['electronics', 'sport', 'books'],
     [894, 213, 173]],
    ['31980', ['kate', 'morgan'], 24, ['clothes', 'books'], [439,
     390]],
    ['32156', ['john', 'doe'], 37, ['electronics', 'home', 'food'],
     [459, 120, 99]],
    ['32761', ['samantha', 'smith'], 29, ['clothes', 'electronics',
     'beauty'], [299, 679, 85]],

    ['32984', ['david', 'white'], 41, ['books', 'home', 'sport'], [234,
     329, 243]],
    ['33001', ['emily', 'brown'], 26, ['beauty', 'home', 'food'], [213,
     659, 79]],
    ['33767', ['maria', 'garcia'], 33, ['clothes', 'food', 'beauty'],
     [499, 189, 63]],
    ['33912', ['jose', 'martinez'], 22, ['sport', 'electronics', 'home'
     ], [259, 549, 109]],
    ['34009', ['lisa', 'wilson'], 35, ['home', 'books', 'clothes'],
     [329, 189, 329]],
    ['34278', ['james', 'lee'], 28, ['beauty', 'clothes', 'electronics'
     ], [189, 299, 579]],
    ]
for user in users:
    if 'clothes' in user[3]:
        user_name = ' '.join(user[1])
        user_age = user[2]
        print(user_name,user_age)
```

    kate morgan 24
    samantha smith 29
    maria garcia 33
    lisa wilson 35
    james lee 28


<div class="alert alert-block alert-success">
<b> Comentário do revisor: </b> <a class="tocSkip"></a>

Correto!
</div>


Apanhei bastante mas acho que consegui.
