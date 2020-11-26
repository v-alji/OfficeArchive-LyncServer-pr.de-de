---
title: Bereitstellen einer Survivable Branch Appliance oder eines Survivable Branch Servers – Aufgaben am zentralen Standort
description: Bereitstelleneiner Survivable Branch Appliance oder Server-Central-Websiteaufgaben
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a Survivable Branch Appliance or Server - central site tasks
ms:assetid: 0f631a36-fc2e-41cd-8a0d-f27e84f4a89e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398189(v=OCS.15)
ms:contentKeyID: 48183422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4460ea215d6fc80ee89f1ca9bc42f08ac5d14617
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430133"
---
# <a name="deploying-a-survivable-branch-appliance-or-server-with-lync-server-2013---central-site-tasks"></a><span data-ttu-id="82e3e-103">Bereitstellen einer Survivable Branch Appliance oder eines Survivable Branch Servers mit Lync Server 2013 – Aufgaben am zentralen Standort</span><span class="sxs-lookup"><span data-stu-id="82e3e-103">Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="82e3e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="82e3e-104">

<span> </span></span></span>

<span data-ttu-id="82e3e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="82e3e-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="82e3e-106">Führen Sie die Aufgaben in diesem Abschnitt auf der zentralen Website aus.</span><span class="sxs-lookup"><span data-stu-id="82e3e-106">Complete the tasks in this section at the central site.</span></span> <span data-ttu-id="82e3e-107">Wenn Sie einen Überlebenden Verzweigungs Server bereitstellen, überspringen Sie die erste Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="82e3e-107">If you’re deploying a Survivable Branch Server, skip the first task.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="82e3e-108">Bevor Sie die Aufgaben in diesem Abschnitt ausführen, müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="82e3e-108">Before you perform the tasks in this section, the following conditions must be in place:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="82e3e-109">Lync Server muss am zentralen Standort eingerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="82e3e-109">Lync Server must be set up at the central site.</span></span></P>
> <LI>
> <P><span data-ttu-id="82e3e-110">Ein Installationstechniker auf der Zweigstelle muss der RTCUniversalSBATechnicians-Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="82e3e-110">An installation technician at the branch site must be added to the RTCUniversalSBATechnicians group.</span></span></P></LI></UL><span data-ttu-id="82e3e-111">Darüber hinaus empfehlen wir, dass Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="82e3e-111">In addition, we recommend that you do the following:</span></span>
> <UL>
> <LI>
> <P><span data-ttu-id="82e3e-112">Stellen Sie einen DHCP-Server an jeder Verzweigungs Website bereit, damit Clients IP-Adressen abrufen können.</span><span class="sxs-lookup"><span data-stu-id="82e3e-112">Deploy a DHCP server at each branch site to enable clients to obtain IP addresses.</span></span></P>
> <LI>
> <P><span data-ttu-id="82e3e-113">Als Alternative zum Bereitstellen eines DHCP-Servers an jeder Verzweigungs Website aktivieren Sie lync Server DHCP auf der Survivable Branch-Appliance oder dem Überlebenden Verzweigungs Server mithilfe des Cmdlets "lync Server-Verwaltungsshell" <STRONG>-Cmdlet-CsRegistrarConfiguration – EnableDHCPServer $true</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="82e3e-113">As an alternative to deploying a DHCP server at each branch site, enable Lync Server DHCP on the Survivable Branch Appliance or Survivable Branch Server by using the Lync Server Management Shell cmdlet <STRONG>Set-CsRegistrarConfiguration –EnableDHCPServer $true</STRONG>.</span></span> <span data-ttu-id="82e3e-114">Ausführliche Informationen finden Sie im Abschnitt "Hardware-und Software Anforderungen" in der Planning-Dokumentation unter den Anforderungen an die <A href="lync-server-2013-branch-site-resiliency-requirements.md">Stabilität der Zweigstelle für lync Server 2013</A> .</span><span class="sxs-lookup"><span data-stu-id="82e3e-114">For details, see the “Hardware and Software Requirements” section of <A href="lync-server-2013-branch-site-resiliency-requirements.md">Branch-site resiliency requirements for Lync Server 2013</A> in the Planning documentation.</span></span></P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="82e3e-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="82e3e-115">In This Section</span></span>

  - [<span data-ttu-id="82e3e-116">Hinzufügen einer Survivable Branch Appliance zu Active Directory in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82e3e-116">Add a Survivable Branch Appliance to Active Directory in Lync Server 2013</span></span>](lync-server-2013-add-a-survivable-branch-appliance-to-active-directory.md)

  - [<span data-ttu-id="82e3e-117">Hinzufügen von Zweigstellenstandorten zur Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82e3e-117">Add branch sites to your topology in Lync Server 2013</span></span>](lync-server-2013-add-branch-sites-to-your-topology.md)

  - [<span data-ttu-id="82e3e-118">Definieren einer Survivable Branch Appliance oder eines Survivable Branch Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="82e3e-118">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)

<span data-ttu-id="82e3e-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="82e3e-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

