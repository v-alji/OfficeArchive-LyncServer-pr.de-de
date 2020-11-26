---
title: 'Lync Server 2013: von der Gesamtstrukturvorbereitung vorgenommene Änderungen'
description: 'Lync Server 2013: Änderungen, die von der Gesamtstrukturvorbereitung vorgenommen wurden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by forest preparation
ms:assetid: 2e12613e-59f2-4810-a32d-24a9789a4a6e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425791(v=OCS.15)
ms:contentKeyID: 48183734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c9bc40539c285e03610b2fc97166842473997fb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435075"
---
# <a name="changes-made-by-forest-preparation-in-lync-server-2013"></a><span data-ttu-id="f6010-103">Änderungen, die von der Gesamtstrukturvorbereitung in lync Server 2013 vorgenommen wurden</span><span class="sxs-lookup"><span data-stu-id="f6010-103">Changes made by forest preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6010-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6010-104">

<span> </span></span></span>

<span data-ttu-id="f6010-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="f6010-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="f6010-106">In diesem Abschnitt werden die globalen Einstellungen und Objekte sowie die Gruppen "Universeller Dienst" und "Verwaltung" beschrieben, die vom Gesamtstrukturvorbereitungsschritt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f6010-106">This section describes the global settings and objects, and the universal service and administration groups that are created by the forest preparation step.</span></span>

<div>

## <a name="active-directory-global-settings-and-objects"></a><span data-ttu-id="f6010-107">Globale Active Directory-Einstellungen und-Objekte</span><span class="sxs-lookup"><span data-stu-id="f6010-107">Active Directory Global Settings and Objects</span></span>

<span data-ttu-id="f6010-108">Wenn Sie globale Einstellungen im Konfigurationscontainer speichern (wie dies bei allen neuen lync Server 2013-Bereitstellungen der Fall ist), verwendet die Gesamtstrukturvorbereitung den vorhandenen Dienste-Container und fügt unter dem Configuration Services-Objekt ein **RTC-Dienst** Objekt hinzu \\ .</span><span class="sxs-lookup"><span data-stu-id="f6010-108">If you store global settings in the Configuration container (as is the case for all new Lync Server 2013 deployments), forest preparation uses the existing Services container and adds an **RTC Service** object under the Configuration\\Services object.</span></span> <span data-ttu-id="f6010-109">Unter dem RTC-Dienstobjekt fügt die Gesamtstrukturvorbereitung ein **globales Einstellungs** Objekt vom Typ Attribut msRTCSIP-Global Container hinzu.</span><span class="sxs-lookup"><span data-stu-id="f6010-109">Under the RTC Service object, forest preparation adds a **Global Settings** object of type msRTCSIP-GlobalContainer.</span></span> <span data-ttu-id="f6010-110">Das Global Settings-Objekt enthält alle Einstellungen, die für die lync Server-Bereitstellung gelten.</span><span class="sxs-lookup"><span data-stu-id="f6010-110">The global settings object holds all the settings that apply to the Lync Server deployment.</span></span> <span data-ttu-id="f6010-111">Wenn Sie globale Einstellungen im Systemcontainer speichern, verwendet die Gesamtstrukturvorbereitung einen Microsoft-Container unter dem Stammdomänen Systemcontainer und ein RTC-Dienstobjekt unter dem \\ Microsoft-Systemobjekt.</span><span class="sxs-lookup"><span data-stu-id="f6010-111">If you store global settings in the System container, forest preparation uses a Microsoft container under the root domain System container and an RTC Service object under the System\\Microsoft object.</span></span>

<span data-ttu-id="f6010-112">Bei der Gesamtstrukturvorbereitung wird auch ein neues **Attribut msRTCSIP-Domänen** Objekt für die Stammdomäne hinzugefügt, in der die Prozedur ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6010-112">Forest preparation also adds a new **msRTCSIP-Domain** object for the root domain in which the procedure is run.</span></span>

