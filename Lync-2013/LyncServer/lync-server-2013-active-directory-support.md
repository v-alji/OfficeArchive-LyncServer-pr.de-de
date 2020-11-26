---
title: 'Lync Server 2013: Active Directory-Unterstützung'
description: Active Directory-Unterstützung für lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory support
ms:assetid: 28ed9ac4-586d-4803-ad45-99c4fa793f54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425756(v=OCS.15)
ms:contentKeyID: 48183679
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 349862b2f541ef3033c9a725a6ff04c6a4e219f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439408"
---
# <a name="active-directory-support-in-lync-server-2013"></a><span data-ttu-id="84573-103">Active Directory-Unterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="84573-103">Active Directory support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84573-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84573-104">

<span> </span></span></span>

<span data-ttu-id="84573-105">_**Letztes Änderungsdatum des Themas:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="84573-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="84573-106">Die lokalen Topologien für Active Directory-Domänendienste, die von lync Server 2013 unterstützt werden, sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="84573-106">The Active Directory Domain Services on-premises topologies that are supported by Lync Server 2013 are as follows:</span></span>

  - <span data-ttu-id="84573-107">Einzelne Gesamtstruktur mit einzelner Domäne</span><span class="sxs-lookup"><span data-stu-id="84573-107">Single forest with single domain</span></span>

  - <span data-ttu-id="84573-108">Einzelne Gesamtstruktur mit einer Struktur und mehreren Domänen</span><span class="sxs-lookup"><span data-stu-id="84573-108">Single forest with a single tree and multiple domains</span></span>

  - <span data-ttu-id="84573-109">Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammenhängenden Namespaces</span><span class="sxs-lookup"><span data-stu-id="84573-109">Single forest with multiple trees and disjoint namespaces</span></span>

  - <span data-ttu-id="84573-110">Mehrere Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="84573-110">Multiple forests in a central forest topology</span></span>

  - <span data-ttu-id="84573-111">Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="84573-111">Multiple forests in a resource forest topology</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="84573-112">Lync Server 2013 unterstützt keine Single-Label-Domänen.</span><span class="sxs-lookup"><span data-stu-id="84573-112">Lync Server 2013 does not support single-label domains.</span></span> <span data-ttu-id="84573-113">Beispielsweise wird eine Gesamtstruktur mit einer Stammdomäne mit dem Namen " <STRONG>contoso. local</STRONG> " unterstützt, aber eine Stammdomäne mit einer einzelnen Bezeichnung, die " <STRONG>local</STRONG> " heißt, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84573-113">For example, a forest with a root domain named <STRONG>contoso.local</STRONG> is supported, but a single-label root domain named <STRONG>local</STRONG> is not supported.</span></span> <span data-ttu-id="84573-114">Ausführliche Informationen finden Sie im Microsoft Knowledge Base-Artikel 300684, "Informationen zum Konfigurieren von Windows für Domänen mit DNS-Namen mit einer Bezeichnung" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A> .</span><span class="sxs-lookup"><span data-stu-id="84573-114">For details, see Microsoft Knowledge Base article 300684, "Information about configuring Windows for domains with single-label DNS names," at <A href="https://go.microsoft.com/fwlink/p/?linkid=143752">https://go.microsoft.com/fwlink/p/?linkId=143752</A>.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="84573-115">Lync Server 2013 unterstützt keine Umbenennung von Domänen.</span><span class="sxs-lookup"><span data-stu-id="84573-115">Lync Server 2013 does not support renaming domains.</span></span> <span data-ttu-id="84573-116">Wenn Sie eine Domäne umbenennen müssen, in der lync Server bereitgestellt wird, müssen Sie zunächst lync Server deinstallieren, dann die Domäne umbenennen und dann lync Server erneut installieren.</span><span class="sxs-lookup"><span data-stu-id="84573-116">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

<span data-ttu-id="84573-117">Ausführliche Informationen zu unterstützten Topologien und Anforderungen für lokale Bereitstellungen finden Sie unter [Anforderungen für Active Directory-Domänendienste, Unterstützung und Topologien in lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="84573-117">For details about supported topologies and requirements for on-premises deployments, see [Active Directory Domain Services requirements, support, and topologies in Lync Server 2013](lync-server-2013-active-directory-domain-services-requirements-support-and-topologies.md) in the Planning documentation.</span></span>

<span data-ttu-id="84573-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84573-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

