---
title: 'Lync Server 2013: Anforderungen und Benutzerrechte für die Konfiguration zum Parken von Anrufen'
description: 'Lync Server 2013: die Voraussetzungen für die Park Konfiguration und die Benutzerrechte.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park configuration prerequisites and user rights
ms:assetid: 25b8cfe0-e4e7-487c-9e78-8c040f629059
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425730(v=OCS.15)
ms:contentKeyID: 48183648
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b01187ad32fa7338765c0fa5b409b4e185e8ad35
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435712"
---
# <a name="call-park-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a><span data-ttu-id="f44fa-103">Anforderungen und Benutzerrechte für die Konfiguration zum Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f44fa-103">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f44fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f44fa-104">

<span> </span></span></span>

<span data-ttu-id="f44fa-105">_**Letztes Änderungsdatum des Themas:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="f44fa-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="f44fa-106">Anruf Parken ist eine anrufverwaltungsfunktion, die standardmäßig bei der Bereitstellung von Enterprise-VoIP installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f44fa-106">Call Park is a call management feature that is installed by default when you deploy Enterprise Voice.</span></span> <span data-ttu-id="f44fa-107">In diesem Thema wird beschrieben, was Sie benötigen, bevor Sie den Anruf Park und die Benutzerrechte konfigurieren können, die Sie zum Ausführen von Konfigurationsaufgaben benötigen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-107">This topic describes what you need to have in place before you can configure Call Park and the user rights that you need to perform configuration tasks.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f44fa-108">Angepasste Musik-in-situ-Dateien für die Anwendung "Parken" werden nicht im Rahmen des lync Server 2013-Wiederherstellungsprozesses gesichert, und die Dateien gehen verloren, wenn die in den Pool hochgeladenen Dateien beschädigt, beschädigt oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="f44fa-108">Customized music-on-hold files for the Call Park application are not backed up as part of the Lync Server 2013 disaster recovery process, and the files will be lost if the files uploaded to the pool are damaged, corrupted, or erased.</span></span> <span data-ttu-id="f44fa-109">Bewahren Sie stets eine separate Sicherungskopie der für geparkte Anrufe hochgeladenen angepassten Musikdateien auf.</span><span class="sxs-lookup"><span data-stu-id="f44fa-109">Always keep a separate backup copy of the customized music-on-hold files that you have uploaded for Call Park.</span></span>



</div>

