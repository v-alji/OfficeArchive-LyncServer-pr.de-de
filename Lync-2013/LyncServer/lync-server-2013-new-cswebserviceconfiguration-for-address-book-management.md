---
title: 'Lync Server 2013: New-CsWebServiceConfiguration für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: New-CsWebServiceConfiguration für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsWebServiceConfiguration for Address Book management
ms:assetid: 49e4ecc5-aa3e-4dd4-a32c-b0dea3758fab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429703(v=OCS.15)
ms:contentKeyID: 48184067
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8972f1b4fe71554e6a8925ddebea6303e2f074a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445435"
---
# <a name="new-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="bed6b-103">New-CsWebServiceConfiguration für die Verwaltung von Adressbüchern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bed6b-103">New-CsWebServiceConfiguration for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bed6b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bed6b-104">

<span> </span></span></span>

<span data-ttu-id="bed6b-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bed6b-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bed6b-106">Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen autorisiert, das New-CsWebServiceConfiguration-Cmdlet lokal auszuführen: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="bed6b-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="bed6b-107">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):</span><span class="sxs-lookup"><span data-stu-id="bed6b-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsWebServiceConfiguration"}

<span data-ttu-id="bed6b-108">Das Cmdlet-New-CsWebServiceConfiguration definiert eine neue Konfiguration für Webdienste in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="bed6b-108">The cmdlet New-CsWebServiceConfiguration defines a new configuration for Web Services in your organization.</span></span> <span data-ttu-id="bed6b-109">Der Bereich für die Webdienstkonfiguration kann sich nur auf der Website oder auf der Dienstebene befinden.</span><span class="sxs-lookup"><span data-stu-id="bed6b-109">The scope for the Web Services configuration can only be at the site or service level.</span></span> <span data-ttu-id="bed6b-110">Auf globaler Ebene kann keine neue Webdienste-Konfiguration erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bed6b-110">It cannot create a new Web Services configuration at the global level.</span></span> <span data-ttu-id="bed6b-111">Das EnableGroupExansion-Attribut ist speziell für das Adressbuch interessant.</span><span class="sxs-lookup"><span data-stu-id="bed6b-111">Specifically of interest to the Address Book is the EnableGroupExansion attribute.</span></span> <span data-ttu-id="bed6b-112">Wenn Sie auf "true" festgelegt ist, können die Webdienste auf Anforderungen für Gruppen Erweiterungen Antworten.</span><span class="sxs-lookup"><span data-stu-id="bed6b-112">If set to True, the Web Services can respond to requests for group expansion.</span></span>

<span data-ttu-id="bed6b-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bed6b-113">For example:</span></span>

    New-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $False -UseCertificateAuth $True

<div>

## <a name="see-also"></a><span data-ttu-id="bed6b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bed6b-114">See Also</span></span>


[<span data-ttu-id="bed6b-115">Neu – CsWebServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bed6b-115">New-CsWebServiceConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWebServiceConfiguration)  
  

<span data-ttu-id="bed6b-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bed6b-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

