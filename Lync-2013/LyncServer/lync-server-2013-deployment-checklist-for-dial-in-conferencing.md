---
title: 'Lync Server 2013: Prüfliste zur Bereitstellung für Einwahlkonferenzen'
description: Checkliste für die lync Server 2013-Bereitstellung für Einwahlkonferenzen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for dial-in conferencing
ms:assetid: 9c8d3ebe-0d70-4a61-9bd0-522286cddd9a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412726(v=OCS.15)
ms:contentKeyID: 48184987
ms.date: 10/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 743b5120bf011ab8467679bea9869a46231b0835
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429741"
---
# <a name="deployment-checklist-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="0ce7d-103">Prüfliste zur Bereitstellung für Einwahlkonferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0ce7d-103">Deployment checklist for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0ce7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0ce7d-104">

<span> </span></span></span>

<span data-ttu-id="0ce7d-105">_**Letztes Änderungsdatum des Themas:** 2014-10-03_</span><span class="sxs-lookup"><span data-stu-id="0ce7d-105">_**Topic Last Modified:** 2014-10-03_</span></span>

<span data-ttu-id="0ce7d-106">Die für Einwahlkonferenzen erforderlichen Komponenten werden bereitgestellt, wenn Sie die Konferenz Arbeitsauslastung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-106">The components required for dial-in conferencing are deployed when you deploy the conferencing workload.</span></span> <span data-ttu-id="0ce7d-107">Bevor Sie Einwahlkonferenzen konfigurieren können, müssen Sie entweder Enterprise-VoIP oder einen Vermittlungs Server und ein PSTN-Gateway (Public Switched Telephone Network) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-107">Before you can configure dial-in conferencing, you need to deploy either Enterprise Voice or a Mediation Server and a public switched telephone network (PSTN) gateway.</span></span>

<span data-ttu-id="0ce7d-108">Alle Schritte in der folgenden Tabelle müssen ausgeführt werden, bevor Benutzer sich vom PSTN aus anrufen können, um an einer Audio/Video-Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-108">All the steps in the following table must be performed before users can dial in from the PSTN to join an audio/video conference.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0ce7d-109">Wenn Sie von Office Communications Server 2007 R2 migrieren, müssen Sie die neuesten Updates auf Ihre Office Communications Server 2007 R2-Umgebung anwenden, bevor Sie Einwahlkonferenzen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-109">If you are migrating from Office Communications Server 2007 R2, you must apply the latest updates to your Office Communications Server 2007 R2 environment before deploying dial-in conferencing.</span></span>



</div>

