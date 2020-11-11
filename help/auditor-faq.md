---
description: Vanliga frågor och svar om Adobe Experience Platform Auditor
seo-description: Vanliga frågor och svar om Adobe Experience Platform Auditor
seo-title: Vanliga frågor om Adobe Experience Platform Auditor
title: Vanliga frågor om Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 3%

---


# Vanliga frågor om Adobe Experience Platform Auditor{#auditor-faq}

I den här artikeln finns svar på vanliga frågor om Adobe Experience Platform Auditor.

* [Vad är Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Är mitt företag berättigat att använda Platform Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Vilka Adobe-tekniker betygsätter Platform Auditor?](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Hur många granskningar kan jag göra?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [Vad crawlas för en granskning?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Hur lång tid tar en revision?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Vilken information finns i en rapport?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Hur användbar är informationen?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Kan plattformsrevisor granska icke-Adobe-teknik?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Kan jag godkänna mina IP-adresser för att tillåta skanning av sidor..](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Använder plattformsgranskaren samma IP-intervall som observationspunkten?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## Vad är Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor är en tjänst inom Adobe Experience Cloud som utvecklats i samarbete med ObservePoint, experter på validering av digitala implementeringar.

Med Platform Auditor kan man skanna upp till 500 webbsidor i taget och få en rapport som visar hur man kan förbättra sina Adobe Experience Cloud-implementeringar så att man får hela värdet av sin investering i Adobe.

## Är jag berättigad att använda Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

Alla Adobe Experience Cloud kundorganisationer har kostnadsfri tillgång till Platform Auditor (från och med den 1 maj 2018). Varje användare måste ge sitt samtycke till Adobe/ObservePoint-användningsvillkoren i Adobe Experience Cloud användargränssnitt innan de kan använda funktionen. Kontakta din kontoansvarige om du vill avanmäla dig från villkoren.

## Hur får jag åtkomst till Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. Du kan också gå direkt till [https://auditor.adobe.com](https://auditor.adobe.com).

## Vilka Adobe-tekniker betygsätter Platform Auditor? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics 
* DTM
* Experience Cloud ID-tjänst (tidigare Marketing Cloud ID-tjänst)
* Målgrupp

Följande Adobe-lösningar ingår för närvarande inte i testmomentet. Stöd för dessa lösningar planeras för framtida uppdateringar.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch

## Hur många granskningar kan jag göra? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Det finns ingen gräns för hur många granskningar du kan köra. Användare är begränsade till en granskning som körs åt gången. Ett fel uppstår om du försöker starta en granskning med samma inställningar som den som körs.

## Vad crawlas för en granskning? {#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint-tekniken crawlar för närvarande URL:er som finns i dokumentlänkar. Länkar som hittas i knappar, sidnumreringswidgetar och andra sådana sidelement crawlas inte.

## Hur föreslår jag nya kriterier för plattformsgranskningstester? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Hur lång tid tar en revision? {#section-5086ae27ef1f4671a9d951348654633a}

Det finns många faktorer som bidrar till den tid det tar att slutföra en revision, bland annat:

* Inläsningstid för sida

   ObservePoint-motorn läser in varje sida i granskningen i en webbläsare. Ju snabbare en sida läses in, desto snabbare slutförs granskningen.
* Samtidiga anslutningar

   Plattformsrevisorn använder en enda anslutning för att besöka varje sida. För fullständiga ObservePoint-konton används så många som 10 motorer samtidigt.
* Nätverkstystnad

   När varje sida har lästs in väntar granskningen på en nätverkstystnad på sju sekunder innan nästa sida öppnas. Om en sida skickar många nätverksbegäranden som inträffar efter att sidan har lästs in, kommer väntetiden att gå ut efter 60 sekunder.
* Återkommande sidor

   Om det inte går att hitta en sida eller tagg lagrar granskningen den URL-adressen och återgår till den senare vid granskningen. Granskningen kommer att besöka en sida upp till tre gånger för att säkerställa att felet inte orsakades av ett tillfälligt problem.
* Bearbetar

   När en granskning har slutförts behandlas och filtreras alla insamlade data enligt reglerna. Bearbetningstiden är betydande, men det tar inte lika lång tid som själva skanningen.

>[!NOTE]
>
>Platform Auditor kör en genomsökning åt gången. Fullständiga ObservePoint-konton kan köra många granskningar i följd.

## Vilken information finns i en rapport? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Varje skanning genererar en rapport som visar vilka URL:er som har skannats, problem som har hittats på dessa webbsidor och rekommendationer för hur problemen ska åtgärdas.

Resultat från inskannade inskannade dokument är uppdelade i tre kategorier:

* Konfiguration
* Taggkonsekvens
* Tagg finns

Utöver dessa tre kategorier innehåller rapporten varningar som innehåller information som du bör känna till, men som inte nödvändigtvis kräver omedelbara åtgärder.

Rekommendationerna som ingår i dessa kategorier delas sedan in i tre ytterligare kategorier:

* Rekommenderas varmt
* Rekommenderas
* Godkänd

## Hur användbar är informationen? {#section-9308c1ea882048b781087ae6d2eee9f0}

Alla rekommendationer som ges via Platform Auditor är avsedda att hjälpa dig att vidta åtgärder för att åtgärda ett problem med implementeringen av Adobe Experience Cloud-lösningar, som DTM eller Target. För att underlätta detta har Platform Auditor-teamet arbetat mycket med att ge mycket detaljerade anvisningar om vad som behöver göras där. Du kan exportera ett kalkylblad med alla skannade URL:er och alla testresultat så att du enkelt kan identifiera problemområden. Här är ett exempel på en rekommendation för en DTM-implementering:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom callback last</b> </p> <p>Funktionen _satellit.pageBottom() krävs för en korrekt DTM-implementering. Lägg till det infogade skriptet omedelbart före den avslutande &lt;/body&gt;-taggen för att säkerställa korrekt DTM-funktionalitet. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Kan plattformsrevisor granska icke-Adobe-teknik? {#section-f6e73c56083b4815bbf901296038bcd4}

Nej. Med ObservePoints fulla erbjudande kan kunderna dock granska och övervaka alla era marknadsföringstaggar och tekniker. Som Adobe-kund har du tillgång till ett kostnadsfritt provkonto. Gå till [ObservePoints Platform Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium)för att få tillgång till ditt testkonto.

## Kan jag godkänna mina IP-adresser för att tillåta skanning av sidor som skyddas av inloggning? {#section-011e4f54c58140ffb93bedeb0745b6cc}

Den här funktionen stöds för närvarande inte utan det fullständiga ObservePoint-erbjudandet.

## Använder plattformsgranskaren samma IP-intervall som ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

Crawlningen utförs av ObservePoint, så samma IP-adresser används.

Mer information finns i dokumentationen [för](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ObservePoint.
