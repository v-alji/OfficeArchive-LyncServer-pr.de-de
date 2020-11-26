---
title: 'Lync Server 2013: Konfigurieren der Pickup für Gruppenanrufe'
description: 'Lync Server 2013: Konfigurieren der Gruppenanruf Abholung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Group Call Pickup
ms:assetid: b4b0a9a0-91c6-43a5-9e2b-a086caeb3f94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945645(v=OCS.15)
ms:contentKeyID: 51541505
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff6be1ea20a98cfaf2addf32c7767940b420c5c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433031"
---
# <a name="configuring-group-call-pickup-in-lync-server-2013"></a><span data-ttu-id="67050-103">Konfigurieren der Gruppenanruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-103">Configuring Group Call Pickup in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="67050-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="67050-104">

<span> </span></span></span>

<span data-ttu-id="67050-105">_**Letztes Änderungsdatum des Themas:** 2013-02-01_</span><span class="sxs-lookup"><span data-stu-id="67050-105">_**Topic Last Modified:** 2013-02-01_</span></span>

<span data-ttu-id="67050-106">Kumulatives Update für lync Server 2013: Februar 2013 führt die Abholung des Gruppenanrufs als neue Enterprise-VoIP-Funktion ein.</span><span class="sxs-lookup"><span data-stu-id="67050-106">Cumulative update for Lync Server 2013: February 2013 introduces Group Call Pickup as a new Enterprise Voice feature.</span></span> <span data-ttu-id="67050-107">Mit der Gruppenanruf-Abholung können Benutzer Anrufe aufnehmen, die für einen anderen Nutzer Klingeln, indem Sie eine Anruf-Abhol Gruppennummer wählen.</span><span class="sxs-lookup"><span data-stu-id="67050-107">Group Call Pickup lets users pick up calls that are ringing for another user by dialing a call pickup group number.</span></span>

<span data-ttu-id="67050-108">Die Komponenten, die von der Gruppenanruf Abholung verwendet werden, werden beim Bereitstellen von Enterprise-VoIP automatisch auf dem Front-End-Server oder Standard Edition-Server installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="67050-108">The components that Group Call Pickup uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="67050-109">Sie müssen jedoch die Gruppenanruf Abholung konfigurieren, bevor Sie für die Benutzer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="67050-109">However, you must configure Group Call Pickup before it is available to users.</span></span>

<span data-ttu-id="67050-110">Dieser Abschnitt führt Sie durch die Konfiguration der Gruppenanruf Abholung.</span><span class="sxs-lookup"><span data-stu-id="67050-110">This section guides you through the configuration of Group Call Pickup.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="67050-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="67050-111">In This Section</span></span>

[<span data-ttu-id="67050-112">Voraussetzungen für Gruppenanruf-Pickup-Konfiguration und Benutzerrechte in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-112">Group Call Pickup configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-group-call-pickup-configuration-prerequisites-and-user-rights.md)

[<span data-ttu-id="67050-113">Bereitstellungsprozess für die Gruppenanruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-113">Deployment process for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-group-call-pickup.md)

[<span data-ttu-id="67050-114">Deploy the SEFAUtil tool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-114">Deploy the SEFAUtil tool in Lync Server 2013</span></span>](lync-server-2013-deploy-the-sefautil-tool.md)

[<span data-ttu-id="67050-115">Konfigurieren von Gruppennummern für die Anruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-115">Configure call pickup group numbers in Lync Server 2013</span></span>](lync-server-2013-configure-call-pickup-group-numbers.md)

[<span data-ttu-id="67050-116">Aktivieren der Gruppenanruf Abholung für Benutzer in lync Server 2013 und Zuweisen einer Gruppennummer</span><span class="sxs-lookup"><span data-stu-id="67050-116">Enable Group Call Pickup for users in Lync Server 2013 and assign a group number</span></span>](lync-server-2013-enable-group-call-pickup-for-users-and-assign-a-group-number.md)

[<span data-ttu-id="67050-117">Übermitteln von Gruppenanruf-Abholaufträgen an Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-117">Communicate Group Call Pickup assignments to users in Lync Server 2013</span></span>](lync-server-2013-communicate-group-call-pickup-assignment-to-users.md)

[<span data-ttu-id="67050-118">Optional Überprüfen der Bereitstellung für die Gruppenanruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="67050-118">(Optional) Verify the Group Call Pickup deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-the-group-call-pickup-deployment.md)

<span data-ttu-id="67050-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="67050-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

