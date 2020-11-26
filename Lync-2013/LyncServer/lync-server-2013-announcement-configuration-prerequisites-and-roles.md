---
title: 'Lync Server 2013: Konfigurationsvoraussetzungen und -rollen für Ansagen'
description: 'Lync Server 2013: Voraussetzungen und Rollen für die Ankündigungs Konfiguration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Announcement configuration prerequisites and roles
ms:assetid: 82f2dfe9-4c5e-4d65-96a1-96495d506ea4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398658(v=OCS.15)
ms:contentKeyID: 48184674
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8e6e7009adc6826c255e28ddda925b0e9be5fd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439968"
---
# <a name="announcement-configuration-prerequisites-and-roles-in-lync-server-2013"></a><span data-ttu-id="c0836-103">Konfigurationsvoraussetzungen und -rollen für Ansagen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0836-103">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0836-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0836-104">

<span> </span></span></span>

<span data-ttu-id="c0836-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="c0836-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="c0836-106">Ankündigung ist eine Enterprise-VoIP-anrufverwaltungsfunktion.</span><span class="sxs-lookup"><span data-stu-id="c0836-106">Announcement is an Enterprise Voice call management feature.</span></span> <span data-ttu-id="c0836-107">In diesem Thema wird beschrieben, was Sie benötigen, bevor Sie die Ankündigung und die Rollenzuweisungen konfigurieren können, die Sie zum Ausführen von Konfigurationsaufgaben benötigen.</span><span class="sxs-lookup"><span data-stu-id="c0836-107">This topic describes what you need to have in place before you can configure Announcement and the role assignments that you need to perform configuration tasks.</span></span>

<span data-ttu-id="c0836-108">In diesem Abschnitt wird davon ausgegangen, dass Sie die Planungsdokumentation zu Ankündigungen gelesen haben (siehe [Planen von Anruf Verwaltungsfeatures in lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="c0836-108">This section assumes that you have read the planning documentation related to Announcement (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="announcement-configuration-prerequisites"></a><span data-ttu-id="c0836-109">Voraussetzungen für die Ankündigungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c0836-109">Announcement Configuration Prerequisites</span></span>

<span data-ttu-id="c0836-110">Für die Ankündigungs Anwendung sind die folgenden Komponenten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="c0836-110">The Announcement application requires the following components:</span></span>

  - <span data-ttu-id="c0836-111">Anwendungsdienst</span><span class="sxs-lookup"><span data-stu-id="c0836-111">Application service</span></span>

  - <span data-ttu-id="c0836-112">Reaktionsgruppenanwendung</span><span class="sxs-lookup"><span data-stu-id="c0836-112">Response Group application</span></span>

  - <span data-ttu-id="c0836-113">Dateispeicher zum Speichern von Audiodateien</span><span class="sxs-lookup"><span data-stu-id="c0836-113">File Store, to hold audio files</span></span>

<span data-ttu-id="c0836-114">Alle diese Komponenten werden standardmäßig installiert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c0836-114">All of these components are installed by default when you deploy Enterprise Voice.</span></span>

</div>

<div>

## <a name="announcement-configuration-roles"></a><span data-ttu-id="c0836-115">Ankündigungs Konfigurations Rollen</span><span class="sxs-lookup"><span data-stu-id="c0836-115">Announcement Configuration Roles</span></span>

<span data-ttu-id="c0836-116">Sie können die folgenden Verwaltungstools verwenden, um Ankündigungen zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="c0836-116">You can use the following administrative tools to configure announcements:</span></span>

  - <span data-ttu-id="c0836-117">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="c0836-117">Lync Server Control Panel</span></span>

  - <span data-ttu-id="c0836-118">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="c0836-118">Lync Server Management Shell</span></span>

<span data-ttu-id="c0836-119">Zum Konfigurieren der Ankündigungs Anwendung ist eine der folgenden Administratorrollen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="c0836-119">Configuring Announcement application requires one of the following administrative roles:</span></span>

  - <span data-ttu-id="c0836-120">**CsVoiceAdministrator**   Diese Administratorrolle kann alle sprachbezogenen Einstellungen und Richtlinien, einschließlich Ankündigungseinstellungen, erstellen, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="c0836-120">**CsVoiceAdministrator**   This administrator role can create, configure, and manage all voice-related settings and policies, including Announcement settings.</span></span>

  - <span data-ttu-id="c0836-121">**CsServerAdministrator**   Diese Administratorrolle kann Server und Dienste verwalten, überwachen und behandeln sowie alle Ankündigungseinstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="c0836-121">**CsServerAdministrator**   This administrator role can manage, monitor, and troubleshoot servers and services, and configure all Announcement settings.</span></span>

  - <span data-ttu-id="c0836-122">**CsAdministrator**   Diese Administratorrolle kann alle administrativen Aufgaben ausführen und alle Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="c0836-122">**CsAdministrator**   This administrator role can perform all administrative tasks and modify all settings.</span></span>

  - <span data-ttu-id="c0836-123">**CsViewOnlyAdministrator**   Diese Administratorrolle kann die Bereitstellung anzeigen, um den Bereitstellungsstatus zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c0836-123">**CsViewOnlyAdministrator**   This administrator role can view the deployment to monitor deployment health.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c0836-124">Ausführliche Informationen zu administrativen Benutzerrechten finden Sie unter <A href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c0836-124">For details about administrative user rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c0836-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0836-125">See Also</span></span>


[<span data-ttu-id="c0836-126">Bereitstellen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0836-126">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="c0836-127">Planen der Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0836-127">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="c0836-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0836-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