### <a name="dial-in-conferencing-deployment-process"></a><span data-ttu-id="0ce7d-110">Bereitstellungsprozess für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="0ce7d-110">Dial-in Conferencing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ce7d-111">Phase</span><span class="sxs-lookup"><span data-stu-id="0ce7d-111">Phase</span></span></th>
<th><span data-ttu-id="0ce7d-112">Schritte</span><span class="sxs-lookup"><span data-stu-id="0ce7d-112">Steps</span></span></th>
<th><span data-ttu-id="0ce7d-113">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="0ce7d-113">Permissions</span></span></th>
<th><span data-ttu-id="0ce7d-114">Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="0ce7d-114">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-115"><strong>Erstellen einer Topologie mit der Konferenz Arbeitsauslastung, einschließlich eines Vermittlungsservers und eines PSTN-Gateways, und Bereitstellen des Front-End-Pools oder des Standard Edition-Servers</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-115"><strong>Create a topology that includes the Conferencing workload, including a Mediation Server and PSTN gateway, and deploy the Front End pool or Standard Edition server</strong></span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="0ce7d-116">Führen Sie den Topologie-Generator aus, um Ihre Topologie zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-116">Run Topology Builder to configure your topology.</span></span> <span data-ttu-id="0ce7d-117">Wählen Sie beim Konfigurieren der Topologie die Einwahlkonferenzoption aus.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-117">While configuring the topology, select the dial-in conferencing option.</span></span></p></li>
<li><p><span data-ttu-id="0ce7d-118">Veröffentlichen der Topologie und Bereitstellen des Front-End-Pools oder des Standard Edition-Servers</span><span class="sxs-lookup"><span data-stu-id="0ce7d-118">Publish the topology and deploy the Front End pool or Standard Edition server.</span></span></p></li>
<li><p><span data-ttu-id="0ce7d-119">Erstellen Sie bei Bedarf einen eigenständigen Vermittlungs Server, und ordnen Sie ihn einem PSTN-Gateway zu.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-119">If necessary, create a stand-alone Mediation Server and associate it with a PSTN gateway.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="0ce7d-120">Dieser Schritt ist nur erforderlich, wenn Sie Enterprise-VoIP nicht bereitstellen und den Vermittlungsserver nicht mit dem Enterprise EditionFront-collocate oder dem Standard Edition-Server abgleichen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-120">This step is required only if you do not deploy Enterprise Voice and do not collocate the Mediation Server with the Enterprise EditionFront End Server or Standard Edition server.</span></span> <span data-ttu-id="0ce7d-121">Wenn Sie Enterprise-VoIP bereitstellen, installieren und konfigurieren Sie Vermittlungsserver und PSTN-Gateways als Teil der Enterprise-VoIP-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-121">If you deploy Enterprise Voice, you install and configure Mediation Servers and PSTN gateways as part of the Enterprise Voice deployment.</span></span> <span data-ttu-id="0ce7d-122">Wenn Sie den Vermittlungsserver collocate, installieren und konfigurieren Sie den Vermittlungsserver als Teil des Front-End-Pools oder der Standard Edition-Server Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-122">If you collocate the Mediation Server, you install and configure the Mediation Server as part of the Front End pool or Standard Edition server deployment.</span></span>


