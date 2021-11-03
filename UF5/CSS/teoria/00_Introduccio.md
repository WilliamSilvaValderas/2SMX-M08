---
marp: true
title: Introducció al CSS
paginate: true
---

# Introducció al CSS

---

## Introducció

Mentre que l'HTML consisteix a definir el contingut d'una pàgina web, CSS tracta de estilitzar una pàgina web. Significa establir colors, tipus de lletra, dimensions, marges, posicions dels elements d'una pàgina web.

L'objectiu però, no és tan sols estètic. Es tracta de fer pàgines webs fàcils de fer servir i fàcils d'entendre.

---

## Què és CSS

**CSS** significa **C**ascading **S**tyle **S**heets. El seu propòsit és _estilar_ llenguatges de marques (com HTML o XML). Per tant, el CSS no té valor per si sol, tret que estigui associat a un document HTML.

CSS dóna vida a un document HTML mitjançant l'elecció de tipus de lletra, l'aplicació de colors, la definició de marges, el posicionament d'elements, l'animació d'interaccions i molt més.

---

## CSS amb l'HTML

Podeu escriure CSS directament en un element HTML, utilitzant l'atribut `style`:

```html
<p style="color: red;">Aquest text és vermell.</p>
```

Podeu utilitzar una etiqueta `<style>` al `<head>` del vostre document HTML:

```html
<html>
  <head>
    <title>Hola món</title>
    <style type="text/css">
      p{ color: red;}
    </style>
  </head>
  <body>
    <p>Aquest paràgraf serà vermell.</p>
  </body>
</html>
```

---

## CSS en un fitxer separat

Podeu escriure el vostre CSS en un fitxer independent amb una extensió `.css` i, a continuació, enllaçar-lo al vostre HTML mitjançant l'etiqueta HTML `<link>`.

```css
p{ color: red;}
```

```html
<html>
  <head>
    <title>Hola món</title>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <p>Aquest paràgraf serà vermell.</p>
  </body>
</html>
```

Utilitzar un fitxer CSS independent és la manera **recomanable** de fer-ho.

---

## Per què no estil directament a l'HTML?

Perquè volem separar el **contingut** (HTML) de la seva **presentació** (CSS).

També facilita el **manteniment**: el mateix fitxer CSS es pot utilitzar per a tot un lloc web. Proporciona **flexibilitat**: centra't en el contingut d'una banda, l'estil de l'altra.

Fins i tot és possible que persones diferents desenvolupin per una banda l'HTML i per l'altre el CSS. I es pot tenir un HTML comú i **diferents opcions de CSS**.

---

## Sintaxi

La sintaxi és molt senzilla:

```css
/* Una regla CSS */
selector{ propietat: valor;}
```

Ho pots llegir com:

```css
qui{ què: com;}
```

CSS és un procés de 3 parts:

* el **selector** defineix _qui_ està orientat, quins elements HTML
* la **propietat** defineix _quina_ característica modificar
* el **valor** defineix _com_ alterar aquesta característica

Tot aquest bloc (selector/propietat/valor) és una **regla CSS**.

---

## Exemple ràpid (I)

Suposem que voleu canviar el color de tots els vostres títols `h2`.

```html
<h2>Alguna cosa</h2>
```

Centreu-vos en el **nom de l'etiqueta** (i oblideu-vos dels claudàtors angulars <> i del text). En el nostre cas, només queda _h2_. Hi ha una relació directa entre el nom de l'etiqueta i el selector.

Utilitzem-ho al nostre CSS com a **selector**, i apliquem un estil:

```css
h2 { background-color: lightgreen;}
```

---

## Exemple ràpid (II)

Ara el color del text no queda bé amb el color de fons. Millorem això:

```css
h2 { 
    background-color: lightgreen;
    color: darkgreen;
}
```

Dues observacions

* hem afegit un parell propietat/valor _segon_, tot mantenint només _un_ selector: podeu establir tantes propietats com vulgueu per a qualsevol conjunt de selectors.
* posem cada parell propietat/valor a la seva _propia línia_: com en HTML, l'**espai en blanc** no és important. Són els caràcters especials `{}` `:` i `;` els que importen. Com a resultat, podeu formatar el vostre CSS com vulgueu, per fer-lo més llegible, sempre que la seva sintaxi sigui vàlida.

---

## Exemple ràpid (III)

Ara ens agradaria posar un estil idèntic també als títols `<h1>`. Podríem copiar i enganxar la regla CSS i només canviar el selector, però, com hauríeu endevinat, hi ha una manera més ràpida:

```css
h1,
h2 { 
    background-color: lightgreen;
    color: darkgreen;
}
```

Ara tenim 2 selectors i 2 propietats. En conseqüència, tenim un _conjunt_ de selectors i un _conjunt_ de propietats (amb els seus valors respectius).

Podem tenir múltiples selectors, múltiples propietats i de vegades (però rarament) diversos valors.

---

## Exemple ràpid (IV)

Com en HTML, pot ser útil escriure comentaris CSS:

```css
/* Aquest és un comentari CSS */

h1,
h2 { 
    background-color: lightgreen;
    color: darkgreen;
}
/*
Els comentaris només estan destinats a ser llegits per humans
i no seran analitzats per l'ordinador
*/
```
