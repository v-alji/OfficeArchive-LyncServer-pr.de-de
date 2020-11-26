---
title: 'Lync Server 2013: Voraussetzungen zur Aktivierung der Kerberos-Authentifizierung'
description: 'Lync Server 2013: Voraussetzungen für die Aktivierung der Kerberos-Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436972"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="d76d5-103">Voraussetzungen zur Aktivierung der Kerberos-Authentifizierung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d76d5-103">Prerequisites for enabling Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d76d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d76d5-104">

<span> </span></span></span>

<span data-ttu-id="d76d5-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d76d5-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d76d5-106">Bevor Sie die Kerberos-Authentifizierung aktivieren, stellen Sie sicher, dass Sie alle erforderlichen Konfigurations-und Infrastruktur Vorbereitungen durchführen:</span><span class="sxs-lookup"><span data-stu-id="d76d5-106">Before enabling Kerberos authentication, make sure that you complete all prerequisite configuration and infrastructure preparations:</span></span>

  - <span data-ttu-id="d76d5-107">Das Active Directory-Schema wird für lync Server 2013 erweitert.</span><span class="sxs-lookup"><span data-stu-id="d76d5-107">Active Directory schema is extended for Lync Server 2013.</span></span>

  - <span data-ttu-id="d76d5-108">Die Active Directory-Gesamtstrukturvorbereitung ist für lync Server 2013 abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d76d5-108">Active Directory forest preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="d76d5-109">Die Active Directory-Domänenvorbereitung ist für lync Server 2013 abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d76d5-109">Active Directory domain preparation is completed for Lync Server 2013.</span></span>

  - <span data-ttu-id="d76d5-110">Der zentrale Verwaltungsspeicher wurde erfolgreich installiert und verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d76d5-110">Central Management store is successfully installed and available.</span></span>

  - <span data-ttu-id="d76d5-111">Die Topologie wurde mithilfe des Topologie-Generators erstellt und veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="d76d5-111">The topology has been created and published by using Topology Builder.</span></span>

  - <span data-ttu-id="d76d5-112">Server und Rollen, die Webdienste erfordern, wurden definiert und bereitgestellt, einschließlich der Front-End-Server, der Standard Edition-Server und der Directors.</span><span class="sxs-lookup"><span data-stu-id="d76d5-112">Servers and roles that require Web Services have been defined and deployed, including Front End Servers, Standard Edition servers, and Directors.</span></span>

  - <span data-ttu-id="d76d5-113">Internet Informationsdienste (IIS) wird mit den empfohlenen Rollendiensten für die Unterstützung von Webdiensten in lync Server 2013 konfiguriert und bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d76d5-113">Internet Information Services (IIS) is configured and deployed with the recommended role services to support Web Services in Lync Server 2013.</span></span>

<span data-ttu-id="d76d5-114">Nachdem die Voraussetzungen erfüllt wurden, sollten Sie bereit sein, mindestens ein Konto für Webdienste zu erstellen, das für die Kerberos-Authentifizierung für Ihre Bereitstellung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d76d5-114">After the prerequisites have been met, you should be ready to create one or more accounts for Web Services to use for Kerberos authentication for your deployment.</span></span> <span data-ttu-id="d76d5-115">Sie müssen mindestens ein Kerberos-Authentifizierungs Konto für jede Bereitstellung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d76d5-115">At a minimum, you need to create one Kerberos authentication account for each deployment.</span></span> <span data-ttu-id="d76d5-116">Sie können jedoch für jede Website ein Konto erstellen, um die lokale Kerberos-Authentifizierung auf der Website bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d76d5-116">However, you can create an account for each site to provide local Kerberos authentication at the site.</span></span> <span data-ttu-id="d76d5-117">Sie können nur ein Kerberos-Authentifizierungs Konto pro Website angeben.</span><span class="sxs-lookup"><span data-stu-id="d76d5-117">You can only specify one Kerberos authentication account per site.</span></span>

<span data-ttu-id="d76d5-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d76d5-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

