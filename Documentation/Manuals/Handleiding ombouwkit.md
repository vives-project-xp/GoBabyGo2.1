<!--Hier komt in hoe ze de ombouwkit moeten maken-->
# Handleiding ombouwset

## Inhoud

    * Onderdelen
    * Materiaal
    * Materiaal
    * Tools
    * Handleiding
    * 

## Onderdelen

Hieronder vind je een lijst van de verschillende onderdelen die nodig zijn om de ombouwset te maken, de leveranciers van de onderdelen alsook een woordje uitleg over de onderdelen.

### Joystick

De joystick die gebruikt dient te worden is van het merkt Joy-IT, deze heeft 4 microschakelaars om de richting door te geven en springt automatisch terug naar de middenpositie. Deze is te verkrijgen bij de leverancier Conrad via deze [link](https://www.conrad.be/nl/p/joy-it-arcade-joystick-professional-8-invoerapparaat-geschikt-voor-arduino-banana-pi-cubieboard-pcduino-raspberry-p-1555268.html?utm_source=google&utm_medium=surfaces&utm_campaign=shopping-feed&utm_content=free-google-shopping-clicks&utm_term=1555268&refresh=true).

### 3D onderdelen

Er zijn 5 verschillende 3D stukken nodig om de joystick vast te zetten op het dashboard van de auto, een doos om de joystick in weg te steken, een deksel om dit af te sluiten, een koppelstuk tussen het dashboard en de doos, een stuk die de stuurstang omhoog houdt en een stuk die dit alles vastzet aan de onderkant van het dashboard. In de map [3D-prints](../3D-prints/) vind je de verschillende onderdelen terug die zullen afgedrukt moeten worden.

### Motor driver

De links rechts richting wordt bepaald aan de hand van de motor die aanwezig is in de auto en een motordriver die er tussen geschakeld wordt. Via de driver wordt de richting en de snelheid van de motor bepaald. De driver die in de schakeling gebruikt wordt is een L298N driver, te verkrijgen bij Otronic via deze [link](https://www.otronic.nl/nl/l298n-motor-driver-board-rood.html).
De L298N is een dubbele H-brug-motordriver die de snelheid en de richting van twee DC-motoren tegelijk mogelijk maakt, in ons geval zullen we maar één motor aansturen. De module kan een DC-motor aansturen met een spanning tussen de 5 en 35V en een piekstroom van 2A. Er zijn twee schroefklemmenblokken aanwezig respectievelijk voor motor A en motor B, een schroefklemblok voor de aarding, de Vcc voor de motor en een 5V-pin die zowel een ingang als een uitgang kan zijn, dit bijvoorbeeld voor een microcontroller. Er zijn 6 control pins aanwezig, pin 1 en 6 dienen om de snelheid van de motoren te regelen met behulp van een microcontroller, pinnen 2 en 3 dienen om de draairichting van motor A te regelen en pinnen 4 en 5 om de draairichting van motor B te regelen. In ons geval zullen we enkel pinnen 2 en 3 gebruiken om de de draairichting van de motor te regelen. Met de pinnen van de draairichting besturen we de schakelaars van de H-brug, als ingang 1 laag is en ingang 2 hoog, zal de motor vooruit bewegen, omgekeerd, als ingang 1 hoog is en ingang 2 laag is zal de moto achteruit bewegen. Als beide ingangen hetzelfde zijn, laag of hoog, zal de motor stoppen.
De L298N zorgt voor een spanningsval van ongeveer 2V, hierdoor zal de spanning op de motorklemmen ongeveer 10V zijn, wat betekent dat we niet de maximale snelheid uit de 12V DC-motor kunnen halen.
<!--Nog eens nakijken op correcte uitleg werking-->

### Regelbare step-down module

Een regelbare step-down module wordt gebruikt om de 12V ingangsspanning te verlagen naar 5V ingangsspanning voor de motor driver aan te sturen. Deze is te verkrijgen bij Otronic via volgende [link](https://www.otronic.nl/nl/regelbare-step-down-module-438v-5a-96-ho-140568470.html).
De DC-DC-Converter reduceert de DC-ingangsspanning tot een specifieke DC-uitgangsspanning. <!--Nog verder uitschrijven-->

### Tuimelschakelaar

De auto wordt voorzien van een kill-switch om de stoom naar beide motoren te onderbreken. Deze tuimelschakelaar is te verkrijgen bij de leverancier Conrad via deze [link](https://www.conrad.be/nl/p/tru-components-1587664-tc-r13-2-05-tuimelschakelaar-250-v-ac-1-5-a-1x-uit-aan-continu-1-stuk-s-1587664.html?utm_source=google&utm_medium=surfaces&utm_campaign=shopping-feed&utm_content=free-google-shopping-clicks&utm_term=1587664&adcampaign=google&tid=16860426636_pla-1587664&gad_source=1&gclid=CjwKCAiAivGuBhBEEiwAWiFmYbr98urP1hYvNQBoRcFG0IOoJQFPxab4w2YgbCKT6JE00yVvjM9n6RoC2s0QAvD_BwE).

## Materiaal

In de onderstaande lijst, staat het nodige materiaal om de ombouwset te maken.

    * 3 stukken 140cm rode flexibele koper draad van <!--maten invullen--> mm dik
    * 4 stukken 30cm rode flexibele koper draad van <!--maten invullen--> mm dik
    * 1 stuk 140cm zwarte flexibele koper draad van <!--maten invullen--> mm dik
    * 2 stukken 30cm zwarte flexibele koper draad van <!--maten invullen--> mm dik
    *<!--hoeveelheid invullen--> 3 way waggo
    *<!--hoeveelheid invullen--> kabelschoenen
    *<!--hoeveelheid invullen--> kabelbinders
    * 4 moeren maat M6
    *<!--hoeveelheid invullen--> M6 metaalschroef van <!--maten invullen-->
    * 4 stuks schroefdraadbussen M3

## Tools

Volgende tools zijn nodig om de ombouwset in elkaar te monteren.

    * Platte schoevendraaier<!--maat ingeven-->
    * Kniptang
    * Ontmanteltang
    * Kabelbinders
    * Soldeerbout
    * <!--nog materiaal toevoegen dat nodig is-->
    * Labels om kabels te labelen

## Handleiding

### Stap 1

Steek 4 schroefdraadbussen maat M6 in de voorziene gaten van de 3D print waar de joystick wordt ingeplaatst. Dit met behulp van een soldeerbout om het plastiek wat te smelten. De soldeerbout dient een dikke punt te hebben en ingesteld worden op ongeveer 200°c. Wacht even tot de warmte wordt over gezet op de schroefdraadbus en smelt deze voorzichtig in het plastiek.
Plaat 2 M6 moeren op de voorziene plaatsen in het 3D design van het dashboard koppelstuk op dezelfde manier als de schroefdraadbussen.

### Stap 2

Ontmantel de rode en zwarte draden zodat ongeveer 1cm plastic van de draad verwijderd is.
Hang aan de 2 lange rode draden een kabelschoen aan één uiteinde, <!--hang aan de zwarte lange draad één kabelschoen,--> hang aan de 2 korte rode draden een kabelschoen aan één uiteinde en hang aan de korte zwarte draden een kabelschoen aan één uiteinde.
Verbind de 2 korte rode draden met een lusterklem alsook de 2 korte zwarte draden.

### Stap

Verbind de draad voor de linkse richting met de motor driver op pin IN1 en de draad voor de rechtse beweging op pin IN2. Verbind daarna een rode draad met output1 en een gele draad met output2 dit om tijdens de ombouw door te verbinden met de motor. Verbind een rode draad met de Vcc, een zwarte draad voor de ground en een rode draad om 5V af te takken voor de joystick. <!--aantal draden en welk kleur draden nog te bepalen-->

### Stap

### Stap


<!--Dit klopt niet in logische opbouw van auto-->
Hang deze vervolgens aan de joystick en label de draden volgens richting, vooruit, achteruit, links en rechts. Steek de draden door het voorziene gat van de 3D print waarin de joystick moet geplaatst worden, rekeninghoudende met de richting. De draden die dienen voor het vooruit rijden dienen vooruit gericht te zitten in de 3D print.
<!--Dit stuk moet bij de handleiding voor installatie van ombouwkit-->
Plaats het 3D stuk met de halve maan uitstulping op de plaats waar het stuur oorspronkelijk moest komen. De kleine cilindervorm plaats je een M6 moet op de voorzien plaats in de 3D print. Schuif dit over de stuurstang en schroef dit vast met een metaalschroef. Dit voorkomt dat de stuurstang zak