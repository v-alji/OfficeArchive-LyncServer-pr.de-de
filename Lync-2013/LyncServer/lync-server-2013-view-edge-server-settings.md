---
title: 'Lync Server 2013: Anzeigen von Edgeserver-Einstellungen'
description: 'Lync Server 2013: Anzeigen von Edgeserver-Einstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Edge Server settings
ms:assetid: 684154cc-cffc-4d2e-8baa-be52c625e5d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747890(v=OCS.15)
ms:contentKeyID: 63969612
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4318b8c97f53f267bb79953af504977f6437214d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446285"
---
# <a name="view-edge-server-settings-in-lync-server-2013"></a><span data-ttu-id="00075-103">Anzeigen von Edgeserver-Einstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00075-103">View Edge Server settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00075-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00075-104">

<span> </span></span></span>

<span data-ttu-id="00075-105">_**Letztes Änderungsdatum des Themas:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="00075-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="00075-106">Allgemeine Edgeserver-Konfigurationen sollten anhand der Daten in der Konfigurationsverwaltungsdatenbank überprüft werden, um sicherzustellen, dass alle Änderungen gemäß den definierten Änderungskontrollverfahren dokumentiert wurden.</span><span class="sxs-lookup"><span data-stu-id="00075-106">General Edge Server configurations should be reviewed against the data in the configuration management database—to help guarantee that all changes were documented as per the defined change control procedures.</span></span>

<span data-ttu-id="00075-107">Weitere Prüfungen können die in den folgenden Abschnitten beschriebenen enthalten:</span><span class="sxs-lookup"><span data-stu-id="00075-107">Additional checks could include those that are described in the following sections:</span></span>

<div>

## <a name="verify-the-allow-and-block-lists"></a><span data-ttu-id="00075-108">Überprüfen der Listen "zulassen" und "blockieren"</span><span class="sxs-lookup"><span data-stu-id="00075-108">Verify the Allow and block lists</span></span>

<span data-ttu-id="00075-109">Überprüfen Sie die SIP-URI-Listen "zulassen" und "blockieren" für Verbunddomänen, um zu ermitteln, ob aufgelistete Namespaces weiterhin gültig sind.</span><span class="sxs-lookup"><span data-stu-id="00075-109">Verify the SIP URI "Allow" and "Block" lists for Federated domains—to determine whether listed namespaces are still valid.</span></span>

<span data-ttu-id="00075-110">Sie können Windows PowerShell verwenden, um die zulässigen und blockierten Listen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00075-110">You can use Windows PowerShell to view the allowed and blocked lists.</span></span> <span data-ttu-id="00075-111">Führen Sie den folgenden Windows PowerShell-Befehl aus, um die Domänen in der Liste zugelassene Domänen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="00075-111">To review the domains on the Allowed Domains list, run the following Windows PowerShell command:</span></span>

`Get-CsAllowedDomain`

<span data-ttu-id="00075-112">Dieser Befehl gibt ähnliche Informationen für die Domänen in der Liste der zulässigen Domänen zurück:</span><span class="sxs-lookup"><span data-stu-id="00075-112">That command returns information similar to this for the domains on the Allowed Domains list:</span></span>

<span data-ttu-id="00075-113">Identität: contoso.com</span><span class="sxs-lookup"><span data-stu-id="00075-113">Identity : contoso.com</span></span>

<span data-ttu-id="00075-114">Domäne: contoso.com</span><span class="sxs-lookup"><span data-stu-id="00075-114">Domain : contoso.com</span></span>

<span data-ttu-id="00075-115">ProxyFqdn :</span><span class="sxs-lookup"><span data-stu-id="00075-115">ProxyFqdn :</span></span>

<span data-ttu-id="00075-116">Kommentar</span><span class="sxs-lookup"><span data-stu-id="00075-116">Comment :</span></span>

<span data-ttu-id="00075-117">MarkForMonitoring: falsch</span><span class="sxs-lookup"><span data-stu-id="00075-117">MarkForMonitoring : False</span></span>

