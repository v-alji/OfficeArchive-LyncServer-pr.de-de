---
title: 'Lync Server 2013: Übersetzungsregeln'
description: 'Lync Server 2013: Übersetzungsregeln.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Translation rules
ms:assetid: 6e067bd4-4931-4385-81ac-2acae45a16d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398520(v=OCS.15)
ms:contentKeyID: 48184460
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65ee21459123ea09f54eb52e65a4d9ecba61c386
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393775"
---
# <a name="translation-rules-in-lync-server-2013"></a><span data-ttu-id="0bbf6-103">Übersetzungsregeln in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0bbf6-103">Translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0bbf6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0bbf6-104">

<span> </span></span></span>

<span data-ttu-id="0bbf6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="0bbf6-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="0bbf6-106">Für lync Server 2013 Enterprise-VoIP müssen alle Wählzeichenfolgen im E. 164-Format normalisiert werden, um RNL (Reverse Number Lookup) durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-106">Lync Server 2013 Enterprise Voice requires that all dial strings be normalized to E.164 format for the purpose of performing reverse number lookup (RNL).</span></span> <span data-ttu-id="0bbf6-107">In Microsoft lync Server 2010 werden Übersetzungsregeln nur für benannte Nummern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-107">In Microsoft Lync Server 2010, translation rules are supported only for called numbers.</span></span> <span data-ttu-id="0bbf6-108">Neu in Microsoft lync Server 2013 werden Übersetzungsregeln auch für Rufnummern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-108">New in Microsoft Lync Server 2013, translation rules are also supported for calling numbers.</span></span> <span data-ttu-id="0bbf6-109">Der *Trunkpeer* (also das zugeordnete Gateway, die Nebenstellenanlage (Private Branch Exchange (PBX) oder der zugeordnete SIP-Trunk) erfordert möglicherweise, dass die Nummern in einem lokalen Wählformat vorliegen.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-109">The *trunk peer* (that is, the associated gateway, private branch exchange (PBX), or SIP trunk) may require that numbers be in a local dialing format.</span></span> <span data-ttu-id="0bbf6-110">Um Nummern aus dem E.164-Format in ein lokales Wählformat zu übersetzen, können Sie eine oder mehrere Übersetzungsregeln definieren, mit denen der Anforderungs-URI vor dem Routen an den Trunkpeer geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-110">To translate numbers from E.164 format to a local dialing format, you can define one or more translation rules to manipulate the request URI before you route it to the trunk peer.</span></span> <span data-ttu-id="0bbf6-111">Sie können beispielsweise eine Übersetzungsregel erstellen, mit der die Vorwahl +44 aus einer Wählzeichenfolge entfernt und durch 0144 ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-111">For example, you could write a translation rule to remove +44 from the beginning of a dial string and replace it with 0144.</span></span>

<span data-ttu-id="0bbf6-112">Durch die ausgehende Routenübersetzung auf dem Server können Sie die Konfigurationsanforderungen der einzelnen Trunkpeers für das Übersetzen von Rufnummern in ein lokales Wählformat reduzieren.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-112">By performing outbound route translation on the server, you can reduce the configuration requirements on each individual trunk peer in order to translate phone numbers into a local dialing format.</span></span> <span data-ttu-id="0bbf6-113">Wenn Sie planen, welche Gateways und wie viele Gateways einem bestimmten Vermittlungs Server Cluster zugeordnet werden sollen, kann es hilfreich sein, trunk-Peers mit ähnlichen lokalen wählanforderungen zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-113">When you plan which gateways, and how many gateways, to associate with a specific Mediation Server cluster, it may be useful to group trunk peers with similar local dialing requirements.</span></span> <span data-ttu-id="0bbf6-114">Dies kann die Anzahl von erforderlichen Übersetzungsregeln und den Zeitaufwand für das Schreiben dieser Regeln reduzieren.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-114">This can reduce the number of required translation rules and the time it takes to write them.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0bbf6-115">Das Zuordnen einer oder mehrerer Übersetzungsregeln zu einer Enterprise Voice trunk-Konfiguration sollte als Alternative zum Konfigurieren von Übersetzungsregeln für den trunk-Peer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-115">Associating one or more translation rules with an Enterprise Voice trunk configuration should be used as an alternative to configuring translation rules on the trunk peer.</span></span> <span data-ttu-id="0bbf6-116">Ordnen Sie Übersetzungsregeln keiner Enterprise-VoIP-trunk-Konfiguration zu, wenn Sie Übersetzungsregeln für den trunk-Peer konfiguriert haben, da die beiden Regeln möglicherweise in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-116">Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer, because the two rules might conflict.</span></span>



</div>

<div>

