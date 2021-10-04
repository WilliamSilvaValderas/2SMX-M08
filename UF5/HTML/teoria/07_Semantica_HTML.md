# Semàntica d'HTML

## HTML proporciona significat

El propòsit de les etiquetes HTML és proporcionar **significat** a un document. No us preocupeu per l’aspecte de la vostra pàgina web. Centreu-vos en la importància de cada etiqueta que utilitzeu.

En funció del contingut que escriviu, podeu triar l'element adequat que coincideixi amb el significat del text.

Aquest **rang** d'elements és prou ampli per adaptar-se a **usos** generals (com ara paràgrafs o llistes), i contingut **més específic** com `<output>` (per mostrar el resultat d'un càlcul) o `<progrés>` (per mostrar el progrés d'una tasca).

### Elements d’estructura: organització de la vostra pàgina

Els elements d’estructura us permeten organitzar les **parts principals** de la vostra pàgina. Normalment contenen altres elements HTML.

A continuació s'explica el que podria incloure una pàgina web típica:

* `<header>` com a **primer** element de la pàgina, que pot incloure el logotip i el slogan.
* `<nav>` com a llista de **enllaços** que van a les diferents pàgines del lloc web.
* `<h1>` com a títol de la pàgina.
* `<article>` com a contingut principal de la pàgina, com una publicació de bloc.
* `<footer>` com a **darrer** element de la pàgina, situat a la part inferior.

### Elements de text: definició del vostre contingut

Dins d’aquests elements d’estructura, normalment trobeu elements **de text** destinats a definir el **propòsit** del vostre contingut.

Utilitzarà principalment:

* `<p>` per als paràgrafs
* `<ul>` per a llistes (sense ordenar)
* `<ol>` per a llistes (ordenades)
* `<li>` per a elements de llista individuals
* `<blockquote>` per a cites

### Elements en línia: distingir el text

Com que els elements de text poden ser llargs però amb contingut variat, els elements **en línia** permeten **distingir** parts del text.

Hi ha molts elements en línia disponibles, però normalment us trobareu amb el següent:

<ul>
  <li> <code>&lt;strong&gt;</code> per a paraules <strong> importants </strong> </li>
  <li> <code>&lt;em&gt;</code> per a paraules <em> emfatitzades </em> </li>
  <li> <code>&lt;a&gt;</code> per als <a href="#"> enllaços </a> </li>
  <li> <code>&lt;small&gt;</code> per a paraules <small> menys importants </small> </li>
  <li> <code>&lt;abbr&gt;</code> per a abreviatures com W3C </li>
</ul>

<apart class = "comentaris">
  Només llegint aquest codi HTML, podeu entendre fàcilment què significa cada <strong> element HTML </strong>.
</aside>

```html
<article>
  <h1> Títol principal de la pàgina </h1>
  <h2> Un subtítol </h2>
  <p>
    Alguna cosa que sigui una altra cosa i alguns <em> èmfasi </em> i fins i tot paraules <strong> importants </strong>.
  </p>
  <p>
    Un altre paràgraf.
  </p>
  <ul>
    <li> Un </li>
    <li> Dos </li>
    <li> Tres </li>
  </ul>
  <blockquote>
    Un cop dit
  </blockquote>
</article>
<aside>
  <h3> Les meves darreres publicacions </h3>
  <ul>
    <li> <a href="#"> Un </a> </li>
    <li> <a href="#"> Un altre </a> </li>
    <li> <a href="#"> Un altre mes </a> </li>
  </ul>
</aside>
```

### Elements genèrics

Quan aparentment no sembla cap element _semantic_ adequat per al vostre contingut, però encara voleu inserir un element HTML (ja sigui per agrupar-lo o per dissenyar-lo), podeu conformar-vos amb un dels dos **elements** genèrics:

* `<div>` per a elements de nivell de bloc
* `<span>` per a elements en línia

Tot i que aquests elements HTML no signifiquen res, seran útils quan comencem a utilitzar CSS.

### No us plantegeu la semàntica

Hi ha aproximadament [100 elements HTML semàntics](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) per triar. Això és molt. Pot ser aclaparador passar per aquesta llista i triar l'element _apropiat_ per al vostre contingut.

Però no dediqueu massa temps a preocupar-vos per això. Si us complau la llista següent per ara, estareu prou bé:

<div class = "table">
  <table>
    <tr>
      <th> Estructura </th>
      <th> Text </th>
      <th> En línia </th>
    </tr>
    <tr>
      <td>
        <code> header </code> <br>
        <code> h1 </code> <br>
        <code> h2 </code> <br>
        <code> h3 </code> <br>
        <code> nav </code> <br>
        <code> footer </code> <br>
        <code> article </code> <br>
        <code> section </code>
      </td>
      <td>
        <code> p </code> <br>
        <code> ul </code> <br>
        <code> ol </code> <br>
        <code> li </code> <br>
        <code> blockquote </code>
      </td>
      <td>
        <code> a </code> <br>
        <code> strong </code> <br>
        <code> em </code> <br>
        <code> q </code> <br>
        <code> abbr </code> <br>
        <code> small </code>
      </td>
    </tr>
  </table>
</div>

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Explica amb les teves paraules que vol dir que la funció de l'HTML es proporcionar significat
