---
title: 'Lync Server 2013: Löschen eines nicht zugewiesenen Nummernbereichs'
description: 'Lync Server 2013: Löschen eines nicht zugewiesenen Nummernbereichs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an unassigned number range
ms:assetid: a8141bfb-b94d-4d0f-a7a9-2e60d10b103a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182565(v=OCS.15)
ms:contentKeyID: 48185090
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 977cae1432c43a7df33e26597efdb364a7fbea08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430490"
---
# <a name="delete-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="d32d7-103">Löschen eines nicht zugewiesenen Nummernbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d32d7-103">Delete an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d32d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d32d7-104">

<span> </span></span></span>

<span data-ttu-id="d32d7-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d32d7-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d32d7-106">Verwenden Sie eines der folgenden Verfahren, um einen nicht zugewiesenen Nummernbereich für Ankündigungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d32d7-106">Use one of the following procedures to delete an unassigned number range for Announcements.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-unassigned-number-range"></a><span data-ttu-id="d32d7-107">So verwenden Sie die lync Server-Systemsteuerung zum Löschen eines nicht zugewiesenen Nummernbereichs</span><span class="sxs-lookup"><span data-stu-id="d32d7-107">To use Lync Server Control Panel to delete an unassigned number range</span></span>

1.  <span data-ttu-id="d32d7-108">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="d32d7-108">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="d32d7-109">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d32d7-109">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d32d7-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d32d7-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d32d7-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d32d7-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d32d7-112">Klicken Sie in der linken Navigationsleiste auf **VoIP-Funktionen** und klicken Sie dann auf **Nicht zugewiesene Nummer**.</span><span class="sxs-lookup"><span data-stu-id="d32d7-112">In the left navigation bar, click **Voice Features** and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="d32d7-113">Geben Sie auf der Seite **Nicht zugewiesene Nummer** im Suchfeld Teile oder den vollständigen Namen des Bereichs nicht zugewiesener Nummern ein, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="d32d7-113">On the **Unassigned Number** page, in the search field, type all or part of the name of the unassigned number range you want to delete.</span></span>

5.  <span data-ttu-id="d32d7-114">Klicken Sie in der resultierenden Liste der Nummernbereiche auf den Namen, klicken Sie auf **Bearbeiten** und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="d32d7-114">In the resulting list of number ranges, click the name, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="d32d7-115">Klicken Sie auf **Commit für alle**.</span><span class="sxs-lookup"><span data-stu-id="d32d7-115">Click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-unassigned-number-range"></a><span data-ttu-id="d32d7-116">So verwenden Sie Windows PowerShell zum Löschen eines nicht zugewiesenen Nummernbereichs</span><span class="sxs-lookup"><span data-stu-id="d32d7-116">To use Windows PowerShell to delete an unassigned number range</span></span>

1.  <span data-ttu-id="d32d7-117">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d32d7-117">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="d32d7-118">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="d32d7-118">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d32d7-119">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d32d7-119">At the command line, type:</span></span>
    
        Remove-CsUnassignedNumber -Identity "<name of unassigned number range>" 
    
    <span data-ttu-id="d32d7-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d32d7-120">For example:</span></span>
    
        Remove-CsUnassignedNumber -Identity "Unassigned range 1"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d32d7-121">Ausführliche Informationen zu weiteren Optionen finden Sie unter <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span><span class="sxs-lookup"><span data-stu-id="d32d7-121">For details about more options, see <A href="https://docs.microsoft.com/powershell/module/skype/Remove-CsCallParkOrbit">Remove-CsCallParkOrbit</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d32d7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d32d7-122">See Also</span></span>


[<span data-ttu-id="d32d7-123">Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d32d7-123">Create or modify an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-unassigned-number-range.md)  


[<span data-ttu-id="d32d7-124">Remove-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="d32d7-124">Remove-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUnassignedNumber)  
[<span data-ttu-id="d32d7-125">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="d32d7-125">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="d32d7-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d32d7-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

