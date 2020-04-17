import random
from tkinter import *
walList1 = [] # Список рандом-чисел
walList2 = []
win = 0
loss = 0
money = 0
n1 = 0
n2 = 0


print('Ведите тип игры: (4)-20, (5)-36, (6)-45, (7)-49')
Type = int(input())

if Type == 4:
  type1 = 4
  type2 = 20
elif Type == 5:
  type1 = 5
  type2 = 36
elif Type == 6:
  type1 = 6
  type2 = 45
elif Type == 7:
  type1 = 7
  type2 = 49
else:
  print('Ввод неверный. Пример ввода: (7)-49 = Ввод - 7')
stol = [] # Список введены чисел

kollichestvo = int(input('Введи колличество игр:'))

if Type == 6 or Type == 7: # 7 из 49 и 6 из 45 ВВОД
  for y in range(type1):
    pole1 = int(input())
    stol1.append(pole1)
elif Type == 5:        # 5 из 36 ВВОД
  for y in range(type1):
    pole1 = int(input())
    stol1.append(pole1)
  for x in range(1):
  
    pole2 = int(input())
    slot2.append(pole2)
elif Type == 4:        # 4 из 20 ВВОД 
  for y in range (4):
    pole1 = int(input())
    stol1.append(pole1)
  for x in range(4):
    pole2 = int(input())
    stol2.append(pole2)

''' stol1 - Первое поле
    stol2 - Второе поле
'''
    
if Type == 6 or Type == 7:
  for u in range (kollichestvo):
    while len(walList1) < type1: 
      wal1 = random.randint(1, type2)
      if walList1.count(wal1) >= 1:
        walList1.remove(wal1)
      else:
        walList1.append(wal1)
        for i in range(type1):  
          if stol[i] in walList1:
            n1 += 1
elif Type == 5:
  for u in range (kollichestvo):
    while len(walList1) < 5:
      wal1 = random.randint(1, type2)
      if walList1.count(wal1):
        walList1.remove(wal1)
      else:
        walList1.append(wal1)
        for i in range(type1):
          if slot1[i] in walList1:
            n1 += 1
    wal2 = random.randint(1, 4)
    if wal2 == slot2:
      n2 += 1
