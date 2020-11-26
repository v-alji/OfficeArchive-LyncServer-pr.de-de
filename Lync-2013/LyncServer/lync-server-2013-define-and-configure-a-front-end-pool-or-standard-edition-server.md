---
title: Definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers
description: Definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define and configure a Front End pool or Standard Edition server
ms:assetid: 713fc263-23dd-414a-b001-82932e4fe966
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398538(v=OCS.15)
ms:contentKeyID: 48184457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd632564f0a5afd1f899ee8487f633c4685d12a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431071"
---
# <a name="define-and-configure-a-front-end-pool-or-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="7d37c-103">Definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d37c-103">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d37c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d37c-104">

<span> </span></span></span>

<span data-ttu-id="7d37c-105">_**Letztes Änderungsdatum des Themas:** 2013-03-08_</span><span class="sxs-lookup"><span data-stu-id="7d37c-105">_**Topic Last Modified:** 2013-03-08_</span></span>

<span data-ttu-id="7d37c-106">Für dieses Verfahren ist keine Mitgliedschaft in einem lokalen Administrator oder einer privilegierten Domänengruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d37c-106">This procedure does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="7d37c-107">Melden Sie sich als Standardbenutzer an einem Computer an.</span><span class="sxs-lookup"><span data-stu-id="7d37c-107">You should log on to a computer as a standard user.</span></span>

<span data-ttu-id="7d37c-108">Wenn Sie einen Enterprise-Server bereitstellen, muss immer eine Mindestanzahl an Front-End-Servern in einem Pool ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-108">If you are deploying an Enterprise server, a minimum number of Front End Servers in a pool must be running at all times.</span></span> <span data-ttu-id="7d37c-109">In der folgenden Tabelle werden diese Anforderungen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="7d37c-109">The following table summarizes these requirements.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d37c-110">Gesamtzahl der Front-End-Server im Pool</span><span class="sxs-lookup"><span data-stu-id="7d37c-110">Total number of Front End Servers in the pool</span></span></th>
<th><span data-ttu-id="7d37c-111">Anzahl der Server, die aktiv sein müssen, damit der Pool funktioniert</span><span class="sxs-lookup"><span data-stu-id="7d37c-111">Number of servers that must be running for pool to be functional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d37c-112">1-2</span><span class="sxs-lookup"><span data-stu-id="7d37c-112">1-2</span></span></p></td>
<td><p><span data-ttu-id="7d37c-113">1</span><span class="sxs-lookup"><span data-stu-id="7d37c-113">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d37c-114">3-4</span><span class="sxs-lookup"><span data-stu-id="7d37c-114">3-4</span></span></p></td>
<td><p><span data-ttu-id="7d37c-115">2</span><span class="sxs-lookup"><span data-stu-id="7d37c-115">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d37c-116">5-6</span><span class="sxs-lookup"><span data-stu-id="7d37c-116">5-6</span></span></p></td>
<td><p><span data-ttu-id="7d37c-117">3</span><span class="sxs-lookup"><span data-stu-id="7d37c-117">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d37c-118">7-8</span><span class="sxs-lookup"><span data-stu-id="7d37c-118">7-8</span></span></p></td>
<td><p><span data-ttu-id="7d37c-119">4</span><span class="sxs-lookup"><span data-stu-id="7d37c-119">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d37c-120">9-10</span><span class="sxs-lookup"><span data-stu-id="7d37c-120">9-10</span></span></p></td>
<td><p><span data-ttu-id="7d37c-121">5</span><span class="sxs-lookup"><span data-stu-id="7d37c-121">5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d37c-122">11-12</span><span class="sxs-lookup"><span data-stu-id="7d37c-122">11-12</span></span></p></td>
<td><p><span data-ttu-id="7d37c-123">6</span><span class="sxs-lookup"><span data-stu-id="7d37c-123">6</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]
> <span data-ttu-id="7d37c-124">Bei lync Server 2013 müssen Sie jedes Mal, wenn Sie einen Front-End-Server aus dem Pool hinzufügen oder entfernen, Dienste neu starten.</span><span class="sxs-lookup"><span data-stu-id="7d37c-124">For Lync Server 2013, any time you add or remove a Front End Server from the pool, you must restart services.</span></span> <span data-ttu-id="7d37c-125">Das Entfernen und Hinzufügen von Servern sollte als separate Vorgänge erfolgen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-125">Removing and adding servers should be done as separate operations.</span></span> <span data-ttu-id="7d37c-126">Wenn Sie beispielsweise zwei Front-End-Server hinzufügen und zwei Front-End-Server entfernen möchten, verwenden Sie den folgenden Prozess:</span><span class="sxs-lookup"><span data-stu-id="7d37c-126">For example, if you are going to add two Front End Servers and remove two Front End Servers, use the following process:</span></span> 
> <OL>
> <LI>
> <P><span data-ttu-id="7d37c-127">Entfernen Sie die beiden Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="7d37c-127">Remove the two Front End Servers.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d37c-128">Veröffentlichen Sie die Topologie, und aktivieren Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="7d37c-128">Publish and re-activate the topology.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d37c-129">Starten Sie die Dienste neu</span><span class="sxs-lookup"><span data-stu-id="7d37c-129">Restart the services</span></span></P>
> <LI>
> <P><span data-ttu-id="7d37c-130">Fügen Sie die beiden Front-End-Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="7d37c-130">Add the two Front End Servers.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d37c-131">Veröffentlichen Sie die Topologie, und aktivieren Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="7d37c-131">Publish and re-activate the topology.</span></span></P>
> <LI>
> <P><span data-ttu-id="7d37c-132">Starten Sie die Dienste neu.</span><span class="sxs-lookup"><span data-stu-id="7d37c-132">Restart the services.</span></span></P></LI></OL>



