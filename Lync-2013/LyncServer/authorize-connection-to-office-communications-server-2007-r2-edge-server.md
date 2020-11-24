---
title: Autorisieren der Verbindung zu Office Communications Server 2007 R2 Edge Server
description: Autorisieren der Verbindung zu Office Communications Server 2007 R2 Edge Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Authorize connection to Office Communications Server 2007 R2 Edge Server
ms:assetid: 14f6798a-28d6-4b3d-8734-942192e1bbf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204702(v=OCS.15)
ms:contentKeyID: 48183493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de8dadb2c476c892f4ffd548ce176d12d3b1a1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394259"
---
# <a name="authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="4be6f-103">Autorisieren der Verbindung zu Office Communications Server 2007 R2 Edge Server</span><span class="sxs-lookup"><span data-stu-id="4be6f-103">Authorize connection to Office Communications Server 2007 R2 Edge Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4be6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4be6f-104">

<span> </span></span></span>

<span data-ttu-id="4be6f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="4be6f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="4be6f-106">Für jeden lync Server 2013-Front-End-Server oder Standard Edition-Server in Ihrem Pilot Pool müssen Sie die Liste der internen Server aktualisieren, die zum Herstellen einer Verbindung mit dem Office Communications Server 2007 R2 Edge-Server autorisiert sind.</span><span class="sxs-lookup"><span data-stu-id="4be6f-106">For each Lync Server 2013 Front End Server or Standard Edition server in your pilot pool, you must update the list of internal servers that are authorized to connect to the Office Communications Server 2007 R2 Edge Server.</span></span> <span data-ttu-id="4be6f-107">Ohne diese Updates funktionieren externe Audio/visuelle (A/V)-Konferenzen für Benutzer, die mit dem Legacy-Edgeserver verbunden sind, nicht.</span><span class="sxs-lookup"><span data-stu-id="4be6f-107">Without these updates, external audio/visual (A/V) conferencing for users joining by using the legacy Edge Server will not work.</span></span>

<div>

## <a name="to-authorize-connection-to-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="4be6f-108">So autorisieren Sie die Verbindung zu Office Communications Server 2007 R2 Edge Server</span><span class="sxs-lookup"><span data-stu-id="4be6f-108">To Authorize Connection to Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="4be6f-109">Öffnen Sie auf dem Office Communications Server 2007 R2-Edgeserver in der Gruppe **Administrative Tools** das Snap-in **Computer Verwaltung** .</span><span class="sxs-lookup"><span data-stu-id="4be6f-109">From the Office Communications Server 2007 R2 Edge Server, from the **Administrative Tools** group, open the **Computer Management** snap-in.</span></span>

2.  <span data-ttu-id="4be6f-110">Erweitern Sie in der Konsolenstruktur **Dienste und Anwendungen**.</span><span class="sxs-lookup"><span data-stu-id="4be6f-110">In the console tree, expand **Services and Applications**.</span></span>

3.  <span data-ttu-id="4be6f-111">Klicken Sie mit der rechten Maustaste auf **Office Communications Server 2007 R2**, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="4be6f-111">Right-click **Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="4be6f-112">Klicken Sie auf die Registerkarte **intern** .</span><span class="sxs-lookup"><span data-stu-id="4be6f-112">Click the **Internal** tab.</span></span>

5.  <span data-ttu-id="4be6f-113">Klicken Sie unter **Server hinzufügen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="4be6f-113">Under **Add Server**, click **Add**.</span></span>

6.  <span data-ttu-id="4be6f-114">Geben Sie im Dialogfeld **Office Communications Server hinzufügen** die entsprechenden Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="4be6f-114">In the **Add Office Communications Server** dialog box, enter the appropriate information:</span></span>
    
      - <span data-ttu-id="4be6f-115">Geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) jedes lync Server 2013-Front-End-Servers oder Standard Edition-Servers und lync Server 2013-Pools an.</span><span class="sxs-lookup"><span data-stu-id="4be6f-115">Specify the fully qualified domain name (FQDN) of each Lync Server 2013 Front End Server or Standard Edition server, and Lync Server 2013 pool.</span></span>
    
      - <span data-ttu-id="4be6f-116">Geben Sie den FQDN des lync Server 2013-Directors an, wenn Sie eine statische Route im Pool konfiguriert haben, die den Computer für den nächsten Hop nach dem FQDN angibt.</span><span class="sxs-lookup"><span data-stu-id="4be6f-116">Specify the FQDN of the Lync Server 2013 Director if you configured a static route on the pool that specifies the next hop computer by its FQDN.</span></span>

7.  <span data-ttu-id="4be6f-117">Nachdem Sie einen Eintrag für jeden lync Server 2013, Front-End-Server, Standard Edition-Server,-Pool und-Director hinzugefügt haben, klicken Sie auf über **nehmen** , und klicken Sie dann auf **OK** , um die Seite Eigenschaften zu schließen.</span><span class="sxs-lookup"><span data-stu-id="4be6f-117">After you have added an entry for each Lync Server 2013, Front End Server, Standard Edition server, pool, and Director, click **Apply** and then click **OK** to close the Properties page.</span></span>

<span data-ttu-id="4be6f-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4be6f-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