<span data-ttu-id="00075-118">Kommentar</span><span class="sxs-lookup"><span data-stu-id="00075-118">Comment :</span></span>

<span data-ttu-id="00075-119">Verwenden Sie den folgenden Befehl, um die Domänen in der Liste der blockierten Domänen zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="00075-119">To review the domains on the blocked domains list, use this command:</span></span>

`Get-CsBlockedDomain`

<span data-ttu-id="00075-120">Sie erhalten wiederum Informationen wie diesen für jede blockierte Domäne:</span><span class="sxs-lookup"><span data-stu-id="00075-120">In turn, you'll receive information such as this for each blocked domain:</span></span>

<span data-ttu-id="00075-121">Identität: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="00075-121">Identity : tailspintoys.com</span></span>

<span data-ttu-id="00075-122">Domäne: tailspintoys.com</span><span class="sxs-lookup"><span data-stu-id="00075-122">Domain : tailspintoys.com</span></span>

<span data-ttu-id="00075-123">Mit Windows PowerShell können Sie auch überprüfen, ob Sie eine Verbindung mit den Domänen in der Liste der zulässigen Domänen herstellen können.</span><span class="sxs-lookup"><span data-stu-id="00075-123">Windows PowerShell also enables you to verify that you can connection to the domains on your Allowed Domains list.</span></span> <span data-ttu-id="00075-124">Mit diesem Befehl wird beispielsweise die Verbindung zwischen Ihrem Edgeserver (dem TargetFqdn) und dem Verbunddomänen-contoso.com überprüft:</span><span class="sxs-lookup"><span data-stu-id="00075-124">For example, this command verifies the connection between your Edge Server (the TargetFqdn) and the federated domain contoso.com:</span></span>

`Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain "contoso.com"`

<span data-ttu-id="00075-125">Dieser Befehl überprüft die Verbindung zwischen Ihrem Edgeserver und allen Domänen, die in der Liste der zulässigen Domänen enthalten sind:</span><span class="sxs-lookup"><span data-stu-id="00075-125">And this command verifies the connection between your Edge Server and all of the domains found on your Allowed Domains list:</span></span>

`Get-CsAllowedDomain | ForEach-Object {Test-CsFederatedPartner -TargetFqdn "atl-edge-001.litwareinc.com" -Domain $_.Domain}`

</div>

<div>

## <a name="verify-multiple-edge-servers-are-identical"></a><span data-ttu-id="00075-126">Überprüfen, ob mehrere Edgeserver identisch sind</span><span class="sxs-lookup"><span data-stu-id="00075-126">Verify multiple Edge Servers are identical</span></span>

<span data-ttu-id="00075-127">Wenn mehrere Edgeserver in einem Lastenausgleichsarray bereitgestellt werden, sollten Sie überprüfen, ob alle Edgeserver im Array auf die gleiche Weise konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="00075-127">If multiple Edge Servers are deployed in a load balanced array, we recommend verifying that all Edge Servers in the array are configured in the same manner.</span></span>

<span data-ttu-id="00075-128">Sie können die Einstellungen für Edgeserver im Detailbereich der lync Server 2013-Erweiterung für das Computerverwaltungs-Snap-in anzeigen.</span><span class="sxs-lookup"><span data-stu-id="00075-128">You can view settings for Edge Servers in the details pane of the Lync Server 2013 extension for the Computer Management snap-in.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="00075-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00075-129">See Also</span></span>


[<span data-ttu-id="00075-130">Get-CsAllowedDomain</span><span class="sxs-lookup"><span data-stu-id="00075-130">Get-CsAllowedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAllowedDomain)  
[<span data-ttu-id="00075-131">Get-CsBlockedDomain</span><span class="sxs-lookup"><span data-stu-id="00075-131">Get-CsBlockedDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsBlockedDomain)  
[<span data-ttu-id="00075-132">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="00075-132">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
  

<span data-ttu-id="00075-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00075-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

