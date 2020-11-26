---
title: Entfernen eines autorisierten Hosteintrags
description: Entfernen eines autorisierten Hosteintrags
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove an authorized host entry
ms:assetid: 56a04140-347e-4eef-bede-0e858534f71e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204902(v=OCS.15)
ms:contentKeyID: 48184177
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95aa8df1745ad3108654fcb9b441b5919d42ec40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443258"
---
# <a name="remove-an-authorized-host-entry"></a><span data-ttu-id="827a9-103">Entfernen eines autorisierten Hosteintrags</span><span class="sxs-lookup"><span data-stu-id="827a9-103">Remove an authorized host entry</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="827a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="827a9-104">

<span> </span></span></span>

<span data-ttu-id="827a9-105">_**Letztes Änderungsdatum des Themas:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="827a9-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="827a9-106">In diesem Thema wird beschrieben, wie Sie einen autorisierten Legacyhost Eintrag entfernen (als *vertrauenswürdiger Anwendungseintrag* in lync Server 2013 bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="827a9-106">This topic describes how to remove a legacy authorized host entry (known as a *trusted application entry* in Lync Server 2013).</span></span> <span data-ttu-id="827a9-107">Wenn Sie die Remoteanrufsteuerung zu einer lync Server 2013-Bereitstellung migrieren, müssen Sie vorhandene autorisierte Hosteinträge für alle SIP-CSTA-Gateways in Ihrer Office Communications Server 2007 R2-Bereitstellung entfernen.</span><span class="sxs-lookup"><span data-stu-id="827a9-107">You must remove existing authorized host entries for any SIP/CSTA gateways in your Office Communications Server 2007 R2 deployment when you migrate remote call control to a Lync Server 2013 deployment.</span></span> <span data-ttu-id="827a9-108">Sie müssen die im Lieferumfang von Office Communications Server 2007 R2 enthaltenen Verwaltungstools verwenden, um die vorhandenen autorisierten Hosteinträge zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="827a9-108">You must use the administrative tools included with Office Communications Server 2007 R2 to remove the existing authorized host entries.</span></span>

<div>

## <a name="to-remove-an-authorized-host-entry-in-an-office-communications-server-2007-r2-deployment"></a><span data-ttu-id="827a9-109">So entfernen Sie einen autorisierten Hosteintrag in einer Office Communications Server 2007 R2-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="827a9-109">To remove an authorized host entry in an Office Communications Server 2007 R2 deployment</span></span>

1.  <span data-ttu-id="827a9-110">Öffnen Sie die Office Communications Server 2007 R2-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="827a9-110">Open the Office Communications Server 2007 R2 administrative console.</span></span>

2.  <span data-ttu-id="827a9-111">Erweitern Sie die Struktur, und klicken Sie mit der rechten Maustaste auf den Pool, in dem der autorisierte Host erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="827a9-111">Expand the tree and right-click the pool where the authorized host was created.</span></span>

3.  <span data-ttu-id="827a9-112">Klicken Sie auf **Eigenschaften**, und klicken Sie dann auf **Front-End-Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="827a9-112">Click **Properties**, and then click **Front End Properties**.</span></span>

4.  <span data-ttu-id="827a9-113">Klicken Sie auf die Registerkarte **Host Autorisierung** .</span><span class="sxs-lookup"><span data-stu-id="827a9-113">Click the **Host Authorization** tab.</span></span>

5.  <span data-ttu-id="827a9-114">Wählen Sie einen Server aus, und klicken Sie dann auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="827a9-114">Select a server, and then click **Remove**.</span></span>

6.  <span data-ttu-id="827a9-115">Klicken Sie in **Eigenschaften** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="827a9-115">In **Properties**, click **OK**.</span></span>

<span data-ttu-id="827a9-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="827a9-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

