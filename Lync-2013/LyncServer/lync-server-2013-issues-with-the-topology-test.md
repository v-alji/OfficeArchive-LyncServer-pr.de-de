---
title: 'Lync Server 2013: Probleme mit dem Topologie-Test'
description: 'Lync Server 2013: Probleme mit dem Topologie-Test.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the topology test
ms:assetid: 821e8916-7b5d-4f64-8fb0-e5cc392ec1bb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205045(v=OCS.15)
ms:contentKeyID: 48184670
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a0f24942844bcf371eff94ee04c8faafcf513d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426711"
---
# <a name="issues-with-the-topology-test-in-lync-server-2013"></a><span data-ttu-id="560db-103">Probleme mit dem Topologie-Test in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="560db-103">Issues with the topology test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="560db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="560db-104">

<span> </span></span></span>

<span data-ttu-id="560db-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="560db-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="560db-106">Wie das Cmdlet " **Test-CsTopology** " bietet Ihnen Best Practice Analyzer eine Möglichkeit, zu überprüfen, ob lync Server 2013 auf globaler Ebene ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="560db-106">Like the **Test-CsTopology** cmdlet, Best Practice Analyzer provides a way for you to verify that Lync Server 2013 is functioning correctly at a global level.</span></span> <span data-ttu-id="560db-107">Standardmäßig überprüft Best Practice Analyzer wie das Cmdlet Ihre gesamte lync Server 2013-Infrastruktur, überprüft, ob die erforderlichen Dienste ausgeführt werden, und dass die entsprechenden Benutzerrechte und Berechtigungen für diese Dienste und für die universellen Sicherheitsgruppen festgesetzt wurden, die bei der Installation von lync Server 2013 erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="560db-107">By default, Best Practice Analyzer, like the cmdlet, checks your entire Lync Server 2013 infrastructure, verifying that the required services are running, and that the appropriate user rights and permissions have been set for these services and for the universal security groups created when you install Lync Server 2013.</span></span>

