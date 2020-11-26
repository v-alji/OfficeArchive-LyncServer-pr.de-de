---
title: 'Lync Server 2013: Schema Attribute und Beschreibungen'
description: 'Lync Server 2013: Schema Attribute und Beschreibungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema attributes and descriptions
ms:assetid: b009df76-9c22-471d-b57a-bda009a98261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412841(v=OCS.15)
ms:contentKeyID: 48185083
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18888d20a772b3e84970e7d874bd6b6964affc75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444959"
---
# <a name="schema-attributes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="3b159-103">Schema Attribute und Beschreibungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b159-103">Schema attributes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b159-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b159-104">

<span> </span></span></span>

<span data-ttu-id="3b159-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="3b159-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="3b159-106">In diesem Abschnitt werden alle Schema Attribute beschrieben, die von lync Server 2013 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-106">This section describes all the schema attributes used by Lync Server 2013.</span></span> <span data-ttu-id="3b159-107">Informationen zu den Klassen, die Attributen zugeordnet sind, finden Sie unter [Schema Attribute nach Klasse in lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span><span class="sxs-lookup"><span data-stu-id="3b159-107">For the classes associated with attributes, see [Schema attributes by class in Lync Server 2013](lync-server-2013-schema-attributes-by-class.md).</span></span> <span data-ttu-id="3b159-108">Eine Liste der Klassen und Attribute, die in lync Server 2013 neu sind, finden Sie unter [Schema Änderungen in lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="3b159-108">For a list of classes and attributes that are new in Lync Server 2013, see [Schema changes in Lync Server 2013](lync-server-2013-schema-changes-in-lync-server-2013.md).</span></span>

<span data-ttu-id="3b159-109">Attribute, die verknüpfte Paare sind, werden als Weiterleitungs-oder zurück-Links angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b159-109">Attributes that are linked pairs are specified as forward links or back links.</span></span> <span data-ttu-id="3b159-110">Ein Attribut, das auf ein anderes Objekt verweist, ist ein Weiterleitungslink; das Attribut des anderen Objekts, das auf das erste Objekt zurückverweist, ist ein Link zurück.</span><span class="sxs-lookup"><span data-stu-id="3b159-110">An attribute that refers to another object is a forward link; the attribute of the other object that refers back to the first object is a back link.</span></span> <span data-ttu-id="3b159-111">Forward-Links sind aktualisierbare, während zurück-Links schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-111">Forward links are updatable, while back links are read-only.</span></span>

<span data-ttu-id="3b159-112">Einige Attribute weisen einen Bitmaskenwert auf.</span><span class="sxs-lookup"><span data-stu-id="3b159-112">Some attributes have a bit-mask value.</span></span> <span data-ttu-id="3b159-113">Bei diesen Attributen wird jede Einstellung durch ein Bit dargestellt, und der angezeigte Dezimalwert stellt die Bit-Position dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-113">For these attributes, each setting is represented by a bit, and the displayed decimal value represents the bit position.</span></span> <span data-ttu-id="3b159-114">Bit-Positionen beginnen mit Bit 0.</span><span class="sxs-lookup"><span data-stu-id="3b159-114">Bit positions start with bit 0.</span></span> <span data-ttu-id="3b159-115">Beispiel: 1 (Binary) ist Bit 0-Satz und 10000 (binär) ist Bit 4 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="3b159-115">For example, 1 (binary) is bit 0 set and 10000 (binary) is bit 4 set.</span></span> <span data-ttu-id="3b159-116">Jedes Bit stellt eine Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-116">Each bit represents a property.</span></span> <span data-ttu-id="3b159-117">Im folgenden finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="3b159-117">The following are some examples:</span></span>

  - <span data-ttu-id="3b159-118">10000 (Binary) hat einen Dezimalwert von 16 (das heißt, Bit 4 ist festzulegen).</span><span class="sxs-lookup"><span data-stu-id="3b159-118">10000 (binary) has a decimal value of 16 (that is, bit 4 is set).</span></span>

  - <span data-ttu-id="3b159-119">100 Millionen (Binary) hat einen Dezimalwert von 256 (das heißt, Bit 8 ist festzulegen).</span><span class="sxs-lookup"><span data-stu-id="3b159-119">100000000 (binary) has a decimal value of 256 (that is, bit 8 is set).</span></span>

  - <span data-ttu-id="3b159-120">1100 (Binary) hat den Dezimalwert 12 (das heißt, Bits 2 und 3 werden festgesetzt; die von beiden Bits dargestellten Eigenschaften sind aktiviert).</span><span class="sxs-lookup"><span data-stu-id="3b159-120">1100 (binary) has a decimal value of 12 (that is, bits 2 and 3 are set; properties represented by both bits are enabled).</span></span>

  - <span data-ttu-id="3b159-121">1111000001 (Binary) hat einen Dezimalwert von 961 (das heißt, Bits 0, 6, 7, 8 und 9 werden festgesetzt; Eigenschaften für jedes dieser Bits sind aktiviert).</span><span class="sxs-lookup"><span data-stu-id="3b159-121">1111000001 (binary) has a decimal value of 961 (that is, bits 0, 6, 7, 8, and 9 are set; properties for each of these bits are enabled).</span></span>

<div id="sectionSection0" class="section">

