# testcontainers-workshop-javatest101
Testcontainers Java 101 opdracht

# Opdracht

Doel van deze opdracht is om de Docker Image van de vorige opdracht te testen m.b.v. Testcontainers en Playwright.
Dit voorbeeldproject is een Java-project, waarbij de testscripts dus in Java worden geschreven.

De Testcontainers-java library is de implementatie van Testcontainers die ervoor zorgt dat alle containers netjes
worden gestart voordat de test begint, en na afloop weer worden opgeruimd.

Playwright is de browser-automation library van Microsoft die we gebruiken om met de browser de web-applicatie, die in de container draait, te kunnen testen.

## Bouwen van het testproject
Voordat we testen kunnen draaien en toevoegen aan het project moeten we de code eerst compileren (bouwen).
Bij voorkeur doen we dit met [IntelliJ](https://www.jetbrains.com/idea/download/) of [VS Code met de Java Plugin](https://code.visualstudio.com/docs/languages/java#_install-visual-studio-code-for-java)

Als je je IDE hebt opgestart kan je de test openen in 
``src/test/nl/salves/workshop/testcontainers/JavaTest.java``

## Toevoegen eigen testgeval
In de JavaTest zijn Testcontainers en Playwright al geconfigureerd.
De Testcontainer is geconfigureerd om een container te starten o.b.v. de Image die we in de vorige opdracht zelf gebouwd hebben.
De Playwright fixture start playwright zelf op en geeft aan hoe we weten dat de container is opgestart.

## Dynamische poorten
De netwerkpoorten waarop we de testcontainers kunnen benaderen zijn altijd dynamisch.
Testcontainers doet dit om zo altijd een stabiele testomgeving te bieden, want op een PC of Build Pipeline zijn bepaalde poorten
nu eenmaal al bezet. Testcontainers lost dit probleem dus op door altijd dynamisch een vrije poort te kiezen.

De API van Testcontainers biedt de mogelijkheid deze poort op te vragen, zodat we Playwright naar het juiste adres kunnen sturen
om onze applicatie te openen in een browser.

Als de container is gestart en Playwright ook een browser heeft geopend, is de testopzet klaar en kunnen we onze
concrete testgevallen gaan werken. Als voorbeeld is er al 1 test geimplementeerd, die een bepaalde tekst opzoekt op de website.

## Afronden opdracht
Rond deze opdracht af door een of meer slagende testcases toe te voegen aan de ``JavaTest`` class.

Voeg je wijzigingen toe met een ``git commit`` en ``git push`` dit naar deze Git-repo. Je kan de test ook in de UI
van GitHub.com zelf aanpassen.

## Na afloop
Na afloop hoef je niets op te ruimen. Dit doet Testcontainers automatisch voor je. Super makkelijk toch?s