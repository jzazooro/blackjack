# blackjack

Mi direccion de GitHub para este repositorio es la siguiente: [GitHub](https://github.com/jzazooro/blackjack.git)
https://github.com/jzazooro/blackjack.git

Hemos programado una version basica de un juego similar al BlackJack
El diagrama de flujo que tenemos en nuestro codigo es el siguiente:

![diagrama de flujo BlackJack](https://github.com/jzazooro/blackjack/blob/main/DIAGRAMADEFLUJO.jpg)

```import random
from random import choice, sample
baraja={
    chr(0x1f0a1): 11,
    chr(0x1f0a2): 2,
    chr(0x1f0a3): 3,
    chr(0x1f0a4): 4,
    chr(0x1f0a5): 5,
    chr(0x1f0a6): 6,
    chr(0x1f0a7): 7,
    chr(0x1f0a8): 8,
    chr(0x1f0a9): 9,
    chr(0x1f0aa): 10,
    chr(0x1f0ab): 10,
    chr(0x1f0ad): 10,
    chr(0x1f0ae): 10,
}

print("cartas: {}".format(" ".join(baraja.keys())))
print("puntos: {}".format(list(baraja.values())))

carta1=11
carta2=2
carta3=3
carta4=4
carta5=5
carta6=6
carta7=7
carta8=8
carta9=9
carta10=10
carta11=10
carta12=10
carta13=10
cartas=[carta1, carta2, carta3, carta4, carta5, carta6, carta7, carta8, carta9, carta10, carta11, carta12, carta13]
a=random.randint(0,12)
b=random.randint(0,12)
c=random.randint(0,12)
d=random.randint(0,12)
puntuacionjugador=cartas[a]+cartas[b]
puntuacionbanca=cartas[c]+cartas[d]
if puntuacionjugador==puntuacionbanca:
    print("has obtenido", a+b, "puntos")
    print("la banca ha obtenido", c+d, "puntos")
    print("la partida ha acabado en empate")
if puntuacionjugador>puntuacionbanca:
    print("has obtenido", a+b, "puntos")
    print("la banca ha obtenido", c+d, "puntos")
    print("¡Enhorabuena has ganado la partida!")
if puntuacionjugador<puntuacionbanca:
    print("has obtenido", a+b, "puntos")
    print("la banca ha obtenido", c+d, "puntos")
    print("Lo siento, la banca te ha ganado")
