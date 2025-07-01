# Grimorio-Ruby
tudo oq eu sei de ruby

## Operações matemáticas
_A maioria das operações ocorrem como na maioria das linguagens._
Exêmplos:
```
  5+5 // 10 
  5-5 // 0
  5/5 // 1
  5*5 // 25
  5**3 // 125
  4%2 // 0
```

_O ruby apresenta, assim como no JavaScript, uma função que disponibiliza diversas operações específicas. Um exêmplo disso é o método **sqrt**_
```
  a = 5 ** 2
  Math.sqrt(a) // 5
```

## Variáveis
_As variáveis são definidas de forma simples, sem ser necessário a definição do tipo da variável. Basta nomear e relacionar o valor._
Exêmplo:
```
  a = 1
  b = "Teste"
  puts b // "Teste"
```

# Metodos Úteis

## Conversão de Classes
_No ruby temos um método para converter a classe de algo. Podemos converter uma variável para String, Integer e Float usando os métodos to_[classe]_
Exêmplos:
```
  a = "1"
  a.to_i // Transforma a variável a em uma String
  a.to_f // Transforma a variável a em um Float
```

### Nil
_Nil é um valor que representa o nada absoluto._
