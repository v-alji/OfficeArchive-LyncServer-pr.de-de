---
title: 'Lync Server 2013: Erforderliche Gruppenmitgliedschaft'
description: 'Lync Server 2013: Anforderungen für die Gruppenmitgliedschaft.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group membership requirements
ms:assetid: 01876843-8717-4e72-baf5-866ac8cceee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204623(v=OCS.15)
ms:contentKeyID: 48183239
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f18fb6fbc782ecd41b7a782965f2cd6a82f6fd5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427838"
---
# <a name="group-membership-requirements-for-lync-server-2013"></a><span data-ttu-id="f0e17-103">Erforderliche Gruppenmitgliedschaft für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0e17-103">Group membership requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0e17-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0e17-104">

<span> </span></span></span>

<span data-ttu-id="f0e17-105">_**Letztes Änderungsdatum des Themas:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="f0e17-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="f0e17-106">In der folgenden Tabelle sind die Gruppen oder Gruppen zusammengefasst, zu denen eine Person gehören soll, um lync Server 2013 erfolgreich zu installieren, zu verwalten und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f0e17-106">The following table summarizes the group or groups that a person should belong to in order to successfully install, manage, and troubleshoot Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0e17-107">Lync Server 2013, ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="f0e17-107">Lync Server 2013 Executable</span></span></th>
<th><span data-ttu-id="f0e17-108">Gruppenmitgliedschaft erforderlich</span><span class="sxs-lookup"><span data-stu-id="f0e17-108">Group Membership Required</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0e17-109"><strong>Setup.exe</strong> – ausführbare Datei, mit der die Installation der lync Server 2013-Verwaltungstools gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f0e17-109"><strong>Setup.exe</strong> – Executable that starts the installation of the Lync Server 2013 administrative tools.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-110">Mitglied der lokalen Gruppe Administratoren auf dem Computer, auf dem die ausführbare Datei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0e17-110">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f0e17-111">Mitglied der Gruppe "Domänenbenutzer", um Informationen in den Active Directory-Domänendiensten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-111">Member of Domain Users group to read information in Active Directory Domain Services.</span></span> <span data-ttu-id="f0e17-112">Diese Berechtigungsstufe ist erforderlich, da für die automatische Installation erforderlicher MSI-Pakete auf dem lokalen Computer Berechtigungen erforderlich sind, die das Lesen und Schreiben von geschützten lokalen Computerressourcen wie Programmdatei Verzeichnissen und geschützte Registrierung, wie etwa die Hive des lokalen Computers, ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-112">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p>
<div>

