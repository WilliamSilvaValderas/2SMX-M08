# La World Wide Web

## El web és una part d’Internet: la part HTTP

### Web

Hem vist com els ordinadors connectats a Internet es comuniquen en diferents idiomes anomenats **protocols**, per intercanviar correus electrònics, fitxers, missatges de xat ...

Un d’aquests protocols s’anomena **HTTP**. És el protocol amb el qual els equips comparteixen **pàgines web** entre si, com el que esteu llegint actualment.

El **web** és la part d’Internet on es comparteixen les pàgines web. Podeu saber que esteu navegant per la web si l'URL comença per 'http: // ¡ o per 'https: //'.

### Pàgina web

Una pàgina web és un **document** escrit en HTML que es comparteix a través del **web**.

Obriu aquests documents amb un **navegador web**.

Per accedir a una pàgina web podeu:

* escriviu el seu **URL**, com ara `http: // gegantsvilanovailageltru.cat / gegants-grossos.html`
* feu clic a un **enllaç**, com [aquest](http://gegantsvilanovailageltru.cat/gegants-grossos.html)

Com que recordar URL és feixuc, el lloc web es basa en **documents interconnectats** mitjançant enllaços per facilitar als usuaris la navegació per Internet.

### Lloc web

Un **lloc web** és simplement una col·lecció de pàgines web ubicades en un **mateix domini**.

* **Web** "http: //"
  * Lloc web `gegantsvilanovailageltru.cat`
    * Pàgina web `/ gegants-grossos.html`
    * Pàgina web `/ gegants-de-la-geltru.html`
    * Pàgina web `/ gegants-petits.html`

### Obrir una pàgina web al navegador

En navegar a <http://gegantsvilanovailageltru.cat/gegants-petits.html>, demaneu a un ordinador d'Internet que obtingui el document `gegants-petits.html`.

En aquest cas, el vostre ordinador és el **client**. Sol·liciteu al servidor _gegantsvilanovailageltru.cat_ (on es troba allotjat el lloc web) que obtingui el fitxer anomenat `gegants-petits.html`.

<div class = "table">
  <table>
    <tr>
      <th>
        <em> Client </em>
        <strong> El vostre ordinador </strong>
      </th>
      <td>
        <q> Hola ordinador gegantsvilanovailageltru.cat M'agradaria que el fitxer <code> gegants-petits.html </code> si us plau </q>
      </td>
    </tr>
    <tr>
      <th>
        <em> Servidor </em>
        <strong> L'equip gegantsvilanovailageltru.cat  </strong>
      </th>
      <td>
        <q> Permeteu-me comprovar si hi és ... </q>
      </td>
    </tr>
    <tr>
      <th>
        <em> Client </em>
        <strong> El vostre ordinador </strong>
      </th>
      <td>
        <q> D'acord, esperaré </q>
      </td>
    </tr>
    <tr>
      <th>
        <em> Servidor </em>
        <strong> L'equip gegantsvilanovailageltru.cat  </strong>
      </th>
      <td>
        <q> Ah, aquí ho teniu! Permeteu-me que us enviï. </q>
      </td>
    </tr>
    <tr>
      <th>
        <em> Client </em>
        <strong> El vostre ordinador </strong>
      </th>
      <td>
        <q> Ho he entès. Gràcies! </q>
      </td>
    </tr>
  </table>
</div>

El vostre navegador pot mostrar "web.html".

El fitxer **no està desat** al vostre ordinador: només es mostra temporalment mentre hi navegueu. Si aneu a <http://gegantsvilanovailageltru.cat/gegants-petits.html> més endavant, demanarà a l'ordinador gegantsvilanovailageltru.cat _de nou_ el mateix fitxer, si encara existeix. D’aquesta manera, us garanteix obtenir sempre la versió més recent del fitxer.

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Defineix que és la web
2. Què és una pàgina web
3. Què és un lloc web
4. Defineix que és un navegador
