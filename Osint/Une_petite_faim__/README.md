# Une petite faim ?

**Category** : Osint
**Points** : 50

Après avoir étudié son compte Instagram, nous sommes remonté jusqu'en 2011, soit l'ouverture de son compte. Il semblerait qu'à ce moment là, notre suspect ait pris des vacances, et selon nos sources sa carte bleu aurait loggué un achat en restauration rapide le plus proche de cet endroit.

Retrouvez le nom de la ville et du restaurant rapide auquel il a été pour nous permettre d'aller enquêter.

Auteur: T0fix

Format: BZHCTF{VILLE:RESTAURANT}

Notes : Les espaces seront remplacés par des tirets '-'.

## Files : 
 - [picture.jpg](./picture.jpg)


# Write up : 
## résolution : 
Une recherche invérsée de l'image nous permet de trouver le nom et l'emplacement de la fontaine : "Fontaine de la rotonde - Aix En Provence"

Aprés avoir tésté le nom des differents fast-food alentours, on se rend compte que le chall est plus subtil que ca.

En relisant l'ennoncé, on voit que l'année ou le suspect s'est rendu dans ce lieu est 2011.

Les archives google-street view ne propose qu'une seule date de cette année : Mars 2011.
En regardant autours de la fontaine à cette date, on trouve un kiosque à crepes, glaces et gauffre qui se nomme "La Fringale" :

https://www.google.fr/maps/@43.526111,5.4455284,3a,75y,101.46h,86.81t/data=!3m7!1e1!3m5!1sflVoMlITHQjg97S84yGsjQ!2e0!5s20110301T000000!7i13312!8i6656


___
## FLAG: 
```
BZHCTF{AIX-EN-PROVENCE:LA-FRINGALE}
```

Chall resolut par croucroute@BZHack