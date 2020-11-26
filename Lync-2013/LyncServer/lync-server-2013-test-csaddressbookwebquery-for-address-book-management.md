---
title: 'Lync Server 2013: Test-CsAddressBookWebQuery für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: Test-CsAddressBookWebQuery für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test-CsAddressBookWebQuery for Address Book management
ms:assetid: 977a9c1f-5f4e-4539-9a26-8748b61a57d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429716(v=OCS.15)
ms:contentKeyID: 48184865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c7448733ed1477d36b887648154d66c96f9e6d0b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441256"
---
# <a name="test-csaddressbookwebquery-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="debc9-103">Test-CsAddressBookWebQuery für die Verwaltung von Adressbüchern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="debc9-103">Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="debc9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="debc9-104">

<span> </span></span></span>

<span data-ttu-id="debc9-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="debc9-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="debc9-106">Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen zum Ausführen des Test-CsAddressBookWebQuery-Cmdlets autorisiert: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="debc9-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookWebQuery cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="debc9-107">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):</span><span class="sxs-lookup"><span data-stu-id="debc9-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

<span data-ttu-id="debc9-108">Ähnlich wie bei der Test-CsAddressBookService synthetischen Transaktion führt Test-CsAddressBookWebQuery eine Abfrage für die Adressbuch-Webabfrage aus, um sicherzustellen, dass Sie ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="debc9-108">Similar to the Test-CsAddressBookService synthetic transaction, Test-CsAddressBookWebQuery performs a query against the Address Book Web Query to ensure that it is operating properly.</span></span> <span data-ttu-id="debc9-109">Das Cmdlet stellt eine Verbindung mit der Web Ticket-Authentifizierung her und stellt die in – UserCredential angegebenen Anmeldeinformationen dar.</span><span class="sxs-lookup"><span data-stu-id="debc9-109">The cmdlet will connect to the Web Ticket authentication and present the credentials specified in –UserCredential.</span></span> <span data-ttu-id="debc9-110">Wenn authentifiziert, gibt das Cmdlet dann die – TargetSipAddress-Informationen an.</span><span class="sxs-lookup"><span data-stu-id="debc9-110">If authenticated, the cmdlet then present the –TargetSipAddress information.</span></span> <span data-ttu-id="debc9-111">Das Cmdlet sollte Erfolg melden, wenn es die Informationen über den Kontakt abrufen konnte.</span><span class="sxs-lookup"><span data-stu-id="debc9-111">The cmdlet should report success if it was able to retrieve the information about the contact.</span></span>

<span data-ttu-id="debc9-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="debc9-112">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com" -TargetSipAddress "sip:bob@contoso.com"

<div>

## <a name="see-also"></a><span data-ttu-id="debc9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="debc9-113">See Also</span></span>


[<span data-ttu-id="debc9-114">Test-CsAddressBookWebQuery</span><span class="sxs-lookup"><span data-stu-id="debc9-114">Test-CsAddressBookWebQuery</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery)  
  

<span data-ttu-id="debc9-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="debc9-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