</div>

<div>

## <a name="active-directory-universal-service-and-administration-groups"></a><span data-ttu-id="f6010-113">Active Directory-universelle Dienst-und Verwaltungsgruppen</span><span class="sxs-lookup"><span data-stu-id="f6010-113">Active Directory Universal Service and Administration Groups</span></span>

<span data-ttu-id="f6010-114">Bei der Gesamtstrukturvorbereitung werden universelle Gruppen basierend auf der von Ihnen angegebenen Domäne erstellt und für diese Gruppen Zugriffssteuerungseinträge (ACEs) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6010-114">Forest preparation creates universal groups based on the domain that you specify and adds access control entries (ACEs) for these groups.</span></span> <span data-ttu-id="f6010-115">In diesem Schritt werden die universellen Gruppen in den Benutzer Containern der Domäne erstellt, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="f6010-115">This step creates the universal groups in the User containers of the domain that you specify.</span></span>

<span data-ttu-id="f6010-116">Universelle Gruppen ermöglichen Administratoren den Zugriff auf und die Verwaltung globaler Einstellungen und Dienste.</span><span class="sxs-lookup"><span data-stu-id="f6010-116">Universal groups allow administrators to access and manage global settings and services.</span></span> <span data-ttu-id="f6010-117">Bei der Gesamtstrukturvorbereitung werden die folgenden Typen von universellen Gruppen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="f6010-117">Forest preparation adds the following types of universal groups:</span></span>

  - <span data-ttu-id="f6010-118">**Administrative Gruppen**   Diese Gruppen definieren Administratorrollen für ein lync Server-Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="f6010-118">**Administrative groups**   These groups define administrator roles for a Lync Server network.</span></span>

  - <span data-ttu-id="f6010-119">**Infrastrukturgruppen**   Diese Gruppen bieten die Berechtigung für den Zugriff auf bestimmte Bereiche der lync Server-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="f6010-119">**Infrastructure groups**   These groups provide permission to access specific areas of the Lync Server infrastructure.</span></span> <span data-ttu-id="f6010-120">Sie funktionieren als Komponenten administrativer Gruppen.</span><span class="sxs-lookup"><span data-stu-id="f6010-120">They function as components of administrative groups.</span></span> <span data-ttu-id="f6010-121">Sie sollten diese Gruppen nicht ändern oder Benutzer direkt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6010-121">You should not modify these groups or add users directly to them.</span></span>

  - <span data-ttu-id="f6010-122">**Dienstgruppen**   Diese Gruppen sind Dienstkonten, die für den Zugriff auf verschiedene lync Server-Dienste erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f6010-122">**Service groups**   These groups are service accounts that are required to access various Lync Server services.</span></span>

<span data-ttu-id="f6010-123">In der folgenden Tabelle werden die administrativen Gruppen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6010-123">The following table describes the administrative groups.</span></span>

### <a name="administrative-groups-created-during-forest-preparation"></a><span data-ttu-id="f6010-124">Während der Gesamtstrukturvorbereitung erstellte administrative Gruppen</span><span class="sxs-lookup"><span data-stu-id="f6010-124">Administrative Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6010-125">Administrative Gruppe</span><span class="sxs-lookup"><span data-stu-id="f6010-125">Administrative group</span></span></th>
<th><span data-ttu-id="f6010-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6010-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6010-127">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="f6010-127">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="f6010-128">Ermöglicht Mitgliedern das Verwalten von Server-und Pooleinstellungen, einschließlich aller Serverrollen, globalen Einstellungen und Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f6010-128">Allows members to manage server and pool settings, including all server roles, global settings, and users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-129">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="f6010-129">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="f6010-130">Ermöglicht Mitgliedern, Benutzereinstellungen zu verwalten und Benutzer von einem Server oder Pool in einen anderen zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="f6010-130">Allows members to manage user settings and move users from one server or pool to another.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6010-131">RTCUniversalReadOnlyAdmins</span><span class="sxs-lookup"><span data-stu-id="f6010-131">RTCUniversalReadOnlyAdmins</span></span></p></td>
<td><p><span data-ttu-id="f6010-132">Ermöglicht Mitgliedern, Server-, Pool-und Benutzereinstellungen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f6010-132">Allows members to read server, pool, and user settings.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f6010-133">In der folgenden Tabelle werden die Infrastrukturgruppen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6010-133">The following table describes the infrastructure groups.</span></span>

