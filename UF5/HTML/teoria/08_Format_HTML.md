# Format d'HTML

## Quan l'espai en blanc no importa

Hi ha una diferència entre el que **s’escriu** al vostre codi HTML i el que **es mostra** al navegador.

Com ja hem vist, les etiquetes HTML, com ara `<p>`, només són _llegides_ pel navegador (per saber quin tipus de contingut està escrit), però **el navegador no les mostra**.

També hem vist com és possible escriure **comentaris** HTML al vostre codi, per ajudar els humans a llegir el codi, sense que el navegador els visualitzi.

Un altre tipus de codi escrit _ignorat_ pel navegador és **l'espai en blanc**, que inclou:

* salts de línia
* línies buides
* tabulacions (o sagnat)

### Salts de línia

El navegador **ignora** els salts de línia i les línies buides (que són una successió de salts de línia) en codi HTML. Només representen un **únic** espai.

```html
<p>
La idea original del web era que hauria de ser un 


espai


de col·laboració on poder comunicar-se compartint informació.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
  La idea original del web era que hauria de ser un espai de col·laboració on poder comunicar-se compartint informació.
  </p>
</td></tr></table>

Per tal de **forçar** un salt de línia, heu d'utilitzar l'element HTML `<br>`:

```html
<p> En el millor dels casos, la vida és completament <br> imprevisible. </p>
```

<table bgcolor="grey"><tr><td>
  <p> En el millor dels casos, la vida és completament <br> imprevisible. </p>
</td></tr></table>

### Tabulacions

Una **tabulació** és un caràcter especial obtingut prement la tecla _ `Tab`. Normalment mou el cursor a la següent tabulació, però de vegades es converteix en 2 espais.

De totes maneres, com un espai normal, una tabulació és **invisible**. El navegador també ignora:

```html
<p>
  Empenyem aquest text
  amb tabulacions.
</p>
```

<table bgcolor="grey"><tr><td>
  <p>
    Empenyem aquest text
    amb tabulacions.
  </p>
</td></tr></table>

Si voleu afegir espai _abans_ d'una paraula, haureu d'utilitzar CSS, que el tractarem amb profunditat més endavant.

### Format d’arbre

Com que els elements HTML es poden anidar els uns als altres, heu de fer un seguiment del **ordre** en què s'han obert, ja que afectarà l'ordre en què es tanquen.

```html
<article> <p> Aquest codi està escrit en una línia <strong> única </strong>. </p> </article>
```

<table bgcolor="grey"><tr><td>
  <article> <p> Aquest codi està escrit en una línia <strong> única </strong>. </p> </article>
</td></tr></table>

Com que pot ser difícil fer un seguiment de l'ordre en què s'han obert els elements HTML, es recomana escriure HTML en un ** format d'arbre **:

```html
<article>
  <p>
    Aquest codi està escrit
    <strong> múltiple </strong>
    línies però no obstant això 
    es mostrarà en una
    <em> única </em>
    líniea.
  </p>
</article>
```

<table bgcolor="grey"><tr><td>
<article>
  <p>
    Aquest codi està escrit
    <strong> múltiple </strong>
    línies però no obstant això 
    es mostrarà en una
    <em> única </em>
    líniea.
  </p>
</article>
</td></tr></table>

El format d'arbre permet replicar _visualment_ els **nivells de nidificació** del vostre codi HTML. Per tant, és fàcil veure que:

* `<article>` és el **avantpassat**
* `<p>` és el **pare** de `<strong>` i `<em>`
* `<strong>` i `<em>` són **germans**

### Escriviu HTML perquè el llegiu

Les tabulacions, les línies buides, els espais successius i els salts de línia són descartats per l'ordinador i es converteixen en un **espai únic**.

Un document HTML és escrit i llegit per un ésser humà, però només _llegit_ per un ordinador. Tenint en compte les tabulacions, els espais i els salts de línia no afecten la manera com un navegador llegirà i, posteriorment, mostrarà la vostra pàgina web, podeu formatar el document de la manera més llegible per a **vosaltres**.

No hi ha regles específiques relatives al format HTML, però hi ha **convencions** implícites, concretament:

* utilitzeu **tabulacions** per ajudar a visualitzar com es **nien els elements HTML**
* posar etiquetes d'obertura i tancament d'elements de nivell de bloc a la seva **pròpia línia**
* escriure elements en línia en una línia (incloses les etiquetes d'obertura i tancament)

## Preguntes que heu de respondre a la [pràctica 1](https://moodle.insjoaquimmir.cat/mod/assign/view.php?id=42051)

1. Per quina raó, tot i que no es veuen en el navegador, es recomanable escriure codi HTML amb salts de línia, tabulacions, etc?
