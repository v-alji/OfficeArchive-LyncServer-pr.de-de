---
title: 'Lync Server 2013: von der Gruppenanruf Abholung verwendete Komponenten'
description: 'Lync Server 2013: von der Gruppenanruf Abholung verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394210"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="42908-103">Von der Gruppenanruf Abholung in lync Server 2013 verwendete Komponenten</span><span class="sxs-lookup"><span data-stu-id="42908-103">Components used by Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42908-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42908-104">

<span> </span></span></span>

<span data-ttu-id="42908-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="42908-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="42908-106">Die Gruppenanruf Abholung wird automatisch bereitgestellt, wenn Sie Enterprise-VoIP und die Anwendung für den Anruf Park bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="42908-106">Group Call Pickup is automatically deployed when you deploy Enterprise Voice and the Call Park application.</span></span> <span data-ttu-id="42908-107">Sie aktivieren die Abholung von Gruppen anrufen, indem Sie die Umlaufbahn Tabelle des Anruf Parks mit getrennten Nummernbereichen konfigurieren, die als Gruppennummern für die Anruf Abholung bestimmt sind, und dann durch Zuweisen von Benutzern zum Anrufen von Abhol Gruppen und zum Aktivieren der Gruppenanruf Abholung.</span><span class="sxs-lookup"><span data-stu-id="42908-107">You enable Group Call Pickup by configuring the Call Park orbit table with separate ranges of numbers designated as call pickup group numbers, and then by assigning users to call pickup groups and enabling the users for Group Call Pickup.</span></span> <span data-ttu-id="42908-108">Die folgenden lync Server-Komponenten unterstützen die Gruppenanruf Abholung:</span><span class="sxs-lookup"><span data-stu-id="42908-108">The following Lync Server components support Group Call Pickup:</span></span>

  - <span data-ttu-id="42908-109">**Anwendungsdienst**   Der Anwendungsdienst stellt eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen bereit, beispielsweise die Anwendung für den Parken von anrufen.</span><span class="sxs-lookup"><span data-stu-id="42908-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="42908-110">Der Anwendungsdienst wird auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="42908-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="42908-111">**Anruf parken-Anwendung**   Die Anwendung "Parken" ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="42908-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="42908-112">Die Abholung von Gruppen anrufen basiert auf der Anwendung "Parken".</span><span class="sxs-lookup"><span data-stu-id="42908-112">Group Call Pickup is based on the Call Park application.</span></span>

  - <span data-ttu-id="42908-113">**Lync Server-Verwaltungsshell**   Sie verwenden die lync Server-Verwaltungsshell zum Verwalten von Gruppenanruf-pickupgruppen.</span><span class="sxs-lookup"><span data-stu-id="42908-113">**Lync Server Management Shell**   You use Lync Server Management Shell to manage Group Call Pickup groups.</span></span>

  - <span data-ttu-id="42908-114">**SEFAUtil Resource Kit-Tool**   Sie verwenden das Feature-Aktivierungs Dienstprogramm für sekundäre Erweiterungen (SEFAUtil), um Benutzer einer Anruf Abhol Gruppe zuzuweisen und die Anruf Abholung für Benutzer zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="42908-114">**SEFAUtil resource kit tool**   You use the secondary extension feature activation utility (SEFAUtil) to assign users to a call pickup group and to enable or disable call pickup for users.</span></span>

<span data-ttu-id="42908-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42908-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

