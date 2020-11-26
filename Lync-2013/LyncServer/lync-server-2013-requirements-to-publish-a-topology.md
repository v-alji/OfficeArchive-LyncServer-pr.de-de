---
title: 'Lync Server 2013: Anforderungen an das Veröffentlichen einer Topologie'
description: 'Lync Server 2013: Anforderungen zum Veröffentlichen einer Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements to publish a topology
ms:assetid: 841cdf5d-d884-414d-ab50-3bb681b622ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg195733(v=OCS.15)
ms:contentKeyID: 48184688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5699657e680b78587b8ba354e9dc538f2e280c56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436356"
---
# <a name="requirements-to-publish-a-topology-in-lync-server-2013"></a><span data-ttu-id="31731-103">Anforderungen an das Veröffentlichen einer Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-103">Requirements to publish a topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31731-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31731-104">

<span> </span></span></span>

<span data-ttu-id="31731-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="31731-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="31731-106">In diesem Thema werden die Infrastruktur-und Softwareanforderungen beschrieben, die für das Veröffentlichen einer Topologie spezifisch sind, sei es mithilfe des Topologie-Generators oder der Befehlszeilenschnittstelle der lync Server 2013-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="31731-106">This topic describes the infrastructure and software requirements that are specific to publishing a topology, whether by using Topology Builder or the Lync Server 2013 Management Shell command-line interface.</span></span> <span data-ttu-id="31731-107">Diese Anforderungen gelten zusätzlich zu den allgemeinen Betriebssystem-, Software-und Berechtigungsanforderungen, die für alle lync Server 2013-Verwaltungstools gelten.</span><span class="sxs-lookup"><span data-stu-id="31731-107">These requirements are in addition to the general operating system, software, and permissions requirements applicable to all Lync Server 2013 administrative tools.</span></span> <span data-ttu-id="31731-108">Stellen Sie sicher, dass Sie die Anforderungen aller administrativen Tools erfüllen, bevor Sie eine Topologie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="31731-108">Make sure that you satisfy all administrative tools requirements before you publish a topology.</span></span>

  - <span data-ttu-id="31731-109">Sie müssen den Topology Builder auf einem Computer ausführen, der mit der gleichen Domäne oder Gesamtstruktur der von Ihnen erstellten lync Server 2013-Bereitstellung verbunden ist, damit die Schritte zur Vorbereitung der Active Directory-Domänendienste bereits abgeschlossen sind, sodass Sie die Verwaltungstools auf diesem Computer zum erfolgreichen Veröffentlichen Ihrer Topologie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="31731-109">You must run Topology Builder on a computer that is joined to the same domain or forest of the Lync Server 2013 deployment you are creating so that Active Directory Domain Services preparation steps are already completed, enabling you to use the administrative tools on that computer to successfully publish your topology.</span></span>

  - <span data-ttu-id="31731-110">Die in der Topologie definierten Computer müssen der Domäne, mit Ausnahme von Edgeserver und in AD DS, beigetreten sein.</span><span class="sxs-lookup"><span data-stu-id="31731-110">The computers defined in the topology must be joined to the domain, except for Edge Servers, and in AD DS.</span></span> <span data-ttu-id="31731-111">Die Computer müssen jedoch nicht online sein, wenn Sie die Topologie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="31731-111">However, the computers do not need to be online when you publish the topology.</span></span>

  - <span data-ttu-id="31731-112">Die Dateifreigabe für den Pool muss erstellt und für Remotebenutzer verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="31731-112">The file share for the pool must be created and available to remote users.</span></span>

  - <span data-ttu-id="31731-113">Zum Veröffentlichen eines Enterprise Edition-Front-End-Pools muss der auf SQL Server basierende Back-End-Server mit der Domäne verbunden sein, in der Sie die Server online bereitstellen, und mit den entsprechenden Firewallregeln konfiguriert werden, um ihn Remotebenutzern zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="31731-113">In order to publish an Enterprise Edition Front End pool, the SQL Server-based Back End Server must be joined to the domain in which you are deploying the servers, online, and configured with the appropriate firewall rules to make it available to remote users.</span></span> <span data-ttu-id="31731-114">Details zum Angeben von Firewall-Ausnahmen finden Sie unter [Grundlegendes zu Firewall-Anforderungen für SQL Server mit lync Server 2013](lync-server-2013-understanding-firewall-requirements-for-sql-server.md).</span><span class="sxs-lookup"><span data-stu-id="31731-114">For details about specifying firewall exceptions, see [Understanding firewall requirements for SQL Server with Lync Server 2013](lync-server-2013-understanding-firewall-requirements-for-sql-server.md).</span></span> <span data-ttu-id="31731-115">Weitere Informationen zum Konfigurieren von SQL Server finden Sie unter [Konfigurieren von SQL Server für lync Server 2013](lync-server-2013-configure-sql-server-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="31731-115">For other details about configuring SQL Server, see [Configure SQL Server for Lync Server 2013](lync-server-2013-configure-sql-server-for-lync-server.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="31731-116">Der Standard Edition-Server verfügt über eine Datenbank, die die veröffentlichte Konfiguration akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="31731-116">Standard Edition server has a collocated database that will accept the published configuration.</span></span> <span data-ttu-id="31731-117">Sie müssen zuerst im lync Server-Bereitstellungs-Assistenten die Aufgabe " <STRONG>First Standard Edition-Server vorbereiten</STRONG> " ausführen.</span><span class="sxs-lookup"><span data-stu-id="31731-117">You must first run the <STRONG>Prepare first Standard Edition server</STRONG> setup task in the Lync Server Deployment Wizard.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="31731-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31731-118">See Also</span></span>


[<span data-ttu-id="31731-119">Veröffentlichen der Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-119">Publish the topology in Lync Server 2013</span></span>](lync-server-2013-publish-the-topology.md)  
[<span data-ttu-id="31731-120">Delegieren von Setupberechtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-120">Delegate setup permissions in Lync Server 2013</span></span>](lync-server-2013-delegate-setup-permissions.md)  


[<span data-ttu-id="31731-121">Softwareanforderungen für Verwaltungstools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-121">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
[<span data-ttu-id="31731-122">Betriebssystemunterstützung für Server und Tools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-122">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)  


[<span data-ttu-id="31731-123">Erforderliche Administratorrechte und Gruppenmitgliedschaften für die Installation und Verwaltung von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31731-123">Administrator rights and permissions required for setup and administration of Lync Server 2013</span></span>](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)  
  

<span data-ttu-id="31731-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31731-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

