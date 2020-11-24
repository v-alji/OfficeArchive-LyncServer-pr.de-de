---
title: Cmdlets in Skype for Business Online, die keinen Bereich oder keine Identität verwenden
description: Cmdlets in Skype for Business Online, die keinen Bereich oder keine Identität verwenden.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that do not use a scope or an identity
ms:assetid: 9c50c732-3c64-4b6a-96fd-8f528eb739ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362824(v=OCS.15)
ms:contentKeyID: 56558839
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7d893c4cf9203c8657dfbdfd7fb2bf46dbdfe4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394246"
---
# <a name="cmdlets-in-skype-for-business-online-that-do-not-use-a-scope-or-an-identity"></a><span data-ttu-id="55187-103">Cmdlets in Skype for Business Online, die keinen Bereich oder keine Identität verwenden</span><span class="sxs-lookup"><span data-stu-id="55187-103">Cmdlets in Skype for Business Online that do not use a scope or an identity</span></span>

 


<span data-ttu-id="55187-104">Die beim Ändern der zulässigen Listen und blockierten Listen verwendeten Cmdlets (Listen, die ermitteln, mit welchen externen Organisationen ihre Benutzer kommunizieren dürfen) verwenden weder einen Bereich noch eine Identität.</span><span class="sxs-lookup"><span data-stu-id="55187-104">The cmdlets used when modifying the allowed lists and blocked lists (lists that determine which outside organizations your users are allowed to communicate with) do not use either a scope or an Identity.</span></span> <span data-ttu-id="55187-105">In der Tat hat das Cmdlet **New-CsEdgeAllowAllKnownDomains** keinerlei Parameter.</span><span class="sxs-lookup"><span data-stu-id="55187-105">In fact, the **New-CsEdgeAllowAllKnownDomains** cmdlet does not have any parameters whatsoever.</span></span> <span data-ttu-id="55187-106">Bei den Cmdlets, die weder einen Bereich noch eine Identität verwenden, handelt es sich um folgende:</span><span class="sxs-lookup"><span data-stu-id="55187-106">The cmdlets that do not use either a scope or an Identity are:</span></span>

  - <span data-ttu-id="55187-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="55187-107">[New-CsEdgeAllowAllKnownDomains](https://technet.microsoft.com/library/jj994088\(v=ocs.15\))</span></span>

  - <span data-ttu-id="55187-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="55187-108">[New-CsEdgeAllowList](https://technet.microsoft.com/library/jj994023\(v=ocs.15\))</span></span>

  - <span data-ttu-id="55187-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="55187-109">[New-CsEdgeDomainPattern](https://technet.microsoft.com/library/jj994040\(v=ocs.15\))</span></span>

<span data-ttu-id="55187-110">Beachten Sie, dass Sie mit dem Cmdlet **New-CsEdgeAllowList** und dem Cmdlet **New-CsEdgeDomainPattern** den Parameter Domain angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="55187-110">Note that, with both the **New-CsEdgeAllowList** cmdlet and the **New-CsEdgeDomainPattern** cmdlet, you must include the Domain parameter.</span></span> <span data-ttu-id="55187-111">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="55187-111">For example:</span></span>

    $x = New-CsEdgeDomainPattern -Domain "fabrikam.com"

## <a name="see-also"></a><span data-ttu-id="55187-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55187-112">See Also</span></span>


[<span data-ttu-id="55187-113">Identitäten, Bereiche und Mandanten in Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="55187-113">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="55187-114">[Die Lync Online-Cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="55187-114">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

