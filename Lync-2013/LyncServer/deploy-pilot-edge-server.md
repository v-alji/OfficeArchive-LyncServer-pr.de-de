---
title: Bereitstellen eines Pilot-Edgeservers
description: Bereitstellen des Pilot Edge-Servers
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Deploy pilot Edge Server
ms:assetid: dab345c0-8577-4c11-ac73-fe8b2a75f4cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205306(v=OCS.15)
ms:contentKeyID: 48185559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d63e9255ad448995fcafa05fed12e97ea151736b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394395"
---
# <a name="deploy-pilot-edge-server"></a><span data-ttu-id="bc908-103">Bereitstellen eines Pilot-Edgeservers</span><span class="sxs-lookup"><span data-stu-id="bc908-103">Deploy pilot Edge Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc908-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc908-104">

<span> </span></span></span>

<span data-ttu-id="bc908-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="bc908-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="bc908-106">In diesem Thema werden die Konfigurationseinstellungen hervorgehoben, die Sie vor der Bereitstellung Ihres lync Server 2013-Edgeserver beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="bc908-106">This topic highlights configuration settings you should be aware of prior to deploying your Lync Server 2013 Edge Server.</span></span> <span data-ttu-id="bc908-107">Die Bereitstellungs-und Konfigurationsprozesse für lync Server 2013 sind mit lync Server 2010 sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="bc908-107">The deployment and configuration processes for Lync Server 2013 are very similar to Lync Server 2010.</span></span> <span data-ttu-id="bc908-108">In diesem Abschnitt werden nur wichtige Punkte hervorgehoben, die Sie im Rahmen der Bereitstellung des pilotpools berücksichtigen sollten.</span><span class="sxs-lookup"><span data-stu-id="bc908-108">This section only highlights key points you should consider as part of your pilot pool deployment.</span></span> <span data-ttu-id="bc908-109">Detaillierte Anweisungen finden Sie unter [Bereitstellen des Zugriffs auf externe Benutzer in lync Server 2013](lync-server-2013-deploying-external-user-access.md) in der Bereitstellungsdokumentation, in der der Bereitstellungsprozess beschrieben wird, sowie Konfigurationsinformationen für den Zugriff durch externe Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bc908-109">For detailed steps, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation, which describes the deployment process and also gives configuration information for external user access.</span></span>

<span data-ttu-id="bc908-110">Wenn Sie im Assistenten zum **Definieren eines neuen Edge-Pools** navigieren, überprüfen Sie die wichtigsten Konfigurationseinstellungen, die in den folgenden Schritten gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc908-110">As you navigate through the **Define New Edge Pool** wizard, review the key configuration settings shown in the following steps.</span></span> <span data-ttu-id="bc908-111">Beachten Sie, dass nur wenige Seiten des Assistenten zum **Definieren eines neuen Edge-Pools** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bc908-111">Note that only a few pages of the **Define New Edge Pool** wizard are shown.</span></span>

<span data-ttu-id="bc908-112">**Definieren eines Edge-Pools**</span><span class="sxs-lookup"><span data-stu-id="bc908-112">**Define an Edge Pool**</span></span>

1.  <span data-ttu-id="bc908-113">Melden Sie sich auf dem Computer, auf dem der Topologie-Generator installiert ist, als Mitglied der Gruppe "Domänen-Admins" oder "RTCUniversalServerAdmins" an.</span><span class="sxs-lookup"><span data-stu-id="bc908-113">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="bc908-114">Navigieren Sie zum lync Server 2013-Knoten.</span><span class="sxs-lookup"><span data-stu-id="bc908-114">Navigate to the Lync Server 2013 node.</span></span> <span data-ttu-id="bc908-115">Klicken Sie mit der rechten Maustaste auf **Edge-Pools**, und klicken Sie auf **neuer Edge-Pool**.</span><span class="sxs-lookup"><span data-stu-id="bc908-115">Right-click **Edge pools**, and click **New Edge pool**.</span></span>
    
    <span data-ttu-id="bc908-116">![Dialogfeld ' neuen Edge-Pool definieren '](images/JJ205306.a90d388c-49ff-4620-a19d-42e2f1bb559c(OCS.15).jpg "Dialogfeld ' neuen Edge-Pool definieren '")</span><span class="sxs-lookup"><span data-stu-id="bc908-116">![Define the New Edge Pool dialog box](images/JJ205306.a90d388c-49ff-4620-a19d-42e2f1bb559c(OCS.15).jpg "Define the New Edge Pool dialog box")</span></span>