</div></li>
</ol></td>
<td><p><span data-ttu-id="0ce7d-123">Domänen-Admins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-123">Domain Admins</span></span></p>
<p><span data-ttu-id="0ce7d-124">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-124">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-125">Administrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-125">Administrator</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="0ce7d-126"><a href="lync-server-2013-deploying-lync-server.md">Bereitstellen von Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-126"><a href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</a></span></span></p></li>
<li><p><span data-ttu-id="0ce7d-127">So erstellen Sie einen eigenständigen vermittlungsserverpool: <a href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Bereitstellen von Vermittlungsservern und Definieren von Peers in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-127">To create a stand-alone Mediation Server pool: <a href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Deploying Mediation Servers and defining peers in Lync Server 2013</a></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-128"><strong>Configure dial plans</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-128"><strong>Configure dial plans</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-129">Bei Wähleinstellungen handelt es sich um einen Satz Rufnummernormalisierungsregeln, die von einem bestimmten Standort aus gewählte Rufnummern in ein einziges Standardformat (E.164) übersetzen, um die Telefonautorisierung und das Anrufrouting zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-129">A dial plan is a set of phone number normalization rules that translate phone numbers dialed from a specific location to a single standard (E.164) format for purposes of phone authorization and call routing.</span></span> <span data-ttu-id="0ce7d-130">Eine von verschiedenen Standorten aus gewählte Rufnummer kann je nach Wähleinstellungen dem Standort entsprechend in unterschiedliche E.164-Nummern aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-130">The same phone number dialed from different locations can, based on the respective dial plans, resolve to different E.164 numbers, as appropriate to each location.</span></span> <span data-ttu-id="0ce7d-131">Wenn Sie Enterprise-VoIP bereitstellen, richten Sie Wählpläne als Teil dieser Bereitstellung ein, und Sie müssen sicherstellen, dass die Wählpläne auch Einwahlkonferenzen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-131">If you deploy Enterprise Voice, you set up dial plans as part of that deployment, and you need to make sure that the dial plans also accommodate dial-in conferencing.</span></span> <span data-ttu-id="0ce7d-132">Wenn Sie Enterprise-VoIP nicht bereitstellen, müssen Sie Wählpläne für Einwahlkonferenzen einrichten.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-132">If you do not deploy Enterprise Voice, you need to set up dial plans for dial-in conferencing.</span></span></p>
<p><span data-ttu-id="0ce7d-133">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell zum Einrichten von Wählplänen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ce7d-133">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to set up dial plans as follows:</span></span></p>
<ol>
<li><p><span data-ttu-id="0ce7d-134">Erstellen Sie einen oder mehrere Sätze mit Wähleinstellungen zum Routen von Zugriffsnummern für die Einwahl.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-134">Create one or more dial plans for routing dial-in access phone numbers.</span></span></p></li>
<li><p><span data-ttu-id="0ce7d-p105">Weisen Sie jedem Pool einen Standardsatz mit Wähleinstellungen zu. Legen Sie die <strong>Region für Einwahlkonferenzen</strong> auf den geografischen Standort fest, für den die Wähleinstellungen gelten. Die Region ordnet die Wähleinstellungen den Zugriffsnummern für die Einwahl zu.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-p105">Assign a default dial plan to each pool. Set the <strong>Dial-in conferencing region</strong> to the geographic location to which the dial plan applies. The region associates the dial plan with dial-in access numbers.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="0ce7d-138">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-138">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-139">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-139">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-140">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-140">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-141">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-141">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-142"><a href="lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md">Konfigurieren von Wählplänen für Einwahlkonferenzen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-142"><a href="lync-server-2013-configure-dial-plans-for-dial-in-conferencing.md">Configure dial plans for dial-in conferencing in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-143"><strong>Sicherstellen, dass den Wähleinstellungen Regionen zugeordnet werden</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-143"><strong>Make sure that dial plans are assigned regions</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-144">Führen Sie die Cmdlets <strong>Get-CsDialPlan</strong> und <strong>Set-CsDialPlan</strong> aus, um sicherzustellen, dass allen Wähleinstellungen eine Region zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-144">Run the <strong>Get-CsDialPlan</strong> and <strong>Set-CsDialPlan</strong> cmdlets to make sure that all dial plans have a region assigned.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-145">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-145">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-146">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-146">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-147">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-147">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-148">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-148">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-149"><a href="lync-server-2013-make-sure-dial-plans-have-assigned-regions.md">Sicherstellen, dass die Wähleinstellungen lync Server 2013 Regionen zugewiesen haben</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-149"><a href="lync-server-2013-make-sure-dial-plans-have-assigned-regions.md">Make sure dial plans Lync Server 2013 have assigned regions</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-150"><strong>(Optional) Überprüfen oder Ändern der Anforderungen an die persönliche Identifikationsnummer (PIN) der Benutzer.</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-150"><strong>(Optional) Verify or modify user personal identification number (PIN) requirements</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-151">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell zum Anzeigen oder Ändern der Konferenz- <strong>PIN-Richtlinie</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-151">Use Lync Server 2013 Control Panel or Lync Server Management Shell to view or modify the Conferencing <strong>PIN Policy</strong>.</span></span> <span data-ttu-id="0ce7d-152">Sie können eine PIN-Mindestlänge, eine maximale Anzahl von Anmeldeversuchen, ein PIN-Ablaufdatum und die Zulässigkeit gängiger Muster festlegen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-152">You can specify minimum PIN length, maximum number of logon attempts, PIN expiration, and whether common patterns are allowable.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-153">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-153">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-154">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-154">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-155">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-155">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-156"><a href="lync-server-2013-optional-verify-pin-policy-settings.md">(Optional) Überprüfen der PIN-Richtlinieneinstellungen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-156"><a href="lync-server-2013-optional-verify-pin-policy-settings.md">(Optional) Verify PIN policy settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-157"><strong>Konfigurieren Sie die Konferenzrichtlinie so, dass Einwahlkonferenzen unterstützt werden.</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-157"><strong>Configure conferencing policy to support dial-in conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-158">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell zum Konfigurieren von <strong>Konferenzrichtlinien</strong> Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-158">Use Lync Server 2013 Control Panel or Lync Server Management Shell to configure <strong>Conferencing Policy</strong> settings.</span></span> <span data-ttu-id="0ce7d-159">Legen Sie folgende Einstellungen fest:</span><span class="sxs-lookup"><span data-stu-id="0ce7d-159">Specify whether:</span></span></p>
<ul>
<li><p><span data-ttu-id="0ce7d-160">Die PSTN-Konferenzeinwahl ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-160">PSTN conference dial-in is enabled.</span></span></p></li>
<li><p><span data-ttu-id="0ce7d-161">Benutzer können anonyme Teilnehmer einladen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-161">Users can invite anonymous participants.</span></span></p></li>
<li><p><span data-ttu-id="0ce7d-p108">Nicht authentifizierte Benutzer können über ausgehende Telefonverbindungen an einer Konferenz teilnehmen. Bei ausgehenden Telefonverbindungen ruft der Konferenzserver den Benutzer an und der Benutzer nimmt das Gespräch an, um an der Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-p108">Unauthenticated users can join a conference by using dial-out phoning. With dial-out phoning, the conference server calls the user, and the user answers the phone to join the conference.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="0ce7d-164">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-164">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-165">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-165">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-166">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-166">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-167"><a href="lync-server-2013-configure-conferencing-policy-for-dial-in.md">Konfigurieren von Konferenzrichtlinien für die Einwahl in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-167"><a href="lync-server-2013-configure-conferencing-policy-for-dial-in.md">Configure conferencing policy for dial-in in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-168"><strong>Configure dial-in access numbers</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-168"><strong>Configure dial-in access numbers</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-169">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell zum Einrichten von Einwahl Zugriffsnummern, die Benutzer anrufen, um sich in eine Konferenz einzuwählen, und geben Sie die Regionen an, die die Zugriffsnummer mit den entsprechenden Wählplänen verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-169">Use Lync Server 2013 Control Panel or Lync Server Management Shell to set up dial-in access numbers that users call to dial in to a conference, and specify the regions that associate the access number with the appropriate dial plans.</span></span> <span data-ttu-id="0ce7d-170">Die ersten drei Zugriffsnummern für die Region, die durch die Wähleinstellungen des Organisators festgelegt wird, sind in der Konferenzeinladung enthalten.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-170">The first three access numbers for the region specified by the organizer's dial plan are included in the conference invitation.</span></span> <span data-ttu-id="0ce7d-171">Alle Zugriffsnummern sind auf der Seite Einstellungen für Einwahlkonferenzen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-171">All access numbers are available on the Dial-in Conferencing Settings page.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="0ce7d-172">Nachdem Sie Einwahl Zugriffsnummern erstellt haben, können Sie das Cmdlet " <STRONG>festlegen-CsDialInConferencingAccessNumber</STRONG> " verwenden, um den Anzeigenamen der Active Directory-Kontaktobjekte zu ändern, damit Benutzer die richtige Zugriffsnummer leichter identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-172">After you create dial-in access numbers, you can use the <STRONG>Set-CsDialInConferencingAccessNumber</STRONG> cmdlet to modify the display name of the Active Directory contact objects so that users can more easily identify the correct access number.</span></span>


