---
layout: post
---
Scratch-tutorial: Labyrinten
============================
*af Martin Dybdal, idé: Martin Exner*

![](del1-billeder/image_00.png)

I denne tutorial vil jeg forklare hvordan du kan lave et spil hvor musen Piv skal finde ost i lastrummet i Kaptajn Hacks sørøverskib!

Start med at oprette en konto på <http://scratch.mit.edu> hvis du ikke allerede har en. Ellers kan du ikke gemme dit spil til næste gang.

Hvis du får problemer mens du er derhjemme, så skriv et spørgsmål på Coding Pirates-forummet: <http://forum.codingpirates.dk/>

## Del 1: Tegn labyrinten og spilleren

Først skal vi tegne hvordan musen skal se ud og labyrinten den skal løb rundt i.

### Vejledning

Start med at klikke på penslen, for at oprette en ny figur (engelsk: sprite):

![](del1-billeder/image_01.png)

Tegn hvordan musen skal se ud og sørg for at du tegner den præcis midt på skærmen! Her er min:

![](del1-billeder/image_02.png)

Lad os give figuren et navn. Det gøres ved at trykke på det lille "i" ved siden af figuren:

![](del1-billeder/image_03.png)

Jeg kalder min for "mus":

![](del1-billeder/image_04.png)

Vi skal også have en labyrint! Den tegner vi som en "baggrund". For at lave en baggrund skal du klikke her:

![](del1-billeder/image_05.png)

Og så her:

![](del1-billeder/image_06.png)

Tegn nu en labyrint. 

**Vigtigt:** Brug den samme farve til alle væggene!

**Hint:** Hold "Shift" (⇧) nede mens du bruger linje-værktøjet, for at tegne helt lige streger!

Her er min labyrint:

![](del1-billeder/image_07.png)

Gangene er blevet lidt små i forhold til musen, så lad os gøre musen lidt mindre, så den kan komme rundt. 

Det gør du ved at trykke på:

![](del1-billeder/image_08.png)

i toppen af skærmen og derefter på figuren der skal blive mindre! Sådan det var bedre:

![](del1-billeder/image_09.png)

## Del 2: Styr med piletasterne

Nu skal vi have musen til at bevæge sig!

### Vejledning

Vælg først musen:

![](del1-billeder/image_10.png)

Tryk derefter på fanebladet "Scripts":

![](del1-billeder/image_11.png)

Vælg "Hændelser":

![](del1-billeder/image_12.png)

Vælg denne brik og flyt den ind på kodeområdet (Scratch-katten’s "hjerne"):

![](del1-billeder/image_13.png)

og ændr den til "højre pil" ved at klikke på den sorte pil:

![](del1-billeder/image_14.png)

Kobl den sammen med denne brik:

![](del1-billeder/image_15.png)

Og så denne:

![](del1-billeder/image_16.png)

Sådan! Så burde du have:

![](del1-billeder/image_17.png)

Byg nu det samme igen, men denne gang skal musen gå til venstre:

![](del1-billeder/image_18.png)

Nogle kloge mennesker har fundet på at:

* -90 betyder venstre

* 90 betyder højre

Prøv spillet ved at trykke på det grønne flag: ![](del1-billeder/image_19.png)

Nu kan man gå frem og tilbage, men vi skal også kunne gå op og ned!

**Opgave**

Prøv om du selv kan finde ud af at gøre så når du trykker på "pil opad" og “pil nedad”, så bevæger musen sig i den retning!

### Musen vender på hovedet!

Hvis musen vender på hovedet når du går til venstre:

![](del1-billeder/image_20.png)

Du behøver ikke forstå hvorfor, bare gør det!

## Del 3: Ikke snyde!

Hvis du har prøvet spillet, så er det ikke så sjovt endnu, for man kan jo gå igennem væggene. Lad os ændre på det!

**Vejledning**

