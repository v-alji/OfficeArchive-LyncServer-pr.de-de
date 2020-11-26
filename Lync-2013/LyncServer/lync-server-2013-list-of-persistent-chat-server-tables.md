---
title: 'Lync Server 2013: Liste der Tabellen für den Server für beständigen Chat'
description: 'Lync Server 2013: Liste der persistenten Chat Server Tabellen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of Persistent Chat Server tables
ms:assetid: 26c9e271-3516-4d90-b930-70fec4e359ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558628(v=OCS.15)
ms:contentKeyID: 48183659
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 838e6d8f83b137923075851b29df4c602a487391
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426585"
---
# <a name="list-of-persistent-chat-server-tables-in-lync-server-2013"></a><span data-ttu-id="5690c-103">Liste der Tabellen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5690c-103">List of Persistent Chat Server tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5690c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5690c-104">

<span> </span></span></span>

<span data-ttu-id="5690c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="5690c-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="5690c-106">Das Datenbank-Schema des beständigen Chats besteht aus den folgenden Tabellen.</span><span class="sxs-lookup"><span data-stu-id="5690c-106">The Persistent Chat database schema consists of the following tables.</span></span>

<div>

## <a name="active-directory-sync"></a><span data-ttu-id="5690c-107">Active Directory-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="5690c-107">Active Directory Sync</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5690c-108">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5690c-108">Table</span></span></th>
<th><span data-ttu-id="5690c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5690c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5690c-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-110"><a href="lync-server-2013-tbladcookie.md">tblADCookie in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-111">Enthält die aktuellen LDAP-Synchronisierungs Cookies (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="5690c-111">Contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span> <span data-ttu-id="5690c-112">Jede Zeile entspricht einer Active Directory-Domänendienst Domäne, die vom beständigen Chat Server aktiv auf Änderungen überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="5690c-112">Each row corresponds to an Active Directory Domain Services domain that Persistent Chat Server is actively monitoring for changes.</span></span> <span data-ttu-id="5690c-113">(In dieser Tabelle werden nur die Active Directory-Domänen dargestellt, die für den beständigen Chat Server relevant sind.)</span><span class="sxs-lookup"><span data-stu-id="5690c-113">(Only the Active Directory domains that are relevant for Persistent Chat Server are represented in this table.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-114"><a href="lync-server-2013-tblprincipalmemberdifference.md">tblPrincipalMemberDifference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-115">Enthält Änderungen an Gruppenmitgliedschaften (sowohl hinzugefügte als auch entfernte Mitglieder), die noch nicht von den späteren Active Directory-Synchronisierungs Schritten verarbeitet wurden und eine der temporären Tabellen (zusammen mit der tblADUpdates-Tabelle) sind, die im ersten Schritt der Active Directory-Synchronisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5690c-115">Contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with tblADUpdates table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="5690c-116">Mitgliedschaftsänderungen werden gespeichert, verarbeitet oder beides, nur für Gruppen, die in der tblPrincipal-Tabelle aufgelistet sind oder in denen bereits Mitglieder aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5690c-116">Membership changes are stored, processed, or both, only for groups that are listed in the tblPrincipal table or that already have members listed there.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-117"><a href="lync-server-2013-tbladupdates.md">tblADUpdates in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-118">Enthält Änderungen an Active Directory-Domänendiensten, die noch nicht von den späteren Active Directory-Synchronisierungs Schritten verarbeitet wurden und eine der temporären Tabellen (zusammen mit der tblPrincipalMemberDifference-Tabelle) sind, die im ersten Schritt der Active Directory-Synchronisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5690c-118">Contains changes to Active Directory Domain Services that have not yet been processed by the later Active Directory Sync steps and is one of the temporary tables (along with the tblPrincipalMemberDifference table) that is used in the first step of Active Directory Sync.</span></span></p>
<p><span data-ttu-id="5690c-119">Änderungen an Active Directory werden nur für Prinzipale gespeichert, verarbeitet oder beides, die bereits in der tblPrincipal-Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5690c-119">Changes to Active Directory are stored, processed, or both only for principals that are already listed in the tblPrincipal table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-120"><a href="lync-server-2013-tblprincipalmembers.md">tblPrincipalMembers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-121">Enthält Prinzipal Mitgliedschaften.</span><span class="sxs-lookup"><span data-stu-id="5690c-121">Contains principal memberships.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-122"><a href="lync-server-2013-tblprincipalmeta.md">tblPrincipalMeta in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-123">Enthält die Prinzipale, die aus Active Directory aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5690c-123">Contains the principals that have to be refreshed from Active Directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-124"><a href="lync-server-2013-tblskippedaffiliations.md">tblSkippedAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-125">Enthält Zugehörigkeiten, die aus irgendeinem Grund nicht aktualisiert werden konnten, in der Regel aufgrund von Active Directory-Zugriffsfehlern.</span><span class="sxs-lookup"><span data-stu-id="5690c-125">Contains affiliations that could not be refreshed for some reason, usually due to Active Directory access errors.</span></span></p>
<p><span data-ttu-id="5690c-126">Diese Tabelle dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="5690c-126">This table is for informational purposes only.</span></span> <span data-ttu-id="5690c-127">Der Inhalt wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5690c-127">Its content is not used.</span></span></p>
<p><span data-ttu-id="5690c-128">Die Prinzipale mit Zuordnungen, die nicht ordnungsgemäß aktualisiert werden konnten, werden in der tblPrincipalMeta-Tabelle aufbewahrt und erhalten eine weitere Chance, aktualisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="5690c-128">The principals with affiliations that could not be refreshed properly are kept in the tblPrincipalMeta table and are given another chance to be refreshed.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="principals-affiliations-nodes-scopes-and-roles"></a><span data-ttu-id="5690c-129">Prinzipale, Zuordnungen, Knoten, Bereiche und Rollen</span><span class="sxs-lookup"><span data-stu-id="5690c-129">Principals, Affiliations, Nodes, Scopes, and Roles</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5690c-130">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5690c-130">Table</span></span></th>
<th><span data-ttu-id="5690c-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5690c-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5690c-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-132"><a href="lync-server-2013-tblprincipaltype.md">tblPrincipalType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-133">Enthält Prinzipaltypen, um zu kategorisieren, was in der tblPrincipal-Tabelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5690c-133">Contains principal types to categorize what is in the tblPrincipal table.</span></span> <span data-ttu-id="5690c-134">Diese Tabelle ist statisch.</span><span class="sxs-lookup"><span data-stu-id="5690c-134">This table is static.</span></span> <span data-ttu-id="5690c-135">Sie wird während der Datenbankerstellung eingerichtet und ändert sich nicht.</span><span class="sxs-lookup"><span data-stu-id="5690c-135">It is set up during database creation and does not change.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-136"><a href="lync-server-2013-tblprincipal.md">tblPrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-137">Enthält alle Prinzipale (Benutzer, Ordner, Gruppen usw.).</span><span class="sxs-lookup"><span data-stu-id="5690c-137">Contains all principals (users, folders, groups, and so on).</span></span> <span data-ttu-id="5690c-138">Der Server für beständigen Chat behandelt dies als flache heterogene Liste.</span><span class="sxs-lookup"><span data-stu-id="5690c-138">Persistent Chat Server handles this as a flat heterogeneous list.</span></span> <span data-ttu-id="5690c-139">Verschiedene Spalten basieren auf dem Typ jedes Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="5690c-139">Various columns are based on the type of each principal.</span></span></p>
<p><span data-ttu-id="5690c-140">Bei den meisten dieser Prinzipale handelt es sich um zwischengespeicherte Kopien von Objekten, die in Active Directory gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="5690c-140">Most of these principals are cached copies of objects stored in Active Directory.</span></span> <span data-ttu-id="5690c-141">Das Erstellen der zwischengespeicherten Kopie in der Prinzipal Tabelle dieser Active Directory-Objekte wird als <em>Bereitstellung</em>bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5690c-141">Creating the cached copy in the Principal table of these Active Directory objects is referred as <em>provisioning</em>.</span></span></p>
<p><span data-ttu-id="5690c-142">Einige Prinzipale werden aggressiver als andere erstellt, und einige Active Directory-Objekte werden insgesamt ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5690c-142">Some principals are created more aggressively than others, and some Active Directory objects are ignored altogether.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-143"><a href="lync-server-2013-tblprincipalaffiliations.md">tblPrincipalAffiliations in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-144">Enthält Haupt Zuordnungen, die Mitgliedschaften in Active Directory-Sicherheitsgruppen, Active Directory-Container usw. beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5690c-144">Contains principal affiliations that describe memberships in Active Directory security groups, Active Directory containers, and so on.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-145"><a href="lync-server-2013-tblnode.md">tblNode in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-145"><a href="lync-server-2013-tblnode.md">tblNode in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-146">Enthält den Kategorie-Knoten, wie in der lync Server-Systemsteuerung verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5690c-146">Contains the category node, as managed in Lync Server Control Panel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-147"><a href="lync-server-2013-tblroletype.md">tblRoleType in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-147"><a href="lync-server-2013-tblroletype.md">tblRoleType in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-148">Enthält Rollentypen und die zugehörigen Berechtigungssätze.</span><span class="sxs-lookup"><span data-stu-id="5690c-148">Contains role types and their associated permission sets.</span></span> <span data-ttu-id="5690c-149">Diese Nachschlagetabelle ist statisch.</span><span class="sxs-lookup"><span data-stu-id="5690c-149">This lookup table is static.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-150"><a href="lync-server-2013-tblscopeprincipal.md">tblScopePrincipal in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-151">Enthält Bereiche, die Knoten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5690c-151">Contains scopes assigned to nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-152"><a href="lync-server-2013-tblprincipalrole.md">tblPrincipalRole in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-153">Enthält Rollen, die Knoten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="5690c-153">Contains roles assigned to nodes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-154"><a href="lync-server-2013-tblsiopwhitelist.md">tblSiopWhiteList in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-155">Enthält die registrierten Add-Ins, die Knoten zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="5690c-155">Contains the registered Add-ins that can be associated with nodes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-156"><a href="lync-server-2013-tblenumattribute.md">tblEnumAttribute in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-157">Enthält nur die hartcodierten &quot; Sichtbarkeits &quot; -und &quot; Verhaltens &quot; Attribute, die in der tblNode-Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5690c-157">Contains only the hardcoded &quot;Visibility&quot; and &quot;Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-158"><a href="lync-server-2013-tblenumvalue.md">tblEnumValue in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-159">Enthält die Werte der hartcodierten &quot; Sichtbarkeits-und Verhaltens &quot; Attribute, die in der tblNode-Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5690c-159">Contains the values of the hardcoded &quot;Visibility” and “Behavior&quot; attributes that are used in the tblNode table.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="invites-chats-and-other-client-support"></a><span data-ttu-id="5690c-160">Einladungen, Chats und andere Client Unterstützung</span><span class="sxs-lookup"><span data-stu-id="5690c-160">Invites, Chats, and Other Client Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5690c-161">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5690c-161">Table</span></span></th>
<th><span data-ttu-id="5690c-162">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5690c-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5690c-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-163"><a href="lync-server-2013-tblprincipalinvites.md">tblPrincipalInvites in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-164">Enthält Einladungen für alle bereitgestellten Benutzer im System für alle Knoten, bei denen die automatische Einladung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5690c-164">Contains invites for all provisioned users in the system for all nodes with Auto Invite enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-165"><a href="lync-server-2013-tblchat.md">tblChat in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-165"><a href="lync-server-2013-tblchat.md">tblChat in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-166">Enthält alle Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="5690c-166">Contains all chat messages.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-167"><a href="lync-server-2013-tbllastinviteid.md">tblLastInviteId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-168">Enthält die letzte Einladungs-ID, die für jeden Benutzer generiert (und in der tblPrincipalInvites-Tabelle verwendet) wurde.</span><span class="sxs-lookup"><span data-stu-id="5690c-168">Contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-169"><a href="lync-server-2013-tbllastchatid.md">tblLastChatId in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-170">Enthält die letzte Chat-ID, die für jeden Benutzer generiert (und in der tblChat-Tabelle verwendet) wurde.</span><span class="sxs-lookup"><span data-stu-id="5690c-170">Contains the last chat ID that was generated (and used in the tblChat table) for each user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-171"><a href="lync-server-2013-tblpreference.md">tblPreference in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-171"><a href="lync-server-2013-tblpreference.md">tblPreference in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-172">Enthält Benutzer-Client-Einstellungen (nur von Legacy-Clients verwendet).</span><span class="sxs-lookup"><span data-stu-id="5690c-172">Contains user client preferences (used by legacy clients only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-173"><a href="lync-server-2013-tblfiletoken.md">tblFileToken in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-174">Enthält temporäre Token für Datei Übertragungs Zwecke.</span><span class="sxs-lookup"><span data-stu-id="5690c-174">Contains temporary tokens for file transfer purposes.</span></span> <span data-ttu-id="5690c-175">Jedes Mal, wenn eine Datei hochgeladen oder heruntergeladen wird, generiert der beständige Chat Dienst ein Token, das der Client für den Zugriff auf den Webdienst-Dateispeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="5690c-175">Each time a file is uploaded or downloaded, the Persistent Chat service generates a token that the client uses to access the Web service file store.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="server-support"></a><span data-ttu-id="5690c-176">Serverunterstützung</span><span class="sxs-lookup"><span data-stu-id="5690c-176">Server Support</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5690c-177">Tabelle</span><span class="sxs-lookup"><span data-stu-id="5690c-177">Table</span></span></th>
<th><span data-ttu-id="5690c-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5690c-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5690c-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-179"><a href="lync-server-2013-tblserveridentity.md">tblServerIdentity in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-180">Enthält die aktiven Server im Server Pool für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="5690c-180">Contains the active servers in the Persistent Chat Server pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-181"><a href="lync-server-2013-tbladminlock.md">tblAdminLock in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-182">Enthält die administratorsperre zum Ausführen einiger Administrator Befehle.</span><span class="sxs-lookup"><span data-stu-id="5690c-182">Contains the administrator lock to run some administrator commands.</span></span> <span data-ttu-id="5690c-183">Der systemrevision-Eintrag in der tblSystemRevision-Tabelle wird nach jeder Version der Sperre inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="5690c-183">The system revision entry in the tblSystemRevision table is incremented after each release of the lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-184"><a href="lync-server-2013-tblsystemrevision.md">tblSystemRevision in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-185">Enthält den Eintrag für die Revisionsnummer (zusammen mit der tblAdminLock-Tabelle), um die Konsistenz auf mehreren Servern zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="5690c-185">Contains the revision number entry used (along with the tblAdminLock table) for achieving consistency across multiple servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5690c-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-186"><a href="lync-server-2013-tblactivepeers.md">tblActivePeers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-187">Enthält aktuelle Peer-to-Peer-Verbindungen zwischen beständigen Chat Diensten.</span><span class="sxs-lookup"><span data-stu-id="5690c-187">Contains current peer-to-peer connections between Persistent Chat services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5690c-188"><a href="lync-server-2013-tblconfig.md">tblConfig in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="5690c-188"><a href="lync-server-2013-tblconfig.md">tblConfig in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="5690c-189">Enthält die Konfiguration des beständigen Chat Servers, die nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5690c-189">Contains the Persistent Chat Server unsupported configuration.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5690c-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5690c-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

