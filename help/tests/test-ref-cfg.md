---
description: Den här referensen innehåller mer information om de tester som Adobe Experience Platform Auditor utför för konfiguration.
seo-description: Den här referensen innehåller mer information om de tester som Adobe Experience Platform Auditor utför för konfiguration.
seo-title: Konfiguration
title: Konfiguration
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 5%

---


# Konfiguration

Den här referensen innehåller mer information om de tester som Adobe Experience Platform Auditor utför för konfiguration.

Konfigurationstester söker efter specifika inställningar, värden eller potentiella konflikter i implementeringen. Platform Auditor utvärderar taggarna mot andra regler och rekommenderade metodtips.

<table id="table_A8A1FC360482447185C8460A18426638"> 
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
    --> <p><b>Advertising Cloud - Konverteringsnamn innehåller endast alfanumeriska tecken</b> </p> <p>Bredd: 3 </p> </td> 
   <td colname="col2"> <p>Parametern <span class="codeph"> ev_conversion_property_name</span> får bara innehålla numeriska och decimala värden EXCEPT för parametern "<span class="codeph"> ev_transid</span>" ( <span class="codeph"> värdet ev_transid</span> kan innehålla text eller numeriska värden) </p> <p>Leta efter <span class="codeph"> everesttech.net</span> -pixlar som innehåller en URL-parameter som börjar med <span class="codeph"> ev_</span>. </p> <p>Exempel: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Kontrollera att egenskapsparametrarna för transaktionen bara innehåller numeriska och decimala värden. </p> <p> <p>Varning:  Andra värdetyper kan orsaka dataförlust. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Konverteringsnamn använder URL-säkra tecken</b> </p> <p>Bredd: 1 </p> </td> 
   <td colname="col2"> <p> Namn på konverteringsegenskaper får inte innehålla ett et-tecken eller frågetecken. </p> <p> Exempel: </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Se till att egenskapsparametrarna för transaktioner inte innehåller ett icke-kodat et-tecken eller frågetecken. Dessa bryter URL-formatet. </p> <p> <p>Varning: Egenskapsparametrar som innehåller ett icke-kodat et-tecken eller frågetecken (till exempel: <span class="codeph"> ev_formComplete?=1</span> eller <span class="codeph"> ev_formComplete&amp;Submit=1</span>), kan resultera i dataförlust. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Transaktions-ID har implementerats korrekt</b> </p> <p>Bredd: 1 </p> </td> 
   <td colname="col2"> <p> Egenskapsnamnet <span class="codeph"> ev_transid=</span> får inte vara tomt. </p> <p>Exempel: </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Egenskapsnamnet <span class="codeph"> ev_transid=</span> får inte lämnas utan ett värde (<span class="codeph"> ev_transid=</span>). Om detta lämnas utan ett värde kan transaktionsdata gå förlorade. Tilldela ett värde till <span class="codeph"> ev_transid=</span> eller ta bort parametern från pixeln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analyser - instansierat i DOM</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics-koden är inte installerad eller kan inte köras. Returnerar 0 när ingen analyskod finns på webbsidan. </p> </td> 
   <td colname="col3"> <p>Kontrollera att Analytics-taggen implementeras på sidan och inte blockeras av efterföljande skriptaktiviteter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analyser - instansierad en gång</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics-koden upptäcktes mer än en gång på sidan. . Returnerar 0 när ingen analyskod finns på webbsidan. </p> </td> 
   <td colname="col3"> <p>Kontrollera att det bara finns en Analytics-tagg på sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Senaste versionen</b> </p> <p>Bredd: 3 </p> <p><a href="https://docs.adobe.com/content/help/sv-SE/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Dina sidor kör inte den senaste versionen av kodbiblioteket för Analytics. Kodbibliotek som används av Experience Cloud-teknik uppdateras och ändras ständigt för att dra nytta av prestandaförbättringar och tillhandahålla de senaste funktionerna. Returnerar 0 när ingen analyskod finns på webbsidan. </p> </td> 
   <td colname="col3"> <p>Installera den senaste versionen av Analytics-biblioteket. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - tredjepartstaggar läses in asynkront efter DOM-klart</b> </p> <p>Bredd: 1 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/resources/load-order.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>För att skapa en balans mellan en bra användarupplevelse och insamling av korrekta data bör tredjepartstaggar aktiveras vid DOM ready. Detta säkerställer att dessa spårningsskript körs utan att webbplatsfunktionaliteten påverkas. </p> </td> 
   <td colname="col3"> <p>Lös det här problemet genom att justera alla regler som kör pixlar från tredje part som ska utlösas på DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-tjänst - senaste version</b> </p> <p>Bredd: 2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Dina sidor kör inte den senaste versionen av kodbiblioteket för Visitor ID-tjänsten, <span class="codeph"> visitorAPI.js</span>. Kodbibliotek som används av Experience Cloud-teknik uppdateras och ändras ständigt för att dra nytta av prestandaförbättringar och tillhandahålla de senaste funktionerna. </p> </td> 
   <td colname="col3"> <p>Installera den senaste versionen av tjänstbiblioteket för Visitor-ID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Senaste version</b> </p> <p>Bredd: 2 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>De här sidorna kör inte den senaste versionen av kodbiblioteket för plattformsstart (Turbine). Kodbibliotek som används av Experience Cloud-teknik uppdateras och ändras ständigt för att dra nytta av prestandaförbättringar och tillhandahålla de senaste funktionerna. </p> </td> 
   <td colname="col3"> <p> Uppdatera plattformsstartbiblioteket genom att återskapa och publicera plattformsstartbiblioteket. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Mål - senaste version</b> </p> <p>Bredd: 2 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Dina sidor kör inte den senaste versionen av kodbiblioteket Target. Kodbibliotek som används av Experience Cloud-teknik uppdateras och ändras ständigt för att dra nytta av prestandaförbättringar och tillhandahålla de senaste funktionerna. </p> </td> 
   <td colname="col3"> <p>Installera den senaste versionen av målbiblioteket. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Mål - mboxDefault föregår mboxCreate </b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>Den korrekta användningen av <span class="codeph"> mboxCreate</span> ser ut ungefär så här: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Kundinnehåll—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Se till att du tar med en <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> -tagg innan du anropar <span class="codeph"> mboxCreate()</span>. at.js kommer inte att lägga till en åt dig. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Mål - Giltig DOCTYPE</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/help/en/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> En ogiltig DOCTYPE upptäcktes. Inga lådor kommer att utlösas i det här scenariot. </p> <p>För at.js måste DOCTYPE vara i standardläge, annars fungerar inte Target. </p> </td> 
   <td colname="col3"> <p>Uppdatera DOCTYPE på sidan. </p> </td> 
  </tr> 
 </tbody> 
</table>

