---
description: Den här referensen innehåller mer information om de aviseringar som visas i Adobe Experience Platform Auditor för tester.
seo-description: Den här referensen innehåller mer information om de aviseringar som visas i Adobe Experience Platform Auditor för tester.
seo-title: Larm
title: Larm
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 1%

---


# Larm{#alerts}

Den här referensen innehåller mer information om de aviseringar som visas i Adobe Experience Platform Auditor för tester.

Varningar visar problem som du bör vara medveten om, men som inte påverkar ditt poängtal. Det här är rekommendationer om god praxis som i vissa fall kanske inte gäller din implementering.

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterier </th> 
   <th colname="col3" class="entry"> Rekommendation </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Korrigera konverteringstagg har implementerats</b> </p> <p>Bredd: 0 </p> </td> 
   <td colname="col2"> <p>Kontrollera om rätt konverteringstagg används. </p> <p> <p>Varning:  Om du använder de föråldrade konverteringstaggarna för TubeMogul kan data gå förlorade. </p> </p> </td> 
   <td colname="col3"> <p>Uppgradera dina konverteringspixlar till de nya konverteringstaggarna för Advertising Cloud-bilder. </p> <p>Detta kan du enkelt göra med Advertising Cloud-tillägget för Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Korrigera JS-tagg som används</b> </p> <p>Bredd: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud bör använda de senaste JavaScript-taggarna. </p> </td> 
   <td colname="col3"> <p>Uppgradera Advertising Cloud JavaScript till den senaste versionen. Om du använder de inaktuella JavaScript-versionerna kan du förlora funktioner. </p> <p>Detta kan göras enklare genom att använda Advertising Cloud-tillägget för Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Tagg för endast bild</b> </p> <p>Bredd: 0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud bildpixelformat bör matcha något av följande rekommenderade format: </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> /rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> /rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> /pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>Uppgradera dina Advertising Cloud-pixlar till de nya Advertising Cloud-taggar som säkerställer att du utnyttjar alla funktioner i Advertising Cloud. </p> <p>Det är enklast att göra med Advertising Cloud-tillägget för Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Synkronisering av pixlar DSP segment aktiverat</b> </p> <p>Bredd: 0 </p> </td> 
   <td colname="col2"> <p>Kontrollera om TubeMogul-segmentpixeln innehåller en DSP synkroniseringsinställning och rekommendera att inställningen läggs till i pixeln. </p> <p>Inställningen DSP synkronisering bestäms av användningen av en frågesträngsparameter, så </p> <p>OM taggen skickas till<span class="codeph"> ("https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;")</span> </p> <p> ELLER <span class="codeph"> "/rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> ELLER <span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>OCH taggen innehåller URL-parametern <span class="codeph"> "sid=")</span> </p> <p>Kontrollera sedan om URL-parametern <span class="codeph"> "cs=0"</span> eller<span class="codeph"> "cs=1"</span> finns och om den inte rekommenderar att <span class="codeph"> "cs=1"</span> läggs till i pixlarna så att målgruppens matchningsfrekvens kan förbättras. </p> </td> 
   <td colname="col3"> <p> Lägg till URL-parametern <span class="codeph"> "cs=1"</span> i dina Advertising Cloud-pixlar så att DSP kan synkroniseras, vilket ökar målgruppsmatchningen. </p> <p>Det är enklast att göra detta med Advertising Cloud-tillägget för Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - sidans nedre återanropsplacering</b> </p> <p>Bredd: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Ytterligare information</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamisk tagghantering kräver funktionen <span class="codeph"> _satellit.pageBottom()</span> . Lägg till det infogade skriptet omedelbart före den avslutande <span class="codeph"> &lt;/body&gt;</span> -taggen för att säkerställa korrekt DTM-funktionalitet. </p> <p> <p>Obs! Det är bäst att använda taggen som den <i>sista</i> taggen i <span class="codeph"> &lt;body&gt;</span>. Om den hittas i <span class="codeph"> &lt;body&gt;</span> -taggen har den en chans att fungera, men eftersom det inte är en bra metod kan den fungera felaktigt eller med oväntade eller oönskade resultat. </p> </p> </td> 
   <td colname="col3"> <p>Lägg till det infogade skriptet omedelbart före den avslutande <span class="codeph"> &lt;/body&gt;</span> -taggen för att säkerställa korrekt DTM-funktionalitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - Self-Hosted</b> </p> <p>Bredd: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> DTM-biblioteket ligger på Adobe Akamai-instansen på <span class="filepath"> assets.adobedtm.com</span>. </p> <p> Självvärdande är det rekommenderade sättet att läsa in DTM eftersom det ger bättre kontroll över webbplatsens prestanda genom cachekontroll, minskar beroenden av skript från tredje part och ger större kontroll över publiceringsprocessen. DTM-biblioteken kan hanteras via din egen webbhosting eller CDN. </p> </td> 
   <td colname="col3"> <p>Självvärdande är det rekommenderade sättet att läsa in DTM på en sida. Även om DTM-värdtjänster via Akamai CDN fungerar i de flesta fall, förbättras sidprestanda av självvärdtjänster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Experience Cloud ID-tjänst - använd endast en AdobeOrg</b> </p> <p>Bredd: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/id-request.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>I en normal MCID-implementering bör en enda AdobeOrg användas. </p> </td> 
   <td colname="col3"> <p>Verifiera att det finns flera AdobeOrg ID:n för den här implementeringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom callback placement</b> </p> <p>Bredd: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Ytterligare information</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>Platform Launch ska ha en <span class="codeph"> pageBottom- </span>callback-funktion som är sist definierad i sidans brödtext om den distribueras synkront. </p> <p> <p>Obs! Det är bäst att använda taggen som den <i>sista</i> taggen i <span class="codeph"> &lt;body&gt;</span>. Om den hittas i <span class="codeph"> &lt;body&gt;</span> -taggen har den en chans att fungera, men eftersom det inte är en bra metod kan den fungera felaktigt eller med oväntade eller oönskade resultat. </p> </p> </td> 
   <td colname="col3"> <p>Platform Launch kräver funktionen <span class="codeph"> _satellit.pageBottom()</span> för synkrona distributioner. Lägg till det infogade skriptet omedelbart före den avslutande <span class="codeph"> &lt;/body&gt;</span> -taggen för att säkerställa rätt plattformsstartfunktion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Self-Hosted</b> </p> <p>Bredd: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Komma igång med Adobe Experience Platform Launch</a> </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> asynkron distribution av plattformsinstallation</a> </p> </td> 
   <td colname="col2"> <p>Plattformsstartbiblioteket ligger på Adobe Akamai-instansen på <span class="filepath"> assets.adobedtm.com</span>. </p> <p>Självvärdande är det rekommenderade sättet att läsa in Platform Launch eftersom det ger bättre kontroll över webbplatsens prestanda genom cachekontroll, minskar beroenden av skript från tredje part och ger större kontroll över publiceringsprocessen. Plattformsstartbiblioteken kan lagras och hanteras via din egen webbhosting eller CDN. </p> </td> 
   <td colname="col3"> <p>Även om hosting via Akamai CDN fungerar i de flesta fall rekommenderar vi att du implementerar självbetjäning som ett första steg i att förbättra sidans prestanda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - ska distribueras asynkront</b> </p> <p>Bredd: 0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>Plattformsuppstart ska distribueras asynkront för optimala prestanda. </p> </td> 
   <td colname="col3"> <p>Inkludera den asynkrona parametern i det infogade skriptet för att säkerställa rätt asynkrona startfunktioner för plattformen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Mål - Innehåll i mboxDefault</b> </p> <p>Bredd: 0 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Innehållet ska finnas i mboxDefault när at.js används. </p> </td> 
   <td colname="col3"> <p>Kontrollera att innehållet är tillgängligt. </p> </td> 
  </tr> 
 </tbody> 
</table>

