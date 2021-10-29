## Lab-1.4

# Begin30◦ . Дано значение угла α в радианах (0 < α < 2·π). Определить значениеэтого же угла в градусах, учитывая, что 180◦ = π радианов. В качествезначения π использовать 3.14

import random

import math

radian = random.uniform(0, 2*math.pi)

#radian = math.pi/2

degree = radian * 180 / math.pi

print("Radians = ",radian)

print("Degree = ",degree)

# Integer20◦. С начала суток прошло N секунд (N — целое). Найти количествополных часов, прошедших с начала суток.

import random

N = random.randrange(0,86400)

print("Число секунд: ", N)

h = int(N/60/60)

print("Целые часы: ", h)


# Boolean30◦. Даны целые числа a, b, c, являющиеся сторонами некоторого треугольника. Проверить истинность высказывания: «Треугольник со сторонами a, b, c является равносторонним»

import random

def TriangleInequality(A,B,C):

    return (A < B+C) and (B < A+C) and (C < A+B)
    
a,b,c = [random.randrange(1, 6) for i in range(0,3)]

while not TriangleInequality(a,b,c):

    a,b,c = [random.randrange(1, 6) for i in range(0,3)]
    
print("Длина a: ", a)

print("Длина b: ", b)

print("Длина c: ", c)

bool_expr = (a == b and a == c)

print("Треугольник является равносторонним: ",bool_expr)


# If20. На числовой оси расположены три точки: A, B, C. Определить, какая издвух последних точек (B или C) расположена ближе к A, и вывести этуточку и ее расстояние от точки A.

import random

A,B,C = random.sample(range(-10, 10), 3)

print("Число A:", A)

print("Число B:", B)

print("Число C:", C)

AB = abs(A-B)

AC = abs(A-C)

print("Расстояние от A до B:",AB)

print("Расстояние от A до C:",AC)

if AB < AC:

    print("В ближе к A")
    
elif AB > AC:

    print("C ближе к A")
    
else:

    print("B и C равноудалены от A")
    
# Case10. Робот может перемещаться в четырех направлениях («С» — север,«З» — запад, «Ю» — юг, «В» — восток) и принимать три цифровые команды: 0 — продолжать движение, 1 — поворот налево, −1 — поворотнаправо. Дан символ C — исходное направление робота и целое число N— посланная ему команда. Вывести направление робота после выполнения полученной команды.

import random

M = random.randrange(1,13)

#M=12

d = {'С' : 'Север', 'З' : 'Запад', 'Ю' : 'Юг', 'B' : 'Восток'}

r = {-1 : "поворот направо", 0 : "продолжать движение", 1 : "поворот налево"}

d1 = {0 : 'С', 1: 'З',  2 : 'Ю', 3 : 'B'}

try:

    i = random.randrange(0,4)
    
    #print("i : ", i)
    
    #print("d1 : ", d1[i])
    
    #print("d : ", d[d1[i]])
    
    C = d[d1[i]]
    
    print("Исходное направление (C) : ", C)
    
    N = random.randrange(-1,2)
    
    print("Команда (N) : ", N)
    
    print("Поворот: ", r[N])
    
    if N == -1:
    
        print("Part -1")
        
        if i == 0:
        
            i = 3
            
            #print("Part ", d[d1[i]])
            
        elif i == 3:
        
            i = 2
            
            #print("Part ", d[d1[i]])
            
        elif i == 2:
        
            i = 1
            
            #print("Part ", d[d1[i]])
            
        elif i == 1:
        
            i == 0
            
            #print("Part ", d[d1[i]])
            
    elif N == 1:
    
        #print("Part -1")
        
        if i == 0:
        
            i = 1
            
        elif i == 1:
        
            i = 2
            
        elif i == 2:
        
            i = 3
            
        elif i == 3:
        
            d1 = 0
            
    C = d[d1[i]]
    
    print("Новое направление (C) : ", C)
    
except KeyError as e:

    print('Ошибка')
    
# For10. Дано целое число N (> 0). Найти сумму1 + 1/2 + 1/3 + . . . + 1/N(вещественное число).

import random
    
N = random.randrange(10)

print('N = ', N)

S = 0.0

for i in range(N):

    S += 1/(i+1)
    
    print(i+1," : ",1/(i+1)," : ",S)
    
print("Sum = ",S)

# For20◦. Дано целое число N (> 0). Используя один цикл, найти сумму1! + 2! + 3! + . . . + N!(выражение N! — N–факториал — обозначает произведение всех целыхчисел от 1 до N: N! = 1·2·. . .·N). Чтобы избежать целочисленного переполнения, проводить вычисления с помощью вещественных переменныхи вывести результат как вещественное число.
	
  import random
  
N = random.randrange(1,10)

print('N = ', N)

F = 1.0

S = 0.0

for i in range(1,N+1):

    F *= i
    
    S += F
    
    print(i," : ", F," : ", S)
    
print("Result:",S)
