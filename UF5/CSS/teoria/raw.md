



---
maquetació: post
títol: "CSS <strong>visualització</strong>"
subtítol: "Canviar el <strong>tipus</strong> d'un element HTML"
secció: css
---

Hem vist com hi ha principalment [2 tipus d'elements HTML](/html-block-inline.html): elements **block-level** i **inline**. També hem esmentat algunes alternatives, com ara **list-item** o **table-cell**.

La propietat `display` permet canviar el _tipus_ de l'element HTML. De manera predeterminada, un paràgraf `<p>` (un element **nivell de bloc**) tindrà un valor de `visualització' predeterminat de `block`, però es pot representar com a **inline**:

```css
p{ visualització: en línia;}
```

### Per què no utilitzar un element HTML en línia, com ara `<span>` llavors?

Perquè trieu un element HTML pel seu **significat**, no per la seva representació. Si hem decidit que un paràgraf és el que millor s'adapta al nostre contingut, no hem de canviar l'etiqueta _només amb finalitats d'estil_. CSS és aquí per tenir cura de l'estil.

En resum, `display` permet alterar el **tipus** d'un element _sense_ canviar-ne el **significat**.

Cada opció de "visualització" té comportaments de representació específics:

* `block` ocuparà tota l'amplada disponible
* `inline` actuarà com a text senzill
* `inline-block` és, com el seu nom indica, un compost de bloc i comportament en línia, una opció _"el millor dels dos mons"_
* `list-item` és similar a `block` ja que ocupa tota l'amplada disponible, però mostra una vinyeta addicional
* "taula", "fila de taula" i "cel·la de taula" tenen un comportament molt específic, encara que inesperat, que permet dissenys més interessants

### visualització: bloqueig

Això convertirà qualsevol element en un element **block**.

Aquesta tècnica s'utilitza sovint als **enllaços** per augmentar la seva zona de clic, que es pot avaluar fàcilment establint un color de fons.

```css
.menu a{ fons: vermell; color: blanc;}
```

```html
<ul class="menu">
  <li>
    <a>Inici</a>
  </li>
  <li>
    <a>Funcions</a>
  </li>
  <li>
    <a>Preus</a>
  </li>
  <li>
    <a>Quant a</a>
  </li>
</ul>
```

<div class="resultat">
  <ul>
    <li>
      <a style="background: red; color: white;">Inici</a>
    </li>
    <li>
      <a style="background: red; color: white;">Funcions</a>
    </li>
    <li>
      <a style="background: red; color: white;">Preus</a>
    </li>
    <li>
      <a style="background: red; color: white;">Quant a</a>
    </li>
  </ul>
</div>

Si convertim aquests enllaços en **blocs**, augmentarem la seva àrea objectiu:

```css
.menu a{ fons: vermell; color: blanc; mostrar: bloc;}
```

<div class="resultat">
  <ul>
    <li>
      <a style="background: red; color: white; display: block;">Inici</a>
    </li>
    <li>
      <a style="background: red; color: white; display: block;">Funcions</a>
    </li>
    <li>
      <a style="background: red; color: white; display: block;">Preus</a>
    </li>
    <li>
      <a style="background: red; color: white; display: block;">Quant a</a>
    </li>
  </ul>
</div>


### pantalla: en línia

Això converteix qualsevol element en elements **inline**, com si només fossin un simple **text**.

Sovint s'utilitza per crear **navegacions horitzontals**, on els **elements de llista** són útils semànticament però no visualment.

```html
<ul class="menu">
  <li>
    <a>Inici</a>
  </li>
  <li>
    <a>Funcions</a>
  </li>
  <li>
    <a>Preus</a>
  </li>
  <li>
    <a>Quant a</a>
  </li>
</ul>
```

<div class="resultat">
  <ul>
    <li>
      <a>Inici</a>
    </li>
    <li>
      <a>Funcions</a>
    </li>
    <li>
      <a>Preus</a>
    </li>
    <li>
      <a>Quant a</a>
    </li>
  </ul>
</div>

```css
.menu li{ mostrar: en línia;}
```

<div class="resultat">
  <ul>
    <li style="display: inline;">
      <a>Inici</a>
    </li>
    <li style="display: inline;">
      <a>Funcions</a>
    </li>
    <li style="display: inline;">
      <a>Preus</a>
    </li>
    <li style="display: inline;">
      <a>Quant a</a>
    </li>
  </ul>
</div>

### visualització: element de llista

Els únics elements HTML que es mostren com a "element de llista" són (no és sorprenent) els **elements de la llista** `<li>`, però també les **descripcions de definicions** `<dd>`.

Un element de llista es representa amb un punt (si està en una llista no ordenada `<ul>`) o amb un número incremental (si es troba dins d'una llista ordenada `<ol>`).

Com que la representació d'aquestes vinyetes i números varia segons els navegadors, i també és difícil d'estilitzar en CSS, la regla `display: list-item` no s'utilitza mai. De fet, és comú que els `<li>`s es representin com a `display: block` o `display: inline`, ja que són més flexibles a l'estil.

### pantalla: cap

Si apliqueu `display: none;` a un element HTML, l'elimina de la vostra pàgina web, com si mai hagués existit al vostre codi.

```css
.gone-baby-gone{ mostrar: cap;}
```

```html
<p>He sentit algú parlar?</p>
<p class="gone-baby-gone">Hahahahahah</p>
<p>He d'estar somiant...</p>
```

<div class="resultat">
  <p>He sentit algú parlar?</p>
  <p style="display: none;">Hahahahahah</p>
  <p>He d'estar somiant...</p>
</div>

Hi ha 3 paràgrafs al codi, però només n'apareixen 2, com si el 2n no hagués existit mai.

### visibilitat: oculta

La propietat CSS `visibility` és lleugerament semblant a `display`. Aplicar `visibility: hidden;` _amaga_ un element de la vostra pàgina, però només el converteix en **invisible**: encara ocupa l'espai que se suposava.

```css
.hollow-man{ visibilitat: oculta;}
```

```html
<p>Tan lluny de mi </p>
<p class="hollow-man">Fins ara no puc veure'l</p>
<p class="hollow-man">Tan lluny de mi</p>
<p class="hollow-man">Estàs tan lluny de mi</p>
<p>Estàs tan lluny...</p>
```

<div class="resultat">
  <p>Tan lluny de mi </p>
  <p style="visibility: hidden;">Fins ara no puc veure'l</p>
  <p style="visibility: hidden;">Tan lluny de mi</p>
  <p style="visibility: hidden;">Estàs tan lluny de mi</p>
  <p>Estàs tan lluny...</p>
</div>

Hi ha 5 paràgrafs al codi, només n'apareixen 2, però l'espai que els paràgrafs ocults haurien d'ocupar _se suposa que_ encara hi és, però no els podeu veure.
---
maquetació: post
títol: "CSS <strong>alçada</strong> i <strong>amplada</strong>"
subtítol: "Configuració de dimensions <strong>fixes</strong> als vostres rectangles"
secció: css
---

Les dimensions (o alçada i amplada) d'un element són **dinàmiques**, ja que fluctuen per adaptar-se al contingut. D'alguna manera és possible establir dimensions **específiques**.

```css
blockquote{ amplada: 600px;}
```

La cita de bloc no ocuparà tota l'amplada disponible, però es mantindrà de 600 píxels d'amplada **en qualsevol situació**:

* si la finestra del navegador és menys ampla que 600 píxels, mostrarà una barra de desplaçament horitzontal
* si la finestra del navegador és més ampla que 600 px, la cita de bloc es mantindrà 600 px d'ample i no ocuparà tot l'espai

Com que només hem establert l'amplada, la cita de bloc continua sent fluida en **altura**: l'alçada es converteix en la dimensió variable per adaptar-se al contingut de la cita de bloc.

### Configuració tant d'alçada com d'amplada

En establir les dimensions d'un element, es mantindrà fix sense importar la longitud del seu contingut.

Què passa si el contingut és més llarg del que pot contenir l'element?
{: .question}

Com que evitem que l'element alteri dinàmicament les seves dimensions, hi ha la possibilitat que el contingut sigui més llarg del que l'element s'adapta i que, posteriorment, es **desbordi**.

El comportament predeterminat pot ser sorprenent: el contingut es mostrarà igualment!

```css
blockquote{ fons: groc; alçada: 50px; amplada: 100 píxels;}
```

```html
<blockquote>El contingut... troba una manera</blockquote>
```

<div class="resultat">
  <blockquote style="background: yellow; height: 50px; width: 100px;">El contingut és... troba una manera</blockquote>
</div>

### Desbordament de CSS

La propietat CSS `overflow` ens permet gestionar el cas que el contingut sigui més llarg que el seu contenidor.

El valor per defecte és `visible`: el contingut es mostrarà de totes maneres, perquè _"Per què voldríeu evitar que l'usuari llegeixi contingut si està present al codi?"_. Podeu considerar **HTML com a prevalent a CSS**.

En aplicar `overflow: hidden;`, simplement _prohibeu_ que es vegi qualsevol contingut desbordat.

<div class="resultat">
  <blockquote style="background: yellow; height: 50px; overflow: hidden; width: 100px;">El contingut és... troba una manera</blockquote>
</div>

Si voleu que el vostre contingut es desbordi, però encara voleu que sigui accessible, podeu decidir mostrar barres de desplaçament aplicant `desbordament: desplaçament`.

<div class="resultat">
  <blockquote style="background: yellow; height: 50px; overflow: scroll; width: 100px;">El contingut és... troba una manera</blockquote>
</div>

Una millor opció és utilitzar `overflow: auto`, ja que les barres de desplaçament només apareixeran _si_ el contingut està desbordant, però romandran ocultes fins aleshores.

<div class="resultat">
  <blockquote style="background: yellow; height: 50px; overflow: auto; width: 100px;">El contingut és... troba una manera</blockquote>
</div>

### Compte amb les dimensions fixes

Sovint es requereix l'aplicació de dimensions específiques perquè un disseny sembli visualment atractiu, però pot tenir conseqüències no desitjades. En aquest sentit:

* Assegureu-vos que el vostre contingut no es desbordi
* si ho fa, utilitzeu "overflow: hidden" o "overflow: auto" per evitar que el vostre disseny es trenqui











---
maquetació: capítol
title: "CSS <strong>Posicionament</strong>"
subtítol: "Trencant el <strong>flux</strong>"
secció: css
---

Fins i tot sense aplicar cap CSS, un document HTML ja té **estil**. El seu contingut segueix un **Flux** natural, depenent directament de l'estructura HTML.

Però les pàgines web sovint volen que els elements es **posicionin** d'una manera determinada per adaptar-se a necessitats de disseny particulars, la qual cosa requereix **trencar** el flux.
---
maquetació: post
títol: "El <strong>Flux</strong>"
subtítol: "El comportament <strong>predeterminat</strong> d'una pàgina web"
secció: css
---

Un document HTML és un document **viu**

Fins i tot sense aplicar cap CSS, un document HTML ja té les seves pròpies regles:

* **fluidesa**: com s'adapta el contingut a les dimensions del navegador
* **ordenació**: en què apareixen els elements d'ordre
* **apilament**: com apareixen els elements uns sobre els altres

Aquest comportament natural és **lògic**.

### Fluidesa

En HTML, el **contingut** és King.

Tots els elements del "bloc" són **fluids**. Naturalment, adaptaran el seu disseny per adaptar-se al seu contingut interior:

* **amplada: 100%**
un bloc ocuparà tota l'amplada disponible
* **l'ajust de línia**
si el contingut en línia d'un bloc no encaixa en una sola línia, continuarà en una línia nova
* **altura: automàtica**
l'alçada d'un bloc varia automàticament per coincidir amb la mida del seu contingut

<div class="result" id="resultat-fluidesa">
  <div>
    Un element de bloc omplirà tota l'<strong>amplada</strong> disponible, mentre que la seva <strong>alçada</strong> variarà automàticament segons la mida del seu contingut.
  </div>
  <div>
    Aquest element serà empès cap avall en funció de l'alçada dels seus predecessors.
  </div>
</div>

<style type="text/css">
#resultat-fluidesa{ alçada: 450px; amplada màxima: 800 píxels;}
#resultat-fluiditat div{ fons: corall; farciment: 20px;}
#resultat-fluiditat div:first-child{ fons: aiguamarina mitjana; animació: expandir 3s altern infinits tots dos;}

@fotogrames clau expandir{
  0% { amplada: 100%;}
  100%{ amplada mínima: 100 píxels; amplada: 50%;}
}
</estil>

* Un "bloc" és per defecte en **amplada total**
* La seva **altura** és l'alçada del seu contingut

### Encàrrec

Els elements HTML es mostren en l'**ordre** en què s'escriuen **al codi**.
Primer al codi -> primer al navegador.

Cada <code>bloc</code> apareix en l'ordre en què apareixen al codi HTML, de <strong>a dalt</strong> a <strong>a baix</strong>.

```html
<p>Primer</p>
<p>Segon</p>
<p>Tercer</p>
<p>Quart</p>
<p>Cinquè</p>
```

<div class="resultat">
  <p>Primer</p>
  <p>Segon</p>
  <p>Tercer</p>
  <p>Quart</p>
  <p>Cinquè</p>
</div>

### Apilament

Un navegador té **3 dimensions**.

Cada element HTML pertany a una **capa** imaginària.

L'**ordre de pila** depèn de com estiguin **imbricats** els elements: els elements secundaris apareixen **a sobre** dels seus respectius pares.

* Cada element **imbricat** apareix _a la part superior_ del seu pare.
* El **més profund** a la jerarquia, el _més_alt_ a la pila.

```html
<div>
  Aquest pare està enrere
  <p>
    Aquest fill imbricat apareix <strong>a sobre</strong> del seu pare
  </p>
</div>
```

<div class="resultat">
  <div style="background: midnightblue; color: blanc; farciment: 20px;">
    Aquest pare està enrere
    <p style="background: mediumseagreen; padding: 20px;">
      Aquest fill imbricat apareix <span style="background: crimson; color: white; padding: 2px 5px;">a la part superior</span> del seu pare
    </p>
  </div>
</div>

### Trencant el flux

Tot i que el comportament predeterminat del navegador és _eficient_, pot ser que no sigui _suficient_ per a les vostres necessitats de disseny.

Diverses propietats CSS permeten **interrompre** el flux:

* "altura" i "amplada" poden alterar la **fluidesa** d'un element
* `float` **pertorba** el comportament d'un element així com el seu entorn
* `posició` `absoluta` i `fixa` **elimina** un element del flux
* `z-index` pot alterar l'ordre en què els elements s'apilen**
---
maquetació: post
títol: "CSS <strong>posició</strong>"
subtítol: "Va a ser manual"
secció: css
---

La propietat CSS `position` és versàtil i potent. Permet _establir_ o _alterar_ la posició d'un element. Té 4 **valors** possibles:

* `static` (valor per defecte)
* 'parental'
* 'absolut'
* 'fixat'

Sovint s'utilitza juntament amb les 4 propietats de **coordenades**:

* 'esquerra'
* 'correcte'
* 'superior'
* 'inferior'

### estàtic

Aquest és el valor de posició **predeterminat**: els elements estàtics només segueixen el [flux natural](css-the-flow.html). No es veuen afectats per cap valor "esquerra", "dreta", "superior" o "inferior".

### relatiu

Quan la "posició" s'estableix com a **relativa**, un element es pot moure segons la seva **posició actual**.

```html
<p>Bé, en Ja hauria de saber el seu propi negoci, vaig pensar, i així vaig agafar la llança i em vaig enfilar cap a l'home vermell tan ràpidament com vaig poder, tan lluny com jo dels meus avantpassats simics</p>
<p>M'imagino que el sític lent, com l'anomenava Ja, es va adonar de sobte de les nostres intencions i que era molt probable que perdés tot el menjar en comptes de doblar-lo com esperava</p>
<p>Quan em va veure pujar per aquella llança, va deixar escapar un xiulet que va fer tremolar bastant el terra i va venir carregant darrere meu a un ritme fantàstic</p>
```

```css
p{ vora: 1px blau sòlid;}
```

<div class="resultat">
  <p style="border: 1px solid blue;">Bé, en Ja hauria de saber el seu propi negoci, vaig pensar, i així vaig agafar la llança i em vaig enfilar cap a l'home vermell tan ràpidament com vaig poder, sent tan lluny del meu avantpassats simis com sóc jo</p>
  <p style="border: 1px solid blue;">M'imagino que el sític lent, com l'anomenava Ja, es va adonar de sobte de les nostres intencions i que era molt probable que perdés tot el menjar en comptes de doblar-lo com havia esperat. </p>
  <p style="border: 1px solid blue;">Quan em va veure pujar per aquella llança, va deixar escapar un xiulet que va fer tremolar bastant el terra i va venir carregant darrere meu a un ritme fantàstic</p>
</div>

Mourem el **segon** paràgraf:

```html
<p>Bé, en Ja hauria de saber el seu propi negoci, vaig pensar, i així vaig agafar la llança i em vaig enfilar cap a l'home vermell tan ràpidament com vaig poder, tan lluny com jo dels meus avantpassats simics</p>
<p class="second">M'imagino que el sític lent, com l'anomenava Ja, es va adonar de sobte de les nostres intencions i que era molt probable que perdés tot el menjar en comptes de doblar-lo com havia esperat</p>
<p>Quan em va veure pujar per aquella llança, va deixar escapar un xiulet que va fer tremolar bastant el terra i va venir carregant darrere meu a un ritme fantàstic</p>
```

```css
.segon{ posició: relatiu; color de la vora: vermell; esquerra: 20px; superior: 10 píxels;}
```

<div class="resultat">
  <p style="border: 1px solid blue;">Bé, en Ja hauria de saber el seu propi negoci, vaig pensar, i així vaig agafar la llança i em vaig enfilar cap a l'home vermell tan ràpidament com vaig poder, sent tan lluny del meu avantpassats simis com sóc jo</p>
  <p style="border: 1px solid red; position: relative; left: 20px; top: 10px;">M'imagino que el sític lent, com l'anomenava Ja, es va adonar de sobte de les nostres intencions i que era molt probable que perdés. tot el seu àpat en comptes de doblar-lo com havia esperat</p>
  <p style="border: 1px solid blue;">Quan em va veure pujar per aquella llança, va deixar escapar un xiulet que va fer tremolar bastant el terra i va venir carregant darrere meu a un ritme fantàstic</p>
</div>

El paràgraf vermell s'ha mogut 20 píxels **des de l'esquerra** i 10 píxels **des de la part superior**, en relació a la seva posició _natural_, on se suposa que es troba.

Observeu com els paràgrafs blaus no s'han mogut gens. Mitjançant el posicionament relatiu, el paràgraf vermell es pot moure lliurement sense interrompre el disseny. L'única cosa fora de lloc és _si mateix_. Tots els altres elements **no sé que l'element s'ha mogut**.

### absolut

Quan la "posició" s'estableix en **absolut**, un element es pot moure segons el **primer avantpassat posicionat**.

#### "Posicionat? Què és un element _posicionat_?"

Un element **posicionat** és aquell que el valor de la "posició" és "relatiu", "absolut" o "fix". Així, tret que la posició no s'estableixi _o_ estàtica, un element es **posiciona**.

La característica d'un element _posicionat_ és que pot actuar com a **punt de referència per als seus elements fills**.

Imaginem una **jerarquia** simple:

```html
<secció>
  Estic en posició relativa.
  <p>
    Estic en posició absoluta!
  </p>
</secció>
```

```css
secció {
  fons: or;
  alçada: 200px;
  farciment: 10px;
  posició: relatiu; /* Això converteix la <secció> en un punt de referència per a la <p> */
}

p {
  fons: verd llima;
  color: blanc;
  farciment: 10px;
  posició: absoluta; /* Això fa que <p> es pugui moure lliurement */
  inferior: 10px; /* 10 píxels des de la part inferior */
  esquerra: 20px; /* 20 píxels des de l'esquerra */
}
```

<div class="resultat">
  <section style="background: gold; height: 200px; margin: 1em 0; padding: 10px; position: relative;">
    Estic en posició relativa.
    <p style="background: limegreen; bottom: 10px; color: white; left: 20px; margin: 0; farcit: 10px; position: absolute;">
      Estic en posició absoluta!
    </p>
  </secció>
</div>

La secció groga té una alçada de `200 px` i la seva posició s'estableix en `relativa', la qual cosa la converteix en un **punt de referència per a tots els meus elements secundaris**.

Com que la posició del paràgraf verd s'estableix en "absoluta", es pot moure lliurement _segons_ la secció groga. En establir els valors "inferior" i "esquerra", es mourà _des_ de la cantonada inferior esquerra.

#### Què passa si posem tant a l'esquerra com a la dreta?

Si l'"amplada" no està establerta, l'aplicació de "esquerra: 0" i "dreta: 0" **estirarà l'element a tota l'amplada**. És l'equivalent a configurar "esquerra: 0" i "amplada: 100%".

Si s'estableix l'amplada, es descarta el valor "correcte".

### arreglat

Quan la "posició" s'estableix a **fixa**, actua com a **absoluta**: podeu establir les coordenades esquerra/dreta i superior/inferior.

L'única diferència és que el **punt de referència és la finestra gràfica**. Significa que un element fix _no es desplaçarà_ amb la pàgina; està _fixat_ a la pantalla.---
maquetació: post
títol: "CSS <strong>float</strong>"
subtítol: "La propietat més imprevisible"
secció: css
---

Darrere de la paraula "flotar", un mar infinit de possibilitats (i males conductes).

"float" és probablement el concepte CSS més difícil d'entendre. El seu comportament pot ser intrigant, inesperat i màgic. Probablement perquè, de totes les propietats de _posicionament_ que hi ha, és la que més _influeix_ en el seu **entorn**.

En altres paraules, aplicar un flotant no només modifica l'element sobre el qual s'aplica ** sinó que també altera els seus avantpassats, germans, descendents i elements següents**.

"float" només pot tenir un d'aquests 3 valors:

* `esquerra` i `dreta` converteix un element en un de **flotant**
* "cap" elimina l'aspecte flotant

### Quan s'ha d'utilitzar el flotador

El propòsit de **flotar** un element és **empènyer-lo cap a un costat** i fer que el text **s'envolti**.

Per explicar el comportament, utilitzem un exemple comú: flotar una imatge dins d'un paràgraf.

```html
<p>
  <img src="https://placehold.it/150x150">
  Les campanes de l'església veïna van fer un rebombori, un carro conduït descuidament va esclatar, entre crits i maleficis, contra l'abeurador del carrer. Uns llums grocs enfermizos anaven i venien a les cases, i alguns dels taxis que passaven lluïen llums sense apagar. I per sobre, l'alba es feia més brillant, clara, estable i tranquil·la.
</p>
```

<div class="resultat">
  <p style="background: gold; padding: 10px; width: 600px;">
    <img src="https://placehold.it/150x150">
    Va ser mentre el rector s'havia assegut i em parlava tan salvatgement sota la bardissa dels prats plans prop d'Halliford, i mentre el meu germà mirava com els fugitius passaven pel pont de Westminster, els marcians havien reprès l'ofensiva. Pel que es pot comprovar a partir dels relats contradictoris que s'han fet, la majoria d'ells van romandre ocupats amb els preparatius a la fossa de Horsell fins a les nou d'aquella nit, afegint-se a una operació que va desenganxar grans volums de fum verd.
  </p>
</div>

El problema a l'hora d'inserir una imatge dins d'un text és que **una imatge ha d'encaixar en una única línia de text** i, per tant, _estendrà_ l'alçada de la línia on es troba. En el nostre cas, la nostra imatge és de 150 píxels d'alçada.

El que volem és embolicar el text al voltant de la imatge:

```css
img{ flotant: esquerra;}
```

<div class="resultat">
  <p style="background: gold; padding: 10px; width: 600px;">
    <img style="float: left;" src="https://placehold.it/150x150">
    Va ser mentre el rector s'havia assegut i em parlava tan salvatgement sota la bardissa dels prats plans prop d'Halliford, i mentre el meu germà mirava com els fugitius passaven pel pont de Westminster, els marcians havien reprès l'ofensiva. Pel que es pot comprovar a partir dels relats contradictoris que s'han fet, la majoria d'ells van romandre ocupats amb els preparatius a la fossa de Horsell fins a les nou d'aquella nit, afegint-se a una operació que va desenganxar grans volums de fum verd.
  </p>
</div>

Com podeu veure, la imatge es **empeny cap a l'esquerra**, i el text que segueix només s'envolta al voltant de la imatge:

* primer, el text es mou cap a la dreta, _al costat_ de la imatge
* aleshores, quan hi hagi espai disponible a sota de la imatge, el text omplirà aquest espai

#### Què passa si el text no és prou llarg?

<div class="resultat">
  <p style="background: gold; padding: 10px; width: 600px;">
    <img style="float: left;" src="https://placehold.it/150x150">
    Va sentir unes passes que corrien cap amunt i cap amunt per les habitacions, i pujant i baixant escales darrere seu
  </p>
</div>

La imatge flotant **desbordarà** perquè és més alta que el seu contenidor groc. I com _de fet_ podeu veure, fins i tot trenca visualment **aquest paràgraf que esteu llegint**.

He deixat intencionadament aquest error de disseny per mostrar _per què_ les carrosses són imprevisibles: fins i tot poden trencar els germans dels seus pares!

Com que `float: left` treu la imatge _fora_ del flux, l'alçada del paràgraf groc és només **l'alçada del seu text**. En altres paraules, l'alçada de la imatge _no es té en compte_.

### Float = bloqueig

Els elements flotants tindran un "display: block" aplicat automàticament, i majoritàriament es comportaran com blocs:

* Podeu establir una alçada i una amplada específiques
* si no s'estableix cap alçada, l'alçada de l'element és la de l'alçada de la línia
* si s'aplica un "amplada: 100%", semblarà un element a nivell de bloc

### Netejant el flotador

La propietat `clear` permet **empènyer elements _després_ del flotant**. Només es pot aplicar en elements **bloc**.

```html
<p>
  <img src="https://placehold.it/150x150">
  <span>Va sentir unes passes que corrien cap amunt i cap amunt per les habitacions, i pujant i baixant escales darrere seu</span>
</p>
```

```css
img{ flotant: esquerra;}
span{ clar: esquerra; mostrar: bloc;}
```

<div class="resultat">
  <p style="background: gold; padding: 10px; width: 600px;">
    <img style="float: left;" src="https://placehold.it/150x150">
    <span style="clear: left; display: block;">Va escoltar unes passes que corrien amunt i avall per les habitacions, i pujant i baixant escales darrere seu</span>
  </p>
</div>

En lloc de tenir el text _al costat_ de la imatge, el `clear: left` empeny el text **a sota** de la imatge.

És diferent de no tenir cap flotador ni clar, ja que la imatge està a la seva pròpia línia i _no_ a la mateixa línia que el text.
