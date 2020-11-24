---
title: 'Lync Server 2013: Zuweisen von Anwesenheitsrichtlinien für einzelne Benutzer'
description: 'Lync Server 2013: Zuweisen von benutzerbezogenen Anwesenheitsrichtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user presence policies
ms:assetid: fd1097b7-248d-4b78-8c43-456b03257c18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182614(v=OCS.15)
ms:contentKeyID: 48185955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c3d4b4bda0c4bb85065d546fdbb4b2578db0e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395175"
---
# <a name="assigning-per-user-presence-policies-in-lync-server-2013"></a><span data-ttu-id="69965-103">Zuweisen von Anwesenheitsrichtlinien für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69965-103">Assigning per-user presence policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69965-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69965-104">

<span> </span></span></span>

<span data-ttu-id="69965-105">_**Letztes Änderungsdatum des Themas:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="69965-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="69965-106">Eine Anwesenheitsrichtlinie besteht aus einer Reihe von Grenzwerten und Einschränkungen, die sich auf die Anwesenheit auswirken.</span><span class="sxs-lookup"><span data-stu-id="69965-106">A presence policy is a set of limits and restrictions that affect presence.</span></span> <span data-ttu-id="69965-107">In der folgenden Tabelle werden die in lync Server 2013 verfügbaren Anwesenheitsrichtlinien Einstellungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69965-107">The following table describes the presence policy settings available in Lync Server 2013.</span></span>

### <a name="presence-policy-settings"></a><span data-ttu-id="69965-108">Einstellungen für Anwesenheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="69965-108">Presence Policy Settings</span></span>

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
<th><span data-ttu-id="69965-109">XML-Name</span><span class="sxs-lookup"><span data-stu-id="69965-109">XML name</span></span></th>
<th><span data-ttu-id="69965-110">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="69965-110">Display name</span></span></th>
<th><span data-ttu-id="69965-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69965-111">Description</span></span></th>
<th><span data-ttu-id="69965-112">Typ</span><span class="sxs-lookup"><span data-stu-id="69965-112">Type</span></span></th>
<th><span data-ttu-id="69965-113">Wert</span><span class="sxs-lookup"><span data-stu-id="69965-113">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69965-114">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="69965-114">CategorySubscriptions</span></span></p></td>
<td><p><span data-ttu-id="69965-115">Maximale Anzahl von Abonnenten Kategorie-Abonnements</span><span class="sxs-lookup"><span data-stu-id="69965-115">Maximum Number of Subscriber Category Subscriptions</span></span></p></td>
<td><p><span data-ttu-id="69965-116">Begrenzt die Anzahl der Abonnements für Abonnenten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="69965-116">Limits the number of subscriber category subscriptions.</span></span> <span data-ttu-id="69965-117">Wenn Communicator beispielsweise die Anwesenheit eines Benutzers abonniert, erhält er ein Kategorie-Abonnement für jede Visitenkarte, Kalenderdaten, Notizen, Dienste und Zustandskategorien.</span><span class="sxs-lookup"><span data-stu-id="69965-117">For example, when Communicator subscribes to a user’s presence, it obtains a category subscription for each of the contact card, calendar data, notes, services, and state categories.</span></span></p>
<p><span data-ttu-id="69965-118">Eine Einstellung von "0" bedeutet, dass der Benutzer oder das Kontaktobjekt nicht von anderen abonniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="69965-118">A setting of 0 means that the user or contact object cannot be subscribed to by others.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="69965-119">Diese Einstellung kann erhebliche Auswirkungen auf die Leistung haben, wenn Sie auf eine hohe Zahl festgelegt ist und der durchschnittliche Benutzer eine große Anzahl von Benutzern abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="69965-119">This setting can have a significant impact on performance if it is set to a high number, and the average user has a large number of users subscribing to his or her presence.</span></span>


