---
title: 'Lync Server 2013: Bereitstellungsprozess für die Gruppenanruf Abholung'
description: 'Lync Server 2013: Bereitstellungsprozess für die Gruppenanruf Abholung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Group Call Pickup
ms:assetid: 082daeac-e667-4e2d-b78d-8e0901f9f0e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945615(v=OCS.15)
ms:contentKeyID: 51541444
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a01409b257c685ae71dfdb13074f2d8ea590cd9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394930"
---
# <a name="deployment-process-for-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="23093-103">Bereitstellungsprozess für die Gruppenanruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23093-103">Deployment process for Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23093-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23093-104">

<span> </span></span></span>

<span data-ttu-id="23093-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="23093-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="23093-106">Dieser Abschnitt enthält eine Übersicht über die Schritte, die beim Bereitstellen von Gruppenanruf Pickups erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="23093-106">This section provides an overview of the steps involved in deploying Group Call Pickup.</span></span> <span data-ttu-id="23093-107">Sie müssen Enterprise Edition oder Standard Edition mit Enterprise-VoIP bereitstellen, bevor Sie die Gruppenanruf Abholung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="23093-107">You must deploy Enterprise Edition or Standard Edition with Enterprise Voice before you configure Group Call Pickup.</span></span> <span data-ttu-id="23093-108">Die für die Gruppenanruf Abholung erforderlichen Komponenten werden bei der Bereitstellung von Enterprise-VoIP installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="23093-108">The components required by Group Call Pickup are installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="group-call-pickup-deployment-process"></a><span data-ttu-id="23093-109">Bereitstellungsprozess für die Gruppenanrufannahme</span><span class="sxs-lookup"><span data-stu-id="23093-109">Group Call Pickup Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23093-110">Phase</span><span class="sxs-lookup"><span data-stu-id="23093-110">Phase</span></span></th>
<th><span data-ttu-id="23093-111">Schritte</span><span class="sxs-lookup"><span data-stu-id="23093-111">Steps</span></span></th>
<th><span data-ttu-id="23093-112">Erforderliche Gruppen und Rollen</span><span class="sxs-lookup"><span data-stu-id="23093-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="23093-113">Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="23093-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23093-114">Aktivieren des SEFAUtil Resource Kit-Tools in der Topologie</span><span class="sxs-lookup"><span data-stu-id="23093-114">Enable the SEFAUtil resource kit tool in the topology</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="23093-115">Erstellen Sie mithilfe des Cmdlets <strong>New-CsTrustedApplicationPool</strong> einen neuen vertrauenswürdigen Anwendungspool.</span><span class="sxs-lookup"><span data-stu-id="23093-115">Use the <strong>New-CsTrustedApplicationPool</strong> cmdlet to create a new trusted application pool.</span></span></p></li>
<li><p><span data-ttu-id="23093-116">Legen Sie mithilfe des Cmdlets <strong>New-CsTrustedApplication</strong> das SEFAUtil-Tool als vertrauenswürdige Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="23093-116">Use the <strong>New-CsTrustedApplication</strong> cmdlet to specify the SEFAUtil tool as trusted application.</span></span></p></li>
<li><p><span data-ttu-id="23093-117">Führen Sie das Cmdlet <strong>Enable-CsTopology</strong> aus, um die Topologie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="23093-117">Run the <strong>Enable-CsTopology</strong> cmdlet to enable the topology.</span></span></p></li>
<li><p><span data-ttu-id="23093-118">Installieren Sie die Resource Kit-Tools auf einem Front-End-Server, der sich im vertrauenswürdigen Anwendungspool befindet, der in Schritt 1 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="23093-118">Install the resource kit tools on a Front End Server that is in the trusted application pool created in step 1.</span></span></p></li>
<li><p><span data-ttu-id="23093-119">Überprüfen Sie, ob SEFAUtil ordnungsgemäß ausgeführt wird. Führen Sie dazu das Tool aus, um die Anrufweiterleitungseinstellungen eines Benutzers in der Bereitstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="23093-119">Verify that SEFAUtil is running correctly by running it to display the call forwarding settings of a user in the deployment.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="23093-120">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="23093-120">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="23093-121"><a href="lync-server-2013-deploy-the-sefautil-tool.md">Deploy the SEFAUtil tool in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23093-121"><a href="lync-server-2013-deploy-the-sefautil-tool.md">Deploy the SEFAUtil tool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23093-122">Konfigurieren von Nummernbereichen für die Anrufannahme in der Orbittabelle für das Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="23093-122">Configure call pickup number ranges in the call park orbit table</span></span></p></td>
<td><p><span data-ttu-id="23093-123">Verwenden Sie das Cmdlet <strong>New-CSCallParkOrbit</strong> , um die Nummernbereiche für die Anruf Abholung in der Umlaufbahn Tabelle des Anrufs zu erstellen, und weisen Sie den Anruf-abholbereich den Typ GroupPickup zu.</span><span class="sxs-lookup"><span data-stu-id="23093-123">Use the <strong>New-CSCallParkOrbit</strong> cmdlet to create call pickup number ranges in the call park orbit table and assign the call pickup ranges the type GroupPickup.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="23093-124">Sie müssen die lync Server-Verwaltungsshell zum Erstellen, ändern, entfernen und Anzeigen von Gruppenanruf-Pickup-Nummernbereichen in der Orbit-Tabelle des Anruf Parks verwenden.</span><span class="sxs-lookup"><span data-stu-id="23093-124">You must use Lync Server Management Shell to create, modify, remove, and view Group Call Pickup number ranges in the call park orbit table.</span></span> <span data-ttu-id="23093-125">Gruppenanruf-Abhol Nummernbereiche sind in der lync Server-Systemsteuerung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="23093-125">Group Call Pickup number ranges are not available in Lync Server Control Panel.</span></span>


