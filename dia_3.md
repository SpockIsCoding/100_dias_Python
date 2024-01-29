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