</div>

<span data-ttu-id="7d37c-133">Nachdem Sie Ihre Topologie definiert haben, gehen Sie wie folgt vor, um einen Front-End-Pool für Ihre Website zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7d37c-133">After you have defined your topology, use the following procedure to define a Front End pool for your site.</span></span> <span data-ttu-id="7d37c-134">Details zum Definieren der Topologie finden Sie unter [definieren und Konfigurieren einer Topologie im Topologie-Generator für lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="7d37c-134">For details about defining the topology, see [Define and configure a topology in Topology Builder for Lync Server 2013](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md).</span></span>

<div>

## <a name="to-define-a-front-end-pool"></a><span data-ttu-id="7d37c-135">So definieren Sie einen Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="7d37c-135">To define a Front End pool</span></span>

1.  <span data-ttu-id="7d37c-136">Klicken Sie im Assistenten zum Definieren eines neuen Front-End-Pools auf der Seite **Neues Front-End-Pool definieren** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-136">In the Define New Front End Pool Wizard, on the **Define the New Front End pool** page, click **Next**.</span></span>

2.  <span data-ttu-id="7d37c-137">Geben Sie auf der Seite **FQDN des Front-End-Pools definieren** einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für den zu erstellenden Pool ein, klicken Sie auf **Enterprise Edition-Front-End-Pool**, und klicken Sie dann auf **weiter**</span><span class="sxs-lookup"><span data-stu-id="7d37c-137">On the **Define the Front End pool FQDN** page, enter a fully qualified domain name (FQDN) for the pool you are creating, click **Enterprise Edition Front End pool**, and then click **Next**.</span></span>

3.  <span data-ttu-id="7d37c-138">Geben Sie auf der Seite **Computer auf diesem Pool definieren** einen Computer-FQDN für den ersten Front-End-Server im Pool ein, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-138">On the **Define the computers in this pool** page, enter a computer FQDN for the first Front End Server in the pool, and then click **Add**.</span></span> <span data-ttu-id="7d37c-139">Wiederholen Sie diesen Schritt für alle weiteren Computer (bis zu zwölf), die Sie dem Pool hinzufügen möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-139">Repeat this step for any additional computers (up to twelve) that you want to add to the pool, and then click **Next**.</span></span>

