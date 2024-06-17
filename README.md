# Teorema-de-pitagoras
#Quando comecei a estudar programação (à uma semana) e aprendi os símbolos de operados me propus a fazer um programa que usasse o teorema de pitagoras para calcular qualquer um dos lados (O que ferrou ja que tive que ir atrás de como calcular raiz quadrada). 
#Ele poderia dizer o valor de qualquer lado, desde que você desse os outros dois valores.
#hoje aprendi a usar os import, e to feliz em reescrever o programa

#fórmula pra calcular hipotenusa h**2 = c1**2 + c2**2
#h**2 = 3**2 + 4**2 -> h**2 = 16+9 -> h**2 = 25 -> h = /-25 #calcular cateto 5**2 = c1 + 4**2 -> 25 - 16 = c1**2 -> 9 = c**2 -> 3 = c1

print('(Digite 0 para o valor que você quer descobrir)')
c1 = float(input('Valor do cateto oposto: '))
c2 = float(input('Valor do cateto adjacente: '))
h = float(input('Valor da hipotenusa: '))

c1_quadrado = c1**2
c2_quadrado = c2**2
h_quadrado = h**2
import math

#Variavel do calculo da hipotenusa
soma_cateto = c2_quadrado + c1_quadrado
raiz_quadrada_catetos = math.sqrt(soma_cateto)
if h == 0:
    print(f'Valor da hipotenusa é: {raiz_quadrada_catetos}')

#variaveis do calculo do cateto oposto
sub_hipo_c2 = h_quadrado - c2_quadrado
raiz_hipo_c2 = math.sqrt(sub_hipo_c2)
if c1 == 0:
    print(f'O valor do cateto oposto é: {raiz_hipo_c2}')

#Variavel do calculo do cateto adjacente
sub_hipo_c1 = h_quadrado - c1_quadrado
raiz_hipo_c1 = math.sqrt(sub_hipo_c1)
if c2 == 0:
    print(f'O valor do cateto adjacente é: {raiz_hipo_c1}')

#Esse tem um problema. Ele da um erro que ainda não entendi como resolve quando me resposnde o valor da hipotenusa
