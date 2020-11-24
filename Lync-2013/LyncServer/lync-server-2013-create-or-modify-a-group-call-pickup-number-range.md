---
title: 'Lync Server 2013: Erstellen oder Ändern eines Gruppenanruf-Abhol Nummernbereichs'
description: 'Lync Server 2013: Erstellen oder Ändern eines Gruppenanruf-Pickup-Nummernbereichs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a Group Call Pickup number range
ms:assetid: 4b442b98-df6b-4e50-8254-b3be9cde21dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945627(v=OCS.15)
ms:contentKeyID: 51541472
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc2072a5d80e9c3b09e0c0d2275233214a21e764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394367"
---
# <a name="create-or-modify-a-group-call-pickup-number-range-in-lync-server-2013"></a><span data-ttu-id="3dbf2-103">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3dbf2-103">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3dbf2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3dbf2-104">

<span> </span></span></span>

<span data-ttu-id="3dbf2-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="3dbf2-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="3dbf2-106">Verwenden Sie das folgende Verfahren, um einen Nummernbereich für die Anrufannahmegruppe in der Orbittabelle für das Parken von Anrufen zu erstellen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-106">Use the following procedure to create or modify a call pickup group number range in the call park orbit table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3dbf2-107">Sie müssen die lync Server-Verwaltungsshell zum Erstellen, ändern, entfernen und Anzeigen von Gruppenanruf-Pickup-Nummernbereichen in der Orbit-Tabelle des Anruf Parks verwenden.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-107">You must use Lync Server Management Shell to create, modify, remove, and view Group Call Pickup number ranges in the call park orbit table.</span></span> <span data-ttu-id="3dbf2-108">Gruppenanruf-Abhol Nummernbereiche sind in der lync Server-Systemsteuerung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-108">Group Call Pickup number ranges are not available in Lync Server Control Panel.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3dbf2-109">Dem Nummernbereich für die Anruf Abholung muss ein GroupPickup-Typ zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-109">The call pickup group number range must be assigned a type of GroupPickup.</span></span> <span data-ttu-id="3dbf2-110">Benutzer sind für die Gruppenanruf Abholung nur aktiviert, wenn die Ihnen zugewiesene Gruppennummer Typ GroupPickup ist.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-110">Users are enabled for Group Call Pickup only if the group number that they are assigned is type GroupPickup.</span></span>



</div>

