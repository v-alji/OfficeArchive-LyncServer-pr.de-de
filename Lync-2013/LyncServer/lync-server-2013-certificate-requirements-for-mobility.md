---
title: 'Lync Server 2013: Zertifikatanforderungen für die Mobilität'
description: 'Lync Server 2013: Zertifikatanforderungen für Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for mobility
ms:assetid: bb0e97af-cf60-4271-a0ab-654429d884ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690044(v=OCS.15)
ms:contentKeyID: 48185251
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 51af74b3efc1ffcb4fe38d7431e315f9b55af943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435362"
---
# <a name="certificate-requirements-for-mobility-in-lync-server-2013"></a><span data-ttu-id="5b264-103">Zertifikatanforderungen für die Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b264-103">Certificate requirements for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b264-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b264-104">

<span> </span></span></span>

<span data-ttu-id="5b264-105">_**Letztes Änderungsdatum des Themas:** 2012-06-24_</span><span class="sxs-lookup"><span data-stu-id="5b264-105">_**Topic Last Modified:** 2012-06-24_</span></span>

<span data-ttu-id="5b264-106">Wenn Sie das Mobilitätsfeature bereitstellen und die automatische Ermittlung für mobile Clients unterstützen, müssen Sie bestimmte Einträge für alternative Namen in Zertifikate einbeziehen, um sichere Verbindungen von den mobilen Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5b264-106">If you deploy the mobility feature and support automatic discovery for mobile clients, you need to include certain subject alternative name entries on certificates to support secure connections from the mobile clients.</span></span>

<span data-ttu-id="5b264-107">Sie müssen die Einträge für den alternativen Antragstellernamen für die automatische Ermittlung für die folgenden Zertifikate einbeziehen:</span><span class="sxs-lookup"><span data-stu-id="5b264-107">You need to include subject alternative name entries for automatic discovery on the following certificates:</span></span>

  - <span data-ttu-id="5b264-108">Directorpool</span><span class="sxs-lookup"><span data-stu-id="5b264-108">Director pool</span></span>

  - <span data-ttu-id="5b264-109">Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="5b264-109">Front End pool</span></span>

  - <span data-ttu-id="5b264-110">Reverseproxy</span><span class="sxs-lookup"><span data-stu-id="5b264-110">Reverse proxy</span></span>

<span data-ttu-id="5b264-111">In diesem Abschnitt werden die Einträge für Alternativen Betreff-Namen beschrieben, die für Ihre Zertifikate für die automatische Erkennung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5b264-111">This section describes the subject alternative name entries that are required on your certificates for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5b264-112">Das erneute Ausstellen von Zertifikaten mithilfe einer internen Zertifizierungsstelle ist in der Regel ein einfacher Vorgang, aber das Hinzufügen von mehreren alternativen Subjektnamen Einträgen zu öffentlichen Zertifikaten, die vom Reverse-Proxy verwendet werden, kann kostspielig sein.</span><span class="sxs-lookup"><span data-stu-id="5b264-112">Reissuing certificates by using an internal certificate authority is typically a simple process, but adding multiple subject alternative name entries to public certificates used by the reverse proxy can be expensive.</span></span> <span data-ttu-id="5b264-113">Wenn Sie über zahlreiche SIP-Domänen verfügen, die das Hinzufügen von alternativen Subjektnamen sehr teuer machen, können Sie den Reverseproxy so konfigurieren, dass er http für die anfängliche AutoErmittlungsdienst Anforderung verwendet, anstatt HTTPS (die Standardkonfiguration) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5b264-113">If you have many SIP domains, making the addition of subject alternative names very expensive, you can configure the reverse proxy to use HTTP for the initial Autodiscover Service request, instead of using HTTPS (the default configuration).</span></span> <span data-ttu-id="5b264-114">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-technical-requirements-for-mobility.md">Technische Voraussetzungen für Mobilität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5b264-114">For details, see <A href="lync-server-2013-technical-requirements-for-mobility.md">Technical requirements for mobility in Lync Server 2013</A>.</span></span>



</div>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="5b264-115">Anforderungen des Director-Pool Zertifikats</span><span class="sxs-lookup"><span data-stu-id="5b264-115">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b264-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b264-116">Description</span></span></th>
<th><span data-ttu-id="5b264-117">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="5b264-117">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b264-118">URL des internen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5b264-118">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="5b264-119">San = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-119">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b264-120">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5b264-120">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="5b264-121">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-121">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="5b264-122">Sie können auch San = \* verwenden. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-122">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="5b264-123">Anforderungen für das Front-End-Pool Zertifikat</span><span class="sxs-lookup"><span data-stu-id="5b264-123">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b264-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b264-124">Description</span></span></th>
<th><span data-ttu-id="5b264-125">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="5b264-125">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b264-126">URL des internen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5b264-126">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="5b264-127">San = lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-127">SAN=lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5b264-128">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5b264-128">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="5b264-129">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-129">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="5b264-130">Sie können auch San = \* verwenden. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-130">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="5b264-131">Zertifikatanforderungen für Reverse Proxy (öffentliche Zertifizierungsstelle)</span><span class="sxs-lookup"><span data-stu-id="5b264-131">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b264-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b264-132">Description</span></span></th>
<th><span data-ttu-id="5b264-133">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="5b264-133">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b264-134">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="5b264-134">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="5b264-135">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="5b264-135">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="5b264-136">Sie weisen dieses San dem Zertifikat zu, das dem SSL-Listener auf dem Reverse-Proxy zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5b264-136">You assign this SAN to the certificate assigned to the SSL Listener on the reverse proxy.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="5b264-137">Ihr Reverse Proxy-Listener weist Alternative Namen für die externen Webdienste-URLs auf (Beispiel: San = lyncwebextpool01. contoso. com und dirwebexternal.contoso.com, wenn Sie den optionalen Director bereitgestellt haben).</span><span class="sxs-lookup"><span data-stu-id="5b264-137">Your reverse proxy listener will have subject alternative names for your external Web Services URL(s) (for example, SAN=lyncwebextpool01.contoso.com, and dirwebexternal.contoso.com if you have deployed the optional Director).</span></span>



<span data-ttu-id="5b264-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b264-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

