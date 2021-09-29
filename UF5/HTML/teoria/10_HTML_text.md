# HTML és text

## El contingut HTML és 90% text

Quan escriviu codi HTML, escriviu **text**. Però el que normalment es mostra al navegador també és **text**.

Tot i que les imatges, els vídeos i la música han augmentat en popularitat, els llocs web continuen majoritàriament amb contingut de text, com ara aquest paràgraf en concret que esteu llegint.

### Paràgrafs

**Els paràgrafs** `<p>` són l'element HTML més utilitzat, ja que actuen com a element de nivell de bloc **predeterminat** i són ràpids d'escriure.

```html
<p>
  L'herba de rang, fins a la cintura, creix a la plana de Phutra, la magnífica herba florida del món interior, cada fulla en particular amb una flor petita de cinc puntes, petites estrelles brillants de diferents colors que centelleixen al fullatge verd per afegir un altre encant al paisatge estrany, però encantador.
</p>
```

### Llistes

**Les llistes** es presenten en 3 variants:

* `<ul>` són llistes sense ordenar
* `<ol>` són llistes ordenades (els elements es numeren automàticament)
* `<dl>` són llistes de definicions

Les llistes HTML requereixen una estructura específica:

* `<ul>` i `<ol>` han d'incloure i ser **pares** directes de `<li>`, que significa **elements de llista**.
* en conseqüència, els elements `<li>` no es poden utilitzar sols i han de ser **fills** directes de `<ul>` o `<ol>`.

#### Llistes no ordenades

Són els tipus de llistes més utilitzats. Estan destinats a agrupar una llista d'elements **indiviudals**, sense cap ordre concret.

```html
<p> La meva llista de la compra: </p>
<ul>
  <li> Llet </li>
  <li> Pa </li>
  <li> Xocolata </li>
  <li> Més xocolata </li>
</ul>
```

Els elements de la llista es mostren amb **punts**.

<table bgcolor="grey"><tr><td>
  <p> La meva llista de la compra: </p>
  <ul>
    <li> Llet </li>
    <li> Pa </li>
    <li> Xocolata </li>
    <li> Més xocolata </li>
  </ul>
</td></tr></table>

#### Llistes ordenades

Les llistes ordenades s’utilitzen quan **l'ordre** dels seus articles és **rellevant**.

```html
<ol>
  <li> Primer pas </li>
  <li> Pas dos </li>
  <li> ???? </li>
  <li> BENEFICI !!! </li>
</ol>
```

Les llistes ordenades **es numeren automàticament** pel navegador. No cal que inclogueu els números al vostre HTML.

#### Llistes de definicions

Les llistes de definicions corresponen a elements que es presenten en **parells**. Han d'incloure parells de termes de definició `<dt>` i descripcions de definició `<dd>` com a fills directes.

```html
<dl>
  <dt> Web </dt>
  <dd> La part d'Internet que conté llocs web i pàgines web </dd>
  <dt> HTML </dt>
  <dd> Un llenguatge de marques per crear pàgines web </dd>
  <dt> CSS </dt>
  <dd> Una tecnologia per millorar l'aspecte de l'HTML </dd>
</dl>
```

<table bgcolor="grey"><tr><td>
  <dl>
    <dt> Web </dt>
    <dd> La part d'Internet que conté llocs web i pàgines web </dd>
    <dt> HTML </dt>
    <dd> Un llenguatge de marques per crear pàgines web </dd>
    <dt> CSS </dt>
    <dd> Una tecnologia per millorar l'aspecte de l'HTML </dd>
  </dl>
</td></tr></table>

Les llistes de definicions poques vegades s’utilitzen perquè els seus casos d’ús són molt específics i només ocorren quan la clau canvia cada vegada. Les taules amb 2 columnes són l’alternativa més popular.

### Cites

Les cites s’utilitzen per identificar una **frase que ha dit algú**.

```html
<p> Sir Tim Berners-Lee va dir: </p>
<blockquote>
  La idea original del web era que hauria de ser un espai de col·laboració per comunicar-se compartint informació.
</blockquote>
```

<table bgcolor="grey"><tr><td>
  <p> Sir Tim Berners-Lee va dir: </p>
  <blockquote>
    La idea original del web era que hauria de ser un espai de col·laboració per comunicar-se compartint informació.
  </blockquote>
</td></tr></table>

### Encapçalaments

Hi ha 6 nivells d'encapçalaments disponibles, que van des de `<h1>` fins a `<h6>`, 1 essent el més important.

Les capçaleres s’utilitzen juntament amb paràgrafs i llistes per dibuixar una estructura natural al vostre document. Com que els encapçalaments tenen més pes semàntic, tingueu cura de mantenir l'equilibri entre contingut important i "normal".

Només l’ús d’encapçalaments en un document HTML no tindria sentit: si tot sembla important, realment no ho és. Heu de proporcionar profunditat a la vostra estructura.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Explica amb les teves paraules per a que s'han de fer servir els encapçalaments (`h1`, `h2`, etc...)
