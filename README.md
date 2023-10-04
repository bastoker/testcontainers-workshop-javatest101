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
``src/test/nl/salves/workshop/testcontainers/JavaTest101.java``
