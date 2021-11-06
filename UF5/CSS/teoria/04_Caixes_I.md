---
marp: true
title: Caixes I
paginate: true
---

# Caixes I

---

## Background

El **background** o fons d'un element HTML és el que apareix _darrere_ del text. Tot i que CSS permet aplicar un fons a qualsevol tipus d'element HTML, s'utilitza principalment en elements a nivell de bloc.

Els fons només s'apliquen a l'element objectiu. Però tenint en compte que **la majoria d'elements HTML tenen un fons transparent**, aplicar un fons al `body` semblarà que s'aplica a tots els elements.

---

## background-color

Valor per defecte: `transparent`.
Heretat pels fills: no.

Com ja hem tractat les diferents maneres de definir un color amb CSS, aplicar un color de fons és senzill:

```css
body{ background-color: #ff0000;}
```

Tot l'element s'omplirà amb un color de fons **vermell**. Tingueu en compte que heu de triar sempre un color de text adequat per mantenir el vostre contingut fàcil de llegir.

---

## background-image

Com que els colors llisos no solen ser suficients, CSS permet aplicar **imatges** com a fons per als elements.

L'aplicació d'una imatge de fons només requereix especificar la seva URL:

```css
body{ background-image: url(images/diagonal-pattern.png);}
```

El comportament de la imatge (com es repeteix, on es col·loca, com es mida) està definit per altres propietats de `background` que ara veurem.

Tingueu en compte que l'element HTML **no canviarà la mida** per adaptar-se a la imatge, ja que la imatge és purament decorativa.

---

## &lt;img&gt; o background-image?

L'element HTML `<img>` és per a imatges que formen part del **contingut**, mentre que les imatges de fons CSS són purament **decoratives**.

De vegades es complicat diferenciar entre contingut i estil. Algunes tècniques visuals són més fàcils d'aconseguir amb fons CSS. Pregunteu-vos si la imatge que utilitzeu és essencial per a la pàgina. Si és així, utilitzeu l'element `<img>`.

---

## Degradats

CSS també permet definir **degradats de color** com a imatges de fons, en 2 formes diferents:

* `linear-gradient` per a gradients en una sola direcció, en forma rectangular
* `radial-gradient` per a gradients en totes direccions, en forma circular

Els degradats de fons es consideren **imatges de fons**:

```css
body{ background-image: linear-gradient(white, grey);}
```

---

## background-position

Per defecte, una imatge de fons es repetirà indefinidament. Podeu especificar la seva **background-position**, escollint un valor `x` horitzontal i un valor `y` vertical.

Per a cada valor, podeu utilitzar:

* valors de píxels `px`
* percentatges, relatius a les dimensions de l'element HTML
* paraules clau com `center`, `left`, `bottom`...

```css
body{ background-position: right bottom;}
```

---

## background-repeat

Per defecte, una imatge de fons es repetirà indefinidament. Podeu triar que es repeteixi només horitzontalment, només verticalment o no.

```css
/* Només horitzontalment */
body{ background-repeat: repeat-x;} 
/* Només verticalment */
body{ background-repeat: repeat-y;}
/* La imatge de fons només apareixerà una vegada */
body{ background-repeat: no-repeat;} 
```

---

## Altres propietats de background

Hi ha altres [propietats de background](https://www.w3schools.com/cssref/css3_pr_background.asp) que podeu fer servir:

* [background-attachment](https://www.w3schools.com/cssref/pr_background-attachment.asp)
* [background-size](https://www.w3schools.com/cssref/css3_pr_background-size.asp)

---

