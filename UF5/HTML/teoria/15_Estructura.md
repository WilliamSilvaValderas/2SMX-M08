# Estructura

## Per organitzar les principals parts de la vostra pàgina web

Quan escriviu contingut HTML com ara paràgrafs, llistes o enllaços, proporcioneu **significat** al vostre _text_. Però és possible que vulgueu **agrupar** alguns d’aquests elements junts.

Per exemple, la pàgina web d'un bloc es pot dividir en **4** parts:

* `header`: una **capçalera** que és similar a totes les pàgines i que és la navegació principal del lloc web
* `main`: un contingut **principal**, que canvia per a cada pàgina: una llista d'articles, un sol article amb comentaris, una pàgina de contacte, etc.
* `sidebar`: una **barra lateral** que enllaça amb arxius i potser categories
* `footer`: un **peu de pàgina** per obtenir enllaços addicionals a pàgines menys importants

Hi ha alguns **elements HTML estructurals** que podeu utilitzar com a **contenidors** per a altres elements.

### Capçalera: header

El `header` sol ser el **primer** element HTML del codi. Actua com una **introducció** a la pàgina web, amb el logotip, un eslògan i enllaços de navegació.

```html
<header>
  <p>
    <a>
      <img src = "my-logo.jpg" alt = "Logotip de Tomaquet.cat">
    </a>
    <em> Un lloc web fantàstic </em>
  </p>
  <ul>
    <li>
      <a href="home.html"> Inici </a>
      <a href="about.html"> Quant a </a>
      <a href="contact.html"> Contacte </a>
    </li>
  </ul>
</header>
```

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

### Principal: main

L'element `main` conté, com el seu nom indica, el **contingut més important de la pàgina**, el que defineix l'objectiu de la pàgina.

Tot i que totes les pàgines web d'un lloc web contenen elements _comuns_ (com la capçalera, la navegació, el peu de pàgina ...), l'element `main` se centra en el contingut **únic**.

### Subapartats: section

L'element `section` permet **agrupar** diferents elements.

Les seccions _elles mateixes_ no tenen un significat específic. Es tracta més de la _relació entre els seus elements secundaris_ que del seu propi significat a la pàgina general.

Podem pensar en fer servir l'element `section` quan, per exemple, dins del `main` tenim diferents parts que volem diferenciar.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Consulta la imatge de [l'article següent](http://www.cellbiol.com/bioinformatics_web_development/chapter-3-your-first-web-page-learning-html-and-css/introducing-html5-footer-header-nav-article-section-and-aside-elements/) on es mostren els elements `header`, `main`, `footer`. Explica, consultant l'article, per a que serveixen els elements `aside` i `nav`.
