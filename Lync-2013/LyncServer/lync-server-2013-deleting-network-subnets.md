---
title: 'Lync Server 2013: Löschen von Netzwerk-Subnetzen'
description: 'Lync Server 2013: Löschen von Netzwerk-Subnetzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network subnets
ms:assetid: c1850f38-40a3-48c9-b6f1-f181c5e63b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721873(v=OCS.15)
ms:contentKeyID: 49733806
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6635ec99b68c4ceb10d1cda343fef35c951bf152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430280"
---
# <a name="deleting-network-subnets-in-lync-server-2013"></a><span data-ttu-id="f887c-103">Löschen von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f887c-103">Deleting network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f887c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f887c-104">

<span> </span></span></span>

<span data-ttu-id="f887c-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f887c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f887c-106">Sie können das folgende Verfahren verwenden, um ein Subnetz zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f887c-106">You can use the following procedure to delete a subnet.</span></span> <span data-ttu-id="f887c-107">In der lync Server-Systemsteuerung können Sie ein Netzwerk-Subnetz erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="f887c-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="f887c-108">Details zum Erstellen oder Ändern von Netzwerk-Subnetzen finden Sie unter Erstellen oder Ändern von Netzwerk-Subnetzen [in lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="f887c-108">For details on creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<span data-ttu-id="f887c-109">In den meisten Bereitstellungen von Microsoft lync Server 2013, bei denen die Anrufannahme Steuerung (Call Admission Control, CAC) implementiert ist, gibt es in der Regel eine große Anzahl von Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="f887c-109">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="f887c-110">Aus diesem Grund ist es am besten, Subnets aus der lync Server-Verwaltungsshell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f887c-110">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="f887c-111">Von dort aus können Sie **New-CsNetworkSubnet** in Verbindung mit dem Windows PowerShell **-Cmdlet Import-CSV** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f887c-111">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="f887c-112">Wenn Sie diese Cmdlets zusammen verwenden, können Sie die subneteinstellungen aus einer CSV-Datei (Comma-Separated Values) lesen und gleichzeitig mehrere Subnetze erstellen.</span><span class="sxs-lookup"><span data-stu-id="f887c-112">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="f887c-113">Beispiele zum Erstellen von Subnetzen aus einer CSV-Datei finden Sie unter [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="f887c-113">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-delete-a-network-subnet"></a><span data-ttu-id="f887c-114">So löschen Sie ein Netzwerk-Subnetz</span><span class="sxs-lookup"><span data-stu-id="f887c-114">To delete a network subnet</span></span>

1.  <span data-ttu-id="f887c-115">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="f887c-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="f887c-116">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f887c-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="f887c-117">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="f887c-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="f887c-118">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Subnetz**.</span><span class="sxs-lookup"><span data-stu-id="f887c-118">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="f887c-119">Klicken Sie auf der Seite **Subnetz** auf das Subnetz, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="f887c-119">On the **Subnet** page, click the subnet that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f887c-120">Sie können mehr als ein Subnetz gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="f887c-120">You can delete more than one subnet at a time.</span></span> <span data-ttu-id="f887c-121">Drücken Sie dazu STRG, und wählen Sie mehrere Subnetze aus, während Sie die STRG-Taste gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="f887c-121">To do this, press CTRL and select multiple subnets while holding down the CTRL key.</span></span> <span data-ttu-id="f887c-122">Wenn Sie alle Subnetze auswählen möchten, klicken Sie im Menü <STRONG>Bearbeiten</STRONG> auf <STRONG>Alles auswählen</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="f887c-122">Or, to select all subnets, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="f887c-123">Klicken Sie im Menü **Bearbeiten** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="f887c-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="f887c-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f887c-124">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f887c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f887c-125">See Also</span></span>


[<span data-ttu-id="f887c-126">Erstellen oder Ändern von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f887c-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
  

<span data-ttu-id="f887c-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f887c-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

