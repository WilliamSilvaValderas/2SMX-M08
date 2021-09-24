# Sintaxi HTML

## Com qualsevol idioma, l'HTML té regles

**HTML** significa **H** iper **T** ext **M** arkup **L** anguage:

* **HyperText** significa que utilitza la part HTTP d'Internet
* **Marcatge** significa que el codi que escriviu està anotat amb paraules clau
* **Idioma** significa que tant un humà com un ordinador poden llegir-lo

Com qualsevol idioma, HTML inclou un conjunt de **regles**. Aquestes regles són relativament senzilles. Es tracta de definir **límits**, saber per on comença alguna cosa i per on acaba alguna cosa.

Aquí teniu un exemple de paràgraf en HTML:

```html
<p> Si Tetris m'ha ensenyat alguna cosa, és que s'acumulen errors i desapareixen els èxits. </p>
```

<table bgcolor="grey"><tr><td> <p> Si Tetris m'ha ensenyat alguna cosa, és que s'acumulen errors i desapareixen els èxits. </p> </td></tr></table>

El que veieu entre **claudàtors** `<` i `>` són etiquetes HTML. Defineixen on comença alguna cosa i on acaba.

Cadascun d'ells té un **significat** específic. En aquest cas, `p` significa **paràgraf**.

Solen anar en parelles:

* l'etiqueta _opening_ `<p>` defineix el **inici** del paràgraf
* l'etiqueta _closing_ `</p>` defineix el seu **final**

L'única diferència entre una etiqueta d'obertura i de tancament és la **barra** `/` que precedeix el nom de l'etiqueta.

Quan es combina una etiqueta d'obertura, una etiqueta de tancament i tot el que hi ha al mig, s'obté un **element HTML**. Tota la línia és un element HTML que utilitza les etiquetes HTML `<p>` i `</p>`.

Si [visualitzeu aquesta mostra al vostre navegador] (/ html / sample-paragraph.html), notareu que el navegador no mostra **les etiquetes HTML**. El navegador només les _llegeix_ per saber quin tipus de **contingut** heu escrit.

### On escriure HTML

Probablement us heu trobat amb fitxers de text senzills, que tenen una extensió `.txt`.

Perquè aquest fitxer de text esdevingui un **document HTML** (en lloc d’un document de text), heu d’utilitzar una extensió `.html`.

Obriu el vostre **editor de text** i copieu i enganxeu el següent:

```html
<p> Aquesta és la meva primera pàgina web! </p>
```

Deseu aquest fitxer com a "my-first-webpage.html" i obriu-lo amb el navegador i veureu:

<table bgcolor="grey"><tr><td> <p> Aquesta és la meva primera pàgina web! </p> </td></tr></table>

Recordeu:

* utilitzeu un editor de text com Visual Studio Code per **crear** documents HTML
* utilitzeu un navegador com Firefox per **obrir** documents HTML

### Atributs

Els atributs actuen com informació **extra** lligada a un element HTML. S'escriuen _dins_ d'una etiqueta HTML. Com a tal, tampoc no els mostra el navegador.

Per exemple, l'atribut `href` s'utilitza per definir l'objectiu d'un **enllaç** (que utilitza una etiqueta **a** nchor):

```html
<a href="https://www.mozilla.com/firefox"> Baixeu Firefox </a>
```

<table bgcolor="grey"><tr><td> <a href="https://www.mozilla.com/firefox"> Baixeu Firefox </a> </td></tr></table>

Hi ha [16 atributs HTML](https://www.w3schools.com/tags/ref_standardattributes.asp) que es poden utilitzar en qualsevol element HTML. Tots són **opcionals**.

Utilitzarà principalment `class` (que s'utilitza per a CSS) i `title` (que és la descripció que apareix quan es passa el cursor per sobre d'un element com aquest).

Alguns elements HTML tenen atributs **obligatoris**. Per exemple, quan s'insereix una imatge, haureu de proporcionar la ubicació de la imatge mitjançant l'atribut `src` (font):

```html
<img src = "#" alt = "Descripció de la imatge">
```

Tenint en compte que l’objectiu de l’element `<img>` és mostrar una imatge, té sentit que sigui **obligatori** el camí cap a la imatge.

### Comentaris

Si escriviu alguna cosa al vostre codi sense interrompre la manera com el navegador mostrarà la vostra pàgina, podeu escriure **comentaris**. El navegador els _ignorarà_ i només serà útil per als humans que escrivim el codi.

Un comentari comença per `<!--` i acaba amb `-->`.

```html
<!-- Aquesta frase serà ignorada pel navegador -->
<p> Hola món! </p>
```

<table bgcolor="grey"><tr><td> <p> Hola món! </p> </td></tr></table>

### Elements _self-closing_

Alguns elements HTML són una única etiqueta, no hi ha etiqueta d'obertura i tancament:

```html
<br /> <!-- salt de línia -->
<hr /> <!-- linia horitzontal -->
<img src = "https://placehold.it/50x50" alt = "Descripció" /> <!-- image -->
<input type = "text" /> <!-- text input -->
```

En aquest [enllaç podeu consultar una llista d'etiquetes _self-closing_](http://xahlee.info/js/html5_non-closing_tag.html)

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Com s'escriu un comentari amb HTML? Per a que serveix?
2. Què són els atributs d'una etiqueta HTML?
3. Què és una etiqueta _self-closing_?
