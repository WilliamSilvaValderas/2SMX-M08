# Formularis

## Per fer una pàgina web interactiva

Mentre navega pel web, la interacció d’un usuari sol és fer clic a **enllaços** per navegar per pàgines web.

Però el web entén que de vegades cal que l'usuari proporcioni la seva pròpia **entrada**. Aquests tipus d'interacció inclouen:

* registrar-se i iniciar la sessió a llocs web
* introduir informació personal (nom, adreça, dades de la targeta de crèdit ...)
* filtrar contingut (mitjançant desplegables, caselles de selecció ...)
* realitzant una cerca
* càrrega de fitxers

Per adaptar-se a aquestes necessitats, HTML proporciona **controls de formulari interactius**:

* entrades de text (per a una o diverses línies)
* botons d'opció
* caselles de selecció
* desplegables
* selector de fitxers per carregar
* botons d'enviament

Aquests controls fan servir diferents **etiquetes HTML**, però la majoria utilitzen l'etiqueta `<input>`. Com que és un element de tancament automàtic, el tipus d'entrada es defineix pel seu atribut "type":

```html
<!-- Una entrada de text -->
<input type = "text">
<!-- Una casella de selecció -->
<input type = "checkbox">
<!-- Un botó d'opció -->
<input type = "radio">
```

  ### L'element Form

El `<form>` és un element de nivell de bloc que defineix una part **interactiva** d'una pàgina web. Com a resultat, tots els controls de formulari (com ara `<input>`, `<textarea>` o `<button>`) han d'aparèixer _dins_ d'un element `<form>`.

**Calen dos atributs HTML**:

* `action` conté una adreça que defineix _on_ s'enviarà la informació del formulari
* El `method` pot ser GET o POST i defineix com s'enviarà la informació del formulari

Normalment, la informació del formulari s’envia a un **servidor**. _Com_ es processaran aquestes dades va més enllà de l'abast d'aquest curs.

Penseu en un formulari com una col·lecció de controls d'entrada que funcionen junts per realitzar una operació **única**. Si escriviu un formulari d'inici de sessió, podríeu tenir **3** controls:

* una entrada de correu electrònic `<input type ="email">`
* una entrada de contrasenya `<input type ="password">`
* un botó d'enviament `<input type ="submit">`

Aquests 3 elements HTML s'inclourien dins d'un únic `<form action ="/login" method ="POST">`.

De manera similar, podríeu afegir un formulari d’inscripció a la mateixa pàgina HTML, en un element separat `<form>`.

### Entrades de text

Gairebé tots els formularis requereixen una entrada **textual** per part dels usuaris, perquè puguin introduir el seu nom, correu electrònic, contrasenya, adreça ... Els controls de formularis de text presenten diferents variacions:

<div class = "table">
  <table>
    <tr>
      <th> Text </th>
      <td> <code>&lt;input type = "text"&gt;</code> </td>
      <td> Permet qualsevol tipus de caràcter </td>
    </tr>
    <tr>
      <th> Correu electrònic </th>
      <td> <code>&lt;input type = "email"&gt;</code> </td>
      <td> Es pot mostrar un advertiment si s'introdueix un correu electrònic no vàlid </td>
    </tr>
    <tr>
      <th> Contrasenya </th>
      <td> <code>&lt;input type = "password"&gt;</code> </td>
      <td> Mostra els punts com a caràcters </td>
    </tr>
    <tr>
      <th> Número </th>
      <td> <code>&lt;input type = "number"&gt;</code> </td>
      <td> Es poden utilitzar les tecles de teclat amunt / avall </td>
    </tr>
    <tr>
      <th> Telèfon </th>
      <td> <code>&lt;input type = "tel"&gt;</code> </td>
      <td> Pot activar un emplenament automàtic </td>
    </tr>
    <tr>
      <th> Text de diverses línies </th>
      <td> <code>&lt;textarea&gt;&lt;/textarea&gt;</code> </td>
      <td> Es pot canviar la mida </td>
    </tr>
  </table>
</div>

Tot i que aquestes entrades tenen un aspecte molt semblant i permeten als usuaris introduir qualsevol tipus de text (fins i tot una entrada incorrecta), el seu tipus proporciona una **semàntica** específica a l’entrada, definint quin tipus d’informació es **suposa** que conté.

Els navegadors poden modificar lleugerament la interfície d'un control per augmentar la seva interactivitat o donar a conèixer quin tipus de contingut és _esperat_.

Per exemple, les entrades de contrasenya mostren punts en lloc de caràcters, i les entrades numèriques permeten augmentar / disminuir el seu valor mitjançant les tecles amunt i avall.

### Marcadors de posició

Les entrades de text poden mostrar un text de **marcador de posició** amb l'atribut `placeholder`, que desapareixerà tan bon punt s'introdueixi algun text.

```html
<input type = "text" placeholder = "Introduïu el vostre nom">
```

Si comenceu a escriure alguna cosa, veureu que desapareix el text _Introduïu el vostre nom_.

### Label

Com que els elements de formulari per si sols no són molt descriptius, solen anar precedits d'un **de text** amb l'etiqueta `label`.

```html
<label> Correu electrònic </label>
<input type = "email">
```

Tot i que els espais reservats ja ofereixen alguns indicis sobre el contingut que s’espera, les etiquetes tenen l’avantatge de mantenir-se visibles en tot moment i es poden utilitzar junt amb altres tipus de controls de formulari, com ara caselles de selecció o botons d’opció.

Tot i que podeu fer servir paràgrafs curts per descriure elements del formulari, l'ús de `<label>` és semànticament més vàlid perquè només existeixen dins dels formularis i es pot emparellar amb un control de formulari específic mitjançant l'atribut `for` i fent coincidir el seu valor amb el `id` de l'entrada.

