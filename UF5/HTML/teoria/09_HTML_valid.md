# HTML vàlid

## Crear codi HTML correcte i comprovar-ho

Fins ara hem estat veient fragments de codi HTML aïllats. Però un **document HTML** (o pàgina web, vol dir el mateix) requereix una estructura específica per tal de ser **vàlid**.

Per què ens importa _validar_ un document HTML?

* **correcte**: el navegador _mostra correctament_ un document vàlid
* **depuració**: el codi HTML no vàlid pot provocar errors difícils de trobar
* **manteniment**: un document vàlid és més fàcil de _actualitzar_ més tard, fins i tot per algú altre

### DOCTYPE

La primera informació que cal proporcionar és el _tipus_ de document HTML que escrivim: el **DOCTYPE**.

Penseu en el tipus de document com la versió d’un cotxe al llarg dels anys: un Ford Fiesta comprat el 1986 era un Fiesta 2. Si en compreu un avui, és un Fiesta 7.

Abans hi havia diverses versions d’HTML que coexistien (XHTML i HTML 4.01 han estat estàndards competidors). Actualment, **HTML 5** és la norma.

Per indicar al navegador que el document HTML és un HTML 5, només cal que inicieu el document amb la línia següent:

```html
<!DOCTYPE html>
```

Això és. Només cal possar-ho-lo i oblidar-lo.

Us podeu preguntar per què aquest tipus de document HTML 5 no menciona el número "5". El W3C va pensar que les definicions anteriors de tipus de document eren massa confuses i van aprofitar per simplificar-la eliminant qualsevol menció a la versió HTML.

### L'element `<html>`

A part de la línia doctype, **tot** el vostre document HTML ha d'estar embolicat dins d'un element `<html>`:

```html
<!DOCTYPE html>
<html>
  <!-- La resta del vostre codi HTML és aquí -->
</html>
```

El `<html>` és tècnicament el **avantpassat** de tots els elements HTML.

### L'element `<head>`

De la mateixa manera que els atributs contenen informació addicional per a un element HTML, l'element `<head>` inclou informació addicional per a _tota_ la pàgina web.

Per exemple, el **títol** de la pàgina (que es mostra a la pestanya) es troba al `<head>`:

```html
<head>
  <title> El meu fabulós bloc </title>
</head>
```

Altres elements HTML poden aparèixer a `<head>` i _només_ a `<head>`:

* `<link>`
* `<meta>`
* `<style>`

### L'element `<body>`

Tot i que el `<head>` només conté metadades que no es volen mostrar en cap lloc (a part del `<title>`), l'element `<body>` és on escrivim tot el nostre contingut. Tot el que hi ha dins del `<body>` es **mostrarà** a la pestanya del navegador.

### Un document HTML vàlid complet

Combinant tots aquests requisits, podem escriure un document HTML senzill i vàlid:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset = "utf-8">
    <title>Hola!</title>
    <meta name="description" content="Un simple tutorial HTML i CSS">
  </head>
  <body>
    <p>Hola món!</p>
  </body>
</html>
```

Si veieu aquest exemple al navegador, veureu que:

* `Hola!`: s'escriu a la pestanya del navegador
* `Hello World!`: És l'únic text que es mostra a la finestra, perquè és l'únic contingut _dins_ del `<body>`

El <abbr title = "World Wide Web Consortium"> W3C </abbr> proporciona un <a href="https://validator.w3.org/#validate_by_input"> servei de validació de marques </a> per comprovar qualsevol document HTML per detectar errors i advertències. Una altre alternativa és el validador [https://html5.validator.nu/](https://html5.validator.nu/)

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Explica, amb les teves pròpies paraules, que vol dir **validar** i per quina raó és important fer-ho.
