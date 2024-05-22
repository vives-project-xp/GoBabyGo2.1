# motor testen
Om de werking te testen va, de verschillende motoren in de auto, is het mogelijk om de verschillende spanningen te meten op de aansluitpinnen van de motordrivers. In het geval van de voorwaardse en achterwaards beweging kan er gemeten worden op de moordriver die is meegeleverd et de auto. Deze driver stuurt de 2 motoren aan die aan de achterkant van de auto te vinden zijn.

![motordriver1](/Images/motordriver1.PNG "motordriver meegeleverd met de auto")

Hieronder zijn de verwachte waarden en de gemeten waarden te zien van de spanningen die over de motoren zouden komen
### verwachtingen
tests|Motor|opmerkingen
:---------------------|:------|:----------------------------------------------
joystick forward | 12V | motoren gaan vooruit
joystick backwards | -12V | motoren gaan achteruit
||
controller forward | 12V | motoren gaan vooruit
controller backwards | -12V | motoren gaan achteruit

### metingen
tests|Motor|opmerkingen
:---------------------|:------|:----------------------------------------------
joystick forward | 12,78V | motoren gaan vooruit
joystick backwards | -12,81V | motoren gaan achteruit
||
controller forward | 12,75V | motoren gaan vooruit
controller backwards | -12,77V | motoren gaan achteruit

Voor de stuurbeweging hebben we een extra motordriver moeten toevoegen aangezien deze beweging normaal gedaan werd door het draaien van het stuur. Er wordt nu gebruik gemaakt van de L298N motordriver, voor de sturing met de joystick, aangezien deze werd gebruikt in het project 'GoBabyGo 2.0' en werkt op 12V die geleverd wordt door de batterij. Door het gebruik van een extra motordriver is er een kleine spanningsval op de uitgang waar de stuurmotor aan verbonde wordt.

Wanneer we gebruik maken van een relais is het mogelijk om de 2 motordrivers te combineren. Op die manier kan gestuurd worden met de joystick en de afstandsbediening waar de 2de optie de voorang krijgt.

![motordriver1](/Images/motordriver2.PNG "extra motordriver")

Hieronder zijn de verwachte waarden en de gemeten waarden te zien van de spanningen die over de motor zou komen
### expectations
tests|Motor|opmerkingen
:---------------------|:------|:----------------------------------------------
joystick left | 7,4V | stuur links
joystick right | -7,4V | stuur rechts
||
controller left | 12V | stuur links
controller right | -12V | stuur rechts
### metingen
tests|Motor|opmerkingen
:---------------------|:------|:----------------------------------------------
joystick left | 8,1V | stuur links
joystick right | -7,95V  | stuur rechts
||
controller left | / | stuur links
controller right | / | stuur rechts

De reden waarom alle metingen hoger zijn dan de verwachte waarde is de spanning van de batterij. Normaal zou deze 12V moten zijn maar na het meten is deze 12,84V