### <a name="infrastructure-groups-created-during-forest-preparation"></a><span data-ttu-id="f6010-134">Während der Gesamtstrukturvorbereitung erstellte Infrastrukturgruppen</span><span class="sxs-lookup"><span data-stu-id="f6010-134">Infrastructure Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6010-135">Infrastrukturgruppe</span><span class="sxs-lookup"><span data-stu-id="f6010-135">Infrastructure group</span></span></th>
<th><span data-ttu-id="f6010-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6010-136">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6010-137">RTCUniversalGlobalWriteGroup</span><span class="sxs-lookup"><span data-stu-id="f6010-137">RTCUniversalGlobalWriteGroup</span></span></p></td>
<td><p><span data-ttu-id="f6010-138">Gewährt Schreibzugriff auf globale Einstellungsobjekte für lync Server.</span><span class="sxs-lookup"><span data-stu-id="f6010-138">Grants write access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-139">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="f6010-139">RTCUniversalGlobalReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="f6010-140">Gewährt schreibgeschützten Zugriff auf globale Einstellungsobjekte für lync Server.</span><span class="sxs-lookup"><span data-stu-id="f6010-140">Grants read-only access to global setting objects for Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6010-141">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="f6010-141">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="f6010-142">Gewährt schreibgeschützten Zugriff auf die lync Server-Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f6010-142">Grants read-only access to Lync Server user settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-143">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="f6010-143">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="f6010-144">Gewährt schreibgeschützten Zugriff auf lync Server-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f6010-144">Grants read-only access to Lync Server settings.</span></span> <span data-ttu-id="f6010-145">Diese Gruppe hat keinen Zugriff auf Einstellungen auf Poolebene, sondern nur auf Einstellungen, die für einen einzelnen Server spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="f6010-145">This group does not have access to pool level settings, only to settings specific to an individual server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6010-146">RTCUniversalSBATechnicians</span><span class="sxs-lookup"><span data-stu-id="f6010-146">RTCUniversalSBATechnicians</span></span></p></td>
<td><p><span data-ttu-id="f6010-147">Gewährt schreibgeschützten Zugriff auf die lync Server-Konfiguration und wird während der Installation in der lokalen Gruppe Administratoren der Überlebenden Branch-Appliances gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f6010-147">Grants read-only access to Lync Server configuration and are placed in the Local Administrators group of the survivable branch appliances during installation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f6010-148">In der folgenden Tabelle werden die Dienstgruppen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f6010-148">The following table describes the service groups.</span></span>

