---
title: 'Lync Server 2013: Benutzerkonten, die für lync Server aktiviert sind'
description: 'Lync Server 2013: Benutzerkonten, die für lync Server aktiviert sind.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User accounts enabled for Lync Server 2013
ms:assetid: 8021087e-5084-4a39-9fef-ab9376c6d371
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182543(v=OCS.15)
ms:contentKeyID: 48184651
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf87177c378ffe61715d5332d2fd23b1d8e6fce6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394815"
---
# <a name="user-accounts-enabled-for-lync-server-2013"></a><span data-ttu-id="d8034-103">Für lync Server 2013 aktivierte Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="d8034-103">User accounts enabled for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8034-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8034-104">

<span> </span></span></span>

<span data-ttu-id="d8034-105">_**Letztes Änderungsdatum des Themas:** 2014-04-18_</span><span class="sxs-lookup"><span data-stu-id="d8034-105">_**Topic Last Modified:** 2014-04-18_</span></span>

<span data-ttu-id="d8034-106">Die Themen in diesem Abschnitt enthalten Schritt-für-Schritt-Verfahren zum Konfigurieren von Benutzereinstellungen, die Sie mit der lync Server 2013-Systemsteuerung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="d8034-106">Topics in this section provide step-by-step procedures for configuring user settings that you can perform using the Lync Server 2013 Control Panel.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="d8034-107">Sie können die lync Server-Systemsteuerung nicht zum Verwalten von Benutzern verwenden, die Mitglieder der Gruppe "Active Directory-Domänenadministratoren" sind.</span><span class="sxs-lookup"><span data-stu-id="d8034-107">You cannot use Lync Server Control Panel to manage users who are members of the Active Directory Domain Admins group.</span></span> <span data-ttu-id="d8034-108">Für Benutzer von Domänenadministratoren können Sie die lync Server-Systemsteuerung nur zum Durchführen von schreibgeschützten Suchvorgängen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8034-108">For Domain Admins users, you can use Lync Server Control Panel only to perform read-only search operations.</span></span> <span data-ttu-id="d8034-109">Wenn Sie Schreibvorgänge für Benutzer von Domänenadministratoren durchführen möchten (beispielsweise für die lync Server-Systemsteuerung aktivieren oder deaktivieren, Pool-oder Richtlinienzuweisungen ändern, Telefoneinstellungen, SIP-Adresse), müssen Sie Windows PowerShell-Cmdlets verwenden, während Sie als Domänenadministrator angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="d8034-109">To perform write operations on Domain Admins users (for example, enable or disable for Lync Server Control Panel, change pool or policy assignments, telephony settings, SIP address), you must use Windows PowerShell cmdlets while logged on as a Domain Admins user.</span></span> <span data-ttu-id="d8034-110">Details zur Verwendung von Windows PowerShell-Cmdlets zum Verwalten von Benutzern finden Sie unter <A href="lync-server-2013-lync-server-management-shell.md">lync Server 2013-Verwaltungsshell</A>.</span><span class="sxs-lookup"><span data-stu-id="d8034-110">For details about using Windows PowerShell cmdlets to manage users, see <A href="lync-server-2013-lync-server-management-shell.md">Lync Server 2013 Management Shell</A>.</span></span>



</div>

