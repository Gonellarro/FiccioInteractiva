## Introducció

Harlowe és un dels 4 llenguatges de programació que disposa Twine i és molt útil per a persones que no tenen coneixements de Javascript, HTML ni CSS. Per tant, està molt orientat a persones que el que volen és crear històries sense tenir un rerefons de programació previ. Això no vol dir que es puguin crear algoritmes, rutines, o programes sense coneixement de programar, perquè Harlowe és en sí un llenguatge com a tal, per tant, obligarà a l’alumne o persona que vulgui crear històries amb aquest llenguatge, a aprendre les bases pròpies.

## Iniciació a Harlowe

Al moment de crear aquesta guia, Harlowe va per la versió 3.3.5 i es pot trobar incrustat dins Twine 2.0 com a llenguatge per defecte. Podem comprovar-ho a Twine anant al menú Twine/Story Formats:


Com s’indica al manual de Harlowe: “En el seu nucli, el llenguatge de Harlowe està dissenyat per ajudar els autors sense familiaritat amb HTML, Javascript o CSS. En lloc d'exigir el coneixement dels tres idiomes, Harlowe ofereix un únic idioma que compleix les necessitats bàsiques dels tres i les parts del qual s'integren perfectament.”
![[formats.jpg]]
![[formats2.jpg]]
És per aquest motiu que és el llenguatge més indicat per aquelles persones que no tinguin coneixements en cap dels llenguatges anomenats i vulguin començar a aprendre a crear narracions de ficció interactiva d’una manera ràpida i molt efectista. També, com es nomena al mateix manual, si volem emprar llenguatges que siguin més propers a la programació web, podem triar l’opció de [SugarCube](https://www.motoslave.net/sugarcube/2/), més indicat per aquest tipus d’escriptors.

Tal i com ens indiquen també al manual de Harlowe, aquest ens anima molt a pensar en una pàgina com un espai interactiu dinàmic, no només una seqüència de prosa seguida d'opcions. Harlowe ens anima a col·locar enllaços i elements interactius enmig del text, no només al final, i a utilitzar-los per canviar la nostra narració de maneres sorprenents i inusuals: inserint o eliminant text en un paràgraf llegit prèviament, canviant l'estil de paraules, canviant només l'enllaç en si mateix i altres efectes per revelar un nou significat al text i comunicar la vostra història d'una manera única per a l'hipertext. 

Finalment hem de dir que malgrat la gran potència de programació de Harlowe i le seves amples possibilitats de crear narracions realment enriquides, la ficció interactiva s'associa habitualment a jocs d'aventures de text amb un alt grau de simulació espacial i text generat per procediments, on controlam un personatge-jugador i manipulem objectes i naveguem per sales. Harlowe (i els altres formats d'històries de Twine) està pensat per a una varietat molt més àmplia d'històries amb una quantitat molt més lleugera d'interacció amb el món interior de la història i, com a tal, no conté construccions de programació preconstruïdes per a habitacions, objectes, inventaris, etc. verbs de manipulació i altres recursos de disseny comuns d'aventures de text.  Si volguéssim aprofundir amb aquests nivells de detall, hauríem de migrar a altres llenguatges de programació com [Inform](http://inform7.com/).

## Fonaments de Harlowe

Harlowe és un llenguatge de programació de marques, com pot ser HTML. Conté un alt nombre de funcions que a priori pot semblar descoratjador, però totes les seves característiques giren al voltant dels tres conceptes molt  senzills:
-   Macros  
-   Hooks
-   Qualsevol cosa que produeixi una variable es pot emprar com una variable

### Macros

Una macro és la unitat bàsica del codi. És una ordre que canvia l'estat del joc o del text d'alguna manera. Per exemple:
(set:) ens permet assignar un valor a una variable
(print:) ens permet imprimir el valor d’una variable  
(for:) ens permet fer una enumeració de valors

### Hooks

Quan empram macros per canviar el text de la nostra història, haurem de col·locar aquest text entre claudàtors, que faran un ganxo o hook. A continuació, podem adjuntar un o més valors a la part davantera del hook per canviar aquest texte. Per exemple:
```harlowe
(set: $ringStolen to true)  
(if: $ringStolen)[The ring, as expected, is gone.]
```

En la primera línia assignam el valor vertader a la variable ringStolen, i a la segona línia avaluem amb la macro if, on si és correcte aquesta avaluació, executarà el text que està entre claudàtors o el hook.

### Variables i resultats de macros com a variables

Les variables i les macros són intercanviables amb els valors que contenen o produeixen: una variable que conté un número es pot utilitzar en qualsevol lloc on es pugui utilitzar un nombre, igual que una macro que produeix un nombre. Això vol dir que tenim un ampli ventall d'expressivitat a l'hora d'escriure el codi de la nostra història: podem guardar valors a variables simplement per estalviar-mos haver d'escriure-les completament repetidament.