### <a name="service-groups-created-during-forest-preparation"></a><span data-ttu-id="f6010-149">Während der Gesamtstrukturvorbereitung erstellte Dienstgruppen</span><span class="sxs-lookup"><span data-stu-id="f6010-149">Service Groups Created During Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6010-150">Dienstgruppe</span><span class="sxs-lookup"><span data-stu-id="f6010-150">Service group</span></span></th>
<th><span data-ttu-id="f6010-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6010-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6010-152">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="f6010-152">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="f6010-153">Enthält Dienstkonten, mit denen Front-End-Server und Standard Edition-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f6010-153">Includes service accounts used to run Front End Server and Standard Edition servers.</span></span> <span data-ttu-id="f6010-154">Mit dieser Gruppe können Server Lese-und Schreibzugriff auf globale lync Server-Einstellungen und Active Directory-Benutzerobjekte erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6010-154">This group allows servers read/write access to Lync Server global settings and Active Directory user objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-155">RTCComponentUniversalServices</span><span class="sxs-lookup"><span data-stu-id="f6010-155">RTCComponentUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="f6010-156">Enthält Dienstkonten, die für die Ausführung von A/V-Konferenzservern, Webdiensten, Mediations Servern, Archivierungsservern und Überwachungs Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6010-156">Includes service accounts used to run A/V Conferencing Servers, Web Services, Mediation Server, Archiving Server, and Monitoring Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6010-157">RTCProxyUniversalServices</span><span class="sxs-lookup"><span data-stu-id="f6010-157">RTCProxyUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="f6010-158">Enthält Dienstkonten, die zum Ausführen von lync Server Edge-Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6010-158">Includes service accounts used to run Lync Server Edge Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-159">RTCUniversalConfigReplicator</span><span class="sxs-lookup"><span data-stu-id="f6010-159">RTCUniversalConfigReplicator</span></span></p></td>
<td><p><span data-ttu-id="f6010-160">Umfasst Server, die an der Replikation des lync Server Central-Verwaltungsspeichers teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="f6010-160">Includes servers that can participate in Lync Server Central Management store replication.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6010-161">RTCSBAUniversalServices</span><span class="sxs-lookup"><span data-stu-id="f6010-161">RTCSBAUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="f6010-162">Gewährt schreibgeschützten Zugriff auf lync Server-Einstellungen, ermöglicht aber die Konfiguration für die Installation eines überlebensfähigen Verzweigungs Servers und die Bereitstellung von Survivable Branch Appliances.</span><span class="sxs-lookup"><span data-stu-id="f6010-162">Grants read-only access to Lync Server settings, but allows for configuration for the installation of a survivable branch server and survivable branch appliance deployment.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f6010-163">Die Gesamtstrukturvorbereitung fügt dann den entsprechenden Infrastrukturgruppen Dienst-und Verwaltungsgruppen wie folgt hinzu:</span><span class="sxs-lookup"><span data-stu-id="f6010-163">Forest preparation then adds service and administration groups to the appropriate infrastructure groups, as follows:</span></span>

  - <span data-ttu-id="f6010-164">RTCUniversalServerAdmins wird zu RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup und RTCUniversalUserReadOnlyGroup hinzugefügt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6010-164">RTCUniversalServerAdmins is added to RTCUniversalGlobalReadOnlyGroup, RTCUniversalGlobalWriteGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="f6010-165">RTCUniversalUserAdmins wird als Mitglied von RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup und RTCUniversalUserReadOnlyGroup hinzugefügt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6010-165">RTCUniversalUserAdmins is added as a member of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

  - <span data-ttu-id="f6010-166">RTCHSUniversalServices, RTCComponentUniversalServices und RTCUniversalReadOnlyAdmins werden als Mitglieder von RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup und RTCUniversalUserReadOnlyGroup hinzugefügt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f6010-166">RTCHSUniversalServices, RTCComponentUniversalServices and RTCUniversalReadOnlyAdmins are added as members of RTCUniversalGlobalReadOnlyGroup, RTCUniversalServerReadOnlyGroup, and RTCUniversalUserReadOnlyGroup.</span></span>

