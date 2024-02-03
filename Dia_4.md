
> [!NOTE] Pedra, Papel, Tesoura, Lagarto, Spock!!
> Iremos desenvolver esse jogo contagiante!!
>


![](img/20240201182549.png)

```python
import random

pedra = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

papel = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

tesoura = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

game_images = [pedra, papel, tesoura]

print("Pedra, Papel, Tesoura, Lagarto, Spock!!!!\n")

user_choice = int(input("O que você escolhe? Digite 0 para pedra, 1 para Papel ou 2 para Tesoura.\n"))

if user_choice >= 3 or user_choice < 0: 
  print("Você digitou um número inválido, você perdeu!\n")
else:
  print(game_images[user_choice])

  computer_choice = random.randint(0, 2)
  print("Escolha da Interligência Artificial:")
  print(game_images[computer_choice])
  if user_choice == 0 and computer_choice == 2:
    print("Você ganhou!\n")
  elif computer_choice == 0 and user_choice == 2:
    print("Você perdeu\n")
  elif computer_choice > user_choice:
    print("Você perdeu\n")
  elif user_choice > computer_choice:
    print("Você ganhou!\n")
  elif computer_choice == user_choice:
    print("É uma armadilha!!, deu empate\n")
print("Vida longa e próspera!!")
        
```

#### Modules

>[!NOTE] Modules
>um módulo é um arquivo contendo definições e instruções Python. Essas definições e instruções podem incluir funções, classes e variáveis que você pode reutilizar em outros programas ou scripts Python. A ideia é organizar o código em módulos para tornar o código mais modular, fácil de entender, e para promover a reutilização de código.

![](img/20240201193548.png)


#### Random

>[!NOTE] Módulo Random
>O módulo `random` em Python fornece funcionalidades relacionadas à geração de números aleatórios. Ele inclui várias funções que permitem criar sequências ou escolher elementos aleatórios.

```python
import random

#Ex.1
numero_aleatorio = random.random() 
print(numero_aleatorio)

#Ex.2
import random 

numero_aleatorio = random.randint(1, 10) 
print(numero_aleatorio)
```

>[!NOTE]Cara ou Coroa?(Head or Tail)
>Jogo de cara ou coroa usando o modulo random.

```python
# Jogo de cara ou coroa usando o módulo random  
import random  
  
print("Quem escolhe o restaurante ?\n")  
print("Vamos tirar no Cara ou Coroa\n")  
  
moeda = random.randint(0, 1)  
  
usuario_escolhe = int(input("Cara ou Coroa ? 0 = Cara, 1 = Coroa\n"))  
  
if usuario_escolhe != 0 and usuario_escolhe != 1:  
    print("Você digitou um valor errado, você perdeu.")  
else:  
    if moeda == 0:  
        moedastr = "Cara"  
    elif moeda == 1:  
        moedastr = "Coroa"  
  
    if usuario_escolhe == moeda:  
        print(f"Você ganhou, deu: {moedastr}")  
    else:  
        print(f"Você perdeu, deu: {moedastr}")
```

```python
#Aqui seria sem nenhuma interação do usuário

import random

moeda = random.randint(0,1)

if moeda == 1:
  moedastr = "Cara"
  print(f"{moedastr}")
else:
  moedastr = "Coroa"
  print(f"{moedastr}")

```

```python
### Mais simples ainda


import random

moeda = random.randint(0,1)

if moeda == 1:
  print("Cara")"
else:
  print("Coroa")
```