---
description: Den här referensen ger mer information om de tester som Adobe Experience Platform Auditor utför för att få en enhetlig tagg.
seo-description: This reference provides more information about the tests Adobe Experience Platform Auditor performs for tag consistency.
seo-title: Tag consistency
title: Konsekvens för taggar
uuid: 16271dd6-3587-4f33-92f8-54ec4a3d6469
exl-id: 681cf2f8-e022-4fb0-a06a-b4986710f501
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

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
