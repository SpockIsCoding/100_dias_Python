#### Data Types

> **String:** é uma variável do tipo texto que é declarada entre aspas ex. "Hello". É possível mostrar qual a posição de cada caractere usando uma lista

```python
#Iremos imprimir apenas o caractere na posição 1, lembrando que começa em 0
print ("hello"[1])
out: e

#Concatenar string. Mesmo se o interger estiver dentro das aspas ele será manipulado como texto. 
print ("amor"+"maior")
out: amormaior
print ("123"+"love")
out: 123love
print ("123"+"456")
out: 123456
```

>**Interger:** é uma variável do tipo inteiro, um número. 

```python
#para declarar um interger basta digitar
123

#soma 
print(1 + 3)
out: 4

#é comum usar o caractere de sublinhado (`_`) como um separador visual em números grandes para tornar mais fácil a leitura dos dígitos. O Interpretador ignora o sublinhado. 
123_456_789
```

> **Float:** é uma variável para se trabalhar com ponto decimal. Pontos Flutuantes são usados para representar números reais. 

```python
3.456
345.6
```

> **Boolean:** são usados para representar apenas dois estados True ou False

```python
True
False
```

> **Len:** len conta quantos caracteres tem em uma string, a questão é que len retorna um valor interger. Quando se tenta concatenar um len com uma string o interpretador apresenta um erro. 

```python
#código que irá apresentar o erro, por que concatenou string com interger
num_char = len(input("Qual é o seu nome ?"))
print("Seu nome tem" + num_char + "caracteres")

#para checar qual o tipo da variável
num_char = len(input("Qual é o seu nome ?"))
print(type(num_char))
out: Qual é o seu nome ? lima
<class 'int'>

#para contornar, basta converter a variável.
num_char = len(input("Qual é o seu nome ? "))
new_num_char = str(num_char)
print("Seu nome tem " + new_num_char + " caracteres")

#outro exemplo, esse usa uma lista para pegar o primeiro e o segundo caractere que foi informado na string e converter para int. 
two_digit_number = input()
num1 = int(two_digit_number[0])
num2 = int(two_digit_number[1])

print(num1 + num2)
```

> **Operações Matemáticas:*** dividir, somar, subtrair, multiplicar, potencializar. 

```python
3 + 5
7 - 4
3 * 2
6 / 3 #uma divisão resulta em um float
2 ** 3 #potencia, exponencial

#Não esquecer de seguir a ordem das operações, PEMDAS
Parênteses = ()
Exponentes = **
Multiplicação = *
Divisão = /
Adição = +
Subtração = -
```

> **IMC:** calculadora simples de IMC. IMC = peso / pela altura elevada ao quadrado

```python
#Entre com a altura ex. 1.74
height = input("Digite sua altura :")
#Entre com o peso em Kg ex. 87
weight = input("Digite o seu peso :")

#Equação
heightf = float(height)
weightf = int(weight)
height2 = (heightf ** 2)
bmi = round(weightf / height2) #A função round é para arredondar números em float,
#e o número depois da vírgula é a quantidade de casas decimais que se deseja após o ponto flutuante.
bmi = (weightf // height2)#Usando divisão dupla (//) tem um efeito similar ao do round, isso declara como interger a equação.
print (f"Seu IMC é igual a : {bmi}") #Observe que incluímos o f antes da sintaxe do print, 
#isso é para formatar uma string usando f-string, a variável fica entre chaves {}

#caso queira saber qual o tipo da variável
print(type(bmi))
out: <class 'float'>
```

>**Expectativa de vida:** calcule quantas semanas nos resta se vivêssemos até os 90 anos.

```python
#1 ano possui 52 semanas
age = input("Digite sua idade :")

life_expect = ((90 - int(age)) * 52) #converto a string age em int
print(f"You have {life_expect} weeks left") #uso f-string para exibir o resultado,
```

>**Gorjeta:** um calculador simples de gorjeta

```python
print("Seja bem-vindo ao Gorja calculator !!!")
conta = input("Qual o valor da conta ?: ")
gorjeta = input ("Quanto quer pagar de gorjeta 10,12,15% ?: ")
pessoas = input ("Quantas pessoas irão dividir a conta ?: ")

gorjeta_total = (float(gorjeta) / 100) #converte string em float  e divide por 100, para obter o percentual
parcial_conta = (gorjeta_total * float(conta) + float(conta)) #converte string em float e multiplica o percentual da gorjeta
#pelo total da conta para obter o valor da conta + o percentual
total_conta_dividida = (parcial_conta / float(pessoas)) #Divide o total da conta + gorjeta pela quantidade de pessoas a mesa

print(f"Cada pessoa deverá pagar R${total_conta_dividida} ")

#observe que não utilizados round ou // para arredondar pois estaríamos arredondado para o menor valor

#para arredondar para cima poderíamos usar o ceil
resultado = dividendo / divisor 
resultado_arredondado = ceil(resultado)

#uma forma mais limpa de se fazer seria o input já convertido:

print("Seja bem-vindo ao Gorja calculator !!!")
conta = float(input("Qual o valor da conta ?: "))
gorjeta = int(input ("Quanto quer pagar de gorjeta 10,12,15% ?: "))
pessoas = int(input ("Quantas pessoas irão dividir a conta ?: "))

gorjeta_total = gorjeta / 100 #obter o percentual
parcial_conta = (gorjeta_total * conta + conta) #multiplica o percentual da gorjeta
#pelo total da conta para obter o valor da conta + o percentual
total_conta_dividida = parcial_conta / pessoas #Divide o total da conta + gorjeta pela quantidade de pessoas a mesa

print(f"Cada pessoa deverá pagar R${total_conta_dividida} ")


```
