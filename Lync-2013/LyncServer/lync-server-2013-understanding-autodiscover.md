---
title: 'Lync Server 2013: Grundlegendes zu AutoErmittlung'
description: 'Lync Server 2013: Grundlegendes zu AutoErmittlung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Autodiscover
ms:assetid: d70a15b7-750b-4e0f-9a7f-0254d6d486c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945654(v=OCS.15)
ms:contentKeyID: 51541522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 295aba4bffbe5d17070702203cfd933284cb12c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394855"
---
# <a name="understanding-autodiscover-in-lync-server-2013"></a><span data-ttu-id="4c47d-103">Grundlegendes zu AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c47d-103">Understanding Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c47d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c47d-104">

<span> </span></span></span>

<span data-ttu-id="4c47d-105">_**Letztes Änderungsdatum des Themas:** 2013-06-03_</span><span class="sxs-lookup"><span data-stu-id="4c47d-105">_**Topic Last Modified:** 2013-06-03_</span></span>

<span data-ttu-id="4c47d-106">Der lync Server 2013-AutoErmittlungsdienst ist ein Feature, das ursprünglich in Microsoft lync Server 2010 als Teil des kumulativen Updates für lync Server 2010: November 2011 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="4c47d-106">The Lync Server 2013 Autodiscover Service is a feature that was originally introduced in Microsoft Lync Server 2010 as part of the Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="4c47d-107">Dieses kumulative Update hat nicht nur Korrekturen, sondern auch Unterstützung für lync Mobile-und lync 2013-Clients bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4c47d-107">In addition to fixes, this cumulative update delivered support for Lync Mobile and Lync 2013 clients.</span></span>

<span data-ttu-id="4c47d-108">In lync Server 2013 ist der AutoErmittlungsdienst ein integraler Bestandteil des Vorgangs externer und interner mobiler Clients, und die AutoErmittlung wird auch auf neue Clients ausgedehnt, wie etwa die kürzlich eingeführte lync Windows Store-App für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c47d-108">In Lync Server 2013, the Autodiscover Service is an integral part of the operation of external and internal mobile clients, and Autodiscover is also extended to new clients, such as the recently introduced Lync Windows Store app for Windows 8.</span></span> <span data-ttu-id="4c47d-109">Die AutoErmittlung wird auch von den lync 2013-Desktop Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-109">Autodiscover is also used by the Lync 2013 desktop clients.</span></span> <span data-ttu-id="4c47d-110">AutoErmittlung wird in lync Server durch die erforderlichen DNS-Einträge (Domain Name System) **lyncdiscover \<domain\> .**</span><span class="sxs-lookup"><span data-stu-id="4c47d-110">Autodiscover is recognized in Lync Server by the required domain name system (DNS) records **lyncdiscover.\<domain\>**</span></span> <span data-ttu-id="4c47d-111">und **lyncdiscoverinternal. \<domain\>**.</span><span class="sxs-lookup"><span data-stu-id="4c47d-111">and **lyncdiscoverinternal.\<domain\>**.</span></span> <span data-ttu-id="4c47d-112">Darüber hinaus bevorzugen neuere Versionen des lync 2010-und lync 2013-Desktop Clients die AutoErmittlung über die DNS-SRV-Einträge (Domain Name System), wobei nur DNS-SRV-Einträge verwendet werden, wenn lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="4c47d-112">Additionally, newer versions of the Lync 2010 and Lync 2013 desktop client prefer Autodiscover over the domain name system (DNS) SRV records, using DNS SRV records only if lyncdiscover.\<domain\></span></span> <span data-ttu-id="4c47d-113">oder lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="4c47d-113">or lyncdiscoverinternal.\<domain\></span></span> <span data-ttu-id="4c47d-114">antwortet nicht oder löst nicht auf.</span><span class="sxs-lookup"><span data-stu-id="4c47d-114">does not respond or does not resolve.</span></span> <span data-ttu-id="4c47d-115">Die lync Windows Store-App für Windows 8 und lync Mobile verwendet die AutoErmittlung ausschließlich und bezieht sich nicht auf die herkömmlichen DNS-SRV-Einträge.</span><span class="sxs-lookup"><span data-stu-id="4c47d-115">The Lync Windows Store app for Windows 8 and Lync Mobile uses Autodiscover exclusively and will not refer to the traditional DNS SRV records.</span></span>

