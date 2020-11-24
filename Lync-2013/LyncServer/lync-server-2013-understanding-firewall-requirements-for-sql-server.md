---
title: 'Lync Server 2013: Grundlegendes zu den Firewallanforderungen für SQL Server'
description: 'Lync Server 2013: Grundlegendes zu den Firewall-Anforderungen für SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding firewall requirements for SQL Server
ms:assetid: 31d7df2c-589f-465e-be74-cf6767db190d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425818(v=OCS.15)
ms:contentKeyID: 48183781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c434474b36ced0fe64b9398f7d0e6136ff523a93
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394850"
---
# <a name="understanding-firewall-requirements-for-sql-server-with-lync-server-2013"></a><span data-ttu-id="7699d-103">Grundlegendes zu den Firewallanforderungen für SQL Server mit Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7699d-103">Understanding firewall requirements for SQL Server with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7699d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7699d-104">

<span> </span></span></span>

<span data-ttu-id="7699d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="7699d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="7699d-106">Bei einer Standard Edition-Bereitstellung werden Firewall-Ausnahmen beim Einrichten von lync Server 2013 automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="7699d-106">For a Standard Edition deployment, firewall exceptions are created automatically during Lync Server 2013 Setup.</span></span> <span data-ttu-id="7699d-107">Bei Enterprise Edition-Bereitstellungen müssen Sie die Firewall-Ausnahmen jedoch manuell auf dem SQL Server-Back-End-Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7699d-107">However, for Enterprise Edition deployments, you must configure the firewall exceptions manually on the SQL Server Back End Server.</span></span> <span data-ttu-id="7699d-108">Das TCP/IP-Protokoll ermöglicht es, einen bestimmten Port einmal für eine bestimmte IP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7699d-108">The TCP/IP protocol allows for a given port to be used once for a given IP address.</span></span> <span data-ttu-id="7699d-109">Das bedeutet, dass Sie für den SQL Server-basierten Server die standardmäßige Datenbankinstanz den standardmäßigen TCP-Port 1433 zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="7699d-109">This means that for the SQL Server-based server you can assign the default database instance the default TCP port 1433.</span></span> <span data-ttu-id="7699d-110">Für alle anderen Instanzen müssen Sie den SQL Server-Konfigurations-Manager verwenden, um eindeutige und nicht verwendete Ports zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7699d-110">For any other instances you will need to use the SQL Server Configuration Manager to assign unique and unused ports.</span></span> <span data-ttu-id="7699d-111">In diesem Thema wird Folgendes behandelt:</span><span class="sxs-lookup"><span data-stu-id="7699d-111">This topic covers:</span></span>

  - <span data-ttu-id="7699d-112">Voraussetzungen für eine Firewall-Ausnahme bei Verwendung der Standardinstanz</span><span class="sxs-lookup"><span data-stu-id="7699d-112">Requirements for a firewall exception when using the default instance</span></span>

  - <span data-ttu-id="7699d-113">Voraussetzungen für eine Firewall-Ausnahme für den SQL Server-Browser Dienst</span><span class="sxs-lookup"><span data-stu-id="7699d-113">Requirements for a firewall exception for the SQL Server Browser service</span></span>

  - <span data-ttu-id="7699d-114">Voraussetzungen für statische Abhör Anschlüsse bei Verwendung benannter Instanzen</span><span class="sxs-lookup"><span data-stu-id="7699d-114">Requirements for static listening ports when using named instances</span></span>

<div>

## <a name="requirements-for-a-firewall-exception-when-using-the-default-instance"></a><span data-ttu-id="7699d-115">Voraussetzungen für eine Firewall-Ausnahme bei Verwendung der Standardinstanz</span><span class="sxs-lookup"><span data-stu-id="7699d-115">Requirements for a Firewall Exception When Using the Default Instance</span></span>

<span data-ttu-id="7699d-116">Wenn Sie bei der Bereitstellung von lync Server 2013 die SQL Server-Standardinstanz für eine Datenbank verwenden, werden die folgenden Firewall-Regel Anforderungen verwendet, um die Kommunikation zwischen dem Front-End-Pool und der SQL Server-Standardinstanz zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="7699d-116">If you are using the SQL Server default instance for any database when deploying Lync Server 2013, the following firewall rule requirements are used to help ensure communication from the Front End pool to the SQL Server default instance.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7699d-117">Protokoll</span><span class="sxs-lookup"><span data-stu-id="7699d-117">Protocol</span></span></th>
<th><span data-ttu-id="7699d-118">Port</span><span class="sxs-lookup"><span data-stu-id="7699d-118">Port</span></span></th>
<th><span data-ttu-id="7699d-119">Richtung</span><span class="sxs-lookup"><span data-stu-id="7699d-119">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7699d-120">TCP</span><span class="sxs-lookup"><span data-stu-id="7699d-120">TCP</span></span></p></td>
<td><p><span data-ttu-id="7699d-121">1433</span><span class="sxs-lookup"><span data-stu-id="7699d-121">1433</span></span></p></td>
<td><p><span data-ttu-id="7699d-122">Eingehend zu SQL Server</span><span class="sxs-lookup"><span data-stu-id="7699d-122">Inbound to SQL Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-a-firewall-exception-for-the-sql-server-browser-service"></a><span data-ttu-id="7699d-123">Voraussetzungen für eine Firewall-Ausnahme für den SQL Server-Browser Dienst</span><span class="sxs-lookup"><span data-stu-id="7699d-123">Requirements for a Firewall Exception for the SQL Server Browser Service</span></span>

