# La Internet

## Una xarxa gegant d'ordinadors

Internet no és el mateix que el web. Internet és més gran, més antic i més variat.

Imagineu com les **carreteres** estan _interconectades_ a tot el món: els carrers petits es connecten amb carrils urbans que es converteixen en carreteres regionals que després es fusionen amb carreteres nacionals i internacionals. Podeu conduir des de casa vostra a qualsevol altra casa del món. Tampoc no hi ha cap centre real en aquesta xarxa viària.

Internet és similar. Però en lloc de carreteres, són **cables**. I en lloc de cases, són **ordinadors**. I en lloc de cotxes que viatgen per aquesta xarxa, és **informació**.

Es va inventar el 1969 per connectar ordinadors a tot USA. Avui dia, _bilions_ de dispositius (inclosos els ordinadors, portàtils, telèfons mòbils, televisors, neveres ...) estan **interconnectats**.

### Client i servidor

Normalment, una connexió a Internet es fa només entre **2** equips:

* un que **tingui** la informació (el _servidor_)
* un que **la vulgui** (el _client_).

Un **client** és un programa que pot adoptar diverses formes:

* un navegador web (com Firefox)
* un client de correu electrònic (com l'Outlook o Thunderbird)
* una aplicació de missatgeria (com Whatsapp)
* un servei de transmissió de vídeo (com Netflix)

Cadascun d'aquests programes recuperarà informació d'un **servidor**, on s'emmagatzema alguna cosa (un lloc web, els vostres correus electrònics, missatges, pel·lícules). Tot i que els programes clients també envien informació al servidor, normalment no l’emmagatzemen, mentre que els servidors sí.

Un **servidor** es pot considerar un ordinador _dedicat_ sempre connectat a Internet, l'únic propòsit del qual és **lliurar** contingut.

Tot i que qualsevol dispositiu connectat a Internet pot ser alhora client i servidor, la majoria de dispositius que fem servir es consideren **cliens**, perquè només recuperem dades i no en proporcionem cap.

### Adreça IP

Com cada casa té una adreça postal específica i única, cada ordinador connectat a Internet rep una **adreça IP** per tal de ser identificat a la xarxa.

Una adreça IP, amb la versió més comu, la 4, sembla una combinació de 4 números: "62.97.127.126".

### Dominis

Tot i que les adreces IP són útils perquè els equips es distingeixin gràcies a la seva singularitat, són difícils de llegir i recordar per a nosaltres, els humans.

És per això que es van crear **dominis** el 1985. _Associen_ una adreça IP com "62.97.127.126" amb una cadena de **text** com a "cruzroja.es". Com a resultat, tots dos són **intercanviables**: podeu anar a <http://62.97.127.126> o <http://cruzroja.es> i acabar al mateix lloc web.

Un domini té **3** parts, que es llegeixen de dreta a esquerra:

* **Domini de primer nivell** (o TLD): n'hi ha de genèrics (".com", ".org", ".net") i específics del país (".us", ".nl", ".fr").
* **Nom de domini**: un nom com a "wikipedia" o "cruzroja", que pot incloure lletres, números, però sense espai ni punt.
* **Subdomini** (opcional). Tot i que aquesta tercera part és opcional, la majoria de llocs web utilitzen `www` com a subdomini predeterminat.

Penseu en els dominis com una forma de **anomenar** els equips connectats a Internet.

_Com puc comprar un domini?_
En realitat, no _compreu un domini_, però sí que **el llogueu** a qui estigui gestionant el TLD que voleu.
Les empreses que gestionen dominis d'Internet s'anomenen **registradors de dominis**. Exemples d'aquest tipus d'empreses són [Namecheap](https://www.namecheap.com/) i [GoDaddy](https://www.godaddy.com/).

### Protocols

El propòsit d’interconectar tots aquests equips és que interactuïn entre ells. I com els humans parlem en diferents _idiomes_, els ordinadors d'Internet parlen mitjançant **protocols**.

Cadascun d'ells té un propòsit diferent:

<div class = "table">
  <table>
    <tr>
      <th> Protocol </th>
      <th> S'utilitza per a </th>
      <th> Creat a </th>
    </tr>
    <tr>
      <td>
        <abbr title = "File Transfer Protocol"> FTP </abbr>
      </td>
      <td> Transferència de fitxers </td>
      <td> 1971 </td>
    </tr>
    <tr>
      <td>
        <abbr title = "Simple Mail Transfer Protocol"> SMTP </abbr>
      </td>
      <td> Enviament de correus electrònics </td>
      <td> 1971 </td>
    </tr>
    <tr>
      <td>
        <abbr title = "Internet Message Access Protocol"> IMAP </abbr>
      </td>
      <td> Rebre correus electrònics </td>
      <td> 1986 </td>
    </tr>
    <tr>
      <td>
        <abbr title = "Internet Relay Chat"> IRC </abbr>
      </td>
      <td> Xat </td>
      <td> 1988 </td>
    </tr>
    <tr>
      <td>
        <abbr title = "HyperText Transfer Protocol"> HTTP </abbr>
      </td>
      <td> Navegació de documents HTML (pàgines web) </td>
      <td> 1989 </td>
    </tr>
  </table>
</div>

### URL

Ara que hem vist com dominis i protocols, podem construir un **URL**: un **U** niform **R** esource **L** ocator.

Per exemple, l'URL d'una pàgina és `http: // gegantsvilanovailageltru.cat / gegants-grossos.html` i es pot dividir en 3 parts:

* `http: //` és el **protocol**
* `gegantsvilanovailageltru.cat` és el **domini**
* `/ gegants-grossos.html` és el **camí**

Aquest URL és **única** i defineix:

* _on_ per trobar alguna cosa a Internet `gegantsvilanovailageltru.cat / gegants-grossos.html`
* _com_ se suposa que l'ordinador l'ha de llegir `http: //`

Els URL poden tenir un aspecte més complex. Podeu llegir sobre [les parts que composen una URL](https://edytapukocz.com/url-partes-ejemplos-facil/).

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Definir Internet, Protocol, Adreça IP
2. Coneixer els protocols FTP, SMTP, IMAP, IRC, HTTP
3. Identificar les parts d'una URL
4. Definir que és un domini, identificar les parts d'un domini i saber els diferents tipus de dominis que hi ha.
