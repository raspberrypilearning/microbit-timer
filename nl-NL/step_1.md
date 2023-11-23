Er kunnen momenten zijn waarop je iets moet timen.

Je kunt op de volgende manier een timer op de LED's tonen.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let seconde = 0; seconde <= 4; seconde++) {
        basic.showNumber(seconde + 1)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```

In deze code:

De `seconde`{:class='microbitvariables'} variabele neemt elke waarde aan van `0` tot het eindgetal (`4` in ons voorbeeld) en telt er elke keer één bij op.

De waarde van de `seconde`{:class='microbitvariables'} variabele wordt opgeteld bij `1` en het totaal wordt gedurende één seconde weergegeven op de LED's (de lengte van de tijd ingesteld in het `pauzeer (ms)`{:class='microbitbasic'} blok).

Nadat het laatste getal (`5`) is weergegeven, wordt het `toon pictogram`{:class='microbitbasic'} blok gebruikt om een muzieknoot te tonen en vervolgens worden de LED's uitgeschakeld door gebruik te maken van het `wis scherm`{:class='microbitbasic'} blok.

Het voorbeeld toont de timer die begint wanneer de micro:bit wordt geschud, maar je kunt hem ook instellen om te starten op andere gebeurtenissen; bijvoorbeeld wanneer er op een knop wordt gedrukt. Je kunt het ook in een functie zetten als je het op verschillende plaatsen in je code wilt aanroepen.

### Wijzig de duur van de timer

Je kunt de duur van de timer wijzigen door het tweede getal in het `voor`{:class='microbitloops'} blok te veranderen. Zet het op één minder dan het aantal waarop je wilt eindigen (vergeet niet dat het `+`{:class='microbitmath'} blok wordt gebruikt).

### Aftellen, niet optellen

Om een aftelling te creëren, moet je de waarde van de `seconde`{:class='microbitvariables'} variabele aftrekken van het eindgetal (`4` in dit voorbeeld) plus één (dus `5` in dit voorbeeld).

Zo zou je de code kunnen veranderen.

```microbit
input.onGesture(Gesture.Shake, function () {
    for (let seconde = 0; seconde <= 4; seconde++) {
        basic.showNumber(5 - seconde)
        basic.pause(1000)
    }
    basic.showIcon(IconNames.EighthNote)
    basic.clearScreen()
})
```