<span data-ttu-id="7699d-124">Der SQL Server-Browser Dienst findet Datenbankinstanzen und kommuniziert den Port, der für die Verwendung der Instanz (benannt oder Standard) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="7699d-124">The SQL Server Browser service will locate database instances and communicate the port that the instance (named or default) is configured to use.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7699d-125">Protokoll</span><span class="sxs-lookup"><span data-stu-id="7699d-125">Protocol</span></span></th>
<th><span data-ttu-id="7699d-126">Port</span><span class="sxs-lookup"><span data-stu-id="7699d-126">Port</span></span></th>
<th><span data-ttu-id="7699d-127">Richtung</span><span class="sxs-lookup"><span data-stu-id="7699d-127">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7699d-128">UDP</span><span class="sxs-lookup"><span data-stu-id="7699d-128">UDP</span></span></p></td>
<td><p><span data-ttu-id="7699d-129">1434</span><span class="sxs-lookup"><span data-stu-id="7699d-129">1434</span></span></p></td>
<td><p><span data-ttu-id="7699d-130">Inbound</span><span class="sxs-lookup"><span data-stu-id="7699d-130">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="requirements-for-static-listening-ports-when-using-named-instances"></a><span data-ttu-id="7699d-131">Voraussetzungen für statische Abhör Anschlüsse bei Verwendung benannter Instanzen</span><span class="sxs-lookup"><span data-stu-id="7699d-131">Requirements for Static Listening Ports When Using Named Instances</span></span>

<span data-ttu-id="7699d-132">Wenn Sie benannte Instanzen in der SQL Server-Konfiguration für Datenbanken verwenden, die lync Server 2013 unterstützen, konfigurieren Sie statische Ports mithilfe des SQL Server-Konfigurations-Managers.</span><span class="sxs-lookup"><span data-stu-id="7699d-132">When using named instances in the SQL Server configuration for databases supporting Lync Server 2013, you configure static ports by using SQL Server Configuration Manager.</span></span> <span data-ttu-id="7699d-133">Nachdem die statischen Ports jeder benannten Instanz zugewiesen wurden, erstellen Sie Ausnahmen für jeden statischen Port in der Firewall.</span><span class="sxs-lookup"><span data-stu-id="7699d-133">After the static ports have been assigned to each named instance, you create exceptions for each static port in the firewall.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7699d-134">Protokoll</span><span class="sxs-lookup"><span data-stu-id="7699d-134">Protocol</span></span></th>
<th><span data-ttu-id="7699d-135">Port</span><span class="sxs-lookup"><span data-stu-id="7699d-135">Port</span></span></th>
<th><span data-ttu-id="7699d-136">Richtung</span><span class="sxs-lookup"><span data-stu-id="7699d-136">Direction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7699d-137">TCP</span><span class="sxs-lookup"><span data-stu-id="7699d-137">TCP</span></span></p></td>
<td><p><span data-ttu-id="7699d-138">Statisch definiert</span><span class="sxs-lookup"><span data-stu-id="7699d-138">Statically defined</span></span></p></td>
<td><p><span data-ttu-id="7699d-139">Inbound</span><span class="sxs-lookup"><span data-stu-id="7699d-139">Inbound</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="sql-server-documentation"></a><span data-ttu-id="7699d-140">SQL Server-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7699d-140">SQL Server Documentation</span></span>

<span data-ttu-id="7699d-141">In der Microsoft SQL Server 2012-Dokumentation finden Sie detaillierte Anleitungen zum Konfigurieren des Firewall-Zugriffs für Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="7699d-141">Microsoft SQL Server 2012 documentation provides detailed guidance on how to configure firewall access for databases.</span></span> <span data-ttu-id="7699d-142">Details zu Microsoft SQL Server 2012 finden Sie unter "Konfigurieren der Windows-Firewall, um SQL Server-Zugriff zu ermöglichen" [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031) .</span><span class="sxs-lookup"><span data-stu-id="7699d-142">For details about Microsoft SQL Server 2012, see “Configuring the Windows Firewall to Allow SQL Server Access” at [https://go.microsoft.com/fwlink/p/?linkId=218031](https://go.microsoft.com/fwlink/p/?linkid=218031).</span></span>

<span data-ttu-id="7699d-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7699d-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

