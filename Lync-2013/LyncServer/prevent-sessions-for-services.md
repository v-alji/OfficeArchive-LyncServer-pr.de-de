---
title: Verhindern von Sitzungen für Dienste
description: Verhindern von Sitzungen für Dienste
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Prevent sessions for services
ms:assetid: 4b541c72-cdc1-4f86-a5a8-c43c24f41d8b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688049(v=OCS.15)
ms:contentKeyID: 49733642
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a452f8091716daa0a15967e2a278e82c5bc8c4f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438463"
---
# <a name="prevent-sessions-for-services"></a><span data-ttu-id="64eaa-103">Verhindern von Sitzungen für Dienste</span><span class="sxs-lookup"><span data-stu-id="64eaa-103">Prevent sessions for services</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64eaa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64eaa-104">

<span> </span></span></span>

<span data-ttu-id="64eaa-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="64eaa-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="64eaa-106">Sie können die Systemsteuerung von Microsoft lync Server 2010 verwenden, um neue Sitzungen für alle lync Server 2010-Dienste zu verhindern, die auf einem bestimmten Computer ausgeführt werden, oder um neue Sitzungen für einen bestimmten lync Server 2010-Dienst zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="64eaa-106">You can use Microsoft Lync Server 2010 Control Panel to prevent new sessions for all the Lync Server 2010 services running on a specific computer or to prevent new sessions for a specific Lync Server 2010 service.</span></span>

<div>

## <a name="to-prevent-new-sessions-for-all-lync-server-services-on-a-computer"></a><span data-ttu-id="64eaa-107">So verhindern Sie, dass neue Sitzungen für alle lync Server-Dienste auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="64eaa-107">To prevent new sessions for all Lync Server services on a computer</span></span>

1.  <span data-ttu-id="64eaa-108">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="64eaa-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="64eaa-109">Öffnen Sie die Lync Server-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="64eaa-109">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="64eaa-110">Klicken Sie in der linken Navigationsleiste auf **Topologie** und dann auf **Status**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-110">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="64eaa-111">Sortieren oder Durchsuchen Sie auf der **Status** Seite die Liste nach Bedarf, um den Computer zu finden, auf dem die Dienste ausgeführt werden, für die Sie neue Sitzungen verhindern möchten, und klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="64eaa-111">On the **Status** page, sort or search through the list as needed to find the computer that is running the services for which you want to prevent new sessions, and then click it.</span></span>

5.  <span data-ttu-id="64eaa-112">Klicken Sie auf **Aktion**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-112">Click **Action**.</span></span>

6.  <span data-ttu-id="64eaa-113">Klicken Sie auf **neue Sitzungen für alle Dienste verhindern**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-113">Click **Prevent new sessions for all services**.</span></span>

</div>

<div>

## <a name="to-prevent-new-sessions-for-a-specific-service"></a><span data-ttu-id="64eaa-114">So verhindern Sie neue Sitzungen für einen bestimmten Dienst</span><span class="sxs-lookup"><span data-stu-id="64eaa-114">To prevent new sessions for a specific service</span></span>

1.  <span data-ttu-id="64eaa-115">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="64eaa-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="64eaa-116">Öffnen Sie die Lync Server-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="64eaa-116">Open Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="64eaa-117">Klicken Sie in der linken Navigationsleiste auf **Topologie** und dann auf **Status**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-117">In the left navigation bar, click **Topology** and then click **Status**.</span></span>

4.  <span data-ttu-id="64eaa-118">Sortieren oder Durchsuchen Sie auf der **Status** Seite die Liste nach Bedarf, um den Computer zu finden, auf dem der Dienst ausgeführt wird, den Sie starten oder beenden möchten, und klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="64eaa-118">On the **Status** page, sort or search through the list as needed to find the computer that is running the service you want to start or stop, and then click it.</span></span>

5.  <span data-ttu-id="64eaa-119">Klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-119">Click **Properties**.</span></span>

6.  <span data-ttu-id="64eaa-120">Sortieren Sie die Liste der Dienste, falls erforderlich, und klicken Sie auf den Dienst, für den Sie neue Sitzungen verhindern möchten.</span><span class="sxs-lookup"><span data-stu-id="64eaa-120">Sort the list of services, if necessary, and click the service for which you want to prevent new sessions.</span></span>

7.  <span data-ttu-id="64eaa-121">Klicken Sie auf **Aktion**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-121">Click **Action**.</span></span>

8.  <span data-ttu-id="64eaa-122">Klicken Sie auf **neue Sitzungen für Dienst verhindern**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-122">Click **Prevent new sessions for service**.</span></span>

9.  <span data-ttu-id="64eaa-123">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="64eaa-123">Click **Close**.</span></span>

<span data-ttu-id="64eaa-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64eaa-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