</div></td>
<td><p><span data-ttu-id="0ce7d-173">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-173">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-174">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-174">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-175">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-175">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-176"><a href="lync-server-2013-configure-dial-in-conferencing-access-numbers.md">Konfigurieren von Einwahlnummern für Einwahlkonferenzen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-176"><a href="lync-server-2013-configure-dial-in-conferencing-access-numbers.md">Configure dial-in conferencing access numbers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-177"><strong>(Optional) Überprüfen der Einwahlkonferenzeinstellungen</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-177"><strong>(Optional) Verify dial-in conferencing settings</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-178">Suchen Sie mithilfe des Cmdlets <strong>Get-CsDialinConferencingAccessNumber</strong> nach Wähleinstellungen, deren Einwahlkonferenzregion von keiner Zugriffsnummer verwendet wird, und nach Zugriffsnummern, denen keine Region zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-178">Use the <strong>Get-CsDialinConferencingAccessNumber</strong> cmdlet to search for dial plans that have a dial-in conferencing region that is not used by any access number and for access numbers that have no region assigned.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-179">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-179">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-180">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-180">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-181">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-181">CsAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-182">CsViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-182">CsViewOnlyAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-183">CsHelpDesk</span><span class="sxs-lookup"><span data-stu-id="0ce7d-183">CsHelpDesk</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-184"><a href="lync-server-2013-optional-verify-dial-in-conferencing-settings.md">(Optional) Überprüfen der Einwahlkonferenzeinstellungen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-184"><a href="lync-server-2013-optional-verify-dial-in-conferencing-settings.md">(Optional) Verify dial-in conferencing settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-185"><strong>(Optional) Ändern der Tastenzuordnung von DTMF-Befehlen</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-185"><strong>(Optional) Modify key mapping of DTMF commands</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-186">Verwenden Sie das Cmdlet " <strong>CsDialinConferencingDtmfConfiguration</strong> ", um die Tasten zu ändern, die für DTMF-Befehle (Dual Tone MultiFrequency) verwendet werden, mit denen die Teilnehmer Konferenzeinstellungen steuern können (wie Stummschaltung und Aufheben der Stummschaltung oder sperren und entsperren).</span><span class="sxs-lookup"><span data-stu-id="0ce7d-186">Use the <strong>Set-CsDialinConferencingDtmfConfiguration</strong> cmdlet to modify the keys used for dual-tone multifrequency (DTMF) commands, which participants can use to control conference settings (such as mute and unmute or lock and unlock).</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-187">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-187">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-188">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-188">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-189">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-189">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-190"><a href="lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md">(Optional) Ändern der Tastenzuordnung für DTMF-Befehle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-190"><a href="lync-server-2013-optional-modify-key-mapping-for-dtmf-commands.md">(Optional) Modify key mapping for DTMF commands in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-191"><strong>(Optional) Ändern des Ankündigungsverhaltens beim Beitreten oder Verlassen einer Konferenz</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-191"><strong>(Optional) Modify conference join and leave announcement behavior</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-192">Ändern Sie mit dem Cmdlet <strong>Set-CsDialinConferencingConfiguration</strong> die Funktionsweise von Ankündigungen, wenn Teilnehmer einer Konferenz beitreten bzw. diese verlassen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-192">Use the <strong>Set-CsDialinConferencingConfiguration</strong> to change how announcements work when participants join and leave conferences.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-193">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-193">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-194">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-194">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-195">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-195">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-196"><a href="lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md">(Optional) Aktivieren und Deaktivieren von Konferenzankündigungen beim Beitreten und Verlassen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-196"><a href="lync-server-2013-optional-enable-and-disable-conference-join-and-leave-announcements.md">(Optional) Enable and disable conference join and leave announcements in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-197"><strong>(Optional) Überprüfen von Einwahlkonferenzen</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-197"><strong>(Optional) Verify dial-in conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-198">Testen Sie mithilfe des Cmdlets <strong>Test-CsDialInConferencing</strong>, ob die Zugriffsnummern für den angegebenen Pool ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-198">Use the <strong>Test-CsDialInConferencing</strong> cmdlet to test that the access numbers for the specified pool work correctly.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-199">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-199">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-200">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-200">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-201">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-201">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-202"><a href="lync-server-2013-optional-verify-dial-in-conferencing.md">(Optional) Überprüfen von Einwahlkonferenzen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-202"><a href="lync-server-2013-optional-verify-dial-in-conferencing.md">(Optional) Verify dial-in conferencing in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-203"><strong>Bereitstellen des Onlinebesprechungs-Add-Ins für Lync 2013</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-203"><strong>Deploy the Online Meeting Add-in for Lync 2013</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-204">Stellen Sie das Online Besprechungs-Add-in für lync 2013 bereit, damit Benutzer Konferenzen planen können, die Einwahlkonferenzen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-204">Deploy the Online Meeting Add-in for Lync 2013 so that users can schedule conferences that support dial-in conferencing.</span></span> <span data-ttu-id="0ce7d-205">Das Online Besprechungs-Add-in für lync 2013 wird automatisch installiert, wenn Sie lync 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-205">The Online Meeting Add-in for Lync 2013 is installed automatically when you install Lync 2013.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-206">Administratoren</span><span class="sxs-lookup"><span data-stu-id="0ce7d-206">Administrators</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-207"><a href="lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md">Bereitstellen des Onlinebesprechungs-Add-Ins für Lync 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-207"><a href="lync-server-2013-deploy-the-online-meeting-add-in-for-lync-2013.md">Deploy the Online Meeting Add-in for Lync 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-208"><strong>Konfigurieren der Benutzerkontoeinstellungen</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-208"><strong>Configure user account settings</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-209">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell, um den URI der Telefon <strong>Leitung</strong> als eindeutige, normalisierte Telefonnummer zu konfigurieren (beispielsweise Tel: + 14255550200).</span><span class="sxs-lookup"><span data-stu-id="0ce7d-209">Use Lync Server 2013 Control Panel or Lync Server Management Shell to configure the telephony <strong>Line URI</strong> as a unique, normalized phone number (for example, tel:+14255550200).</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-210">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-210">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="0ce7d-211">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-211">CsAdministrator</span></span></p>
<p><span data-ttu-id="0ce7d-212">CsUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="0ce7d-212">CsUserAdministrator</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-213"><a href="lync-server-2013-configure-user-account-settings.md">Konfigurieren der Benutzerkontoeinstellungen  in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-213"><a href="lync-server-2013-configure-user-account-settings.md">Configure user account settings in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ce7d-214">(Empfohlen) Konfigurieren von Konferenzverzeichnissen</span><span class="sxs-lookup"><span data-stu-id="0ce7d-214">(Recommended) Configure conference directories</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-215">Verwenden Sie das Cmdlet <strong>New-CsConferenceDirectory</strong>, um ein Konferenzverzeichnis pro 999 Benutzer im Pool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-215">Use the <strong>New-CsConferenceDirectory</strong> cmdlet to create one conference directory for every 999 users in the pool.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-216">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-216">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-217"><a href="lync-server-2013-dial-in-conferencing-requirements.md">Anforderungen für Einwahlkonferenzen in lync Server 2013</a> <a href="recommended-create-conference-directories.md">(empfohlen) Erstellen von Konferenz Verzeichnissen</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-217"><a href="lync-server-2013-dial-in-conferencing-requirements.md">Dial-in conferencing requirements in Lync Server 2013</a> <a href="recommended-create-conference-directories.md">(Recommended) Create Conference Directories</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ce7d-218"><strong>(Optional) Einladen von Benutzern zu Einwahlkonferenzen und Festlegen der anfänglichen PIN</strong></span><span class="sxs-lookup"><span data-stu-id="0ce7d-218"><strong>(Optional) Welcome users to dial-in conferencing and set the initial PIN</strong></span></span></p></td>
<td><p><span data-ttu-id="0ce7d-219">Verwenden Sie das <strong>CsPinSendCAWelcomeMail-</strong> Skript, um die anfänglichen Pins der Benutzer festzulegen und eine Willkommens-e-Mail zu senden, die die ursprüngliche PIN und einen Link zur Seite Einstellungen für Einwahlkonferenzen enthält.</span><span class="sxs-lookup"><span data-stu-id="0ce7d-219">Use the <strong>Set-CsPinSendCAWelcomeMail</strong> script to set users' initial PINs and send a welcome email that contains the initial PIN and a link to the Dial-in Conferencing Settings page.</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-220">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="0ce7d-220">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="0ce7d-221"><a href="lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md">(Optional) Einladen von Benutzern zu Einwahlkonferenzen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="0ce7d-221"><a href="lync-server-2013-optional-welcome-users-to-dial-in-conferencing.md">(Optional) Welcome users to dial-in conferencing in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="0ce7d-222">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0ce7d-222">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

