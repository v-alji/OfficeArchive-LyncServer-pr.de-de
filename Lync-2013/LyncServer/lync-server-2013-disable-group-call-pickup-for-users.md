---
title: 'Lync Server 2013: Deaktivieren der Gruppenanruf Abholung für Benutzer'
description: 'Lync Server 2013: Deaktivieren Sie die Gruppenanruf Abholung für Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3f5b4542cf7bb8ea5be524d2695701979ec2987
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429105"
---
# <a name="disable-group-call-pickup-for-users-in-lync-server-2013"></a><span data-ttu-id="d1e8a-103">Deaktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e8a-103">Disable Group Call Pickup for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1e8a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1e8a-104">

<span> </span></span></span>

<span data-ttu-id="d1e8a-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="d1e8a-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="d1e8a-106">Gehen Sie wie folgt vor, um die Gruppenanruf Abholung für einen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-106">Use the following procedure to disable Group Call Pickup for a user.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d1e8a-107">Wenn Sie die Gruppenanruf Abholung für einen Benutzer deaktivieren, wird die dem Benutzer zugewiesene Anrufgruppen Nummer nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-107">When you disable Group Call Pickup for a user, the call pickup group number that was assigned to the user is not retained.</span></span> <span data-ttu-id="d1e8a-108">Wenn Sie anschließend die Gruppenanruf Abholung für diesen Benutzer wieder aktivieren möchten, müssen Sie die Nummer für die Anruf-Abhol Gruppe mit dem/enablegrouppickup-Parameter erneut zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-108">If you subsequently want to re-enable Group Call Pickup for that user, you must assign the call pickup group number again with the /enablegrouppickup parameter.</span></span>



</div>

<div>

## <a name="to-disable-group-call-pickup-for-a-user"></a><span data-ttu-id="d1e8a-109">So deaktivieren Sie die Gruppenanruf Abholung für einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="d1e8a-109">To disable Group Call Pickup for a user</span></span>

1.  <span data-ttu-id="d1e8a-110">Melden Sie sich mit Administratorrechten an dem Computer an, auf dem Sie das SEFAUtil-Tool installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d1e8a-110">Log on to the computer where you installed the SEFAUtil tool with administrator rights.</span></span>

2.  <span data-ttu-id="d1e8a-111">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d1e8a-111">At the command line, run:</span></span>
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    <span data-ttu-id="d1e8a-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d1e8a-112">For example:</span></span>
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1e8a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1e8a-113">See Also</span></span>


[<span data-ttu-id="d1e8a-114">Zuweisen von Gruppenanruf-Abhol Nummern zu Benutzern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e8a-114">Assign Group Call Pickup numbers to users in Lync Server 2013</span></span>](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[<span data-ttu-id="d1e8a-115">Aktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e8a-115">Enable Group Call Pickup for users in Lync Server 2013</span></span>](lync-server-2013-enable-group-call-pickup-for-users.md)  
  

<span data-ttu-id="d1e8a-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1e8a-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