<span data-ttu-id="f44fa-110">In diesem Abschnitt wird davon ausgegangen, dass Sie die Planungsdokumentation zum Parken von Anrufen gelesen haben (siehe [Planen von Anruf Verwaltungsfeatures in lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span><span class="sxs-lookup"><span data-stu-id="f44fa-110">This section assumes that you have read the planning documentation related to Call Park (see [Planning for call management features in Lync Server 2013](lync-server-2013-planning-for-call-management-features.md)).</span></span>

<div>

## <a name="call-park-configuration-prerequisites"></a><span data-ttu-id="f44fa-111">Voraussetzungen für die Konfiguration des Anruf Parks</span><span class="sxs-lookup"><span data-stu-id="f44fa-111">Call Park Configuration Prerequisites</span></span>

<span data-ttu-id="f44fa-112">Für den Parken von Anrufen sind die folgenden Komponenten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="f44fa-112">Call Park requires the following components:</span></span>

  - <span data-ttu-id="f44fa-113">Anwendungsdienst</span><span class="sxs-lookup"><span data-stu-id="f44fa-113">Application service</span></span>

  - <span data-ttu-id="f44fa-114">Anwendung zum Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="f44fa-114">Call Park application</span></span>

<span data-ttu-id="f44fa-115">Diese Komponenten werden automatisch installiert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-115">These components are installed automatically when you deploy Enterprise Voice.</span></span>

<span data-ttu-id="f44fa-116">Wenn Sie möchten, dass Anrufer Musik hören, während der Anruf abgestellt wird, ist auch eine Musik-auf-halten-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f44fa-116">If you want callers to hear music while the call is parked, a music-on-hold file is also required.</span></span> <span data-ttu-id="f44fa-117">Wenn Sie Enterprise-VoIP bereitstellen, wird automatisch eine standardmäßige Music-on-halten-Datei installiert.</span><span class="sxs-lookup"><span data-stu-id="f44fa-117">A default music-on-hold file is installed automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="f44fa-118">Sie können die Standarddatei durch ihre eigene Musik-in-halten-Datei ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-118">You can substitute the default file with your own music-on-hold file.</span></span> <span data-ttu-id="f44fa-119">Call Park verwendet den Dateispeicher, um die Audiodatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f44fa-119">Call Park uses File Store to hold the audio file.</span></span>

</div>

<div>

## <a name="call-park-configuration-user-rights"></a><span data-ttu-id="f44fa-120">Konfigurations Benutzerrechte des Anruf Parks</span><span class="sxs-lookup"><span data-stu-id="f44fa-120">Call Park Configuration User Rights</span></span>

<span data-ttu-id="f44fa-121">Sie können die folgenden Verwaltungstools zum Konfigurieren des Anruf Parks verwenden:</span><span class="sxs-lookup"><span data-stu-id="f44fa-121">You can use the following administrative tools to configure Call Park:</span></span>

  - <span data-ttu-id="f44fa-122">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="f44fa-122">Lync Server Control Panel</span></span>

  - <span data-ttu-id="f44fa-123">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="f44fa-123">Lync Server Management Shell</span></span>

<span data-ttu-id="f44fa-124">Sie verwenden diese Tools, um die Umlaufbahn Tabelle des Anruf Parks einzurichten und andere Einstellungen zu konfigurieren, die von Call Park verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f44fa-124">You use these tools to set up the Call Park orbit table and to configure other settings used by Call Park.</span></span>

<span data-ttu-id="f44fa-125">Die Konfiguration des Anruf Parks erfordert je nach Aufgabe eine der folgenden Administratorrollen:</span><span class="sxs-lookup"><span data-stu-id="f44fa-125">Configuring Call Park requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="f44fa-126">**CsVoiceAdministrator:** Diese Administratorrolle kann alle sprachbezogenen Einstellungen und Richtlinien erstellen, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="f44fa-126">**CsVoiceAdministrator:** This administrator role can create, configure, and manage all voice-related settings and policies.</span></span>

  - <span data-ttu-id="f44fa-127">**CsUserAdministrator:** Mit dieser Administratorrolle kann der Anruf Park in der VoIP-Richtlinie aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="f44fa-127">**CsUserAdministrator:** This administrator role can enable Call Park in voice policy.</span></span> <span data-ttu-id="f44fa-128">Diese Administratorrolle verfügt auch über die schreibgeschützte Ansicht Zugriff auf alle Sprachkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-128">This administrator role also has read-only view access to all voice configurations.</span></span>

  - <span data-ttu-id="f44fa-129">**CsServerAdministrator:** Diese Administratorrolle kann Server und Dienste verwalten, überwachen und Problembehandlung durchführen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-129">**CsServerAdministrator:** This administrator role can manage, monitor, and troubleshoot servers and services.</span></span>

  - <span data-ttu-id="f44fa-130">**CsAdministrator:** Diese Administratorrolle kann alle Aufgaben von CsVoiceAdministrator, CsServerAdministrator und CsUserAdministrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="f44fa-130">**CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator, CsServerAdministrator, and CsUserAdministrator.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f44fa-131">Details zu Administratorrechten finden Sie unter <A href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f44fa-131">For details about administrative rights, see <A href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f44fa-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f44fa-132">See Also</span></span>


[<span data-ttu-id="f44fa-133">Bereitstellen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f44fa-133">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  


[<span data-ttu-id="f44fa-134">Planen der Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f44fa-134">Planning for call management features in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-management-features.md)  
  

<span data-ttu-id="f44fa-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f44fa-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

