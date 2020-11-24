---
title: 'Lync Server 2013: Bereitstellungsberechtigungen für SQL Server'
description: 'Lync Server 2013: Bereitstellungsberechtigungen für SQL Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment permissions for SQL Server
ms:assetid: 56ea0c02-bcf5-4d45-aa13-570531c29074
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398375(v=OCS.15)
ms:contentKeyID: 48184197
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be5985bc8f3173b03d8969d3dd58cfbf8daf85f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394927"
---
# <a name="deployment-permissions-for-sql-server-in-lync-server-2013"></a><span data-ttu-id="5886e-103">Bereitstellungsberechtigungen für SQL Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5886e-103">Deployment permissions for SQL Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5886e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5886e-104">

<span> </span></span></span>

<span data-ttu-id="5886e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="5886e-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="5886e-106">Microsoft SQL Server 2012 hat bestimmte Anforderungen beim Installieren und Bereitstellen von lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5886e-106">Microsoft SQL Server 2012 has specific requirements when installing and deploying Lync Server 2013.</span></span> <span data-ttu-id="5886e-107">Da Windows und SQL Server Ihre Sicherheit anders definieren, gewährt die Anmeldung als Administrator in der Active Directory-Domäne implizit keine Berechtigungen für SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5886e-107">Because Windows and SQL Server define their security differently, logging in as an administrator in the Active Directory domain does not implicitly grant permissions for SQL Server.</span></span> <span data-ttu-id="5886e-108">Sie müssen auch ein Mitglied der sysadmin-Entität auf dem SQL Server-basierten Server sein, den Sie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5886e-108">You must also be a member of the sysadmin entity on the SQL Server-based server you are configuring.</span></span>

<div>

## <a name="permissions-required-for-database-and-lync-server-installation"></a><span data-ttu-id="5886e-109">Für die Installation von Datenbank und lync Server erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="5886e-109">Permissions Required for Database and Lync Server Installation</span></span>

<span data-ttu-id="5886e-110">Die folgenden Optionen erläutern drei Berechtigungen und Gruppen Mitgliedschafts Zuordnungen für die Installation von lync Server 2013-Dateien und SQL Server-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5886e-110">The following options detail three permissions and group membership associations for installation of Lync Server 2013 files and SQL Server databases.</span></span> <span data-ttu-id="5886e-111">Wählen Sie das Szenario aus, das den Anforderungen Ihrer Organisation am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="5886e-111">Choose the scenario that best meets the requirements of your organization.</span></span>

### <a name="permissions-and-group-membership-associations"></a><span data-ttu-id="5886e-112">Berechtigungen und Gruppen Mitgliedschafts Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="5886e-112">Permissions and Group Membership Associations</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5886e-113">SQL Server-oder lync Server 2013-Rolle</span><span class="sxs-lookup"><span data-stu-id="5886e-113">SQL Server or Lync Server 2013 role</span></span></th>
<th><span data-ttu-id="5886e-114">Role-Typical von SQL Server-Berechtigungen und Gruppenmitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="5886e-114">Role-Typical SQL Server permissions and group membership</span></span></th>
<th><span data-ttu-id="5886e-115">Rollen typische lync Server 2013-Berechtigungen und Gruppenmitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="5886e-115">Role-typical Lync Server 2013 permissions and group membership</span></span></th>
<th><span data-ttu-id="5886e-116">Berechtigungs Ergebnis</span><span class="sxs-lookup"><span data-stu-id="5886e-116">Permissions outcome</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5886e-117">Lync Server 2013-Administrator</span><span class="sxs-lookup"><span data-stu-id="5886e-117">Lync Server 2013 administrator</span></span></p></td>
<td><p><span data-ttu-id="5886e-118">Es muss eine Mitgliedschaft in der SQL Server-Sicherheitsgruppe SysAdmins und Mitglied der Gruppe der lokalen Administratoren von SQL Server gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="5886e-118">Must be granted membership of sysadmins SQL Server security group and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="5886e-119">Muss ein Mitglied der RTCUniversalServerAdmins-Gruppe sein</span><span class="sxs-lookup"><span data-stu-id="5886e-119">Must be a member of the RTCUniversalServerAdmins group</span></span></p></td>
<td><p><span data-ttu-id="5886e-120">Der lync Server 2013-Administrator verfügt über die erforderlichen Berechtigungen zum Installieren von lync Server 2013-und SQL Server-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5886e-120">Lync Server 2013 administrator has the proper permissions to install both Lync Server 2013 and SQL Server databases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5886e-121">SQL Server-Administrator</span><span class="sxs-lookup"><span data-stu-id="5886e-121">SQL Server administrator</span></span></p></td>
<td><p><span data-ttu-id="5886e-122">SQL Server sysadmin-Gruppenmitglied (oder Äquivalent) und Mitglied der Gruppe der lokalen SQL Server-Administratoren</span><span class="sxs-lookup"><span data-stu-id="5886e-122">SQL Server sysadmin group member (or equivalent) and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="5886e-123">Muss ein Mitglied der RTCUniversalServerReadOnly-Gruppe sein</span><span class="sxs-lookup"><span data-stu-id="5886e-123">Must be a member of the RTCUniversalServerReadOnly group</span></span></p></td>
<td><p><span data-ttu-id="5886e-124">Der SQL Server-Administrator verfügt über die erforderlichen Berechtigungen zum Installieren von lync Server 2013-und SQL Server-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="5886e-124">SQL Server administrator has the proper permissions to install both Lync Server 2013 and SQL Server databases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5886e-125">Beide Administratoren Teilen Installationsaufgaben</span><span class="sxs-lookup"><span data-stu-id="5886e-125">Both administrators sharing installation duties</span></span></p></td>
<td><p><span data-ttu-id="5886e-126">Der SQL Server-Administrator ist Mitglied der Gruppe Sysadmins (oder Äquivalent) und Mitglied der Gruppe der lokalen Administratoren von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5886e-126">SQL Server administrator is member of sysadmins group (or equivalent) and member of the SQL Server local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="5886e-127">Lync Server 2013-Administrator ist Mitglied von RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="5886e-127">Lync Server 2013 administrator is member of RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="5886e-128">Der lync Server 2013-Administrator kann lync Server 2013 installieren, die Datenbankenkönnen aber nicht installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5886e-128">The Lync Server 2013 administrator can install Lync Server 2013, but cannot install the databases.</span></span> <span data-ttu-id="5886e-129">Der SQL Server-Administrator verwendet die lync Server-Verwaltungsshell und die Windows PowerShell-Cmdlets, die vom lync Server 2013-Administrator bereitgestellt werden, um die Datenbanken zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5886e-129">The SQL Server administrator uses the Lync Server Management Shell and Windows PowerShell cmdlets provided by the Lync Server 2013 administrator to install the databases.</span></span> <span data-ttu-id="5886e-130">Die vom SQL Server-Administrator verwendete lync Server 2013-Verwaltungsshell ist auf dem Front-End-Server installiert.</span><span class="sxs-lookup"><span data-stu-id="5886e-130">The Lync Server 2013 Management Shell used by the SQL Server administrator is installed on the Front End Server.</span></span> <span data-ttu-id="5886e-131">Dadurch entfällt die Notwendigkeit, die lync Server 2013-Verwaltungstools auf dem SQL Server-basierten Server zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5886e-131">This eliminates the need to install the Lync Server 2013 administrative tools on the SQL Server-based server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5886e-132">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5886e-132">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

