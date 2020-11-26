---
title: 'Lync Server 2013: Löschen eines Gruppenanruf-Abhol Nummernbereichs'
description: 'Lync Server 2013: Löschen eines Gruppenanruf-Pickup-Nummernbereichs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Group Call Pickup number range
ms:assetid: 521891f3-7a5d-45de-92dc-d57025453159
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945629(v=OCS.15)
ms:contentKeyID: 51541475
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b40d423b64d29300741c55433864128897c3ac8f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430707"
---
# <a name="delete-a-group-call-pickup-number-range-in-lync-server-2013"></a><span data-ttu-id="486e7-103">Löschen eines Gruppenanruf-Pickup-Nummernbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="486e7-103">Delete a Group Call Pickup number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="486e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="486e7-104">

<span> </span></span></span>

<span data-ttu-id="486e7-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="486e7-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="486e7-106">Gehen Sie wie folgt vor, um einen Gruppenanruf-Nummernbereich zu löschen.</span><span class="sxs-lookup"><span data-stu-id="486e7-106">Use the following procedure to delete a Group Call Pickup number range.</span></span>

<div>

## <a name="to-delete-a-call-pickup-group-number-range"></a><span data-ttu-id="486e7-107">So löschen Sie den Nummernbereich einer Anruf-Abhol Gruppe</span><span class="sxs-lookup"><span data-stu-id="486e7-107">To delete a call pickup group number range</span></span>

1.  <span data-ttu-id="486e7-108">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="486e7-108">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="486e7-109">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="486e7-109">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="486e7-110">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="486e7-110">At the command line, type:</span></span>
    
        Remove-CsCallParkOrbit -Identity "<group number range name>" 
    
    <span data-ttu-id="486e7-111">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="486e7-111">For example:</span></span>
    
        Remove-CsCallParkOrbit -Identity "Redmond call pickup"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="486e7-112">Ausführliche Informationen zu weiteren Optionen finden Sie unter <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="486e7-112">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="486e7-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="486e7-113">See Also</span></span>


[<span data-ttu-id="486e7-114">Erstellen oder Ändern eines orbitbereichs für einen Anruf Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="486e7-114">Create or modify a Call Park orbit range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)  


[<span data-ttu-id="486e7-115">Remove-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="486e7-115">Remove-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit)  
[<span data-ttu-id="486e7-116">Get-CsCallParkOrbit</span><span class="sxs-lookup"><span data-stu-id="486e7-116">Get-CsCallParkOrbit</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCallParkOrbit)  
  

<span data-ttu-id="486e7-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="486e7-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