<span data-ttu-id="3dbf2-111">Die Nummernbereiche für die Anrufannahmegruppe müssen folgenden Regeln entsprechen:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-111">The call pickup group number ranges must comply with the following rules:</span></span>

  - <span data-ttu-id="3dbf2-112">Die Startnummer für den Bereich muss kleiner oder gleich der Endnummer sein.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-112">The beginning number of the range must be less than or equal to the ending number of the range.</span></span>

  - <span data-ttu-id="3dbf2-113">Der Wert der Startnummer des Bereichs muss dieselbe Länge aufweisen wie der Wert der Endnummer des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-113">The value of the beginning number of the range must be the same length as the ending number of the range.</span></span>

  - <span data-ttu-id="3dbf2-p103">Der Nummernbereich muss eindeutig sein. Für diesen Bereich sind keine Überschneidungen mit einem anderen Bereich zulässig.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-p103">The number range must be unique. This range cannot overlap with any other range.</span></span>

  - <span data-ttu-id="3dbf2-116">Wenn der Zahlenbereich mit dem Zeichen beginnt \* \# , muss der Bereich größer als 100 sein.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-116">If the number range begins with the character \* or \#, the range must be greater than 100.</span></span>

  - <span data-ttu-id="3dbf2-117">Gültige Werte: muss mit der Zeichenfolge des regulären Ausdrucks übereinstimmen ( \[ \\ \* | \# \] ? \[ 1-9 \] \\ d {0,7} ) | ( \[ 1-9 \] \\ d {0,8} ).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-117">Valid values: Must match the regular expression string (\[\\\*|\#\]?\[1-9\]\\d{0,7})|(\[1-9\]\\d{0,8}).</span></span> <span data-ttu-id="3dbf2-118">Dies bedeutet, dass der Wert eine Zeichenfolge sein muss, die entweder mit dem Zeichen \* oder \# einer Zahl von 1 bis 9 beginnt (das erste Zeichen darf keine NULL sein).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-118">This means the value must be a string beginning with either the character \* or \# or a number 1 through 9 (the first character cannot be a zero).</span></span> <span data-ttu-id="3dbf2-119">Wenn das erste Zeichen \* oder ist \# , muss das folgende Zeichen eine Zahl von 1 bis 9 sein (es darf keine NULL sein).</span><span class="sxs-lookup"><span data-stu-id="3dbf2-119">If the first character is \* or \#, the following character must be a number 1 through 9 (it cannot be a zero).</span></span> <span data-ttu-id="3dbf2-120">Nachfolgende Zeichen können eine beliebige Zahl von 0 bis 9 bis zu sieben zusätzlichen Zeichen sein (beispielsweise " \# 6000", " \* 92000", " \* 95551212" und "915551212").</span><span class="sxs-lookup"><span data-stu-id="3dbf2-120">Subsequent characters can be any number 0 through 9 up to seven additional characters (for example, "\#6000", "\*92000", "\*95551212", and "915551212").</span></span> <span data-ttu-id="3dbf2-121">Wenn das erste Zeichen nicht \* oder ist \# , muss das erste Zeichen eine Zahl von 1 bis 9 sein (es darf nicht NULL sein), gefolgt von bis zu acht Zeichen, jeweils eine Zahl von 0 bis 9 (beispielsweise "915551212"; "41212"; "300").</span><span class="sxs-lookup"><span data-stu-id="3dbf2-121">If the first character is not \* or \#, the first character must be a number 1 through 9 (it cannot be zero), followed by up to eight characters, each a number 0 through 9 (for example, "915551212", "41212", "300").</span></span>

<div>

## <a name="to-create-or-modify-a-call-pickup-group-range"></a><span data-ttu-id="3dbf2-122">So erstellen oder ändern Sie einen Bereich für die Anrufannahmegruppe</span><span class="sxs-lookup"><span data-stu-id="3dbf2-122">To create or modify a call pickup group range</span></span>

1.  <span data-ttu-id="3dbf2-123">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-123">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="3dbf2-124">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-124">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3dbf2-125">Mit **New-CsCallParkOrbit** erstellen Sie einen neuen Nummernbereich für die Anrufannahmegruppe.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-125">Use **New-CsCallParkOrbit** to create a new range of call pickup group numbers.</span></span> <span data-ttu-id="3dbf2-126">Mit **Set-CsCallParkOrbit** ändern Sie einen vorhandenen Nummernbereich für die Anrufannahmegruppe.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-126">Use **Set-CsCallParkOrbit** to modify an existing range of call pickup numbers.</span></span>
    
    <span data-ttu-id="3dbf2-127">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-127">At the command line, run:</span></span>
    
        New-CsCallParkOrbit -Identity <name of call pickup group range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range> -CallParkService <FQDN or service ID of the Application service that hosts the Call Park application> -Type GroupPickup
    
    <span data-ttu-id="3dbf2-128">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3dbf2-128">For example:</span></span>
    
        New-CsCallParkOrbit -Identity "Redmond call pickup" -NumberRangeStart 100 -NumberRangeEnd 199 -CallParkService redmond-applicationserver-1 -Type GroupPickup
    
    <span data-ttu-id="3dbf2-129">Das folgende Beispiel zeigt, wie ein Nummernbereich von Orbits für das Parken von Anrufen zu Anrufannahmegruppen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-129">The following example shows how to change a range of numbers from call park orbits to call pickup groups.</span></span>
    
        Set-CsCallParkOrbit -Identity "Redmond call pickup" -Type GroupPickup
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="3dbf2-130">Verwenden Sie dieses Cmdlet zum Ändern der zugewiesenen Nummernbereiche nur dann, wenn Sie ursprünglich einen falschen Typ angegeben haben und der Gruppenbereich noch nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-130">Use this cmdlet to change the type assigned to number ranges only if you initially specified the incorrect type and the group range is not yet in use.</span></span> <span data-ttu-id="3dbf2-131">Wenn der Nummernbereich bereits verwendet wird und Sie den Typ von „CallPark“ zu „GroupPickup“ oder umgekehrt ändern, funktioniert entweder das Parken von Anrufen oder die Gruppenanrufannahme für diesen Nummernbereich nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-131">If you change the number range from CallPark to GroupPickup or vice versa and the number range is already in use, either Call Park or Group Call Pickup will stop working for that number range.</span></span> <span data-ttu-id="3dbf2-132">Wenn Sie beispielsweise einen Zahlenbereich von CallPark in GroupPick ändern, kann die Anwendung für den Anruf Park diesen Bereich von Umlaufbahnen nicht mehr zum Parken von Anrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3dbf2-132">For example, if you change a number range from CallPark to GroupPick, the Call Park application can no longer use that range of orbits to park calls.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3dbf2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dbf2-133">See Also</span></span>


[<span data-ttu-id="3dbf2-134">Löschen eines Umlauf Bereichs für einen Anruf Park in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3dbf2-134">Delete a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-delete-a-call-park-orbit-range.md)  


[<span data-ttu-id="3dbf2-135">Neu – CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="3dbf2-135">New-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsCallParkOrbit)  
[<span data-ttu-id="3dbf2-136">Satz-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="3dbf2-136">Set-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsCallParkOrbit)  
  

<span data-ttu-id="3dbf2-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3dbf2-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