<span data-ttu-id="4c47d-116">In lync Server 2013 wird die AutoErmittlung erweitert, um dem Client zu kommunizieren, welche Elemente, Features und Kommunikationsmethoden dem Client zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="4c47d-116">In Lync Server 2013, Autodiscover is expanded to communicate to the client which elements, features, and communication methods are available to the client.</span></span> <span data-ttu-id="4c47d-117">Die Informationen werden über eine Anforderung kommuniziert, die vom Client gesendet wird, und die lync Server-Webdienste antwortet mit einer klar definierten Antwort, mit der der Name der für den Client verfügbaren Namen und die Kontaktaufnahme mit diesen Features im Format des Auto Ermittlungs Antwortdokuments beantwortet werden.</span><span class="sxs-lookup"><span data-stu-id="4c47d-117">The information is communicated through a request that is sent from the client, and the Lync Server web services responds with a clearly defined response that names what is available to the client, and how to contact those features in the format of the Autodiscover Response document.</span></span>

<span data-ttu-id="4c47d-118">Die beste Methode, um das Antwortdokument für die AutoErmittlung zu verstehen, einschließlich der Art und Weise, wie die Webdienste Features an Clients über dieses Dokument übermitteln, besteht darin, jede Zeile in einer typischen Antwort des lync Web Service-Antwortdokuments für die automatische Erkennung zu analysieren und zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4c47d-118">The best way to understand the Autodiscover response document, including how the web services communicate features to clients through this document, is to dissect and define each line in a typical response from the Lync web service Autodiscover response document.</span></span>

<div class="">


> [!NOTE]  
> <span data-ttu-id="4c47d-119">In den Details, die Folgen, hat sich der Benutzer bereits auf dem Stammserver authentifiziert, indem er auf eine Authentifizierungsanforderung reagiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-119">In the details that follow, the user has already authenticated to the home server by responding to an authentication request.</span></span>



</div>

<div class="">


> [!NOTE]  
> <span data-ttu-id="4c47d-120">Der lync-Auto Ermittlungs-Webdienst ist in den <STRONG>Microsoft Office-Protokollen</STRONG> im Abschnitt <STRONG>Open Specifications</STRONG> der <STRONG>Microsoft Developer Network</STRONG> (MSDN)-Bibliothek definiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-120">The Lync Autodiscover Web Service is defined in the <STRONG>Microsoft Office Protocols</STRONG> in the <STRONG>Open Specifications</STRONG> section of the <STRONG>Microsoft Developer Network</STRONG> (MSDN) library.</span></span> <span data-ttu-id="4c47d-121">Ausführliche Informationen finden Sie im vollständigen Spezifikationsdokument "lync autodiscover Web Service Protocol" unter: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A> .</span><span class="sxs-lookup"><span data-stu-id="4c47d-121">For details, see the full specification document, "Lync Autodiscover Web Service Protocol," at: <A href="https://go.microsoft.com/fwlink/?linkid=273839">https://go.microsoft.com/fwlink/?LinkId=273839</A>.</span></span> <span data-ttu-id="4c47d-122">Details zur Authentifizierung finden Sie unter "OC Authentication Web Service Protocol" unter <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A> .</span><span class="sxs-lookup"><span data-stu-id="4c47d-122">For details about authentication, see "OC Authentication Web Service Protocol" at <A href="https://go.microsoft.com/fwlink/?linkid=279015">https://go.microsoft.com/fwlink/?LinkId=279015</A>.</span></span>



</div>

<div>

## <a name="the-lync-server-web-service-autodiscover-response"></a><span data-ttu-id="4c47d-123">Die Antwort auf die AutoErmittlung des lync Server-Webdiensts</span><span class="sxs-lookup"><span data-stu-id="4c47d-123">The Lync Server Web Service Autodiscover Response</span></span>

<span data-ttu-id="4c47d-124">Die Antwort, die beim Senden der Auto Ermittlungsanforderung zurückgegeben wird, ist für einen internen oder externen Client identisch.</span><span class="sxs-lookup"><span data-stu-id="4c47d-124">The response returned when the Autodiscover request is sent is the same for an internal or an external client.</span></span> <span data-ttu-id="4c47d-125">Einige Parameter, die Standort abhängig sind, können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="4c47d-125">Some parameters that are location–aware may change.</span></span> <span data-ttu-id="4c47d-126">Wenn eine Clientanforderung empfangen wird, der tatsächliche Pool aber nicht mit der Kontaktperson ist, wird der Benutzerpool für diesen Benutzer festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="4c47d-126">If a client request is received, but the actual pool is other than the one that has been contacted, the user’s home pool will be set for that user.</span></span> <span data-ttu-id="4c47d-127">Ein Kollege, dessen Benutzerkonto sich in einem anderen Pool befindet, sich aber vom gleichen Office aus anmeldet, würde eine etwas andere Antwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c47d-127">A colleague whose user account is on a different pool, but logging in from the same office, would get a slightly different response.</span></span> <span data-ttu-id="4c47d-128">Die Antwort gibt den richtigen Front-End-Server oder Front-End-Pool für diesen Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="4c47d-128">The response indicates the correct Front End Server or Front End pool for that user.</span></span>

