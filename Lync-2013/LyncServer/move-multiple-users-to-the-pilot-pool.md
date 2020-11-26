---
title: Verschieben mehrerer Benutzer in den Pilot Pool
description: Verschieben mehrerer Benutzer in den Pilot Pool
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move multiple users to the pilot pool
ms:assetid: 90d0590c-922c-4933-b778-9dd850b59310
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205096(v=OCS.15)
ms:contentKeyID: 48184838
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 121509fbad863b0ce2d6cc9c7e9afaef360e2eb6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438496"
---
# <a name="move-multiple-users-to-the-pilot-pool"></a><span data-ttu-id="2cfad-103">Verschieben mehrerer Benutzer in den Pilot Pool</span><span class="sxs-lookup"><span data-stu-id="2cfad-103">Move multiple users to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2cfad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2cfad-104">

<span> </span></span></span>

<span data-ttu-id="2cfad-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="2cfad-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="2cfad-106">Mithilfe der lync Server 2013-Systemsteuerung oder der lync Server 2013-Verwaltungsshell können Sie mehrere Benutzer aus Ihrem lync Server 2010-Pool in ihren lync Server 2013-Pilot Pool verschieben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-106">You can move multiple users from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="2cfad-107">So verschieben Sie mehrere Benutzer mithilfe der lync Server 2013-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="2cfad-107">To move multiple users by using the Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="2cfad-108">Öffnen Sie die **Lync Server-Systemsteuerung**.</span><span class="sxs-lookup"><span data-stu-id="2cfad-108">Open **Lync Server Control Panel**.</span></span>

2.  <span data-ttu-id="2cfad-109">Klicken Sie auf **Benutzer** und anschließend auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="2cfad-109">Click **Users**, click Search, and then click **Find**.</span></span>

