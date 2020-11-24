---
title: Cmdlets in Skype for Business Online, die den globalen Bereich und den Transponder Bereich verwenden
description: Cmdlets in Skype for Business Online, die den globalen Bereich und den Transponder Bereich verwenden.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use the global scope and the tag scope
ms:assetid: 1e2bc055-8a72-425e-967b-e253add7018c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362774(v=OCS.15)
ms:contentKeyID: 56558824
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba89ebe7322159027c5de765117afd366cb3dc23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394143"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-the-global-scope-and-the-tag-scope"></a><span data-ttu-id="346d3-103">Cmdlets in Skype for Business Online, die den globalen Bereich und den Transponder Bereich verwenden</span><span class="sxs-lookup"><span data-stu-id="346d3-103">Cmdlets in Skype for Business Online that use the global scope and the tag scope</span></span>

 


<span data-ttu-id="346d3-104">In Skype for Business Online können Richtlinien entweder im *globalen Bereich* oder auf dem *Transponder Bereich* (oder *pro Benutzerbereich*) konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="346d3-104">In Skype for Business Online, policies can be configured at either the *global scope* or at the *tag scope* (or *per-user scope*).</span></span> <span data-ttu-id="346d3-105">Wenn Sie die **Get-CS-** Cmdlets verwenden, müssen Sie keinen Bereich oder keine Identität angeben.</span><span class="sxs-lookup"><span data-stu-id="346d3-105">When using the **Get-Cs** cmdlets, you do not have to specify a scope or identity.</span></span> <span data-ttu-id="346d3-106">Wenn Sie eines dieser Cmdlets ohne Parameter aufrufen, werden alle relevanten Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="346d3-106">If you call one of these cmdlets without any parameters, then all the relevant items will be returned.</span></span> <span data-ttu-id="346d3-107">Dieser Befehl gibt beispielsweise Informationen zu allen ihren Richtlinien für den externen Zugriff zurück:</span><span class="sxs-lookup"><span data-stu-id="346d3-107">For example, this command returns information about all your external access policies:</span></span>

    Get-CsExternalAccessPolicy

<span data-ttu-id="346d3-108">Sie müssen nur den Parameter Identity oder den Filter-Parameter einbeziehen, wenn Sie die zurückgegebenen Daten einschränken möchten.</span><span class="sxs-lookup"><span data-stu-id="346d3-108">You need to include only the Identity parameter or the Filter parameter if you want to limit the returned data.</span></span> <span data-ttu-id="346d3-109">Wenn Sie beispielsweise nur die globale Richtlinie zurückgeben möchten, verwenden Sie diesen Befehl:</span><span class="sxs-lookup"><span data-stu-id="346d3-109">For example, to return only the global policy, use this command:</span></span>

    Get-CsExternalAccessPolicy -Identity "global"

<span data-ttu-id="346d3-110">Verwenden Sie den folgenden Befehl, um eine benutzerspezifische Richtlinie mit der Identität "RedmondAccessPolicy" zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="346d3-110">To return a per-user policy that has the Identity “RedmondAccessPolicy”, use this command:</span></span>

    Get-CsExternalAccessPolicy -Identity "RedmondAccessPolicy"


> [!NOTE]  
> <span data-ttu-id="346d3-111">Wenn Sie auf eine Richtlinie pro Benutzer verweisen, <STRONG>ist das Tagpräfix optional</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="346d3-111">When referencing a per-user policy, the tag <STRONG>prefix</STRONG> is optional.</span></span> <span data-ttu-id="346d3-112">Diese Syntax, die das Präfix enthält, ist ebenfalls gültig:</span><span class="sxs-lookup"><span data-stu-id="346d3-112">This syntax, which includes the prefix, is also valid:</span></span><BR><span data-ttu-id="346d3-113">Get-CsExternalAccessPolicy – Identity "Tag: RedmondAccessPolicy"</span><span class="sxs-lookup"><span data-stu-id="346d3-113">Get-CsExternalAccessPolicy –Identity "tag:RedmondAccessPolicy"</span></span>



<span data-ttu-id="346d3-114">Verwenden Sie diesen Befehl, um alle Richtlinien mit Ausnahme der globalen Richtlinien (also alle pro-Benutzer-Richtlinien) zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="346d3-114">To return all policies except the global policies (that is, all the per-user policies), use this command:</span></span>

    Get-CsExternalAccessPolicy -Filter "tag:*"

<span data-ttu-id="346d3-115">Die folgenden Cmdlets arbeiten sowohl für den globalen Bereich als auch für den Bereich pro Benutzer (Tag):</span><span class="sxs-lookup"><span data-stu-id="346d3-115">The following cmdlets operate against both the global scope and the per-user (tag) scope:</span></span>

  - <span data-ttu-id="346d3-116">[Get-CsClientPolicy](https://technet.microsoft.com/library/gg398830\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-116">[Get-CsClientPolicy](https://technet.microsoft.com/library/gg398830\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-117">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/gg398293\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-117">[Get-CsConferencingPolicy](https://technet.microsoft.com/library/gg398293\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-118">[Get-CsDialPlan](https://technet.microsoft.com/library/gg413043\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-118">[Get-CsDialPlan](https://technet.microsoft.com/library/gg413043\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-119">[Get-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425805\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-119">[Get-CsExternalAccessPolicy](https://technet.microsoft.com/library/gg425805\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg398348\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-120">[Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/library/gg398348\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-121">[Get-CsPresencePolicy](https://technet.microsoft.com/library/gg398463\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-121">[Get-CsPresencePolicy](https://technet.microsoft.com/library/gg398463\(v=ocs.15\))</span></span>

  - <span data-ttu-id="346d3-122">[Get-CsVoicePolicy](https://technet.microsoft.com/library/gg398101\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-122">[Get-CsVoicePolicy](https://technet.microsoft.com/library/gg398101\(v=ocs.15\))</span></span>


> [!NOTE]  
> <span data-ttu-id="346d3-123">Trotz des Namens sind die Wählpläne in der Regel Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="346d3-123">Despite the name, dial plans are, functionally speaking, policies.</span></span> <span data-ttu-id="346d3-124">Der Begriff <EM>Wählplan</EM> wird anstelle von Wähl Richtlinien verwendet, um die Terminologie beizubehalten, die in früheren Versionen von lync Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="346d3-124">The term <EM>dial plan</EM> is used instead of, for example, dialing policy, in order to preserve the terminology used with previous versions of Lync Server.</span></span>



## <a name="see-also"></a><span data-ttu-id="346d3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="346d3-125">See Also</span></span>


[<span data-ttu-id="346d3-126">Identitäten, Bereiche und Mandanten in Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="346d3-126">Identities, scopes, and tenants in Skype for Business Online</span></span>](identities-scopes-and-tenants-in-skype-for-business-online.md)  
<span data-ttu-id="346d3-127">[Die Lync Online-Cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="346d3-127">[The Skype for Business Online cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))</span></span>

