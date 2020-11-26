---
title: 'Lync Server 2013: Löschen eines Workflows'
description: 'Lync Server 2013: Löschen eines Workflows'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a workflow
ms:assetid: 0469a6b8-ce1e-459b-bc3d-4c8adf2d97d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520944(v=OCS.15)
ms:contentKeyID: 48183274
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a588a1dc0428660db95d4d492abbd1b157ca7a0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430651"
---
# <a name="delete-a-workflow-in-lync-server-2013"></a><span data-ttu-id="96890-103">Löschen eines Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="96890-103">Delete a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="96890-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="96890-104">

<span> </span></span></span>

<span data-ttu-id="96890-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="96890-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="96890-106">Verwenden Sie eines der folgenden Verfahren, um einen Workflow zu löschen.</span><span class="sxs-lookup"><span data-stu-id="96890-106">Use one of the following procedures to delete a workflow.</span></span>

<div>

## <a name="to-use-lync-server-control-panel-delete-a-workflow"></a><span data-ttu-id="96890-107">So verwenden Sie die lync Server-Systemsteuerung Löschen eines Workflows</span><span class="sxs-lookup"><span data-stu-id="96890-107">To use Lync Server Control Panel delete a workflow</span></span>

1.  <span data-ttu-id="96890-108">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="96890-108">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="96890-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="96890-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="96890-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="96890-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="96890-111">Klicken Sie in der linken Navigationsleiste auf **Reaktionsgruppen** und dann auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="96890-111">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="96890-112">Klicken Sie auf der Seite **Workflow** auf **Workflow erstellen oder bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="96890-112">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="96890-113">Geben Sie im Feld **Dienstsuche auswählen einen** Teil des Namens des **ApplicationServer** -Diensts ein, der den zu löschenden Workflow hostet.</span><span class="sxs-lookup"><span data-stu-id="96890-113">In the **Select a Service** search field, type part or all of the name of the **ApplicationServer** service that hosts the workflow that you want to delete.</span></span>

6.  <span data-ttu-id="96890-114">Klicken Sie in der Liste der Dienste auf den gewünschten Dienst, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="96890-114">In the list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="96890-115">Die Webseite des Reaktionsgruppen-Konfigurationstools wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="96890-115">The Response Group Configuration Tool webpage opens.</span></span> <span data-ttu-id="96890-116">Sie können die Webseite für das Reaktionsgruppen-Konfigurations Tool auch direkt in einem Webbrowser öffnen, indem Sie eine Verbindung mit <STRONG>https:// &lt; webPoolFqdn &gt; /RgsConfig</STRONG>herstellen.</span><span class="sxs-lookup"><span data-stu-id="96890-116">You can also open the Response Group Configuration Tool webpage directly from a web browser by connecting to <STRONG>https://&lt;webPoolFqdn&gt;/RgsConfig</STRONG>.</span></span>

    
    </div>

7.  <span data-ttu-id="96890-117">Suchen Sie unter **vorhandenen Workflow verwalten** nach dem Workflow, den Sie löschen möchten, und klicken Sie dann unter **Aktion** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="96890-117">Under **Manage an Existing Workflow**, locate the workflow you want to delete, and then under **Action**, click **Delete**.</span></span>

8.  <span data-ttu-id="96890-118">Klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="96890-118">Click **Yes**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-delete-a-workflow"></a><span data-ttu-id="96890-119">So löschen Sie einen Workflow mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96890-119">To use Windows PowerShell to delete a workflow</span></span>

1.  <span data-ttu-id="96890-120">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="96890-120">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="96890-121">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="96890-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="96890-122">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="96890-122">At the command line, run:</span></span>
    
        Get-CsRgsWorkflow -Identity <Application Server service> -Name "<name of workflow>" | Remove-CsRgsWorkflow
    
    <span data-ttu-id="96890-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="96890-123">For example:</span></span>
    
        Get-CsRgsWorkflow -Identity service:ApplicationServer:redmond.contoso.com -Name "Help Desk" | Remove-CsRgsWorkflow

<span data-ttu-id="96890-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="96890-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

