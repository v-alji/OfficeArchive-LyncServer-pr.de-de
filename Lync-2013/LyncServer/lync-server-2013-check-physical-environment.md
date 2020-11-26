---
title: 'Lync Server 2013: Überprüfen der physikalischen Umgebung'
description: 'Lync Server 2013: Überprüfen der physikalischen Umgebung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Performing physical environmental checks
ms:assetid: 153aee5e-3adf-4dbf-bf41-53e4fba51fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720558(v=OCS.15)
ms:contentKeyID: 63969582
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d963485b109e0afdf21b3a9085fa28884dfc3100
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434998"
---
# <a name="performing-physical-environmental-checks"></a><span data-ttu-id="cb74b-103">Durchführen physischer Umgebungsüberprüfungen</span><span class="sxs-lookup"><span data-stu-id="cb74b-103">Performing physical environmental checks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb74b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb74b-104">

<span> </span></span></span>

<span data-ttu-id="cb74b-105">_**Letztes Änderungsdatum des Themas:** 2014-04-30_</span><span class="sxs-lookup"><span data-stu-id="cb74b-105">_**Topic Last Modified:** 2014-04-30_</span></span>

<span data-ttu-id="cb74b-106">Bevor Sie die Leistung, Verfügbarkeit und Funktionalität der lync Server 2013-Bereitstellung überprüfen, sollten Sie die physikalische Umgebung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cb74b-106">Before checking the performance, availability, and functionality of the Lync Server 2013 deployment, you should check the physical environment.</span></span> <span data-ttu-id="cb74b-107">Beispielsweise muss die Temperatur des Serverraums gesenkt werden, oder es muss ein Netzwerkkabel ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cb74b-107">For example, the server room temperature might have to be lowered, or a network cable might have to be replaced.</span></span> <span data-ttu-id="cb74b-108">Um optimale Ergebnisse zu erzielen, führen Sie die folgenden physikalischen Umweltinspektionen durch:</span><span class="sxs-lookup"><span data-stu-id="cb74b-108">For best results, perform the following physical environmental inspections:</span></span>

  - <span data-ttu-id="cb74b-109">**Physikalische Sicherheitsmaßnahmen**   Physischer Sicherheitsschutz wie Sperren, Türen und eingeschränkte Zugriffs Räume müssen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="cb74b-109">**Physical security measures**   Physical security protection such as locks, doors, and restricted-access rooms must be secured.</span></span> <span data-ttu-id="cb74b-110">Überprüfen Sie, ob unbefugte und erzwungene Einträge und Anzeichen von Geräteschäden auftreten.</span><span class="sxs-lookup"><span data-stu-id="cb74b-110">Check for any unauthorized and forced entries and signs of equipment damage.</span></span>

  - <span data-ttu-id="cb74b-111">**Temperatur und Luftfeuchtigkeit**   Hohe Temperaturen, schlechte Luftzirkulation und Feuchtigkeit können dazu führen, dass Hardwarekomponenten überhitzt werden.</span><span class="sxs-lookup"><span data-stu-id="cb74b-111">**Temperature and humidity**   High temperature, poor air flow, and humidity can cause hardware components to overheat.</span></span> <span data-ttu-id="cb74b-112">Überprüfen Sie Temperatur und Luftfeuchtigkeit, um sicherzustellen, dass die Umweltsysteme wie Heizung und Klimatisierung akzeptable Bedingungen und Funktionen in den Spezifikationen des Hardwareherstellers aufrecht erhalten können.</span><span class="sxs-lookup"><span data-stu-id="cb74b-112">Check temperature and humidity to help to make sure that the environmental systems such as heating and air conditioning can maintain acceptable conditions and function within the hardware manufacturer's specifications.</span></span> <span data-ttu-id="cb74b-113">Wenn neue Geräte vor kurzem installiert wurden, prüfen Sie auch, ob der Luftstrom sowohl von als auch von den Servern ungehindert ist und die Herstellerspezifikation erfüllt.</span><span class="sxs-lookup"><span data-stu-id="cb74b-113">When new equipment has recently been installed, also check that air flow both to and from the servers is unimpeded and meets manufacturer spec.</span></span>

  - <span data-ttu-id="cb74b-114">**Geräte und Komponenten**   Die lync Server 2013-Organisation basiert auf einem funktionierenden physikalischen Netzwerk und der zugehörigen Hardware.</span><span class="sxs-lookup"><span data-stu-id="cb74b-114">**Devices and components**   The Lync Server 2013 organization relies on a functioning physical network and related hardware.</span></span> <span data-ttu-id="cb74b-115">Stellen Sie sicher, dass Router, Switches, Hubs, physikalische Kabel und Verbinder funktionsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="cb74b-115">Make sure that routers, switches, hubs, physical cables, and connectors are operational.</span></span>

<span data-ttu-id="cb74b-116">Die Einzelheiten zur Durchführung dieser Prüfungen hängen stark von Ihrer Installations Website und der ausgewählten Server Hardware ab.</span><span class="sxs-lookup"><span data-stu-id="cb74b-116">The specifics on how to perform these checks will depend greatly on your installation site and the server hardware that was chosen.</span></span> <span data-ttu-id="cb74b-117">Wenn Sie diese Prüfung zum ersten Mal durchführen, lesen Sie die Hardwaredokumentation, und notieren Sie sich die gewünschten Parameter für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="cb74b-117">The first time that you perform this check, refer to the hardware documentation and note the desired parameters for future reference.</span></span>

### <a name="desired-server-space-environment"></a><span data-ttu-id="cb74b-118">Gewünschte Serverraum Umgebung</span><span class="sxs-lookup"><span data-stu-id="cb74b-118">Desired server space environment</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb74b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb74b-119">Parameter</span></span></th>
<th><span data-ttu-id="cb74b-120">Gewünschter Wert oder Bereich</span><span class="sxs-lookup"><span data-stu-id="cb74b-120">Desired value or range</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb74b-121">Temperatur</span><span class="sxs-lookup"><span data-stu-id="cb74b-121">Temperature</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb74b-122">Feuchtigkeit</span><span class="sxs-lookup"><span data-stu-id="cb74b-122">Humidity</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb74b-123">Front of Server Faces</span><span class="sxs-lookup"><span data-stu-id="cb74b-123">Front of server faces</span></span></p></td>
<td><p><span data-ttu-id="cb74b-124">Hot-Aisle/Cold-Aisle</span><span class="sxs-lookup"><span data-stu-id="cb74b-124">Hot aisle / cold aisle</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb74b-125">Ungehinderte Abgas Freigabe</span><span class="sxs-lookup"><span data-stu-id="cb74b-125">Unimpeded exhaust clearance</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="cb74b-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb74b-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

