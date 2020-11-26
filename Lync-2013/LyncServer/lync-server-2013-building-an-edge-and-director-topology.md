---
title: 'Lync Server 2013: Erstellen einer Edge- und Director-Topologie'
description: 'Lync Server 2013: Erstellen einer Edge-und Director-Topologie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Building an edge and Director topology
ms:assetid: 11e5759e-d69f-4c39-8994-f467c279c558
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398202(v=OCS.15)
ms:contentKeyID: 48183451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcb2d422136cf0a421c68ebc2adba50f03c5cc85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435936"
---
# <a name="building-an-edge-and-director-topology-in-lync-server-2013"></a><span data-ttu-id="677fa-103">Erstellen einer Edge- und Director-Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="677fa-103">Building an edge and Director topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="677fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="677fa-104">

<span> </span></span></span>

<span data-ttu-id="677fa-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="677fa-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="677fa-106">Das Erstellen der Topologie umfasst die folgenden Planungs-und Bereitstellungsaufgaben:</span><span class="sxs-lookup"><span data-stu-id="677fa-106">Building the topology involves the following planning and deployment tasks:</span></span>

  - <span data-ttu-id="677fa-107">**Planung**   Sie müssen eine geeignete Topologie für Ihre Organisation definieren und die Komponenten identifizieren, die für die Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="677fa-107">**Planning**   You need to define an appropriate topology for your organization and identify the components required to deploy it.</span></span> <span data-ttu-id="677fa-108">Dies sind die Standardschritte des Planungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="677fa-108">These are standard steps in the planning process.</span></span> <span data-ttu-id="677fa-109">Das mit lync Server 2013 bereitgestellte Planungs Tool für Microsoft lync Server 2013 macht es einfach, den Planungsprozess zu starten, sowie die Möglichkeit, einfach Änderungen vorzunehmen, wenn Ihre Anforderungen und Pläne finalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="677fa-109">The Microsoft Lync Server 2013, Planning Tool provided with Lync Server 2013 makes it easy to start the planning process, as well as including the ability to easily make changes as your requirements and plans are finalized.</span></span>

  - <span data-ttu-id="677fa-110">**Bereitstellung**   Die Topologie, die Sie mit dem Topologie-Generator definieren, ist für die Bereitstellung von lync Server 2013-Servern unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="677fa-110">**Deployment**   The topology that you define using Topology Builder is essential to the deployment of any Lync Server 2013 server.</span></span> <span data-ttu-id="677fa-111">Wenn Sie die Definition und Veröffentlichung Ihrer Topologie mit dem Topologie-Generator im Rahmen ihrer Planungsbemühungen nicht abgeschlossen haben, müssen Sie diese durchführen und die Topologie veröffentlichen, bevor Sie Ihre Edgeserver bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="677fa-111">If you do not finish defining and publishing your topology by using Topology Builder as part of your planning efforts, you must complete it and publish the topology before you deploy your Edge Servers.</span></span>

<span data-ttu-id="677fa-112">Sie können keine Edge-Server-Komponenten bereitstellen, bis Sie mindestens einen internen Pool bereitgestellt haben, und Sie müssen den Topologie-Generator installieren, um einen internen Pool bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="677fa-112">You cannot deploy Edge Server components until you have deployed at least one internal pool, and you must install Topology Builder to deploy an internal pool.</span></span> <span data-ttu-id="677fa-113">In diesem Abschnitt wird die Installation von Topology Builder nicht behandelt, da dies Teil des Installationsvorgangs für den internen Pool ist.</span><span class="sxs-lookup"><span data-stu-id="677fa-113">This section does not cover installation of Topology Builder because that is part of the installation process for the internal pool.</span></span>

<span data-ttu-id="677fa-114">Details zu diesen Tools finden Sie unter [Bereitstellungscheckliste für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="677fa-114">For details about these tools, see [Deployment checklist for external user access in Lync Server 2013](lync-server-2013-deployment-checklist-for-external-user-access.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="677fa-115">Wenn Sie zuvor mithilfe des Topologie-Generators eine vollständige Topologie einschließlich der Edge-Topologie definiert haben, können Sie die <A href="lync-server-2013-define-your-edge-topology.md">Definition ihrer Edge-Topologie in lync Server 2013</A> überspringen und <A href="lync-server-2013-publish-your-topology.md">Ihre Topologie in lync Server 2013</A> -Aufgaben in diesem Abschnitt veröffentlichen, doch müssen Sie den <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export ihrer lync Server 2013-Topologie durchführen und diese in externe Medien für die Edge-Installationsaufgabe kopieren</A> .</span><span class="sxs-lookup"><span data-stu-id="677fa-115">If you previously used Topology Builder to define a complete topology, including the edge topology, you do can skip the <A href="lync-server-2013-define-your-edge-topology.md">Define your edge topology in Lync Server 2013</A> and <A href="lync-server-2013-publish-your-topology.md">Publish your topology in Lync Server 2013</A> tasks in this section, but you do need to complete the <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A> task.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="677fa-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="677fa-116">In This Section</span></span>

  - [<span data-ttu-id="677fa-117">Definieren der Edgetopologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="677fa-117">Define your edge topology in Lync Server 2013</span></span>](lync-server-2013-define-your-edge-topology.md)

  - [<span data-ttu-id="677fa-118">Definieren von optionalen Director-Topologien in einer Topologie für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="677fa-118">Define optional Director topologies in your topology for Lync Server 2013</span></span>](lync-server-2013-define-optional-director-topologies-in-your-topology.md)

  - [<span data-ttu-id="677fa-119">Veröffentlichen der Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="677fa-119">Publish your topology in Lync Server 2013</span></span>](lync-server-2013-publish-your-topology.md)

  - [<span data-ttu-id="677fa-120">Exportieren der Lync Server 2013-Topologie und Kopieren auf externe Medien zur Edgeinstallation</span><span class="sxs-lookup"><span data-stu-id="677fa-120">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)

<span data-ttu-id="677fa-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="677fa-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

