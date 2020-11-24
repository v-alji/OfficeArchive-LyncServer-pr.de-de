---
title: 'Lync Server 2013: Prüfliste für die Bereitstellung der Anrufsteuerung'
description: 'Lync Server 2013: Bereitstellungscheckliste für die Anrufsteuerung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for call admission control
ms:assetid: 7e56a169-3e63-44ab-bf28-1fdeb52381c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398631(v=OCS.15)
ms:contentKeyID: 48184621
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea5b16d41228faf01637e7e0d78f5ce56f950a19
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393822"
---
# <a name="deployment-checklist-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="7f527-103">Prüfliste für die Bereitstellung der Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f527-103">Deployment checklist for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f527-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f527-104">

<span> </span></span></span>

<span data-ttu-id="7f527-105">_**Letztes Änderungsdatum des Themas:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="7f527-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="7f527-106">Damit Sie effektiv für die Anrufsteuerung (CAC) planen können, müssen Sie Folgendes in Frage stellen:</span><span class="sxs-lookup"><span data-stu-id="7f527-106">To plan effectively for call admission control (CAC), you need to consider the following:</span></span>

  - <span data-ttu-id="7f527-107">Voraussetzungen für die Bereitstellung von CAC.</span><span class="sxs-lookup"><span data-stu-id="7f527-107">Prerequisites for deploying CAC.</span></span>

  - <span data-ttu-id="7f527-108">Informationen, die für CAC-und Konfigurationsentscheidungen erforderlich sind, die Sie im Vorfeld der Bereitstellung vornehmen müssen.</span><span class="sxs-lookup"><span data-stu-id="7f527-108">Information required for CAC and configuration decisions that you must make in advance of deployment.</span></span>

<div>

## <a name="deployment-prerequisites-for-call-admission-control"></a><span data-ttu-id="7f527-109">Voraussetzungen für die Bereitstellung der Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="7f527-109">Deployment Prerequisites for Call Admission Control</span></span>

<span data-ttu-id="7f527-110">Bevor Sie die Anrufsteuerung bereitstellen, müssen Sie Ihre lync Server 2013-internen Server bereits bereitgestellt haben, einschließlich eines Front-End-Pools oder eines Standard Edition-Servers.</span><span class="sxs-lookup"><span data-stu-id="7f527-110">Before you deploy call admission control, you must already have deployed your Lync Server 2013 internal servers, including either a Front End pool or a Standard Edition server.</span></span>

</div>

<div>

## <a name="information-requirements-for-call-admission-control"></a><span data-ttu-id="7f527-111">Informationsanforderungen für die Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="7f527-111">Information Requirements for Call Admission Control</span></span>

<span data-ttu-id="7f527-112">In der folgenden Tabelle sind die erforderlichen Informationen für die Bereitstellung der Anrufsteuerung zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="7f527-112">The following table summarizes the required information for deploying call admission control.</span></span>