4.  <span data-ttu-id="7d37c-140">Aktivieren Sie auf der Seite **Features auswählen** die Kontrollkästchen für die Features, die in diesem Front-End-Pool angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-140">On the **Select features** page, select the check boxes for the features that you want on this Front End pool.</span></span> <span data-ttu-id="7d37c-141">Wenn Sie beispielsweise nur Chat-und Anwesenheitsfeatures bereitstellen, aktivieren Sie das Kontrollkästchen **Konferenz Konferenzen** , um die mehrteilige Chatfunktion zuzulassen, aber nicht die Kontrollkästchen **Einwahl (PSTN) Conferencing**, **Enterprise Voice** oder **Anrufsteuerung** zu aktivieren, da Sie die Features für sprach-, Video-und kollaborative Konferenzen darstellen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-141">For example, if you are deploying only instant messaging (IM) and presence features, you would select the **Conferencing** check box to allow multiparty IM but would not select the **Dial-in (PSTN) conferencing**, **Enterprise Voice**, or **Call Admission Control** check boxes, because they represent voice, video, and collaborative conferencing features.</span></span>
    
      - <span data-ttu-id="7d37c-142">**Konferenzen**   Diese Auswahl ermöglicht einen umfangreichen Satz von Features, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="7d37c-142">**Conferencing**   This selection enables a rich set of features including:</span></span>
        
          - <span data-ttu-id="7d37c-143">Chatten mit mehr als zwei Teilnehmer in einer Chatsitzung.</span><span class="sxs-lookup"><span data-stu-id="7d37c-143">IM with more than two parties in an IM session.</span></span>
        
          - <span data-ttu-id="7d37c-144">Konferenz, die Zusammenarbeit in Dokumenten, Anwendungsfreigabe und Desktopfreigabe umfasst.</span><span class="sxs-lookup"><span data-stu-id="7d37c-144">Conferencing, which includes document collaboration, application sharing, and desktop sharing.</span></span>
        
          - <span data-ttu-id="7d37c-145">A/v-Konferenzen, mit denen Benutzer in Echtzeit Audio/Video-Konferenzen (a/v) führen können, ohne externe Dienste wie den Live Meeting-Dienst oder eine Audio-Bridge eines Drittanbieters zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-145">A/V conferencing, which enables users to have real-time audio/video (A/V) conferences without the need for external services such as the Live Meeting service or a third-party audio bridge.</span></span>
    
      - <span data-ttu-id="7d37c-146">**Einwahlkonferenzen (PSTN)**   Ermöglicht Benutzern die Teilnahme am Audioteil einer lync Server 2013-Konferenz mithilfe eines PSTN-Telefons (Public Switched Telephone Network), ohne dass ein Audiokonferenz-Anbieter erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7d37c-146">**Dial-in (PSTN) conferencing**   Allows users to join the audio portion of a Lync Server 2013 conference by using a public switched telephone network (PSTN) phone without requiring an audio conferencing provider.</span></span>
    
      - <span data-ttu-id="7d37c-147">**Enterprise-VoIP**   Enterprise-VoIP ist die VoIP-Lösung (Voice over IP) in lync Server 2013, mit der Benutzer Telefonanrufe tätigen und empfangen können.</span><span class="sxs-lookup"><span data-stu-id="7d37c-147">**Enterprise Voice**   Enterprise Voice is the Voice over IP (VoIP) solution in Lync Server 2013 that allows users to make and receive phone calls.</span></span> <span data-ttu-id="7d37c-148">Sie würden dieses Feature bereitstellen, wenn Sie beabsichtigen, lync Server 2013 für Sprachanrufe, Voicemail und andere Funktionen zu verwenden, die ein Hardwaregerät oder einen Software Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-148">You would deploy this feature if you plan to use Lync Server 2013 for voice calls, voice mail, and other functions that use a hardware device or a software client.</span></span>
    
      - <span data-ttu-id="7d37c-149">**Anrufsteuerung (CAC)**   CAC bestimmt anhand der verfügbaren Netzwerkbandbreite, ob Echt Zeit Kommunikationssitzungen wie Sprach-oder Videoanrufe eingerichtet werden können.</span><span class="sxs-lookup"><span data-stu-id="7d37c-149">**Call admission control (CAC)**   CAC determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="7d37c-150">Wenn Sie nur Chat und Anwesenheit bereitgestellt haben, ist CAC nicht erforderlich, da keine dieser beiden Features CAC verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d37c-150">If you have deployed only IM and presence, CAC is not needed because neither of these two features uses CAC.</span></span>
    
      - <span data-ttu-id="7d37c-151">**Archivierung**   Die Archivierung bietet eine Möglichkeit zum Archivieren von Chat Inhalten, Konferenz (Besprechungs-) Inhalten oder beidem, die über lync Server 2013 gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-151">**Archiving**   Archiving provides a way for you to archive IM content, conferencing (meeting) content, or both that is sent through Lync Server 2013.</span></span>
    
      - <span data-ttu-id="7d37c-152">**Überwachung**   Mit Monitoring Server können Sie numerische Daten erfassen, die die Medienqualität in Ihrem Netzwerk und Endpunkten beschreiben, Nutzungsinformationen zu VoIP-Anrufen, Chatnachrichten, A/V-Unterhaltungen, Besprechungen, Anwendungsfreigabe und Dateiübertragungen sowie Anruf Fehler und Informationen zur Problembehandlung bei fehlgeschlagenen anrufen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-152">**Monitoring**   Monitoring Server enables you to collect numerical data that describes the media quality on your network and endpoints, usage information related to VoIP calls, IM messages, A/V conversations, meetings, application sharing, and file transfers, and call error and troubleshooting information for failed calls.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="7d37c-153">Wenn Sie CAC in Ihrer Bereitstellung aktivieren möchten, müssen Sie CAC in genau einem Pool pro zentralen Standort aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d37c-153">If you would like to enable CAC in your deployment, it is required that you enable CAC in exactly one pool per central site.</span></span> <span data-ttu-id="7d37c-154">CAC wird empfohlen, wenn Sie Sprachfeatures oder A/V-Konferenzen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-154">CAC is recommended if you are deploying voice features or A/V conferencing.</span></span>

    
    </div>
    
    <span data-ttu-id="7d37c-155">In der folgenden Tabelle sind die verfügbaren Funktionen (oben) und die den Benutzern angebotenen Funktionen (links) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d37c-155">The following table shows the available features (top) and the functions offered to users (left).</span></span> <span data-ttu-id="7d37c-156">Die Auswahl in der Tabelle ist das, was Sie auswählen sollten, um diese Features für Ihre Organisation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d37c-156">The selections in the table are what you should select to enable those features for your organization.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    <col style="width: 20%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th></th>
    <th><span data-ttu-id="7d37c-157">Konferenzen</span><span class="sxs-lookup"><span data-stu-id="7d37c-157">Conferencing</span></span></th>
    <th><span data-ttu-id="7d37c-158">Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="7d37c-158">Dial-In Conferencing</span></span></th>
    <th><span data-ttu-id="7d37c-159">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="7d37c-159">Enterprise Voice</span></span></th>
    <th><span data-ttu-id="7d37c-160">Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="7d37c-160">Call Admission Control</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="7d37c-161">Chat und Anwesenheit</span><span class="sxs-lookup"><span data-stu-id="7d37c-161">Instant messaging and presence</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-162">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-162">X</span></span></p></td>
    <td></td>
    <td></td>
    <td></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7d37c-163">Konferenzen</span><span class="sxs-lookup"><span data-stu-id="7d37c-163">Conferencing</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-164">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-164">X</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-165">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-165">X</span></span></p></td>
    <td></td>
    <td></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="7d37c-166">A/V-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="7d37c-166">A/V conferencing</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-167">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-167">X</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-168">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-168">X</span></span></p></td>
    <td></td>
    <td><p><span data-ttu-id="7d37c-169">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-169">X</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="7d37c-170">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="7d37c-170">Enterprise Voice</span></span></p></td>
    <td></td>
    <td></td>
    <td><p><span data-ttu-id="7d37c-171">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-171">X</span></span></p></td>
    <td><p><span data-ttu-id="7d37c-172">X</span><span class="sxs-lookup"><span data-stu-id="7d37c-172">X</span></span></p></td>
    </tr>
    </tbody>
    </table>


