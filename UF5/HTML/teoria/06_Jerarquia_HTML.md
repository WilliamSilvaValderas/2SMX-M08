# Jerarquia d'HTML

## És un gran arbre familiar

Un document HTML és com un gran **arbre genealògic**, amb pares, germans, fills, avantpassats i descendents.

Prové de la capacitat de **anidar** elements HTML entre si.

### Nesting

Escrivim un paràgraf senzill i el millorem _diferenciant_ parts del text, inserint dos elements **en línia**:

```html
<p>
  Sir <strong> Alex Ferguson </strong> va dir una vegada sobre Filipo Inzaghi: <q>Aquell noi ha d'haver nascut fora de joc.</q>.
</p>
```

<table bgcolor="grey"><tr><td> 
<p> Sir <strong> Alex Ferguson </strong> va dir una vegada sobre Filipo Inzaghi: <q>Aquell noi ha d'haver nascut fora de joc.</q>. </p> </td></tr></table>

En aquesta configuració:

* l'element `<strong>` dóna més importància a les paraules "Alex Ferguson"
* el `<q>` marca la seva cita sobre Inzaghi

El fet que `<strong>` es mostri en **negreta** és **només el comportament predeterminat del navegador**. Recordeu que heu de triar els elements HTML segons el seu significat, i no el seu aspecte.

En aquest cas:

* `<p>` és l'element **pare** de `<strong>` i `<q>`
* `<strong>` i `<q>` són **elements** fills de `<p>`
* `<strong>` i `<q>` són elements **germans**

### Ordre

El funcionament del **nidificació** depèn de la ubicació de les etiquetes _obertura_ i _tancament_.

Com que un element HTML comprèn una etiqueta d'obertura, una etiqueta de tancament i tot el que hi ha entre, un element _child_ s'ha de tancar **abans de** tancar l'element _parent_.

```html
<! - Aquest és un codi INVÀLID. :-( ->
<p>
  Aquest codi HTML no funcionarà perquè l'etiqueta "forta" s'obre aquí <strong> però només es tanca després del paràgraf.
</p> </strong>
```

Com que el `<strong>` s'ha obert _després del `<p>` (i per tant es considera un **fill** de" `<p>`), l'element" `<strong>` "s'ha de tancar **abans de** el seu pare `<p>`.

```html
<! - Aquest codi és vàlid. :-) ->
<p>
  Aquest codi HTML funcionarà perquè l'etiqueta "forta" s'obre <strong> i es tanca </strong> correctament.
</p>
```

### Profunditat

Com que els elements fills poden contenir _altres_ elements fills, és possible escriure una **jerarquia més profunda** dins d'un document HTML.

El nostre paràgraf anterior podria formar part d'un bloc **article**:

```html
<article>
  <h1> Cites de futbol famosos </h1>
  <p>
    Sir <strong> Alex Ferguson </strong> va dir una vegada sobre Filipo Inzaghi: <q>Aquell noi ha d'haver nascut fora de joc</q>.
  </p>
  <p>
    Quan va ser criticat per John Carew, <strong> Zlatan Ibrahimovic </strong> va respondre: <q>El que fa Carew amb un futbol, ​​ho puc fer amb una taronja</q>.
  </p>
  <p>
    <strong> George Best </strong> va dir <q>Vaig gastar molts diners en begudes alcohòliques, ocells i cotxes ràpids. La resta només els vaig malbaratar</q> quan em van preguntar sobre el seu estil de vida.
  </p>
</article>
```

---
<table bgcolor="grey"><tr><td>
  <article>
    <h1> Cites de futbol famosos </h1>
    <p>
      Sir <strong> Alex Ferguson </strong> va dir una vegada sobre Filipo Inzaghi: <q>Aquell noi ha d'haver nascut fora de joc</q>.
    </p>
    <p>
      Quan va ser criticat per John Carew, <strong> Zlatan Ibrahimovic </strong> va respondre: <q>El que fa Carew amb un futbol, ​​ho puc fer amb una taronja</q>.
    </p>
    <p>
      <strong> George Best </strong> va respondre <q>Vaig gastar molts diners en begudes alcohòliques, ocells i cotxes ràpids. La resta només els vaig malbaratar</q> quan em van preguntar sobre el seu estil de vida.
    </p>
  </article>
</td></tr></table>
---

En aquesta configuració:

* `<article>` és el **avantpassat** de tots els altres elements
* `<article>` és el **pare** del `<h1>` i del 3 `<p>`
* `<h1>` i els 3 `<p>` són **germans**
* cada `<p>` és el **pare** dels `<strong>` i `<q>` que contenen
* tots els `<h1>`,`<p>`, `<strong>` i `<q>` són tots **descendents** de` <article> `

L’analogia de l’arbre genealògic encara s’aplica quan **travessem** diverses capes de nidificació HTML:

* un **descendent** de l'element X és qualsevol element _contingut_ dins de X
* un **nen** només és un descendent _directe_
* un **avantpassat** de l'element Y és qualsevol element que _contingui_ Y
* el **pare** és només el primer avantpassat _directe_
* Un **germà** de l'element X és qualsevol element que tingui el mateix pare

### Nidificació en bloc i en línia

Els elements **de bloc** poden contenir elements de bloc o en línia.

Tanmateix, els elements **inline** només poden contenir altres elements _inline_,amb lúnica excepció de l'element d'enllaç `<a>`!

```html
<! - Aquest és un codi INVÀLID. :-( ->
<strong>
  <p> No podeu posar cap paràgraf dins d'una etiqueta "strong".
</strong>
```

Només cal recordar l’avantpassat / descendent, pare / fill i germans. Aquesta jerarquia serà útil a CSS.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Explica amb un exemple l'ordre correcte d'obrir i tancar elements que són un dins de l'altre