> [!TIP]  
> <span data-ttu-id="f0e17-113">Sie können auch Setup Berechtigungen an Benutzer oder Gruppen delegieren, denen Sie nicht die Mitgliedschaft in der Gruppe Domänenadministratoren gewähren möchten.</span><span class="sxs-lookup"><span data-stu-id="f0e17-113">You can also delegate setup permissions to users or groups to whom you do not want to grant membership in the Domain Admins group.</span></span> <span data-ttu-id="f0e17-114">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-granting-setup-permissions.md">Gewähren von Setup Berechtigungen in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0e17-114">For details, see <A href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</A> in the Deployment documentation.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0e17-115"><strong>Deploy.exe</strong> – von setup.exe aufgerufen, ist deploy.exe für die Bereitstellung der Softwarekomponenten für die Serverrollen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="f0e17-115"><strong>Deploy.exe</strong> – Called by setup.exe, deploy.exe is responsible for the deployment of the software components for the server roles.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-116">Mitglied der lokalen Gruppe Administratoren auf dem Computer, auf dem die ausführbare Datei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0e17-116">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f0e17-117">Mitglied der Gruppe "Domänenbenutzer", um Informationen in AD DS zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-117">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="f0e17-118">Diese Berechtigungsstufe ist erforderlich, da für die automatische Installation erforderlicher MSI-Pakete auf dem lokalen Computer Berechtigungen erforderlich sind, die das Lesen und Schreiben von geschützten lokalen Computerressourcen wie Programmdatei Verzeichnissen und geschützte Registrierung, wie etwa die Hive des lokalen Computers, ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-118">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span> <span data-ttu-id="f0e17-119">Die Mitgliedschaft in der RtcUniversalReadOnlyAdmins-Gruppe ist erforderlich, um den zentralen Verwaltungsspeicher lesen zu können.</span><span class="sxs-lookup"><span data-stu-id="f0e17-119">Membership in RtcUniversalReadOnlyAdmins group is necessary to read the Central Management store.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="f0e17-120">Wenn Sie das BetriebssystemWindows Vista oder Windows 7 ausführen, werden Sie von der Benutzerkontensteuerung (User Account Control, UAC) aufgefordert, die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-120">If you are running the Windows Vista operating system or Windows 7 operating system, you will be prompted by User Account Control (UAC) to proceed with installation.</span></span> <span data-ttu-id="f0e17-121">Wenn Sie mit einem Standardbenutzerkonto angemeldet sind, benötigen Sie eine Person, die ein Mitglied der lokalen Gruppe Administratoren ist, um Anmeldeinformationen einzugeben, wenn Sie aufgefordert werden, ein Konto mit den Berechtigungen zum Installieren der Software einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f0e17-121">If you are logged on with a standard user account, you will need someone who is a member of the Local Administrators group to provide credentials when prompted for an account with permissions to install the software.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0e17-122"><strong>Bootstrapper.exe</strong> – von setup.exe aufgerufen, ist bootstrapper.exe für die Bereitstellung und Konfiguration von Serverrollen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="f0e17-122"><strong>Bootstrapper.exe</strong> – Called by setup.exe, bootstrapper.exe is responsible for deployment and configuration of server roles.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-123">Mitglied der lokalen Gruppe Administratoren auf dem Computer, auf dem die ausführbare Datei ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0e17-123">Member of the Local Administrators group on the computer from which the executable is run.</span></span> <span data-ttu-id="f0e17-124">Mitglied der RTCUniversalServerAdmins-Gruppe, um Bootstrapper.exe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-124">Member of the RTCUniversalServerAdmins group to run Bootstrapper.exe.</span></span> <span data-ttu-id="f0e17-125">Mitglied der Gruppe "Domänenbenutzer", um Informationen in AD DS zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-125">Member of Domain Users group to read information in AD DS.</span></span> <span data-ttu-id="f0e17-126">Diese Berechtigungsstufe ist erforderlich, da für die automatische Installation erforderlicher MSI-Pakete auf dem lokalen Computer Berechtigungen erforderlich sind, die das Lesen und Schreiben von geschützten lokalen Computerressourcen wie Programmdatei Verzeichnissen und geschützte Registrierung, wie etwa die Hive des lokalen Computers, ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-126">This level of permission is required because the automatic installation of required MSI packages on the local computer requires privileges that allow reading from and writing to protected local computer resources such as Program Files directories, and protected registry such as the Local Machine hive.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0e17-127"><strong>TopologyBuilder</strong> – Assistenten gesteuerte Benutzeroberfläche zum Erstellen, anzeigen, anpassen und Validieren von lync Server 2013-Topologien.</span><span class="sxs-lookup"><span data-stu-id="f0e17-127"><strong>TopologyBuilder</strong> – Wizard-driven user interface to create, view, adjust, and validate Lync Server 2013 topologies.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-128">Mitglied der lokalen Gruppe Administratoren auf dem Computer, auf dem die ausführbare Datei ausgeführt wird, um die Topologie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-128">Member of the Local Administrators group on the computer from which the executable is run to view the topology.</span></span> <span data-ttu-id="f0e17-129">Mitglied der RTCUniversalServerAdmins-Gruppe, um die Konfigurationseinstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f0e17-129">Member of the RTCUniversalServerAdmins group to change configuration settings.</span></span> <span data-ttu-id="f0e17-130">Mitglied der Gruppe "RTCUniversalServerAdmins", Gruppe "Domänen-Admins" oder Mitglied der RTCUniversalServerAdmins-Gruppe (nur, wenn der Gruppe Berechtigungen für die Stellvertretung erteilt wurden), um die Topologie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-130">Member of the RTCUniversalServerAdmins group and Domain Admins group, or member of the RTCUniversalServerAdmins group (only if the group has been granted delegate setup permissions), to publish the topology.</span></span> <span data-ttu-id="f0e17-131">Details zum Delegieren von Setup Berechtigungen, damit Mitglieder der RTCUniversalServerAdmins-Gruppe die Topologie veröffentlichen können, ohne Mitglieder der Gruppe "Domänen-Admins" zu sein, finden Sie unter <a href="lync-server-2013-granting-setup-permissions.md">Gewähren von Setup Berechtigungen in lync Server 2013</a> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0e17-131">For details about delegating setup permissions to allow members of the RTCUniversalServerAdmins group to publish the topology without being members of the Domain Admins group, see <a href="lync-server-2013-granting-setup-permissions.md">Granting setup permissions in Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0e17-132"><strong>AdminUIHost</strong> – webbasierte grafische Benutzeroberfläche für die Verwaltung von lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f0e17-132"><strong>AdminUIHost</strong> – Web-based graphical user interface for managing Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-133">Mitglied der CsAdministrator-Gruppe oder Mitglied einer anderen rollenbasierten zugriffssteuerungsrolle (Role-Based Access Control, RBAC), der die bestimmte administrative Aufgabe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f0e17-133">Member of CsAdministrator group or member of another role-based access control (RBAC) role to which the specific administrative task is assigned.</span></span> <span data-ttu-id="f0e17-134">Die lync Server 2013-Systemsteuerung implementiert Konfigurationsänderungen, indem Sie die lync Server 2013-Verwaltungsshell-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0e17-134">Lync Server 2013 Control Panel implements configuration changes by running Lync Server 2013 Management Shell cmdlets.</span></span> <span data-ttu-id="f0e17-135">Eine Liste der vordefinierten Rollen und die Cmdlets, die Mitglieder ausführen dürfen, finden Sie unter <a href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</a> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0e17-135">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0e17-136"><strong>PowerShell.exe mit dem lync Server 2013-Modul geladen</strong> – Befehlszeilen-Verwaltungstool mit Cmdlets, die für die Verwaltung von lync Server 2013 spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f0e17-136"><strong>PowerShell.exe with the Lync Server 2013 module loaded</strong> – Command-line administrative tool with cmdlets specific to management of Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="f0e17-137">Mitglied der CsAdministrator-Gruppe oder Mitglied einer anderen RBAC-Rolle, der das jeweilige Cmdlet zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f0e17-137">Member of CsAdministrator group or member of another RBAC role to which the specific cmdlet has been assigned.</span></span> <span data-ttu-id="f0e17-138">Eine Liste der vordefinierten Rollen und die Cmdlets, die Mitglieder ausführen dürfen, finden Sie unter <a href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</a> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0e17-138">For a list of predefined roles and the cmdlets members are permitted to run, see <a href="lync-server-2013-planning-for-role-based-access-control.md">Planning for role-based access control in Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="f0e17-139">Oder, abhängig vom Cmdlet, Mitglied einer oder mehrerer der folgenden Gruppen:</span><span class="sxs-lookup"><span data-stu-id="f0e17-139">Or, member of one or more of the following groups, depending on the cmdlet:</span></span></p>
<ul>
<li><p><span data-ttu-id="f0e17-140">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="f0e17-140">RTCUniversalServerAdmins</span></span></p></li>
<li><p><span data-ttu-id="f0e17-141">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="f0e17-141">RTCUniversalUserAdmins</span></span></p></li>
<li><p><span data-ttu-id="f0e17-142">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="f0e17-142">RTCUniversalReadOnlyAdmins</span></span></p></li>
</ul></td>
</tr><span data-ttu-id="f0e17-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0e17-143">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

