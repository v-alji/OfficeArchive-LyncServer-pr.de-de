---
title: 'Lync Server 2013: Löschen einer Agentengruppe'
description: 'Lync Server 2013: Löschen einer Agentengruppe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an agent group
ms:assetid: df385fd1-62f4-42b7-a349-4eb38dea50c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182597(v=OCS.15)
ms:contentKeyID: 48185670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dded2db0957e37a624d7e8bf3a06e102f8d35cad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430644"
---
# <a name="delete-an-agent-group-in-lync-server-2013"></a><span data-ttu-id="8a3af-103">Löschen einer Agentengruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a3af-103">Delete an agent group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a3af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a3af-104">

<span> </span></span></span>

<span data-ttu-id="8a3af-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="8a3af-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="8a3af-106">Verwenden Sie eines der folgenden Verfahren, um eine Agentengruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="8a3af-106">Use one of the following procedures to delete an agent group.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-an-agent-group"></a><span data-ttu-id="8a3af-107">So löschen Sie eine Agentengruppe mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="8a3af-107">To use Lync Server Control Panel to delete an agent group</span></span>

1.  <span data-ttu-id="8a3af-108">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a3af-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="8a3af-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8a3af-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8a3af-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8a3af-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8a3af-111">Klicken Sie auf der linken Navigationsleiste auf **Reaktionsgruppen** und dann auf **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="8a3af-111">In the left navigation bar, click **Response Groups**, and then click **Group**.</span></span>

4.  <span data-ttu-id="8a3af-112">Geben Sie auf der Seite **Antwortgruppen** den Namen der zu löschenden Agentengruppe ganz oder teilweise in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="8a3af-112">On the **Response Groups** page, type all or part of the name of the agent group that you want to delete in the search field.</span></span>

5.  <span data-ttu-id="8a3af-113">Klicken Sie in der Ergebnisliste auf die Gruppe, die Sie löschen möchten, klicken Sie auf **Bearbeiten** und dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="8a3af-113">In the resulting list, click the group that you want to delete, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="8a3af-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a3af-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-an-agent-group"></a><span data-ttu-id="8a3af-115">So löschen Sie eine Agentengruppe mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a3af-115">To use Windows PowerShell to delete an agent group</span></span>

1.  <span data-ttu-id="8a3af-116">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a3af-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="8a3af-117">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="8a3af-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="8a3af-118">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="8a3af-118">At the command line, run:</span></span>
    
        Get-CsRgsAgentGroup -Identity <Application Server service> -Name "<name of agent group>" | Remove-CsRgsAgentGroup
    
    <span data-ttu-id="8a3af-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8a3af-119">For example:</span></span>
    
        Get-CsRgsAgentGroup -Identity service:ApplicationServer:redmond.contoso.com -Name "Human Resources" | Remove-CsRgsAgentGroup

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8a3af-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a3af-120">See Also</span></span>


[<span data-ttu-id="8a3af-121">Erstellen oder Ändern einer Agentengruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a3af-121">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  


[<span data-ttu-id="8a3af-122">Remove-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="8a3af-122">Remove-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsRgsAgentGroup)  
[<span data-ttu-id="8a3af-123">Get-CsRgsAgentGroup</span><span class="sxs-lookup"><span data-stu-id="8a3af-123">Get-CsRgsAgentGroup</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsAgentGroup)  
  

<span data-ttu-id="8a3af-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a3af-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

