---
title: 'Lync Server 2013: Aktivieren oder Deaktivieren von Hot Desking'
description: 'Lync Server 2013: Aktivieren oder Deaktivieren der Hot-Desk-Funktion.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable hot desking
ms:assetid: 93a7fed6-f61a-4b41-9336-a8320afa87cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994057(v=OCS.15)
ms:contentKeyID: 51803968
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3fd22c9bf51078324cfe5e215bd154503c2d9b57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393982"
---
# <a name="enable-or-disable-hot-desking-in-lync-server-2013"></a><span data-ttu-id="c019b-103">Aktivieren oder Deaktivieren von Hot Desking in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c019b-103">Enable or disable hot desking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c019b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c019b-104">

<span> </span></span></span>

<span data-ttu-id="c019b-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="c019b-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="c019b-106">Sie können Telefone im öffentlichen Bereich als *Hot-Desk-Telefone* einrichten.</span><span class="sxs-lookup"><span data-stu-id="c019b-106">You can set up common area phones as *hot-desk phones*.</span></span> <span data-ttu-id="c019b-107">Mit Hot-Desk-Telefonen können sich Benutzer bei Ihrem eigenen Benutzerkonto anmelden und nach der Anmeldung die lync Server-Features und ihre eigenen Benutzerprofileinstellungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c019b-107">With hot-desk phones, users can log on to their own user account, and, after they are logged on, use Lync Server features and their own user profile settings.</span></span> <span data-ttu-id="c019b-108">Hot-Desking wird mithilfe von Clientrichtlinien verwaltet: zum Aktivieren oder Deaktivieren der Hot-Desk-Funktion müssen Sie die Clientrichtlinien ändern, die von ihren Telefonen im öffentlichen Bereich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c019b-108">Hot desking is managed by using client policies: to enable or disable hot desking, you need to modify the client policies that are used by your common area phones.</span></span> <span data-ttu-id="c019b-109">Details zum Ermitteln der Konferenzrichtlinien, die ihren Telefonen im öffentlichen Bereich zugewiesen wurden, finden Sie unter [Anzeigen von allgemeinen Telefon Informationen in lync Server 2013](lync-server-2013-view-common-area-phone-information.md).</span><span class="sxs-lookup"><span data-stu-id="c019b-109">For details about how to determine the conferencing policies that have been assigned to your common area phones, see [View common area phone information in Lync Server 2013](lync-server-2013-view-common-area-phone-information.md).</span></span>

<span data-ttu-id="c019b-110">Sie verwenden den EnableHotdesking-Parameter des Cmdlets **New-CSClientPolicy** oder das Cmdlet " **Satz-CSClientPolicy** ", um die Hot-Desk-Funktion auf einem Smartphone wie folgt zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c019b-110">You use the EnableHotdesking parameter of the **New-CSClientPolicy** cmdlet or the **Set-CSClientPolicy** cmdlet to enable or disable hot desking on a phone, as follows.</span></span> <span data-ttu-id="c019b-111">Führen Sie diese Cmdlets entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell aus.</span><span class="sxs-lookup"><span data-stu-id="c019b-111">Run these cmdlets from either the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="c019b-112">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="c019b-112">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>


<div>

## <a name="enabling-hot-desking"></a><span data-ttu-id="c019b-113">Aktivieren von Hot-Desking</span><span class="sxs-lookup"><span data-stu-id="c019b-113">Enabling hot desking</span></span>

  - <span data-ttu-id="c019b-114">Wenn Sie die Hot-Desk-Funktion für ein Telefon im öffentlichen Bereich aktivieren möchten, müssen Sie die Clientrichtlinie ändern, die diesem Telefon (oder einer Sammlung von Telefonen) zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c019b-114">To enable hot desking for a common area phone, you must modify the client policy that has been assigned to that phone (or collection of phones).</span></span>
    
    <span data-ttu-id="c019b-115">Nachdem Sie die zu ändernde Richtlinie identifiziert haben, besteht der nächste Schritt darin, das Cmdlet " **setCsClientPolicy** " zu verwenden, um den EnableHotdesking-Parameter auf "true" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c019b-115">After you have identified the policy that needs to be modified, the next step is to use the **Set-CsClientPolicy** cmdlet to set the EnableHotdesking parameter to True.</span></span> <span data-ttu-id="c019b-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c019b-116">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $True

  - <span data-ttu-id="c019b-117">Alternativ können Sie das Cmdlet **New-CsClientPolicy** verwenden, um eine neue Clientrichtlinie zu erstellen, die eine Hot-Desk-Funktion ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c019b-117">Alternatively, you can use the **New-CsClientPolicy** cmdlet to create a new client policy that enables hot desking.</span></span> <span data-ttu-id="c019b-118">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c019b-118">For example:</span></span>
    
        New-CsClientPolicy -Identity "NewCommonAreaPhonePolicy" - EnableHotdesking $True

</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c019b-119">Nachdem diese Richtlinie erstellt wurde, müssen Sie Sie den entsprechenden Telefonen im öffentlichen Bereich zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c019b-119">After this policy has been created, you must assign it to the appropriate common area phones.</span></span> <span data-ttu-id="c019b-120">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">Zuweisen von Richtlinien in lync Server 2013 zu einem gemeinsamen Bereichs Telefon</A>.</span><span class="sxs-lookup"><span data-stu-id="c019b-120">For details, see <A href="lync-server-2013-assign-policies-to-a-common-area-phone.md">Assign policies in Lync Server 2013 to a common area phone</A>.</span></span>



</div>

<div>

## <a name="disabling-hot-desking"></a><span data-ttu-id="c019b-121">Deaktivieren des Hot-Desking</span><span class="sxs-lookup"><span data-stu-id="c019b-121">Disabling hot desking</span></span>

  - <span data-ttu-id="c019b-122">Um die Hot-Desk-Funktion für ein Telefon im öffentlichen Bereich zu deaktivieren, setzen Sie den EnableHotdesking-Parameter des Cmdlets " **CsClientPolicy** " auf den Standardwert false zurück.</span><span class="sxs-lookup"><span data-stu-id="c019b-122">To disable hot desking for a common area phone, reset the EnableHotdesking parameter of the **Set-CsClientPolicy** cmdlet to the default value of False.</span></span> <span data-ttu-id="c019b-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c019b-123">For example:</span></span>
    
        Set-CsClientPolicy -Identity "CommonAreaPhonePolicy" - EnableHotdesking $False

</div>

<span data-ttu-id="c019b-124">Ausführliche Informationen finden Sie in den Hilfethemen zum Cmdlet [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) und dem Cmdlet " [Satz-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) ".</span><span class="sxs-lookup"><span data-stu-id="c019b-124">For details, see the Help topics for the [New-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsClientPolicy) cmdlet and the [Set-CsClientPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsClientPolicy) cmdlet.</span></span>

<span data-ttu-id="c019b-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c019b-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

