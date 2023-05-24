---
description: Den här referensen innehåller mer information om de tester som Adobe Experience Platform Auditor utför för att kontrollera om taggar finns.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs for tag presence.
seo-title: Tag presence
title: Tagg presence
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
exl-id: a6ac4d95-2f96-4abb-b39b-4dd0d8df5fe8
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 5%

---

# Tagg presence

Den här referensen innehåller mer information om de tester som Adobe Experience Platform Auditor utför för att kontrollera om taggar finns.

Plattformsgranskaren utvärderar om taggen finns och om den finns på rätt plats i sidkoden.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Test </th> 
   <th colname="col2" class="entry"> Kriterier </th> 
   <th colname="col3" class="entry"> Rekommendation </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - kodnärvaro</b> </p> <p>Bredd: 5 </p> </td> 
   <td colname="col2"> <p> Advertising Cloud-taggen är inte tillgänglig i DOM. </p> </td> 
   <td colname="col3"> <p>Implementera taggen Advertising Cloud med tillägget Advertising Cloud för Adobe Experience Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - segmentpixel implementerad</b> </p> <p>Bredd: 5 </p> </td> 
   <td colname="col2"> <p> Uppgradera dina Advertising Cloud-segmentpixlar till de nya Advertising Cloud-taggar som bara innehåller bilder. Om du använder de föråldrade AMO-segmenttaggarna kan data gå förlorade. </p> </td> 
   <td colname="col3"> <p>Implementera Advertising Cloud-segmentpixeln med tillägget Advertising Cloud för Platform launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analyser - läses in i DOM</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Det gick inte att identifiera Adobe Analytics-taggen. </p> </td> 
   <td colname="col3"> <p>Installera den senaste versionen av Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Biblioteket har lästs in</b> </p> <p>Bredd: 5 </p> <p>Ytterligare information: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM-felsökning</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Lägg till sidhuvuds- och sidfotskod</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Det gick inte att hitta ett globalt _satellitobjekt i DOM. Dynamic Tag Management är inte installerat eller kan inte köras. </p> </td> 
   <td colname="col3"> <p>Kontrollera att DTM-biblioteket är implementerat på sidan och inte blockeras av efterföljande skriptaktiviteter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - En inbäddningskod</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Produktionsplatser bör bara läsa in ett DTM-bibliotek. </p> </td> 
   <td colname="col3"> <p>Kontrollera att det bara är produktionsbiblioteket som läses in på sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom-återanrop finns i &lt;body&gt;</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellit.pageBottom()</span> callback-funktionen hittades inte i <span class="codeph"> &lt;body&gt;</span> på sidan, vilket krävs av Dynamic Tag Management. </p> <p>Testet misslyckas om <span class="codeph"> pageBottom </span>anropet inte finns på sidan eller om det finns på sidan <span class="codeph"> &lt;head&gt;</span> -tagg (eller någon annan oväntad plats). Det går bara om <span class="codeph"> pageBottom</span> finns någonstans i <span class="codeph"> &lt;body&gt;</span> -tagg. Om den inte finns på sidan alls fungerar den inte och de andra två <span class="codeph"> pageBottom</span> testerna kommer också att misslyckas. </p> </td> 
   <td colname="col3"> <p>Lägg till det infogade skriptet omedelbart före stängningen <span class="codeph"> &lt;/body&gt;</span> -tagg för att säkerställa korrekt DTM-funktionalitet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom-tagg utlöses</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> The DTM <code> pageBottom</code> -taggen kunde inte identifieras. </p> <p>Detta kan inträffa om samtalet sker inom en <code> if</code> programsats som resulterar i något liknande <code> if (false) {_satellite.pageBottom()}</code>. Även om taggen kan finnas och placeras på rätt sätt kanske den ändå inte fungerar. </p> </td> 
   <td colname="col3"> <p>Installera DTM <code> pageBottom</code> på alla sidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-tjänst - kodnärvaro</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>Det gick inte att hitta Experience Cloud ID-tjänstkoden. Experience Cloud ID (MCID) rekommenderas för att du ska få ut så mycket som möjligt av dina Experience Cloud-lösningar och för att ID-hanteringen ska fungera i alla Experience Cloud-lösningar. </p> </td> 
   <td colname="col3"> <p> Installera den senaste versionen av MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-tjänst - cookie-närvaro</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/tools/macid.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> AMCV_</span> Det gick inte att hitta cookie. Du måste instansiera ett besökarobjekt från <span class="codeph"> VisitorAPI.js</span> kod. </p> </td> 
   <td colname="col3"> <p> Om det här är en DTM-implementering kontrollerar du att AdobeOrg-id:t har angetts korrekt i MCID-verktyget. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Experience Cloud ID-tjänst - MID-värde finns</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/sv-SE/id-service/using/intro/cookies.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> MID-värdet hittades inte i <span class="codeph"> AMCV_</span> cookie. </p> </td> 
   <td colname="col3"> <p>Testa igen för att kontrollera om det finns någon MCID API-fördröjning. Kontakta Adobe kundtjänst om problemet kvarstår. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b> Starta - Biblioteket har lästs in</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Det gick inte att hitta ett globalt _satellitobjekt i DOM. platforma launchen är inte installerad eller kan inte köras. </p> </td> 
   <td colname="col3"> <p>Kontrollera att Platforma launchen är implementerad på sidan och inte blockeras av efterföljande skriptaktiviteter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - Not have multiple embed scripts</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>Det får inte finnas flera inbäddade skript inlästa på sidan. Produktionsplatser bör bara läsa in ett Platform launch-bibliotek. </p> </td> 
   <td colname="col3"> <p>Kontrollera att det bara är produktionsbiblioteket som läses in på sidan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom-återanrop finns i &lt;body&gt;</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> The <span class="codeph"> _satellit.pageBottom()</span> callback-funktionen hittades inte i <span class="codeph"> &lt;body&gt;</span> på sidan, vilket krävs som Platform launch. </p> <p>Testet misslyckas om <span class="codeph"> pageBottom </span>anropet inte finns på sidan eller om det finns på sidan <span class="codeph"> &lt;head&gt;</span> -tagg (eller någon annan oväntad plats). Det går bara om <span class="codeph"> pageBottom</span> finns någonstans i <span class="codeph"> &lt;body&gt;</span> -tagg. Om den inte finns på sidan alls fungerar den inte och de andra två <span class="codeph"> pageBottom</span> testerna kommer också att misslyckas. </p> </td> 
   <td colname="col3"> <p>Lägg till det infogade skriptet omedelbart före stängningen <span class="codeph"> &lt;/body&gt;</span> för att säkerställa att Platforma launchen fungerar som den ska. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - pageBottom-återanrop ska inte finnas när den distribueras asynkront</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>The <span class="codeph"> _satellit.pageBottom()</span> återanrop hittades på sidan, vilket inte bör vara fallet när Platform launch distribueras asynkront. </p> </td> 
   <td colname="col3"> <p>Ta bort<span class="codeph"> _satellit.pageBottom()</span> skript för att aktivera rätt Platform launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Mål - kod finns</b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p>Målet ska definieras i DOM. </p> </td> 
   <td colname="col3"> <p>Installera den senaste versionen av Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Mål - Biblioteket har lästs in i &lt;head&gt;</b> </p> <p>Bredd: 4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Målbiblioteket ska läsas in i <span class="codeph"> &lt;head&gt;</span> -tagg. </p> </td> 
   <td colname="col3"> <p> Kontrollera att målbiblioteket har lästs in i <span class="codeph"> &lt;head&gt;</span> -tagg. </p> </td> 
  </tr> 
 </tbody> 
</table>