5.  <span data-ttu-id="7d37c-173">Auf der Seite **"Serverrollen auswählen** " können Sie den Vermittlungsserver auf dem Front-End-Server collocate oder als eigenständigen Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-173">On the **Select collocated server roles** page, you can to collocate the Mediation Server on the Front End Server or to deploy it as a stand-alone server.</span></span>
    
    <span data-ttu-id="7d37c-174">Sie können den Vermittlungs Server im Front-End-Pool collocate.</span><span class="sxs-lookup"><span data-stu-id="7d37c-174">You can collocate the Mediation Server on the Front End pool.</span></span>
    
      - <span data-ttu-id="7d37c-175">Wenn Sie beabsichtigen, den Vermittlungs Server im Front-End-Pool der Enterprise Edition collocate, stellen Sie sicher, dass das Kontrollkästchen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d37c-175">If you intend to collocate the Mediation Server on the Enterprise Edition Front End pool, ensure the check box is selected.</span></span> <span data-ttu-id="7d37c-176">Die Serverrolle wird auf den Servern im Pool bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7d37c-176">The server role will be deployed on the pool servers.</span></span>
    
      - <span data-ttu-id="7d37c-177">Wenn Sie den Vermittlungsserver als eigenständigen Server bereitstellen möchten, deaktivieren Sie das entsprechende Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-177">If you intend to deploy the Mediation Server as a stand-alone server, clear the appropriate check box.</span></span> <span data-ttu-id="7d37c-178">Nachdem Sie den Front-End-Server vollständig bereitgestellt haben, werden Sie den Vermittlungsserver in einem separaten Bereitstellungsschritt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-178">You will deploy Mediation Server in a separate deployment step after you completely deploy the Front End Server.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="7d37c-179">Wir empfehlen, dass Sie den Vermittlungs Server nach Möglichkeit collocate.</span><span class="sxs-lookup"><span data-stu-id="7d37c-179">We recommend that you collocate the Mediation Server if possible.</span></span> <span data-ttu-id="7d37c-180">Ausführliche Informationen zur Unterstützung für sich selbst oder eigenständige Vermittlungsserver finden Sie unter <A href="lync-server-2013-components-and-topologies-for-mediation-server.md">Komponenten und Topologien für Mediation Server in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7d37c-180">For details about support for collocated or stand-alone Mediation Servers, see <A href="lync-server-2013-components-and-topologies-for-mediation-server.md">Components and topologies for Mediation Server in Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>

