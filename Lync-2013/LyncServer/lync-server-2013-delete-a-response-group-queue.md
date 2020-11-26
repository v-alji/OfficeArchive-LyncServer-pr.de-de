---
title: 'Lync Server 2013: Löschen einer Antwortgruppen Warteschlange'
description: 'Lync Server 2013: Löschen einer Reaktionsgruppen Warteschlange'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a Response Group queue
ms:assetid: 67c7a489-8c5f-4c6b-9387-9d4c11d43695
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521008(v=OCS.15)
ms:contentKeyID: 48184356
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76b00257a12b872615ebc124abff595268b120e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430686"
---
# <a name="delete-a-response-group-queue-in-lync-server-2013"></a><span data-ttu-id="d1e8e-103">Löschen einer Reaktionsgruppen Warteschlange in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e8e-103">Delete a Response Group queue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1e8e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1e8e-104">

<span> </span></span></span>

<span data-ttu-id="d1e8e-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d1e8e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d1e8e-106">Verwenden Sie eines der folgenden Verfahren, um eine Warteschlange zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-106">Use one of the following procedures to delete a queue.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-to-delete-a-queue"></a><span data-ttu-id="d1e8e-107">So verwenden Sie die lync Server-Systemsteuerung zum Löschen einer Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d1e8e-107">To use Lync Server Control Panel to delete a queue</span></span>

1.  <span data-ttu-id="d1e8e-108">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="d1e8e-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d1e8e-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8e-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d1e8e-111">Klicken Sie in der linken Navigationsleiste auf **Reaktionsgruppen** und dann auf **Warteschleife**.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-111">In the left navigation bar, click **Response Groups**, and then click **Queue**.</span></span>

4.  <span data-ttu-id="d1e8e-112">Geben Sie im Suchfeld den Namen der zu löschenden Warteschlange ganz oder teilweise ein.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-112">In the search field, type part or all of the name of the queue you want to delete.</span></span>

5.  <span data-ttu-id="d1e8e-113">Klicken Sie in der Liste der Warteschlangen auf die gewünschte Warteschlange, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-113">In the list of queues, click the queue that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="d1e8e-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-114">Click **OK**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-queue"></a><span data-ttu-id="d1e8e-115">So verwenden Sie Windows PowerShell zum Löschen einer Warteschlange</span><span class="sxs-lookup"><span data-stu-id="d1e8e-115">To use Windows PowerShell to delete a queue</span></span>

1.  <span data-ttu-id="d1e8e-116">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-116">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="d1e8e-117">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="d1e8e-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="d1e8e-118">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d1e8e-118">At the command line, run:</span></span>
    
        Get-CsRgsQueue -Identity <Application Server service> -Name "<name of queue>" | Remove-CsRgsQueue
    
    <span data-ttu-id="d1e8e-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d1e8e-119">For example:</span></span>
    
        Get-CsRgsQueue -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsQueue

<span data-ttu-id="d1e8e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1e8e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

