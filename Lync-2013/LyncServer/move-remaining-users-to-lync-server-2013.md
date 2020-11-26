---
title: Verschieben der verbleibenden Benutzer zu Lync Server 2013
description: Verschieben von verbleibenden Benutzern auf lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move remaining users to Lync Server 2013
ms:assetid: 72025e1b-97d1-40e9-8a98-28c018942b48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688090(v=OCS.15)
ms:contentKeyID: 49733689
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 291b58d6644f9ac8f10c63f6585ba865602580df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438446"
---
# <a name="move-remaining-users-to-lync-server-2013"></a><span data-ttu-id="61b2f-103">Verschieben der verbleibenden Benutzer zu Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61b2f-103">Move remaining users to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61b2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61b2f-104">

<span> </span></span></span>

<span data-ttu-id="61b2f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="61b2f-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="61b2f-106">Mithilfe der lync Server-Systemsteuerung oder der lync Server-Verwaltungsshell können Sie Benutzer zur neuen lync Server 2013-Bereitstellung verschieben.</span><span class="sxs-lookup"><span data-stu-id="61b2f-106">You can move users to the new Lync Server 2013 deployment by using either Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="61b2f-107">Sie müssen einige Voraussetzungen erfüllen, um einen reibungslosen Übergang zu lync Server 2013 zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="61b2f-107">You must meet some requirements to ensure a smooth transition to Lync Server 2013.</span></span> <span data-ttu-id="61b2f-108">Details zu den Voraussetzungen für die Durchführung der Verfahren in diesem Thema finden Sie unter [Konfigurieren von Clients für die Migration](configure-clients-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="61b2f-108">For details about prerequisites to completing the procedures in this topic, see [Configure clients for migration](configure-clients-for-migration.md).</span></span> <span data-ttu-id="61b2f-109">Detaillierte Anweisungen zum Verschieben von Benutzern finden Sie unter [Phase 4: Verschieben von Testbenutzern in den Pilot Pool](phase-4-move-test-users-to-the-pilot-pool.md).</span><span class="sxs-lookup"><span data-stu-id="61b2f-109">For detailed steps about moving users, see [Phase 4: Move test users to the pilot pool](phase-4-move-test-users-to-the-pilot-pool.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="61b2f-110">Sie können das Snap-in Active Directory-Benutzer und-Computer oder die lync Server 2010-Verwaltungstools nicht verwenden, um Benutzer aus ihrer Legacyumgebung in lync Server 2013 zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="61b2f-110">You cannot use the Active Directory Users and Computers snap-in or the Lync Server 2010 administrative tools to move users from your legacy environment to Lync Server 2013.</span></span>



</div>

<span data-ttu-id="61b2f-111">Wenn Sie einen Benutzer in einen lync Server 2013-Pool verschieben, werden die Daten für den Benutzer in die Back-End-Datenbank verschoben, die dem neuen Pool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="61b2f-111">When you move a user to an Lync Server 2013 pool, the data for the user is moved to the back-end database that is associated with the new pool.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="61b2f-112">Dazu gehören die vom Legacy Benutzer erstellten aktiven Besprechungen.</span><span class="sxs-lookup"><span data-stu-id="61b2f-112">This includes the active meetings created by the legacy user.</span></span> <span data-ttu-id="61b2f-113">Wenn ein älterer Benutzer beispielsweise eine Konferenz für <STRONG>Meine Besprechung</STRONG> konfiguriert hat, steht diese Konferenz nach dem Verschieben des Benutzers weiterhin im neuen lync Server 2013-Pool zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="61b2f-113">For example, if a legacy user has configured a <STRONG>my meeting</STRONG> conference, that conference will still be available in the new Lync Server 2013 pool after the user has been moved.</span></span> <span data-ttu-id="61b2f-114">Die Details für den Zugriff auf die Besprechung sind weiterhin dieselbe <STRONG>Konferenz-URL und Konferenz-ID</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="61b2f-114">The details to access that meeting will still be the same <STRONG>conference URL and conference ID</STRONG>.</span></span> <span data-ttu-id="61b2f-115">Der einzige Unterschied besteht darin, dass die Konferenz jetzt im lync Server 2013-Pool und nicht im lync Server 2010-Pool gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="61b2f-115">The only difference is that the conference is now hosted in the Lync Server 2013 pool, and not in the Lync Server 2010 pool.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="61b2f-116">Für Homing-Benutzer in lync Server 2013 müssen keine aktualisierten Clients gleichzeitig bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="61b2f-116">Homing users on Lync Server 2013 does not require that you deploy upgraded clients at the same time.</span></span> <span data-ttu-id="61b2f-117">Neue Funktionen stehen Benutzern nur zur Verfügung, wenn Sie ein Upgrade auf die neue Client Software durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="61b2f-117">New functionality will be available to users only when they have upgraded to the new client software.</span></span>



</div>

<div>

## <a name="post-migration-task"></a><span data-ttu-id="61b2f-118">Aufgabe der nach der Migration</span><span class="sxs-lookup"><span data-stu-id="61b2f-118">Post Migration Task</span></span>

1.  <span data-ttu-id="61b2f-119">Nachdem Sie die Benutzer verschoben haben, überprüfen Sie die konferenzrichtlinie, die Ihnen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="61b2f-119">After you move users, verify the conferencing policy that is assigned to them.</span></span>

2.  <span data-ttu-id="61b2f-120">Um sicherzustellen, dass Besprechungen, die von Benutzern verwaltet werden, die in lync Server 2013 verwaltet werden, nahtlos mit Verbundbenutzern funktionieren, die sich in lync Server 2010 befinden, sollten die den migrierten Benutzern zugewiesenen Konferenzrichtlinien anonymen Teilnehmern ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="61b2f-120">To ensure that meetings organized by users homed on Lync Server 2013 work seamlessly with federated users who are homed on Lync Server 2010, the conferencing policy assigned to the migrated users should allow anonymous participants.</span></span>

3.  <span data-ttu-id="61b2f-121">Konferenzrichtlinien, die anonymen Teilnehmern erlauben, **können Teilnehmern erlauben, anonyme Benutzer einzuladen** , die in der lync Server 2013-Systemsteuerung ausgewählt sind, und **AllowAnonymousParticipantsInMeetings** in der Ausgabe des Cmdlets **Get-CsConferencingPolicy** in der lync Server-Verwaltungsshell auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61b2f-121">Conferencing policies that allow anonymous participants have **Allow participants to invite anonymous users** selected in Lync Server 2013 Control Panel and have **AllowAnonymousParticipantsInMeetings** set to **True** in the output from the **Get-CsConferencingPolicy** cmdlet in the Lync Server Management Shell.</span></span>

4.  <span data-ttu-id="61b2f-122">Details zum Konfigurieren von Konferenzrichtlinien mithilfe der lync Server-Verwaltungsshell finden Sie unter Dokumentation zu CsConferencingPolicy in der lync Server [-](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingPolicy) Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="61b2f-122">For details about configuring conferencing policy by using Lync Server Management Shell, see [Set-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsConferencingPolicy) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="61b2f-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61b2f-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

