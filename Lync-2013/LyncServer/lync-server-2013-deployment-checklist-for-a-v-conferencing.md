---
title: Lync Server 2013-Bereitstellungscheckliste für A/V-Konferenzen
description: Lync Server 2013-Bereitstellungscheckliste für A/V-Konferenzen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for A/V conferencing
ms:assetid: 6d47426f-6559-407b-9ac1-2453f0b7a2a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619183(v=OCS.15)
ms:contentKeyID: 49733684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9a4584172ed4c01eb163ea51aa4f62c2ce75185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429755"
---
# <a name="deployment-checklist-for-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="0876e-103">Bereitstellungscheckliste für A/V-Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0876e-103">Deployment checklist for A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0876e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0876e-104">

<span> </span></span></span>

<span data-ttu-id="0876e-105">_**Letztes Änderungsdatum des Themas:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="0876e-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="0876e-106">Wie bei der Bereitstellung Ihrer anderen lync Server 2013-Komponenten erfordert die Bereitstellung von a/V-Konferenzen, dass Sie den Topologie-Generator verwenden, um eine Topologie zu erstellen und zu veröffentlichen, in der Konferenzen integriert sind.</span><span class="sxs-lookup"><span data-stu-id="0876e-106">As with deployment of your other Lync Server 2013 components, deployment of A/V conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="0876e-107">Bereitstellungssequenz</span><span class="sxs-lookup"><span data-stu-id="0876e-107">Deployment Sequence</span></span>

<span data-ttu-id="0876e-108">Sie können Konferenzen gleichzeitig bereitstellen, indem Sie Ihre anfängliche Topologie bereitstellen oder nachdem Sie mindestens einen Front-End-Pool oder Standard Edition-Server bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="0876e-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="0876e-109">Konferenz Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="0876e-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="0876e-110">Die folgende Tabelle enthält eine Übersicht über die erforderlichen Schritte zum Bereitstellen von Konferenzen in einer vorhandenen Topologie.</span><span class="sxs-lookup"><span data-stu-id="0876e-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0876e-111">Phase</span><span class="sxs-lookup"><span data-stu-id="0876e-111">Phase</span></span></th>
<th><span data-ttu-id="0876e-112">Schritte</span><span class="sxs-lookup"><span data-stu-id="0876e-112">Steps</span></span></th>
<th><span data-ttu-id="0876e-113">Rollen und Gruppenmitgliedschaften</span><span class="sxs-lookup"><span data-stu-id="0876e-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="0876e-114">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="0876e-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0876e-115"><strong>Installieren der erforderlichen Hardware und Software</strong></span><span class="sxs-lookup"><span data-stu-id="0876e-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="0876e-116">Konferenzen werden auf Front-End-Servern eines Front-End-Pools und von Standard Edition-Servern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0876e-116">Conferencing runs on Front End Servers of a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="0876e-117">Abgesehen von den herkömmlichen Anforderungen zur Installation dieser Server bestehen keine zusätzlichen Hardware- oder Softwareanforderungen.</span><span class="sxs-lookup"><span data-stu-id="0876e-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="0876e-118">In lync Server 2013 werden Office Web Apps und der Office Web Apps-Server verwendet, um die Freigabe und das Rendern von PowerPoint-Präsentationen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0876e-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="0876e-119">Details zum Installieren und Konfigurieren des Office Web Apps-Servers finden Sie unter <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Konfigurieren der Integration in Office Web Apps Server und lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0876e-119">For details about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="0876e-120">Domänenbenutzer, der Mitglied der lokalen Administratorgruppe ist</span><span class="sxs-lookup"><span data-stu-id="0876e-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="0876e-121"><a href="lync-server-2013-supported-hardware.md">Unterstützte Hardware für lync Server 2013</a> in der Dokumentation zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0876e-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="0876e-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Unterstützung für Server Software und-Infrastruktur in lync Server 2013</a> in der Dokumentation zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="0876e-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="0876e-123"><a href="lync-server-2013-determining-your-system-requirements.md">Ermitteln der Systemanforderungen für lync Server 2013</a> in der Planungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="0876e-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="0876e-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technische Voraussetzungen für die Archivierung in lync Server 2013</a> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="0876e-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0876e-125"><strong>Erstellen der geeigneten internen Topologie zur Unterstützung von Konferenzen</strong></span><span class="sxs-lookup"><span data-stu-id="0876e-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="0876e-126">Führen Sie den Topologie-Generator aus, um der Topologie Konferenzen hinzuzufügen, und veröffentlichen Sie dann die Topologie.</span><span class="sxs-lookup"><span data-stu-id="0876e-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="0876e-127">Zum Definieren einer Topologie: Konto, das Mitglied der lokalen Benutzergruppe ist</span><span class="sxs-lookup"><span data-stu-id="0876e-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="0876e-128">So veröffentlichen Sie die Topologie: ein Konto, das ein Mitglied der Gruppe "Domänen-Admins" und der RTCUniversalServerAdmins-Gruppe ist und das Vollzugriffsberechtigungen (Lesen/Schreiben/ändern) für die Dateifreigabe hat, die für den lync Server 2013-Dateispeicher verwendet werden soll (damit der Topologie-Generator die erforderlichen DACLs konfigurieren kann)</span><span class="sxs-lookup"><span data-stu-id="0876e-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="0876e-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Definieren und konfigurieren Sie eine Topologie im Topologie-Generator für lync Server 2013</a> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="0876e-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0876e-130"><strong>Konfigurieren von Konferenzrichtlinien und-Support</strong></span><span class="sxs-lookup"><span data-stu-id="0876e-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="0876e-131">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell, um Konferenzeinstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0876e-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="0876e-132">RTCUniversalServerAdmins-Gruppe (nur Windows PowerShell) oder Zuweisen von Benutzern zur []-oder CSAdministrator-Rolle</span><span class="sxs-lookup"><span data-stu-id="0876e-132">RTCUniversalServerAdmins group (Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="0876e-133"><a href="lync-server-2013-conferencing-policies.md">Konferenzrichtlinien in lync Server 2013</a> in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="0876e-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0876e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0876e-134">See Also</span></span>


[<span data-ttu-id="0876e-135">Übersicht über Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0876e-135">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)  
[<span data-ttu-id="0876e-136">Definieren der Anforderungen für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0876e-136">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)  
  

<span data-ttu-id="0876e-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0876e-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