### <a name="schema-attributes-for-lync-server-2013"></a><span data-ttu-id="3b159-122">Schema Attribute für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b159-122">Schema Attributes for Lync Server 2013</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b159-123">Attribut</span><span class="sxs-lookup"><span data-stu-id="3b159-123">Attribute</span></span></th>
<th><span data-ttu-id="3b159-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b159-124">Description</span></span></th>
<th><span data-ttu-id="3b159-125">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3b159-125">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b159-126">DNSHostName</span><span class="sxs-lookup"><span data-stu-id="3b159-126">dnsHostName</span></span></p></td>
<td><p><span data-ttu-id="3b159-127">Ein vorhandenes Attribut in den Active Directory-Domänendiensten, das jetzt den <strong>Attribut msRTCSIP-</strong> und <strong>Attribut msRTCSIP-MonitoringServer</strong> -Klassen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-127">An existing attribute in Active Directory Domain Services that is now associated with the <strong>msRTCSIP-Pool</strong> and <strong>msRTCSIP-MonitoringServer</strong> classes.</span></span> <span data-ttu-id="3b159-128">Dieses Attribut gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Pools oder Überwachungsservers an.</span><span class="sxs-lookup"><span data-stu-id="3b159-128">This attribute specifies the fully qualified domain name (FQDN) of a pool or Monitoring Server.</span></span></p>
<p><span data-ttu-id="3b159-129">Ein gültiger Wert für jedes Segment ist 63 Zeichen; ein gültiger Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-129">A valid value for each segment is 63 characters; a valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-130">Neu in Microsoft Office Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-130">New in Microsoft Office Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-131">MSDS-SourceObjectDN</span><span class="sxs-lookup"><span data-stu-id="3b159-131">msDS-SourceObjectDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-132">Dieses Attribut enthält die Zeichenfolgendarstellung des Distinguished Name (DN) des Objekts in einer anderen Gesamtstruktur, die diesem Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="3b159-132">This attribute contains the string representation of the distinguished name (DN) of the object in another forest that corresponds to this object.</span></span> <span data-ttu-id="3b159-133">Dieses Attribut wird für die Erweiterung der Verteilergruppe und für die automatische Anwesenheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b159-133">This attribute is used for distribution group expansion and auto attendance.</span></span> <span data-ttu-id="3b159-134">Dieses Attribut ist im standardmäßigen Active Directory-Schema für Windows Server 2003 R2 definiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-134">This attribute is defined in the default Active Directory schema for Windows Server 2003 R2.</span></span></p>
<p><span data-ttu-id="3b159-135">Um zu vermeiden, dass ein Upgrade von AD DS auf Windows Server 2003 R2 erforderlich ist, wird das Windows Server 2003-Schema durch die Active Directory-Schemavorbereitung mit dieser Attributdefinition erweitert.</span><span class="sxs-lookup"><span data-stu-id="3b159-135">To avoid requiring an upgrade of AD DS to Windows Server 2003 R2, Active Directory schema preparation extends the Windows Server 2003 schema with this attribute definition.</span></span></p></td>
<td><p><span data-ttu-id="3b159-136">Neu in Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-136">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-137">msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="3b159-137">msExchUCVoiceMailSettings</span></span></p></td>
<td><p><span data-ttu-id="3b159-138">Dieses mehrwertige Attribut enthält Einstellungen für Voicemail.</span><span class="sxs-lookup"><span data-stu-id="3b159-138">This multi-valued attribute holds voice mail settings.</span></span> <span data-ttu-id="3b159-139">Dieses Attribut wird für Exchange Unified Messaging (um) freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3b159-139">This attribute is shared with Exchange Unified Messaging (UM).</span></span></p></td>
<td><p><span data-ttu-id="3b159-140">Neu in Microsoft lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-140">New in Microsoft Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-141">msExchUserHoldPolicies</span><span class="sxs-lookup"><span data-stu-id="3b159-141">msExchUserHoldPolicies</span></span></p></td>
<td><p><span data-ttu-id="3b159-142">Dieses mehrwertige Attribut enthält Bezeichner für für den Benutzer geltende Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="3b159-142">This multi-value attribute holds identifiers for hold policies that apply to the user.</span></span> <span data-ttu-id="3b159-143">Aufbewahrungsrichtlinien behalten Postfachelemente für den Benutzer für die Dauer des haltebereichs bei.</span><span class="sxs-lookup"><span data-stu-id="3b159-143">Hold policies preserve mailbox items for the user for the duration of the hold.</span></span> <span data-ttu-id="3b159-144">Dieses Attribut wird für Exchange 2013 freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3b159-144">This attribute is shared with Exchange 2013.</span></span></p></td>
<td><p><span data-ttu-id="3b159-145">Neu in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3b159-145">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-146">Attribut msRTCSIP-AcpInfo</span><span class="sxs-lookup"><span data-stu-id="3b159-146">msRTCSIP-AcpInfo</span></span></p></td>
<td><p><span data-ttu-id="3b159-147">Dieses Attribut speichert Informationen zu Audiokonferenz-Anbietern für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b159-147">This attribute stores audio conferencing provider information for a user.</span></span></p></td>
<td><p><span data-ttu-id="3b159-148">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-148">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-149">Attribut msRTCSIP-ApplicationDestination</span><span class="sxs-lookup"><span data-stu-id="3b159-149">msRTCSIP-ApplicationDestination</span></span></p></td>
<td><p><span data-ttu-id="3b159-150">Dieses Attribut verweist auf den vertrauenswürdigen Diensteintrag für den Anwendungs Kontakt.</span><span class="sxs-lookup"><span data-stu-id="3b159-150">This attribute points to the trusted service entry for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="3b159-151">Neu in Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-151">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-152">Attribut msRTCSIP-applicationlist</span><span class="sxs-lookup"><span data-stu-id="3b159-152">msRTCSIP-ApplicationList</span></span></p></td>
<td><p><span data-ttu-id="3b159-153">Dieses Attribut enthält eine Liste der gehosteten Anwendungen auf dem Anwendungsserver.</span><span class="sxs-lookup"><span data-stu-id="3b159-153">This attribute contains a list of hosted applications on the application server.</span></span></p></td>
<td><p><span data-ttu-id="3b159-154">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-154">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-155">Attribut msRTCSIP-ApplicationOptions</span><span class="sxs-lookup"><span data-stu-id="3b159-155">msRTCSIP-ApplicationOptions</span></span></p></td>
<td><p><span data-ttu-id="3b159-156">Dieses Attribut gibt die Optionen für den Anwendungs Kontakt an.</span><span class="sxs-lookup"><span data-stu-id="3b159-156">This attribute specifies the options for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="3b159-157">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-157">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-158">Attribut msRTCSIP-ApplicationPrimaryLanguage</span><span class="sxs-lookup"><span data-stu-id="3b159-158">msRTCSIP-ApplicationPrimaryLanguage</span></span></p></td>
<td><p><span data-ttu-id="3b159-159">Dieses Attribut enthält die primäre Sprache für den Anwendungs Kontakt.</span><span class="sxs-lookup"><span data-stu-id="3b159-159">This attribute contains the primary language for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="3b159-160">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-160">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-161">Attribut msRTCSIP-ApplicationSecondaryLanguages</span><span class="sxs-lookup"><span data-stu-id="3b159-161">msRTCSIP-ApplicationSecondaryLanguages</span></span></p></td>
<td><p><span data-ttu-id="3b159-162">Dieses Attribut mit mehreren Werten enthält die sekundären Sprachen für den Anwendungs Kontakt.</span><span class="sxs-lookup"><span data-stu-id="3b159-162">This multiple value attribute contains the secondary languages for the application contact.</span></span></p></td>
<td><p><span data-ttu-id="3b159-163">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-163">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-164">Attribut msRTCSIP-ApplicationServerBL</span><span class="sxs-lookup"><span data-stu-id="3b159-164">msRTCSIP-ApplicationServerBL</span></span></p></td>
<td><p><span data-ttu-id="3b159-165">Dieses Attribut enthält eine Liste der Anwendungsserver, die zu diesem Pool gehören.</span><span class="sxs-lookup"><span data-stu-id="3b159-165">This attribute contains a list of application servers that belong to this pool.</span></span> <span data-ttu-id="3b159-166">Der entsprechende Forward-Link zu diesem zurück Link-Attribut lautet <strong>Attribut msRTCSIP-ApplicationServerPoolLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-166">The corresponding forward link to this back link attribute is <strong>msRTCSIP-ApplicationServerPoolLink</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-167">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-167">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-168">Attribut msRTCSIP-ApplicationServerPoolLink</span><span class="sxs-lookup"><span data-stu-id="3b159-168">msRTCSIP-ApplicationServerPoolLink</span></span></p></td>
<td><p><span data-ttu-id="3b159-169">Dieses Attribut verweist auf den Pool, zu dem dieser Anwendungsserver gehört.</span><span class="sxs-lookup"><span data-stu-id="3b159-169">This attribute points to the pool to which this application server belongs.</span></span> <span data-ttu-id="3b159-170">Dies ist der Link weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="3b159-170">This is the forward link.</span></span> <span data-ttu-id="3b159-171">Der entsprechende rückwärts Link lautet <strong>Attribut msRTCSIP-ApplicationServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-171">The corresponding backward link is <strong>msRTCSIP-ApplicationServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-172">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-172">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-173">Attribut msRTCSIP-ArchiveDefault (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-173">msRTCSIP-ArchiveDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-174">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-174">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-175">Veraltet in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-175">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-176">Attribut msRTCSIP-ArchiveDefaultFlags (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-176">msRTCSIP-ArchiveDefaultFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-177">Dieses Attribut gibt den globalen Standardwert innerhalb der Gesamtstrukturgrenze für die Archivierung der gesamten Benutzerkommunikation an.</span><span class="sxs-lookup"><span data-stu-id="3b159-177">This attribute specifies the global default within the forest boundary for archiving all user communications.</span></span> <span data-ttu-id="3b159-178">Dies wird vom Archivierungs-Agent-Layer erzwungen.</span><span class="sxs-lookup"><span data-stu-id="3b159-178">This is enforced by the archiving agent layer.</span></span> <span data-ttu-id="3b159-179">Der Wertebereich für dieses Attribut lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-179">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-180"><strong>True</strong>: alle Benutzer archivieren</span><span class="sxs-lookup"><span data-stu-id="3b159-180"><strong>TRUE</strong>: Archive all users</span></span></p></li>
<li><p><span data-ttu-id="3b159-181"><strong>Falsch</strong>: nicht alle Benutzer archivieren</span><span class="sxs-lookup"><span data-stu-id="3b159-181"><strong>FALSE</strong>: Do not archive all users</span></span></p></li>
</ul>
<p><span data-ttu-id="3b159-182">Dieses Attribut steuert Global innerhalb der Gesamtstruktur-Grenze, wie die Benutzerkommunikation in einem internen Netzwerk archiviert wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-182">This attribute globally controls, within the forest boundary, how user communications within an internal network are archived.</span></span></p>
<p><span data-ttu-id="3b159-183"><strong>Live Communications Server 2005-Verhalten (jetzt eingestellt)</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-183"><strong>Live Communications Server 2005 behavior (now retired)</strong></span></span></p>
<p><span data-ttu-id="3b159-184">Der Wertebereich für dieses Attribut lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-184">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-185">0: Archivieren des Nachrichtentexts [Bit 0]</span><span class="sxs-lookup"><span data-stu-id="3b159-185">0: Archive the message body [bit 0]</span></span></p></li>
<li><p><span data-ttu-id="3b159-186">1: den Nachrichtentext nicht archivieren [Bit 0]</span><span class="sxs-lookup"><span data-stu-id="3b159-186">1: Do not archive the message body [bit 0]</span></span></p></li>
</ul>
<p><span data-ttu-id="3b159-187"><strong>Office Communications Server 2007-Verhalten</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-187"><strong>Office Communications Server 2007 behavior</strong></span></span></p>
<p><span data-ttu-id="3b159-188">Der Wertebereich für dieses Attribut lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-188">The range of values for this attribute is as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-189">0: ArchiveFederationDefaultWithoutBody (eingestellt)</span><span class="sxs-lookup"><span data-stu-id="3b159-189">0: ArchiveFederationDefaultWithoutBody (retired)</span></span></p></li>
<li><p><span data-ttu-id="3b159-190">1-2: ArchiveInternalCommunications</span><span class="sxs-lookup"><span data-stu-id="3b159-190">1-2: ArchiveInternalCommunications</span></span></p></li>
<li><p><span data-ttu-id="3b159-191">3-4: ArchiveFederatedCommunications</span><span class="sxs-lookup"><span data-stu-id="3b159-191">3-4: ArchiveFederatedCommunications</span></span></p></li>
<li><p><span data-ttu-id="3b159-192">5: RecordPresenceRegistrations</span><span class="sxs-lookup"><span data-stu-id="3b159-192">5: RecordPresenceRegistrations</span></span></p></li>
<li><p><span data-ttu-id="3b159-193">6: RecordIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-193">6: RecordIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-194">7: RecordGroupIMCallDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-194">7: RecordGroupIMCallDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-195">8: RecordFileTransferInstances</span><span class="sxs-lookup"><span data-stu-id="3b159-195">8: RecordFileTransferInstances</span></span></p></li>
<li><p><span data-ttu-id="3b159-196">9: RecordAudioCallDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-196">9: RecordAudioCallDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-197">10: RecordVideoCallDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-197">10: RecordVideoCallDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-198">11: RecordRemoteAssistanceCallDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-198">11: RecordRemoteAssistanceCallDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-199">12: RecordApplicationSharingDetails</span><span class="sxs-lookup"><span data-stu-id="3b159-199">12: RecordApplicationSharingDetails</span></span></p></li>
<li><p><span data-ttu-id="3b159-200">13: RecordMeetingInstantiations</span><span class="sxs-lookup"><span data-stu-id="3b159-200">13: RecordMeetingInstantiations</span></span></p></li>
<li><p><span data-ttu-id="3b159-201">14: RecordMeetingJoins</span><span class="sxs-lookup"><span data-stu-id="3b159-201">14: RecordMeetingJoins</span></span></p></li>
<li><p><span data-ttu-id="3b159-202">15: RecordDataJoins</span><span class="sxs-lookup"><span data-stu-id="3b159-202">15: RecordDataJoins</span></span></p></li>
<li><p><span data-ttu-id="3b159-203">16: RecordAVJoins</span><span class="sxs-lookup"><span data-stu-id="3b159-203">16: RecordAVJoins</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-204">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-204">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-205">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-205">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-206">Attribut msRTCSIP-ArchiveFederationDefault (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-206">msRTCSIP-ArchiveFederationDefault (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-207">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-207">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-208">Veraltet in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-208">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-209">Attribut msRTCSIP-ArchiveFederationDefaultFlags (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-209">msRTCSIP-ArchiveFederationDefaultFlags (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-210">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-210">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-211">Veraltet in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-211">Obsolete in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-212">Attribut msRTCSIP-ArchivingEnabled</span><span class="sxs-lookup"><span data-stu-id="3b159-212">msRTCSIP-ArchivingEnabled</span></span></p></td>
<td><p><span data-ttu-id="3b159-213">Dieses Attribut ist eine ganze Zahl, die als Bitfeld verwendet wird, um zu steuern, ob die Kommunikation eines einzelnen Benutzers archiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b159-213">This attribute is an integer used as a bit field to control whether a single user’s communications are to be archived.</span></span> <span data-ttu-id="3b159-214">Dieses Steuerelement wird vom Archivierungs-Agent-Layer erzwungen.</span><span class="sxs-lookup"><span data-stu-id="3b159-214">This control is enforced by the archiving agent layer.</span></span> <span data-ttu-id="3b159-215">Sie ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-215">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-216">Der Bereich dieses Attributs ist für einen einzelnen Benutzer oder Kontakt spezifisch.</span><span class="sxs-lookup"><span data-stu-id="3b159-216">The scope of this attribute is specific to a single user or contact.</span></span> <span data-ttu-id="3b159-217">Die gültigen Werte (und zugeordnete Bit-Positionen) in lync Server lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-217">The valid values (and associated bit positions) in Lync Server are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-218">0: nicht archivieren (kein Bit-Satz)</span><span class="sxs-lookup"><span data-stu-id="3b159-218">0: Do not archive (no bit set)</span></span></p></li>
<li><p><span data-ttu-id="3b159-219">1: eingestellt (Bit-Position 0)</span><span class="sxs-lookup"><span data-stu-id="3b159-219">1: Retired (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="3b159-220">2: eingestellt (Bit-Position 1)</span><span class="sxs-lookup"><span data-stu-id="3b159-220">2: Retired (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="3b159-221">4: Archivieren interner Kommunikation (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-221">4: Archive internal communications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-222">8: Archivieren der Föderations Kommunikation (Bit-Position 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-222">8: Archive federated communications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="3b159-223">Zuvor gültige Werte in Live Communications Server 2005 lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-223">Previously valid values in Live Communications Server 2005 are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-224">0: Verwenden Sie den Standardwert, der in dieser Rangfolge von <strong>Attribut msRTCSIP-ArchiveDefault</strong> und <strong>Attribut msRTCSIP-ArchiveFederation</strong> definiert ist:</span><span class="sxs-lookup"><span data-stu-id="3b159-224">0:Use the default value defined by <strong>msRTCSIP-ArchiveDefault</strong> and <strong>msRTCSIP-ArchiveFederation</strong> in this order of precedence:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-225">1: Archivieren</span><span class="sxs-lookup"><span data-stu-id="3b159-225">1: Archive</span></span></p></li>
<li><p><span data-ttu-id="3b159-226">2: nicht archivieren</span><span class="sxs-lookup"><span data-stu-id="3b159-226">2: Do not archive</span></span></p></li>
<li><p><span data-ttu-id="3b159-227">3: Archivieren ohne Nachrichtentext</span><span class="sxs-lookup"><span data-stu-id="3b159-227">3: Archive without the message body</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="3b159-228">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-228">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-229">Attribut msRTCSIP-ArchivingServerData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-229">msRTCSIP-ArchivingServerData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-230">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-230">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-231">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-231">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-232">Attribut msRTCSIP-ArchivingServerVersion (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-232">msRTCSIP-ArchivingServerVersion (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-233">Dieses Attribut definiert die Version des Archivierungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="3b159-233">This attribute defines the version of the Archiving service.</span></span> <span data-ttu-id="3b159-234">Bei diesem Attribut handelt es sich um einen monoton zunehmenden ganzzahligen Typ, der mit jeder offiziellen Produktversion inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-234">This attribute is a monotonously increasing integer type that increments with each official product release.</span></span> <span data-ttu-id="3b159-235">Die möglichen gültigen Werte lauten:</span><span class="sxs-lookup"><span data-stu-id="3b159-235">The possible valid values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-236">Undefined: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b159-236">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="3b159-237">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="3b159-237">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="3b159-238">Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-238">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="3b159-239">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-239">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="3b159-240">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3b159-240">4: Office Communications Server 2007 R2</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-241">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-241">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-242">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-243">Attribut msRTCSIP-BackEndServer</span><span class="sxs-lookup"><span data-stu-id="3b159-243">msRTCSIP-BackEndServer</span></span></p></td>
<td><p><span data-ttu-id="3b159-244">Dieses Attribut gibt den FQDN des Back-End-Servers des Pools an.</span><span class="sxs-lookup"><span data-stu-id="3b159-244">This attribute specifies the FQDN of the Back End Server of the pool.</span></span> <span data-ttu-id="3b159-245">Da es nur einen einzigen Back-End-Server pro Pool geben kann, handelt es sich hierbei um ein Single-Value-Attribut.</span><span class="sxs-lookup"><span data-stu-id="3b159-245">Because there can only be a single Back End Server per pool, this is a single-valued attribute.</span></span></p>
<p><span data-ttu-id="3b159-246">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-246">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-247">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-247">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-248">Attribut msRTCSIP-ConferenceDirectoryHomePool</span><span class="sxs-lookup"><span data-stu-id="3b159-248">msRTCSIP-ConferenceDirectoryHomePool</span></span></p></td>
<td><p><span data-ttu-id="3b159-249">Dieses Attribut enthält den Bezeichner des Pools, der das Konferenzverzeichnis hostet.</span><span class="sxs-lookup"><span data-stu-id="3b159-249">This attribute contains the identifier of the pool that hosts the conference directory.</span></span></p></td>
<td><p><span data-ttu-id="3b159-250">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-250">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-251">Attribut msRTCSIP-ConferenceDirectoryId</span><span class="sxs-lookup"><span data-stu-id="3b159-251">msRTCSIP-ConferenceDirectoryId</span></span></p></td>
<td><p><span data-ttu-id="3b159-252">Dieses Attribut enthält den Bezeichner eines Konferenz Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="3b159-252">This attribute contains the identifier of a conference directory.</span></span></p></td>
<td><p><span data-ttu-id="3b159-253">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-253">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-254">Attribut msRTCSIP-ConferenceDirectoryTargetPool</span><span class="sxs-lookup"><span data-stu-id="3b159-254">msRTCSIP-ConferenceDirectoryTargetPool</span></span></p></td>
<td><p><span data-ttu-id="3b159-255">Dieses Attribut enthält den Bezeichner des Pools, in den das Konferenzverzeichnis verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-255">This attribute contains the identifier of the pool to which the conference directory is being moved.</span></span></p></td>
<td><p><span data-ttu-id="3b159-256">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-256">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-257">Attribut msRTCSIP-Standard</span><span class="sxs-lookup"><span data-stu-id="3b159-257">msRTCSIP-Default</span></span></p></td>
<td><p><span data-ttu-id="3b159-258">Dieses boolesche Attribut definiert, ob es sich bei der Verwendung des Telefons um eine Standardverwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="3b159-258">This Boolean attribute defines whether the phone usage is a default usage.</span></span> <span data-ttu-id="3b159-259">Wenn dieses Attribut auf " <strong>true</strong>" festgelegt ist, handelt es sich bei der Verwendung des Telefons um eine Standardverwendung, die vom Administrator nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-259">If this attribute is set to <strong>TRUE</strong>, the phone usage is a default usage and cannot be deleted by the administrator.</span></span> <span data-ttu-id="3b159-260">Wenn dieses Attribut auf " <strong>false</strong>" festgelegt ist, kann die Verwendung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-260">If this attribute is set to <strong>FALSE</strong>, the usage can be deleted.</span></span></p></td>
<td><p><span data-ttu-id="3b159-261">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-261">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-262">Attribut msRTCSIP-DefaultCWAExternalURL</span><span class="sxs-lookup"><span data-stu-id="3b159-262">msRTCSIP-DefaultCWAExternalURL</span></span></p></td>
<td><p><span data-ttu-id="3b159-263">Dieses Attribut identifiziert die Communicator Web Access-URL für Benutzer, die sich außerhalb der Organisation befinden.</span><span class="sxs-lookup"><span data-stu-id="3b159-263">This attribute identifies the Communicator Web Access URL for users who are outside the organization.</span></span></p></td>
<td><p><span data-ttu-id="3b159-264">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-264">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-265">Attribut msRTCSIP-DefaultCWAInternalURL</span><span class="sxs-lookup"><span data-stu-id="3b159-265">msRTCSIP-DefaultCWAInternalURL</span></span></p></td>
<td><p><span data-ttu-id="3b159-266">Dieses Attribut identifiziert die Communicator Web Access-URL für Benutzer, die sich innerhalb der Organisation befinden.</span><span class="sxs-lookup"><span data-stu-id="3b159-266">This attribute identifies the Communicator Web Access URL for users who are inside the organization.</span></span></p></td>
<td><p><span data-ttu-id="3b159-267">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-267">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-268">Attribut msRTCSIP-DefaultLocationProfileLink (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-268">msRTCSIP-DefaultLocationProfileLink (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-269">Dieses Attribut mit einem Wert enthält den Distinguished Name (DN) eines ihm zugewiesenen Standortprofil-Klassenobjekts.</span><span class="sxs-lookup"><span data-stu-id="3b159-269">This single-valued attribute contains the distinguished name (DN) of a location profile class object assigned to it.</span></span></p>
<p><span data-ttu-id="3b159-270">Link weiterleiten: <strong>Link-ID 11036</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-270">Forward link: <strong>Link ID 11036</strong></span></span></p>
<p><span data-ttu-id="3b159-271">Der entsprechende rückwärts Link lautet <strong>Attribut msRTCSIP-ServerReferenceBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-271">The corresponding backward link is <strong>msRTCSIP-ServerReferenceBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-272">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-272">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-273">Attribut msRTCSIP-DefaultPolicy (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-273">msRTCSIP-DefaultPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-274">Dieses boolesche Attribut gibt an, ob es sich bei der Richtlinie um eine Standardrichtlinie handelt.</span><span class="sxs-lookup"><span data-stu-id="3b159-274">This Boolean attribute specifies whether the policy is a default policy.</span></span> <span data-ttu-id="3b159-275">Die Richtlinie ist eine Standardrichtlinie, wenn Sie auf " <strong>true</strong>" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-275">The policy is a default policy when set to <strong>TRUE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-276">Neu in Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-276">New in Office Communications Server 2007</span></span></p>
<p><span data-ttu-id="3b159-277">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-277">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-278">Attribut msRTCSIP-DefaultRouteToEdgeProxy (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-278">msRTCSIP-DefaultRouteToEdgeProxy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-279">Dieses Attribut gibt den FQDN des Edge-Servers an, auf dem der Access-Edgedienst ausgeführt wird, wenn er direkt aufgerufen werden kann, oder des Hardwarelastenausgleichs für einen Serverpool, auf dem Access Edge Service ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-279">This attribute specifies the FQDN of either the Edge Server running the Access Edge service, if it can be accessed directly, or of the hardware load balancer for a pool of servers running Access Edge service.</span></span> <span data-ttu-id="3b159-280">Wenn auf den Servern, auf denen Access Edge Service ausgeführt wird, nur über einen oder mehrere Directors zugegriffen werden kann, gibt dieses Attribut den FQDN und optional die Portnummer des Directors oder des Hardwarelastenausgleichs an, der einen Director-Pool bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-280">If the servers running Access Edge service can be accessed only through one or more Directors, this attribute specifies the FQDN and, optionally, the port number of the Director or of the hardware load balancer serving a Director pool.</span></span></p>
<p><span data-ttu-id="3b159-281">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-281">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-282">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-282">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-283">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-283">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-284">Attribut msRTCSIP-DefaultRouteToEdgeProxyPort (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-284">msRTCSIP-DefaultRouteToEdgeProxyPort (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-285">Dieses Attribut stellt die Portnummer dar, die für die Verbindung mit dem Server, auf dem Access Edge Service ausgeführt wird, verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b159-285">This attribute represents the port number that should be used to connect to the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="3b159-286">Der gültige Wert ist ein ganzzahliger Wert, der den zu verwendenden Port angibt.</span><span class="sxs-lookup"><span data-stu-id="3b159-286">The valid value is an integer value specifying the port to be used.</span></span> <span data-ttu-id="3b159-287">Der Standardwert ist 5061.</span><span class="sxs-lookup"><span data-stu-id="3b159-287">The default value is 5061.</span></span></p></td>
<td><p><span data-ttu-id="3b159-288">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-288">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-289">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-289">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-290">Attribut msRTCSIP-DefPresenceSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-290">msRTCSIP-DefPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-291">Dieses Attribut stellt den Standardtimeout Zeitraum für Anwesenheitsabonnements dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-291">This attribute represents the default presence subscription time-out period.</span></span></p></td>
<td><p><span data-ttu-id="3b159-292">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-292">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-293">Attribut msRTCSIP-DefRegistrationTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-293">msRTCSIP-DefRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-294">Dieses Attribut steht für das Standardtimeout Fenster für die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="3b159-294">This attribute represents the default registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-295">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-295">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-296">Attribut msRTCSIP-DefRoamingDataSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-296">msRTCSIP-DefRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-297">Dieses Attribut steht für das Standardtimeout Fenster des Roaming-Daten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3b159-297">This attribute represents the default roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-298">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-298">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-299">msRTCSIP-DeploymentLocator</span><span class="sxs-lookup"><span data-stu-id="3b159-299">msRTCSIP-DeploymentLocator</span></span></p></td>
<td><p><span data-ttu-id="3b159-300">Dieses Attribut wird in einer geteilten Domänentopologie verwendet und enthält einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN).</span><span class="sxs-lookup"><span data-stu-id="3b159-300">This attribute is used in a split domain topology and contains a fully qualified domain name (FQDN).</span></span></p></td>
<td><p><span data-ttu-id="3b159-301">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-301">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-302">Attribut msRTCSIP-Description (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-302">msRTCSIP-Description (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-303">Dieses Single-Value-UNICODE-Zeichenfolgenattribut enthält eine Beschreibung dieser Telefonroute oder Normalisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="3b159-303">This single-valued UNICODE string attribute contains a friendly description of this phone route or normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="3b159-304">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-304">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-305">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-305">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-306">Attribut msRTCSIP-DomainData</span><span class="sxs-lookup"><span data-stu-id="3b159-306">msRTCSIP-DomainData</span></span></p></td>
<td><p><span data-ttu-id="3b159-307">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-307">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-308">Attribut msRTCSIP-Domänenname</span><span class="sxs-lookup"><span data-stu-id="3b159-308">msRTCSIP-DomainName</span></span></p></td>
<td><p><span data-ttu-id="3b159-309">Dieses Attribut stellt eine für die Registrierungsstelle konfigurierte Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-309">This attribute represents a domain configured for the Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-310">Attribut msRTCSIP-EdgeProxyData</span><span class="sxs-lookup"><span data-stu-id="3b159-310">msRTCSIP-EdgeProxyData</span></span></p></td>
<td><p><span data-ttu-id="3b159-311">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-311">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-312">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-312">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-313">Attribut msRTCSIP-EdgeProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-313">msRTCSIP-EdgeProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-314">Dieses Attribut gibt den FQDN des Servers an, auf dem Access Edge-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-314">This attribute specifies the FQDN of the server running Access Edge service.</span></span></p>
<p><span data-ttu-id="3b159-315">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-315">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-316">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-316">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-317">Attribut msRTCSIP-EnableBestEffortNotify (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-317">msRTCSIP-EnableBestEffortNotify (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-318">Dieses Attribut steuert, ob ein Server als Antwort auf eine subscribe-Anforderung von einem Client eine Aufforderung zur Benachrichtigung über beste Leistung (BENOTIFY) anstelle einer Benachrichtigungsanforderung generiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-318">This attribute controls whether a server generates a Best Effort NOTIFY (BENOTIFY) request, instead of a NOTIFY request, in response to a SUBSCRIBE request from a client.</span></span> <span data-ttu-id="3b159-319">BENOTIFY ist eine leistungsverbessernde Erweiterung des Subscribe-Benachrichtigungs Handshakes, bei der der Server statt regelmäßiger Benachrichtigungsanforderungen BENOTIFY-Anforderungen generiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-319">BENOTIFY is a performance-enhancing extension to the subscribe notification handshake where the server generates BENOTIFY requests, instead of regular NOTIFY requests.</span></span> <span data-ttu-id="3b159-320">Der Leistungsvorteil besteht darin, dass eine BENOTIFY-Anforderung keine 200-OK-Antwort vom Client erfordert, wie dies bei der Benachrichtigungsanforderung der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-320">The performance benefit is that a BENOTIFY request does not require a 200 OK response from the client as the NOTIFY request does.</span></span></p>
<p><span data-ttu-id="3b159-321">Die gültigen Werte sind " <strong>wahr</strong> " oder " <strong>falsch</strong>".</span><span class="sxs-lookup"><span data-stu-id="3b159-321">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="3b159-322">Live Communications Server 2003 unterstützt keine BENOTIFY-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="3b159-322">Live Communications Server 2003 does not support BENOTIFY requests.</span></span> <span data-ttu-id="3b159-323">Um mit Serveranwendungen zu interagieren, die mit der Live Communications Server 2003-Server-API auf Live Communications Server 2005-und Drittanbieterservern geschrieben wurden, können BENOTIFY-Anforderungen deaktiviert werden, indem der Wert auf <STRONG>false</STRONG>festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-323">To interoperate with server applications written with the Live Communications Server 2003 server API running on Live Communications Server 2005 and third-party servers, BENOTIFY requests can be disabled by setting its value to <STRONG>FALSE</STRONG>.</span></span> <span data-ttu-id="3b159-324">BENOTIFY ist derzeit nicht Teil des IETF (Internet Engineering Task Force) SIP-Standardisierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="3b159-324">BENOTIFY is not currently part of the IETF (Internet Engineering Task Force) SIP standardization process.</span></span>


</div></td>
<td><p><span data-ttu-id="3b159-325">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-325">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-326">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-326">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-327">Attribut msRTCSIP-EnableFederation (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-327">msRTCSIP-EnableFederation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-328">Dieses Attribut ist ein globaler Schalter, den IT-Administratoren verwenden, um zu konfigurieren, ob Benutzer mit Benutzern aus anderen Organisationen kommunizieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="3b159-328">This attribute is a global switch that IT administrators use to configure whether users are allowed to communicate with users from other organizations.</span></span> <span data-ttu-id="3b159-329">Sie ermöglicht es einem Administrator, das <strong>FederationEnabled</strong> -Attribut eines einzelnen Benutzers zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3b159-329">It enables an administrator to overwrite an individual user’s <strong>FederationEnabled</strong> attribute.</span></span> <span data-ttu-id="3b159-330">Dieses Attribut kann hilfreich sein, um das interne Netzwerk vor Internet Angriffen zu schützen, die möglicherweise durch Würmer, Viren oder gezielte Angriffe auf das Unternehmen verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-330">This attribute can be useful to help protect the internal network from Internet attacks that may be caused by worms, viruses, or targeted attacks on the company.</span></span></p>
<p><span data-ttu-id="3b159-331">Die gültigen Werte (und zugeordnete Bit-Positionen) lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-331">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-332">1: aktiviert für öffentliche Chat Verbindungen (Bit-Position 0)</span><span class="sxs-lookup"><span data-stu-id="3b159-332">1: Enabled for public IM connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="3b159-333">2: reserviert (Bit-Position 1)</span><span class="sxs-lookup"><span data-stu-id="3b159-333">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="3b159-334">4: reserviert (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-334">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-335">8: reserviert (Bit-Position 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-335">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="3b159-336">16: Remote-Anrufsteuerung aktiviert [Telefonie] (Bit-Position 4)</span><span class="sxs-lookup"><span data-stu-id="3b159-336">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="3b159-337">64: AllowOrganizeMeetingWithAnonymousParticipants lautet (Benutzern gestatten, anonyme Benutzer zu Besprechungen einzuladen (Bit-Position 6)</span><span class="sxs-lookup"><span data-stu-id="3b159-337">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="3b159-338">128: UCEnabled (Aktivieren von Benutzern für Unified Communications) (Bit-Position 7)</span><span class="sxs-lookup"><span data-stu-id="3b159-338">128: UCEnabled (enable users for unified communications) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="3b159-339">256: EnabledForEnhancedPresence (Aktivieren des Benutzers für öffentliche Chat Verbindungen) (Bit-Position 8)</span><span class="sxs-lookup"><span data-stu-id="3b159-339">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="3b159-340">512: RemoteCallControlDualMode (Bit-Position 9)</span><span class="sxs-lookup"><span data-stu-id="3b159-340">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-341">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-341">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-342">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-342">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-343">Attribut msRTCSIP-EnterpriseServices</span><span class="sxs-lookup"><span data-stu-id="3b159-343">msRTCSIP-EnterpriseServices</span></span></p></td>
<td><p><span data-ttu-id="3b159-344">Dieses Attribut gibt an, ob die Enterprise-Dienste auf dem angegebenen Server geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-344">This attribute indicates whether the Enterprise Services are loaded on the given server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-345">Attribut msRTCSIP-ExtensionData</span><span class="sxs-lookup"><span data-stu-id="3b159-345">msRTCSIP-ExtensionData</span></span></p></td>
<td><p><span data-ttu-id="3b159-346">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-346">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-347">Attribut msRTCSIP-ExternalAccessCode</span><span class="sxs-lookup"><span data-stu-id="3b159-347">msRTCSIP-ExternalAccessCode</span></span></p></td>
<td><p><span data-ttu-id="3b159-348">Dieses Attribut enthält die Wähl Vorwahl für den externen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3b159-348">This attribute contains the dial code for external access.</span></span></p></td>
<td><p><span data-ttu-id="3b159-349">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-349">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-350">Attribut msRTCSIP-FederationEnabled</span><span class="sxs-lookup"><span data-stu-id="3b159-350">msRTCSIP-FederationEnabled</span></span></p></td>
<td><p><span data-ttu-id="3b159-351">Dieses Attribut steuert, ob ein einzelner Benutzer für den Verbund aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-351">This attribute controls whether a single user is enabled for federation.</span></span> <span data-ttu-id="3b159-352">Sie wird von der Enterprise Services-Schicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="3b159-352">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="3b159-353">Sie ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-353">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-354">Die gültigen Werte sind " <strong>wahr</strong> " oder " <strong>falsch</strong>".</span><span class="sxs-lookup"><span data-stu-id="3b159-354">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-355">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-355">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-356">Attribut msRTCSIP-FrontEndServers</span><span class="sxs-lookup"><span data-stu-id="3b159-356">msRTCSIP-FrontEndServers</span></span></p></td>
<td><p><span data-ttu-id="3b159-357">Dieses Attribut ist eine mehrwertige Liste der Domänennamen aller Enterprise Edition-Server, die einem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-357">This attribute is a multi-valued list of the domain names of all Enterprise Edition servers associated with a pool.</span></span></p>
<p><span data-ttu-id="3b159-358">Link zurück: <strong>Link-ID 11023</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-358">Back link: <strong>Link ID 11023</strong></span></span></p>
<p><span data-ttu-id="3b159-359">Der entsprechende Weiterleitungslink zu diesem zurück <strong>-Link lautet Attribut msRTCSIP-PoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-359">The corresponding forward link to this back link is <strong>msRTCSIP-PoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-360">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-360">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-361">Attribut msRTCSIP-Gateways (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-361">msRTCSIP-Gateways (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-362">Dieses Attribut für mehrwertige Zeichenfolgen enthält eine Liste der Gateways und Ports (pro Gateway).</span><span class="sxs-lookup"><span data-stu-id="3b159-362">This multi-valued string attribute contains a list of gateways and ports (per gateway).</span></span></p></td>
<td><p><span data-ttu-id="3b159-363">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-363">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-364">Attribut msRTCSIP-GlobalSettingsData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-364">msRTCSIP-GlobalSettingsData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-365">Dieses Attribut speichert Name: Wert-Paare.</span><span class="sxs-lookup"><span data-stu-id="3b159-365">This attribute stores name:value pairs.</span></span> <span data-ttu-id="3b159-366">Das bereits definierte Name: Wert-Paar ist für die Einstellung <strong>Polling für Anwesenheit zulassen</strong> .</span><span class="sxs-lookup"><span data-stu-id="3b159-366">The already-defined name:value pair is for the <strong>allow polling for presence</strong> setting.</span></span></p></td>
<td><p><span data-ttu-id="3b159-367">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-367">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-368">Attribut msRTCSIP-Gruppierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="3b159-368">msRTCSIP-GroupingID</span></span></p></td>
<td><p><span data-ttu-id="3b159-369">Dieses Attribut ist ein eindeutiger Bezeichner einer Gruppe, die zum Gruppieren von Adressbucheinträgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-369">This attribute is a unique identifier of a group that is used to group address book entries.</span></span></p></td>
<td><p><span data-ttu-id="3b159-370">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-370">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-371">Attribut msRTCSIP-Homeserver (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-371">msRTCSIP-HomeServer (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-372">Neu in Live Communications Server 2003 (nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="3b159-372">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="3b159-373">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-373">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-374">Attribut msRTCSIP-HomeServerString (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-374">msRTCSIP-HomeServerString (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-375">Neu in Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b159-375">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="3b159-376">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-376">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-377">Attribut msRTCSIP-Heimuser (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-377">msRTCSIP-HomeUsers (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-378">Neu in Live Communications Server 2003 (nicht verwendet).</span><span class="sxs-lookup"><span data-stu-id="3b159-378">New in Live Communications Server 2003 (not used).</span></span></p>
<p><span data-ttu-id="3b159-379">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-379">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-380">Attribut msRTCSIP-InternetAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="3b159-380">msRTCSIP-InternetAccessEnabled</span></span></p></td>
<td><p><span data-ttu-id="3b159-381">Dieses Attribut steuert, ob ein einzelner Benutzer für den Zugriff durch externe Benutzer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-381">This attribute controls whether a single user is enabled for outside user access.</span></span> <span data-ttu-id="3b159-382">Sie wird von der Enterprise Services-Schicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="3b159-382">It is enforced by the Enterprise Services layer.</span></span> <span data-ttu-id="3b159-383">Sie ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-383">It is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-384">Die gültigen Werte sind " <strong>wahr</strong> " oder " <strong>falsch</strong>".</span><span class="sxs-lookup"><span data-stu-id="3b159-384">The valid values are <strong>TRUE</strong> or <strong>FALSE</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-385">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-385">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-386">Attribut msRTCSIP-IsMaster (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-386">msRTCSIP-IsMaster (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-387">Neu in Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b159-387">New in Live Communications Server 2003</span></span></p>
<p><span data-ttu-id="3b159-388">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-388">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-389">Attribut msRTCSIP-Zeile</span><span class="sxs-lookup"><span data-stu-id="3b159-389">msRTCSIP-Line</span></span></p></td>
<td><p><span data-ttu-id="3b159-390">Dieses Attribut mit einem Wert enthält die Geräte-ID (entweder den SIP-URI oder den Tel-URI des Telefons, den der Benutzer steuert), der von lync für die Telefonie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-390">This single-valued attribute contains the device ID (either the SIP URI or the TEL URI of the phone the user controls) used by Lync for telephony.</span></span> <span data-ttu-id="3b159-391">Dieses Attribut ist für die Replikation des globalen Katalogs markiert und indiziert.</span><span class="sxs-lookup"><span data-stu-id="3b159-391">This attribute is marked for Global Catalog replication and is indexed.</span></span> <span data-ttu-id="3b159-392">Wenn ein Benutzer für Enterprise-VoIP aktiviert ist, speichert dieses Attribut die normalisierte E. 164-Version der Telefonnummer des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3b159-392">If a user is enabled for Enterprise Voice, this attribute stores the E.164 normalized version of the user’s phone number.</span></span></p></td>
<td><p><span data-ttu-id="3b159-393">Neu in Microsoft Office Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-393">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-394">Attribut msRTCSIP-LineServer</span><span class="sxs-lookup"><span data-stu-id="3b159-394">msRTCSIP-LineServer</span></span></p></td>
<td><p><span data-ttu-id="3b159-395">Dieses Attribut mit einem Wert enthält den SIP-URI des CSTA-SIP-Gatewayservers.</span><span class="sxs-lookup"><span data-stu-id="3b159-395">This single-valued attribute contains the SIP URI of the CSTA-SIP gateway server.</span></span> <span data-ttu-id="3b159-396">Dieses Attribut ist für die Replikation des globalen Katalogs markiert, aber nicht indiziert.</span><span class="sxs-lookup"><span data-stu-id="3b159-396">This attribute is marked for Global Catalog replication but is not indexed.</span></span></p></td>
<td><p><span data-ttu-id="3b159-397">Neu in Microsoft Office Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-397">New in Microsoft Office Live Communications Server 2005 with SP1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-398">Attribut msRTCSIP-LocalNormalizationData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-398">msRTCSIP-LocalNormalizationData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-399">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-399">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-400">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-400">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-401">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-401">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-402">Attribut msRTCSIP-LocalNormalizationLinks (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-402">msRTCSIP-LocalNormalizationLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-403">Dieses mehrwertige Attribut enthält eine Liste der lokalen normalisierungs Namen (Distinguished Names, DN), die diesem Standortprofil zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-403">This multi-valued attribute contains a list of local normalization distinguished names (DN) associated with this location profile.</span></span> <span data-ttu-id="3b159-404">Der Typ dieses Attributs ist eine DN-Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="3b159-404">The type of this attribute is a DN binary.</span></span> <span data-ttu-id="3b159-405">Es gibt eine 1: n-Beziehung zwischen Standortprofil und lokalen Normalisierungsregeln.</span><span class="sxs-lookup"><span data-stu-id="3b159-405">There is a one-to-many relationship between location profile and local normalization rules.</span></span> <span data-ttu-id="3b159-406">Die Reihenfolge der Liste der DNS für die lokale Normalisierung muss in der vom Administrator angegebenen Reihenfolge verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-406">The ordering of the list of local normalization DNs must be maintained in the order specified by the administrator.</span></span> <span data-ttu-id="3b159-407">Die Beibehaltung der Reihenfolge wird durch den binären Teil der DN-Binärdatei verwaltet, der den Reihenfolgeindex angibt.</span><span class="sxs-lookup"><span data-stu-id="3b159-407">The preservation of order is maintained by the binary portion of the DN binary, which specifies the order index.</span></span></p>
<p><span data-ttu-id="3b159-408">Link weiterleiten: <strong>Link-ID 11034</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-408">Forward link: <strong>Link ID 11034</strong></span></span></p>
<p><span data-ttu-id="3b159-409">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-LocationProfileBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-409">The corresponding back link to this forward link attribute is <strong>msRTCSIP-LocationProfileBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-410">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-410">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-411">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-411">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-412">Attribut msRTCSIP-LocalNormalizationOptions</span><span class="sxs-lookup"><span data-stu-id="3b159-412">msRTCSIP-LocalNormalizationOptions</span></span></p></td>
<td><p><span data-ttu-id="3b159-413">Dieses Attribut enthält eine Liste der Optionen für die Normalisierungsregel.</span><span class="sxs-lookup"><span data-stu-id="3b159-413">This attribute contains a list of options for the normalization rule.</span></span></p></td>
<td><p><span data-ttu-id="3b159-414">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-414">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-415">Attribut msRTCSIP-LocationName (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-415">msRTCSIP-LocationName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-416">Dieses Attribut mit einem Wert enthält einen Anzeigenamen für das Standortprofil, das angibt, an welcher Position dieses Profil steht.</span><span class="sxs-lookup"><span data-stu-id="3b159-416">This single-valued attribute contains a friendly name for the location profile that indicates which location this profile represents.</span></span> <span data-ttu-id="3b159-417">Da es mehrere Standortprofile geben kann, benötigt der Administrator eine Möglichkeit, zwischen verschiedenen Profilen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="3b159-417">Because there can be multiple location profiles, the administrator needs a way to distinguish between different profiles.</span></span></p></td>
<td><p><span data-ttu-id="3b159-418">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-418">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-419">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-419">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-420">Attribut msRTCSIP-locationProfileBL (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-420">msRTCSIP-locationProfileBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-421">Dieses mehrwertige Attribut enthält eine Liste mit definierten Namen für Standortprofile.</span><span class="sxs-lookup"><span data-stu-id="3b159-421">This multi-valued attribute contains a list of location profile distinguished names.</span></span> <span data-ttu-id="3b159-422">Dieses Attribut gibt den zurück-Link zu einem oder mehreren Standortprofilen an.</span><span class="sxs-lookup"><span data-stu-id="3b159-422">This attribute specifies the back link to one or more location profiles.</span></span></p>
<p><span data-ttu-id="3b159-423">Link zurück: <strong>Link-ID 11035</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-423">Back link: <strong>Link ID 11035</strong></span></span></p>
<p><span data-ttu-id="3b159-424">Dieses Attribut entspricht dem Forward-Link <strong>Attribut msRTCSIP-LocalNormalizationLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-424">This attribute corresponds to the forward link <strong>msRTCSIP-LocalNormalizationLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-425">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-425">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-426">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-426">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-427">Attribut msRTCSIP-LocationProfileData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-427">msRTCSIP-LocationProfileData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-428">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-428">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-429">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-429">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-430">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-430">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-431">Attribut msRTCSIP-LocationProfileOptions</span><span class="sxs-lookup"><span data-stu-id="3b159-431">msRTCSIP-LocationProfileOptions</span></span></p></td>
<td><p><span data-ttu-id="3b159-432">Dieses Attribut enthält die Optionen für das Standortprofil.</span><span class="sxs-lookup"><span data-stu-id="3b159-432">This attribute contains the options for the location profile.</span></span></p></td>
<td><p><span data-ttu-id="3b159-433">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-433">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-434">Attribut msRTCSIP-MappingContact</span><span class="sxs-lookup"><span data-stu-id="3b159-434">msRTCSIP-MappingContact</span></span></p></td>
<td><p><span data-ttu-id="3b159-435">Dieses Attribut mit mehreren Werten enthält eine Liste von Anwendungs Kontakten.</span><span class="sxs-lookup"><span data-stu-id="3b159-435">This multiple-value attribute holds a list of application contacts.</span></span></p></td>
<td><p><span data-ttu-id="3b159-436">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-436">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-437">Attribut msRTCSIP-MappingLocation</span><span class="sxs-lookup"><span data-stu-id="3b159-437">msRTCSIP-MappingLocation</span></span></p></td>
<td><p><span data-ttu-id="3b159-438">Dieses Attribut mit mehreren Werten enthält eine Liste von Standortprofilen.</span><span class="sxs-lookup"><span data-stu-id="3b159-438">This multiple-value attribute holds a list of location profiles.</span></span></p></td>
<td><p><span data-ttu-id="3b159-439">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-439">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-440">Attribut msRTCSIP-MaxNumOutstandingSearchPerServer (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-440">msRTCSIP-MaxNumOutstandingSearchPerServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-441">Dieses Attribut stellt die maximale Anzahl ausstehender Suchanforderungen pro Server dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-441">This attribute represents the maximum number of outstanding search requests per server.</span></span></p></td>
<td><p><span data-ttu-id="3b159-442">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-442">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-443">Attribut msRTCSIP-MaxNumSubscriptionsPerUser (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-443">msRTCSIP-MaxNumSubscriptionsPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-444">Das Attribut stellt die maximale Anzahl von Abonnements pro Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-444">The attribute represents the maximum number of subscriptions per user.</span></span></p></td>
<td><p><span data-ttu-id="3b159-445">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-445">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-446">Attribut msRTCSIP-MaxPresenceSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-446">msRTCSIP-MaxPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-447">Dieses Attribut stellt das maximale Timeout Fenster für Abonnements dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-447">This attribute represents the maximum subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-448">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-448">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-449">Attribut msRTCSIP-MaxRegistrationsTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-449">msRTCSIP-MaxRegistrationsTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-450">Dieses Attribut stellt das Timeout Fenster für maximale Registrierungen dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-450">This attribute represents the maximum registrations time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-451">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-451">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-452">Attribut msRTCSIP-MaxRoamingDataSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-452">msRTCSIP-MaxRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-453">Dieses Attribut steht für das maximale Timeout Fenster für Roaming-Daten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3b159-453">This attribute represents the maximum roaming data subscriptions time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-454">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-454">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-455">Attribut msRTCSIP-MCUData</span><span class="sxs-lookup"><span data-stu-id="3b159-455">msRTCSIP-MCUData</span></span></p></td>
<td><p><span data-ttu-id="3b159-456">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-456">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-457">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-457">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-458">Attribut msRTCSIP-MCUFactoryAddress</span><span class="sxs-lookup"><span data-stu-id="3b159-458">msRTCSIP-MCUFactoryAddress</span></span></p></td>
<td><p><span data-ttu-id="3b159-459">Bei diesem Attribut handelt es sich um ein Dienst Kontrollpunkt-Attribut unter der Computerklasse, das einen Link zurück zur Factory-Einheit (Multipoint Control Unit, MCU) angibt, zu der er gehört.</span><span class="sxs-lookup"><span data-stu-id="3b159-459">This attribute is a service control point attribute under the computer class that specifies a link back to the multipoint control unit (MCU) Factory to which it belongs.</span></span> <span data-ttu-id="3b159-460">Dieser Dienst Kontrollpunkt und das Attribut werden für jede Microsoft-MCU erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-460">This service control point and attribute is created for every Microsoft MCU.</span></span> <span data-ttu-id="3b159-461">Jede Microsoft-MCU muss den Back-End-Server des Pools finden, zu dem Sie gehört, um Einstellungen auf Poolebene abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b159-461">Each Microsoft MCU must find the Back End Server of the pool to which it belongs, in order to retrieve pool-level settings from it.</span></span></p>
<p><span data-ttu-id="3b159-462">Der Wert dieses Attributs ist der Distinguished Name (DN) der MCU-Factory.</span><span class="sxs-lookup"><span data-stu-id="3b159-462">The value of this attribute is the distinguished name (DN) of the MCU Factory.</span></span> <span data-ttu-id="3b159-463">Hierbei handelt es sich um ein Single-Value-Attribut, das für die Replikation des globalen Katalogs markiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-463">This is a single-valued attribute and marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-464">Link weiterleiten: <strong>Link-ID 11026</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-464">Forward link: <strong>Link ID 11026</strong></span></span></p>
<p><span data-ttu-id="3b159-465">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-MCUServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-465">The corresponding back link to this forward link attribute is <strong>msRTCSIP-MCUServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-466">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-466">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-467">Attribut msRTCSIP-MCUFactoryData</span><span class="sxs-lookup"><span data-stu-id="3b159-467">msRTCSIP-MCUFactoryData</span></span></p></td>
<td><p><span data-ttu-id="3b159-468">Hierbei handelt es sich um ein reserviertes Attribut mit mehreren Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="3b159-468">This is a multi-string reserved attribute.</span></span> <span data-ttu-id="3b159-469">In diesem Attribut gespeicherte Einstellungen werden als Name = Wert-Paare dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-469">Settings stored in this attribute are represented as name=value pairs.</span></span> <span data-ttu-id="3b159-470">Derzeit definierte Name = Wert-Paare:</span><span class="sxs-lookup"><span data-stu-id="3b159-470">Currently defined name=value pairs are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-471">FactoryURL = &lt; URL&gt;</span><span class="sxs-lookup"><span data-stu-id="3b159-471">FactoryURL = &lt;URL&gt;</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-472">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-472">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-473">Attribut msRTCSIP-MCUFactoryPath</span><span class="sxs-lookup"><span data-stu-id="3b159-473">msRTCSIP-MCUFactoryPath</span></span></p></td>
<td><p><span data-ttu-id="3b159-474">Hierbei handelt es sich um ein Single-Value-Attribut, das den Distinguished Name (DN) einer einzelnen MCU-Factory enthält, die einem Pool zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-474">This is a single-valued attribute that contains the distinguished name (DN) of a single MCU factory associated with a pool.</span></span></p>
<p><span data-ttu-id="3b159-475">Link weiterleiten: <strong>Link-ID 11024</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-475">Forward link: <strong>Link ID 11024</strong></span></span></p>
<p><span data-ttu-id="3b159-476">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-PoolAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-476">The corresponding back link to this forward link attribute is <strong>msRTCSIP-PoolAddresses</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-477">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-477">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-478">Attribut msRTCSIP-MCUFactoryProviderID</span><span class="sxs-lookup"><span data-stu-id="3b159-478">msRTCSIP-MCUFactoryProviderID</span></span></p></td>
<td><p><span data-ttu-id="3b159-479">Dieses Attribut ist eine Single-Wert-Zeichenfolge, die die GUID des MCU-Factory-Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="3b159-479">This attribute is a single-valued string that specifies the GUID of the MCU factory provider.</span></span> <span data-ttu-id="3b159-480">Basierend auf dem GUID-Wert bestimmt der MCU Factory-Prozess, ob dieser MCU-Typ gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b159-480">Based on the GUID value, the MCU factory process determines whether to service this MCU type.</span></span> <span data-ttu-id="3b159-481">Wenn es sich bei dem GUID-Wert um <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>handelt, wird der MCU-factoryprozess (standardmäßig in lync Server verfügbar) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3b159-481">If the GUID value is <strong>{F0810510-424F-46ef-84FE-6CC720DF1791}</strong>, then the MCU factory process (available by default in Lync Server) will process it.</span></span> <span data-ttu-id="3b159-482">Für einen beliebigen anderen GUID-Wert wird der MCU-factoryprozess nicht von dem MCU-Typ gewartet.</span><span class="sxs-lookup"><span data-stu-id="3b159-482">For any other GUID value, the MCU factory process will not service the MCU type.</span></span></p></td>
<td><p><span data-ttu-id="3b159-483">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-483">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-484">Attribut msRTCSIP-MCUServers</span><span class="sxs-lookup"><span data-stu-id="3b159-484">msRTCSIP-MCUServers</span></span></p></td>
<td><p><span data-ttu-id="3b159-485">Dieses Attribut ist eine mehrwertige Liste mit Distinguished Names (DN).</span><span class="sxs-lookup"><span data-stu-id="3b159-485">This attribute is a multi-valued list of distinguished names (DN).</span></span> <span data-ttu-id="3b159-486">Dieses Attribut enthält eine Liste aller MCU-Server desselben Typs und Lieferanten, die dieser MCU-Factory zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-486">This attribute contains a list of all MCU servers of the same type and vendor associated with this MCU factory.</span></span> <span data-ttu-id="3b159-487">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-487">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p>
<p><span data-ttu-id="3b159-488">Link zurück: Link-ID 11027</span><span class="sxs-lookup"><span data-stu-id="3b159-488">Back link: Link ID 11027</span></span></p>
<p><span data-ttu-id="3b159-489">Der entsprechende Weiterleitungslink zu diesem zurück <strong>-Link lautet Attribut msRTCSIP-MCUFactoryAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-489">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-490">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-490">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-491">Attribut msRTCSIP-MCUType</span><span class="sxs-lookup"><span data-stu-id="3b159-491">msRTCSIP-MCUType</span></span></p></td>
<td><p><span data-ttu-id="3b159-492">Dieses Attribut ist eine einwertige Zeichenfolge, die das Medium angibt, das die MCU verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-492">This attribute is a single-valued string that specifies the medium the MCU can handle.</span></span></p>
<p><span data-ttu-id="3b159-493">Unterstützte gültige Typen:</span><span class="sxs-lookup"><span data-stu-id="3b159-493">Supported valid types are:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-494">Besprechung</span><span class="sxs-lookup"><span data-stu-id="3b159-494">meeting</span></span></p></li>
<li><p><span data-ttu-id="3b159-495">Audio-Video</span><span class="sxs-lookup"><span data-stu-id="3b159-495">audio-video</span></span></p></li>
<li><p><span data-ttu-id="3b159-496">Chat</span><span class="sxs-lookup"><span data-stu-id="3b159-496">chat</span></span></p></li>
<li><p><span data-ttu-id="3b159-497">Telefon-conf</span><span class="sxs-lookup"><span data-stu-id="3b159-497">phone-conf</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-498">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-498">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-499">Attribut msRTCSIP-MCUVendor</span><span class="sxs-lookup"><span data-stu-id="3b159-499">msRTCSIP-MCUVendor</span></span></p></td>
<td><p><span data-ttu-id="3b159-500">Dieses Attribut ist eine Single-Wert-Zeichenfolge, die den Namen eines MCU-Anbieters angibt.</span><span class="sxs-lookup"><span data-stu-id="3b159-500">This attribute is a single-valued string that specifies an MCU vendor’s name.</span></span> <span data-ttu-id="3b159-501">Dieses Attribut wird von allen Microsoft-MCU als <strong>Microsoft Corporation</strong>angegeben.</span><span class="sxs-lookup"><span data-stu-id="3b159-501">All Microsoft MCUs will specify this attribute to be <strong>Microsoft Corporation</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-502">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-502">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-503">Attribut msRTCSIP-MeetingFlags (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-503">msRTCSIP-MeetingFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-504">Dieses Attribut definiert verschiedene Besprechungsoptionen, die für alle Benutzer oder Kontaktobjekte global aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-504">This attribute defines different meeting options that are enabled globally for all users or contact objects.</span></span> <span data-ttu-id="3b159-505">Dieses Attribut ist ein Bitmaskenwert vom Typ "ganze Zahl".</span><span class="sxs-lookup"><span data-stu-id="3b159-505">This attribute is a bit-mask value of integer type.</span></span></p>
<p><span data-ttu-id="3b159-506">Die gültigen Werte (und zugeordnete Bit-Positionen) lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-506">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-507">0: AllowOrganizeMeetingWithAnonymousParticipants lautet ist keine (Benutzer dürfen keine anonymen Benutzer zu Besprechungen einladen) (kein Bits-Satz)</span><span class="sxs-lookup"><span data-stu-id="3b159-507">0: AllowOrganizeMeetingWithAnonymousParticipants is None (do not allow users to invite anonymous users to meetings) (no bits set)</span></span></p></li>
<li><p><span data-ttu-id="3b159-508">4: AllowOrganizeMeetingWithAnonymousParticipants lautet ist jeder (allen Benutzern gestatten, anonyme Benutzer zu Besprechungen einzuladen) (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-508">4: AllowOrganizeMeetingWithAnonymousParticipants is Everyone (allow all users to invite anonymous users to meetings) (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-509">8: AllowOrganizeMeetingWithAnonymousParticipants lautet ist UsePerUserSetting (Benutzern gestatten, anonyme Benutzer zu Besprechungen basierend auf der Einstellung pro Benutzer einzuladen) (Bit-Position 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-509">8: AllowOrganizeMeetingWithAnonymousParticipants is UsePerUserSetting (allow users to invite anonymous users to meetings based on per user setting) (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="3b159-510">16: UserPerUserMeetingPolicy (die Besprechungsrichtlinie wird pro Benutzerdefiniert) (Bit-Position 4)</span><span class="sxs-lookup"><span data-stu-id="3b159-510">16: UserPerUserMeetingPolicy (meeting policy is defined per user) (bit position 4)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-511">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-511">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-512">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-512">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-513">Attribut msRTCSIP-MeetingPolicy (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-513">msRTCSIP-MeetingPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-514">Dieses Attribut gibt den Distinguished Name (DN) der Richtlinie an, die der Administrator für diesen Benutzer als Single-Wert-Attribut zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="3b159-514">This attribute specifies the distinguished name (DN) of the policy the administrator has assigned for this user as a single-valued attribute.</span></span></p></td>
<td><p><span data-ttu-id="3b159-515">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-515">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-516">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-516">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-517">Attribut msRTCSIP-MinPresenceSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-517">msRTCSIP-MinPresenceSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-518">Dieses Attribut steht für das minimale Timeout Fenster für Anwesenheitsabonnements.</span><span class="sxs-lookup"><span data-stu-id="3b159-518">This attribute represents the minimum presence subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-519">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-519">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-520">Attribut msRTCSIP-MinRegistrationTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-520">msRTCSIP-MinRegistrationTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-521">Dieses Attribut steht für das minimale Registrierungstimeout Fenster.</span><span class="sxs-lookup"><span data-stu-id="3b159-521">This attribute represents the minimum registration time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-522">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-522">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-523">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-523">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-524">Attribut msRTCSIP-MinRoamingDataSubscriptionTimeout (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-524">msRTCSIP-MinRoamingDataSubscriptionTimeout (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-525">Dieses Attribut stellt das minimale Timeout Fenster für Roaming-Daten Abonnements dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-525">This attribute represents the minimum roaming data subscription time-out window.</span></span></p></td>
<td><p><span data-ttu-id="3b159-526">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-526">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-527">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-527">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-528">Attribut msRTCSIP-MirrorBackEndServer</span><span class="sxs-lookup"><span data-stu-id="3b159-528">msRTCSIP-MirrorBackEndServer</span></span></p></td>
<td><p><span data-ttu-id="3b159-529">Dieses Attribut wird zum Speichern des vom Front-End-Pool verwendeten gespiegelten SQL Server-Back-Ends verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b159-529">This attribute is used to store the mirrored SQL Server backend used by the Front End pool.</span></span></p></td>
<td><p><span data-ttu-id="3b159-530">Neu in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3b159-530">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-531">Attribut msRTCSIP-MobilityFlags</span><span class="sxs-lookup"><span data-stu-id="3b159-531">msRTCSIP-MobilityFlags</span></span></p></td>
<td><p><span data-ttu-id="3b159-532">Dieses Attribut enthält Optionen und Flags, mit denen Mobilitätseinstellungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-532">This attribute contains options and flags that define mobility settings.</span></span></p></td>
<td><p><span data-ttu-id="3b159-533">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-533">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-534">Attribut msRTCSIP-MobilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3b159-534">msRTCSIP-MobilityPolicy</span></span></p></td>
<td><p><span data-ttu-id="3b159-535">Dieses Attribut enthält den DN für ein mobilitätsrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b159-535">This attribute contains the DN for a mobility policy object.</span></span></p></td>
<td><p><span data-ttu-id="3b159-536">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-536">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-537">Attribut msRTCSIP-NumDevicesPerUser (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-537">msRTCSIP-NumDevicesPerUser (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-538">Dieses Attribut stellt die zulässige Anzahl von Geräten dar, auf denen ein Benutzer für die SIP-Kommunikation registrieren und den Anwesenheitsstatus abonnieren kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-538">This attribute represents the allowed number of devices on which a user can register for SIP communications and subscribe to presence.</span></span></p></td>
<td><p><span data-ttu-id="3b159-539">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-539">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-540">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-540">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-541">Attribut msRTCSIP-OptionFlags</span><span class="sxs-lookup"><span data-stu-id="3b159-541">msRTCSIP-OptionFlags</span></span></p></td>
<td><p><span data-ttu-id="3b159-542">Dieses Attribut gibt die Optionen an, die für den Benutzer oder das Kontaktobjekt aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-542">This attribute specifies the options that are enabled for the user or contact object.</span></span> <span data-ttu-id="3b159-543">Dieses Attribut ist ein Bitmaskenwert vom Typ Integer.</span><span class="sxs-lookup"><span data-stu-id="3b159-543">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="3b159-544">Jede Option wird durch ein Bit dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-544">Each option is represented by a bit.</span></span> <span data-ttu-id="3b159-545">Dieses Attribut ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-545">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-546">Die gültigen Werte (und zugeordnete Bit-Positionen) lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-546">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-547">1: für öffentliche Instant Messaging (im)-Konnektivität (Bit-Position 0) aktiviert</span><span class="sxs-lookup"><span data-stu-id="3b159-547">1: Enabled for public instant messaging (IM) connectivity (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="3b159-548">2: reserviert (Bit-Position 1)</span><span class="sxs-lookup"><span data-stu-id="3b159-548">2: Reserved (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="3b159-549">4: reserviert (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-549">4: Reserved (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-550">8: reserviert (Bit-Position 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-550">8: Reserved (bit position 3)</span></span></p></li>
<li><p><span data-ttu-id="3b159-551">16: Remote-Anrufsteuerung aktiviert [Telefonie] (Bit-Position 4)</span><span class="sxs-lookup"><span data-stu-id="3b159-551">16: Remote call control Enabled [Telephony] (bit position 4)</span></span></p></li>
<li><p><span data-ttu-id="3b159-552">64: AllowOrganizeMeetingWithAnonymousParticipants lautet (Benutzern gestatten, anonyme Benutzer zu Besprechungen einzuladen (Bit-Position 6)</span><span class="sxs-lookup"><span data-stu-id="3b159-552">64: AllowOrganizeMeetingWithAnonymousParticipants (allow users to invite anonymous users to meetings (bit position 6)</span></span></p></li>
<li><p><span data-ttu-id="3b159-553">128: UCEnabled (Aktivieren von Benutzern für UC) (Bit-Position 7)</span><span class="sxs-lookup"><span data-stu-id="3b159-553">128: UCEnabled (enable users for UC) (bit position 7)</span></span></p></li>
<li><p><span data-ttu-id="3b159-554">256: EnabledForEnhancedPresence (Aktivieren des Benutzers für öffentliche Chat Verbindungen) (Bit-Position 8)</span><span class="sxs-lookup"><span data-stu-id="3b159-554">256: EnabledForEnhancedPresence (enable user for public IM connectivity) (bit position 8)</span></span></p></li>
<li><p><span data-ttu-id="3b159-555">512: RemoteCallControlDualMode (Bit-Position 9)</span><span class="sxs-lookup"><span data-stu-id="3b159-555">512: RemoteCallControlDualMode (bit position 9)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-556">Neu in Live Communications Server 2005 mit SP1.</span><span class="sxs-lookup"><span data-stu-id="3b159-556">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-557">msRTCSIP-OriginatorSID</span><span class="sxs-lookup"><span data-stu-id="3b159-557">msRTCSIP-OriginatorSID</span></span></p></td>
<td><p><span data-ttu-id="3b159-558">Dieses Attribut wird in Ressourcen-und zentralen Gesamtstruktur Topologien verwendet, um die einmalige Anmeldung zu aktivieren, wenn die Objekt-Nr des Benutzers aus dem Windows NT Server-Prinzipal Konto in dieses Attribut des entsprechenden Benutzers oder Kontaktobjekts in der Ressource oder der zentralen Gesamtstruktur kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-558">This attribute is used in resource and central forest topologies to enable single sign-on when a user’s ObjectSID from the Windows NT Server principal account is copied into this attribute of the corresponding user or contact object in the resource or central forest.</span></span> <span data-ttu-id="3b159-559">Communicator Web Access sucht nach einem Benutzer in AD DS mithilfe dieses Attributs oder der Objekt-Nr des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3b159-559">Communicator Web Access searches for a user in AD DS using this attribute or the user’s ObjectSID.</span></span> <span data-ttu-id="3b159-560">Dieses Attribut ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-560">This attribute is marked for global catalog replication.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-561">Attribut msRTCSIP-OwnerUrn</span><span class="sxs-lookup"><span data-stu-id="3b159-561">msRTCSIP-OwnerUrn</span></span></p></td>
<td><p><span data-ttu-id="3b159-562">Dieses Attribut ist der Uniform Resource Name (URN) des Besitzers für einen Anwendungs Kontakt.</span><span class="sxs-lookup"><span data-stu-id="3b159-562">This attribute is the Uniform Resource Name (URN) of the owner for an application contact.</span></span></p></td>
<td><p><span data-ttu-id="3b159-563">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-563">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-564">Attribut msRTCSIP-Muster (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-564">msRTCSIP-Pattern (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-565">Dieses Attribut mit einer Wert Zeichenfolge enthält ein Muster, das für die Übereinstimmung von Wähl Nummern im E. 164-Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-565">This single-valued string attribute contains a pattern used for matching dial numbers into E.164 format.</span></span> <span data-ttu-id="3b159-566">Wenn die Wählnummer mit diesem Muster übereinstimmt, wird die Übersetzung auf die gewählte Nummer angewendet.</span><span class="sxs-lookup"><span data-stu-id="3b159-566">If the dial number matches this pattern, the translation is applied to the dialed number.</span></span></p></td>
<td><p><span data-ttu-id="3b159-567">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-567">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-568">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-568">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-569">Attribut msRTCSIP-PhoneRouteBL (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-569">msRTCSIP-PhoneRouteBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-570">Dieses mehrwertige Attribut enthält eine Liste von Distinguished Names (DN) für die Telefonroute.</span><span class="sxs-lookup"><span data-stu-id="3b159-570">This multi-valued attribute contains a list of phone route distinguished names (DN).</span></span> <span data-ttu-id="3b159-571">Dieses Attribut gibt den zurück-Link zu einer oder mehreren Telefonrouten an.</span><span class="sxs-lookup"><span data-stu-id="3b159-571">This attribute specifies the back link to one or more phone routes.</span></span></p>
<p><span data-ttu-id="3b159-572">Link zurück: <strong>Link-ID 11033</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-572">Back link: <strong>Link ID 11033</strong></span></span></p>
<p><span data-ttu-id="3b159-573">Dieses Attribut entspricht dem Forward-Link <strong>Attribut msRTCSIP-RouteUsageLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-573">This attribute corresponds to the forward link <strong>msRTCSIP-RouteUsageLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-574">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-574">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-575">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-575">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-576">Attribut msRTCSIP-PhoneRouteData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-576">msRTCSIP-PhoneRouteData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-577">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-577">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-578">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-578">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-579">Attribut msRTCSIP-PhoneRouteName (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-579">msRTCSIP-PhoneRouteName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-580">Dieses Single-Value-UNICODE-Zeichenfolgenattribut gibt den Anzeigenamen der Telefonroute an, sodass vom Administrator einfach darauf verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-580">This single valued UNICODE string attribute specifies the friendly name of the phone route, so it can easily be referenced by the administrator.</span></span></p></td>
<td><p><span data-ttu-id="3b159-581">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-581">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-582">Attribut msRTCSIP-PhoneUsageData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-582">msRTCSIP-PhoneUsageData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-583">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-583">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-584">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-584">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-585">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-585">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-586">Attribut msRTCSIP-PolicyContent (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-586">msRTCSIP-PolicyContent (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-587">Dieses Attribut ist eine Unicode-Zeichenfolge mit einem Wert.</span><span class="sxs-lookup"><span data-stu-id="3b159-587">This attribute is a single-valued Unicode string.</span></span> <span data-ttu-id="3b159-588">Dieses Zeichenfolgenattribut enthält die Richtliniendefinition im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="3b159-588">This string attribute contains the policy definition in XML format.</span></span> <span data-ttu-id="3b159-589">Die XML-Schema Definition ist in verschiedenen Richtlinientypen üblich, nur die Einstellungen unterscheiden sich für jeden Richtlinientyp.</span><span class="sxs-lookup"><span data-stu-id="3b159-589">The XML schema definition is common across different policy types, only the settings are different for each policy type.</span></span></p>
<p><span data-ttu-id="3b159-590">Die XML-Schema Definition (XSD) ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3b159-590">The XML schema definition (XSD) is defined as follows:</span></span></p>
<pre><code>&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;xs:schema id=&quot;instance&quot; xmlns=&quot;&quot; xmlns:xs=&quot;http://www.w3.org/2001/XMLSchema&quot; xmlns:msdata=&quot;urn:schemas-microsoft-com:xml-msdata&quot;&gt;
  &lt;xs:element name=&quot;instance&quot; msdata:IsDataSet=&quot;true&quot;&gt;
    &lt;xs:complexType&gt;
      &lt;xs:choice maxOccurs=&quot;unbounded&quot;&gt;
        &lt;xs:element name=&quot;property&quot; nillable=&quot;true&quot;&gt;
          &lt;xs:complexType&gt;
            &lt;xs:simpleContent msdata:ColumnName=&quot;property_Text&quot; msdata:Ordinal=&quot;1&quot;&gt;
              &lt;xs:extension base=&quot;xs:string&quot;&gt;
                &lt;xs:attribute name=&quot;name&quot; type=&quot;xs:string&quot; /&gt;
              &lt;/xs:extension&gt;
            &lt;/xs:simpleContent&gt;
          &lt;/xs:complexType&gt;
        &lt;/xs:element&gt;
      &lt;/xs:choice&gt;
    &lt;/xs:complexType&gt;
  &lt;/xs:element&gt;
&lt;/xs:schema&gt;</code></pre></td>
<td><p><span data-ttu-id="3b159-591">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-591">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-592">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-592">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-593">Attribut msRTCSIP-Spalte PolicyData (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-593">msRTCSIP-PolicyData (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-594">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-594">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-595">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-595">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-596">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-596">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-597">Attribut msRTCSIP-policyType (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-597">msRTCSIP-PolicyType (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-598">Dieses Single-Value-UNICODE-Zeichenfolgenattribut enthält den Richtlinientyp.</span><span class="sxs-lookup"><span data-stu-id="3b159-598">This single-valued Unicode string attribute contains the policy type.</span></span> <span data-ttu-id="3b159-599">Gültige Richtlinientypen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-599">Valid policy types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-600">Besprechung</span><span class="sxs-lookup"><span data-stu-id="3b159-600">meeting</span></span></p></li>
<li><p><span data-ttu-id="3b159-601">Telefonie</span><span class="sxs-lookup"><span data-stu-id="3b159-601">telephony</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-602">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-602">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-603">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-603">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-604">Attribut msRTCSIP-PoolAddress</span><span class="sxs-lookup"><span data-stu-id="3b159-604">msRTCSIP-PoolAddress</span></span></p></td>
<td><p><span data-ttu-id="3b159-605">Dieses Attribut gibt einen Link zurück zu dem Pool, zu dem ein Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="3b159-605">This attribute specifies a link back to the pool to which a computer belongs.</span></span> <span data-ttu-id="3b159-606">Dieses Attribut wird unabhängig davon festgesetzt, ob auf dem Computer die Standard Edition oder die Enterprise-Edition von lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-606">This attribute is set regardless of whether the computer is running the Standard Edition or the Enterprise Edition of Lync Server.</span></span> <span data-ttu-id="3b159-607">Dieses Attribut ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-607">This attribute is marked for global catalog replication.</span></span></p>
<p><span data-ttu-id="3b159-608">Der gültige Wert ist der Domänenname des Pools.</span><span class="sxs-lookup"><span data-stu-id="3b159-608">The valid value is the domain name of the pool.</span></span></p>
<p><span data-ttu-id="3b159-609">Link weiterleiten: <strong>Link-ID 11022</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-609">Forward link: <strong>Link ID 11022</strong></span></span></p>
<p><span data-ttu-id="3b159-610">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-FrontEndServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-610">The corresponding back link to this forward link attribute is <strong>msRTCSIP-FrontEndServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-611">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-611">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-612">Attribut msRTCSIP-PoolAddresses</span><span class="sxs-lookup"><span data-stu-id="3b159-612">msRTCSIP-PoolAddresses</span></span></p></td>
<td><p><span data-ttu-id="3b159-613">Hierbei handelt es sich um ein mehrwertiges Attribut, das eine Liste der Distinguished Names (DN) der Pools enthält, denen die MCU-Factory zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-613">This is a multi-valued attribute that contains a list of the distinguished names (DN) of pools with which the MCU factory is associated.</span></span></p>
<p><span data-ttu-id="3b159-614">Link zurück: <strong>Link-ID 11025</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-614">Back link: <strong>Link ID 11025</strong></span></span></p>
<p><span data-ttu-id="3b159-615">Der entsprechende Weiterleitungslink zu diesem zurück <strong>-Link lautet Attribut msRTCSIP-MCUFactoryPath</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-615">The corresponding forward link to this back link is <strong>msRTCSIP-MCUFactoryPath</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-616">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-616">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-617">Attribut msRTCSIP-PoolData</span><span class="sxs-lookup"><span data-stu-id="3b159-617">msRTCSIP-PoolData</span></span></p></td>
<td><p><span data-ttu-id="3b159-618">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-618">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-619">Neu in Live Communications Server 2005 mit SP1.</span><span class="sxs-lookup"><span data-stu-id="3b159-619">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-620">Attribut msRTCSIP-PoolDisplayName</span><span class="sxs-lookup"><span data-stu-id="3b159-620">msRTCSIP-PoolDisplayName</span></span></p></td>
<td><p><span data-ttu-id="3b159-621">Dieses Attribut gibt einen beliebigen Namen für einen Pool an, der von der Verwaltungskonsole angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-621">This attribute specifies an arbitrary name for a pool that is displayed by the management console.</span></span> <span data-ttu-id="3b159-622">Dieser Name kann vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-622">This name can be changed by the administrator.</span></span></p>
<p><span data-ttu-id="3b159-623">Der gültige Wert ist eine Zeichenfolge, die den Namen eines Pools darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-623">The valid value is a string representing the name of a pool.</span></span></p></td>
<td><p><span data-ttu-id="3b159-624">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-624">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-625">Attribut msRTCSIP-PoolDomainFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-625">msRTCSIP-PoolDomainFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-626">Dieses Attribut ist ein einwertiger Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="3b159-626">This attribute is a single-valued string value.</span></span> <span data-ttu-id="3b159-627">Der Wert dieses Attributs steht, sofern vorhanden, für den Domänen-FQDN des Pools, wenn der Administrator einen Front-End-Pool mit einem FQDN erstellen möchte, der nicht der Active Directory-Domänenstruktur entspricht, in der der Front-End-Pool erstellt wird (beispielsweise ein SIP-Namespace, der vom DNS-Namespace (Domain Name System) nicht mehr verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="3b159-627">The value of this attribute, when present, represents the pool’s domain FQDN if the administrator wants to create a Front End pool with an FQDN that does not conform to the Active Directory domain structure in which the Front End pool is created (for example, a SIP namespace disjoined from Domain Name System (DNS) namespace).</span></span></p>
<p><span data-ttu-id="3b159-628">Wir empfehlen, dass Sie den Domänen-FQDN des Front-End-Pools dem Domänennamen Teil als die Active Directory-Domäne zuordnen, in der sich der Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="3b159-628">We recommend that you map the Front End pool domain FQDN to the domain name portion as the Active Directory domain in which the pool resides.</span></span> <span data-ttu-id="3b159-629">Wenn in diesem Attribut kein Wert vorhanden ist, wird der FQDN des Front-End-Pools standardmäßig auf die Active Directory-Domänennamenstruktur zurückgeführt, die durch das <strong>dNSHostName</strong> -Attribut gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-629">Therefore, when no value is present in this attribute, the Front End pool FQDN will default to the Active Directory domain name structure, as denoted by the <strong>dnsHostName</strong> attribute.</span></span></p></td>
<td><p><span data-ttu-id="3b159-630">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-630">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-631">Attribut msRTCSIP-PoolFunctionality</span><span class="sxs-lookup"><span data-stu-id="3b159-631">msRTCSIP-PoolFunctionality</span></span></p></td>
<td><p><span data-ttu-id="3b159-632">Eine mehrwertige Liste der Domänennamen aller lync Server-Enterprise Edition-Server, die einem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-632">A multi-valued list of the domain names of all Lync Server, Enterprise Edition servers associated with a pool.</span></span> <span data-ttu-id="3b159-633">Dieses Attribut des Typs Integer definiert, ob der Pool Instant Messaging (im) und Anwesenheitsfunktionen und Besprechungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b159-633">This attribute of type integer defines whether the pool is capable of instant messaging (IM) and presence, and meetings.</span></span></p>
<p><span data-ttu-id="3b159-634">Die möglichen gültigen Wertetypen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-634">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-635">Undefined: Chat-und Anwesenheitsdienst (Live Communications Server 2005 und 2003)</span><span class="sxs-lookup"><span data-stu-id="3b159-635">Undefined: IM and Presence Service (Live Communications Server 2005 and 2003)</span></span></p></li>
<li><p><span data-ttu-id="3b159-636">1: Chat und Anwesenheitsdienst (lync Server)</span><span class="sxs-lookup"><span data-stu-id="3b159-636">1: IM and Presence Service (Lync Server)</span></span></p></li>
<li><p><span data-ttu-id="3b159-637">2: Chat und Anwesenheits-und Besprechungs Dienst (lync Server)</span><span class="sxs-lookup"><span data-stu-id="3b159-637">2: IM and Presence and Meeting Service (Lync Server)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-638">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-638">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-639">Attribut msRTCSIP-pooltype</span><span class="sxs-lookup"><span data-stu-id="3b159-639">msRTCSIP-PoolType</span></span></p></td>
<td><p><span data-ttu-id="3b159-640">Dieses Attribut gibt an, ob ein Serverpool den Standard Edition-Server oder Enterprise Edition-Server ausführt.</span><span class="sxs-lookup"><span data-stu-id="3b159-640">This attribute specifies whether a server pool is running Standard Edition server or Enterprise Edition server.</span></span> <span data-ttu-id="3b159-641">Dieses Attribut ist ein Bitmaskenwert vom Typ Integer.</span><span class="sxs-lookup"><span data-stu-id="3b159-641">This attribute is a bit-mask value of type integer.</span></span> <span data-ttu-id="3b159-642">Jede Option wird durch ein Bit dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-642">Each option is represented by a bit.</span></span></p>
<p><span data-ttu-id="3b159-643">Die gültigen Werte (und zugeordnete Bit-Positionen) lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-643">The valid values (and associated bit positions) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-644">1: Standard Edition-Server, hostet Benutzer (Bit-Position 0)</span><span class="sxs-lookup"><span data-stu-id="3b159-644">1: Standard Edition server, hosts users (bit position 0)</span></span></p></li>
<li><p><span data-ttu-id="3b159-645">2: Enterprise Edition-Server, hostet Benutzer (Bit-Position 1)</span><span class="sxs-lookup"><span data-stu-id="3b159-645">2: Enterprise Edition server, hosts users (bit position 1)</span></span></p></li>
<li><p><span data-ttu-id="3b159-646">4: Standard Edition-Server, Host-Anwendungen (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-646">4: Standard Edition server, hosts applications (bit position 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-647">8: Enterprise Edition-Server, Host-Anwendungen (Bit-Position 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-647">8: Enterprise Edition server, hosts applications (bit position 3)</span></span></p></li>
</ul>
<p><span data-ttu-id="3b159-648">Da lync Server keine Pools unterstützt, die nur Anwendungen hosten, gelten die einzigen gültigen Werte wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-648">Because Lync Server does not support pools that host only applications, the only valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-649">5: Standard Edition-Server, hostet Benutzer und Anwendungen (Bit-Positionen 0 und 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-649">5: Standard Edition server, hosts users and applications (bit positions 0 and 2)</span></span></p></li>
<li><p><span data-ttu-id="3b159-650">10: Enterprise Edition-Server, hostet Benutzer und Anwendungen (Bit-Positionen 1 und 3)</span><span class="sxs-lookup"><span data-stu-id="3b159-650">10: Enterprise Edition server, hosts users and applications (bit positions 1 and 3)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-651">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-651">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-652">Attribut msRTCSIP-PoolVersion</span><span class="sxs-lookup"><span data-stu-id="3b159-652">msRTCSIP-PoolVersion</span></span></p></td>
<td><p><span data-ttu-id="3b159-653">Dieses Attribut definiert die Pool-Version.</span><span class="sxs-lookup"><span data-stu-id="3b159-653">This attribute defines the pool version.</span></span> <span data-ttu-id="3b159-654">Hierbei handelt es sich um einen ganzzahligen Typ, der mit jeder Hauptprodukt Version inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-654">It is an integer type that is incremented with each major product release.</span></span></p>
<p><span data-ttu-id="3b159-655">Die möglichen gültigen Wertetypen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-655">The possible valid value types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-656">0: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b159-656">0: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="3b159-657">1: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="3b159-657">1: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="3b159-658">2: Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-658">2: Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="3b159-659">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-659">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="3b159-660">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3b159-660">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="3b159-661">5: lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="3b159-661">5: Lync Server 2010</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-662">Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-662">Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-663">Attribut msRTCSIP-PresenceFlags</span><span class="sxs-lookup"><span data-stu-id="3b159-663">msRTCSIP-PresenceFlags</span></span></p></td>
<td><p><span data-ttu-id="3b159-664">Dieses Attribut enthält Optionen und Flags, mit denen Anwesenheitseinstellungen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-664">This attribute contains options and flags that define presence settings.</span></span></p></td>
<td><p><span data-ttu-id="3b159-665">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-665">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-666">Attribut msRTCSIP-PresencePolicy</span><span class="sxs-lookup"><span data-stu-id="3b159-666">msRTCSIP-PresencePolicy</span></span></p></td>
<td><p><span data-ttu-id="3b159-667">Dieses Attribut enthält den DN für ein Anwesenheitsrichtlinienobjekt.</span><span class="sxs-lookup"><span data-stu-id="3b159-667">This attribute contains the DN for a presence policy object.</span></span></p></td>
<td><p><span data-ttu-id="3b159-668">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-668">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-669">Attribut msRTCSIP-PrimaryHomeServer</span><span class="sxs-lookup"><span data-stu-id="3b159-669">msRTCSIP-PrimaryHomeServer</span></span></p></td>
<td><p><span data-ttu-id="3b159-670">Dieses Attribut ermöglicht einem Benutzer oder Kontakt für SIP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3b159-670">This attribute enables a user or contact for SIP messaging.</span></span> <span data-ttu-id="3b159-671">Sie wird der Contact-Klasse hinzugefügt, da in der zentralen Gesamtstrukturtopologie die Kontaktobjekte, nicht die Benutzerobjekte, SIP-fähig sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-671">It is added to the contact class because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="3b159-672">Der gültige Wert ist der DN des Standard Edition-Servers oder des Enterprise Edition-Front-End-Pools, in dem ein Benutzer beheimatet ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-672">The valid value is the DN of the Standard Edition server or Enterprise Edition Front End pool where a user is homed.</span></span></p></td>
<td><p><span data-ttu-id="3b159-673">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-673">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-674">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="3b159-674">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="3b159-675">Dieses Attribut enthält die SIP-Adresse eines angegebenen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3b159-675">This attribute contains the SIP address of a given user.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-676">Attribut msRTCSIP-Privatsphäre</span><span class="sxs-lookup"><span data-stu-id="3b159-676">msRTCSIP-PrivateLine</span></span></p></td>
<td><p><span data-ttu-id="3b159-677">Dieses Attribut enthält die Geräte-ID des privaten Leitungs Geräts.</span><span class="sxs-lookup"><span data-stu-id="3b159-677">This attribute contains the device ID of the private line device.</span></span></p></td>
<td><p><span data-ttu-id="3b159-678">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-678">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-679">Attribut msRTCSIP-routingfähig</span><span class="sxs-lookup"><span data-stu-id="3b159-679">msRTCSIP-Routable</span></span></p></td>
<td><p><span data-ttu-id="3b159-680">Dieses Attribut ist ein boolesches Attribut, das verwendet wird, um zu ermitteln, ob lync Server zum Weiterleiten an diesen Dienst mit seiner GRUU-Adresse autorisiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-680">This attribute is a Boolean attribute used to determine whether Lync Server is authorized to route to this service using its GRUU address.</span></span> <span data-ttu-id="3b159-681">Wenn dieser Wert auf " <strong>true</strong>" festgelegt ist, ist lync Server zum Weiterleiten an diesen Dienst autorisiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-681">If this value is set to <strong>TRUE</strong>, Lync Server is authorized to route to this service.</span></span> <span data-ttu-id="3b159-682">Wenn dieser Wert auf " <strong>false</strong>" festgelegt ist, ist lync Server nicht zum Weiterleiten an diesen Dienst autorisiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-682">If this value is set to <strong>FALSE</strong>, Lync Server is not authorized to route to this service.</span></span></p></td>
<td><p><span data-ttu-id="3b159-683">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-683">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-684">Attribut msRTCSIP-RouteUsageAttribute (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-684">msRTCSIP-RouteUsageAttribute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-685">Dieses Single-Value-UNICODE-Zeichenfolgenattribut definiert ein Attribut, das die Verwendung für eine Telefonroute qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b159-685">This single-valued UNICODE string attribute defines an attribute that qualifies the usage for a phone route.</span></span> <span data-ttu-id="3b159-686">Die Auswahl einer Telefonroute wird auf der Grundlage von zwei Elementen bestimmt: dem Nutzungs Attribut, das der Telefonroute zugewiesen ist, und den zulässigen Richtlinien Verwendungsattributen des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="3b159-686">Selection of a phone route is determined based on two elements: the usage attribute assigned to the phone route and the caller’s allowed policy usage attributes.</span></span> <span data-ttu-id="3b159-687">Die erste Telefonroute mit einem Nutzungs Attribut, das der zulässigen Verwendung des Anrufers entspricht, ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3b159-687">The first phone route with a usage attribute that matches the caller’s allowed usage is selected.</span></span></p></td>
<td><p><span data-ttu-id="3b159-688">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-688">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-689">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-689">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-690">Attribut msRTCSIP-RouteUsageLinks (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-690">msRTCSIP-RouteUsageLinks (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-691">Dieses Attribut für mehrwertigen Distinguished Name (DN) enthält eine Liste der definierten Namen für die Routenverwendung.</span><span class="sxs-lookup"><span data-stu-id="3b159-691">This multi-valued distinguished name (DN) attribute contains a list of route usage distinguished names.</span></span></p>
<p><span data-ttu-id="3b159-692">Link weiterleiten: <strong>Link-ID 11032</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-692">Forward link: <strong>Link ID 11032</strong></span></span></p>
<p><span data-ttu-id="3b159-693">Dieses Attribut ist ein Forward-Link zum entsprechenden Backlink <strong>Attribut msRTCSIP-PhoneRouteBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-693">This attribute is a forward link to the corresponding back link <strong>msRTCSIP-PhoneRouteBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-694">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-694">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-695">Attribut msRTCSIP-RoutingPoolDN</span><span class="sxs-lookup"><span data-stu-id="3b159-695">msRTCSIP-RoutingPoolDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-696">Dieses Attribut enthält den DN, der auf den Pool verweist, der den gesamten SIP-Datenverkehr an diesen MCU oder vertrauenswürdigen Dienst durchlaufen muss.</span><span class="sxs-lookup"><span data-stu-id="3b159-696">This attribute contains the DN that points to the pool that all SIP traffic addressed to this MCU or Trusted Service must go through.</span></span></p></td>
<td><p><span data-ttu-id="3b159-697">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-697">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-698">Attribut msRTCSIP-RuleName (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-698">msRTCSIP-RuleName (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-699">Dieses einmalige UNICODE-Zeichenfolgenattribut gibt den Anzeigenamen der Normalisierungsregel an, sodass von einem Administrator einfach darauf verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-699">This single-valued UNICODE string attribute specifies the friendly name of the normalization rule, so it can easily be referenced by an administrator.</span></span></p></td>
<td><p><span data-ttu-id="3b159-700">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-700">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-701">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-701">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-702">Attribut msRTCSIP-Schemaversion</span><span class="sxs-lookup"><span data-stu-id="3b159-702">msRTCSIP-SchemaVersion</span></span></p></td>
<td><p><span data-ttu-id="3b159-703">Dieses Attribut steht für die Schemaversion, die derzeit in der Organisation bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-703">This attribute represents the schema version currently deployed in the organization.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-704">Attribut msRTCSIP-SearchMaxRequests (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-704">msRTCSIP-SearchMaxRequests (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-705">Dieses Attribut schränkt die Anzahl der Suchergebnisse ein, die von einer Verzeichnissuche zurückgegeben werden sollen, wenn ein Benutzer mit Communicator nach einem Kontakt sucht.</span><span class="sxs-lookup"><span data-stu-id="3b159-705">This attribute limits the number of search results to be returned from a directory search when a user searches for a contact using Communicator.</span></span> <span data-ttu-id="3b159-706">Mit diesem Attribut wird der vom Client bereitgestellte Wert überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3b159-706">This attribute will override the value provided by the client.</span></span></p></td>
<td><p><span data-ttu-id="3b159-707">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-707">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-708">Attribut msRTCSIP-SearchMaxResults (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-708">msRTCSIP-SearchMaxResults (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-709">Dieses Attribut schränkt die Anzahl der zurückgegebenen Suchanforderungen ein.</span><span class="sxs-lookup"><span data-stu-id="3b159-709">This attribute limits the number of search requests returned.</span></span></p></td>
<td><p><span data-ttu-id="3b159-710">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-710">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-711">Attribut msRTCSIP-ServerBL</span><span class="sxs-lookup"><span data-stu-id="3b159-711">msRTCSIP-ServerBL</span></span></p></td>
<td><p><span data-ttu-id="3b159-712">Bei diesem mehrwertigen Attribut handelt es sich um einen Link zurück, der eine Liste von Distinguished Names (DN) enthält.</span><span class="sxs-lookup"><span data-stu-id="3b159-712">This multi-valued attribute is a back link that contains a list of distinguished names (DN).</span></span> <span data-ttu-id="3b159-713">Dieser DNS-Punkt verweist auf ein Pool-oder <strong>TrustedService</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b159-713">These DNs point to a pool or <strong>TrustedService</strong> object.</span></span></p>
<p><span data-ttu-id="3b159-714">Dieses Attribut entspricht dem Forward-Link <strong>Attribut msRTCSIP-TrustedServiceLinks</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-714">This attribute corresponds to the forward link <strong>msRTCSIP-TrustedServiceLinks</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-715">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-715">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-716">Attribut msRTCSIP-Server</span><span class="sxs-lookup"><span data-stu-id="3b159-716">msRTCSIP-ServerData</span></span></p></td>
<td><p><span data-ttu-id="3b159-717">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-717">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-718">Attribut msRTCSIP-ServerReferenceBL (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-718">msRTCSIP-ServerReferenceBL (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-719">Dieses mehrwertige Attribut enthält eine Liste von Distinguished Names.</span><span class="sxs-lookup"><span data-stu-id="3b159-719">This multi-valued attribute contains a list of distinguished names.</span></span> <span data-ttu-id="3b159-720">Bei diesen definierten Namen handelt es sich um zurück-Links, die auf andere Serverobjekte verweisen, denen ein Standardstandortprofil zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b159-720">These distinguished names are back links that reference other server objects that can be assigned a default location profile.</span></span></p>
<p><span data-ttu-id="3b159-721">Link zurück: <strong>Link-ID 11037</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-721">Back link: <strong>Link ID 11037</strong></span></span></p>
<p><span data-ttu-id="3b159-722">Der entsprechende Weiterleitungslink zu diesem zurück <strong>-Link lautet Attribut msRTCSIP-DefaultLocationProfileLink</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-722">The corresponding forward link to this back link is <strong>msRTCSIP-DefaultLocationProfileLink</strong>.</span></span></p>
<p><span data-ttu-id="3b159-723">Dieses zurück Link-Attribut verweist nur auf Pools und Vermittlungsserver.</span><span class="sxs-lookup"><span data-stu-id="3b159-723">This back link attribute references pools and Mediation Servers only.</span></span></p></td>
<td><p><span data-ttu-id="3b159-724">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-724">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-725">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-725">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-726">Attribut msRTCSIP-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="3b159-726">msRTCSIP-ServerVersion</span></span></p></td>
<td><p><span data-ttu-id="3b159-727">Dieses Attribut definiert die Versionsinformationen des Servers.</span><span class="sxs-lookup"><span data-stu-id="3b159-727">This attribute defines the version information of the server.</span></span> <span data-ttu-id="3b159-728">Diese Versionsnummer gilt für alle Serverrollen.</span><span class="sxs-lookup"><span data-stu-id="3b159-728">This version number applies to all server roles.</span></span> <span data-ttu-id="3b159-729">Hierbei handelt es sich um eine monoton-Ganzzahl, die mit jeder offiziellen Produktversion inkrementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-729">It is a monotonously increasing integer that increments with each official product release.</span></span></p>
<p><span data-ttu-id="3b159-730">Die möglichen gültigen Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-730">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-731">Undefined: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b159-731">Undefined: Live Communications Server 2003</span></span></p>
<p>                 <span data-ttu-id="3b159-732">Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="3b159-732">Live Communications Server 2005</span></span></p>
<p>                 <span data-ttu-id="3b159-733">Live Communications Server 2005 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3b159-733">Live Communications Server 2005 with SP1</span></span></p></li>
<li><p><span data-ttu-id="3b159-734">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-734">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="3b159-735">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3b159-735">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="3b159-736">5: lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="3b159-736">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="3b159-737">6: lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b159-737">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-738">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-738">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-739">Attribut msRTCSIP-Quellobjekttyp</span><span class="sxs-lookup"><span data-stu-id="3b159-739">msRTCSIP-SourceObjectType</span></span></p></td>
<td><p><span data-ttu-id="3b159-740">Dieses Attribut mit einem Wert vom Typ "Ganzzahl" gibt den Typ des Objekts an, auf das <strong>msDS-SourceObjectDN</strong> zeigt, wie im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3b159-740">This single-valued attribute of integer type specifies the type of object the <strong>msDS-SourceObjectDN</strong> points to, as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-741">NULL | 0x00000001: stellt ein Windows NT Server Principal-Benutzerobjekt aus einer anderen Gesamtstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-741">null | 0x00000001: Represents a Windows NT Server principal user object from a different forest</span></span></p></li>
<li><p><span data-ttu-id="3b159-742">Die folgenden Attribute stellen einen Gruppentyp aus einer anderen Gesamtstruktur für die Erweiterung der Verteilergruppe dar:</span><span class="sxs-lookup"><span data-stu-id="3b159-742">The following attributes represent a group type from a different forest for distribution group expansion:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="3b159-743">0x00000002: ADS_GROUP_TYPE_GLOBAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="3b159-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="3b159-744">0x00000004: ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="3b159-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="3b159-745">0x00000004: ADS_GROUP_TYPE_LOCAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="3b159-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span><span class="sxs-lookup"><span data-stu-id="3b159-746">0x00000008: ADS_GROUP_TYPE_UNIVERSAL_GROUP</span></span></p></li>
<li><p><span data-ttu-id="3b159-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span><span class="sxs-lookup"><span data-stu-id="3b159-747">0x80000000: ADS_GROUP_TYPE_SECURITY_ENABLED</span></span></p></li>
<li><p><span data-ttu-id="3b159-748">0x90000000: stellt eine automatische Telefonzentrale oder ein Teilnehmerzugriffs Objekt aus derselben Gesamtstruktur oder einer anderen Gesamtstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="3b159-748">0x90000000: Represents an Auto-Attendant or subscriber access object from the same forest or a different forest</span></span></p></li>
</ul></li>
</ul></td>
<td><p><span data-ttu-id="3b159-749">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-749">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-750">Attribut msRTCSIP-SubscriptionAuthRequired (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-750">msRTCSIP-SubscriptionAuthRequired (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-751">Neu in Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b159-751">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="3b159-752">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-752">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-753">Attribut msRTCSIP-TargetHomeServer</span><span class="sxs-lookup"><span data-stu-id="3b159-753">msRTCSIP-TargetHomeServer</span></span></p></td>
<td><p><span data-ttu-id="3b159-754">Mit diesem Attribut können Sie einen Benutzer oder ein Kontaktobjekt aus einem lync Server-Pool in einen anderen verschieben.</span><span class="sxs-lookup"><span data-stu-id="3b159-754">This attribute enables you to move a user or contact object from one Lync Server pool to another.</span></span> <span data-ttu-id="3b159-755">Dieses Attribut wird der Contact-Klasse hinzugefügt, da in der zentralen Gesamtstrukturtopologie die Kontaktobjekte, nicht die Benutzerobjekte, SIP-fähig sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-755">This attribute is added to the contact class, because in the central forest topology, contact objects, not user objects, are SIP enabled.</span></span></p>
<p><span data-ttu-id="3b159-756">Der gültige Wert ist der DN des Ziel-Standard Edition-Servers oder-Front-End-Pools, in den ein Benutzer verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b159-756">The valid value is the DN of the destination Standard Edition server or Front End pool to which a user is to be moved.</span></span></p></td>
<td><p><span data-ttu-id="3b159-757">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-757">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-758">Attribut msRTCSIP-TargetPhoneNumber (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-758">msRTCSIP-TargetPhoneNumber (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-759">Dieses Attribut mit einer Wert Zeichenfolge enthält ein Telefonnummernmuster oder einen Bereich, der an die in <strong>Attribut msRTCSIP-Gateways</strong>definierten Gateways weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b159-759">This single-valued string attribute contains a phone number pattern or range to route to the specified gateways defined in <strong>msRTCSIP-Gateways</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-760">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-760">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-761">Attribut msRTCSIP-TargetUserPolicies</span><span class="sxs-lookup"><span data-stu-id="3b159-761">msRTCSIP-TargetUserPolicies</span></span></p></td>
<td><p><span data-ttu-id="3b159-762">Dieses Attribut speichert Name-Wert-Paare für Zielrichtlinien für lync Server-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b159-762">This attribute stores name-value pairs for target policies for Lync Server users.</span></span></p></td>
<td><p><span data-ttu-id="3b159-763">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-763">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-764">Attribut msRTCSIP-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="3b159-764">msRTCSIP-TenantId</span></span></p></td>
<td><p><span data-ttu-id="3b159-765">Dieses Attribut speichert den eindeutigen Bezeichner für einen Mandanten.</span><span class="sxs-lookup"><span data-stu-id="3b159-765">This attribute stores the unique identifier for a tenant.</span></span></p></td>
<td><p><span data-ttu-id="3b159-766">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-766">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-767">Attribut msRTCSIP-Translation (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-767">msRTCSIP-Translation (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-768">Dieses Attribut wird von der Sprachfunktion von lync Server verwendet und enthält die Übersetzungs Zeichenfolge, die für die gewählte Nummer gelten soll, wenn eine Übereinstimmung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-768">This attribute is used by the voice feature of Lync Server and contains the translation string to apply on the dialed number, if a match is found.</span></span></p></td>
<td><p><span data-ttu-id="3b159-769">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-769">New in Office Communications Server 2007.</span></span></p>
<p><span data-ttu-id="3b159-770">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-770">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-771">Attribut msRTCSIP-TrustedMCUData</span><span class="sxs-lookup"><span data-stu-id="3b159-771">msRTCSIP-TrustedMCUData</span></span></p></td>
<td><p><span data-ttu-id="3b159-772">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-772">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-773">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-773">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-774">Attribut msRTCSIP-TrustedMCUFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-774">msRTCSIP-TrustedMCUFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-775">Dieses Attribut ist ein Zeichenfolgenwert, der den FQDN des MCU enthält.</span><span class="sxs-lookup"><span data-stu-id="3b159-775">This attribute is a string value that contains the FQDN of the MCU.</span></span> <span data-ttu-id="3b159-776">Hierbei handelt es sich um ein Single-Value-Attribut.</span><span class="sxs-lookup"><span data-stu-id="3b159-776">This is a single-valued attribute.</span></span> <span data-ttu-id="3b159-777">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-777">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-778">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-778">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-779">Attribut msRTCSIP-TrustedProxyData</span><span class="sxs-lookup"><span data-stu-id="3b159-779">msRTCSIP-TrustedProxyData</span></span></p></td>
<td><p><span data-ttu-id="3b159-780">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-780">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-781">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-781">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-782">Attribut msRTCSIP-TrustedProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-782">msRTCSIP-TrustedProxyFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-783">Dieses Attribut ist ein Zeichenfolgenwert, der den FQDN des Servers enthält, auf dem Proxy Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-783">This attribute is a string value that contains the FQDN of the server running Proxy Server.</span></span> <span data-ttu-id="3b159-784">Dieses Attribut ist ein Single-Wert.</span><span class="sxs-lookup"><span data-stu-id="3b159-784">This attribute is single-valued.</span></span> <span data-ttu-id="3b159-785">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-785">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-786">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-786">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-787">Attribut msRTCSIP-TrustedServerData</span><span class="sxs-lookup"><span data-stu-id="3b159-787">msRTCSIP-TrustedServerData</span></span></p></td>
<td><p><span data-ttu-id="3b159-788">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-788">This attribute is reserved for future use.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-789">Attribut msRTCSIP-TrustedServerFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-789">msRTCSIP-TrustedServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-790">Dieses Attribut ist ein Single-Value-Attribut, das den FQDN eines vertrauenswürdigen Servers darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-790">This attribute is a single-valued attribute that represents the FQDN of a trusted server.</span></span></p></td>
<td><p><span data-ttu-id="3b159-791">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-791">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-792">Attribut msRTCSIP-TrustedServerVersion</span><span class="sxs-lookup"><span data-stu-id="3b159-792">msRTCSIP-TrustedServerVersion</span></span></p></td>
<td><p><span data-ttu-id="3b159-793">Dieses Attribut gibt die Versionsnummer eines Servers in der Liste der vertrauenswürdigen Server an.</span><span class="sxs-lookup"><span data-stu-id="3b159-793">This attribute specifies the version number of a server in the trusted server list.</span></span></p>
<p><span data-ttu-id="3b159-794">Die möglichen gültigen Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-794">The possible valid values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-795">NULL: Live Communications Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b159-795">NULL: Live Communications Server 2003</span></span></p></li>
<li><p><span data-ttu-id="3b159-796">2: Live Communications Server 2005</span><span class="sxs-lookup"><span data-stu-id="3b159-796">2: Live Communications Server 2005</span></span></p></li>
<li><p><span data-ttu-id="3b159-797">3: Office Communications Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-797">3: Office Communications Server 2007</span></span></p></li>
<li><p><span data-ttu-id="3b159-798">4: Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="3b159-798">4: Office Communications Server 2007 R2</span></span></p></li>
<li><p><span data-ttu-id="3b159-799">5: lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="3b159-799">5: Lync Server 2010</span></span></p></li>
<li><p><span data-ttu-id="3b159-800">6: lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b159-800">6: Lync Server 2013</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-801">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-801">New in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-802">Attribut msRTCSIP-TrustedServiceFlags</span><span class="sxs-lookup"><span data-stu-id="3b159-802">msRTCSIP-TrustedServiceFlags</span></span></p></td>
<td><p><span data-ttu-id="3b159-803">Dieses Attribut definiert die Optionen, die für den vertrauenswürdigen Dienst aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-803">This attribute defines the options that are enabled for the trusted service.</span></span></p></td>
<td><p><span data-ttu-id="3b159-804">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-804">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-805">Attribut msRTCSIP-TrustedServiceLinks</span><span class="sxs-lookup"><span data-stu-id="3b159-805">msRTCSIP-TrustedServiceLinks</span></span></p></td>
<td><p><span data-ttu-id="3b159-806">Dieses mehrwertige Attribut enthält eine Liste von Distinguished Names (DN), die auf ein vertrauenswürdiges Dienstobjekt verweisen, beispielsweise einen Media Relay-Authentifizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="3b159-806">This multi-valued attribute contains a list of distinguished names (DN) that reference a trusted service object, such as a Media Relay Authentication Service.</span></span> <span data-ttu-id="3b159-807">Ein Media Relay-Authentifizierungsdienst (physisch auf dem Edgeserver mit dem A/V-Konferenzdienst) muss einem Pool zugeordnet sein, um audioszenarien für Remotebenutzer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3b159-807">A Media Relay Authentication Service (physically collocated on the Edge Server running the A/V Conferencing service) must be associated with a pool to support audio scenarios for remote users.</span></span></p>
<p><span data-ttu-id="3b159-808">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-ServerBL</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-808">The corresponding back link to this forward link attribute is <strong>msRTCSIP-ServerBL</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-809">UC</span><span class="sxs-lookup"><span data-stu-id="3b159-809">UC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-810">Attribut msRTCSIP-TrustedServicePort</span><span class="sxs-lookup"><span data-stu-id="3b159-810">msRTCSIP-TrustedServicePort</span></span></p></td>
<td><p><span data-ttu-id="3b159-811">Dieses Attribut ist eine ganze Zahl, die die Portnummer definiert, die zum Herstellen der Verbindung mit diesem GRUU-Dienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b159-811">This attribute is an integer that defines the port number used to connect to this GRUU service.</span></span></p></td>
<td><p><span data-ttu-id="3b159-812">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-812">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-813">Attribut msRTCSIP-TrustedServiceType</span><span class="sxs-lookup"><span data-stu-id="3b159-813">msRTCSIP-TrustedServiceType</span></span></p></td>
<td><p><span data-ttu-id="3b159-814">Dieses Attribut ist ein Zeichenfolgenwert, der den Typ des GRUU-Diensts definiert, den er darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-814">This attribute is a string value that defines the type of GRUU service it represents.</span></span></p>
<p><span data-ttu-id="3b159-815">Die gültigen GRUU-Diensttypen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-815">The valid GRUU service types are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-816">„MediationServer“</span><span class="sxs-lookup"><span data-stu-id="3b159-816">MediationServer</span></span></p></li>
<li><p><span data-ttu-id="3b159-817">Gateway</span><span class="sxs-lookup"><span data-stu-id="3b159-817">Gateway</span></span></p></li>
<li><p><span data-ttu-id="3b159-818">Media Relay-Authentifizierungsdienst (MRAS)</span><span class="sxs-lookup"><span data-stu-id="3b159-818">Media Relay Authentication Service (MRAS)</span></span></p></li>
<li><p><span data-ttu-id="3b159-819">QoSM</span><span class="sxs-lookup"><span data-stu-id="3b159-819">QoSM</span></span></p></li>
<li><p><span data-ttu-id="3b159-820">Attribut msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="3b159-820">msRTCSIP-UserExtension CWA</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-821">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-821">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-822">Attribut msRTCSIP-TrustedWebComponentsServerData</span><span class="sxs-lookup"><span data-stu-id="3b159-822">msRTCSIP-TrustedWebComponentsServerData</span></span></p></td>
<td><p><span data-ttu-id="3b159-823">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-823">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-824">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-824">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-825">Attribut msRTCSIP-TrustedWebComponentsServerFQDN</span><span class="sxs-lookup"><span data-stu-id="3b159-825">msRTCSIP-TrustedWebComponentsServerFQDN</span></span></p></td>
<td><p><span data-ttu-id="3b159-826">Dieses Attribut ist ein Zeichenfolgenwert, der den FQDN des IIS mit lync Server-Webdiensten enthält.</span><span class="sxs-lookup"><span data-stu-id="3b159-826">This attribute is a string value that contains the FQDN of the IIS running Lync Server Web Services.</span></span> <span data-ttu-id="3b159-827">Hierbei handelt es sich um ein Single-Value-Attribut.</span><span class="sxs-lookup"><span data-stu-id="3b159-827">This is a single-valued attribute.</span></span> <span data-ttu-id="3b159-828">Der gültige Wert für jedes Segment ist 63 Zeichen; der gültige Wert für den gesamten FQDN ist 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3b159-828">The valid value for each segment is 63 characters; the valid value for the entire FQDN is 255 characters.</span></span></p></td>
<td><p><span data-ttu-id="3b159-829">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-829">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-830">Attribut msRTCSIP-UCFlags (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-830">msRTCSIP-UCFlags (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-831">Dieses Attribut definiert verschiedene UC-Optionen, die für alle Benutzer-oder Kontaktobjekte global aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-831">This attribute defines different UC options that are enabled globally to all user or contact objects.</span></span> <span data-ttu-id="3b159-832">Dieses Attribut ist ein Bitmaskenwert vom Typ "ganze Zahl".</span><span class="sxs-lookup"><span data-stu-id="3b159-832">This attribute is a bit-mask value of integer type.</span></span> <span data-ttu-id="3b159-833">Jede Option wird durch das vorhanden sein eines Bits dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-833">Each option is represented by the presence of a bit.</span></span></p>
<p><span data-ttu-id="3b159-834">Der mögliche gültige Wert (und die zugehörige Bit-Position) lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-834">The possible valid value (and associated bit position) are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-835">4: UsePerUserUCPolicy (Bit-Position 2)</span><span class="sxs-lookup"><span data-stu-id="3b159-835">4: UsePerUserUCPolicy (bit position 2)</span></span></p></li>
</ul>
<p><span data-ttu-id="3b159-836">Wenn dieses Bit festgelegt ist, wird die UC-Richtlinie pro Benutzerdefiniert.</span><span class="sxs-lookup"><span data-stu-id="3b159-836">When this bit is set, the UC policy is defined per user.</span></span></p></td>
<td><p><span data-ttu-id="3b159-837">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-837">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-838">Attribut msRTCSIP-UCPolicy (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-838">msRTCSIP-UCPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-839">Dieses Attribut mit einem Wert enthält den Distinguished Name (DN) der UC-Richtlinie, die der Administrator für diesen Benutzer zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="3b159-839">This single-valued attribute contains the distinguished name (DN) of the UC policy that the administrator has assigned for this user.</span></span></p></td>
<td><p><span data-ttu-id="3b159-840">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-840">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-841">Attribut msRTCSIP-UserDomainList (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-841">msRTCSIP-UserDomainList (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="3b159-842">Dieses Attribut enthält eine Liste aller Domänen in einer Gesamtstruktur, die SIP-fähige Benutzer hosten.</span><span class="sxs-lookup"><span data-stu-id="3b159-842">This attribute provides a list of all the domains in a forest that host SIP-enabled users.</span></span> <span data-ttu-id="3b159-843">Der Standardwert ist eine leere Liste, die angibt, dass alle Domänen in der Gesamtstruktur SIP-fähig sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-843">The default is an empty list, indicating that all domains in the forest are SIP-enabled.</span></span></p>
<p><span data-ttu-id="3b159-844">Gültige Werte sind mehrere Zeichenfolgen, die die Domänennamen einzelner Domänen darstellen.</span><span class="sxs-lookup"><span data-stu-id="3b159-844">Valid values are multiple strings representing the domain names of individual domains.</span></span></p></td>
<td><p><span data-ttu-id="3b159-845">Neu in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-845">New in Live Communications Server 2005.</span></span></p>
<p><span data-ttu-id="3b159-846">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="3b159-846">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-847">Attribut msRTCSIP-UserEnabled</span><span class="sxs-lookup"><span data-stu-id="3b159-847">msRTCSIP-UserEnabled</span></span></p></td>
<td><p><span data-ttu-id="3b159-848">Dieses Attribut bestimmt, ob der Benutzer derzeit für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3b159-848">This attribute determines whether the user is currently enabled for Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-849">Attribut msRTCSIP-UserExtension</span><span class="sxs-lookup"><span data-stu-id="3b159-849">msRTCSIP-UserExtension</span></span></p></td>
<td><p><span data-ttu-id="3b159-850">Dieses mehrwertige Attribut enthält eine Liste von Name-Wert-Paaren im Format von &quot; Name = Wert. &quot; Dieses Attribut ist für die Replikation des globalen Katalogs markiert.</span><span class="sxs-lookup"><span data-stu-id="3b159-850">This multi-valued attribute contains a list of name-value pairs in the format of &quot;name=value.&quot; This attribute is marked for global catalog replication.</span></span></p></td>
<td><p><span data-ttu-id="3b159-851">Neu in Live Communications Server 2005 mit SP1.</span><span class="sxs-lookup"><span data-stu-id="3b159-851">New in Live Communications Server 2005 with SP1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-852">Attribut msRTCSIP-UserLocationProfile</span><span class="sxs-lookup"><span data-stu-id="3b159-852">msRTCSIP-UserLocationProfile</span></span></p></td>
<td><p><span data-ttu-id="3b159-853">Dieses Attribut enthält den Distinguished Name (DN), der auf ein Standortprofilobjekt verweist.</span><span class="sxs-lookup"><span data-stu-id="3b159-853">This attribute contains the distinguished name (DN) that points to a location profile object.</span></span></p></td>
<td><p><span data-ttu-id="3b159-854">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="3b159-854">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-855">Attribut msRTCSIP-UserPolicies</span><span class="sxs-lookup"><span data-stu-id="3b159-855">msRTCSIP-UserPolicies</span></span></p></td>
<td><p><span data-ttu-id="3b159-856">Dieses Attribut speichert Name-Wert-Paare für Benutzerrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="3b159-856">This attribute stores name-value pairs for user policies.</span></span></p></td>
<td><p><span data-ttu-id="3b159-857">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="3b159-857">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-858">Attribut msRTCSIP-UserPolicy</span><span class="sxs-lookup"><span data-stu-id="3b159-858">msRTCSIP-UserPolicy</span></span></p></td>
<td><p><span data-ttu-id="3b159-859">Hierbei handelt es sich um ein mehrwertiges Attribut, das eine Liste von definierten Namen mit binären (DN_WITH_BINARY) enthält, die auf globale Benutzerrichtlinien unterschiedlicher Typen verweisen.</span><span class="sxs-lookup"><span data-stu-id="3b159-859">This is a multi-valued attribute containing a list of distinguished names with binary (DN_WITH_BINARY) pointing to global user policies of different types.</span></span> <span data-ttu-id="3b159-860">Der binäre Teil gibt den Typ der Richtlinie an, auf die der DN-Anteil verweist.</span><span class="sxs-lookup"><span data-stu-id="3b159-860">The binary part indicates the type of policy to which the DN portion points.</span></span></p>
<p><span data-ttu-id="3b159-861">Die gültigen binären Werte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3b159-861">The valid binary values are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-862">0x00000001: Besprechungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3b159-862">0x00000001: Meeting policy</span></span></p></li>
<li><p><span data-ttu-id="3b159-863">0x00000002: UC-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="3b159-863">0x00000002: UC policy</span></span></p></li>
<li><p><span data-ttu-id="3b159-864">0x00000005: Anwesenheitsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3b159-864">0x00000005: Presence policy</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-865">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-865">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-866">Attribut msRTCSIP-UserRoutingGroupId</span><span class="sxs-lookup"><span data-stu-id="3b159-866">msRTCSIP-UserRoutingGroupId</span></span></p></td>
<td><p><span data-ttu-id="3b159-867">Hierbei handelt es sich um die SIP-Routinggruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="3b159-867">This is the SIP routing group ID.</span></span> <span data-ttu-id="3b159-868">Benutzer in der gleichen Gruppe werden für denselben Front-End-Server registriert.</span><span class="sxs-lookup"><span data-stu-id="3b159-868">Users in the same group will register to the same Front End Server.</span></span></p></td>
<td><p><span data-ttu-id="3b159-869">Neu in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3b159-869">New in Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-870">Attribut msRTCSIP-WebComponentsData</span><span class="sxs-lookup"><span data-stu-id="3b159-870">msRTCSIP-WebComponentsData</span></span></p></td>
<td><p><span data-ttu-id="3b159-871">Hierbei handelt es sich um ein mehrwertiges Attribut.</span><span class="sxs-lookup"><span data-stu-id="3b159-871">This is a multi-valued attribute.</span></span> <span data-ttu-id="3b159-872">Dieses Attribut ist für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3b159-872">This attribute is reserved for future use.</span></span></p></td>
<td><p><span data-ttu-id="3b159-873">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-873">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-874">Attribut msRTCSIP-WebComponentsPoolAddress</span><span class="sxs-lookup"><span data-stu-id="3b159-874">msRTCSIP-WebComponentsPoolAddress</span></span></p></td>
<td><p><span data-ttu-id="3b159-875">Dieses Attribut mit einem Wert verweist auf den Pool oder den Standard Edition-Server, zu dem die Webkomponenten gehören.</span><span class="sxs-lookup"><span data-stu-id="3b159-875">This single-valued attribute points to the pool or Standard Edition server to which the web components belong.</span></span></p>
<p><span data-ttu-id="3b159-876">Link weiterleiten: <strong>Link-ID 11028</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-876">Forward link: <strong>Link ID 11028</strong></span></span></p>
<p><span data-ttu-id="3b159-877">Der entsprechende Link zurück zu diesem Forward Link-Attribut lautet <strong>Attribut msRTCSIP-WebComponentsServers</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-877">The corresponding back link to this forward link attribute is <strong>msRTCSIP-WebComponentsServers</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-878">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-878">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-879">Attribut msRTCSIP-WebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="3b159-879">msRTCSIP-WebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="3b159-880">Dieses Attribut ist eine mehrwertige Liste mit definierten Namen.</span><span class="sxs-lookup"><span data-stu-id="3b159-880">This attribute is a multi-valued list of distinguished names.</span></span> <span data-ttu-id="3b159-881">Dieses Attribut enthält eine Liste aller Webserver, die diesem Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3b159-881">This attribute contains a list of all Web servers associated with this pool.</span></span></p>
<p><span data-ttu-id="3b159-882">Link zurück: <strong>Link-ID 11029</strong></span><span class="sxs-lookup"><span data-stu-id="3b159-882">Back link: <strong>Link ID 11029</strong></span></span></p>
<p><span data-ttu-id="3b159-883">Der entsprechende Weiterleitungslink zu diesem zurück <strong>-Link lautet Attribut msRTCSIP-WebComponentsPoolAddress</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b159-883">The corresponding forward link to this back link is <strong>msRTCSIP-WebComponentsPoolAddress</strong>.</span></span></p></td>
<td><p><span data-ttu-id="3b159-884">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="3b159-884">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-885">Attribut msRTCSIP-WMIInstanceId (veraltet)</span><span class="sxs-lookup"><span data-stu-id="3b159-885">msRTCSIP-WMIInstanceId (obsolete)</span></span></p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="3b159-886">Neu in Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3b159-886">New in Live Communications Server 2003.</span></span></p>
<p><span data-ttu-id="3b159-887">Veraltet in Live Communications Server 2005.</span><span class="sxs-lookup"><span data-stu-id="3b159-887">Obsolete in Live Communications Server 2005.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-888">OtherIPPhone</span><span class="sxs-lookup"><span data-stu-id="3b159-888">OtherIPPhone</span></span></p></td>
<td><p><span data-ttu-id="3b159-889">Dieses vorhandene Active Directory-Attribut wird von der Telefonie verwendet, um die Liste der alternativen TCP/IP-Adressen für ein Telefon festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3b159-889">This existing Active Directory attribute is used by telephony to specify the list of alternate TCP/IP addresses for a phone.</span></span></p></td>
<td><p><span data-ttu-id="3b159-890">Neu im Windows Server 2008-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="3b159-890">New in Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-891">PhoneOfficeOther</span><span class="sxs-lookup"><span data-stu-id="3b159-891">PhoneOfficeOther</span></span></p></td>
<td><p><span data-ttu-id="3b159-892">Dieses vorhandene Active Directory-Attribut wird von den VoIP-Komponenten in lync Server für nur-Kontaktobjekte verwendet, um Anrufe an die automatische Telefonzentrale und die Teilnehmerzugriffsnummern von Unified Messaging weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="3b159-892">This existing Active Directory attribute is used by the voice components in Lync Server, for contact objects only, for the purpose of routing calls to the unified messaging auto-attendant and subscriber access numbers.</span></span> <span data-ttu-id="3b159-893">Die bedingungslose Anruf Weiterleitungsadresse wird in diesem mehrwertigen Attribut gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3b159-893">The unconditional call forwarding address is stored in this multi-valued attribute.</span></span> <span data-ttu-id="3b159-894">Dieses Konto wird für den spezifischen Zweck der automatischen Telefonzentrale und des Abonnenten Zugriffs erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b159-894">This account is created for the specific purpose of auto-attendant and subscriber access.</span></span> <span data-ttu-id="3b159-895">Die Attribute dieses Kontos sollten nicht von Administratoren geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3b159-895">This account’s attributes should not be modified by administrators.</span></span></p></td>
<td><p><span data-ttu-id="3b159-896">Neu im Windows 2000-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="3b159-896">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b159-897">ProxyAddresses</span><span class="sxs-lookup"><span data-stu-id="3b159-897">ProxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="3b159-898">Dieses vorhandene Active Directory-mehrwertige Attribut ist Teil des Active Directory-Basisschemas, das in Windows 2000 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b159-898">This existing Active Directory multi-valued attribute is part of the base Active Directory schema introduced in Windows 2000.</span></span> <span data-ttu-id="3b159-899">Dieses Attribut enthält die verschiedenen X400-, x500-und SMTP-Adressen der e-Mail-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="3b159-899">This attribute contains the various X400, X500, and SMTP addresses of the user’s email.</span></span> <span data-ttu-id="3b159-900">In Live Communications Server 2003 und höher wird der SIP-URI des Benutzers mithilfe des SIP:-Tags zu dieser Liste hinzugefügt &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="3b159-900">In Live Communications Server 2003 and later, the user’s SIP URI is added to this list, using the &quot;sip:&quot; tag.</span></span></p>
<p><span data-ttu-id="3b159-901">Die folgenden Anwendungen durchsuchen den SIP-URI des Benutzers anhand dieses Attributs:</span><span class="sxs-lookup"><span data-stu-id="3b159-901">The following applications search the user’s SIP URI from this attribute:</span></span></p>
<ul>
<li><p><span data-ttu-id="3b159-902">Microsoft Office Outlook 2003-Messaging-und Zusammenarbeitsclient</span><span class="sxs-lookup"><span data-stu-id="3b159-902">Microsoft Office Outlook 2003 messaging and collaboration client</span></span></p></li>
<li><p><span data-ttu-id="3b159-903">Microsoft Office SharePoint Server 2007</span><span class="sxs-lookup"><span data-stu-id="3b159-903">Microsoft Office SharePoint Server 2007</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="3b159-904">Neu im Windows 2000-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="3b159-904">New in Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b159-905">TelephoneNumber</span><span class="sxs-lookup"><span data-stu-id="3b159-905">TelephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="3b159-906">Dieses vorhandene Active Directory-Attribut enthält die Telefonnummer für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b159-906">This existing Active Directory attribute contains the telephone number for the user.</span></span></p></td>
<td><p><span data-ttu-id="3b159-907">Neu im Windows 2000-Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="3b159-907">New in Windows 2000 operating system.</span></span></p></td>
</tr><span data-ttu-id="3b159-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b159-908">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

