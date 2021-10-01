# Enllaços

## El nucli de la web

Els **enllaços** són essencials en HTML, ja que el web es va dissenyar inicialment per ser una xarxa d'informació de documents **enllaçats** entre si.

La part `Hipertext` d'HTML defineix quin tipus d'enllaços utilitzem: enllaços _hipertext_, també coneguts com a **hiperenllaços**.

En HTML, els enllaços són **elements integrats** escrits amb l'etiqueta `<a>`.

L'atribut `href` (referència d'hipertext) s'utilitza per definir  l'**objectiu** de l'enllaç (on navegueu quan feu clic).

```html
<p>
  Per cercar alguna cosa, visiteu <a href="https://www.google.com"> Google </a>.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Per cercar alguna cosa, visiteu <a href="https://www.google.com"> Google </a>.
  </p>
</td></tr></table>

Els enllaços són la **principal** interacció d'una pàgina web: podeu navegar d'un document a un altre fent clic als enllaços.

Hi ha **3** tipus d'objectiu que podeu definir.

* **salts** per navegar per la mateixa pàgina
* **URL** relatius, generalment per navegar pel mateix lloc web
* **URL** absoluts, generalment per navegar a un altre lloc web

### Salts

**Salts** per navegar _dintre_ de la **mateixa** pàgina. Si el valor comença amb `#`, podeu provocar un salt a un element HTML amb un atribut específic `id`.

Per exemple, `<a href="#footer">` navegarà fins al `<div id ="footer">` dins del mateix document HTML. Aquest tipus de href s'utilitza sovint per tornar a la part superior de la pàgina.

### URL relatius

Si voleu definir un enllaç a una altra pàgina del mateix lloc web, podeu utilitzar URL **relatius**.

Però, en relació amb què? Bé, en relació amb la **pàgina actual**.

Utilitzem un exemple senzill on la carpeta `el-meu-primer-lloc-web` conté 2 fitxers HTML:

<ul class = "files">
  <li>
    <i class = "fa fa-folder-o"> </i>
    el-meu-primer-lloc-web
    <ul>
      <li>
        <i class = "fa fa-file-code-o"> </i>
        home.html
      </li>
      <li>
        <i class = "fa fa-file-code-o"> </i>
        contact.html
      </li>
    </ul>
  </li>
</ul>

A `home.html`, voleu definir un enllaç a `contact.html`.

Com que els dos fitxers es troben **a la mateixa carpeta**, només podeu escriure a `home.html`:

```html
<p>
  Aneu a la <a href="contact.html"> pàgina de contacte </a>.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Aneu a la <a href="contact.html"> pàgina de contacte </a>.
  </p>
</td></tr></table>

En un lloc web real, el procés és similar.

Suposem que teniu un lloc web anomenat "https://ireallylovecats.com" en el qual teniu dues pàgines web: `index.html` i `gallery.html`:

<ul class = "files">
  <li>
    <i class = "fa fa-folder-o"> </i>
    ireallylovecats.com
    <ul>
      <li>
        <i class = "fa fa-file-code-o"> </i>
        index.html
      </li>
      <li>
        <i class = "fa fa-file-code-o"> </i>
        gallery.html
      </li>
    </ul>
  </li>
</ul>

A `index.html` podeu escriure el següent enllaç:

```html
<p>
  Visiteu la <a href="gallery.html"> galeria </a>.
</p>
```

Recordeu: els llocs web s’allotgen en **equips** igual que el que feu servir actualment. Simplement es diuen **servidors** perquè el seu únic propòsit és allotjar llocs web. Però encara tenen **fitxers** i **carpetes** com ara ordinadors "normals".

### URL absoluts

Si volguéssiu compartir la vostra galeria de gats amb un amic, no podríeu enviar només `gallery.html`, ja que aquest **relatiu** URL només funciona per als documents HTML que es troben al mateix **ordinador** o el mateix **domini**.

Necessiteu l'URL _completa_ del document HTML: "https://ireallylovecats.com/gallery.html".

Aquest URL es pot segmentar en tres parts:

* **protocol** `https: //`
* **domini** `ireallylovecats.com`
* **camí del fitxer** `gallery.html`

Aquest **URL absolut** és **autosuficient**: independentment d'on utilitzeu el formulari d'enllaç, conté _tota_ la informació necessària per trobar el fitxer correcte, al domini correcte, amb el protocol correcte.

Normalment utilitzeu URL absoluts que defineixen un enllaç des del vostre lloc web a un altre lloc web.

Al fitxer `https://ireallylovecats.com/gallery.html`, podríeu escriure:

```html
<p>
  Trobeu més imatges dels meus gats al meu <a href="https://twitter.com/ireallylovecats"> compte de Twitter </a>.
</p>
```

### Enllaços relatius o absoluts?

Suposem que voleu enllaçar del primer al segon. L’enfocament més directe és utilitzar l’URL absolut. Per tant, afegiu `<a href="https://ireallylovecats.com/gallery.html"> Aneu a la segona pàgina </a>` al fitxer `index.html`.

Com que els dos fitxers es troben al mateix directori, podeu utilitzar l'URL **relativa** utilitzant `<a href="first-blog-post.html">`. Això és útil si decidiu moure el directori: els enllaços no es trencaran perquè els objectius de l'enllaç són relatius entre si, sempre que moveu els dos fitxers simultàniament i els mantingueu al mateix directori. Aquest enfocament relatiu és particularment útil en canviar de domini.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Per quina raó és recomenable fer servir enllaços relatius per enllaçar pàgines d'un mateix lloc web?