</div>
<div>

> [!NOTE]  
> <span data-ttu-id="23093-p103">Um eine nahtlose Integration in vorhandene Wählpläne zu ermöglichen, sind Nummernbereiche in der Regel als Block virtueller Durchwahlnummern konfiguriert. Das Zuweisen von DID (Direct Inward Dialing)-Nummern als Orbitnummern in der Orbittabelle für das Parken von Anrufen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="23093-p103">For seamless integration with existing dial plans, number ranges are typically configured as a block of virtual extensions. Assigning Direct Inward Dialing (DID) numbers as range numbers in the call park orbit table is not supported.</span></span>


</div></td>
<td><p><span data-ttu-id="23093-128">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="23093-128">RTCUniversalServerAdmins</span></span></p>
<p><span data-ttu-id="23093-129">CsVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="23093-129">CsVoiceAdministrator</span></span></p>
<p><span data-ttu-id="23093-130">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="23093-130">CsServerAdministrator</span></span></p>
<p><span data-ttu-id="23093-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="23093-131">CsAdministrator</span></span></p></td>
<td><p><span data-ttu-id="23093-132"><a href="lync-server-2013-configure-call-pickup-group-numbers.md">Konfigurieren von Gruppennummern für die Anruf Abholung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23093-132"><a href="lync-server-2013-configure-call-pickup-group-numbers.md">Configure call pickup group numbers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23093-133">Zuweisen einer Anruf-Abholnummer zu Benutzern und Aktivieren der Gruppenanruf Abholung für die Benutzer</span><span class="sxs-lookup"><span data-stu-id="23093-133">Assign a call pickup number to users, and enable Group Call Pickup for the users</span></span></p></td>
<td><p><span data-ttu-id="23093-134">Verwenden Sie den/enablegrouppickup-Parameter im SEFAUtil Resource Kit-Tool, um die Gruppenanruf Abholung zu aktivieren und Benutzern eine Anruf-Abholnummer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="23093-134">Use the /enablegrouppickup parameter in the SEFAUtil resource kit tool to enable Group Call Pickup and assign a call pickup number for users.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="23093-135"><a href="lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md">Aktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013 und Zuweisen einer Gruppennummer</a></span><span class="sxs-lookup"><span data-stu-id="23093-135"><a href="lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23093-136">Informieren der Benutzer über die ihnen zugewiesene Nummer für die Anrufannahme und weitere relevante Nummern</span><span class="sxs-lookup"><span data-stu-id="23093-136">Notify users of their assigned call pickup number and any other number of interest</span></span></p></td>
<td><p><span data-ttu-id="23093-137">Da Benutzer einen Anruf an einen Gruppenanruf-Pickup-Benutzer abrufen können, möchten Sie möglicherweise mehr als eine Gruppe überwachen.</span><span class="sxs-lookup"><span data-stu-id="23093-137">Because any user can retrieve a call made to a Group Call Pickup user, users may want to monitor more than one group.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="23093-138"><a href="lync-server-2013-communicate-group-call-pickup-assignment-to-users.md">Übermitteln von Gruppenanruf-Abholaufträgen an Benutzer in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23093-138"><a href="lync-server-2013-communicate-group-call-pickup-assignment-to-users.md">Communicate Group Call Pickup assignments to users in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23093-139">Überprüfen der Bereitstellung Ihrer Gruppenanruf Abholung</span><span class="sxs-lookup"><span data-stu-id="23093-139">Verify your Group Call Pickup deployment</span></span></p></td>
<td><p><span data-ttu-id="23093-140">Testen Sie Anrufe und das Abrufen von Anrufen, um sicherzustellen, dass Ihre Konfiguration erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="23093-140">Test placing and retrieving calls to make sure that your configuration works as expected.</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="23093-141"><a href="lync-server-2013-optional-verify-the-group-call-pickup-deployment.md">Optional Überprüfen der Bereitstellung für die Gruppenanruf Abholung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23093-141"><a href="lync-server-2013-optional-verify-the-group-call-pickup-deployment.md">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</a></span></span></p></td>
</tr><span data-ttu-id="23093-142">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23093-142">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

