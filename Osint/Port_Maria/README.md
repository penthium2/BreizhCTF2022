# Port Maria

**Category** : Osint
**Points** : 50

Dans le but de retracer le trajet de notre suspect, nous avons trouvé sur son compte Instagram une photo liée à un déplacement en avion.

Retrouvez le nom de la ville et du port que l'on voit sur la photo.

Auteur: T0fix

Format: BZHCTF{VILLE:PORT-X}

Notes : Les espaces seront remplacés par des tirets '-'.

## Files : 
 - [insta1.jpg](./insta1.jpg)


___
# Write up : 
## résolution : 
La photo nous donne une vue aérienne du port ainsi que le logo de la compagnie aérienne.

En recherchant "Compagnie aerienne logo T vert" sur Google, on tombe tout de suite sur la compagnie Transavia.

La couleur des maisons et des toits fait penser au sud de la France et en regadant sur le site www.transavia.com, on trouve des villes comme Marseille ou Nice dans les destinations.

En comparant la photo aux vues aérienne de Google Maps, on reconnait le port de Nice : Port Lympia.
___
## FLAG: 
```

BZHCTF{NICE:PORT-LYMPIA}
```
Chall resolut par croucroute@BZHack