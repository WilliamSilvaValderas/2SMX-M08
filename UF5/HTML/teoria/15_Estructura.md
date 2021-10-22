# Estructura

## Per organitzar les principals parts de la vostra pàgina web

Quan escriviu contingut HTML com ara paràgrafs, llistes o enllaços, proporcioneu **significat** al vostre _text_. Però és possible que vulgueu **agrupar** alguns d’aquests elements junts.

Per exemple, la pàgina web d'un bloc es pot dividir en **4** parts:

* `header`: una **capçalera** que és similar a totes les pàgines i que és la navegació principal del lloc web (dins de `nav`)
* `article`: un contingut independent, complert, que canvia per a cada pàgina. Per exemple, una noticia, o un recepta de cuina, o la informació de contacte amb l'autor/a de la pàgina, etc.
* `sidebar`: una **barra lateral** que enllaça amb arxius i potser categories
* `footer`: un **peu de pàgina** per obtenir enllaços addicionals a pàgines menys importants

Hi ha alguns **elements HTML estructurals** que podeu utilitzar com a **contenidors** per a altres elements.

### Capçalera: header

El `header` sol ser el **primer** element HTML del codi. Actua com una **introducció** a la pàgina web, potser amb el logotip, el nom de la pàgina i enllaços de navegació.

```html
<header>
  <img src = "my-logo.jpg" alt = "Logotip de Tomaquet.cat">
  <h1>Tomàquets per tothom!</h1>
  <nav>
    <ul>
      <li>
        <a href="home.html"> Inici </a>
        <a href="about.html"> Quant a </a>
        <a href="contact.html"> Contacte </a>
      </li>
    </ul>
  </nav>
</header>
```

### Contingut: article

L'element `article` especifica contingut independent i autònom. Un article hauria de tenir sentit per si sol i hauria de ser possible distribuir-lo independentment de la resta del lloc web. Per exemple, es pot utilitzar l'element `<article>` a:

* Publicacions del fòrum
* Publicacions de blocs
* Comentaris dels usuaris
* Descripcions d'un producte a una botiga
* Articles de diaris

És possible que hi hagi més d'un element `article` a una pàgina web, per exemple, podriem tenir totes les noticies d'un diari i posar cadascuna d'elles dins d'una etiqueta `article`.

### Subapartats: section

L'element `section` permet **agrupar** diferents elements.

Les seccions _elles mateixes_ no tenen un significat específic. Es tracta més de la _relació entre els seus elements secundaris_ que del seu propi significat a la pàgina general.

Podem pensar en fer servir l'element `section` quan, per exemple, dins d'una etiqueta `article` tenim diferents parts que volem diferenciar.

### Peu de pàgina: footer

A diferència de la capçalera, el `footer` sol ser el **darrer** element d'una pàgina, on es repeteixen els enllaços de navegació principals i s'afegeixen els secundaris.

```html
<footer>
  <p> Tomaquet.cat | Copyright 2021 </p>
  <ul>
    <li>
      <a href="home.html"> Inici </a>
    </li>
    <li>
      <a href="about.html"> Quant a </a>
    </li>
    <li>
      <a href="contact.html"> Contacte </a>
    </li>
  </ul>
  <ul>
    <li>
      <a href="privacy-policy.html"> Política de privadesa </a>
    </li>
    <li>
      <a href="terms-of-use.html"> Condicions d'ús </a>
    </li>
  </ul>
</footer>
```

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Consulta la imatge de [l'article següent](http://www.cellbiol.com/bioinformatics_web_development/chapter-3-your-first-web-page-learning-html-and-css/introducing-html5-footer-header-nav-article-section-and-aside-elements/) on es mostren els elements `header`, `main`, `footer`. Explica, consultant l'article, per a que serveixen els elements `aside` i `nav`.
