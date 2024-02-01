

#### Troca (switch) de variáveis

> Para a troca de variáveis é preciso criar um nova variável provisória que receberá o valor que será posteriormente utilizado. Isso pq uma variável irá sobrescrever a outra. 

```python
#Q: Troque A por B, B por A
a=10
b=20
#Errado, quando A=B, o valor de A passa a não existir mais. Assim, Se B = A, os valores ficarão iguais.
a=b
b=a
#Certo, C recebe o valor de A, A recebe o Valor de B, e B recebe o valor de A que foi guardado em C
c=a
a=b
b=c

print("A: "+a)
print("B: "+b)
```

#### Espaçamento e quebra de linha

> Para dar um espaçamento ou coloca o espaço na string antes do final das aspas ou coloca uma string vazia
> Para quebra de linha basta colocar \n

```python
print("Jesus "+"te "+"ama\n")
print("E"+" "+"Eu"+" "+"também")
```

#### Input e Len

> Input é para entrada de dados, onde o sistema espera uma interação do usuário
> Len é para contar quantos caracteres tem uma variável. Len exibe um valor inteiro. 

```python
#Há uma forma simples porém pode ficar com uma linha enorme. 
print(len(input()))
#Há uma forma mais complexa declarando todas as variáveis. 
nome = input("digite seu nome :")
valor = len(nome)
print(valor)
```


