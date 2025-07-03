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

## Variáveis
As variáveis são definidas de forma simples, sem ser necessário a definição do tipo da variável. Basta nomear e relacionar o valor.
**Exemplo**:
```rb
  a = 1
  b = "Teste"
  puts b # "Teste"
```


# Array
Array é basicamente uma lista ordenada
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
```

## Métodos
### reject
O metodo reject retorna a array sem os componentes que condizem com a condição desejada. Basta nomear a variável transitora e definir a condição.
**Exemplo**:
```rb
  lista = [1, 2, 3, 4, 5, 6]

  lista.reject { |numero| numero > 3 } # Nomeia a variável transitora como numero e "rejeita" os numeros maiores que 3
```

### inspect
O método inspect mostra a array de modo "puro"
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.inspect # [1, 2, 3, 4, 5, 6]
```
### pop
O método pop retira o último ítem da array
**Exemplo**:
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.pop()
lista.inspect # [1, 2, 3, 4, 5]
```

# Hash
Hash é basicamente um objeto do JavaScript. Uma lista não ordenada, onde você requisita o valor pelo nome e não pelo índice.
**Exemplo:**
```rb
pessoa = { nome: "Heitor", idade: 16, profissão: "Fullstack" }
```

## Métodos
### Adicionar e atualizar valores
Para adicionar valores basta definir 

### each
O each no Hash é um pouco diferente. Nele você adicionará dois parâmetros ao invés de 1. O primeiro sendo a chave e o outro sendo o valor.
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

## Conversão de Classes
No ruby temos um método para converter a classe de algo. Podemos converter uma variável para String, Integer e Float usando os métodos to[classe]
**Exêmplos**:
```rb
  a = "1"
  a.to_i # Transforma a variável a em uma String
  a.to_f # Transforma a variável a em um Float
```
