---
marp: true
title: Text
paginate: true
---

# Text

---

## Introducció

Les pàgines web consisteixen principalment en **text** Tot i que CSS també permet alterar el disseny d'una pàgina web, formatar el text amb CSS és el primer que fa la gent.

CSS proporciona diverses propietats **font**, que afecten directament la representació del text. La propietat `font-family` defineix _quina_ font utilitzar.

---

## Famílies de tipus de lletra genèriques

Els tipus de lletra s'agrupen en 5 famílies **genèriques**:

* `serif` [amb petites decoracions adjuntes al final de cada caràcter](https://www.freecodecamp.org/news/html-font-css-font-family-example-serif-and-sans-serif-characters/#theseriffonttype)
* `sans-serif`
* `monoespace`
* `cursive` (no s'utilitza mai)
* `fantasy` (no s'utilitza mai)

```css
/* aplica un tipus de lletra per a tot el document HTML */
body{ font-family: sans-serif;}
```

---

## Tipus de lletra específic

El problema amb l'ús de noms de tipus de lletra genèrics és que el disseny de la vostra pàgina web es basarà en el tipus de lletra establert per l'usuari a la seva configuració.

Com que probablement voleu que la vostra pàgina web tingui el mateix aspecte a l'ordinador de qualsevol persona, voldreu definir un tipus de lletra **específic** per utilitzar-lo. Per fer-ho, només cal que utilitzeu el **nom** del tipus de lletra.

```css
body{ font-family: 'Arial';}
```

La vostra pàgina web utilitzarà Arial **sempre que estigui instal·lada a l'ordinador de l'usuari**.

---

## Tipus de lletra segurs per a la web

Arial és una opció segura, perquè s'instal·la a tots els ordinadors Windows i Mac, i a la majoria de sistemes Linux. És per això que Arial es considera un tipus de lletra **segur per a la web**. N'hi ha aquests tipus de lletra segurs per a la web:

* Arial (sans-serif)
* Verdana (sans-serif)
* Helvetica (sans-serif)
* Tahoma (sans-serif)
* Trebuchet MS (sans-serif)
* Times New Roman (serif)
* Georgia (serif)
* Garamond (serif)
* Courier New (monospace)

---

## Aplicant una llista de tipus de lletra

Tot i que utilitzar _qualsevol_ d'aquests valors per a la propietat `font-family` és una aposta segura, podeu definir valors **de reserva** escrivint una **llista de famílies de tipus de lletra**:

```css
body{ font-family: Georgia, 'Times New Roman', serif;}
```

En definir **valors múltiples** per a `font-family`, el navegador buscarà el primer valor `Georgia` i l'utilitzarà. Si no està disponible, utilitzarà el següent `Times New Roman`. Finalment, si aquest tampoc està disponible, utilitzarà el tipus de lletra `serif` predeterminat del navegador.

---

## Incloure una font

Com que els dissenyadors volen utilitzar tipus de lletra més originals, però encara volen que la seva pàgina web sembli exactament igual a l'ordinador de qualsevol persona, és possible **incloure una font** en una pàgina web. D'aquesta manera, s'asseguren que el tipus de lletra estigui disponible encara que no estigui present a l'ordinador de l'usuari, simplement perquè el lloc web proporciona el tipus de lletra.

Per exemple [Google proporciona fonts que pots incloure a la teva web](https://www.w3schools.com/howto/howto_google_fonts.asp).

---

## font-size

Ja hem tractat les unitats de mida CSS que s'utilitzen per definir la mida de la lletra, entre altres coses.

```css
p{ font-size: 16px;}
```

Tingueu en compte que establir una mida de lletra de `16px` no farà que cada lletra sigui `16px` d'alçada. La mida _real_ de cada lletra depèn de la família de tipus de lletra utilitzada.

---

## font-style

Aquesta propietat pot fer que el vostre text sigui _cursiva_:

```css
h2{ font-style: italic;}
```

Valor per defecte: `font-style: normal;`.

Un altre valor possible és `oblique`, però mai s'utilitza.

---

## font-weight

Aquesta propietat pot fer que el vostre text sigui **negreta**:

```css
h2{ font-weight: bold;}
```

Valor per defecte: `font-weight: normal;`.

Depenent de la `font-family` utilitzada, hi ha una gamma de pesos de lletra disponibles, des de `100` fins a `900`.

```css
h2{ font-weight: 700; }/* bold */
```

Molt poques fonts proporcionen els 9 pesos. La [font Exo](https://www.google.com/fonts/specimen/Exo) és una d'elles. La majoria en trobareu 400 (normal) i 700 (negreta), i de vegades 300 (clar) i 500 (mitjana).

---

## font-variant

Aquesta propietat converteix el vostre text en majúscules petites:

```css
h2{ font-variant: small-caps;}
```

Valor per defecte: `font-variant: normal;`.

No és una propietat molt utilitzada.

---

## line-height (I)

La propietat `line-height`, quan s'aplica a l'element de nivell de bloc, defineix, com el seu nom suggereix literalment, l'**altura de cada línia**.

La propietat `line-height` utilitza les unitats següents:

* `px`
* 'em'
* `%`
* nombres sense unitat, com `1,5`.

Els valors sense unitats actuen bàsicament com a percentatges. Per tant, `150%` és igual a `1,5`. Aquest últim és més compacte i llegible.

---

## line-height (II)

El propòsit de l'alçada de línia és definir un interlineat llegible per al vostre text. Com que la llegibilitat depèn de la mida del text, es recomana utilitzar un valor **dinàmic** relatiu a la mida del text. Per tant, no es recomana utilitzar `px` perquè defineix un valor **estàtic**.

El mètode recomanat és **números sense unitat**:

* Per al text del cos, es recomana una alçada de línia d'1,5 vegades la mida del text.
* Per als encapçalaments, es recomana una alçada de línia d'1,2

```css
/* alçada de la línia calculada serà de 16 * 1,5 = 24px. */
body{ font-size: 16px; line-height: 1.5;}
```

---

## line-height (III)

Com que la propietat `line-height` és **heretada** pels elements fills, romandrà coherent sense importar quina `font-size` s'apliqui posteriorment.

```css
body{ font-size: 16px; line-height: 1.5;}
p{ font-size: 18px;}
```

L'element `p` tindrà una alçada de línia de `27px` (18 * 1'5 = 27)

---

## font

En CSS, algunes propietats es poden **agrupar** sota una altra propietat, per estalviar temps i espai. La propietat `font` agrupa, en aquest ordre concret, les propietats:

* `font-style`
* `font-variant`
* `font-weight`
* `font-size`
* `line-height`
* `font-family`

Així, podeu definir 6 propietats mitjançant una única:

```css
/* Observeu la / entre font-size i line-height */
body{ font: italic small-caps bold 16px/1.5 Arial, sans-serif;}
```

---

## text-align

La propietat `text-align` s'ha d'aplicar a un element a nivell de bloc i defineix com s'alineen horitzontalment el seu text i els elements secundaris en línia.

```css
body{ text-align: left;}
```

Els valors més utilitzats són `left`, `right`, `center` i `justify`.

El valor per defecte de `text-align` és `start`. Bàsicament, `start` pot ser `left` o `right`, depenent de la **direcció** establerta al document HTML. La propietat CSS `direction` pot ser `ltr` (d'esquerra a dreta) o `rtl` (de dreta a esquerra).

---

## text-decoration

La propietat `text-decoration` s'utilitza per afegir una línia al vostre text.

Valor per defecte: `none`.

```css
.deleted{ text-decoration: line-through;}
```

També pot tenir els valors `overline` i `underline`. Per defecte, els enllaços HTML (`<a>`) tenen una `text-decoration: underline;` aplicada. Una de les primeres coses que solen fer els programadors és eliminar aquest estil predeterminat:

```css
a{ text-decoration: none;}
```

---

## text-indent

La propietat `text-indent` permet afegir espai abans de la primera lletra de la primera línia d'un element de nivell de bloc.

Valor per defecte: `0` (zero)

```css
p{ text-indent: 30px;}
```

Com a la propietat `font-size`, podeu utilitzar valors `px`, `em` o fins i tot `%`.

---

## text-shadow

En CSS, podeu afegir ombra a un text, perquè sigui més elegant o més llegible.

Es defineix:

* `x` el desplaçament horitzontal
* `y` el desplaçament vertical
* el desenfocament o _blur_
* el `color`.

```css
h1{ text-shadow: 0 2px 5px rgba(0,0,0,0.5);}
```

Només calen els valors `x` i `y`. El "desenfocament" per defecte és `0` (zero), mentre que el `color` és el color del text per defecte.

---

## text-transform

La propietat `text-transform` modifica l'aparença d'un text per mostrar-lo en majúscules i/o minúscules. Els valors possible són:

* `uppercase`
* `lowercase`
* `capitalize` (transforma la primera lletra de cada paraula en majúscula)

```css
h1, h2{ text-transform: capitalize;}
```