<span data-ttu-id="4c47d-129">Ein Beispiel für ein Antwortdokument für die AutoErmittlung:</span><span class="sxs-lookup"><span data-stu-id="4c47d-129">An example of an Autodiscover Response document:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">
       <User>
          <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>
          <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>
          <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>
          <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>
          <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>
          <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>
          <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>
          <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>
          <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>
          <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>
          <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>
          <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>
          <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>
          <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>
          <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>
          <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>
       </User>
    </AutodiscoverResponse>

<div>

## <a name="autodiscover-response-document-details"></a><span data-ttu-id="4c47d-130">Details des Auto Ermittlungs Antwortdokuments</span><span class="sxs-lookup"><span data-stu-id="4c47d-130">Autodiscover Response Document Details</span></span>

<span data-ttu-id="4c47d-131">Das Antwortdokument für die AutoErmittlung kann in einem von zwei Formaten vorliegen.</span><span class="sxs-lookup"><span data-stu-id="4c47d-131">The Autodiscover Response document can be in one of two formats.</span></span> <span data-ttu-id="4c47d-132">Das Standardformat ist eine JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="4c47d-132">The default format is a JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="4c47d-133">Das andere Format ist das XML-Dokument (Extensible Markup Language).</span><span class="sxs-lookup"><span data-stu-id="4c47d-133">The other format is extensible markup language (XML) document.</span></span> <span data-ttu-id="4c47d-134">Der XML-Code wird für dieses Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-134">The XML is used for this example.</span></span> <span data-ttu-id="4c47d-135">Die Anforderung und Antwort sind vorhersehbar, da das Dokument über ein definiertes Schema verfügt, das das Format bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4c47d-135">The request and response are predictable because the document has a defined schema that determines the format.</span></span> <span data-ttu-id="4c47d-136">Die Zeile im Dokument, die das verwendete Schema beschreibt, ist die erste Zeile in der Anforderung oder Antwort:</span><span class="sxs-lookup"><span data-stu-id="4c47d-136">The line in the document that describes the schema used is the first line in the request or response:</span></span>

    <AutodiscoverResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" AccessLocation="External">

<span data-ttu-id="4c47d-137">Die Definition von **Zugriffsort = "extern"** gibt an, dass die Anforderung von einem externen Benutzer vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="4c47d-137">The definition of **AccessLocation=”External”** indicates that the request was made from an external user.</span></span>

    <SipServerInternalAccess fqdn="pool01.contoso.com" port="5061"/>

&nbsp;

    <SipServerExternalAccess fqdn="sip.contoso.com" port="5061"/>

<span data-ttu-id="4c47d-138">SipServerInternalAccess und SipServerExternalAccess werden zurzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-138">SipServerInternalAccess and SipServerExternalAccess are currently not used.</span></span> <span data-ttu-id="4c47d-139">Diese Einträge sind für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-139">These entries are reserved for future use.</span></span>

    <SipClientInternalAccess fqdn=" pool01.contoso.com" port="443"/>

&nbsp;

    <SipClientExternalAccess fqdn="sip.contoso.com " port="443"/>

<span data-ttu-id="4c47d-140">SipClientInternalAccess und SipClientExternalAccess beschreiben den vollqualifizierten Domänennamen und-Port, den ein interner oder externer Client für den Zugriff auf den festgelegten SIP-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-140">SipClientInternalAccess and SipClientExternalAccess describe the fully qualified domain name and port that an internal or external client will use to access the defined SIP Server.</span></span> <span data-ttu-id="4c47d-141">Der lync-Desktop Client und die lync Windows Store-App verwenden diese Einträge basierend auf Ihrem Standort (intern oder extern), um den Director oder Front-End-Server zu finden.</span><span class="sxs-lookup"><span data-stu-id="4c47d-141">The Lync desktop client and the Lync Windows Store app use these entries, based on their location (internal or external) to find the Director or Front End Server.</span></span>

    <Link token="Internal/Autodiscover" href="https://webinternal.contoso.net/Autodiscover/AutodiscoverService.svc/root"/>

