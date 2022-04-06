# Tête en l'air

**Category** : Radio
**Points** : 492

La tour de contrôle nous a signalé la présence d'un aéronef à proximité, pouvez-vous nous en apprendre un peu plus sur cet aéronef ?

Auteur: LaChenilleBarbue

rtl_tcp : challenges.ctf.bzh 28001 (freq: 1090Mhz)

Format : BZHCTF{INDICATIF:VILLE_SURVOLEE:MODEL_AERONEF}

# wirte Up :

Nous somme sur un chall qui nous indique que c'est la tour de controle qui nous donne les information.
Le chall nous donnait aussi la fréquence : 1090Mhz

après une recherche sur ce type de fréquence je tombe sur cela : 

```
Les fréquences 1030 et 1090 MHz sont en outre utilisées pour les radars secondaires (c’est-à-dire ceux interrogeant un transpondeur dans l’avion, alors que les radars primaires utilisent simplement le signal radar réfléchi par l’avion) afin de localiser les avions et fournir cette information au contrôle aérien. C’est aujourd’hui la source essentielle d’information pour le contrôle aérien. Certains modes à ces fréquences permettent l’anticollision entre avions (TCAS) et la transmission de la localisation d’un avion sans interrogation (ADS-B). Suites aux décisions prises lors de la dernière Conférence Mondiale des Radiocommunications ( CMR -15), les satellites vont désormais pouvoir écouter à la fréquence de 1090 MHz les messages ADS-B émis par les aéronefs afin d’assurer un suivi global des vols et éviter que l’on puisse perdre trace d’un vol, comme cela s’était produit avec celui de la Malaysian Airlines MH370.
```

Après plusieur heure pour trouver le bon outil j'ai enfin ce qu'il me faut : 
https://github.com/wiedehopf/adsb-scripts/

en lisant bien le git je tombe sur l'install oneline pour une débian ( bon je suis sous ferado, mais j'ai une VM kali ) : 

```
sudo bash -c "$(wget -O - https://github.com/wiedehopf/adsb-scripts/raw/master/readsb-install.sh)" 
```

Le plus dur est arrivé, enfin pour moi ! comment utilisé **dump1090-mutability** avec une source réseau... est là les heure ont défilé... avec des pauses... des discutions... et le déclic d'un **ami** :

*ba via netcat, non ?*

Let's go marco :

nc challenges.ctf.bzh 28001 | dump1090-mutability --ifile - > dump

extrait du fichier dump : 

```
*8ddddbfc580b8779739f7a7fe8ee;
CRC: 000000
RSSI: -7.7 dBFS
Score: 1800
Time: 3179850.75us
DF:17 AA:DDDBFC CA:5 ME:580B8779739F7A
 Extended Squitter Airborne position (barometric altitude) (11)
  ICAO Address:  DDDBFC (Mode S / ADS-B)
  Air/Ground:    airborne
  Altitude:      1200 ft barometric
  CPR type:      Airborne
  CPR odd flag:  odd
  CPR NUCp/NIC:  7
  CPR latitude:  48.01179 (113849)
  CPR longitude: -1.74021 (106362)
  CPR decoding:  global
```

BINGO \o/ on à des infos ! 

On sait que le flag est style : 
```
BZHCTF{INDICATIF:VILLE_SURVOLEE:MODEL_AERONEF}
```

**3 choses à trouver :** 

* Model Aeronef : 

    L'ICAO est le code des modèle d'avion on va sur ce syte pour trouver notre bonheur : 

    https://www.flightradar24.com/data/aircraft/f-chap

    AIRCRAFT : **ASH-25**

* Ville survolée :

    Les coordoné gps : 
    
    ```
    CPR latitude:  48.01179 (113849)
    CPR longitude: -1.74021 (106362)
    ```

    ville : 35170 **Bruz**, France

* indicatif :

    après plusieur tentative et analyse en temps réèl, ba pas grand chose....

    On va changer les options du notre application et basculé en mode interactif ! 

    ```
    nc challenges.ctf.bzh 28001 | dump1090-mutability --ifile - --interactive
    ```
    BINGO \o/ toutes les x secondes on voit aparitre cette string : 
    ```
    P0UP4RD
    ```

On balance **le FLAG** : 
```
BZHCTF{P0UP4RD:BRUZ:ASH-25}
```