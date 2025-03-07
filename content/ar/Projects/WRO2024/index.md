---
title: "2024 WRO إيران"
date: 2024-08-09
draft: false
summary: "دوري روبوسبورتس تنس مزدوج 2024"
description: "اكتشف تجربة يوسف شيخلسلام في WRO 2024 في جزيرة كيش، حيث فاز فريقه بالميدالية البرونزية في دوري RoboSports Double Tennis. اقرأ عن رحلتهم وتحدياتهم ونجاحهم في أحد أكثر مسابقات الروبوتات إثارة."
series: ["WRO"]
series_order: 2
---

## المقدمة
اليوم، شاركت في WRO إيران 2024 في *جزيرة كيش* في دوري روبوسبورتس تنس مزدوج. حققنا *المركز الثالث* ونلنا *الميدالية البرونزية*.

## السيناريو
**تنس مزدوج**:  
تتضمن كل مباراة من التحدي فريقين من الطلاب. كل فريق يحضر روبوتين. يعمل كلا الروبوتين على نفس نصف الملعب، وهدفهم هو التعاون في مهمة مشتركة – دفع جميع الكرات البرتقالية من نصفهم إلى نصف الفريق الآخر.

{{< figure
    src="field.png"
    alt="rbmsrf"
    caption="ملعب روبوسبورت تنس مزدوج"
    >}}

## روبوتنا
### المواصفات  
استخدم روبوتنا **Arduino Leonardo** كمعالج، وأربعة محركات DC صفراء عادية للحركة، ومحركين DC للمُرسل، و **كاميرا AI من UnitV** لاكتشاف الكرات.

<img class="thumbnailshadow" src="unitv.png">

### التصميم  
تم تصميم PCB باستخدام **ALtium Designer**، و *CAD* تم باستخدام **SolidWorks**. تم استخدام *IDE* الخاص بـ **Arduino IDE**.

{{< figure
    src="robotd.png"
    alt="ROBOTSOLID"
    caption="عرض ميكانيكي للروبوت في SolidWorks"
    >}}

### تصميم المُرسل  
تم تصميم المُرسل بشكل يشبه المقلاع، باستخدام القوة الدورانية لرفع الكرة ورميها للأمام.

### الخوارزمية  
عندما يبدأ الروبوت، يقوم بعمل مسح لتحديد موقع *الكرة الأرجوانية*. بناءً على الموقع، يتم تنفيذ مجموعة من التعليمات لدفع *الكرة البرتقالية* من جانبنا مع الحفاظ على *الكرة الأرجوانية*. بعد ذلك، ينتقل الروبوت إلى *وضع الكاميرا*، حيث تقوم الكاميرا بإنشاء **خطة (X,Y)**. بناءً على موقع *الكرة البرتقالية*، يتم اتخاذ الإجراءات التالية:

```C
if (orange_y_coord > 50) {
    LEFT(90);
  } else if (orange_y_coord < -50) {
    RIGHT(90);
  } else if (orange_y_coord >= -50 && orange_y_coord <= 50 && orange_y_coord !=0) {
    FORWARDKICK();
  }
```


## المعرض

### مثال على الخوارزمية
![Algo](algo.gif)


### الصور
{{< gallery >}}
  <img src="upme.jpg" class="grid-w33" />
  <img src="memedal.jpg" class="grid-w33" />
  <img src="gp.jpg" class="grid-w33" />
  <img src="post.jpg" class="grid-w33" />
  <img src="meupag.jpg"  class="grid-w33" />
  <img src="sideme.jpg" class="grid-w33" />
  <img src="frontme.jpg" class="grid-w33" />
{{< /gallery >}}
