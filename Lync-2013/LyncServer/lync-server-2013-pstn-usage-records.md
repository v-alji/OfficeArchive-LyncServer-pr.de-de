---
title: 'Lync Server 2013: PSTN-Verwendungsdatensätze'
description: 'Lync Server 2013: PSTN-Verwendungsdaten Sätze.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN usage records
ms:assetid: b5f624aa-abe8-455b-a8e3-c228be230463
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412878(v=OCS.15)
ms:contentKeyID: 48185188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f8ff428dc2fa5cf8cf0f10e37f0f79c38d70d70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394578"
---
# <a name="pstn-usage-records-in-lync-server-2013"></a><span data-ttu-id="a3565-103">PSTN-Verwendungsdatensätze in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3565-103">PSTN usage records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3565-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3565-104">

<span> </span></span></span>

<span data-ttu-id="a3565-105">_**Letztes Änderungsdatum des Themas:** 2012-09-23_</span><span class="sxs-lookup"><span data-stu-id="a3565-105">_**Topic Last Modified:** 2012-09-23_</span></span>

<span data-ttu-id="a3565-106">Die Planung von PSTN-Nutzungsdaten Sätzen besteht hauptsächlich darin, alle Anrufberechtigungen aufzulisten, die derzeit in Ihrer Organisation gelten, vom CEO bis hin zu Leiharbeitern, Beratern und Kontingenten Mitarbeitern.</span><span class="sxs-lookup"><span data-stu-id="a3565-106">Planning PSTN usage records consists mainly of listing all the call permissions that are currently in force in your organization, from the CEO to temporary workers, consultants, and contingent staff.</span></span> <span data-ttu-id="a3565-107">Dieser Prozess bietet auch die Möglichkeit, vorhandene Anrufberechtigungen erneut zu überprüfen und zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3565-107">This process also provides an opportunity to reexamine existing call permissions and revise them.</span></span> <span data-ttu-id="a3565-108">Sie können PSTN-Verwendungsdaten Sätze nur für diese Anrufberechtigungen erstellen, die für Ihre erwarteten Enterprise-VoIP-Benutzer gelten, doch eine bessere Lösung mit langer Reichweite könnte darin liegen, PSTN-Verwendungsdaten Sätze für alle Anrufberechtigungen zu erstellen, und zwar unabhängig davon, ob einige derzeit nicht für die Gruppe von Benutzern gelten, die für Enterprise-VoIP aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3565-108">You can create PSTN usage records only for those call permissions that apply to your anticipated Enterprise Voice users, but a better long-range solution might be to create PSTN usage records for all call permissions, regardless of whether some may not currently apply to the group of users to be enabled for Enterprise Voice.</span></span> <span data-ttu-id="a3565-109">Wenn sich die Anrufberechtigungen ändern oder neue Benutzer mit unterschiedlichen Anrufberechtigungen hinzugefügt werden, haben Sie bereits die erforderlichen PSTN-Nutzungsdatensätze erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3565-109">If call permissions change or new users with different call permissions are added, you will have already created the required PSTN usage records.</span></span>

<span data-ttu-id="a3565-110">Im Folgenden sehen Sie eine typische PSTN-Verwendungstabelle.</span><span class="sxs-lookup"><span data-stu-id="a3565-110">The following table shows a typical PSTN usage table.</span></span>

### <a name="pstn-usage-records"></a><span data-ttu-id="a3565-111">PSTN-Verwendungseinträge</span><span class="sxs-lookup"><span data-stu-id="a3565-111">PSTN Usage Records</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3565-112">Telefonattribut</span><span class="sxs-lookup"><span data-stu-id="a3565-112">Phone attribute</span></span></th>
<th><span data-ttu-id="a3565-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3565-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3565-114">Local</span><span class="sxs-lookup"><span data-stu-id="a3565-114">Local</span></span></p></td>
<td><p><span data-ttu-id="a3565-115">Ortsgespräche</span><span class="sxs-lookup"><span data-stu-id="a3565-115">Local calls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3565-116">Long-Distance</span><span class="sxs-lookup"><span data-stu-id="a3565-116">Long-Distance</span></span></p></td>
<td><p><span data-ttu-id="a3565-117">Ferngespräche</span><span class="sxs-lookup"><span data-stu-id="a3565-117">Long distance calls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3565-118">International</span><span class="sxs-lookup"><span data-stu-id="a3565-118">International</span></span></p></td>
<td><p><span data-ttu-id="a3565-119">Auslandsgespräche</span><span class="sxs-lookup"><span data-stu-id="a3565-119">International calls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3565-120">Delhi</span><span class="sxs-lookup"><span data-stu-id="a3565-120">Delhi</span></span></p></td>
<td><p><span data-ttu-id="a3565-121">Vollzeitmitarbeiter in Delhi</span><span class="sxs-lookup"><span data-stu-id="a3565-121">Delhi full-time employees</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3565-122">Redmond</span><span class="sxs-lookup"><span data-stu-id="a3565-122">Redmond</span></span></p></td>
<td><p><span data-ttu-id="a3565-123">Vollzeitmitarbeiter in Redmond</span><span class="sxs-lookup"><span data-stu-id="a3565-123">Redmond full-time employees</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3565-124">RedmondTemps</span><span class="sxs-lookup"><span data-stu-id="a3565-124">RedmondTemps</span></span></p></td>
<td><p><span data-ttu-id="a3565-125">Zeitarbeiter in Redmond</span><span class="sxs-lookup"><span data-stu-id="a3565-125">Redmond temporary employees</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3565-126">Zurich</span><span class="sxs-lookup"><span data-stu-id="a3565-126">Zurich</span></span></p></td>
<td><p><span data-ttu-id="a3565-127">Vollzeitmitarbeiter in Zürich</span><span class="sxs-lookup"><span data-stu-id="a3565-127">Zurich full-time employees</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3565-p102">PSTN-Verwendungseinträge alleine führen keine Aktionen aus. Um sie verwenden zu können, müssen Sie sie mit Folgendem verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="a3565-p102">By themselves, PSTN usage records do not do anything. For them to work, you must associate them with the following:</span></span>

  - <span data-ttu-id="a3565-130">VoIP-Richtlinien, die Benutzern zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a3565-130">Voice policies, which are assigned to users.</span></span>

  - <span data-ttu-id="a3565-131">Routen, die Rufnummern zugewiesen sind</span><span class="sxs-lookup"><span data-stu-id="a3565-131">Routes, which are assigned to phone numbers.</span></span>

<span data-ttu-id="a3565-132">Details zu VoIP-Richtlinien und-Routen finden Sie unter [VoIP-Richtlinien in lync Server 2013](lync-server-2013-voice-policies.md) und [VoIP-Routen in lync Server 2013](lync-server-2013-voice-routes.md).</span><span class="sxs-lookup"><span data-stu-id="a3565-132">For details about voice policies and routes, see [Voice policies in Lync Server 2013](lync-server-2013-voice-policies.md) and [Voice routes in Lync Server 2013](lync-server-2013-voice-routes.md).</span></span> <span data-ttu-id="a3565-133">Ausführliche Informationen zum Erstellen und Konfigurieren von [VoIP-Routen für ausgehende Anrufe finden Sie in lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="a3565-133">For details about how to create and configure them, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>

<span data-ttu-id="a3565-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3565-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

