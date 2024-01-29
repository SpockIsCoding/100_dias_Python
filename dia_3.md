## Dia 3

#### Odd or Even

> **Odd or Even ?:** ímpar ou par ?. É uma continha simples onde verifica-se se um número pode ser dividido por 2 sem restar nada além de 0. Isto é, um número par (even). Se a conta resultar em algo diferente de 0 é um número ímpar (odd).
> Para obtermos isso basta pegar o número e % 2, assim o Python já retorna com o valor 0 ou não. O módulo (%) é usado para obter-se o resto de uma divisão de um número por outro.  

```python
#uma forma mais detalhada. 
numero = int (input())

resto = numero % 2

if numero == 0:
    print ("é um número par.")
else:
    print ("é um número impar.")

#um forma mais simples.
numero = int(input())

if numero % 2 == 0:
    print("é um número par.")
else:
    print("é um número ímpar.")
```

#### If/Elif/Else

> **Nested if/else:** um if dentro de outro if, uma condição dentro de outra condição. se tiver + que 1.20cm, se for maior de 18, faça isso, se não faça isso. 


![](20240128212139.png)

```python
print("Bem vindo ao caminho dos esquecidos!!!")
print("Prepare-se para uma viagem inesquecível.")
altura = int(input("Qual a sua altura em Cm ?"))

if altura >= 120:
    print("Você pode seguir o caminho.")
    idade = int(input("Qual a sua idade ?"))
    if idade >= 18: #este é "Nested" porque está dentro de uma condição. 
        print("Pagar R$10.")
    else:
        print("Pagar R$5.")
else:
    print("Desculpe, você não pode seguir o caminho.")
```

**Nested if/elif/else:** um elif dentro de um if, uma condição dentro de outra condição. se tiver + que 1.20cm, se for maior de 18 cobre r$12, se for menor que 12 cobre r$5, se for entre 12 e 18 cobre r$7. 
Posso usar vários elif dentro de um if. 

![](20240128213632.png)

```python
print("Bem vindo ao caminho dos esquecidos!!!")
print("Prepare-se para uma viagem inesquecível.")
altura = int(input("Qual a sua altura em Cm ?"))

if altura >= 120:
    print("Você pode seguir o caminho.")
    idade = int(input("Qual a sua idade ?"))
    if idade >= 18: #este é "Nested" porque está dentro de uma condição. 
        print("Pagar R$12.")
    elif idade <=12:
        print("Pagar R$5.")
    else:
	    print("Pagar R$7.")
else:
    print("Desculpe, você não pode seguir o caminho.")

```

>**IMC 2.0:** Nossa calculadora de IMC (índice de massa corporal) melhorada, com uma codificação mais robusta. 

```python
#Entre com a altura ex. 1.74
height = input("Digite sua altura :")
#Entre com o peso em Kg ex. 87
weight = input("Digite o seu peso :")

#Equação
heightf = float(height)
weightf = int(weight)
height2 = (heightf ** 2)

imc = (weightf // height2)#Usando divisão dupla (//) tem um efeito similar ao do round, isso declara como interger a equação.

if imc < 18.5:
    print(f"Você está magricelo, seu IMC é {imc}, alimente-se!")
elif imc >= 18.5 and imc < 25:
    print(f"Você está no shape, seu IMC é {imc}!")
elif imc >= 25 and imc < 30:
    print(f"Você está mei gordin, seu IMC é {imc}.")
elif imc >=30 and imc < 35:
    print(f"Você está obeso, seu IMC é {imc}.")
elif imc >= 35:
    print(f"Você está morrendo, seu IMC é {imc}")

### uma forma mais enxuta seria

if imc < 18.5: 
	print("Você está abaixo do peso, alimente-se!") 
elif 18.5 <= imc < 25: 
	print("Você está no shape!") 
elif 25 <= imc < 30: 
	print("Você está mei gordin.") 
elif 30 <= imc < 35: 
	print("Você está obeso.") 
elif imc >= 35: 
	print("Você está morrendo")
```

**Obs:** o código será lido de cima para baixo, assim nosso código poderia ser conforme abaixo.

```python
#Entre com a altura ex. 1.74
height = input("Digite sua altura :")
#Entre com o peso em Kg ex. 87
weight = input("Digite o seu peso :")

#Equação
heightf = float(height)
weightf = int(weight)
height2 = (heightf ** 2)

imc = (weightf // height2)#Usando divisão dupla (//) tem um efeito similar ao do round, isso declara como interger a equação.
print (imc)
if imc < 18.5:
    print(f"Você está magricelo, seu IMC é {imc}, alimente-se!")
elif imc < 25:
    print(f"Você está no shape, seu IMC é {imc}!")
elif imc < 30:
    print(f"Você está mei gordin, seu IMC é {imc}.")
elif imc < 35:
    print(f"Você está obeso, seu IMC é {imc}.")
else:
    print(f"Você está morrendo, seu IMC é {imc}")
```

**Ano bissexto (leap year):** Um ano bissexto ocorre a cada quatro anos para corrigir a discrepância entre o ano solar e o calendário anual.
> 
> Assim é como você determina se um ano específico é um ano bissexto.
- em cada ano que é divisível por 4 sem resto
- exceto em cada ano que é uniformemente divisível por 100 sem resto
- a menos que o ano também seja divisível por 400 sem resto

![](20240128224221.png)


```python
print("Vamos verificar se o ano é bissexto.")
ano = int(input("Digite o ano:"))

if ano % 4 == 0:
    if ano % 100 == 0:
        if ano % 400 == 0:
            print("É um ano bissexto")
        else:
            print("Não é um ano bissexto")
    else:
        print("É um ano bissexto")
else:
    print("Não é um ano bissexto")
```

#### If/Else, múltiplas condições

>Na imagem a seguir temos if e elif (esquerda) onde se 1(uma) das condições for verdadeira já atinge o objetivo e para a execução do código. À direta temos Multiple if que vai checando se uma condição for verdadeira, e, se for, segue para verificar a próxima condição. 

![](20240129185156.png)

![](20240129185843.png)
