---
title: 'Lync Server 2013: Konfigurieren eines vorhandenen zentralen Verwaltungsservers'
description: 'Lync Server 2013: Konfigurieren eines vorhandenen zentralen Verwaltungsservers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure an existing Central Management Server
ms:assetid: d715b24a-1256-4a7c-a5ef-1cee41d6b733
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205315(v=OCS.15)
ms:contentKeyID: 48185584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef93281be2537ca5e4a5892a8617500ce54f3c45
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434124"
---
# <a name="configure-an-existing-central-management-server-in-lync-server-2013"></a><span data-ttu-id="4a71a-103">Konfigurieren eines vorhandenen zentralen Verwaltungsservers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4a71a-103">Configure an existing Central Management Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a71a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a71a-104">

<span> </span></span></span>

<span data-ttu-id="4a71a-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="4a71a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="4a71a-106">Wenn Sie einen zentralen Verwaltungs Server aus einer vorhandenen lync Server 2013-Bereitstellung wieder verwenden, müssen Sie das unten beschriebene Verfahren ausführen, um sicherzustellen, dass die lync Server-Systemsteuerung und Windows PowerShell ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="4a71a-106">If you reuse a Central Management Server from an existing Lync Server 2013 deployment, you must run the procedure described below to make sure that Lync Server Control Panel and Windows PowerShell function correctly.</span></span>

<div>

## <a name="to-configure-an-existing-central-management-server"></a><span data-ttu-id="4a71a-107">So konfigurieren Sie einen vorhandenen zentralen Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="4a71a-107">To configure an existing Central Management Server</span></span>

1.  <span data-ttu-id="4a71a-108">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4a71a-108">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4a71a-109">Verwenden Sie das Cmdlet **Update-CsAdminRole** , um die rollenbasierten zugriffssteuerungsrollen zu aktualisieren, die auf dem zentralen Verwaltungs Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="4a71a-109">Use the **Update-CsAdminRole** cmdlet to update the role-based access control (RBAC) roles stored in the Central Management Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4a71a-110">Es wird keine Ausgabe erwartet, es sei denn, es liegt ein Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="4a71a-110">No output is expected unless there is an error.</span></span>

    
    <span data-ttu-id="4a71a-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a71a-111"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