<span data-ttu-id="560db-108">Zusätzlich zur Überprüfung der Gültigkeit von lync Server als Ganzes überprüft **Test-CsTopology** auch die Gültigkeit eines bestimmten Diensts.</span><span class="sxs-lookup"><span data-stu-id="560db-108">In addition to verifying the validity of Lync Server as a whole, **Test-CsTopology** also checks the validity of a specific service.</span></span> <span data-ttu-id="560db-109">Details zur Verwendung des Cmdlets zum Testen bestimmter Dienste finden Sie unter [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="560db-109">For details about using the cmdlet to test specific services, see [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) in the Lync Server Management Shell documentation.</span></span> <span data-ttu-id="560db-110">Verwenden Sie die folgenden Informationen, um Probleme mit Ihrer Topologie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="560db-110">Use the following information to help resolve issues with your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="560db-111">Je nach Konfiguration Ihrer Edgeserver und der zugehörigen Umkreisnetzwerk Einstellungen, einschließlich Firewalleinstellungen und-Berechtigungen, ist Best Practices Analyzer möglicherweise nicht in der Lage, auf Ihre Edgeserver zuzugreifen und diese zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="560db-111">Depending on the configuration of your Edge Servers and any related perimeter network settings, including firewall settings and permissions, Best Practices Analyzer might not be able to access and scan your Edge Servers.</span></span> <span data-ttu-id="560db-112">Wenn Sie bei der Überprüfung Edgeserver einbeziehen und die Berichte darauf hindeuten, dass ein Problem beim Zugriff auf Edgeserver vorliegt, deaktivieren Sie das Kontrollkästchen <STRONG>Edgeserver</STRONG> , und führen Sie den Scan erneut aus, um zu verhindern, dass das Problem in Berichten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="560db-112">If you include Edge Servers in your scan and the reports indicate that there is an issue accessing Edge Servers, clear the <STRONG>Edge Servers</STRONG> check box and run the scan again to prevent the issue from showing up in reports.</span></span>



</div>

<div>

## <a name="resolving-issues-with-your-topology"></a><span data-ttu-id="560db-113">Beheben von Problemen mit Ihrer Topologie</span><span class="sxs-lookup"><span data-stu-id="560db-113">Resolving Issues with Your Topology</span></span>

<span data-ttu-id="560db-114">Wenn der Topologie-Test Probleme mit Ihrer Topologie gefunden hat, sind diese Probleme wahrscheinlich auf Probleme zurückzuführen, die beim Veröffentlichen oder Aktivieren Ihrer Topologie aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="560db-114">If the topology test found issues with your topology, these issues are probably caused by issues that occurred when you published or enabled your topology.</span></span>

<span data-ttu-id="560db-115">Wenn Sie Änderungen an Ihrer Topologie vornehmen, werden die Änderungen erst wirksam, wenn Sie sowohl veröffentlicht als auch aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="560db-115">When you make changes to your topology, the changes take effect only when they have been both published and enabled.</span></span> <span data-ttu-id="560db-116">Sie müssen Topologie-Generator verwenden, um Topologie-Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="560db-116">You must use Topology Builder to make topology changes.</span></span> <span data-ttu-id="560db-117">Nachdem Sie Änderungen vorgenommen haben, können Sie diese Änderungen dann mithilfe des Topologie-Generators veröffentlichen und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="560db-117">After you make changes, you can then publish and enable those changes by using Topology Builder.</span></span>

<span data-ttu-id="560db-118">Wenn Sie die Änderungen veröffentlichen, werden die neuen Informationen (beispielsweise eine neue Website oder eine neue Serverrolle) in den zentralen Verwaltungsspeicher geschrieben.</span><span class="sxs-lookup"><span data-stu-id="560db-118">When you publish the changes, the new information (for example, a new site or a new server role) is written to the Central Management store.</span></span> <span data-ttu-id="560db-119">Diese neuen (oder die neu geänderten) Objekte treten jedoch nicht unmittelbar in Ihre Topologie ein.</span><span class="sxs-lookup"><span data-stu-id="560db-119">However, these new (or the newly modified) objects do not immediately join your topology.</span></span> <span data-ttu-id="560db-120">Objekte treten nur bei der Aktivierung der aktualisierten Topologie in Ihre Topologie ein.</span><span class="sxs-lookup"><span data-stu-id="560db-120">Objects join your topology only when you enable the updated topology.</span></span> <span data-ttu-id="560db-121">Wenn Sie die Option "veröffentlichen" im Topologie-Generator auswählen, treten beide Schritte auf: die Änderungen werden veröffentlicht (das heißt, Sie werden in den zentralen Verwaltungsspeicher geschrieben), und dann wird die neue Topologie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="560db-121">If you select the Publish option in Topology Builder both of these steps occur: the changes are published (that is, they are written to the Central Management store) and then the new topology is enabled.</span></span>

<span data-ttu-id="560db-122">Standardmäßig sind Mitglieder der RTCUniversalServerAdmins-Gruppe autorisiert, das Cmdlet **Publish-CsTopology** und das Cmdlet **enable-CsTopology** auszuführen.</span><span class="sxs-lookup"><span data-stu-id="560db-122">By default, members of the RTCUniversalServerAdmins group are authorized to run the **Publish-CsTopology** cmdlet and the **Enable-CsTopology** cmdlet.</span></span> <span data-ttu-id="560db-123">Wenn jedoch keine Setup-Berechtigungen delegiert wurden, müssen Sie als Domänenadministrator angemeldet sein, um **Publish-CsTopology** ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="560db-123">However, if setup permissions have not been delegated, you must be logged on as a domain administrator to run **Publish-CsTopology**.</span></span> <span data-ttu-id="560db-124">Um RTCUniversalServerAdmins das Recht zu geben, das Cmdlet **Publish-CsTopology** tatsächlich zu verwenden, müssen Sie das **Grant-CsSetupPermission-** Cmdlet auf jedem Active Directory-Container ausführen, der Computer mit lync Server-Diensten enthält.</span><span class="sxs-lookup"><span data-stu-id="560db-124">To give RTCUniversalServerAdmins the right to actually use the **Publish-CsTopology** cmdlet, you must run the **Grant-CsSetupPermission** cmdlet on every Active Directory container that contains computers running Lync Server services.</span></span> <span data-ttu-id="560db-125">Um RTCUniversalServerAdmins das Recht zu geben, das Cmdlet **enable-CsTopology** zu verwenden, müssen Sie das Cmdlet " **Satz-CsSetupPermission** " für jeden Active Directory-Domänendienst Container ausführen, der Computer mit lync Server-Diensten enthält.</span><span class="sxs-lookup"><span data-stu-id="560db-125">To give RTCUniversalServerAdmins the right to use the **Enable-CsTopology** cmdlet, you must run the **Set-CsSetupPermission** cmdlet against every Active Directory Domain Services container that contains computers running Lync Server services.</span></span> <span data-ttu-id="560db-126">Beachten Sie, dass dies für das Aktivieren und Veröffentlichen einer Topologie mithilfe des Topologie-Generators gilt.</span><span class="sxs-lookup"><span data-stu-id="560db-126">Note that this applies to enabling and publishing a topology by using Topology Builder.</span></span> <span data-ttu-id="560db-127">Wenn Sie die Berechtigungen nicht mithilfe von " **CsSetupPermission**" delegiert haben, kann nur ein Domänenadministrator eine Topologie mithilfe des Topologie-Generators aktivieren und veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="560db-127">If you have not delegated permissions by using **Set-CsSetupPermission**, only a domain administrator can enable and publish a topology through Topology Builder.</span></span>

<span data-ttu-id="560db-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="560db-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

