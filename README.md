# Grimorio-Ruby
Aqui você vai encontrar tudo o que eu sei de ruby! Fique a vontade para consultar! ;)  
<img src="https://i.pinimg.com/originals/e6/1a/65/e61a65e7b63871eefdc208a138ccafc9.gif" height="50px">

# Operações matemáticas
A maioria das operações ocorrem como na maioria das linguagens.  
**Exemplos**:
```rb
  5+5 # 10 
  5-5 # 0
  5/5 # 1
  5*5 # 25
  5**3 # 125
  4%2 # 0
```

O ruby apresenta, assim como no JavaScript, uma função que disponibiliza diversas operações específicas. Um exêmplo disso é o método **sqrt**  
**Exemplo**:
```rb
  a = 5 ** 2
  Math.sqrt(a) # 5
```

# Variáveis
As variáveis são definidas de forma simples, sem ser necessário a definição do tipo da variável. Basta nomear e relacionar o valor.  
**Exemplo**:
```rb
  a = 1
  b = "Teste"
  puts b # "Teste"
```

## String
String é basicamente uma classe de variável que guarda um conjunto de caracteres, formando um texto.  
**Exemplo**:
```rb
texto = "Esse é um texto"
```

### Métodos
***
#### CAPITALIZE
O método capitalize é um método que pega o primeiro caractere e, se ele estiver em caixa baixa, transforma em caixa alta.  
**Exemplo**:
```rb
texto = "teste"
puts texto.capitalize # "Teste"
```

#### UPCASE
O método upcase retorna a string com todos os seus caracteres em caixa alta.  
**Exemplo**:
```rb
texto = "teste"
puts texto.upcase # "TESTE"
```

#### STRIP, LSTRIP E RSTRIP 
Esses métodos servem para retirar os espaços vazios que tem ao redor de uma String. Sendo o **lstrip** para remover os da esquerda, o **rstrip** os da direita e o **strip** para remover dos dois lados.  
_OBS: Essa remoção ocorre a partir do último, primeiro ou ambos dependendo de qual você usou._  
**Exemplo**:
```rb
texto = "        Esse é um texto exemplo         "
puts texto.lstrip # "Esse é um texto exemplo         "
puts texto.rstrip # "        Esse é um texto exemplo"
puts texto.strip  # "Esse é um texto exemplo"
```

#### DELETE_PREFIX E DELETE_SUFFIX
Esses métodos retornam a String sem o conteúdo, do início ou final, passado como argumento dependendo de qual você usar. Sendo delete_prefix para o início e delete_suffix para o final.  
```rb
texto = "Esse é um texto exemplo"
puts texto.delete_prefix("Esse") # " é um texto exemplo"
puts texto.delete_suffix("exemplo") # "Esse é um texto "
```

#### RJUST E LJUST
Esses métodos pegam uma String e fazem ela ter o tamanho desejado adicionando os caracteres que você passou. O **rjust** adiciona os caracteres na esquerda e o **ljust** adiciona os caracteres na direita.  
_OBS: Quando você não passa nenhum caractere como argumento ele adiciona caracteres vazios._  
**Exemplo**:
```rb
texto = "teste"
puts texto.rjust(10) # "     teste"
puts texto.ljust(10) # "teste     "
```

## Integer
O Integer é uma classe de variável que guarda um número inteiro.  
**Exemplo**:
```rb
numero_inteiro = 3
```

### Métodos
___
#### EVEN? E ODD?
Esses métodos são usados para identificar se um Integer é par ou ímpar. `even?` retorna **true** se o Integer for par e `odd?` retorna **true** se for ímpar.  
**Exemplo**:
```rb
puts 2.even? # true
puts 3.odd?  # true
```

## Array
Array é basicamente uma classe de variável que armazena uma lista ordenada.  
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
```

### Métodos
#### JOIN
O métpdo `join` retorna todos os ítens interceptados por o que você desejar.  
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]

puts lista.join(", ") # 1, 2, 3, 4, 5, 6
```

#### REJECT
O método `reject` retorna o array sem os elementos que satisfazem a condição definida no bloco.  
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.reject { |numero| numero > 3 }
# Retorna: [1, 2, 3]
```

#### INSPECT
O método `inspect` mostra a array de modo "puro" (forma legível e representativa).  
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
puts lista.inspect # [1, 2, 3, 4, 5, 6]
```

#### POP
O método `pop` retira o último item da array.  
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.pop
puts lista.inspect # [1, 2, 3, 4, 5]
```

#### PUSH
O método `push` coloca algo na posição final da array.
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.push(8)
puts lista.inspect # [1, 2, 3, 4, 5, 6, 8]
```

