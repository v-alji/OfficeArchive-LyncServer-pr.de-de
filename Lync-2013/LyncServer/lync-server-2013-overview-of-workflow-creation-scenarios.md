---
title: 'Lync Server 2013: Übersicht über Szenarios zur Erstellung von Workflows'
description: 'Lync Server 2013: Übersicht über Workflow Erstellungs Szenarien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of workflow creation scenarios
ms:assetid: 05e0c175-0f1a-4bb1-b048-c68584d00649
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204646(v=OCS.15)
ms:contentKeyID: 48183309
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a38627e7abb058be2050c0db0b46fa06dfd75287
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437168"
---
# <a name="overview-of-workflow-creation-scenarios-in-lync-server-2013"></a><span data-ttu-id="aad72-103">Übersicht über Szenarios zur Erstellung von Workflows in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aad72-103">Overview of workflow creation scenarios in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aad72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aad72-104">

<span> </span></span></span>

<span data-ttu-id="aad72-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="aad72-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="aad72-106">Beim Erstellen von Workflows stehen zwei mögliche Szenarien zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="aad72-106">When you create workflows, there are two possible scenarios:</span></span>

  - <span data-ttu-id="aad72-107">**Der Administrator erstellt und konfiguriert den Workflow**: Das Mitglied der Rolle „CsResponseGroupAdministrator“ (oder einer gleichwertigen Rolle) erstellt und aktiviert den Workflow und alle Elemente im Workflow, z. B. die Agentgruppen, Warteschleifen, Feiertage und Geschäftszeiten, Wartemusik usw.</span><span class="sxs-lookup"><span data-stu-id="aad72-107">**The Administrator creates and configures the workflow** — The CsResponseGroupAdministrator role member (or equivalent) creates and activates the workflow and all elements in the workflow, such as the agent groups, queues, holiday and business hours, music on hold, and so on.</span></span>

  - <span data-ttu-id="aad72-p101">**Der Administrator erstellt den Workflow und der Manager konfiguriert die Optionen**: Das Mitglied der Rolle „CsResponseGroupAdministrator“ (oder einer gleichwertigen Rolle) definiert den primären SIP-URI und den Anzeigenamen, weist Mitglieder der Rolle „CsResponseGroupManager“ zu, wählt eine Warteschleife aus und aktiviert den Workflow. Das CsResponseGroupManager-Mitglied kann sich dann anmelden und die Konfiguration des Workflows bearbeiten, indem es Agentgruppen erstellt und die Gruppe ebenfalls der Warteschleife zuweist und die Telefonnummer, Feiertage und Geschäftszeiten, Wartemusik usw. konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="aad72-p101">**The Administrator creates the workflow and the Manager configures options** — The CsResponseGroupAdministrator role member (or equivalent) defines the primary SIP URI, Display Name, assigns a member or members of the CsResponseGroupManager role, and selects a queue and activates the workflow. The CsResponseGroupManager can then log on and edit the configuration of the workflow by creating agent groups and also assigns the group to the queue, configuring the telephone number, holiday and business hours, music on hold, and so on.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="aad72-p102">Wenn Sie einen verwalteten Workflow erstellen möchten, müssen Sie den Workflow als aktiv erstellen. Nach dem Speichern eines aktiven, verwalteten Workflows können Sie den Workflow ändern und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="aad72-p102">When you want to create a managed workflow, you need to create the workflow as active. After you save an active, managed workflow, you can then modify and deactivate the workflow.</span></span>

    
    <span data-ttu-id="aad72-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aad72-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

