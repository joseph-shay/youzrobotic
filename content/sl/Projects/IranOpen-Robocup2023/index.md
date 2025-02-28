---
title: "2023 IranOpen RoboCup"
date: 2023-04-25
draft: false
summary: "Tekmovanje 2023 IranOpen RoboCup"
description: "Raziskujte izkušnjo Yousefa Shaykholeslama na RoboCup 2023, kjer se robotika in umetna inteligenca združita za reševanje resničnih problemov. Pridobite vpogled v sodelovanje njegove ekipe, izzive in nepozabne trenutke iz enega najbolj vodilnih tekmovanj v robotiki na svetu."
series: ["RoboCup"]
series_order: 1
---

## Uvod
Leta 2023 sem se udeležil tekmovanja IranOpen 2023 RoboCup v *Teheranu* v ligi RCJ Lightweight Soccer z mojo ekipo **After X**. Dosegli smo **prvo mesto** in predstavljali Iran na tekmovanju v Bordeauxu.

---

## Naš robot
Imeli smo dva robota z enako mehansko in električno zasnovo, vendar z različnimi programi (eden kot vratar in drugi kot napadalec).
<img class="thumbnailshadow" src="featured.jpg">

---

## Tehnične lastnosti

### Mikro
Mozg robota je **STM32F405RGT6**, ki ima *168 MHz*!!!

### Motorji
Naši roboti so uporabljali **Maxon DCX16L**, ki je zelo občutljiv in lahko doseže hitrosti do 1000RPM pri 9V napetosti.
<img class="thumbnailshadow" src="MaxonDCX16L.jpg">

### Pogonski gonilniki
Za pogon **Maxon DCX16L** smo uporabili **TB12FNG** gonilnike za vsak motor (skupaj 4).

### Premikanje
Premikanje robota je bilo omogočeno s pomočjo **4-kolesnega OmniDirectional premikanja**, ki omogoča robotu, da se premika v **vsako** smer.
<img class="thumbnailshadow" src="omniwheel.jpg">

### Prepoznavanje žoge
Iskanje žoge na igrišču, ki je IR oddajna žoga, smo izvedli s pomočjo **TSSP senzorjev** v krožni postavitvi.

### Prepoznavanje izhoda
Če je robot zapustil rob igrišča (bela črta okoli igrišča), je to pomenilo napako, zato smo namestili krožno postavitev **NJL senzorjev** za zaznavanje bele črte.

### Prepoznavanje gola
Napadalni robot je imel eno **OpenMV Cam H7** kamero in je zaznal gol, da je, ko je žoga bila v "ustih" robota, ta odšel proti golu.

---

## Galerija
{{< button href="https://fazilirc.ir/news/afterx/" target="https://fazilirc.ir/news/afterx/" >}}
fazili raziskovalni center
{{< /button >}}
---

### Eden od naših tekem
{{< youtube 6Dq_Vl1imRc >}}

### Fotografije

{{< gallery >}}
  <img src="arivie.jpg" class="grid-w33" />
  <img src="photo.jpg" class="grid-w33" />
  <img src="photoarive.jpg" class="grid-w33" />
  <img src="robot.jpg" class="grid-w33" />
  <img src="tdp.jpg" class="grid-w33" />
  <img src="trophy.jpg" class="grid-w33" />
{{< /gallery >}}
