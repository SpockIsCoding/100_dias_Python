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