6.  <span data-ttu-id="7d37c-181">Mit der Seite **Serverrollen mit diesem Front-End-Pool verknüpfen** können Sie Serverrollen mit dem Front-End-Pool definieren und zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-181">The **Associate server roles with this Front End pool** page lets you define and associate server roles with the Front End pool.</span></span> <span data-ttu-id="7d37c-182">Die folgende Rolle ist verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7d37c-182">The following role is available:</span></span>
    
    <span data-ttu-id="7d37c-183">**Aktivieren eines Edge-Pools**   Definiert und ordnet einen einzelnen Edgeserver oder einen Pool von Edgeserver zu.</span><span class="sxs-lookup"><span data-stu-id="7d37c-183">**Enable an Edge pool**   Defines and associates a single Edge Server or a pool of Edge Servers.</span></span> <span data-ttu-id="7d37c-184">Ein Edgeserver vereinfacht die Kommunikation und Zusammenarbeit zwischen Benutzern innerhalb der Organisation und Personen außerhalb der Organisation, einschließlich Verbundbenutzern.</span><span class="sxs-lookup"><span data-stu-id="7d37c-184">An Edge Server facilitates communication and collaboration between users inside the organization and people outside the organization, including federated users.</span></span>
    
    <span data-ttu-id="7d37c-185">Es gibt zwei mögliche Szenarien, mit denen Sie die Serverrollen bereitstellen und zuordnen können:</span><span class="sxs-lookup"><span data-stu-id="7d37c-185">There are two possible scenarios that you can use to deploy and associate the server roles:</span></span>
    
    <span data-ttu-id="7d37c-186">In Szenario 1 definieren Sie eine neue Topologie für eine Neuinstallation.</span><span class="sxs-lookup"><span data-stu-id="7d37c-186">For scenario one, you are defining a new topology for a new installation.</span></span> <span data-ttu-id="7d37c-187">Sie können sich der Installation auf eine von zwei Arten nähern:</span><span class="sxs-lookup"><span data-stu-id="7d37c-187">You can approach the installation in one of two ways:</span></span>
    
      - <span data-ttu-id="7d37c-188">Deaktivieren Sie das Kontrollkästchen, und fahren Sie mit dem Definieren der Topologie fort.</span><span class="sxs-lookup"><span data-stu-id="7d37c-188">Leave the check box clear and proceed with defining the topology.</span></span> <span data-ttu-id="7d37c-189">Nachdem Sie den Front-End-Server und den Back-End-Server veröffentlicht, konfiguriert und getestet haben, können Sie den Topologie-Generator erneut ausführen, um die Rollenserver zur Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-189">After you have published, configured, and tested the Front End and Back End Server roles, you can run Topology Builder again to add the role servers to the topology.</span></span> <span data-ttu-id="7d37c-190">Mit dieser Strategie können Sie den Front-End-Pool und den Server, auf dem SQL Server ausgeführt wird, ohne zusätzliche Komplikationen durch zusätzliche Rollen testen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-190">This strategy will enable you to test the Front End pool and the server running SQL Server without additional complications from additional roles.</span></span> <span data-ttu-id="7d37c-191">Wenn Sie die anfänglichen Tests abgeschlossen haben, können Sie den Topologie-Generator zur Auswahl der erforderlichen Rollen erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-191">After you have completed your initial testing, you can run Topology Builder again to select the roles you need to deploy.</span></span>
    
      - <span data-ttu-id="7d37c-192">Wählen Sie die Rollen aus, die installiert werden müssen, und richten Sie anschließend die Hardware für die ausgewählten Rollen ein.</span><span class="sxs-lookup"><span data-stu-id="7d37c-192">Select roles that you need to install, and then set up the hardware to accommodate the selected roles.</span></span>
    
    <span data-ttu-id="7d37c-193">Für Szenario zwei verfügen Sie über eine vorhandene Bereitstellung, und ihre Infrastruktur ist für neue Rollen bereit, oder Sie müssen vorhandene Rollen einem neuen Front-End-Server zuordnen:</span><span class="sxs-lookup"><span data-stu-id="7d37c-193">For scenario two, you have an existing deployment and your infrastructure is ready for new roles or you need to associate existing roles with a new Front End Server:</span></span>
    
      - <span data-ttu-id="7d37c-194">In diesem Fall wählen Sie die Rollen aus, die Sie dem neuen Front-End-Server bereitstellen oder zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="7d37c-194">In this case, you will select the roles that you intend to deploy or associate with the new Front End Server.</span></span> <span data-ttu-id="7d37c-195">In beiden Fällen fahren Sie mit der Definition der Rollen fort, richten gegebenenfalls erforderliche Hardware ein und führen die Installation aus.</span><span class="sxs-lookup"><span data-stu-id="7d37c-195">In either case, you will proceed with the definition of the roles, set up any needed hardware, and proceed with the installation.</span></span>