<span data-ttu-id="f6010-167">Bei der Gesamtstrukturvorbereitung werden auch die folgenden rollenbasierten Zugriffssteuerungsgruppen erstellt:</span><span class="sxs-lookup"><span data-stu-id="f6010-167">Forest preparation also creates the following role-based access control (RBAC) groups:</span></span>

  - <span data-ttu-id="f6010-168">CSAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-168">CSAdministrator</span></span>

  - <span data-ttu-id="f6010-169">CSArchivingAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-169">CSArchivingAdministrator</span></span>

  - <span data-ttu-id="f6010-170">CSHelpDesk</span><span class="sxs-lookup"><span data-stu-id="f6010-170">CSHelpDesk</span></span>

  - <span data-ttu-id="f6010-171">CSLocationAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-171">CSLocationAdministrator</span></span>

  - <span data-ttu-id="f6010-172">CSResponseGroupAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-172">CSResponseGroupAdministrator</span></span>

  - <span data-ttu-id="f6010-173">CSServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-173">CSServerAdministrator</span></span>

  - <span data-ttu-id="f6010-174">CSUserAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-174">CSUserAdministrator</span></span>

  - <span data-ttu-id="f6010-175">CSViewOnlyAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-175">CSViewOnlyAdministrator</span></span>

  - <span data-ttu-id="f6010-176">CSVoiceAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6010-176">CSVoiceAdministrator</span></span>

  - <span data-ttu-id="f6010-177">CsPersistentChatAdministator</span><span class="sxs-lookup"><span data-stu-id="f6010-177">CsPersistentChatAdministator</span></span>

  - <span data-ttu-id="f6010-178">CsResponseGroupManager</span><span class="sxs-lookup"><span data-stu-id="f6010-178">CsResponseGroupManager</span></span>