```html
<label for = "first_name"> Nom </label>
<input id = "first_name" type = "text">
```

En fer clic a l’etiqueta, se centrarà l’entrada de text i es col·locarà el cursor de text a dins. Tot i que aquest emparellament sembla inútil, serà útil amb caselles de selecció i botons d’opció.

### Caselles de selecció

**Les caselles de selecció** són controls de formulari que només tenen 2 estats: marcats o no marcats. Bàsicament permeten a l'usuari dir "Sí" o "No" a alguna cosa.

```html
<input type = "checkbox"> Recordeu-me
```

Com que pot ser difícil fer clic a una casella de selecció petita, es recomana embolicar una `<label>` al voltant de la casella de selecció **i** la seva descripció.

```html
<label>
  <input type = "checkbox"> Accepto els termes
</label>
```

Podeu fer clic a _Accepto els termes_ per canviar la casella de selecció.

Per defecte, es desmarca una entrada de casella de selecció. Podeu marcar-lo com a marcat mitjançant l’atribut simplement anomenat `checked`.

```html
<label>
  <input type = "checkbox" checked> Utilitzar com a adreça de facturació
</label>
```

### Botons d'opció

Podeu presentar a l’usuari una **llista d’opcions** per triar mitjançant els botons d’opció.

Perquè aquest control de formulari funcioni, el vostre codi HTML ha de **agrupar** una llista de botons d'opció. Això s'aconsegueix utilitzant el mateix valor per a l'atribut "nom":

```html
<label> Estat civil </label>
<label>
  <input type = "radio" name = "status">
  Solter
</label>
<label>
  <input type = "radio" name = "status">
  Casat
</label>
<label>
  <input type = "radio" name = "status">
  Divorciada
</label>
<label>
  <input type = "radio" name = "status">
  Vidu
</label>
```

Com que tots els botons d'opció utilitzen el mateix _valor_ per al seu atribut `name` (en aquest cas el valor `status`), en seleccionar una opció es desseleccionaran totes les altres. Es diu que els botons d’opció són **mútuament excloents**.

#### Diferència entre botons d'opció i caselles de selecció

Tot i que hi ha una casella de selecció **sola**, els botons d'opció només poden aparèixer com a **llista** (el que significa tenir almenys _2_ opcions).

A més, fer clic a una casella de selecció és **opcional**, mentre que triar un dels botons d'opció és **obligatori**. Per això, és impossible desmarcar un botó d’opció tret que trieu una opció de germà. Però, al final, sempre es selecciona un dels botons d’opció.

### Menús desplegables

Si el nombre d'opcions per triar ocupa massa espai, podeu utilitzar els menús desplegables `<select>`.

Funcionen com botons de ràdio. Només el seu disseny és diferent.

```html
<select>
  <option> Gener </option>
  <option> Febrer </option>
  <option> Març </option>
  <option> Abril </option>
  <option> Maig </option>
  <option> Juny </option>
  <option> Juliol </option>
  <option> Agost </option>
  <option> Setembre </option>
  <option> Octubre </option>
  <option> Novembre </option>
  <option> Desembre </option>
</select>
```

#### Menús desplegables d'elecció múltiple

Si afegiu l'atribut `multiple`, podeu proporcionar la possibilitat de seleccionar diverses opcions.

```html
<label> Quins navegadors teniu? </label>
<select multiple>
  <option> Google Chrome </option>
  <option> Internet Explorer </option>
  <option> Mozilla Firefox </option>
  <option> Opera </option>
  <option> Safari </option>
</select>
```

Seleccioneu diverses opcions mantenint Ctrl i fent clic. Aquesta pot ser una bona alternativa a l’ús de diverses caselles de selecció seguides.

### Exemple: un formulari d'inscripció complet

```html
<form action = "/signup" method = "POST">
  <p>
    <label> Títol </label>
    <label>
      <input type = "radio" name = "title" value = "mr">
      Sr.
    </label>
    <label>
      <input type = "radio" name = "title" value = "mrs">
      mrs
    </label>
    <label>
      <input type = "radio" name = "title" value = "miss">
      Senyoreta
    </label>
  </p>
  <p>
    <label> Nom </label>
    <input type = "text" value = "first_name">
  </p>
  <p>
    <label> Cognom </label>
    <input type = "text" value = "last_name">
  </p>
  <p>
    <label> Correu electrònic </label>
    <input type = "email" value = "email">
  </p>
  <p>
    <label> Número de telèfon </label>
    <input type = "tel" value = "phone">
  </p>
  <p>
    <label> Contrasenya </label>
    <input type = "password" value = "password">
  </p>
  <p>
    <label> Confirmeu la vostra contrasenya </label>
    <input type = "password" value = "password_confirm">
  </p>
  <p>
    <label> País </label>
    <select>
      <option> Canadà </option>
      <option> França </option>
      <option> Alemanya </option>
      <option> Itàlia </option>
      <option> Japó </option>
      <option> Rússia </option>
      <option> Regne Unit </option>
      <option> Estats Units </option>
    </select>
  </p>
  <p>
    <label>
      <input type = "checkbox" value = "terms">
      Accepto els <a href="/terms"> termes i condicions </a>
    </label>
  </p>
  <p>
    <button>
      Registra't
    </button>
  </p>
</form>
```

Hi ha altres controls de formulari disponibles, però hem cobert els que més faran servir.

És hora de començar a **dissenyar** la nostra pàgina.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Busca quines diferència hi ha entre posar en un formulari el valor `GET` o `POST` a l'atribut `method`.
