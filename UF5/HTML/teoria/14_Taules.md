# Taules

## Per a dades multidimensionals

Les **taules** HTML estan destinades només a les **dades tabulars**, que són qualsevol tipus de contingut que es pot disposar semànticament en **files** i **columnes**.

És com tenir un **full de càlcul**.

### Sintaxi

La creació d’una taula en HTML requereix una **estructura específica**:

* obriu un `<table>`
* afegiu files amb `<tr>`
* afegiu cel·les _regulars_ amb `<td>` o cel·les _encapçalades_ amb `<th>`

Aquesta **jerarquia** és obligatòria i són necessaris els 3 elements per construir una taula.

Quan escriviu el codi, heu de definir les cel·les de la taula d’esquerra a dreta i, després, de baix a baix.

```html
<table>
  <tr>
    <td> John Lennon </td>
    <td> Guitarra rítmica </td>
  </tr>
  <tr>
    <td> Paul McCartney </td>
    <td> Baix </td>
  </tr>
  <tr>
    <td> George Harrison </td>
    <td> Guitarra principal </td>
  </tr>
  <tr>
    <td> Ringo Starr </td>
    <td> Bateria </td>
  </tr>
</table>
```

<table bgcolor="grey"><tr><td>
  <table>
    <tr>
      <td> John Lennon </td>
      <td> Guitarra rítmica </td>
    </tr>
    <tr>
      <td> Paul McCartney </td>
      <td> Baix </td>
    </tr>
    <tr>
      <td> George Harrison </td>
      <td> Guitarra principal </td>
    </tr>
    <tr>
      <td> Ringo Starr </td>
      <td> Bateria </td>
    </tr>
  </table>
</td></tr></table>

Com podeu veure, una taula en HTML és relativament **detallada**: hi ha moltes etiquetes per a poques files de dades.

### thead, tfoot i tbody

Igual que una pàgina web pot tenir una capçalera i un peu de pàgina, una **taula** pot tenir un cap, un cos i un peu. Com qualsevol cosa en HTML, això és purament per raons **semàntiques**: proporcionar més estructura a la vostra taula.

`<thead>`, `<tfoot>` i `<tbody>` són col·leccions de **files**. Com a tals, són fills _directes_ de `<table>` i pares _directes_ d'un o més `<tr>`. En resum, afegeixen **un nivell de jerarquia**.

`<thead>` i `<tfoot>` s'utilitzen com a **resum** de les columnes.

Millorem la taula anterior amb un cap i un cos:

```html
<table>
  <thead>
    <tr>
      <th> Nom </th>
      <th> Instrument </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td> John Lennon </td>
      <td> Guitarra rítmica </td>
    </tr>
    <tr>
      <td> Paul McCartney </td>
      <td> Baix </td>
    </tr>
    <tr>
      <td> George Harrison </td>
      <td> Guitarra principal </td>
    </tr>
    <tr>
      <td> Ringo Starr </td>
      <td> Bateria </td>
    </tr>
  </tbody>
</table>
```

<table bgcolor="grey"><tr><td>
  <table>
    <thead>
      <tr>
        <th> Nom </th>
        <th> Instrument </th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td> John Lennon </td>
        <td> Guitarra rítmica </td>
      </tr>
      <tr>
        <td> Paul McCartney </td>
        <td> Baix </td>
      </tr>
      <tr>
        <td> George Harrison </td>
        <td> Guitarra principal </td>
      </tr>
      <tr>
        <td> Ringo Starr </td>
        <td> Bateria </td>
      </tr>
    </tbody>
  </table>
</td></tr></table>

### Particularitat de `<tfoot>`

Afegim també un peu a la taula:

```html
<table>
  <thead>
    <tr>
      <th> Nom </th>
      <th> Instrument </th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <th> Nom </th>
      <th> Instrument </th>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td> John Lennon </td>
      <td> Guitarra rítmica </td>
    </tr>
    <tr>
      <td> Paul McCartney </td>
      <td> Baix </td>
    </tr>
    <tr>
      <td> George Harrison </td>
      <td> Guitarra principal </td>
    </tr>
    <tr>
      <td> Ringo Starr </td>
      <td> Bateria </td>
    </tr>
  </tbody>
</table>
```

<table bgcolor="grey"><tr><td>
  <table>
    <thead>
      <tr>
        <th> Nom </th>
        <th> Instrument </th>
      </tr>
    </thead>
    <tfoot>
      <tr>
        <th> Nom </th>
        <th> Instrument </th>
      </tr>
    </tfoot>
    <tbody>
      <tr>
        <td> John Lennon </td>
        <td> Guitarra rítmica </td>
      </tr>
      <tr>
        <td> Paul McCartney </td>
        <td> Baix </td>
      </tr>
      <tr>
        <td> George Harrison </td>
        <td> Guitarra principal </td>
      </tr>
      <tr>
        <td> Ringo Starr </td>
        <td> Bateria </td>
      </tr>
    </tbody>
  </table>
</td></tr></table>

Tot i que hem afegit un `<tfoot>` **abans que** el `<tbody>`, aquest apareix **al final**.

Prové del fet que el `<tbody>` pot contenir una gran quantitat de files. Però el navegador vol representar el peu abans de rebre totes les (potencialment nombroses) files de dades. Per això, `<tfoot>` és el primer del codi.

### colspan i rowspan

Podeu **combinar** columnes o files utilitzant respectivament els espais de fila i colspan.

Tingueu en compte que per combinar _columnes_ heu d'utilitzar l'atribut `rowspan`, ja que permet _espandir_ una **columna** a través de diverses _files_.

```html
<table>
  <tr>
    <th colspan = "2"> Singles de Michael Jackson </th>
  </tr>
  <tr>
    <th rowspan = "3"> 1979 </th>
    <td> Don't Stop 'Til You Get Enough </td>
  </tr>
  <tr>
    <td> Rock with You </td>
  </tr>
  <tr>
    <td> Off the Wall </td>
  </tr>
</table>
```

<table bgcolor="grey"><tr><td>
  <table>
    <tr>
      <th colspan = "2"> Singles de Michael Jackson </th>
    </tr>
    <tr>
      <td rowspan = "3"> 1979 </td>
      <td> Don't Stop 'Til You Get Enough </td>
    </tr>
    <tr>
      <td> Rock with You </td>
    </tr>
    <tr>
      <td> Off the Wall </td>
    </tr>
  </table>
</td></tr></table>

La cel·la "Michael Jackson Singles" ocupa dues columnes, de manera que la fila següent inclou **dues** cel·les.

Com que la cel·la "1979" abasta tres files, les dues files següents només inclouen una **una** cel·la, per deixar espai a la columna "1979".

Pot ser difícil fer un seguiment de quantes cèl·lules falten o són superflues. Una manera senzilla de construir una taula completa de 2 per 4 primer i, després, eliminar les cel·les mentre afegiu atributs `colspan` i `rowspan`.
En el nostre cas, se suposa que tenim **8** cel·les. Només escrivim **5** cel·les, però els fitxers `colspan ="2"` i `rowspan = "3"` afegeixen **3 cel·les addicionals**.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Quina diferència hi ha entre l'etiqueta `<td>` i `<th>`?