7.  <span data-ttu-id="7d37c-196">Führen Sie auf der Seite **SQL Store definieren** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="7d37c-196">On the **Define the SQL store** page, do one of the following:</span></span>
    
      - <span data-ttu-id="7d37c-197">Zum Verwenden eines SQL Server-Speichers, der bereits in Ihrer Topologie definiert wurde, wählen Sie eine Instanz unter **SQL-Speicher** aus.</span><span class="sxs-lookup"><span data-stu-id="7d37c-197">To use an existing SQL Server store that has already been defined in your topology, select an instance from **SQL store**.</span></span>
    
      - <span data-ttu-id="7d37c-198">Wenn Sie eine neue SQL Server-Instanz zum Speichern von Poolinformationen definieren möchten, klicken Sie auf **neu** , und geben Sie dann den **SQL Server-FQDN** im Dialogfeld **neuen SQL-Speicher definieren** ein.</span><span class="sxs-lookup"><span data-stu-id="7d37c-198">To define a new SQL Server instance to store pool information, click **New** and then specify the **SQL Server FQDN** in the **Define New SQL Store** dialog box.</span></span>
    
      - <span data-ttu-id="7d37c-199">Zum Angeben des Namens einer SQL Server-Instanz wählen Sie **Benannte Instanz** und geben Sie anschließend den Namen der Instanz an.</span><span class="sxs-lookup"><span data-stu-id="7d37c-199">To specify the name of a SQL Server instance, select **Named Instance**, and then specify the name of the instance.</span></span>
    
      - <span data-ttu-id="7d37c-200">Klicken Sie auf **Standardinstanz**, um die Standardinstanz zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-200">To use the default instance, click **Default instance**.</span></span>
    
      - <span data-ttu-id="7d37c-201">Wenn Sie die SQL-Spiegelung verwenden möchten, wählen Sie **SQL-Spiegelung aktivieren** aus, und wählen Sie eine vorhandene Instanz aus, oder erstellen Sie eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d37c-201">To use SQL Mirroring, select **Enable SQL mirroring** and select an existing instance or create a new instance.</span></span>

8.  <span data-ttu-id="7d37c-202">Führen Sie auf der Seite " **Dateifreigabe definieren** " eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="7d37c-202">On the **Define the file share** page, do one of the following:</span></span>
    
      - <span data-ttu-id="7d37c-203">Zum Verwenden einer Dateifreigabe, die bereits in Ihrer Topologie definiert wurde, wählen Sie **Zuvor definierte Dateifreigabe verwenden**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-203">To use a file share that has already been defined in your topology, select **Use a previously defined file share**.</span></span>
    
      - <span data-ttu-id="7d37c-204">Zum Definieren einer neuen Dateifreigabe wählen Sie **Neue Dateifreigabe definieren**, geben Sie im Feld **Dateiserver-FQDN** den vollqualifizierten Domänennamen des vorhandenen Dateiservers ein, auf dem sich die Dateifreigabe befinden soll, und geben Sie anschließend einen Namen für die Dateifreigabe in das Feld **Dateifreigabe** ein.</span><span class="sxs-lookup"><span data-stu-id="7d37c-204">To define a new file share, select **Define a new file share**, in the **File Server FQDN** box, enter the FQDN of the existing file server where the file share is to reside, and then enter a name for the file share in the **File Share** box.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="7d37c-205">Die Dateifreigabe für lync Server 2013 kann nicht auf dem Front-End-Server gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-205">The file share for Lync Server 2013 cannot be located on the Front End Server.</span></span> <span data-ttu-id="7d37c-206">Beachten Sie, dass sich die Dateifreigabe in diesem Beispiel auf dem auf SQL Server basierenden Back-End-Server befand.</span><span class="sxs-lookup"><span data-stu-id="7d37c-206">Note that in this example, the file share has been located on the SQL Server-based Back End Server.</span></span> <span data-ttu-id="7d37c-207">Dies ist möglicherweise kein optimaler Ort für die Anforderungen Ihrer Organisation, und ein Dateiserver ist möglicherweise eine bessere Wahl.</span><span class="sxs-lookup"><span data-stu-id="7d37c-207">This might not be an optimal location for your organization’s requirements, and a file server might be a better choice.</span></span> <span data-ttu-id="7d37c-208">Sie können die Dateifreigabe definieren, ohne sie erstellt zu haben.</span><span class="sxs-lookup"><span data-stu-id="7d37c-208">You can define the file share without the file share having been created.</span></span> <span data-ttu-id="7d37c-209">Sie müssen die Dateifreigabe am definierten Speicherort erstellen, bevor Sie die Topologie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-209">You will need to create the file share in the location you define before you publish the topology.</span></span>

    
    </div>