## Hash
Hash é basicamente um objeto como no JavaScript. Uma lista não ordenada, onde você acessa os valores por chave e não por índice.  
**Exemplo:**
```rb
pessoa = { nome: "Heitor", idade: 16, profissão: "Fullstack" }
```

### Métodos
#### ADICIONAR E ATUALIZAR VALORES
Para adicionar ou atualizar valores em um hash, basta usar a chave com o operador `=`.  
**Exemplo:**
```rb
pessoa[:cidade] = "Recife"
pessoa[:idade] = 17
```

#### EACH
O `each` em hashes usa dois parâmetros: a chave e o valor.  
**Exemplo**:
```rb
pessoa = { nome: "Heitor", cidade: "Recife" }
pessoa.each do |chave, valor|
  puts "#{chave}: #{valor}"
end
```


# Loops
Os loops são uma forma mais pratica de fazer uma mesma ação várias vezes.

## while
A sintaxe do **while** é bem simples. Basta colocar a condição no loop que o que está dentro dele irá acontecer enquanto a condição não for verdadeira.  
**Exemplo**:
```rb
  while [condição]
    [código]
  end
```
## for
No for é um pouco mais complicado. O primeiro argumento será a variável do loop, que muda de acordo com o funcionamento dele, e o segundo argumento é a condição limite do loop, que define onde ele começa e onde ele termina.  
**Exemplo**:
```rb
  for numero in 1..5 # Diz que a variavel numero ira transicionar de 1 a 5
    puts numero
  end
  # Recomendo que teste para entender melhor
```
## times
O times é lembra um pouco o for. Porém nele você coloca a variável do loop em cima e o que acontece com ela no própio código.  
**Exemplo**:
```rb
  3.times do |[variável]|
    puts "Número: #{[variável] [condição]}
  end
```
## each
O each é um método de array que passa por todos os itens dela e faz algo cada vez que passar. Como parâmetro você passa a variável, que será a correspondente ao ítem onde o loop se encontra no momento.  
**Exemplo**:
```rb
  lista = ["abc", "def", "ghi"]
  contagem = 0

  lista.each do |item| # Passa por todos os ítems de "lista" e ,para cada item, mostra o ítem onde o loop se encontra no momento e adiciona 1 ao contador
      puts item
      contagem += 1
  end

  puts contagem
```

# Métodos gerais
## empty?
O método empty indica se uma variável, de qualquer tipo, se econtra vazia.  
**Exemplo**:
Usando em uma array para verificar se ela está vazia.
```rb
array = []
puts array.empty? # true
```

### include?
Esse método indica se uma variável contém um conteúdo passado.  
**Exemplo**:  
Usando em uma Array de frutas para verificar se ela contém a fruta maçã.
```rb
frutas = ["banana", "uva", "pêra"]
puts frutas.include?("maçã") # false
```

### start_with? e end_with?
Esses métodos retornam se uma variável começa, ou acaba, com um conteúdo que você passou.  
**Exemplo**:
Usando para verificar se uma String começa com "Esse" e se termina com "exemoplo", passando isso como argumento.
```rb
texto = "Esse é um texto exemplo"
puts texto.start_with?("Esse") # true
puts texto.end_with?("exemplo") # true
```

## size ou length
Esses metódos retornam o tamanho de uma variável de acordo com como esse tamanho é definido. Usar em uma String retorna-ra a quantidade de caracteres, usar em uma Array retorna-ra a quantidade de ítems.  
_OBS: Os dois métodos fazem a mesma coisa._  
**Exemplo**:
Verificando o tamanho de uma String e de uma Array
```rb
texto = "Esse é um exemplo de texto"
puts texto.length # 26

array = [1, 2, 3, 4, 5, 6, 7]
puts array.size # 7
```

## index
O index é um método onde você passa um valor e ele retorna a posição dele na variável em questão.  
**Exemplo**:  
Usando para verificar onde se encontra a palavra "galera" em uma String.  
_OBS: Por estar passando uma palavra inteira como argumento ele retorna a posição da primeira letra._
```rb
teste = "Olá galera do canal"
puts teste.index("galera")
```

## to_s, to_i e to_f
No ruby temos um método para converter a classe de algo. Podemos converter uma variável para String, Integer e Float usando os métodos to_s,to_i e to_f.  
**Exemplos**:
Usando para transformar uma String em um Integer e um Float
```rb
  a = "1"
  a.to_i # Retorna a variável a em um Integer
  a.to_f # Retorna a variável a em um Float
```