</div></td>
<td><p><span data-ttu-id="69965-120">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="69965-120">Integer</span></span></p></td>
<td><p><span data-ttu-id="69965-121">0-3000</span><span class="sxs-lookup"><span data-stu-id="69965-121">0-3000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69965-122">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="69965-122">PromptedSubscribers</span></span></p></td>
<td><p><span data-ttu-id="69965-123">Maximale Anzahl von Benachrichtigungen für Anwesenheitsabonnements in der Warteschlange</span><span class="sxs-lookup"><span data-stu-id="69965-123">Maximum Number of Queued Presence Subscription Alerts</span></span></p></td>
<td><p><span data-ttu-id="69965-124">Schränkt die Anzahl von Einträgen in der Tabelle "angeforderte Abonnenten" ein.</span><span class="sxs-lookup"><span data-stu-id="69965-124">Limits the number of entries in the prompted subscribers table.</span></span> <span data-ttu-id="69965-125">Diese Einstellung bestimmt die maximale Anzahl von Eingabeaufforderungen, die für einen bestimmten Benutzer in die Warteschlange gestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="69965-125">This setting determines the maximum number of prompts that can be queued for a given user.</span></span> <span data-ttu-id="69965-126">Wenn Benutzer a beispielsweise die Anwesenheit von Benutzer b abonniert hat, erhält Benutzer b eine Aufforderung, dass Benutzer a jetzt Benutzer b abonniert hat, und in der Tabelle mit der Aufforderung "Abonnenten" von Benutzer b wird eine Bestätigungsaufforderung erstellt.</span><span class="sxs-lookup"><span data-stu-id="69965-126">For example, when user A subscribes to user B’s presence, user B receives a prompt that user A is now subscribed to user B, and an acknowledgement prompt is created in user B’s prompted subscribers table.</span></span> <span data-ttu-id="69965-127">Nachdem der Benutzer b das Abonnement akzeptiert oder bestätigt hat, wird die Bestätigungsaufforderung aus der Tabelle "angeforderte Abonnenten" von Benutzer b entfernt.</span><span class="sxs-lookup"><span data-stu-id="69965-127">After user B accepts, or acknowledges, the subscription, the acknowledgement prompt is removed from user B’s prompted subscribers table.</span></span></p>
<p><span data-ttu-id="69965-128">Eine Einstellung von "0" bedeutet, dass der Benutzer nicht dazu aufgefordert wird, wenn jemand seine Anwesenheit abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="69965-128">A setting of 0 means that the user is not prompted when someone subscribes to his or her presence.</span></span></p></td>
<td><p><span data-ttu-id="69965-129">Ganzzahl oder Token</span><span class="sxs-lookup"><span data-stu-id="69965-129">Integer or Token</span></span></p></td>
<td><p><span data-ttu-id="69965-130">0-500</span><span class="sxs-lookup"><span data-stu-id="69965-130">0-500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69965-131">Standardmäßig werden beim Bereitstellen von lync Server die Richtlinien **Standardrichtlinie** und **Dienst: Medium** -Anwesenheitsrichtlinien installiert.</span><span class="sxs-lookup"><span data-stu-id="69965-131">By default, the **Default Policy** and **Service: Medium** presence policies are installed when you deploy Lync Server.</span></span> <span data-ttu-id="69965-132">In der folgenden Tabelle werden die spezifischen Einstellungen der beiden Anwesenheitsrichtlinien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69965-132">The following table describes the specific settings of the two presence policies.</span></span>

### <a name="presence-policies"></a><span data-ttu-id="69965-133">Anwesenheitsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="69965-133">Presence Policies</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69965-134">Richtlinienname</span><span class="sxs-lookup"><span data-stu-id="69965-134">Policy name</span></span></th>
<th><span data-ttu-id="69965-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69965-135">Description</span></span></th>
<th><span data-ttu-id="69965-136">CategorySubscriptions</span><span class="sxs-lookup"><span data-stu-id="69965-136">CategorySubscriptions</span></span></th>
<th><span data-ttu-id="69965-137">PromptedSubscribers</span><span class="sxs-lookup"><span data-stu-id="69965-137">PromptedSubscribers</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69965-138">Standardrichtlinie</span><span class="sxs-lookup"><span data-stu-id="69965-138">Default Policy</span></span></p></td>
<td><p><span data-ttu-id="69965-139">Richtlinie für typische Benutzer.</span><span class="sxs-lookup"><span data-stu-id="69965-139">Policy for typical users.</span></span> <span data-ttu-id="69965-140">Dies ist die standardmäßige Anwesenheitsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="69965-140">This is the default presence policy.</span></span></p></td>
<td><p><span data-ttu-id="69965-141">1000</span><span class="sxs-lookup"><span data-stu-id="69965-141">1000</span></span></p></td>
<td><p><span data-ttu-id="69965-142">200</span><span class="sxs-lookup"><span data-stu-id="69965-142">200</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69965-143">Dienst: Mittel</span><span class="sxs-lookup"><span data-stu-id="69965-143">Service: Medium</span></span></p></td>
<td><p><span data-ttu-id="69965-144">Richtlinie für Anwendungen, die mehr Benutzer benötigen, um die Anwesenheit des Objekts zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="69965-144">Policy for applications that require more users to subscribe to the object’s presence.</span></span></p></td>
<td><p><span data-ttu-id="69965-145">1000</span><span class="sxs-lookup"><span data-stu-id="69965-145">1000</span></span></p></td>
<td><p><span data-ttu-id="69965-146">0</span><span class="sxs-lookup"><span data-stu-id="69965-146">0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="69965-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69965-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

