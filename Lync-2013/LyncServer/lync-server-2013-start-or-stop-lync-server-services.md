---
title: 'Lync Server 2013: Starten oder Beenden von lync Server-Diensten'
description: 'Lync Server 2013: Starten oder Beenden von lync Server Services.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Start or stop Lync Server 2013 services
ms:assetid: 1c70b4ec-9de5-4f7a-a3c9-c0eb76710505
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520958(v=OCS.15)
ms:contentKeyID: 48183554
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d6e6520cbf6fda38676beab984c2d006061b019
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423680"
---
# <a name="start-or-stop-lync-server-2013-services"></a><span data-ttu-id="4871b-103">Starten oder Beenden von lync Server 2013-Diensten</span><span class="sxs-lookup"><span data-stu-id="4871b-103">Start or stop Lync Server 2013 services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4871b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4871b-104">

<span> </span></span></span>

<span data-ttu-id="4871b-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="4871b-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="4871b-106">Sie können die lync Server-Systemsteuerung verwenden, um alle lync Server 2013-Dienste zu starten oder zu beenden, die auf einem bestimmten Computer ausgeführt werden, oder um einen bestimmten Dienst zu starten oder zu beenden.</span><span class="sxs-lookup"><span data-stu-id="4871b-106">You can use Lync Server Control Panel to start or stop all the Lync Server 2013 services running on a specific computer or to start or stop a specific service.</span></span>

<div>

## <a name="to-start-or-stop-all-lync-server-services-on-a-computer"></a><span data-ttu-id="4871b-107">So starten oder beenden Sie alle lync Server-Dienste auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="4871b-107">To start or stop all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="4871b-108">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="4871b-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span> <span data-ttu-id="4871b-109">Sie können feststellen, ob Ihnen die CsServerAdministrator-oder CsAdministrator-RBAC-Rolle zugewiesen wurde, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="4871b-109">You can determine whether you have been assigned the CsServerAdministrator or the CsAdministrator RBAC role by running a command similar to the following:</span></span>
    
        Get-CsAdminRoleAssignment -Identity "kenmyer"

2.  <span data-ttu-id="4871b-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4871b-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4871b-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4871b-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4871b-112">Klicken Sie in der linken Navigationsleiste auf **Topologie** und dann auf **Status**.</span><span class="sxs-lookup"><span data-stu-id="4871b-112">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="4871b-113">Sortieren oder Durchsuchen Sie auf der **Status** Seite die Liste nach Bedarf, um den Computer zu finden, auf dem die Dienste ausgeführt werden, die Sie starten oder beenden möchten, und klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="4871b-113">On the **Status** page, sort or search through the list as needed to find the computer that is running the services you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="4871b-114">Klicken Sie auf **Aktion**.</span><span class="sxs-lookup"><span data-stu-id="4871b-114">Click **Action**.</span></span>

6.  <span data-ttu-id="4871b-115">Klicken Sie auf **alle Dienste starten** oder **alle Dienste beenden**.</span><span class="sxs-lookup"><span data-stu-id="4871b-115">Click **Start All services** or **Stop All services**.</span></span>

</div>

<div>

## <a name="to-start-or-stop-a-specific-service"></a><span data-ttu-id="4871b-116">So starten oder beenden Sie einen bestimmten Dienst</span><span class="sxs-lookup"><span data-stu-id="4871b-116">To start or stop a specific service</span></span>

1.  <span data-ttu-id="4871b-117">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="4871b-117">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="4871b-118">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4871b-118">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4871b-119">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4871b-119">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4871b-120">Klicken Sie in der linken Navigationsleiste auf **Topologie** und dann auf **Status**.</span><span class="sxs-lookup"><span data-stu-id="4871b-120">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="4871b-121">Sortieren oder Durchsuchen Sie auf der **Status** Seite die Liste nach Bedarf, um den Computer zu finden, auf dem der Dienst ausgeführt wird, den Sie starten oder beenden möchten, und klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="4871b-121">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="4871b-122">Klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="4871b-122">Click **Properties**.</span></span>

6.  <span data-ttu-id="4871b-123">Sortieren Sie die Liste der Dienste, falls erforderlich, und klicken Sie auf den Dienst, den Sie starten oder beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4871b-123">Sort the list of services, if necessary, and click the service you want to start or stop.</span></span>

7.  <span data-ttu-id="4871b-124">Klicken Sie auf **Aktion**.</span><span class="sxs-lookup"><span data-stu-id="4871b-124">Click **Action**.</span></span>

8.  <span data-ttu-id="4871b-125">Klicken Sie auf **Dienst starten** oder **Dienst beenden**.</span><span class="sxs-lookup"><span data-stu-id="4871b-125">Click **Start service** or **Stop service**.</span></span>

9.  <span data-ttu-id="4871b-126">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="4871b-126">Click **Close**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4871b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4871b-127">See Also</span></span>


[<span data-ttu-id="4871b-128">Verhindern von Sitzungen für Dienste in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4871b-128">Prevent sessions for services in Lync Server 2013</span></span>](lync-server-2013-prevent-sessions-for-services.md)  


[<span data-ttu-id="4871b-129">Verwalten der Lync Server 2013-Topologie</span><span class="sxs-lookup"><span data-stu-id="4871b-129">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="4871b-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4871b-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