### <a name="information-requirements-for-call-admission-control-deployment"></a><span data-ttu-id="7f527-113">Informationsanforderungen für die Bereitstellung von Anruf Zulassungs Steuerungen</span><span class="sxs-lookup"><span data-stu-id="7f527-113">Information Requirements for Call Admission Control Deployment</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f527-114">Informationen</span><span class="sxs-lookup"><span data-stu-id="7f527-114">Information</span></span></th>
<th><span data-ttu-id="7f527-115">Zusammenfassung der erforderlichen Informationen</span><span class="sxs-lookup"><span data-stu-id="7f527-115">Summary of Information Required</span></span></th>
<th><span data-ttu-id="7f527-116">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7f527-116">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f527-117">Für Ihre Organisation erforderliche lync Server-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f527-117">Lync Server capabilities required by your organization</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-118">Von Ihrer Organisation unterstützte Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f527-118">Capabilities to be supported by your organization</span></span></p></li>
<li><p><span data-ttu-id="7f527-119">Funktionen, die für einzelne Benutzer aktiviert werden können</span><span class="sxs-lookup"><span data-stu-id="7f527-119">Capabilities to be enabled for individual users</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definieren der Anforderungen Ihrer Organisation für die Anrufsteuerung in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-120"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f527-121">Topologien und Komponenten, die bereitgestellt werden sollen</span><span class="sxs-lookup"><span data-stu-id="7f527-121">Topologies and components to be deployed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-122">Mit CAC verknüpfte Komponenten werden automatisch als Teil von lync Server 2013 installiert</span><span class="sxs-lookup"><span data-stu-id="7f527-122">CAC related components are automatically installed as part of Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definieren der Anforderungen Ihrer Organisation für die Anrufsteuerung in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-123"><a href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f527-124">Systemanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-124">System requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-125">Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-125">Hardware requirements</span></span></p></li>
<li><p><span data-ttu-id="7f527-126">Softwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-126">Software requirements</span></span></p></li>
<li><p><span data-ttu-id="7f527-127">Anforderungen für die Übersetzung</span><span class="sxs-lookup"><span data-stu-id="7f527-127">Collocation requirements</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-128"><a href="lync-server-2013-determining-your-system-requirements.md">Ermitteln Ihrer Systemanforderungen für Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-128"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f527-129">Infrastrukturanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-129">Infrastructure requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-130">Für CAC sind keine spezifischen Infrastrukturanforderungen erforderlich</span><span class="sxs-lookup"><span data-stu-id="7f527-130">No specific infrastructure requirements are necessary for CAC</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastrukturanforderungen für die Anrufsteuerung in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-131"><a href="lync-server-2013-infrastructure-requirements-for-call-admission-control.md">Infrastructure requirements for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f527-132">Netzwerkschnittstellen Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-132">Network interface requirements</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-133">Interne und externe Schnittstelleninformationen</span><span class="sxs-lookup"><span data-stu-id="7f527-133">Internal and external interface information</span></span></p></li>
<li><p><span data-ttu-id="7f527-134">Routing Informationen (einschließlich Informationen im NextHop-Blog unter dem <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a> Kundenantwort Kanal des Microsoft lync Server-Teams)</span><span class="sxs-lookup"><span data-stu-id="7f527-134">Routing information (including information on the NextHop blog at <a href="https://go.microsoft.com/fwlink/p/?linkid=203149">https://go.microsoft.com/fwlink/p/?LinkId=203149</a>, Microsoft Lync Server team’s customer response channel)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-135"><a href="lync-server-2013-deploying-external-user-access.md">Bereitstellen des Zugriffs durch externe Benutzer in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-135"><a href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f527-136">Bereitstellungsstrategie</span><span class="sxs-lookup"><span data-stu-id="7f527-136">Deployment strategy</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-137">Bereitstellungssequenz</span><span class="sxs-lookup"><span data-stu-id="7f527-137">Deployment sequence</span></span></p></li>
<li><p><span data-ttu-id="7f527-138">Arbeitsgruppe oder Domäne</span><span class="sxs-lookup"><span data-stu-id="7f527-138">Workgroup or domain</span></span></p></li>
<li><p><span data-ttu-id="7f527-139">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="7f527-139">Security</span></span></p></li>
<li><p><span data-ttu-id="7f527-140">Überwachen und überwachen</span><span class="sxs-lookup"><span data-stu-id="7f527-140">Monitoring and auditing</span></span></p></li>
<li><p><span data-ttu-id="7f527-141">Hardware Überlegungen</span><span class="sxs-lookup"><span data-stu-id="7f527-141">Hardware considerations</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Bewährte Methoden für die Anrufsteuerung in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-142"><a href="lync-server-2013-best-practices-for-call-admission-control.md">Best practices for call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f527-143">Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="7f527-143">Deployment process</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f527-144">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7f527-144">Prerequisites</span></span></p></li>
<li><p><span data-ttu-id="7f527-145">Informationsanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f527-145">Information requirements</span></span></p></li>
<li><p><span data-ttu-id="7f527-146">Verfahren und Verfahren</span><span class="sxs-lookup"><span data-stu-id="7f527-146">Process and procedures</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="7f527-147"><a href="lync-server-2013-configure-call-admission-control.md">Konfigurieren der Anrufsteuerung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="7f527-147"><a href="lync-server-2013-configure-call-admission-control.md">Configure call admission control in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7f527-148">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f527-148">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

