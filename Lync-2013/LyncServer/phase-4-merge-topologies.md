---
title: 'Phase 4: Zusammenführen von Topologien'
description: 'Phase 4: Zusammenführen von Topologien'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 4: Merge topologies'
ms:assetid: 81eb5bb2-1fd7-4611-a2aa-eb2393c8abc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205044(v=OCS.15)
ms:contentKeyID: 48184668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 421cb83a57979ae677d4db76d2c8c3535f8e0dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438764"
---
# <a name="phase-4-merge-topologies"></a><span data-ttu-id="4a174-103">Phase 4: Zusammenführen von Topologien</span><span class="sxs-lookup"><span data-stu-id="4a174-103">Phase 4: Merge topologies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4a174-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4a174-104">

<span> </span></span></span>

<span data-ttu-id="4a174-105">_**Letztes Änderungsdatum des Themas:** 2012-03-29_</span><span class="sxs-lookup"><span data-stu-id="4a174-105">_**Topic Last Modified:** 2012-03-29_</span></span>

<span data-ttu-id="4a174-106">Die folgenden Themen enthalten eine Übersicht über die erforderlichen Schritte zum Zusammenführen Ihrer Microsoft Office Communications Server 2007 R2-Pools mit Microsoft lync Server 2013-Pools.</span><span class="sxs-lookup"><span data-stu-id="4a174-106">The following topics outline the steps needed to merge your Microsoft Office Communications Server 2007 R2 pools to Microsoft Lync Server 2013 pools.</span></span> <span data-ttu-id="4a174-107">Zunächst verwenden Sie den Zusammenführungs-Assistenten des Topologie-Generators zum Zusammenführen von Topologieinformationen.</span><span class="sxs-lookup"><span data-stu-id="4a174-107">First, you use the Topology Builder Merge wizard to merge topology information.</span></span> <span data-ttu-id="4a174-108">Dieses Tool sammelt Informationen zu Ihrer Office Communications Server 2007 R2-Umgebung, einschließlich Edgeserver-Informationen, und veröffentlicht diese Informationen in einer mit lync Server 2013 freigegebenen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="4a174-108">This tool collects information about your Office Communications Server 2007 R2 environment, including Edge Server information, and publishes that information to a database shared with Lync Server 2013.</span></span> <span data-ttu-id="4a174-109">Nachdem Sie die zusammengeführte Topologie veröffentlicht haben, wird der Topologie-Generator verwendet, um die Informationen zur Topologie von Office Communications Server 2007 R2 und Informationen zur neu bereitgestellten lync Server 2013-Topologie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a174-109">After you publish the merged topology, Topology Builder is used to view the Office Communications Server 2007 R2 topology information and information about the newly deployed Lync Server 2013 topology.</span></span> <span data-ttu-id="4a174-110">Schließlich verwenden Sie Cmdlets der lync Server-Verwaltungsshell zum Importieren von Richtlinien und Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="4a174-110">Finally, you use Lync Server Management Shell cmdlets to import policies and configuration settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4a174-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4a174-111">In This Section</span></span>

  - [<span data-ttu-id="4a174-112">Installieren des WMI-abwärts Kompatibilitätspakets</span><span class="sxs-lookup"><span data-stu-id="4a174-112">Install WMI Backward Compatibility package</span></span>](install-wmi-backward-compatibility-package.md)

  - [<span data-ttu-id="4a174-113">Zusammenführen mit dem Zusammenführungs-Assistenten für Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="4a174-113">Merge using Topology Builder Merge wizard</span></span>](merge-using-topology-builder-merge-wizard.md)

  - [<span data-ttu-id="4a174-114">Importieren von Richtlinien und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="4a174-114">Import policies and settings</span></span>](import-policies-and-settings.md)

  - [<span data-ttu-id="4a174-115">Überprüfen von Topologieinformationen</span><span class="sxs-lookup"><span data-stu-id="4a174-115">Verify topology information</span></span>](verify-topology-information.md)

<span data-ttu-id="4a174-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4a174-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

