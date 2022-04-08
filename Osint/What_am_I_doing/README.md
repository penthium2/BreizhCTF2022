# What am I doing

**Category** : Osint
**Points** : 308

On sait que notre suspect devait effectuer un rdv avec un certain agent durant ces 3 dernières années, prouvez-le.

Auteur: T0fix

Format: BZHCTF{}


# Write up : 
## résolution : 
Grace au challenge "Account", on connait l'adresse mail du suspect : lucas.delagalett@gmail.com

En testant l'adresse https://calendar.google.com/calendar/u/0/embed?src=lucas.delagalett@gmail.com on voit que l'on a accés à son agenda.
En fouillant celui-ci, on voit un RDV nommé "REUNION ESPION" à la date du 17/09/2020. Ce RDV contient le Flag.


___
## FLAG: 
```
BZHCTF{W3ll_U_found_Me_OSS1000} 
```

Chall resolut par croucroute@BZHack
