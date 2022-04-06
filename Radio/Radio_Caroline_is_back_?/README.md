# Radio Caroline is back ?

**Category** : Radio
**Points** : 439

On a identifier une fréquence porteuse non autorisée sur la bande FM, peux tu en extraire de l'information ?

Auteur: LaChenilleBarbue

rtl_tcp : challenges.ctf.bzh 28002

Format : BZHCTF{information}

# wirte Up :

J'ai utilisé le logiciel GQRX

setting : 

```
Device : RTL-SDR Stectrum Server

Devive String : rtl_tcp=challenges.ctf.bzh:28002

Input rate : 2500000 ( 2.5Msps) 
    en jouant avec cette valeur on acélère ou ralentit le flux audio
```

Dans GQRX il fallait choisir le mode : **WFM(mono)**, afin d'avoir un son sans trop de parasites.

Puis j'ai enregistré le flux via la function **rec** de GQRX

Pour gagner du temps j'ai utilisé un site de convertion audio to txt : https://virtualspeech.com/tools/audio-to-text-converter

pour avoir cette "horeur" :

```
d'associer TF Accolade. Cette zéro trois neuf faisait de six quatre décès. Huit deux huit zéro six à zéro zéro un cinq le neuf sept trois de neuf un quatre huit e six Accolade.
```

Cela ma donné une bonne base une fois retranscrit en chiffres et lettres pour avoir un début de flag et en jouant avec VLC en répétition vitesse ralentie puis acélérée j'ai trouvé le flag : 


```
BZHCTF{7039z64dc8e1806a001f59f73291486}
```



