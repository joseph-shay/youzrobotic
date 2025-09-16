---
title: "2024 Iran WRO"
date: 2024-08-09
draft: false
summary: "Dvojni teniški turnir WRO RoboSports 2024"
description: "Odkrijte izkušnje Yousefa Shaykholeslama na WRO 2024 na otoku Kish, kjer je njegova ekipa osvojila bronasto medaljo v ligi RoboSports Double Tennis. Preberite o njihovi poti, izzivih in uspehu v enem izmed najbolj vznemirljivih tekmovanj v robotiki."
series: ["WRO"]
series_order: 2
---

## Uvod
Danes sem tekmoval na WRO Iran 2024 na *Kish Island* v ligi RoboSports Double Tennis. Dosegli smo *tretje mesto* in osvojili *bronasto medaljo*.

## Scenarij
**Double-Tennis**:  
Vsaka tekma izziva vključuje dva študentska tima. Vsak tim pripravi dva robota. Oba robota delujeta na isti polovici igrišča, njun cilj pa je sodelovati pri skupnem nalogi – premakniti vse oranžne žoge iz svoje polovice na nasprotno polovico.

{{< figure
    src="field.png"
    alt="rbmsrf"
    caption="RoboSport Double-Tennis igrišče"
    >}}

## Naš robot
### Tehnične lastnosti  
Naš robot je uporabljal **Arduino Leonardo** kot procesor, štiri običajne rumene DC motorje za gibanje, dva DC motorja za udarce ter **UnitV AI kamero** za zaznavanje žoge.

<img class="thumbnailshadow" src="unitv.png">

### Oblikovanje  
Oblikovanje PCB je bilo narejeno v **ALtium Designer**, CAD pa v **SolidWorks**. IDE, ki smo ga uporabili, je bil **Arduino IDE**.

{{< figure
    src="robotd.png"
    alt="ROBOTSOLID"
    caption="Mehanski pogled robota v SolidWorks"
    >}}

### Oblikovanje udarca  
Udarni mehanizem je narejen kot katapulta, ki uporablja vrtilno silo za dviganje žoge in njeno metanje naprej.

### Algoritem  
Ko se je robot zagnal, je izvedel skeniranje za določitev položaja *ljubičaste žoge*. Na podlagi položaja je bil izveden sklop ukazov za premikanje *oranžne žoge* z naše strani, ob tem pa smo ohranili *ljubičasto žogo*. Po tem je robot prešel v *način kamere*, kjer je kamera ustvarila **(X,Y)** koordinatno ravnino. Na podlagi položaja *oranžne žoge* so bili sprejeti naslednji ukazi:

```C
if (orange_y_coord > 50) {
    LEFT(90);
  } else if (orange_y_coord < -50) {
    RIGHT(90);
  } else if (orange_y_coord >= -50 && orange_y_coord <= 50 && orange_y_coord !=0) {
    FORWARDKICK();
  }
  
```

## Galerija

### En primer algoritma
![Algo](algo.gif)


### Fotografije
{{< gallery >}}
  <img src="upme.jpg" class="grid-w33" />
  <img src="memedal.jpg" class="grid-w33" />
  <img src="gp.jpg" class="grid-w33" />
  <img src="post.jpg" class="grid-w33" />
  <img src="meupag.jpg"  class="grid-w33" />
  <img src="sideme.jpg" class="grid-w33" />
  <img src="frontme.jpg" class="grid-w33" />
{{< /gallery >}}