3.  <span data-ttu-id="bc908-117">Ein Edge-Pool kann ein Pool mit **mehreren Computern** oder ein **einzelner Computerpool** sein.</span><span class="sxs-lookup"><span data-stu-id="bc908-117">An Edge pool can be a **Multiple computer pool** or **Single computer pool**.</span></span>
    
    <span data-ttu-id="bc908-118">![Definieren des Dialogfelds "FQDN des Edge-Pools"](images/JJ205306.4904fe8f-537c-4e66-a399-1bd8a316dc10(OCS.15).jpg "Definieren des Dialogfelds "FQDN des Edge-Pools"")</span><span class="sxs-lookup"><span data-stu-id="bc908-118">![Define the Edge Pool FQDN dialog box](images/JJ205306.4904fe8f-537c-4e66-a399-1bd8a316dc10(OCS.15).jpg "Define the Edge Pool FQDN dialog box")</span></span>

4.  <span data-ttu-id="bc908-119">Aktivieren Sie auf der Seite **"Features auswählen** " die Föderation oder den XMPP-Verbund nicht.</span><span class="sxs-lookup"><span data-stu-id="bc908-119">On the **Select features** page, do not enable federation or XMPP federation.</span></span> <span data-ttu-id="bc908-120">Föderation und XMPP-Föderation sind beide derzeit über den Legacy-Edgeserver von lync Server 2010 weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc908-120">Federation and XMPP federation are both currently routed through the legacy Lync Server 2010 Edge Server.</span></span> <span data-ttu-id="bc908-121">Diese Features werden in einer späteren Migrationsphase konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bc908-121">These features will be configured in a later phase of migration.</span></span>
    
    <span data-ttu-id="bc908-122">![Dialogfeld ' Features auswählen '](images/JJ205306.cb0b45a4-2856-45ba-bd97-e49fafbb077e(OCS.15).jpg "Dialogfeld ' Features auswählen '")</span><span class="sxs-lookup"><span data-stu-id="bc908-122">![Select Features dialog box](images/JJ205306.cb0b45a4-2856-45ba-bd97-e49fafbb077e(OCS.15).jpg "Select Features dialog box")</span></span>

5.  <span data-ttu-id="bc908-123">Führen Sie als nächstes die folgenden Assistentenseiten aus: **externe FQDNs**, **definieren Sie die interne IP-Adresse**, und definieren Sie **die externe IP-Adresse**.</span><span class="sxs-lookup"><span data-stu-id="bc908-123">Next, continue completing the following wizard pages: **External FQDNs**, **Define the internal IP address**, and **Define the external IP address**.</span></span>

6.  <span data-ttu-id="bc908-124">Wählen Sie auf der Seite **Nächster Hop definieren** den Director für den nächsten Hop des lync Server 2010-Edge-Pools aus.</span><span class="sxs-lookup"><span data-stu-id="bc908-124">On the **Define the next hop** page, select the Director for the next hop of the Lync Server 2010 Edge pool.</span></span>
    
    <span data-ttu-id="bc908-125">![Dialogfeld ' nächster Hop definieren '](images/JJ205306.11baf3ea-74f5-4eb7-8650-b03b3b190416(OCS.15).jpg "Dialogfeld ' nächster Hop definieren '")</span><span class="sxs-lookup"><span data-stu-id="bc908-125">![Define the Next Hop dialog box](images/JJ205306.11baf3ea-74f5-4eb7-8650-b03b3b190416(OCS.15).jpg "Define the Next Hop dialog box")</span></span>