## <a name="example-translation-rules"></a><span data-ttu-id="0bbf6-117">Beispielübersetzungsregeln</span><span class="sxs-lookup"><span data-stu-id="0bbf6-117">Example Translation Rules</span></span>

<span data-ttu-id="0bbf6-118">Die folgenden Beispiele für Übersetzungsregeln zeigen, wie Sie Regeln auf dem Server erstellen können, um Nummern aus dem E.164-Format in ein lokales Format für den Trunkpeer zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-118">The following examples of translation rules show how you can develop rules on the server to translate numbers from E.164 format to a local format for the trunk peer.</span></span>

<span data-ttu-id="0bbf6-119">Ausführliche Informationen zum Implementieren von Übersetzungsregeln finden Sie unter [Definieren von Übersetzungsregeln in lync Server 2013](lync-server-2013-defining-translation-rules.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="0bbf6-119">For details about how to implement translation rules, see [Defining translation rules in Lync Server 2013](lync-server-2013-defining-translation-rules.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0bbf6-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bbf6-120">Description</span></span></th>
<th><span data-ttu-id="0bbf6-121">Anfangsziffern</span><span class="sxs-lookup"><span data-stu-id="0bbf6-121">Starting Digits</span></span></th>
<th><span data-ttu-id="0bbf6-122">Länge</span><span class="sxs-lookup"><span data-stu-id="0bbf6-122">Length</span></span></th>
<th><span data-ttu-id="0bbf6-123">Zu entfernende Ziffern</span><span class="sxs-lookup"><span data-stu-id="0bbf6-123">Digits to Remove</span></span></th>
<th><span data-ttu-id="0bbf6-124">Hinzuzufügende Ziffern</span><span class="sxs-lookup"><span data-stu-id="0bbf6-124">Digits to Add</span></span></th>
<th><span data-ttu-id="0bbf6-125">Vergleichsmuster</span><span class="sxs-lookup"><span data-stu-id="0bbf6-125">Matching Pattern</span></span></th>
<th><span data-ttu-id="0bbf6-126">Übersetzung</span><span class="sxs-lookup"><span data-stu-id="0bbf6-126">Translation</span></span></th>
<th><span data-ttu-id="0bbf6-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0bbf6-127">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bbf6-128">Normales Ferngespräch in den USA</span><span class="sxs-lookup"><span data-stu-id="0bbf6-128">Conventional long-distance dialing in U.S.</span></span></p>
<p><span data-ttu-id="0bbf6-129">(Entfernen des Pluszeichens „+“)</span><span class="sxs-lookup"><span data-stu-id="0bbf6-129">(strip out the ‘+’)</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-130">+1</span><span class="sxs-lookup"><span data-stu-id="0bbf6-130">+1</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-131">Exakt 12</span><span class="sxs-lookup"><span data-stu-id="0bbf6-131">Exactly 12</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-132">1</span><span class="sxs-lookup"><span data-stu-id="0bbf6-132">1</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-133">0</span><span class="sxs-lookup"><span data-stu-id="0bbf6-133">0</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-134">^\+(1 \ d {10} ) $</span><span class="sxs-lookup"><span data-stu-id="0bbf6-134">^\+(1\d{10})$</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-135">$1</span><span class="sxs-lookup"><span data-stu-id="0bbf6-135">$1</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-136">+14255551010 wird zu 14255551010</span><span class="sxs-lookup"><span data-stu-id="0bbf6-136">+14255551010 becomes 14255551010</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bbf6-137">Internationales Ferngespräch aus den USA</span><span class="sxs-lookup"><span data-stu-id="0bbf6-137">U.S. international long-distance dialing</span></span></p>
<p><span data-ttu-id="0bbf6-138">(Entfernen des Pluszeichens „+“ und Hinzufügen von 011)</span><span class="sxs-lookup"><span data-stu-id="0bbf6-138">(strip out ‘+’ and add 011)</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="0bbf6-139">Mindestens 11</span><span class="sxs-lookup"><span data-stu-id="0bbf6-139">At least 11</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-140">1</span><span class="sxs-lookup"><span data-stu-id="0bbf6-140">1</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-141">011</span><span class="sxs-lookup"><span data-stu-id="0bbf6-141">011</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-142">^\+(\d {9} \d +) $</span><span class="sxs-lookup"><span data-stu-id="0bbf6-142">^\+(\d{9}\d+)$</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-143">011$1</span><span class="sxs-lookup"><span data-stu-id="0bbf6-143">011$1</span></span></p></td>
<td><p><span data-ttu-id="0bbf6-144">+441235551010 wird zu 011441235551010</span><span class="sxs-lookup"><span data-stu-id="0bbf6-144">+441235551010 becomes 011441235551010</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0bbf6-145">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0bbf6-145">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

