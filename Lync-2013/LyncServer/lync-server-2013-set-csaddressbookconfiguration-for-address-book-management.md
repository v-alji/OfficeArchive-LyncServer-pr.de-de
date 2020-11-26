---
title: 'Lync Server 2013: Set-CsAddressBookConfiguration für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: Set-CsAddressBookConfiguration für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set-CsAddressBookConfiguration for Address Book management
ms:assetid: 3a64ceb1-9f79-4f3b-bf33-eaf346dbd60d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429700(v=OCS.15)
ms:contentKeyID: 48183913
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab7a58510b2bb6232d9908c77cf6b70bbeb927f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444756"
---
# <a name="set-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="5d961-103">Set-CsAddressBookConfiguration für die Verwaltung von Adressbüchern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d961-103">Set-CsAddressBookConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d961-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d961-104">

<span> </span></span></span>

<span data-ttu-id="5d961-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5d961-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5d961-106">Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen autorisiert, das Set-CsAddressBookConfiguration-Cmdlet lokal auszuführen: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="5d961-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="5d961-107">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):</span><span class="sxs-lookup"><span data-stu-id="5d961-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsAddressBookConfiguration"}

<span data-ttu-id="5d961-108">Set-CsAddressBookConfiguration ähnelt dem Cmdlet New-CsAddressBookConfiguration, es wird jedoch verwendet, um eine vorhandene Konfiguration zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5d961-108">Set-CsAddressBookConfiguration is similar to the New-CsAddressBookConfiguration cmdlet, except it is used to modify an existing configuration.</span></span>

<span data-ttu-id="5d961-109">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5d961-109">For example:</span></span>

    Set-CsAddressBookConfiguration -identity site:Redmond -RunTimeOfDay 23:00

<div>

## <a name="see-also"></a><span data-ttu-id="5d961-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d961-110">See Also</span></span>


[<span data-ttu-id="5d961-111">Satz-CsAddressBookConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d961-111">Set-CsAddressBookConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsAddressBookConfiguration)  
  

<span data-ttu-id="5d961-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d961-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

