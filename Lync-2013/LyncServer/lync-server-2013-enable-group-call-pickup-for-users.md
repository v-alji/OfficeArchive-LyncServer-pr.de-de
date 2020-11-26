---
title: 'Lync Server 2013: Aktivieren der Gruppenanruf Abholung für Benutzer'
description: 'Lync Server 2013: Aktivieren der Gruppenanruf Abholung für Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable Group Call Pickup for users
ms:assetid: 20ec5f41-6ba2-4156-82ed-b91d05b62a6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945620(v=OCS.15)
ms:contentKeyID: 51541457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 27951e9000fd17aac90339cf2a507757ae96a397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437595"
---
# <a name="enable-group-call-pickup-for-users-in-lync-server-2013"></a><span data-ttu-id="4855c-103">Aktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4855c-103">Enable Group Call Pickup for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4855c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4855c-104">

<span> </span></span></span>

<span data-ttu-id="4855c-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="4855c-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="4855c-106">Verwenden Sie das SEFAUtil Resource Kit-Tool, um die Gruppenanruf Abholung für Benutzer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4855c-106">Use the SEFAUtil resource kit tool to enable Group Call Pickup for users.</span></span> <span data-ttu-id="4855c-107">Benutzern muss eine Gruppennummer mit dem Typ GroupPickup in der Orbit-Tabelle des Anruf Parks zugewiesen werden, damit die Gruppenanruf Abholung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4855c-107">Users must be assigned a group number with type GroupPickup in the call park orbit table to have Group Call Pickup enabled.</span></span> <span data-ttu-id="4855c-108">Sie weisen eine Gruppennummer für die Anruf Abholung zu und aktivieren die Gruppenanruf Abholung gleichzeitig mithilfe des/enablegrouppickup-Parameters, wenn Sie SEFAUtil.exe ausführen.</span><span class="sxs-lookup"><span data-stu-id="4855c-108">You assign a call pickup group number and enable Group Call Pickup at the same time by using the /enablegrouppickup parameter when you run SEFAUtil.exe.</span></span>

<div>

## <a name="to-enable-group-call-pickup-for-a-user"></a><span data-ttu-id="4855c-109">So aktivieren Sie die Gruppenanruf Abholung für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="4855c-109">To enable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="4855c-110">Melden Sie sich mit Administratorrechten an dem Computer an, auf dem Sie das SEFAUtil-Tool installiert haben.</span><span class="sxs-lookup"><span data-stu-id="4855c-110">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="4855c-111">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="4855c-111">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /enablegrouppickup:<group number>
    
    <span data-ttu-id="4855c-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4855c-112">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /enablegrouppickup:199

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4855c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4855c-113">See Also</span></span>


[<span data-ttu-id="4855c-114">Zuweisen von Gruppenanruf-Abhol Nummern zu Benutzern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4855c-114">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[<span data-ttu-id="4855c-115">Deaktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4855c-115">Disable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-disable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="4855c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4855c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

