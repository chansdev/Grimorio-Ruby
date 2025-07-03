# Grimorio-Ruby
tudo oq eu sei de ruby

## Operações matemáticas
_A maioria das operações ocorrem como na maioria das linguagens._
Exemplos:
```rb
  5+5 # 10 
  5-5 # 0
  5/5 # 1
  5*5 # 25
  5**3 # 125
  4%2 # 0
```

_O ruby apresenta, assim como no JavaScript, uma função que disponibiliza diversas operações específicas. Um exêmplo disso é o método **sqrt**_
```rb
  a = 5 ** 2
  Math.sqrt(a) # 5
```

## Variáveis
_As variáveis são definidas de forma simples, sem ser necessário a definição do tipo da variável. Basta nomear e relacionar o valor._
Exemplo:
```rb
  a = 1
  b = "Teste"
  puts b # "Teste"
```

## Loops
### while
_A sintaxe do **while** é bem simples. Basta colocar a condição no loop que o que está dentro dele irá acontecer enquanto a condição não for verdadeira._
Exemplo:
```rb
  while [condição]
    [código]
  end
```
### for
_No for é um pouco mais complicado. O primeiro argumento será a variável do loop, que muda de acordo com o funcionamento dele, e o segundo argumento é a condição limite do loop, que define onde ele começa e onde ele termina._
```rb
  for numero in 1..5 # Diz que a variavel numero ira transicionar de 1 a 5
    puts numero
  end
  # Recomendo que teste para entender melhor
```
### times
_O times é lembra um pouco o for. Porém nele você coloca a variável do loop em cima e o que acontece com ela no própio código._
Exemplo:
```rb
  3.times do |[variável]|
    puts "Número: #{[variável] [condição]}
  end
```
### each
_O each é um método de array que passa por todos os itens dela e faz algo cada vez que passar. Como parâmetro você passa a variável, que será a correspondente ao ítem onde o loop se encontra no momento._
Exemplo:
```rb
  lista = ["abc", "def", "ghi"]
  contagem = 0

  lista.each do |item| # Passa por todos os ítems de "lista" e ,para cada item, mostra o ítem onde o loop se encontra no momento e adiciona 1 ao contador
      puts item
      contagem += 1
  end

  puts contagem
```

# Métodos
## Array
### reject
_O metodo reject retorna a array sem os componentes que condizem com a condição desejada. Basta nomear a variável transitora e definir a condição._
Exemplo:
```rb
  lista = [1, 2, 3, 4, 5, 6]

  lista.reject { |numero| numero > 3 } # Nomeia a variável transitora como numero e "rejeita" os numeros maiores que 3
```

### inspect
_O método inspect mostra a array de modo "puro"_
Exemplo:
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.inspect # [1, 2, 3, 4, 5, 6]
```
### pop
_O método pop retira o último ítem da array_
```rb
lista = [1, 2, 3, 4, 5, 6]
lista.pop()
lista.inspect # [1, 2, 3, 4, 5]
```

# Métodos gerais

## Conversão de Classes
_No ruby temos um método para converter a classe de algo. Podemos converter uma variável para String, Integer e Float usando os métodos to_[classe]_
Exêmplos:
```rb
  a = "1"
  a.to_i # Transforma a variável a em uma String
  a.to_f # Transforma a variável a em um Float
```
