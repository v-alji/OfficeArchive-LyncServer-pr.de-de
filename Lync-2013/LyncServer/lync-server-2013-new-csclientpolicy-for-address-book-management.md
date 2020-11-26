---
title: 'Lync Server 2013: New-CsClientPolicy für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: New-CsClientPolicy für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New-CsClientPolicy for Address Book management
ms:assetid: ef4415fc-82c4-4dc8-97d1-37a084553343
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429726(v=OCS.15)
ms:contentKeyID: 48185771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12c14534c7af447f30a01b1bbbd1679a8375c705
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425110"
---
# <a name="new-csclientpolicy-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="157f6-103">New-CsClientPolicy für die Verwaltung von Adressbüchern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="157f6-103">New-CsClientPolicy for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="157f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="157f6-104">

<span> </span></span></span>

<span data-ttu-id="157f6-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="157f6-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="157f6-106">Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen zum Ausführen des New-CsClientPolicy-Cmdlets autorisiert: RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="157f6-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsClientPolicy cmdlet: RTCUniversalServerAdmins.</span></span> <span data-ttu-id="157f6-107">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):</span><span class="sxs-lookup"><span data-stu-id="157f6-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsClientPolicy"}

<span data-ttu-id="157f6-108">Das Cmdlet New-CsClientPolicy definiert eine große Anzahl von Einstellungen für die Bereitstellung von Clients für Features, die in lync Server 2013 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="157f6-108">The cmdlet New-CsClientPolicy defines a large number of settings for provisioning clients for features that are available in Lync Server 2013.</span></span> <span data-ttu-id="157f6-109">Für den Adressbuchdienst ist der Parameter AddressBookAvailability von Interesse.</span><span class="sxs-lookup"><span data-stu-id="157f6-109">For the Address Book Service, the parameter AddressBookAvailability is of interest.</span></span> <span data-ttu-id="157f6-110">Dieser Parameter, der direkte Auswirkungen auf die für Clients verfügbaren Optionen hat, bietet drei mögliche Optionen:</span><span class="sxs-lookup"><span data-stu-id="157f6-110">This parameter, which directly impacts the options available to clients, has three possible options:</span></span>

  - <span data-ttu-id="157f6-111">WebSearchAndFileDownload</span><span class="sxs-lookup"><span data-stu-id="157f6-111">WebSearchAndFileDownload</span></span>

  - <span data-ttu-id="157f6-112">WebSearchOnly</span><span class="sxs-lookup"><span data-stu-id="157f6-112">WebSearchOnly</span></span>

  - <span data-ttu-id="157f6-113">FileDownloadOnly</span><span class="sxs-lookup"><span data-stu-id="157f6-113">FileDownloadOnly</span></span>

<span data-ttu-id="157f6-114">Nach der Definition wird bestimmt, wie der Zugriff auf das Adressbuch durch Clients erfolgt.</span><span class="sxs-lookup"><span data-stu-id="157f6-114">When defined, it determines how the Address Book is accessed by clients.</span></span> <span data-ttu-id="157f6-115">Wenn Sie diesen Parameter definieren, müssen Sie eine der Optionen definieren.</span><span class="sxs-lookup"><span data-stu-id="157f6-115">If you define this parameter, you must define one of the options.</span></span> <span data-ttu-id="157f6-116">Wenn Sie diese Einstellung nicht ändern, bleibt die standardmäßige WebSearchAndFileDownload in Kraft.</span><span class="sxs-lookup"><span data-stu-id="157f6-116">If you do not modify this setting, the default WebSearchAndFileDownload remains in effect.</span></span>

<span data-ttu-id="157f6-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="157f6-117">For example:</span></span>

    New-CsClientPolicy -Identity RedmondClientPolicy -DisableCalendarPresence $True -DisablePhonePresence $True -DisplayPhoto "PhotosFromADOnly" -AddressBookAvailability "WebSearchOnly"

<div>

## <a name="see-also"></a><span data-ttu-id="157f6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="157f6-118">See Also</span></span>


[<span data-ttu-id="157f6-119">Neu – CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="157f6-119">New-CsClientPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy)  
  

<span data-ttu-id="157f6-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="157f6-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

