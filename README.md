# S3L3-Python-Pierre-lobrillo
Scrivere un programma in python che calcola perimetro di figure.
Abbiamo creato un programma che calcola il perimetro di un quadrato, un rettangolo e la circonferenza di un cerchio.
Abbiamo individuato, le variabile base, altezza,  raggio, circonferenza, perimetro. e abbiamo elencato le condizioni.
1) I numeri inseriti devono esse reali positivi quindi "float".
2) Nel caso del quadrato, base deve essere uguale a altezza e raggio = 0;
3) Per rettangolo base e altezza devono essere diversi da zero e non uguale, con raggio = 0.
4) Per cerchio, base=altezza=0 e raggio superiore a 0.
5) Negli altri casi il programma legga error. 

import math

# Chiediamo all'utente di inserire base, altezza e raggio
base = float(input("Inserisci la base: "))
altezza = float(input("Inserisci l'altezza: "))
raggio = float(input("Inserisci il raggio: "))

# Verifichiamo base > 0, altezza > 0 e raggio > 0
if base < 0 or altezza < 0 or raggio < 0:
    print("Inserire solo valori positivi")
else:
    if base == altezza and raggio == 0:
        # Quadrato
        perimetro = base * 4
        print("Il perimetro del quadrato è:", perimetro)
    elif base != altezza and raggio == 0:
        # Rettangolo
        perimetro = base * 2 + altezza * 2
        print("Il perimetro del rettangolo è:", perimetro)
    elif base == altezza and raggio > 0:
        # Cerchio
        circonferenza = 2 * math.pi * raggio
        print("La circonferenza del cerchio è:", circonferenza)
    else:
        print("Errore nei valori inseriti.")
