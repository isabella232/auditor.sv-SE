---
description: Denna referens innehåller mer information om de tester som granskaren utför.
seo-description: Denna referens innehåller mer information om de tester som granskaren utför.
seo-title: Testreferens
title: Testreferens
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 78105ff6766f48f3aaccfeda281e5b4883be856a

---


# Testreferens{#test-reference}

Denna referens innehåller mer information om de tester som granskaren utför.

**Aktuell rubric-testversion:** 1.0.5

Varje test viktas. Testpoängen är lika med den tilldelade vikten. Om du klarar ett test med en vikt på fem får du fem poäng.

* 0: Aviserar dig om problem som du bör vara medveten om, men som inte påverkar ditt resultat.
* 1: Rekommenderar en optimering. Ingen inverkan på datakvaliteten.
* 2: Om du inte gör det här testet får du inte tillgång till de senaste funktionerna och korrigeringarna i Experience Cloud.
* 3: Testar effektiviteten och huruvida implementeringen följer bästa praxis.
* 4: Fel innebär att du kanske samlar in otillförlitliga data.
* 5: Fel innebär att du kan se dataförlust.

Testerna godkänns/misslyckas. De kontrollerar om testvillkoren är uppfyllda eller inte, så det finns inga partiella poängvärden för partiell överensstämmelse. Om testet till exempel söker efter den senaste versionen av en Adobe-lösning och du bara är en version efter, får du samma resultat som om du är fem versioner tillbaka. De senaste versionerna innehåller prestandaförbättringar och felkorrigeringar, så du bör använda den senaste versionen.

Vi **rekommenderar** att du korrigerar alla resultat för nivå 4 till 5.

Vi **rekommenderar** att du korrigerar alla resultat för nivå 1 till 3.

## Vilka Adobe-tekniker betygsätter Auditor? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analyser
* DTM
* Experience Cloud ID Service (tidigare Marketing Cloud ID Service)
* Mål

Följande Adobe-lösningar ingår för närvarande inte i testmomentet. Stöd för dessa lösningar planeras för framtida uppdateringar.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Starta