<span data-ttu-id="f6010-179">Details zu den Rollen und den jeweils zulässigen Aufgaben finden Sie unter [Planen der rollenbasierten Zugriffssteuerung in lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f6010-179">For details about RBAC roles and the tasks allowed for each, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="f6010-180">Bei der Gesamtstrukturvorbereitung werden sowohl private als auch öffentliche ACEs erstellt.</span><span class="sxs-lookup"><span data-stu-id="f6010-180">Forest preparation creates both private and public ACEs.</span></span> <span data-ttu-id="f6010-181">Es werden private ACEs im Container für globale Einstellungen erstellt, der von lync Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6010-181">It creates private ACEs on the global settings container used by Lync Server.</span></span> <span data-ttu-id="f6010-182">Dieser Container wird nur von lync Server verwendet und befindet sich entweder im Konfigurationscontainer oder im System Container in der Stammdomäne, je nachdem, wo Sie die globalen Einstellungen speichern.</span><span class="sxs-lookup"><span data-stu-id="f6010-182">This container is used only by Lync Server and is located either in the Configuration container or the System container in the root domain, depending on where you store global settings.</span></span> <span data-ttu-id="f6010-183">Die von der Gesamtstrukturvorbereitung erstellten öffentlichen ACEs sind in der folgenden Tabelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f6010-183">The public ACEs created by forest preparation are listed in the following table.</span></span>

### <a name="public-aces-created-by-forest-preparation"></a><span data-ttu-id="f6010-184">Von der Gesamtstrukturvorbereitung erstellte öffentliche ACEs</span><span class="sxs-lookup"><span data-stu-id="f6010-184">Public ACEs created by Forest Preparation</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6010-185">ACE</span><span class="sxs-lookup"><span data-stu-id="f6010-185">ACE</span></span></th>
<th><span data-ttu-id="f6010-186">RTCUniversalGlobalReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="f6010-186">RTCUniversalGlobalReadOnlyGroup</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6010-187">Read Root Domain System Container (nicht geerbt)<strong>\*</strong></span><span class="sxs-lookup"><span data-stu-id="f6010-187">Read root domain System Container (not inherited)<strong>\*</strong></span></span></p></td>
<td><p><span data-ttu-id="f6010-188">X</span><span class="sxs-lookup"><span data-stu-id="f6010-188">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6010-189">Lesen des DisplaySpecifiers-Containers der Konfiguration (nicht geerbt)</span><span class="sxs-lookup"><span data-stu-id="f6010-189">Read Configuration’s DisplaySpecifiers container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="f6010-190">X</span><span class="sxs-lookup"><span data-stu-id="f6010-190">X</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="f6010-191"><STRONG>\*</STRONG>Nicht geerbte ACEs gewähren unter diesen Containern keinen Zugriff auf untergeordnete Objekte.</span><span class="sxs-lookup"><span data-stu-id="f6010-191"><STRONG>\*</STRONG>ACEs that are not inherited do not grant access to child objects under these containers.</span></span> <span data-ttu-id="f6010-192">ACEs, die geerbt werden, gewähren Zugriff auf untergeordnete Objekte unter diesen Containern.</span><span class="sxs-lookup"><span data-stu-id="f6010-192">ACEs that are inherited grant access to child objects under these containers.</span></span>



</div>

<span data-ttu-id="f6010-193">Im Konfigurationscontainer führt die Gesamtstrukturvorbereitung unter dem Konfigurationsnamenskontext die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="f6010-193">On the Configuration container, under the Configuration naming context, forest preparation performs the following tasks:</span></span>

  - <span data-ttu-id="f6010-194">Fügt einen Eintrag **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** für die **RTC-Eigenschaften** Seite unter den Attributen adminContextMenu und adminPropertyPages des Sprachanzeige Bezeichners für Benutzer, Kontakte und InetOrgPersons hinzu (beispielsweise CN = User-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="f6010-194">Adds an entry **{AB255F23-2DBD-4bb6-891D-38754AC280EF}** for the **RTC property** page under the adminContextMenu and adminPropertyPages attributes of the language display specifier for users, contacts, and InetOrgPersons (for example, CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="f6010-195">Fügt unter **Erweiterte Rechte** , die für die Benutzer-und Kontaktklassen gelten, ein **RTCPropertySet** -Objekt vom Typ **controlAccessRight** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f6010-195">Adds an **RTCPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to the User and Contact classes.</span></span>

  - <span data-ttu-id="f6010-196">Fügt unter **Erweiterte Rechte** , die für Benutzer-, Kontakt-, ou-und domainDNS-Klassen gelten, ein **RTCUserSearchPropertySet** -Objekt vom Typ **controlAccessRight** hinzu.</span><span class="sxs-lookup"><span data-stu-id="f6010-196">Adds an **RTCUserSearchPropertySet** object of type **controlAccessRight** under **Extended-Rights** that applies to User, Contact, OU, and DomainDNS classes.</span></span>

  - <span data-ttu-id="f6010-197">Fügt **Attribut msRTCSIP-PrimaryUserAddress** unter dem **extraColumns** -Attribut der einzelnen Organisations Einheits Anzeigebezeichner (z. b. CN = organizationalUnit-Display, CN = 409, CN = DisplaySpecifiers) hinzu und kopiert die Werte des **extraColumns** -Attributs der Standardanzeige (beispielsweise CN = default-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="f6010-197">Adds **msRTCSIP-PrimaryUserAddress** under the **extraColumns** attribute of each language organizational unit (OU) display specifier (for example, CN=organizationalUnit-Display,CN=409,CN=DisplaySpecifiers) and copies the values of the **extraColumns** attribute of the default display (for example, CN=default-Display, CN=409,CN=DisplaySpecifiers).</span></span>

  - <span data-ttu-id="f6010-198">Fügt **Attribut msRTCSIP-PrimaryUserAddress**-, **Attribut msRTCSIP-PrimaryHomeServer**-und **Attribut msRTCSIP-UserEnabled-** Filterattribute unter dem **attributeDisplayNames** -Attribut der einzelnen Sprachanzeige Bezeichner für Benutzer, Kontakte und InetOrgPerson-Objekte hinzu (beispielsweise in Englisch: CN = User-Display, CN = 409, CN = DisplaySpecifiers).</span><span class="sxs-lookup"><span data-stu-id="f6010-198">Adds **msRTCSIP-PrimaryUserAddress**, **msRTCSIP-PrimaryHomeServer**, and **msRTCSIP-UserEnabled** filtering attributes under the **attributeDisplayNames** attribute of each language display specifier for Users, Contacts, and InetOrgPerson objects (for example, in English: CN=user-Display,CN=409,CN=DisplaySpecifiers).</span></span>

<span data-ttu-id="f6010-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6010-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

