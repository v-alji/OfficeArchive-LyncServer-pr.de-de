---
title: 'Lync Server 2013: Ermitteln Ihrer Systemanforderungen'
description: 'Lync Server 2013: Ermitteln der Systemanforderungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determining your system requirements
ms:assetid: 620e81e2-42df-4eda-8498-bd56a14aa0e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398438(v=OCS.15)
ms:contentKeyID: 48184286
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ceca8eabb234ae7fd483372ff5e611664ecc4fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429489"
---
# <a name="determining-your-system-requirements-for-lync-server-2013"></a><span data-ttu-id="54dc6-103">Ermitteln Ihrer Systemanforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-103">Determining your system requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="54dc6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="54dc6-104">

<span> </span></span></span>

<span data-ttu-id="54dc6-105">_**Letztes Änderungsdatum des Themas:** 2014-01-02_</span><span class="sxs-lookup"><span data-stu-id="54dc6-105">_**Topic Last Modified:** 2014-01-02_</span></span>

<span data-ttu-id="54dc6-106">Alle Server mit lync Server müssen bestimmte Mindestsystemanforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="54dc6-106">All servers running Lync Server must meet certain minimum system requirements.</span></span> <span data-ttu-id="54dc6-107">Zu den System Anforderungen für lync Server gehören die Server Hardware, das Betriebssystem, das auf jedem Server installiert werden soll, sowie verwandte Softwareanforderungen, wie etwa die Windows-Updates und andere Software, die auf den Servern installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="54dc6-107">System requirements for Lync Server include the server hardware, the operating system to be installed on each server, and related software requirements, such as the Windows updates and other software that must be installed on the servers.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="54dc6-108">Lync Server ist nur in einer 64-Bit-Edition verfügbar, die 64-Bit-Hardware und eine 64-Bit-Edition von Windows Server erfordert.</span><span class="sxs-lookup"><span data-stu-id="54dc6-108">Lync Server is available only in a 64-bit edition, which requires 64-bit hardware and a 64-bit edition of Windows Server.</span></span> <span data-ttu-id="54dc6-109">Die Ausnahme ist das Microsoft lync Server 2013, Planungs Tool, das in einer 32-Bit-Edition verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="54dc6-109">The exception is the Microsoft Lync Server 2013, Planning Tool, which is available in a 32-bit edition.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="54dc6-110">Ausführliche Informationen zur Active Directory-Unterstützung, zu unterstützten Topologien, zur Server Zusammenstellung und zu anderen Problemen mit der Unterstützung finden Sie unter <A href="lync-server-2013-supportability.md">Support für lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="54dc6-110">For details about Active Directory support, supported topologies, server collocation, and other supportability issues, see <A href="lync-server-2013-supportability.md">Supportability for Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="54dc6-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="54dc6-111">In This Section</span></span>

  - [<span data-ttu-id="54dc6-112">Serverhardwareplattformen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-112">Server hardware platforms for Lync Server 2013</span></span>](lync-server-2013-server-hardware-platforms.md)

  - [<span data-ttu-id="54dc6-113">Betriebssystemunterstützung für Server und Tools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-113">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)

  - [<span data-ttu-id="54dc6-114">Unterstützte Datenbanksoftware in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-114">Database software support in Lync Server 2013</span></span>](lync-server-2013-database-software-support.md)

  - [<span data-ttu-id="54dc6-115">Zusätzliche Softwareanforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-115">Additional software requirements for Lync Server 2013</span></span>](lync-server-2013-additional-software-requirements.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="54dc6-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54dc6-116">See Also</span></span>


[<span data-ttu-id="54dc6-117">Unterstützte Client- und Gerätehardware in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-117">Client and device hardware support in Lync Server 2013</span></span>](lync-server-2013-client-and-device-hardware-support.md)  
[<span data-ttu-id="54dc6-118">Unterstützung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="54dc6-118">Supportability for Lync Server 2013</span></span>](lync-server-2013-supportability.md)  
  

<span data-ttu-id="54dc6-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="54dc6-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

