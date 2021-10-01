# Semàntica en línia

## Les petites parts dins d'un bloc de text

Tot i que els paràgrafs i les llistes estan destinats a identificar **blocs** sencers de text, de vegades volem donar significat a una paraula (o algunes paraules) _dintre_ d’un text.

### Strong

Per a paraules **importants**, utilitzeu l'etiqueta `<strong>`:

```html
<p>
  Això és <strong> important </strong> o potser no.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Això és <strong> important </strong> o potser no.
  </p>
</td></tr></table>

Per defecte, els elements `<strong>` es mostren en **negreta**, però tingueu en compte que només és el comportament predeterminat del navegador. No utilitzeu `<strong>` _només_ per posar algun text en negreta, sinó per donar-li més **importància**.

### Èmfasi

Per a les paraules _accentuades_, utilitzeu l'etiqueta `<em>`:

```html
<p>
  Això es <em> emfatitza </em> o potser no.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Això es <em> emfatitza </em> o potser no.
  </p>
</td></tr></table>

Per defecte, els elements `<em>` es mostren a _italic_, però tingueu en compte que només és el comportament predeterminat del navegador. No utilitzeu `<em>` _només_ per posar text en cursiva, sinó per posar-li èmfasi.

### Abreviatures

Les abreviatures com W3C o CD poden utilitzar l'element `<abbr>`:

```html
<p>
  Acabo de comprar un <abbr> CD </abbr>.
</p>
```

Podeu afegir un atribut "title" ** per especificar la descripció de l'abreviatura, que apareixerà passant el cursor per l'element:

```html
<p>
  Acabo de comprar un <abbr title = "Compact Disc"> CD </abbr>.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Acabo de comprar un <abbr title = "Compact Disc"> CD </abbr>.
  </p>
</td></tr></table>

### Cites en línia

L'element `<blockquote>` és un element de **nivell de bloc**. Té una versió **en línia**: `<q>`:

```html
<p>
  Va dir <q>Hello World</q> i va sortir.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Va dir <q>Hello World</q> i va sortir.
  </p>
</td></tr></table>

### Altres elements en línia

Hi ha molts altres [elements semàntics en línia](https://developer.mozilla.org/en/docs/Web/HTML/Element#Inline_text_semantics) per triar, però hem cobert els més habituals.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Explica que fan les etiquetes inline `<kbd>` i `<code>`.