<span data-ttu-id="d8034-111">Wenn Sie eine beliebige lync Server 2013-Verwaltungsaufgabe ausführen, die die Suche nach einem Benutzer oder das Filtern von Benutzersuchergebnissen umfasst, gibt es einige Benutzereigenschaften, die in den Active Directory-Domänendiensten als Attribute vorhanden sind, aber erst nach der Bereitstellung von Microsoft Exchange Server in den globalen Katalog repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="d8034-111">When you perform any Lync Server 2013 administrative task that involves searching for a user or filtering user search results, there are some user properties that exist as attributes in Active Directory Domain Services but are not replicated to the global catalog until Microsoft Exchange Server is deployed.</span></span> <span data-ttu-id="d8034-112">Microsoft Exchange, nicht lync Server, kennzeichnet die folgenden Attribute für die Replikation beim globalen Katalog, wenn die Installation erfolgt:</span><span class="sxs-lookup"><span data-stu-id="d8034-112">Microsoft Exchange, not Lync Server, marks the following attributes for replication to the global catalog when it is installed:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8034-113">Benutzerinformationen</span><span class="sxs-lookup"><span data-stu-id="d8034-113">User Information</span></span></th>
<th><span data-ttu-id="d8034-114">Adresse und Telefon</span><span class="sxs-lookup"><span data-stu-id="d8034-114">Address and Phone</span></span></th>
<th><span data-ttu-id="d8034-115">Organisation</span><span class="sxs-lookup"><span data-stu-id="d8034-115">Organization</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8034-116">Initialen</span><span class="sxs-lookup"><span data-stu-id="d8034-116">Initials</span></span></p></td>
<td><p><span data-ttu-id="d8034-117">Straßenanschrift</span><span class="sxs-lookup"><span data-stu-id="d8034-117">Street address</span></span></p>
<p><span data-ttu-id="d8034-118">Land/Region</span><span class="sxs-lookup"><span data-stu-id="d8034-118">Country/region</span></span></p>
<p><span data-ttu-id="d8034-119">Pager</span><span class="sxs-lookup"><span data-stu-id="d8034-119">Pager</span></span></p>
<p><span data-ttu-id="d8034-120">Fax</span><span class="sxs-lookup"><span data-stu-id="d8034-120">Fax</span></span></p>
<p><span data-ttu-id="d8034-121">Mobil</span><span class="sxs-lookup"><span data-stu-id="d8034-121">Mobile</span></span></p></td>
<td><p><span data-ttu-id="d8034-122">Titel</span><span class="sxs-lookup"><span data-stu-id="d8034-122">Title</span></span></p>
<p><span data-ttu-id="d8034-123">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="d8034-123">Company</span></span></p>
<p><span data-ttu-id="d8034-124">Abteilung</span><span class="sxs-lookup"><span data-stu-id="d8034-124">Department</span></span></p>
<p><span data-ttu-id="d8034-125">Office</span><span class="sxs-lookup"><span data-stu-id="d8034-125">Office</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="d8034-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d8034-126">In This Section</span></span>

  - [<span data-ttu-id="d8034-127">Anzeigen von Informationen zu Benutzerkonten, die für lync Server 2013 aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="d8034-127">Viewing information about user accounts enabled for Lync Server 2013</span></span>](lync-server-2013-viewing-information-about-user-accounts-enabled-for-lync-server.md)

  - [<span data-ttu-id="d8034-128">Aktivieren und Deaktivieren von Benutzern für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-128">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)

  - [<span data-ttu-id="d8034-129">Verwalten von Enterprise-VoIP für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-129">Managing Enterprise Voice for users in Lync Server 2013</span></span>](lync-server-2013-managing-enterprise-voice-for-users.md)

  - [<span data-ttu-id="d8034-130">Ändern von Benutzerkontoeigenschaften in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-130">Modifying user account properties in Lync Server 2013</span></span>](lync-server-2013-modifying-user-account-properties.md)

  - [<span data-ttu-id="d8034-131">Verwalten von Richtlinien für den externen Zugriff für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-131">Manage external access policy in Lync Server 2013</span></span>](lync-server-2013-manage-external-access-policy-for-your-organization.md)

  - [<span data-ttu-id="d8034-132">Zuweisen von Richtlinien für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-132">Assigning per-user policies in Lync Server 2013</span></span>](lync-server-2013-assigning-per-user-policies.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d8034-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8034-133">See Also</span></span>


[<span data-ttu-id="d8034-134">Cmdlets für die Benutzerverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-134">User management cmdlets in Lync Server 2013</span></span>](lync-server-2013-user-management-cmdlets.md)  


[<span data-ttu-id="d8034-135">Verwalten von Benutzern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8034-135">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="d8034-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8034-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

