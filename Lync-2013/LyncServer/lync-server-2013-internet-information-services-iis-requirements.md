---
title: 'Lync Server 2013: IIS-Anforderungen (Internetinformationsdienste)'
description: 'Lync Server 2013: Anforderungen für Internet Informationsdienste (IIS).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Internet Information Services (IIS) requirements
ms:assetid: 4f57a605-a8a9-4c5a-9a18-05ecb3d9ab6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398321(v=OCS.15)
ms:contentKeyID: 48184128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd8de55fa4611c3ab29eac7d7c28c522b418e77d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426861"
---
# <a name="internet-information-services-iis-requirements-in-lync-server-2013"></a><span data-ttu-id="6517a-103">IIS-Anforderungen (Internetinformationsdienste) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6517a-103">Internet Information Services (IIS) requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6517a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6517a-104">

<span> </span></span></span>

<span data-ttu-id="6517a-105">_**Letztes Änderungsdatum des Themas:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="6517a-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="6517a-106">Mehrere lync Server 2013-Komponenten erfordern Internet Informationsdienste (IIS).</span><span class="sxs-lookup"><span data-stu-id="6517a-106">Several Lync Server 2013 components require Internet Information Services (IIS).</span></span> <span data-ttu-id="6517a-107">In diesem Thema werden die speziellen IIS-Features beschrieben, die für die Unterstützung von lync Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6517a-107">This topic describes the specific IIS features required to support Lync Server.</span></span> <span data-ttu-id="6517a-108">In den Themen in diesem Abschnitt werden die Anforderungen bestimmter Komponenten für IIS beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6517a-108">The topics in this section describe the requirements of specific components for IIS.</span></span>

<span data-ttu-id="6517a-109">Wenn die Rolle des Webservers (IIS) unter Windows Server 2008 aktiviert ist, werden standardmäßig verschiedene Rollendienste installiert.</span><span class="sxs-lookup"><span data-stu-id="6517a-109">When the Web Server (IIS) role is enabled on Windows Server 2008, various role services are installed by default.</span></span> <span data-ttu-id="6517a-110">In der folgenden Tabelle werden die zusätzlichen Rollendienste beschrieben, die installiert werden müssen, wenn die Webserver (IIS)-Rolle unter Windows Server 2008 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6517a-110">The following table describes the additional role services that must be installed when the Web Server (IIS) role is enabled on Windows Server 2008.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6517a-111">Rollendienst</span><span class="sxs-lookup"><span data-stu-id="6517a-111">Role service</span></span></th>
<th><span data-ttu-id="6517a-112">Feature</span><span class="sxs-lookup"><span data-stu-id="6517a-112">Feature</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6517a-113">Allgemeine HTTP-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6517a-113">Common HTTP Features</span></span></p></td>
<td><p><span data-ttu-id="6517a-114">HTTP-Umleitung</span><span class="sxs-lookup"><span data-stu-id="6517a-114">HTTP Redirection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6517a-115">Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="6517a-115">Application Development</span></span></p></td>
<td><p><span data-ttu-id="6517a-116">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="6517a-116">ASP.NET</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6517a-117">Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="6517a-117">Application Development</span></span></p></td>
<td><p><span data-ttu-id="6517a-118">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="6517a-118">.NET Extensibility</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6517a-119">Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="6517a-119">Application Development</span></span></p></td>
<td><p><span data-ttu-id="6517a-120">ISAPI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="6517a-120">ISAPI Extensions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6517a-121">Anwendungsentwicklung</span><span class="sxs-lookup"><span data-stu-id="6517a-121">Application Development</span></span></p></td>
<td><p><span data-ttu-id="6517a-122">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="6517a-122">ISAPI Filters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6517a-123">Integrität und Diagnose</span><span class="sxs-lookup"><span data-stu-id="6517a-123">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="6517a-124">Protokollierungstools</span><span class="sxs-lookup"><span data-stu-id="6517a-124">Logging Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6517a-125">Integrität und Diagnose</span><span class="sxs-lookup"><span data-stu-id="6517a-125">Health and Diagnostics</span></span></p></td>
<td><p><span data-ttu-id="6517a-126">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="6517a-126">Tracing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6517a-127">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6517a-127">Security</span></span></p></td>
<td><p><span data-ttu-id="6517a-128">Standardauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="6517a-128">Basic Authentication</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6517a-129">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6517a-129">Security</span></span></p></td>
<td><p><span data-ttu-id="6517a-130">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6517a-130">Windows Authentication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6517a-131">Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="6517a-131">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="6517a-132">IIS-Verwaltungsskripts und -tools</span><span class="sxs-lookup"><span data-stu-id="6517a-132">IIS Management Scripts and Tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6517a-133">Verwaltungstools</span><span class="sxs-lookup"><span data-stu-id="6517a-133">Management Tools</span></span></p></td>
<td><p><span data-ttu-id="6517a-134">IIS 6-Verwaltungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="6517a-134">IIS 6 Management Compatibility</span></span></p></td>
</tr>
</tbody>
</table>


<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="Sicherheits" alt="security" /><span data-ttu-id="6517a-136">Sicherheitshinweis:</span><span class="sxs-lookup"><span data-stu-id="6517a-136">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6517a-137">Wenn Sie IIS 7,0 unter einem Windows Server 2008-Betriebssystem verwenden, deaktiviert das lync Server-Setup die Kernelmodus-Authentifizierung in IIS.</span><span class="sxs-lookup"><span data-stu-id="6517a-137">If you are using IIS 7.0 on a Windows Server 2008 operating system, Lync Server Setup disables kernel mode authentication in IIS.</span></span></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6517a-138">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6517a-138">In This Section</span></span>

  - [<span data-ttu-id="6517a-139">IIS-Anforderungen für Front-End-Pools und Standard Edition-Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6517a-139">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>](lync-server-2013-iis-requirements-for-front-end-pools-and-standard-edition-servers.md)

<span data-ttu-id="6517a-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6517a-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

