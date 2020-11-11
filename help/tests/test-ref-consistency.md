---
description: Den här referensen ger mer information om de tester som Adobe Experience Platform Auditor utför för att få en enhetlig tagg.
seo-description: Den här referensen ger mer information om de tester som Adobe Experience Platform Auditor utför för att få en enhetlig tagg.
seo-title: Konsekvens för taggar
title: Konsekvens för taggar
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 8%

---


# Konsekvens för taggar

Den här referensen ger mer information om de tester som Adobe Experience Platform Auditor utför för att få en enhetlig tagg.

Plattformsgranskarens konsekvenskonstester söker efter inkonsekvenser på alla skannade sidor. Detta är värden eller konfigurationer som ska vara desamma på alla sidor på webbplatsen för att säkerställa korrekt datainsamling.

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
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
    --> <p><b>Analyser - Konsekvent kodversion </b> </p> <p>Bredd: 5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/home.html" format="html" scope="external"> Ytterligare information</a> </p> </td> 
   <td colname="col2"> <p> Mer än en version av Analytics-koden hittades. </p> </td> 
   <td colname="col3"> <p>Ersätt alla instanser av Analytics med den aktuella versionen. </p> </td> 
  </tr> 
 </tbody> 
</table>
