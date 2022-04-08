# Mais où est donc or ni car ?

**Category** : Osint
**Points** : 267

Après avoir envoyé un de nos agents pour une filature, il a réussi à s'approcher de la cible mais la photo qu'il a prise est partiellement exploitable. Nous souhaiterions avoir plus d'informations sur son potentiel véhicule.

Auteur: LaChenilleBarbue

Format : BZHCTF{plaque:vin:date_de_mise_en_circulation(dd-mm-yyyy)}

## Files : 
 - [plate.png](./plate.png)


___
# Write up : 
## résolution : 
Sur la photo "plate.png" on peut deviner que l'immatriculation est de la forme "FC-8**-ZD", on apprend egalement que la voiture est une Clio.

Avec le peut que l'on voit des deux chiffres manquants, on sait que les valeurs possibles sont 2, 3 ,5, 6 ,7 ,8 et 9.

En testant plusieurs combinaisons sur le site https://siv-auto.fr/ On finit par tomber sur une Clio immatriculée FC-823-ZD.
Le reste des informations est donné dans la fiche du site. 
___
## FLAG: 
```

BZHCTF{FC823ZD:VF1BB0A0F20759497:23-07-1999}
```
Chall resolut par croucroute@BZHack