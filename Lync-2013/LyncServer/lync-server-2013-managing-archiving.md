---
title: 'Lync Server 2013: Verwalten der Archivierung'
description: 'Lync Server 2013: Verwalten der Archivierung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013 Archiving
ms:assetid: 48c6cc8c-c2c1-4534-9a8a-fd5eb738076a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520990(v=OCS.15)
ms:contentKeyID: 48184003
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c7010645f36a7144ea508447d2c628bc8feacb0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425976"
---
# <a name="managing-lync-server-2013-archiving"></a><span data-ttu-id="0311d-103">Verwalten der Lync Server 2013-Archivierung</span><span class="sxs-lookup"><span data-stu-id="0311d-103">Managing Lync Server 2013 Archiving</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0311d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0311d-104">

<span> </span></span></span>

<span data-ttu-id="0311d-105">_**Letztes Änderungsdatum des Themas:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="0311d-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="0311d-106">Wenn Sie die Archivierung für Ihre Organisation bereitstellen, geben Sie die anfängliche Konfiguration während der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="0311d-106">When you deploy Archiving for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="0311d-107">Es kann jedoch vorkommen, dass Sie ändern möchten, wie Sie die Archivierungsunterstützung für das tägliche Management implementieren oder neue Anforderungen in Ihrer Organisation erfüllen möchten.</span><span class="sxs-lookup"><span data-stu-id="0311d-107">However, there may be times when you want to change how you implement archiving support for day-to-day management or to meet new requirements in your organization.</span></span> <span data-ttu-id="0311d-108">Möglicherweise müssen Sie den Archivierungs Support für eine bestimmte Website, einen Pool oder für Benutzer in Ihrer Organisation anders einrichten.</span><span class="sxs-lookup"><span data-stu-id="0311d-108">For example, you may need to set up archiving support differently for a specific site, pool, or users within your organization.</span></span> <span data-ttu-id="0311d-109">Für Benutzer, die in lync Server 2013 verwaltet werden, erstellen und Anpassen Sie Archivierungsrichtlinien und-Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0311d-109">For users homed on Lync Server 2013, you do this be creating and customizing archiving policies and configurations.</span></span> <span data-ttu-id="0311d-110">Wenn Sie die Microsoft Exchange-Integration verwenden, müssen Sie auch die Exchange 2013-Einstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0311d-110">If you use Microsoft Exchange integration, you must also configure Exchange 2013 settings.</span></span> <span data-ttu-id="0311d-111">Dieser Abschnitt enthält Informationen und Verfahren, mit denen Sie Änderungen an ihrer Archivierungs Bereitstellung vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="0311d-111">This section provides information and procedures to enable you to make changes to your Archiving deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0311d-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0311d-112">In This Section</span></span>

  - [<span data-ttu-id="0311d-113">Funktionsweise der Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0311d-113">How Archiving works in Lync Server 2013</span></span>](lync-server-2013-how-archiving-works.md)

  - [<span data-ttu-id="0311d-114">Verwalten der Archivierung interner und externer Kommunikation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0311d-114">Managing the Archiving of internal and external communications in Lync Server 2013</span></span>](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)

  - [<span data-ttu-id="0311d-115">Verwalten von Archivierungs Konfigurationsoptionen in lync Server 2013 für Ihre Organisation, ihre Websites und Pools</span><span class="sxs-lookup"><span data-stu-id="0311d-115">Managing Archiving configuration options in Lync Server 2013 for your organization, sites, and pools</span></span>](lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md)

  - [<span data-ttu-id="0311d-116">Ändern der Optionen für die Archivierungsdatenbank in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0311d-116">Changing Archiving database options in Lync Server 2013</span></span>](lync-server-2013-changing-archiving-database-options.md)

  - [<span data-ttu-id="0311d-117">Exportieren von archivierten Daten aus lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0311d-117">Exporting archived data from Lync Server 2013</span></span>](lync-server-2013-exporting-archived-data.md)

<span data-ttu-id="0311d-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0311d-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

