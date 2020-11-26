---
title: 'Lync Server 2013: (optional) Überprüfen der Antwortgruppen Bereitstellung'
description: 'Lync Server 2013: (optional) Überprüfen der Reaktionsgruppen Bereitstellung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: (Optional) Verify Response Group deployment
ms:assetid: 202ca4ab-8e6d-44a4-b7c8-071133074feb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687989(v=OCS.15)
ms:contentKeyID: 49733579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cfe15026bc1fcfbe10b593987d2717fc0dc8104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424849"
---
# <a name="optional-verify-response-group-deployment-in-lync-server-2013"></a><span data-ttu-id="d8f3c-103">Optional Überprüfen der Bereitstellung von Reaktionsgruppen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8f3c-103">(Optional) Verify Response Group deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8f3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8f3c-104">

<span> </span></span></span>

<span data-ttu-id="d8f3c-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="d8f3c-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="d8f3c-106">Nachdem Sie die Reaktionsgruppe konfiguriert haben, müssen Sie die Konfiguration überprüfen, um sicherzustellen, dass Ihre Reaktionsgruppen wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d8f3c-106">After you configure Response Group, you need to verify the configuration to make sure your response groups work as expected.</span></span> <span data-ttu-id="d8f3c-107">Führen Sie mindestens eine Überprüfung der folgenden Szenarien mit den folgenden Benutzertypen durch:</span><span class="sxs-lookup"><span data-stu-id="d8f3c-107">At minimum, verify the following scenarios by using the following types of users:</span></span>

<span data-ttu-id="d8f3c-108">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d8f3c-108">**Users**</span></span>

  - <span data-ttu-id="d8f3c-109">Ein Benutzer, der sich in lync Server 2013 befindet</span><span class="sxs-lookup"><span data-stu-id="d8f3c-109">A user who is homed on Lync Server 2013</span></span>

  - <span data-ttu-id="d8f3c-110">Ein externer Benutzer, der das Telefonfestnetz (Public Switched Telephone Network, PSTN) verwendet</span><span class="sxs-lookup"><span data-stu-id="d8f3c-110">An external user who uses the public switched telephone network (PSTN)</span></span>

  - <span data-ttu-id="d8f3c-111">Ein Agent, der sich auf lync Server 2013 befindet</span><span class="sxs-lookup"><span data-stu-id="d8f3c-111">An agent who is homed on Lync Server 2013</span></span>

<span data-ttu-id="d8f3c-112">**Szenarien**</span><span class="sxs-lookup"><span data-stu-id="d8f3c-112">**Scenarios**</span></span>

  - <span data-ttu-id="d8f3c-113">Der lync Server 2013-Benutzer ruft die Reaktionsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="d8f3c-113">The Lync Server 2013 user calls the response group.</span></span>

  - <span data-ttu-id="d8f3c-114">Der externe Benutzer ruft die Reaktionsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d8f3c-114">The external user calls the response group.</span></span>

  - <span data-ttu-id="d8f3c-115">Ein Benutzer ruft die Reaktionsgruppe an, während der Agent sich in einem Gespräch befindet; der Benutzer wird in der Warteschleife platziert.</span><span class="sxs-lookup"><span data-stu-id="d8f3c-115">A user calls the response group while the agent is on another call and goes to the queue.</span></span>

<span data-ttu-id="d8f3c-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8f3c-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