3.  <span data-ttu-id="2cfad-110">Wählen Sie zwei Benutzer aus, die Sie in den lync Server 2013-Pool verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="2cfad-110">Select two users that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="2cfad-111">In diesem Beispiel werden die Benutzer Chen Yang und Claus Hansen verschoben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-111">In this example, we will move users Chen Yang and Claus Hansen.</span></span>
    
    <span data-ttu-id="2cfad-112">![Verschieben von Benutzern in einen bestimmten Registrierungspool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Verschieben von Benutzern in einen bestimmten Registrierungspool")</span><span class="sxs-lookup"><span data-stu-id="2cfad-112">![Move users to specific register pool](images/JJ205096.70d510e1-8e6b-40a5-a80b-27cbc63fc337(OCS.15).jpg "Move users to specific register pool")</span></span>  

4.  <span data-ttu-id="2cfad-113">Wählen Sie im Menü **Aktion** die Option **ausgewählte Benutzer in Pool verschieben** aus.</span><span class="sxs-lookup"><span data-stu-id="2cfad-113">From the **Action** menu, select **Move selected users to pool**.</span></span>

5.  <span data-ttu-id="2cfad-114">Wählen Sie in der Dropdownliste den lync Server 2013-Pool aus.</span><span class="sxs-lookup"><span data-stu-id="2cfad-114">From the drop-down list, select the Lync Server 2013 pool.</span></span>

6.  <span data-ttu-id="2cfad-115">Klicken Sie auf **Aktion** und dann auf **Ausgewählte Benutzer in Pool verschieben**.</span><span class="sxs-lookup"><span data-stu-id="2cfad-115">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="2cfad-116">Klicken Sie anschließend auf OK.</span><span class="sxs-lookup"><span data-stu-id="2cfad-116">Click OK.</span></span>
    
    <span data-ttu-id="2cfad-117">![Dialogfeld ' Benutzer verschieben, Ziel Registrierungspool '](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Dialogfeld ' Benutzer verschieben, Ziel Registrierungspool '")</span><span class="sxs-lookup"><span data-stu-id="2cfad-117">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

7.  <span data-ttu-id="2cfad-118">Überprüfen Sie, ob die Spalte des **registrierungspools** für die Benutzer jetzt den lync Server 2013-Pool enthält, der angibt, dass die Benutzer erfolgreich verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="2cfad-118">Verify that the **Registrar pool** column for the users now contains the Lync Server 2013 pool, which indicates that the users have been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-multiple-users-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="2cfad-119">So verschieben Sie mehrere Benutzer mithilfe der lync Server 2013-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="2cfad-119">To move multiple users by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="2cfad-120">Öffnen Sie die lync Server 2013-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="2cfad-120">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="2cfad-121">Geben Sie in der Befehlszeile Folgendes ein, und ersetzen Sie **Benutzer1** und **User2** durch bestimmte Benutzernamen, die Sie verschieben möchten, und ersetzen Sie den **\_ FQDN des Pools** durch den Namen des Ziel Pools.</span><span class="sxs-lookup"><span data-stu-id="2cfad-121">At the command line, type the following and replace **User1** and **User2** with specific user names you want to move and replace **pool\_FQDN** with the name of the destination pool.</span></span> <span data-ttu-id="2cfad-122">In diesem Beispiel werden die Benutzer Hao Chen und Katie Jordan verschoben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-122">In this example we will move users Hao Chen and Katie Jordan.</span></span>
    
        Get-CsUser -Filter {DisplayName -eq "User1" -or DisplayName - eq "User2"} | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="2cfad-123">![Beispiel für ein PowerShell-Get-CsUser-Cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Beispiel für ein PowerShell-Get-CsUser-Cmdlet")</span><span class="sxs-lookup"><span data-stu-id="2cfad-123">![Example of PowerShell Get-CsUser cmdlet](images/JJ205096.767ff9fc-755d-4a80-a710-5b1367aecbe0(OCS.15).jpg "Example of PowerShell Get-CsUser cmdlet")</span></span>  

3.  <span data-ttu-id="2cfad-124">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="2cfad-124">At the command line, type the following</span></span>
    
        Get-CsUser -Identity "User1"

4.  <span data-ttu-id="2cfad-125">Die Identität des **Registrierungsstellen Pools** sollte nun auf den Pool verweisen, den Sie im vorherigen Schritt als **Pool- \_ FQDN** angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-125">The **Registrar Pool** identity should now point to the pool you specified as **pool\_FQDN** in the previous step.</span></span> <span data-ttu-id="2cfad-126">Das vorhanden sein dieser Identität bestätigt, dass der Benutzer erfolgreich verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2cfad-126">The presence of this identity confirms that the user has been successfully moved.</span></span> <span data-ttu-id="2cfad-127">Wiederholen Sie den Schritt, um zu überprüfen, ob **User2** verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2cfad-127">Repeat step to verify **User2** has been moved.</span></span>
    
    <span data-ttu-id="2cfad-128">![Ausgabe des PowerShell-Cmdlets Get-UsUser Identity](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Ausgabe des PowerShell-Cmdlets Get-UsUser Identity")</span><span class="sxs-lookup"><span data-stu-id="2cfad-128">![Output of PowerShell Get-UsUser -Identity cmdlet](images/JJ205096.8ff04c67-37a0-4156-bfbc-28f9f7b137c8(OCS.15).jpg "Output of PowerShell Get-UsUser -Identity  cmdlet")</span></span>  

</div>

<div>

## <a name="to-move-all-users-at-the-same-time-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="2cfad-129">So verschieben Sie alle Benutzer gleichzeitig mithilfe der lync Server 2013-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="2cfad-129">To move all users at the same time by using the Lync Server 2013 Management Shell</span></span>

<span data-ttu-id="2cfad-130">In diesem Beispiel wurden alle Benutzer an den lync Server 2010 Pool (pool01.contoso.net) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-130">In this example, all users have been returned to the Lync Server 2010 pool (pool01.contoso.net).</span></span> <span data-ttu-id="2cfad-131">Mit der lync Server 2013-Verwaltungsshell werden alle Benutzer gleichzeitig in den lync Server 2013-Pool (pool02.contoso.net) verschoben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-131">Using the Lync Server 2013 Management Shell, we will move all users at the same time to the Lync Server 2013 pool (pool02.contoso.net).</span></span>

1.  <span data-ttu-id="2cfad-132">Öffnen Sie die **lync Server 2013-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="2cfad-132">Open the **Lync Server 2013 Management Shell**.</span></span>

2.  <span data-ttu-id="2cfad-133">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="2cfad-133">At the command line, type the following:</span></span>
    
        Get-CsUser -OnLyncServer | Move-CsUser -Target "pool_FQDN"
    
    <span data-ttu-id="2cfad-134">![PowerShell-Cmdlet und Ergebnisse in der Verwaltungsshell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell-Cmdlet und Ergebnisse in der Verwaltungsshell")</span><span class="sxs-lookup"><span data-stu-id="2cfad-134">![PowerShell cmdlet and results in Management Shell](images/JJ205096.1e57ccb1-9378-4dc7-82b7-dcaa63a285c6(OCS.15).png "PowerShell cmdlet and results in Management Shell")</span></span>  

3.  <span data-ttu-id="2cfad-135">Führen Sie als nächstes " **Get-CsUser** " für einen der Pilotbenutzer aus.</span><span class="sxs-lookup"><span data-stu-id="2cfad-135">Next, run **Get-CsUser** for one of the pilot users.</span></span>
    
        Get-CsUser -Identity "Hao Chen"

4.  <span data-ttu-id="2cfad-136">Die Identität des **registrierungspools** für jeden Benutzer verweist nun auf den Pool, den Sie im vorherigen Schritt als "Pool- \_ FQDN" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="2cfad-136">The **Registrar Pool** identity for each user now points to the pool you specified as “pool\_FQDN” in the previous step.</span></span> <span data-ttu-id="2cfad-137">Das vorhanden sein dieser Identität bestätigt, dass der Benutzer erfolgreich verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="2cfad-137">The presence of this identity confirms that the user has been successfully moved.</span></span>

5.  <span data-ttu-id="2cfad-138">Darüber hinaus können wir die Liste der Benutzer in der lync Server 2013-Systemsteuerung anzeigen und überprüfen, ob der Wert des registrierungspools nun auf den lync Server 2013-Pool verweist.</span><span class="sxs-lookup"><span data-stu-id="2cfad-138">Additionally, we can view the list of users in the Lync Server 2013 Control Panel and verify that the Registrar Pool value now points to the Lync Server 2013 pool.</span></span>
    
    <span data-ttu-id="2cfad-139">![Benutzerliste der lync Server 2013-Systemsteuerung](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Benutzerliste der lync Server 2013-Systemsteuerung")</span><span class="sxs-lookup"><span data-stu-id="2cfad-139">![Lync Server 2013 Control Panel user list](images/JJ205096.3f2e87a7-ec59-43c5-82cb-e770108bfb04(OCS.15).jpg "Lync Server 2013 Control Panel user list")</span></span>  

<span data-ttu-id="2cfad-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2cfad-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

