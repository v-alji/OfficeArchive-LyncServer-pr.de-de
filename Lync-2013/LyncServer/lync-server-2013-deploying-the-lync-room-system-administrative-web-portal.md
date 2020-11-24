---
title: 'Lync Server 2013: Bereitstellen des administrativen lync Room System-Webportals'
description: 'Lync Server 2013: Bereitstellen des administrativen lync Room System-Webportals.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying the Lync Room System Administrative Web Portal
ms:assetid: ecba5b36-632e-40b9-9c2e-ab825baf7a46
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn436324(v=OCS.15)
ms:contentKeyID: 56737621
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e67723b3ddf3f452c53411e560420bb0b043128e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393991"
---
# <a name="deploying-the-lync-room-system-administrative-web-portal-in-lync-server-2013"></a><span data-ttu-id="14afa-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14afa-103">Deploying the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14afa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14afa-104">

<span> </span></span></span>

<span data-ttu-id="14afa-105">_**Letztes Änderungsdatum des Themas:** 2015-05-04_</span><span class="sxs-lookup"><span data-stu-id="14afa-105">_**Topic Last Modified:** 2015-05-04_</span></span>

<span data-ttu-id="14afa-106">Das Microsoft lync Server 2013 lync-Verwaltungsportal ist ein Webportal, das Organisationen zum Verwalten Ihrer lync Room-Konferenzräume verwenden können.</span><span class="sxs-lookup"><span data-stu-id="14afa-106">The Microsoft Lync Server 2013 Lync Room System (LRS) Administrative Web Portal is a web portal that organizations can use to maintain their Lync Room System conference rooms.</span></span> <span data-ttu-id="14afa-107">Administratoren können das LRS-Verwaltungs Webportal verwenden, um die LRS-Integrität zu überwachen, beispielsweise indem Sie angeschlossene Audio/Videogeräte überwachen.</span><span class="sxs-lookup"><span data-stu-id="14afa-107">Administrators can use the LRS Administrative Web Portal to monitor LRS health, for example by monitoring audio/video devices that are connected.</span></span> <span data-ttu-id="14afa-108">Mit diesem Portal können Administratoren über Remoteverbindungen Diagnoseinformationen sammeln, um die Konferenzraumintegrität zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="14afa-108">With this portal, administrators can remotely collect diagnostic information to monitor conference room health.</span></span>

<span data-ttu-id="14afa-109">Das administrative LRS-Webportal wird auf jedem lync-Front-End-Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="14afa-109">The LRS Administrative Web Portal is deployed on every Lync Front End Server.</span></span> <span data-ttu-id="14afa-110">Dieses Handbuch enthält Anweisungen für Administratoren zum Installieren und Konfigurieren des LRS-Verwaltungsportals.</span><span class="sxs-lookup"><span data-stu-id="14afa-110">This guide provides instructions for administrators about how to install and configure the LRS Administrative Web Portal.</span></span> <span data-ttu-id="14afa-111">Sie ist für Administratoren vorgesehen, die über Kenntnisse der lync Server-Verwaltung verfügen und über Administratorrechte verfügen, um die lync Server-Topologie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="14afa-111">It is intended for administrators who have knowledge of Lync Server administration, and who have administrator user rights to modify the Lync Server topology.</span></span>

<span data-ttu-id="14afa-112">Nachdem das LRS Administrative Web Portal auf dem Server bereitgestellt wurde, können Administratoren den Status aller LRS-Räume überprüfen, indem Sie sich auf Ihren eigenen Computern oder Laptops bei der Website anmelden.</span><span class="sxs-lookup"><span data-stu-id="14afa-112">After LRS Administrative Web Portal is deployed on the server, administrators can check the status of all LRS rooms by logging on to the site from their own computers or laptops.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="14afa-113">Wenn Sie das administrative LRS-Webportal in einer Microsoft lync Server 2013-Bereitstellung installieren, sollten Sie das administrative Webportal des <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">Microsoft lync Room-Systems für lync Server 2013</A>verwenden.</span><span class="sxs-lookup"><span data-stu-id="14afa-113">When you install the LRS Administrative Web Portal in a Microsoft Lync Server 2013 deployment, you should use the <A href="https://go.microsoft.com/fwlink/p/?linkid=544806">Microsoft Lync Room System Administrative Web Portal for Lync Server 2013</A>.</span></span><BR><span data-ttu-id="14afa-114">Eine neue Version des LRS-Administrator-Webportal steht für Skype for Business Server 2015 zur Verfügung, Sie sollten diese Version aber nur installieren, wenn Sie Skype for Business Server 2015 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="14afa-114">A new version of the LRS Administrative Web Portal is available for Skype for Business Server 2015, but you should not install that version unless you have deployed Skype for Business Server 2015.</span></span> <span data-ttu-id="14afa-115">Laden Sie das <A href="https://go.microsoft.com/fwlink/?linkid=544807">Administrative Webportal des Microsoft lync Room-Systems für Skype for Business Server 2015</A>herunter.</span><span class="sxs-lookup"><span data-stu-id="14afa-115">Download the <A href="https://go.microsoft.com/fwlink/?linkid=544807">Microsoft Lync Room System Administrative Web Portal for Skype for Business Server 2015</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="14afa-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="14afa-116">In This Section</span></span>

[<span data-ttu-id="14afa-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span><span class="sxs-lookup"><span data-stu-id="14afa-117">Configuring your Lync Server 2013 environment for the Lync Room System Administrative Web Portal</span></span>](lync-server-2013-configuring-your-environment-for-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="14afa-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14afa-118">Installing the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-installing-the-lync-room-system-administrative-web-portal.md)

[<span data-ttu-id="14afa-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14afa-119">Using the Lync Room System Administrative Web Portal in Lync Server 2013</span></span>](lync-server-2013-using-the-lync-room-system-administrative-web-portal.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="14afa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14afa-120">See Also</span></span>


[<span data-ttu-id="14afa-121">Bereitstellen von Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14afa-121">Deploying conferencing in Lync Server 2013</span></span>](lync-server-2013-deploying-conferencing.md)  
  

<span data-ttu-id="14afa-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14afa-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