7.  <span data-ttu-id="bc908-126">Verbinden Sie auf der Seite **Front-End-oder Mediations Pools zuordnen** keinen Pool mit diesem Edge-Pool zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="bc908-126">On the **Associate Front End or Mediation pools** page, do not associate a pool with this Edge pool at this time.</span></span> <span data-ttu-id="bc908-127">Der externe Mediendatenverkehr wird derzeit über den Legacy-Edgeserver von lync Server 2010 weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="bc908-127">External media traffic is currently routed through the legacy Lync Server 2010 Edge Server.</span></span> <span data-ttu-id="bc908-128">Diese Einstellung wird in einer späteren Migrationsphase konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bc908-128">This setting will be configured in a later phase of migration.</span></span>
    
    <span data-ttu-id="bc908-129">![Dialogfeld ' Front-End-Pools zuordnen '](images/JJ205306.fe0da887-7b51-4564-afc5-d57da95a2eb6(OCS.15).jpg "Dialogfeld ' Front-End-Pools zuordnen '")</span><span class="sxs-lookup"><span data-stu-id="bc908-129">![Associate Front End Pools dialog box](images/JJ205306.fe0da887-7b51-4564-afc5-d57da95a2eb6(OCS.15).jpg "Associate Front End Pools dialog box")</span></span>

8.  <span data-ttu-id="bc908-130">Klicken Sie auf **Fertig stellen** , und **veröffentlichen** Sie die Topologie.</span><span class="sxs-lookup"><span data-stu-id="bc908-130">Click **Finish** and then **Publish** the topology.</span></span>

9.  <span data-ttu-id="bc908-131">Führen Sie die Schritte unter [Installieren von Edge-Servern für lync Server 2013](lync-server-2013-install-edge-servers.md) in der Bereitstellungsdokumentation aus, um die Dateien auf dem neuen Edgeserver zu installieren, Zertifikate zu konfigurieren und die Dienste zu starten.</span><span class="sxs-lookup"><span data-stu-id="bc908-131">Follow the steps in [Install Edge Servers for Lync Server 2013](lync-server-2013-install-edge-servers.md) in the Deployment documentation to install the files on the new Edge Server, configure certificates, and start the services.</span></span>

<span data-ttu-id="bc908-132">Es ist sehr wichtig, dass Sie die Richtlinien in den Themen zum [Bereitstellen des Zugriffs externer Benutzer in lync Server 2013](lync-server-2013-deploying-external-user-access.md) in der Bereitstellungsdokumentation befolgen.</span><span class="sxs-lookup"><span data-stu-id="bc908-132">It’s very important that you follow the guidelines in the topics [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span> <span data-ttu-id="bc908-133">Dieser Abschnitt enthält lediglich einige Anleitungen zu Konfigurationseinstellungen beim Installieren dieser Serverrollen.</span><span class="sxs-lookup"><span data-stu-id="bc908-133">This section merely provided some guidance on configuration settings when installing these server roles.</span></span>

<span data-ttu-id="bc908-134">Sie sollten jetzt einen Legacy-lync Server 2010-Edgeserver parallel zu einer lync Server 2013-Edgeserver-Bereitstellung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bc908-134">You should now have a legacy Lync Server 2010 Edge Server deployed in parallel with a Lync Server 2013 Edge server deployment.</span></span> <span data-ttu-id="bc908-135">Überprüfen Sie, ob beide Bereitstellungen ordnungsgemäß ausgeführt werden, Dienste gestartet sind, und Sie können jede Bereitstellung verwalten, bevor Sie in die nächste Phase wechseln.</span><span class="sxs-lookup"><span data-stu-id="bc908-135">Verify that both deployments are running properly, services are started, and you can administer each deployment prior to moving to the next phase.</span></span>

<span data-ttu-id="bc908-136"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc908-136"></div>

<span> </span>

</div>

</div>

</span></span></div>

