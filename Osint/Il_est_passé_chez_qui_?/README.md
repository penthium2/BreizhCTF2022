# Il est passé chez qui ?

**Category** : Osint
**Points** : 162

Après avoir recupéré le numéro de téléphone de la cible, nous souhaitons pouvoir le mettre sur écoute. Pour effectuer la demande à l'opérateur, nous devons identifier celui-ci. Pouvez-vous vous en charger ?

Auteur: LaChenilleBarbue

Format : BZHCTF{MCCMNC:OPERATEUR}

___

# Write up

## opérateur :
Après une légère recherche on aprends que l'Arcep a un site qui nous permet de savoir le nom de l'opérateur d'un numéro de téléphone.

via ce site : 


https://www.arcep.fr/demarches-et-services/professionnels/base-numerotation.html?tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5B%40extension%5D=ArcepBasetechnique&tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5B%40vendor%5D=GAYA&tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5B%40controller%5D=BaseTechnique&tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5B%40action%5D=search&tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5Barguments%5D=YTowOnt93f79ac872f3e891e3d121304494af15ceeb744e4&tx_arcepbasetechnique_basetechnique%5B__referrer%5D%5B%40request%5D=a%3A4%3A%7Bs%3A10%3A%22%40extension%22%3Bs%3A18%3A%22ArcepBasetechnique%22%3Bs%3A11%3A%22%40controller%22%3Bs%3A13%3A%22BaseTechnique%22%3Bs%3A7%3A%22%40action%22%3Bs%3A6%3A%22search%22%3Bs%3A7%3A%22%40vendor%22%3Bs%3A4%3A%22GAYA%22%3B%7Da2bf59f355c30621a92ab741b949e14e74a32abc&tx_arcepbasetechnique_basetechnique%5B__trustedProperties%5D=a%3A1%3A%7Bs%3A6%3A%22search%22%3Ba%3A1%3A%7Bs%3A7%3A%22numeros%22%3Bi%3A1%3B%7D%7D6c5a73b9b235b8db1e19b0bafed7ac83147025d4&tx_arcepbasetechnique_basetechnique%5Bsearch%5D%5Bnumeros%5D=075791#c981


On découvre donc que la société  est : 

**Société Legos-Local exchange-Global opération services**
___

## MCC MNC :

Afin de trouvé les numeros MCC et MNC je suis passé par wikipedia :

https://fr.wikipedia.org/wiki/Mobile_Network_Code

et on y retrouve la socité de l'opérateur avec un nom racoursit : 

```
MCC MNC opérateur  
208	17	Legos
```
___
## FLAG : 
```
 BZHCTF{20817:LEGOS}
 ```