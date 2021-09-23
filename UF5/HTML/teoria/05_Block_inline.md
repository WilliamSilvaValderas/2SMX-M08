# Block i inline

## HTML té 2 tipus principals d'elements

En HTML, trobareu principalment 2 tipus d'elements HTML:

* **BLOCK** elements com:

  * paràgrafs `<p>`
  * llistes: sense ordenar (amb punts) `<ul>` o llistes ordenades (amb números) `<ol>`
  * encapçalaments: des del primer nivell `<h1>` fins als encapçalaments del 6è nivell `<h6>`
  * articles `<article>`
  * seccions `<section>`
  * cometes llargues `<blockquote>`

* **INLINE** elements com:

  * enllaços `<a>`
  * paraules emfatitzades `<em>`
  * paraules importants `<strong>`
  * cometes curtes `<q>`
  * abreviatures `<abbr>`

Els elements **de bloc** estan destinats a **estructurar** les parts principals de la pàgina dividint el contingut en blocs _coherents_.

Els elements **en línia** estan destinats a diferenciar _part_ d'un text, per donar-li una funció o significat particular. Els elements en línia solen contenir una sola o poques paraules.

```html
<p> Heu vist aquest <a href="https://www.youtube.com"> increïble vídeo </a> a YouTube? </p>
```

### Obrir i tancar etiquetes

**Tots els** elements de nivell de bloc tenen etiquetes d'obertura i tancament.

Com a resultat, els elements que contenen auto-tancament (*self-closing*) són elements **en línia**, simplement perquè la seva sintaxi no els permet contenir cap altre element HTML.

<div class = "table">
  <table>
    <tr>
      <th class = "empty"> </th>
      <th> Teniu etiquetes d'obertura i tancament </th>
      <th> Tancament automàtic </th>
    </tr>
    <tr>
      <th> Elements de bloc </th>
      <td>
        <code>&lt;p&gt;</code>
        <code>&lt;/ p&gt;</code>
        <br>
        <code>&lt;ul&gt;</code>
        <code>&lt;/ul&gt;</code>
        <br>
        <code>&lt;ol&gt;</code>
        <code>&lt;/ol&gt;</code>
      </td>
      <td>
        <strong> Impossible </strong>
      </td>
    </tr>
    <tr>
      <th> Elements en línia </th>
      <td>
        <code>&lt;a&gt;</code>
        <code>&lt;/a&gt;</code>
        <br>
        <code>&lt;strong&gt;</code>
        <code>&lt;/strong&gt;</code>
        <br>
        <code>&lt;em&gt;</code>
        <code>&lt;/em&gt;</code>
      </td>
      <td>
        <code>&lt;input&gt;</code>
        <br>
        <code>&lt;br&gt;</code>
        <br>
        <code>&lt;img&gt;</code>
      </td>
    </tr>
  </table>
</div>

### Altres tipus d'elements HTML

Hi ha algunes etiquetes que no es poden assignar com a etiquetes del tipus `block`, però tampoc com a etiquetes del tipus `inline`. Les més conegudes són les següents:

* **elements de llista**: `<li>`
* **taula**, **files de taula**, **cel·les de taula**: `<table>`, `<tr>` i `<td>` respectivament

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Què vol dir que un element és del tipus `block`? Per a que serveixen els elements d'aquest tipus?
2. Què vol dir que un element és del tipus `inline`? Per a que serveixen els elements d'aquest tipus?
