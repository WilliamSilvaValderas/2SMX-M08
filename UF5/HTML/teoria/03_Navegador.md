# Un navegador

## Un navegador és un visor de documents. Quin tipus de document? Pàgines web

Actualment utilitzeu un _navegador web_ per llegir aquesta _pàgina web_ escrita en _HTML_.

### Documents HTML

**Les pàgines web** són **documents HTML**, com altres fitxers de l'ordinador. Només són fitxers de text amb una extensió `.html`.

A l’ordinador, probablement tingueu diferents **tipus** de fitxers:

* `.jpg` per a imatges
* `.mp3` per a la música
* `.avi` per als vídeos
* `.doc` per als documents de Word
* `.xls` per als fulls de càlcul d'Excel

Cadascun d'aquests _tipus_ de fitxers els pot obrir un **programa** específic. Alguns d'aquests programes només poden _obrir_ aquests fitxers, mentre que d'altres poden _obrir_ i _creant_ fitxers.

A Windows o Mac, per defecte, les **extensions de fitxer** estan ocultes. En aquest curs ens cal que siguin visibles. Per tant, seguiu aquestes instruccions per mostrar les extensions de fitxer:

* **Windows**: [Mostra o oculta les extensions de nom de fitxer](https://windows.microsoft.com/en-us/windows/show-hide-file-name-extensions)

* **Mac**: [Mostra i oculta les extensions de nom de fitxer](https://support.apple.com/kb/PH10845?locale=en_US)

Per exemple:

* L'VLC pot **obrir fitxers** `.mp3` però no els pot crear.
* Tanmateix, Microsoft Word pot **obrir** i **crear fitxers** `.doc`.

<div class = "table">
  <table>
    <tr>
      <th> Programa </th>
      <th> Tipus </th>
      <th>
        Es poden <em> obrir </em> aquests fitxers
      </th>
      <th>
        També podeu <em> crear </em> aquests fitxers?
      </th>
    </tr>
    <tr>
      <td> Microsoft Word </td>
      <td> Editor de paraules </td>
      <td>
        <code> .doc </code>
        <code> .docx </code>
      </td>
      <td class = "yes"> <span> Sí </span> </td>
    </tr>
    <tr>
      <td> Pinta </td>
      <td> Gràfics </td>
      <td>
        <code> .jpg </code>
        <code> .gif </code>
        <code> .bmp </code>
      </td>
      <td class = "yes"> <span> Sí </span> </td>
    </tr>
    <tr>
      <td> VLC </td>
      <td> Reproductor de vídeo </td>
      <td>
        <code> .avi </code>
        <code> .mpg </code>
      </td>
      <td class = "no"> No </td>
    </tr>
    <tr>
      <td> iTunes </td>
      <td> Reproductor de música </td>
      <td>
        <code> .mp3 </code>
        <code> .wav </code>
        <code> .aiff </code>
      </td>
      <td class = "no"> No </td>
    </tr>
    <tr>
      <td> Firefox </td>
      <td> Navegador web </td>
      <td>
        <code> .html </code>
      </td>
      <td class = "no"> No </td>
    </tr>
    <tr>
      <td> Bloc de notes </td>
      <td> Editor de text </td>
      <td>
        <code> .text </code>
        <code> .html </code>
      </td>
      <td class = "yes"> <span> Sí </span> </td>
    </tr>
  </table>
</div>

El programa utilitzat per **obrir** documents HTML és un **navegador**, com Firefox o Google Chrome.
El programa utilitzat per **crear** documents HTML és un **editor de text**, com Sublime Text o [Visual Studio Code](https://code.visualstudio.com/)

### codi font HTML

El codi HTML té aquest aspecte:

```html
<p> Hola món </p>
```

Aquest codi s’escriu amb un **editor de text**. Podeu veure les etiquetes `<p>` i `</p>` que signifiquen **paràgraf**.

Quan les obre un **navegador**, aquestes etiquetes **no es mostren**, sinó que **són interpretades** pel navegador:

<table bgcolor="grey"><tr><td>
  <p> Hola món </p>
</td></tr></table>

El navegador veu les etiquetes `<p>` i `</p>` i entén que "Hello World" és un **paràgraf**.

Recordeu que un document HTML es pot obrir de **2 maneres**:

* per un **editor de text** que _visualitza_ el codi font
* per un **navegador** que _interpreta_ el codi font

### Llista de navegadors web

Com que el web s'ha convertit en l'ús principal d'Internet, tots els ordinadors i telèfons intel·ligents tenen un navegador predeterminat instal·lat.

Els més populars són:

* **Chrome** https://www.google.com/chrome/
* **Firefox** https://www.mozilla.org/firefox/
* **Internet Explorer** https://www.microsoft.com/download/internet-explorer.aspx
* **Opera** https://www.opera.com/
* **Safari** https://www.apple.com/safari/

### Llista d'editors de text

Els més populars són:

* **Bloc de notes ++** https://notepad-plus-plus.org/
* **Text sublim** https://www.sublimetext.com/
* **Visual Studio Code** https://code.visualstudio.com/

N’haureu d’instal·lar un per **escriure** HTML i CSS.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Quina diferència hi ha entre obrit un document HTML amb un editor de text i amb un navegador?
2. Quin editor de text fem servir en aquest mòdul? Quina llicència té? Amb quins sistemes operatius funciona?
