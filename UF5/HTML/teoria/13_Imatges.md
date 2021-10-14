# Imatges

## Després del text, venen les imatges

**Les imatges** són el primer contingut no textual que ha aparegut al web. La majoria de formats d’imatges que podeu trobar a l’ordinador també es poden mostrar al navegador: `.jpg`, `.gif` (animat o no), `.png` (transparent o no)...

### Sintaxi

**Les imatges** utilitzen l'element `<img>`, que és un element de **tancament automàtic** (només té una etiqueta d'obertura).

L'atribut `src` defineix l'**ubicació** de la imatge. Igual que amb els enllaços, podeu utilitzar URL relatius o _absoluts_. L'atribut `alt` proporciona **informació alternativa en text** per si l'imatge no es pot visualitzar (un error, connexió lenta o s'està fent servir un programa de lectura de pantalla, per exemple, per una persona invident).

<ul class = "files">
  <li>
    <i class = "fa fa-folder-o"> </i>
    el meu primer lloc web
    <ul>
      <li>
        <i class = "fa fa-file-code-o"> </i>
        home.html
      </li>
      <li>
        <i class = "fa fa-image"> </i>
        gat.jpg
      </li>
    </ul>
  </li>
</ul>

```html
<p>
  Mireu el meu gat.
  <br>
  <img src="gat.jpg" alt="el meu gat">
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Mireu el meu gat.
    <br>
    <img src="../exemples/gat.jpg" width="300" alt="el meu gat">
  </p>
</td></tr></table>



### Dimensions

Totes les imatges tenen **2 dimensions**: una **amplada** i una **alçada**. La imatge del gat que es mostrava anteriorment té 910 píxels d'ample i 603 d'alt.

En inserir una imatge en HTML, **no cal que n'especifiqueu les dimensions**: el navegador la mostrarà automàticament a **mida completa**.

Si voleu modificar les dimensions d’una imatge, tot i que és possible en HTML, es recomana utilitzar CSS, com veurem en capítols posteriors.

### Voleu bloquejar-lo o inserir-lo?

Tot i que una imatge té una amplada i una alçada, i visualment és un gran rectangle, una imatge no **és un element de bloc HTML**, sinó que en realitat és un **element en línia**.

Això es deu a que l'element `<img>` és un element de **tancament automàtic**: tècnicament no pot contenir cap altre element HTML i, per tant, es considera un element en línia, com ara `<a>`, `<strong>` o `<em>`.

Aquest comportament en línia pot tenir resultats inesperats:

```html
<p>
  Hi ha un gat
  <img src="gat.jpg">
  al mig del paràgraf!
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Hi ha una gat
    <img src="../exemples/gat.jpg" width="300">
    al mig del paràgraf!
  </p>
</td></tr></table>

Com que en HTML, el **contingut és el que importa**, les imatges es mostraran independentment de quedin bé o malament, com l'exemple anterior.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Busqueu informació de quins formats d'imatge són aptes per una pàgina web.