&nbsp;

    <Link token ="External/Autodiscover" href="https://webexternal.contoso.com/Autodiscover/AutodiscoverService.svc/root"/>

<span data-ttu-id="4c47d-142">Die `Autodiscover` Verweise enthalten die Dienst Einstiegspunkte für den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="4c47d-142">The `Autodiscover` references contain the service entry points for the Autodiscover service.</span></span> <span data-ttu-id="4c47d-143">Das Token-Attribut enthält den Namen des Diensts, und die href-Eigenschaft ist eine URL, die für den Client definiert, in dem der Dienst gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c47d-143">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="4c47d-144">Clients in einem externen Netzwerk verwenden `External/Autodiscover` .</span><span class="sxs-lookup"><span data-stu-id="4c47d-144">Clients on an external network use the `External/Autodiscover`.</span></span> <span data-ttu-id="4c47d-145">Der AutoErmittlungsdienst wird als Teil des Bereitstellungsprozesses installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-145">The Autodiscover service is installed as part of the deployment process.</span></span> <span data-ttu-id="4c47d-146">`Internal/Autodiscover` wird derzeit nicht verwendet und ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-146">`Internal/Autodiscover` is not currently used, and is reserved for future use.</span></span>

    <Link token="Internal/AuthBroker" href="https://webinternal.contoso.net/Reach/sip.svc"/>

&nbsp;

    <Link token="External/AuthBroker" href="https://webexternal.contoso.com/Reach/sip.svc"/>

<span data-ttu-id="4c47d-147">Die `AuthBroker` Verweise enthalten die Dienst Einstiegspunkte für den internen und den externen Authentifizierungsbroker Dienst, in diesem Fall SIP. svc.</span><span class="sxs-lookup"><span data-stu-id="4c47d-147">The `AuthBroker` references contain the service entry points for the internal and the external authentication broker service, in this case, sip.svc.</span></span> <span data-ttu-id="4c47d-148">Das Token-Attribut enthält den Namen des Diensts, und die href-Eigenschaft ist eine URL, die für den Client definiert, in dem der Dienst gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c47d-148">The token attribute contains the name of the service, and the href is a URL that defines for the client where the service can be found.</span></span> <span data-ttu-id="4c47d-149">Clients im internen Netzwerk mit Verwendung `Internal/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="4c47d-149">Clients on the internal network with use `Internal/AuthBroker`.</span></span> <span data-ttu-id="4c47d-150">Clients in einem externen Netzwerk verwenden `External/AuthBroker` .</span><span class="sxs-lookup"><span data-stu-id="4c47d-150">Clients on an external network use the `External/AuthBroker`.</span></span> <span data-ttu-id="4c47d-151">Der AuthBroker-Dienst wird als Teil des Bereitstellungsprozesses ihrer internen lync Server 2013-Bereitstellungs Webdienste installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-151">The AuthBroker service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/WebScheduler" href="https://webinternal.contoso.net/Scheduler"/>

&nbsp;

    <Link token="External/WebScheduler" href="https://webexternal.contoso.com/Scheduler"/>

<span data-ttu-id="4c47d-152">Das `WebScheduler` Token verweist auf die URLs für den Clientzugriff auf die webbasierte Planung für lync Server-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="4c47d-152">The `WebScheduler` token references the URLs for client access to the web-based scheduling for Lync Server conferences.</span></span> <span data-ttu-id="4c47d-153">Derzeit wird nur die `External/WebScheduler` verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-153">Currently, only the `External/WebScheduler` is used.</span></span> <span data-ttu-id="4c47d-154">Der Webplaner wird im Rahmen des Bereitstellungsprozesses ihrer internen lync Server 2013-Bereitstellungs Webdienste installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-154">The WebScheduler is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Mcx" href="https://webexternal.contoso.net/Mcx/McxService.svc"/>

&nbsp;

    <Link token="External/Mcx" href="https://webexternal.contoso.com/Mcx/McxService.svc"/>

