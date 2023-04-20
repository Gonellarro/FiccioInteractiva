## Breus fonaments de Twine

### Stories o històries
Qualsevol cosa feta amb Twine es pot anomenar amb qualsevol nom. No hi ha normes sobre convencions de noms i tot, des de jocs experimentals fins a novel·les més tradicionals, es pot crear a Twine. En general, l'editor de Twine anomena els projectes individuals Històries.

### Passatges
Els passatges es poden pensar com a divisions de temps, espai o combinacions dels dos. També es poden considerar blocs de diàleg, seccions de codi o simplement maneres de dividir un projecte complicat en parts més fàcils d'entendre. A Twine, els passatges són el nucli de qualsevol història. Podem veure els passatges com:

-   Una unitat de text, representada amb quadrats a l'eina.  
-   Cada passatge es connecta a altres a través dels enllaços.
-   El passatge, que té la icona d'un coet, és on comença la nostra història.
  
Per defecte, els enllaços són unidireccionals. Exemples:
``` harlowe
[[Entrada a la cova]]
```

Ens crearà un enllaç al passatge “Entrada a la cova”

``` harlowe
[[Entrada a la cova|EntradaCova]]
```

La canonada, "|", es pot utilitzar per canviar el nom d'un enllaç del texte que es veurà a la narració.

``` harlowe
[[EntradaCova<-Entrada a la cova]]
```

A partir de Twine 2, se'ns permetet encaminar on volem dirigir un passatge.

### Variables
En terminologia de programació, una variable és un contenidor per a un valor que pot canviar. A Twine, una variable és una manera d'emmagatzemar i actuar sobre dades d'algun tipus. Qualsevol cosa, des d'un nombre fins a una sèrie de caràcters, es pot emmagatzemar en una variable. A diferència d'altres codis o texts d'un passatge, les variables comencen més habitualment amb el signe del dolar ($) o el guió baix (_) als formats de història Harlowe i SugarCube. 

- Story Variables, són les que comencen per $ i mantenen el seu valor durant tota la història. Per exemple, el nom del personatge o el comptador de vida.
- Temporary Variables, són les que comencen per _ i només mantenen el seu valor dins un passatge. Per exemple, el valor d’una tirada d’un dau o una variable dins un for