---
title: 'Lync Server 2013: Konfigurieren von Ansagen für nicht zugewiesene Nummern'
description: 'Lync Server 2013: Konfigurieren von Ankündigungen für nicht zugewiesene Nummern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring announcements for unassigned numbers
ms:assetid: 45633dd3-78de-4934-867e-33969fc25368
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425944(v=OCS.15)
ms:contentKeyID: 48184035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ab636f0c6157118a00d5e46521555086c5e520
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394643"
---
# <a name="configuring-announcements-for-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="f0abc-103">Konfigurieren von Ansagen für nicht zugewiesene Nummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-103">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0abc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0abc-104">

<span> </span></span></span>

<span data-ttu-id="f0abc-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="f0abc-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="f0abc-106">Bei der Ankündigungs Anwendung handelt es sich um ein Enterprise-VoIP-Feature, mit dem Sie konfigurieren können, was mit Anrufen zu nicht zugewiesenen Erweiterungen geschieht (Erweiterungen, die für Ihre Organisation gültig sind, aber keiner Person oder einem Telefon zugeordnet sind).</span><span class="sxs-lookup"><span data-stu-id="f0abc-106">The Announcement application is an Enterprise Voice feature that enables you to configure what happens to calls to unassigned extensions (extensions that are valid for your organization, but are not assigned to a person or a phone).</span></span> <span data-ttu-id="f0abc-107">So können Sie beispielsweise Anrufe an nicht zugewiesene Nummern konfigurieren, um eine Nachricht wiederzugeben oder an ein anderes Ziel oder beides übertragen zu werden.</span><span class="sxs-lookup"><span data-stu-id="f0abc-107">For example, you can configure calls to unassigned numbers to play a message, or to be transferred to a different destination, or both.</span></span>

<span data-ttu-id="f0abc-108">Die Ankündigungs Anwendung wird auf dem Front-End-Server oder Standard Edition-Server als Feature der reaktionsgruppenanwendung installiert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f0abc-108">The Announcement application is installed as a feature of Response Group application on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="f0abc-109">Sie müssen Ansagen konfigurieren, indem Sie Audiodateien hochladen oder die Text-zu-Sprache-Funktion und die Tabelle nicht zugewiesener Nummern konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f0abc-109">You need to configure Announcements by uploading your audio files or by configuring text-to-speech (TTS) and configuring the unassigned number table.</span></span>

<span data-ttu-id="f0abc-110">Dieser Abschnitt führt Sie durch die Konfiguration von lync Server-Ankündigungen.</span><span class="sxs-lookup"><span data-stu-id="f0abc-110">This section guides you through the configuration of Lync Server Announcements.</span></span> <span data-ttu-id="f0abc-111">Es wird davon ausgegangen, dass Sie die Planungsabschnitte in Bezug auf Ankündigungen bereits gelesen und einen Enterprise Edition-Server oder einen Standard Edition-Server mit Enterprise-VoIP bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="f0abc-111">It assumes that you have already read the planning sections related to Announcements and deployed an Enterprise Edition server or a Standard Edition server with Enterprise Voice.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f0abc-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f0abc-112">In This Section</span></span>

  - [<span data-ttu-id="f0abc-113">Konfigurationsvoraussetzungen und -rollen für Ansagen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-113">Announcement configuration prerequisites and roles in Lync Server 2013</span></span>](lync-server-2013-announcement-configuration-prerequisites-and-roles.md)

  - [<span data-ttu-id="f0abc-114">Bereitstellungsprozess für die Ankündigungs Anwendung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-114">Deployment process for the Announcement application in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-the-announcement-application.md)

  - [<span data-ttu-id="f0abc-115">Erstellen einer Ankündigung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-115">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="f0abc-116">Konfigurieren der Tabelle nicht zugewiesener Nummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-116">Configure the unassigned number table in Lync Server 2013</span></span>](lync-server-2013-configure-the-unassigned-number-table.md)

  - [<span data-ttu-id="f0abc-117">Optional Überprüfen der Ankündigungs Bereitstellung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-117">(Optional) Verify Announcement deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-announcement-deployment.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f0abc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0abc-118">See Also</span></span>


[<span data-ttu-id="f0abc-119">Planen der Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0abc-119">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="f0abc-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0abc-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