9.  <span data-ttu-id="7d37c-210">Führen Sie auf der Seite **Geben Sie die Webdienste-URL** an eine oder beide der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="7d37c-210">On the **Specify the Web Services URL** page, do one or both of the following:</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="7d37c-211">Die Basis-URL ist die Webdienstidentität der URL ohne https://.</span><span class="sxs-lookup"><span data-stu-id="7d37c-211">The base URL is the Web Services identity for the URL, minus the https://.</span></span> <span data-ttu-id="7d37c-212">Wenn beispielsweise die vollständige URL für die Webdienste des Pools lautet https://pool01.contoso.net , lautet die Basis-URL pool01.contoso.net.</span><span class="sxs-lookup"><span data-stu-id="7d37c-212">For example, if the full URL for the Web Services of the pool is https://pool01.contoso.net, the base URL is pool01.contoso.net.</span></span>

    
    </div>
    
    <div>
    

    > [!WARNING]
    > <span data-ttu-id="7d37c-213">Wenn Sie über mehr als einen Front-End-Pool oder Front-End-Server verfügen, muss der FQDN für externe Webdienste eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7d37c-213">If you have more than one Front End pool or Front End Server, the external Web services FQDN must be unique.</span></span> <span data-ttu-id="7d37c-214">Wenn Sie beispielsweise den FQDN eines externen Webdiensts eines Front-End-Servers als <STRONG>pool01.contoso.com</STRONG>definieren, können Sie <STRONG>pool01.contoso.com</STRONG> nicht für einen anderen Front-End-Pool oder Front-End-Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-214">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span>

    
    </div>
    
    1.  <span data-ttu-id="7d37c-215">Wenn Sie den DNS-Lastenausgleich konfigurieren, aktivieren Sie das Kontrollkästchen **Interner FQDN des Webdienste-Pools außer Kraft setzen** , geben Sie die interne Basis-URL ein (die sich vom FQDN des Pools unterscheiden muss und beispielsweise Internal- \<your base URL\> ) in der **internen Basis-URL** sein kann.</span><span class="sxs-lookup"><span data-stu-id="7d37c-215">If you are configuring DNS load balancing, select the **Override internal Web Services pool FQDN** check box, enter the internal base URL (which must be different from the pool FQDN and could be, for example, internal-\<your base URL\>) in **Internal Base URL**.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="7d37c-216">Wenn Sie sich entscheiden, die internen Webdienste mit einem selbst definierten FQDN zu überschreiben, muss jeder FQDN für jeden anderen Front-End-Pool, Director oder Director-Pool eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7d37c-216">If you decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span> <span data-ttu-id="7d37c-217"><STRONG>Verwenden Sie nur Standardzeichen</STRONG> (A – Z, a – z, 0 – 9 und Bindestriche), wenn Sie URLs oder vollqualifizierte Domänennamen definieren.</span><span class="sxs-lookup"><span data-stu-id="7d37c-217"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when defining URLs or fully qualified domain names.</span></span> <span data-ttu-id="7d37c-218">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="7d37c-218">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="7d37c-219">Nicht-Standardzeichen in einem URL oder vollqualifizierten Domänennamen (FQDN) werden von externen DNS und öffentlichen Zertifizierungsstellen (wenn die URL oder der FQDN dem Antragstellernamen oder dem alternativen Antragstellernamen im Zertifikat zugewiesen werden muss) häufig nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d37c-219">Nonstandard characters in a URL or FQDN are often not supported by external DNS and public CAs (that is, when the URL or FQDN must be assigned to the subject name or subject alternative name in the certificate).</span></span>

        
        </div>
    
    2.  <span data-ttu-id="7d37c-220">Optional können Sie die externe Basis-URL in der **externen Basis-URL** eingeben.</span><span class="sxs-lookup"><span data-stu-id="7d37c-220">Optionally enter the external base URL in **External Base URL**.</span></span> <span data-ttu-id="7d37c-221">Sie würden die externe Basis-URL eingeben, um Sie von ihrer internen Domänen Namensgebung zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-221">You would enter the external base URL to differentiate it from your internal domain naming.</span></span> <span data-ttu-id="7d37c-222">Beispielsweise ist Ihre interne Domäne contoso.net, aber ihr externer Domänenname lautet contoso.com.</span><span class="sxs-lookup"><span data-stu-id="7d37c-222">For example, your internal domain is contoso.net, but your external domain name is contoso.com.</span></span> <span data-ttu-id="7d37c-223">Sie würden die URL mit dem contoso.com-Domänennamen definieren.</span><span class="sxs-lookup"><span data-stu-id="7d37c-223">You would define the URL using the contoso.com domain name.</span></span> <span data-ttu-id="7d37c-224">Dies ist auch im Fall eines Reverseproxys wichtig.</span><span class="sxs-lookup"><span data-stu-id="7d37c-224">This is also important in the case of a reverse proxy.</span></span> <span data-ttu-id="7d37c-225">Der Domänenname der externen Basis-URL würde dem Domänennamen des vollqualifizierten Domänennamens des Reverseproxys entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-225">The external base URL domain name would be the same as the domain name of the FQDN of the reverse proxy.</span></span> <span data-ttu-id="7d37c-226">Für Sofortnachrichten und Anwesenheitsinformationen ist der HTTP-Zugriff auf den Front-End-Pool erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d37c-226">Instant messaging and presence does require HTTP access to the Front End pool.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="7d37c-227">Wenn Sie den DNS-Lastenausgleich verwenden möchten, müssen Sie die entsprechenden DNS-Einträge erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-227">To use DNS load balancing, you must create the appropriate DNS records.</span></span> <span data-ttu-id="7d37c-228">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configure-dns-for-load-balancing.md">Konfigurieren von DNS für den Lastenausgleich in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7d37c-228">For details, see <A href="lync-server-2013-configure-dns-for-load-balancing.md">Configure DNS for load balancing in Lync Server 2013</A>.</span></span>

    
    </div>

