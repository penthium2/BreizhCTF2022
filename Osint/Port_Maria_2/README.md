# Port Maria 2

**Category** : Osint
**Points** : 353

Toujours dans le but de retracer le trajet de notre suspect, sur le compte Instagram, nous avons trouvé une deuxième photo liée à un retour (?) en avion.

Retrouvez le nom de la ville de décollage et du port que l'on voit sur la photo.

Auteur: T0fix

Format: BZHCTF{VILLE:PORT-X}

Notes : Les espaces seront remplacés par des tirets '-'.

## Files : 
 - [insta2.jpg](./insta2.jpg)

___
# Write Up : 

## analyse :
Après une analyse de la photo nous découvrons 2 information importante et utile permetant de ciblé au miuex notre recherche.

* 1ère Information :

Il y a des marais salan en contre bas

Il n'y a pas beaucoup de zone en france avec des marais salant il y a :
La bretagne
La vendé
La camargue
principalement.


 * 2ème Information :

Il y a un port avec des réserves pétrolières

Cette information nous aidé a centré notre investigation, en Vendée il y a pas de type de port, En bretagne les marais salant sont éloigné des port pétroler ( je pense à donges)
___
## résolution :

En couplant aéroport et port pétrollié on arrive dans la zone de **Marseille**.

Via google map en vu satélite on tombe sur ce que l'on cherchait : 
https://www.google.fr/maps/place/Marseille/@43.4672041,5.113103,11009m/data=!3m1!1e3!4m5!3m4!1s0x12c9bf4344da5333:0x40819a5fd970220!8m2!3d43.296482!4d5.36978?hl=fr&authuser=0

J'ai mis une photo pour mieux voir le port et son nom qui est : 
** Port de la Pointe **

___
## FLAG :
```
BZHCTF{MARSEILLE:PORT-DE-LA-POINTE}
```