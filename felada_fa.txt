import random

wr=open('H:\fa.txt','w')
fakitermelesnap=[]

nap=1
while nap !=32:
    fatermeles=random.randint(50,100)
    fakitermelesnap.append(fatermeles)
    nap+=1
print(fakitermelesnap)
wr.write(f'{fakitermelesnap}\n')

Legnagyobb=fakitermelesnap[0]
Legkisebb=fakitermelesnap[0]
számláló=0
for x in fakitermelesnap:
    if x > Legnagyobb:
        Legnagyobb =x
    elif x < Legkisebb:
        Legkisebb = x  
    if x > 82:
        számláló +=1
        
print(f"Ez volt a legnagyobb fa kitermelés októberben: {Legnagyobb}.")
print(f'Ez volt a legkisebb fa kitermelés októberben: {Legkisebb}.')
print(f"Ennyiszer volt a fa kitermelés nagyobb min 82 m3: {számláló}.")
wr.write(f'Ez volt a legnagyobb fa kitermelés októberben: {Legnagyobb}.\n')
wr.write(f'Ez volt a legkisebb fa kitermelés októberben: {Legkisebb}.\n')
wr.write(f"Ennyiszer volt a fa kitermelés nagyobb min 82 m3: {számláló}.\n")

count = 0
for num in fakitermelesnap:
    count = count + 1

n = len(fakitermelesnap)
ker = fakitermelesnap[19]

i = 0
while i < n and fakitermelesnap[i] != ker:
    i = i + 1
if(i < n):
    print(f"Október 20-án ennyi volt a fa kitermelés: {ker}.")
    wr.write(f"Október 20-án ennyi volt a fa kitermelés: {ker}.\n")

napok=len(fakitermelesnap)

összeg = 0
for num in fakitermelesnap:
    összeg = összeg + num

print(f'Október átlag fa kitermelése: {összeg/napok:2.0f}.')
wr.write(f'Október átlag fa kitermelése: {összeg/napok:2.0f}.\n')