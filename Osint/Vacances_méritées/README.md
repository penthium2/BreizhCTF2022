# Vacances méritées

**Category** : Osint
**Points** : 50

Selon son compte instagram, notre suspect est parti en 'vacances' dans un pays froid, retrouvez le nom du pont qu'il a emprunté, cela nous indiquera une position précise d'où il a pu passer.

Auteur: T0fix

Format: BZHCTF{PONT}

## Files : 
 - [vacances1.jpg](./vacances1.jpg)
 - [vacances2.jpg](./vacances2.jpg)


___
# Write up : 
## résolution : 
Sur la photo "vacance1.jpg" on peut voir le nom de domaine "peeva.fi", une recherche google nous indique que le ".fi" est pour la Finlande.
On y voit aussi le nom "PeeVatuote", une autre recherche sur google maps nou emmène au centre de la Finlande, à coté de la ville de Rovaniemi.

Sur la photo "vacance2.jpg"  On peut voir que le numéros de la route où se situe le pont se termine par un 8.

Toujours sur google maps, on peut trouver la route 78 partant de Rovaniemi vers le sud.

En suivant cette route, on arrive vite sur le pont de la photo.
___
## FLAG: 
```
BZHCTF{JATKANKYNTTILA} 
```
Chall resolut par croucroute@BZHack
