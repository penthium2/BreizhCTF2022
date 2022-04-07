# Account

**Category** : Osint
**Points** : 50

Nous avons seulement un pseudo lié à une adresse sous la forme prenom.nom@gmail.com (sûrement utile pour nos prochaines recherches) pour un de nos suspect : lucdlgett

Retrouvez le nom et prénom complet de celui-ci dans le but de pouvoir commencer nos recherches.

Auteur: T0fix

Format: BZHCTF{PRENOM-NOM}

___
# write up :

Au vu des informations on peut vite deviner que "lucdlgett" est le speudo utilisé sur des réseaux sociaux. 

Il y a plusieurs réseaux qui utilisent le speudo dans les liens de profils, comme tiwwter et instagram.

On trouve sur intagram ce profils : https://www.instagram.com/lucdlgett/

celui-ci nous indique qu'il est de retour sur insta.


Prenons note de toutes les information pour chaques photos :
 ___
 * 1ère photo : 

https://www.instagram.com/p/Cbvcj4ljPzo/

    lucdlgett : De retour sur Insta, pas facile de se faire pirater.. 😅 Je vais reposter les photos de mon ancien compte!

* 2ème photo : 

https://www.instagram.com/p/CbvcytLD0gV/


    lucdlgett :[Juin 2010] Petit couché de soleil


* 3ème photo : 

https://www.instagram.com/p/CbvdZ13jYi6/

    lucdlgett : [2011] Sympa ces petites vacances !!

* 4ème photo : 

https://www.instagram.com/p/Cbvd3QRD7cm/


    lucdlgett : [2019] Et oui, de retour sur Insta! Petit tour à la mer non loin de ma maison secondaire

*petite remarque de cette photo : les la plage de mon enfance, cela fait du bien de la voir dans un CTF. merci au créateur*

* 5ème photo :

https://www.instagram.com/p/Cbvd9-fDDjp/


    lucdlgett : [2020] A votre avis, il y a combien de mètres?

* 6ème photo : 

https://www.instagram.com/p/CbvhedkDWsr/

    lucdlgett : Got my new book

* 7ème photo : 

https://www.instagram.com/p/CbvmFnQj5wK/


    lucdlgett : Encore de superbes vacances au soleil !!

* 8ème photo :

https://www.instagram.com/p/CbwxeJgDJx8/


    lucdlgett : Et hop la petite cuisine

* 9ème photo : 

https://www.instagram.com/p/CbxHiOgjzhc/


    lucdlgett : Et ça, c'était au Mexique !

* 10ème photo : 

https://www.instagram.com/p/CbxVIoPjukp/


    lucdlgett : Alors, à votre avis, je suis où ?

* 11ème photo : 

https://www.instagram.com/p/CbxgGZnjage/

Rien d'interessant

* 12ème photo : 

https://www.instagram.com/p/CbxzPSODw71/


    lucdlgett : Le petit dernier !!


___

## Résolution du chall  :

Sur la photo N°6 on trouve un pc avec une fenètre de login donnant le prénom et le nom.

**Lucas Delagalett**

___
## FLAG : 
```
BZHCTF{LUCAS-DELAGALETT}
```