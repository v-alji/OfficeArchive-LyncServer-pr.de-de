---
title: 'Lync Server 2013: Adressbuchserver-Cmdlets'
description: 'Lync Server 2013: Adressbuchserver-Cmdlets.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Address Book Server cmdlets
ms:assetid: 33da45da-3c57-4d04-9679-f0e5a0cfd37e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415643(v=OCS.15)
ms:contentKeyID: 48183793
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e4fef903d25f0d2707410e017f4eb280282bbdab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439996"
---
# <a name="address-book-server-cmdlets-in-lync-server-2013"></a><span data-ttu-id="2af3c-103">Cmdlets des Adressbuchservers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2af3c-103">Address Book Server cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2af3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2af3c-104">

<span> </span></span></span>

<span data-ttu-id="2af3c-105">_**Letztes Änderungsdatum des Themas:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="2af3c-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="2af3c-106">Adressbuchserver sind Vermittler zwischen Active Directory-Domänendiensten und Microsoft lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2af3c-106">Address Book servers are intermediaries between Active Directory Domain Services and Microsoft Lync Server 2013.</span></span> <span data-ttu-id="2af3c-107">Der Adressbuchserver stellt sicher, dass die in lync Server 2013 gespeicherten Benutzerinformationen mit den in Active Directory gespeicherten Benutzerinformationen synchron sind.</span><span class="sxs-lookup"><span data-stu-id="2af3c-107">The Address Book server ensures that the user information stored in Lync Server 2013 is in synch with the user information stored in Active Directory.</span></span> <span data-ttu-id="2af3c-108">Dies erfolgt durch regelmäßiges Synchronisieren von Adressbuchdateien mit Informationen, die in der Benutzerdatenbank gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2af3c-108">This is done by periodically synching Address Book files with information stored in the User database.</span></span> <span data-ttu-id="2af3c-109">Lync Server enthält wiederum eine Reihe von Cmdlets für die Verwaltung von Adressbuch Servern.</span><span class="sxs-lookup"><span data-stu-id="2af3c-109">In turn, Lync Server includes a number of cmdlets for managing Address Book servers.</span></span>

<div>

## <a name="address-book-server-cmdlets"></a><span data-ttu-id="2af3c-110">Adressbuch Server-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2af3c-110">Address Book Server Cmdlets</span></span>

<span data-ttu-id="2af3c-111">In der lync Server-Systemsteuerung können die Adressbuchserver Einstellungen nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="2af3c-111">You cannot configure the Address Book Server settings in Lync Server Control Panel.</span></span> <span data-ttu-id="2af3c-112">Windows PowerShell ist das wichtigste Tool für die Verwaltung dieser Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="2af3c-112">Windows PowerShell is the primary tool for managing these settings.</span></span> <span data-ttu-id="2af3c-113">Die folgende Liste enthält Cmdlets, die sich direkt auf die Verwaltung des Adressbuchservers beziehen:</span><span class="sxs-lookup"><span data-stu-id="2af3c-113">The following is a list of cmdlets that relate directly to managing the Address Book Server:</span></span>

<span data-ttu-id="2af3c-114">**Adressbuchserver**</span><span class="sxs-lookup"><span data-stu-id="2af3c-114">**Address Book Server**</span></span>

  - <span></span>  
    <span data-ttu-id="2af3c-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-115">[Get-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398132(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2af3c-116">[Neu – CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-116">[New-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398395(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2af3c-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-117">[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="2af3c-118">[Satz-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-118">[Set-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg412784(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2af3c-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-119">[Update-CsAddressBook](https://technet.microsoft.com/library/Gg398194(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2af3c-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-120">[Debug-CsAddressBookReplication](https://technet.microsoft.com/library/JJ205232(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2af3c-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-121">[Test-CsAddressBookService](https://technet.microsoft.com/library/Gg398661(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="2af3c-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="2af3c-122">[Test-CsAddressBookWebQuery](https://technet.microsoft.com/library/Gg398773(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2af3c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2af3c-123">See Also</span></span>


[<span data-ttu-id="2af3c-124">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="2af3c-124">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="2af3c-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2af3c-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