10. <span data-ttu-id="7d37c-229">Wenn Sie auf der Seite **"Features auswählen** " **Konferenzen** ausgewählt haben, wählen Sie auf der Seite **Office Web Apps Server auswählen** die Option **Pool mit einem Office Web Apps-Server verknüpfen** aus, und klicken Sie dann auf **neu** (oder wählen Sie in der Dropdownliste einen vorhandenen Office Web Apps-Server aus) aus.</span><span class="sxs-lookup"><span data-stu-id="7d37c-229">If you selected **Conferencing** on the **Select Features** page, on the **Select an Office Web Apps Server** page select **Associate pool with an Office Web Apps Server** and then click **New** (or select an existing Office Web Apps Server from the drop-down list).</span></span>

11. <span data-ttu-id="7d37c-230">Geben Sie im Dialogfeld **Neuen Office Web Apps-Server definieren** den vollqualifizierten Domänennamen (FQDN) Ihres Office Web Apps-Servercomputers im Feld **FQDN von Office Web Apps-Server** ein. Anschließend sollte im Feld **Office Web Apps-Server-Such-URL** automatisch die Such-URL Ihres Office Web Apps-Servers stehen.</span><span class="sxs-lookup"><span data-stu-id="7d37c-230">In the **Define New Office Web Apps Server** dialog box, type the fully qualified domain name (FQDN) of your Office Web Apps Server computer in the **Office Web Apps Server FQDN** box; when you do this, your Office Web Apps Server discovery URL should automatically be entered into the **Office Web Apps Server discovery URL** box.</span></span>
    
    <span data-ttu-id="7d37c-231">Wenn der Office Web Apps-Server lokal und in derselben Netzwerkzone wie lync Server 2013 installiert ist, sollte die Option **Office Web Apps Server in einem externen Netzwerk bereitgestellt werden (also Umkreis/Internet)** , nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="7d37c-231">If the Office Web Apps Server is installed on-premises and in the same network zone as Lync Server 2013 then the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)** should not be selected.</span></span>
    
    <span data-ttu-id="7d37c-232">Wenn der Office Web Apps-Server außerhalb Ihrer internen Firewall bereitgestellt ist, aktivieren Sie die Option **Office Web Apps-Server ist in einem externen Netzwerk (d. h. Umkreis/Internet) bereitgestellt**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-232">If the Office Web Apps Server is deployed outside your internal firewall, then select the option **Office Web Apps Server is deployed in an external network (that is, perimeter/Internet)**.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="7d37c-233">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Konfigurieren der Integration in Office Web Apps Server und lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7d37c-233">For details, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>

    
    </div>

12. <span data-ttu-id="7d37c-234">Wählen Sie auf der Seite **Archivierungs-SQL-Speicher definieren** eine vorhandene Instanz oder SQL Server aus, oder definieren Sie eine neue Instanz zum Speichern der Daten, die mit den Archivierungsdaten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7d37c-234">On the **Define the Archiving SQL store** page, select an existing instance or SQL Server, or define a new instance to store the data associated with archiving data.</span></span>

13. <span data-ttu-id="7d37c-235">Wählen Sie auf der Seite **Definieren der Überwachung des SQL Stores** eine vorhandene Instanz oder SQL Server aus, oder definieren Sie eine neue Instanz zum Speichern der Daten, die mit Überwachungsdaten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7d37c-235">On the **Define the Monitoring SQL store** page, select an existing instance or SQL Server, or define a new instance to store the data associated with monitoring data.</span></span>

14. <span data-ttu-id="7d37c-236">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-236">Click **Next**.</span></span> <span data-ttu-id="7d37c-237">Wenn Sie auf der Seite **Serverrollen mit diesem Front-End-Pool zuordnen** andere Rollen Server definiert haben, werden die Seiten des Assistenten für die Rollenkonfiguration separat geöffnet, damit Sie die Serverrollen konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="7d37c-237">If you defined other role servers on the **Associate server roles with this Front End pool** page, separate role configuration wizard pages will open to let you configure the server roles.</span></span> <span data-ttu-id="7d37c-238">Ausführliche Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7d37c-238">For details, see the following:</span></span>
    
    [<span data-ttu-id="7d37c-239">Bereitstellen des Zugriffs durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d37c-239">Deploying external user access in Lync Server 2013</span></span>](lync-server-2013-deploying-external-user-access.md)

15. <span data-ttu-id="7d37c-240">Wenn Sie keine zusätzlichen Serverrollen zum Konfigurieren und Bereitstellen ausgewählt haben oder wenn Sie die Konfiguration der zusätzlichen Rollen Server abgeschlossen haben, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="7d37c-240">If you did not select additional server roles to configure and deploy, or when you have finished the configuration of the additional role servers, click **Finish**.</span></span>

<span data-ttu-id="7d37c-241"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d37c-241"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

