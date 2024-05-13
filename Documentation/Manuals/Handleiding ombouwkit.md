# Handleiding ombouwkit

## Inhoud

* [Onderdelen](#onderdelen)
* [Materiaal](#materiaal)
* [Tools](#tools)
* [Handleiding](#handleiding)

## Onderdelen

Hieronder vind je een lijst van de verschillende onderdelen die nodig zijn om de ombouwset te maken, de leveranciers van de onderdelen alsook een woordje uitleg over de onderdelen.

### Joystick

De joystick die gebruikt dient te worden is van het merkt Joy-IT, deze heeft 4 microschakelaars om de richting door te geven en springt automatisch terug naar de middenpositie. Deze is te verkrijgen bij de leverancier Conrad via deze [link](https://www.conrad.be/nl/p/joy-it-arcade-joystick-professional-8-invoerapparaat-geschikt-voor-arduino-banana-pi-cubieboard-pcduino-raspberry-p-1555268.html?utm_source=google&utm_medium=surfaces&utm_campaign=shopping-feed&utm_content=free-google-shopping-clicks&utm_term=1555268&refresh=true).

### 3D onderdelen

Er zijn 5 verschillende 3D stukken nodig om de joystick vast te zetten op het dashboard van de auto, een doos om de joystick in weg te steken, een deksel om dit af te sluiten, een koppelstuk tussen het dashboard en de doos, een stuk die de stuurstang omhoog houdt en een stuk die dit alles vastzet aan de onderkant van het dashboard. In de map [3D-prints](../3D-prints/) vind je de verschillende onderdelen terug die zullen afgedrukt moeten worden.

### Motor driver

De links-rechtssturing wordt bepaald aan de hand van de motor die aanwezig is op de stuurstang in de auto. Via de driver wordt de richting van de motor bepaald deze is een L298N driver, te verkrijgen bij Otronic via deze [link](https://www.otronic.nl/nl/l298n-motor-driver-board-rood.html). [Datasheet L298N](DatasheetL298_H_Bridge.pdf)
De L298N is een dubbele H-brug-motordriver die de snelheid en de richting van twee DC-motoren tegelijk mogelijk maakt, in ons geval moeten we maar één motor aansturen. De module kan een DC-motor aansturen met een spanning tussen de 5 en 35V en een piekstroom van 2A.

Er zijn twee schroefklemmenblokken aanwezig respectievelijk voor motor A en motor B, een schroefklemblok voor de aarding, de Vcc voor de motor en een 5V-pin die zowel een ingang als een uitgang kan zijn, dit bijvoorbeeld voor een microcontroller. Er zijn 6 control pins aanwezig, pin 1 en 6 dienen om de snelheid van de motoren te regelen met behulp van een microcontroller, pinnen 2 en 3 dienen om de draairichting van motor A te regelen en pinnen 4 en 5 om de draairichting van motor B te regelen.

In ons geval zullen we enkel pinnen 2 en 3 gebruiken om de draairichting van de motor te regelen. Met de pinnen van de draairichting besturen we de schakelaars van de motor driver, als ingang 1 laag is en ingang 2 hoog, zal de motor vooruit bewegen, omgekeerd, als ingang 1 hoog is en ingang 2 laag is zal de moto achteruit bewegen. Als beide ingangen hetzelfde zijn, laag of hoog, zal de motor stoppen.

De L298N zorgt voor een spanningsval van ongeveer 2V, hierdoor zal de spanning op de motorklemmen ongeveer 10V zijn, wat betekent dat we niet de maximale snelheid uit de 12V DC-motor kunnen halen.

### Tuimelschakelaar

De auto wordt voorzien van een kill-switch om de stroom naar beide motoren te onderbreken.
Deze tuimelschakelaar is te verkrijgen bij de leverancier Conrad via deze [link](https://www.conrad.be/nl/p/tru-components-1587664-tc-r13-2-05-tuimelschakelaar-250-v-ac-1-5-a-1x-uit-aan-continu-1-stuk-s-1587664.html?utm_source=google&utm_medium=surfaces&utm_campaign=shopping-feed&utm_content=free-google-shopping-clicks&utm_term=1587664&adcampaign=google&tid=16860426636_pla-1587664&gad_source=1&gclid=CjwKCAiAivGuBhBEEiwAWiFmYbr98urP1hYvNQBoRcFG0IOoJQFPxab4w2YgbCKT6JE00yVvjM9n6RoC2s0QAvD_BwE).

## Materiaal

In de onderstaande lijst, staat het nodige materiaal om de ombouwset te maken.

* 3 x 140cm rode h05v-k flexibele koper kabel van ø 1.5mm²  = 420 cm
* 7 x 20cm rode h05v-k flexibele koper kabel van ø 1.5mm²  = 140 cm
* 3 x 30cm zwarte h05v-k flexibele koper kabel van  ø 1.5mm² = 30cm
* 9 x Wago verbindingsklem 3-voudig  geschikt voor geleiders met maximale doorsnede van 4mm²
* 8 x Kabelschoenen (Indien je een ander type joystick gebruikt controleer steeds dat de kabelschoenen passen naar behoren.)
* 2 x Female jumper connector dupont (krimp uitvoering)
* 5 x Moeren maat M5
* 5 x Metaalschroeven maat M5
* 4 x Schroefdraadbussen M3
* 4 x Metaalschroef M3 30mm

* Optie:  Adereindhuls

## Tools

Volgende tools zijn nodig om de ombouwset in elkaar te monteren.

* Platte kop schoevendraaier
* Kruiskop schroevendraaier
* (Zij)Kniptang
* Striptang (Best een instelbare voor de verschillende diameters.)
* Soldeerbout
* Soldeertin (Eventueel Flux)
* Soldeermat
* Dupont Krimptang
  
* Optie: Labels om kabels te labelen

## Handleiding

### Stap 1: 3D-prints joystick

Plaats de 4 schroefdraadbussen maat M3 in de daarvoor bestemde gaten van de 3D-print waar de joystick wordt geplaatst.
Gebruik hiervoor een soldeerbout om het plastic voorzichtig te laten smelten.
Zorg ervoor dat de soldeerbout een dikke punt heeft en ingesteld is op ± 200°C.
Wacht even totdat de warmte gelijkmatig wordt verdeeld en smelt de schroefdraadbus voorzichtig in het plastic.
Doe hetzelfde voor de stuurstanghouder waar een uitsparing is voorzien voor een M5-moer.
Plaats 2x M5-moeren in de daarvoor voorziene plaats van het dashboard koppelstuk en schuif 2x M5-moeren in de voorziene gleuven van het dashboardkoppelstuk.

Schroef de metalen plaat die standaard aan de joystick hangt los en bevestig in plaats daarvan het deksel voor de doos aan de joystick met de bijbehorende schroeven.
Schroef de groene stukken onderaan de joystick los, deze zijn niet nodig.

![Doos joystick](/Images/DoosJoystick.png "Doos met alle schroefdraadbussen")

![Schroefdraadbussen doos](/Images/SchroefdraadCloseUp.png "Close-up schroefdraadbussen")

![Gleuf voor moer](/Images/GleufjesMoeren.png "Gleuven voorzien voor moeren")

![Moer stuurstang](/Images/MoerStuurstang.png "Vastgezette moer stuurstang")

![Bovenkant joystick](/Images/BovenkantJoystick.png "Bovenkant joystick met metalen plaat")

![Deksel met joystick](/Images/DekselJoystick.png "Deksel voor de doos op de joystick")

![Onderkant joystick](/Images/OnderkantJoystick.png "Onderkant joystick groene stukken voor richtingbepaling")

### Stap 2: Voorbereiding bekabeling

Knip 3 rode kabels van ±140cm lang en 7 kabels van ± 20cm lang.
Knip 3 zwarte kabels van ± 20cm lang.
Ontmantel alle kabels zodat ±1cm isolatie van de draad verwijderd is.

Bevestig een female jumper connector aan het uiteinde van 2 lange rode flexibele kabels en plaats ze in een plastic pin behuizing met behulp van de krimptang.
Vertin het andere uiteinde en bevestig hier kabelschoentjes aan. Label de 2 kabels met respectievelijk links en rechts.
Vertin beide uiteinden van de laatste lange rode kabel en plaats op één uiteinde een wago-connector. Label deze kabel met 5V.

Vertin alle uiteinden van de 7 stukken rode kabel. Bevestig kabelschoentjes aan 2 korte rode kabels en vertin het ander uiteinde.
Plaats deze 2 rode kabels samen met de lange rode kabel in een wago-connector.
Bevestig kabelschoentjes aan 2 korte rode kabels en plaats op beide uiteinden een wago.
Label deze 2 kabels met respectievelijk vooruit en achteruit.

Vertin alle uiteinden van de 3 korte zwarte kabels en bevestig kabelschoentjes aan 2 van deze kabels. Plaats twee kabels samen in een wago-connector.

**Opmerking:**
Als alternatief voor het vertinnen van de koperen kabels kan ook een adereindhuls gebruikt worden.

![Jumper connector uiteinde](/Images/JumperConnector.png "Twee jumper connectors")

![5V connector](/Images/Wago5V.png "Wago om de 5V door te lussen")

![5V connector full view](/Images/Wago5VFullView.png "Wago om de 5V door te lussen")

![Ground connector](/Images/WagoGroundCloseUp.png "Wago om de ground door te lussen")

### Stap 3: Verbinding motor driver

Verbind 3 korte rode kabels met de motordriver respectievelijk met OUT1, OUT2 en +12V verbind alle uiteinden van de kabels met een wago.

Verbind 1 korte zwarte draad met de motordriver respectievelijk met GND en verbind het uiteinde van de draad met een wago.

Verbind de 5V kabel met de 5V pin op de motordriver.

Verbind de linkse gelabelde kabel met de IN1 en de rechts gelabelde kabel met de IN2.

![Bovenkant motordriver](/Images/MotorDriverFront.png "Bovenaanzicht motordriver")

![Onderkant motordriver](/Images/MotorDriverBack.png "Onderaanzicht motordriver")

![Pin aansluiting jumper connector](/Images/ConnectIN1-IN2.png "Vooraanzicht motordriver")

### Stap 4 Kill-switch maken

Knip 1 rode kabel van 1m40 lang en 1 zwarte kabel van 1m40 lang.
Ontmantel beide kabels zodat ongeveer 1cm van de isolatie verwijderd is, vertin één kant van de beide kabels en maak de vorm van een haakje, vertin het andere uiteinde.
Vijs de haakjes die gemaakt werden vast aan de kill-switch en plaats op het andere uiteinden van de rode en zwarte draad een wago.

![Aansluiting kill-switch](/Images/BekabelingKillSwitch.png "Aansluiting kabels killswitch")

![Vorm koper draad](/Images/VormKabelKillSwitch.png "Vorm haakje koper draad")