Lad os først tænke over hvad vi skal. Vi skal have gjort, sådan at man ikke rykker fremad, når man går ind i "noget der er gult" (eller den farve som du har tegnet din labyrints vægge). Vi skal altså holde øje med om man går ind i noget gult og hvis man gør det, så skal man rykkes tilbage hvor man kom fra.

Vi laver det som et nyt script, så vi skal have sådan en start-brik:

![](del1-billeder/image_21.png)

alt hvad der er nedenunder den bliver udført når man starter spillet.

Gå nu ind under styring:![](del1-billeder/image_22.png)

og find den her brik:

![](del1-billeder/image_23.png)

Den gentager det der inde i den UENDELIGT! Prøv f.eks. at gøre sådan her:

![](del1-billeder/image_24.png)

Nu vil musen hele tiden gå baglæns, fordi jeg skrev -5!

Vi ville gerne have den til at gå baglæns, men kun **hvis** den rørte noget gult! Så vi skal have fat i en "**hvis **… **så**" brik. Den ligger også under “styring”:

![](del1-billeder/image_25.png)

Og inde i den skal vi så fortælle

1. hvad det er den skal tjekke (at vi rører en gul væg)

2. hvad det er den skal gøre hvis vi rører væggen (gå baglæns)

Det første kan vi gøre ved at gå ind under ![](del1-billeder/image_26.png) og vælge brikken

![](del1-billeder/image_27.png)

For at ændre så den tjekker gul:

* Tryk på det røde felt

* Tryk derefter på noget gult (væggen i din labyrint)

At gå baglæns har vi allerede fundt ud af, vi skal bare "gå -5 trin":

![](del1-billeder/image_28.png)

Nu kan vi sætte det hele sammen:

![](del1-billeder/image_29.png)

## Del 4: Tegn en ost

Lad os placere noget ost i lastrummet!

### Vejledning

Tryk på penslen for at lave en ny figur:

![](del1-billeder/image_30.png)

Ændr navnet til "ost1"

![](del1-billeder/image_31.png)

Tegn osten. Her er hvordan den ser ud:

![](del1-billeder/image_32.png)

## Del 5: Opdag når musen rører ved osten

Vi skal have lavet et script der opdager hvornår musen har taget osten og flytter osten til et nyt sted i labyrinten!

**Vejledning**

Nu skal du vælge osten hvis du ikke allerede har gjort det:

![](del1-billeder/image_33.png)

og trykke op "Scripts":

![](del1-billeder/image_34.png)

Vi skal have gjort lidt ligesom vi gjorde da vi opdagede om vi rørte en væg. Så start med at bygge:

![](del1-billeder/image_35.png)

"hvis"-brikken skal nu tjekke om osten rører ved musen, så vi skal bruge denne brik:

![](del1-billeder/image_36.png)

og indstille den til at blive aktiveret når vi rører ved musen:

![](del1-billeder/image_37.png)

Så nu har vi:

![](del1-billeder/image_38.png)

Det der står inde i "maven" af hvis-brikken bliver kørt hver gang osten rører ved musen! 

Hvad skal vi have til at ske? Vi kunne f.eks. flytte osten til et andet sted på brættet.

![](del1-billeder/image_39.png)

Nu virker spillet! 

Lad dine venner prøve det næste gang de er på besøg. Det kan være de har nogle forslag til hvordan det bliver flottere eller sjovere!

## Udvidelser

Der er massere af muligheder for at udvide spillet, her er nogle idéer:

 * Tilføj en modspiller, så man kan konkurrere om hvem der kan få flest oste
 * Tilføj teleportere, så man kan hoppe fra den ene ende af banen til den anden
 * Tilføj flere baner, så når man har klaret den første, så skifter baggrunden til en anden labyrint
 * Tilføj point-tæller
 * Tilføj nøgler og døre, så man skal samle en nøgle op for at åbne specielle døre
 * Game-over skærm
 * Tillykke-skærm når man har vundet
 * Menu til at starte spillet

