---
title: Voraussetzungen für Gruppenanruf-Pickup-Konfiguration und Benutzerrechte
description: Voraussetzungen für Gruppenanruf-Abholung und Benutzerrechte
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427873"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="556e6-103">Voraussetzungen für Gruppenanruf-Pickup-Konfiguration und Benutzerrechte in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="556e6-103">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="556e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="556e6-104">

<span> </span></span></span>

<span data-ttu-id="556e6-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="556e6-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="556e6-106">Bei der Gruppenanruf Abholung handelt es sich um ein Anruf Verwaltungsfeature, das standardmäßig bei der Bereitstellung von Enterprise-VoIP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="556e6-106">Group Call Pickup is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="556e6-107">In diesem Thema wird beschrieben, was Sie benötigen, bevor Sie die Gruppenanruf Abholung und die Benutzerrechte konfigurieren können, die Sie zum Ausführen von Konfigurationsaufgaben benötigen.</span><span class="sxs-lookup"><span data-stu-id="556e6-107">This topic describes what you need to have in place before you can configure Group Call Pickup and the user rights that you need to perform configuration tasks.</span></span>

<span data-ttu-id="556e6-108">In diesem Abschnitt wird davon ausgegangen, dass Sie die Planungsdokumentation gelesen haben, die sich auf die Gruppenanruf Abholung bezieht (siehe [Planen der Gruppenanruf Abholung in lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span><span class="sxs-lookup"><span data-stu-id="556e6-108">This section assumes that you have read the planning documentation related to Group Call Pickup (see [Planning for Group Call Pickup in Lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).</span></span>

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a><span data-ttu-id="556e6-109">Voraussetzungen für Gruppenanruf-Pickup-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="556e6-109">Group Call Pickup Configuration Prerequisites</span></span>

<span data-ttu-id="556e6-110">Für die Gruppenanruf Abholung sind die folgenden Komponenten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="556e6-110">Group Call Pickup requires the following components:</span></span>

  - <span data-ttu-id="556e6-111">Anwendungsdienst</span><span class="sxs-lookup"><span data-stu-id="556e6-111">Application service</span></span>

  - <span data-ttu-id="556e6-112">Anwendung zum Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="556e6-112">Call Park application</span></span>

<span data-ttu-id="556e6-113">Diese Komponenten werden automatisch installiert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="556e6-113">These components are installed automatically when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a><span data-ttu-id="556e6-114">Benutzerrechte für Gruppenanruf-Pickup-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="556e6-114">Group Call Pickup Configuration User Rights</span></span>

<span data-ttu-id="556e6-115">Sie verwenden die folgenden Verwaltungstools, um die Gruppenanruf Abholung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="556e6-115">You use the following administrative tools to configure Group Call Pickup:</span></span>

  - <span data-ttu-id="556e6-116">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="556e6-116">Lync Server Management Shell</span></span>

  - <span data-ttu-id="556e6-117">SEFAUtil Resource Kit-Tool</span><span class="sxs-lookup"><span data-stu-id="556e6-117">SEFAUtil resource kit tool</span></span>

<span data-ttu-id="556e6-118">Verwenden Sie die lync Server-Verwaltungsshell zum Erstellen und Verwalten von Anruf-Abhol Gruppen in der Orbit-Tabelle des Anruf Parks.</span><span class="sxs-lookup"><span data-stu-id="556e6-118">Use Lync Server Management Shell to create and manage call pickup groups in the Call Park orbit table.</span></span> <span data-ttu-id="556e6-119">Verwenden Sie das SEFAUtil Resource Kit-Tool, um eine Anruf Abhol Gruppe zuzuweisen und die Gruppenanruf Abholung für Benutzer zu aktivieren oder die Gruppenanruf Abholung für Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="556e6-119">Use the SEFAUtil resource kit tool to assign a call pickup group and enable Group Call Pickup for users or to disable Group Call Pickup for users.</span></span>

<span data-ttu-id="556e6-120">Die Konfiguration der Gruppenanruf Abholung erfordert je nach Aufgabe eine der folgenden Administratorrollen:</span><span class="sxs-lookup"><span data-stu-id="556e6-120">Configuring Group Call Pickup requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="556e6-121">**CsVoiceAdministrator:** Diese Administratorrolle kann alle sprachbezogenen Einstellungen und Richtlinien erstellen, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="556e6-121">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="556e6-122">**CsUserAdministrator:** Mit dieser Administratorrolle kann die Gruppenanruf Abholung für Benutzer aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="556e6-122">**CsUserAdministrator:** This administrator role can enable Group Call Pickup for users.</span></span> <span data-ttu-id="556e6-123">Diese Administratorrolle verfügt auch über die schreibgeschützte Ansicht Zugriff auf alle Sprachkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="556e6-123">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="556e6-124">**CsServerAdministrator:** Diese Administratorrolle kann Server und Dienste verwalten, überwachen und Problembehandlung durchführen.</span><span class="sxs-lookup"><span data-stu-id="556e6-124">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="556e6-125">**CsAdministrator:** Diese Administratorrolle kann alle Aufgaben von CsVoiceAdministrator, CsServerAdministrator und CsUserAdministrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="556e6-125">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="556e6-126">Details zu Administratorrechten finden Sie unter <A href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="556e6-126">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="556e6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="556e6-127">See Also</span></span>


[<span data-ttu-id="556e6-128">Bereitstellen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="556e6-128">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="556e6-129">Planen der Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="556e6-129">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="556e6-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="556e6-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

