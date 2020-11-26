---
title: 'Lync Server 2013: Sichern von Archivierungs-und Überwachungsdatenbanken'
description: 'Lync Server 2013: Sichern von Archivierungs-und Überwachungsdatenbanken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Archiving and Monitoring databases
ms:assetid: c120db81-b02c-4a4c-90cd-8aca6cff64f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202188(v=OCS.15)
ms:contentKeyID: 51541515
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49b4fa194bffa27a52f32d61a729eeaa31cc0ad3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438120"
---
# <a name="backing-up-archiving-and-monitoring-databases-in-lync-server-2013"></a><span data-ttu-id="b3594-103">Sichern von Archivierungs-und Überwachungsdatenbanken in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3594-103">Backing up Archiving and Monitoring databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3594-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3594-104">

<span> </span></span></span>

<span data-ttu-id="b3594-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="b3594-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="b3594-106">Wenn Sie die Archivierung oder Überwachung bereitgestellt haben, müssen Sie diese Datenbanken entsprechend der SQL Server-Sicherungsrichtlinie Ihrer Organisation sichern.</span><span class="sxs-lookup"><span data-stu-id="b3594-106">If you deployed Archiving or Monitoring, you need to back up these databases according to your organization's SQL Server backup policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b3594-107">Die Einstellungen für Archivierung und Überwachung werden beim Sichern des zentralen Verwaltungsspeichers gesichert.</span><span class="sxs-lookup"><span data-stu-id="b3594-107">The settings for Archiving and Monitoring are backed up when you back up the Central Management store.</span></span> <span data-ttu-id="b3594-108">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-backing-up-core-data-and-settings.md">Sichern von Core-Daten und-Einstellungen in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="b3594-108">For details, see <A href="lync-server-2013-backing-up-core-data-and-settings.md">Backing up core data and settings in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="b3594-109">Zum Archivieren und überwachen können Sie ein SQL Server-Tool wie SQL Server Management Studio verwenden, um eine manuelle Sicherung durchzuführen, oder Sie können die SQL Server-Verwaltungstools verwenden, um reguläre automatische Sicherungen zu planen.</span><span class="sxs-lookup"><span data-stu-id="b3594-109">For Archiving and Monitoring, you can use a SQL Server tool such as SQL Server Management Studio to perform a manual backup, or you can use SQL Server management tools to schedule regular, automatic backups.</span></span>

<span data-ttu-id="b3594-110"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3594-110"></div>

<span> </span>

</div>

</div>

</span></span></div>