<span data-ttu-id="4c47d-155">`Internal/Mcx` und `External/Mcx` sind die Speicherorte der Mobilitätsdienste, die im kumulativen Update für lync Server 2010: November 2011 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="4c47d-155">`Internal/Mcx` and `External/Mcx` are the locations of the Mobility services, introduced in Cumulative Update for Lync Server 2010: November 2011.</span></span> <span data-ttu-id="4c47d-156">Diese Verweise werden weiterhin von lync 2010 Mobile auf allen unterstützten Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-156">These references will continue to be used by Lync 2010 Mobile on all supported devices.</span></span> <span data-ttu-id="4c47d-157">Der MCX-Dienst wird als Teil des Bereitstellungsprozesses ihrer internen lync Server 2013-Bereitstellungs Webdienste installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-157">The Mcx service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/Ucwa" href="https://webinternal.contoso.net/ucwa/v1/applications"/>

&nbsp;

    <Link token="External/Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

&nbsp;

    <Link token="Ucwa" href="https://webexternal.contoso.com/ucwa/v1/applications"/>

<span data-ttu-id="4c47d-158">**Internal/Ucwa**, **External/Ucwa** und **Ucwa** bieten Clients einen Mittel für den Zugriff auf die Unified Communications Web Application-Programmierschnittstelle (Ucwa-API oder einfach Ucwa).</span><span class="sxs-lookup"><span data-stu-id="4c47d-158">**Internal/Ucwa**, **External/Ucwa** and **Ucwa** provide a means for clients to access the Unified Communications Web Application Programming Interface (UCWA API, or simply UCWA).</span></span> <span data-ttu-id="4c47d-159">`Internal/Ucwa` und `External/Ucwa` virtuelle Verzeichnisse sind Zugriffspunkte, die für zukünftige Funktionserweiterungen reserviert sind und nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c47d-159">`Internal/Ucwa` and `External/Ucwa` virtual directories are access points reserved for future feature enhancement, and are not used.</span></span> <span data-ttu-id="4c47d-160">Das `Ucwa` virtuelle Verzeichnis wird für Microsoft lync Mobile (eingeführt mit lync Server 2013) auf allen unterstützten Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c47d-160">The `Ucwa` virtual directory is used for Microsoft Lync Mobile (introduced with Lync Server 2013) on all supported devices.</span></span> <span data-ttu-id="4c47d-161">Der UCWA-Dienst wird als Teil des Bereitstellungsprozesses ihrer internen lync Server 2013-Bereitstellungs Webdienste installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-161">The UCWA service is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Internal/XFrame" href="https://webinternal.contoso.net/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="External/XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

&nbsp;

    <Link token="XFrame" href="https://webexternal.contoso.com/Autodiscover/XFrame/XFrame.html"/>

<span data-ttu-id="4c47d-162">`Internal/XFrame`, **External/Xframe** und **Xframe** bieten Zugriff auf UCWA-basierte Serveranwendungen.</span><span class="sxs-lookup"><span data-stu-id="4c47d-162">`Internal/XFrame`, **External/XFrame** and **XFrame** provide access for UCWA-based server applications.</span></span> <span data-ttu-id="4c47d-163">Xframe wird als Teil des Bereitstellungsprozesses ihrer internen lync Server 2013-Bereitstellungs Webdienste installiert.</span><span class="sxs-lookup"><span data-stu-id="4c47d-163">XFrame is installed as part of the deployment process of your internal Lync Server 2013 deployment web services.</span></span>

    <Link token="Self" href="https://webexternal.contoso.net/Autodiscover/AutodiscoverService.svc/root/user"/>

<span data-ttu-id="4c47d-164">Das `Self` Token bezieht sich auf spezifische Informationen für den Client (Benutzer Antworttyp), der die Anforderung vornimmt.</span><span class="sxs-lookup"><span data-stu-id="4c47d-164">The `Self` token refers to information specific to the client (user response type) that is making the request.</span></span> <span data-ttu-id="4c47d-165">Der Client, der diese Anforderung gestellt hat, war extern, und dieser autodiscover-Verweis bezieht sich auf den Benutzer Teil des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="4c47d-165">The client that made this request was external, and this Autodiscover reference is to the user portion of the Autodiscover service.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4c47d-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c47d-166">See Also</span></span>


[<span data-ttu-id="4c47d-167">Systemanforderungen für Komponenten für den Zugriff durch externe Benutzer für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c47d-167">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)  
[<span data-ttu-id="4c47d-168">Planen der AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c47d-168">Planning for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-planning-for-autodiscover.md)  
  

<span data-ttu-id="4c47d-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c47d-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

