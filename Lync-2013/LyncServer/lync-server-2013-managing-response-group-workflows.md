---
title: 'Lync Server 2013: Verwalten von reaktionsgruppenworkflows'
description: 'Lync Server 2013: Verwalten von reaktionsgruppenworkflows'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Response Group workflows
ms:assetid: 42cfccdd-2844-4875-b4e3-813e1df15f08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520986(v=OCS.15)
ms:contentKeyID: 48183974
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2223fed2b5b030a2c92e0b958ae8545a7717f848
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437224"
---
# <a name="managing-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="204ba-103">Verwalten von reaktionsgruppenworkflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-103">Managing Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="204ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="204ba-104">

<span> </span></span></span>

<span data-ttu-id="204ba-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="204ba-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="204ba-106">Ein Workflow der Reaktionsgruppe definiert das Verhalten eines Anrufs ab dem Zeitpunkt, zu dem das Telefon klingelt, bis zu dem Zeitpunkt, zu dem ein Agent den Anruf annimmt.</span><span class="sxs-lookup"><span data-stu-id="204ba-106">A Response Group workflow defines the behavior of a call from the time that the phone rings to the time that an agent answers the call.</span></span> <span data-ttu-id="204ba-107">Der Workflow umfasst Warteschlangen-und Routinginformationen und enthält Informationen zu den Gruppen "Hunt Group" oder "Interactive Voice Response (IVR)".</span><span class="sxs-lookup"><span data-stu-id="204ba-107">The workflow includes queue and routing information, and includes either hunt group or interactive voice response (IVR) information.</span></span>

<span data-ttu-id="204ba-108">In den Themen in diesem Abschnitt werden bewährte Methoden für das Entwerfen von IVR-Workflows erläutert, und es wird erläutert, wie benutzerdefinierte Geschäftszeiten und Feiertagssätze erstellt, wie Workflows erstellt oder geändert und Arbeitsgruppen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="204ba-108">Topics in this section identify best practices for designing IVR workflows, and explain how to create customized business hours and holiday sets, how to create or modify workflows, and how to delete workgroups.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="204ba-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="204ba-109">In This Section</span></span>

  - [<span data-ttu-id="204ba-110">Entwerfen von Anrufflüssen für interaktive Sprachantwort in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-110">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="204ba-111">Optional Definieren der Geschäftszeiten der Reaktionsgruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-111">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)

  - [<span data-ttu-id="204ba-112">Optional Definieren von Feiertagssätzen für Reaktionsgruppen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-112">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)

  - [<span data-ttu-id="204ba-113">Erstellen oder Ändern eines Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-113">Create or modify a workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-workflow.md)

  - [<span data-ttu-id="204ba-114">Löschen eines Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="204ba-114">Delete a workflow in Lync Server 2013</span></span>](lync-server-2013-delete-a-workflow.md)

<span data-ttu-id="204ba-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="204ba-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

