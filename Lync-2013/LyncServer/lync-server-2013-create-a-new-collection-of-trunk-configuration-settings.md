---
title: 'Lync Server 2013: Erstellen einer neuen Sammlung von trunk-Konfigurationseinstellungen'
description: 'Lync Server 2013: Erstellen Sie eine neue Sammlung von trunk-Konfigurationseinstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new collection of trunk configuration settings
ms:assetid: 4ebd710c-38cd-4cff-9a45-df029d424580
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688054(v=OCS.15)
ms:contentKeyID: 49733647
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16ef4bb6393ec2385eaf7c642734bbc803d4dff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432184"
---
# <a name="create-a-new-collection-of-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="36de2-103">Erstellen einer neuen Sammlung von trunk-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36de2-103">Create a new collection of trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36de2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36de2-104">

<span> </span></span></span>

<span data-ttu-id="36de2-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="36de2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="36de2-106">SIP Trunk-Konfigurationseinstellungen definieren die Beziehungen und Funktionen zwischen einem Vermittlungs Server und dem PSTN-Gateway (Public Switched Telephone Network), einer IP-Public Branch Exchange (PBX) oder einem Session Border Controller (SBC) beim Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="36de2-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="36de2-107">Diese Einstellungen geben unter anderem Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="36de2-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="36de2-108">Ob Medienumgehung für die Trunks aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="36de2-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="36de2-109">Die Bedingungen, unter denen RTCP-Pakete (Real-Time Transport Control Protocol) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="36de2-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="36de2-110">Ob die SRTP-Verschlüsselung (Secure Real-Time Protocol) für jeden trunk erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="36de2-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="36de2-111">Wenn Sie Microsoft lync Server 2013 installieren, wird eine globale Sammlung von SIP-Trunk-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="36de2-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="36de2-112">Darüber hinaus können Administratoren benutzerdefinierte Auflistungen mit Einstellungen auf Standort- oder Dienstebene erstellen (nur für den PSTN-Gatewaydienst).</span><span class="sxs-lookup"><span data-stu-id="36de2-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span>

<span data-ttu-id="36de2-113">Beim Erstellen von SIP-Trunk-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung stehen Ihnen die folgenden Optionen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="36de2-113">When creating SIP trunk configuration settings using Lync Server Control Panel, the following options are available to you:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36de2-114">Benutzeroberflächeneinstellung</span><span class="sxs-lookup"><span data-stu-id="36de2-114">UI Setting</span></span></th>
<th><span data-ttu-id="36de2-115">PowerShell-Parameter</span><span class="sxs-lookup"><span data-stu-id="36de2-115">PowerShell Parameter</span></span></th>
<th><span data-ttu-id="36de2-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36de2-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36de2-117">Name</span><span class="sxs-lookup"><span data-stu-id="36de2-117">Name</span></span></p></td>
<td><p><span data-ttu-id="36de2-118">Identität</span><span class="sxs-lookup"><span data-stu-id="36de2-118">Identity</span></span></p></td>
<td><p><span data-ttu-id="36de2-p103">Eindeutige ID für die Sammlung. Diese Eigenschaft ist schreibgeschützt. Sie können die Identität einer Sammlung von Trunkkonfigurationseinstellungen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="36de2-p103">Unique identifier for the collection. This property is read-only; you cannot change the Identity of a collection of trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36de2-121">Description</span></span></p></td>
<td><p><span data-ttu-id="36de2-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36de2-122">Description</span></span></p></td>
<td><p><span data-ttu-id="36de2-123">Bietet Administratoren eine Möglichkeit, zusätzliche Informationen zu den Einstellungen zu speichern (z. B. Zweck der Trunkkonfiguration).</span><span class="sxs-lookup"><span data-stu-id="36de2-123">Provides a way for administrators to store addition information about the settings (for example, the purpose of the trunk configuration).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-124">Maximal unterstützte frühe Dialoge</span><span class="sxs-lookup"><span data-stu-id="36de2-124">Maximum early dialogs supported</span></span></p></td>
<td><p><span data-ttu-id="36de2-125">MaxEarlyDialogs</span><span class="sxs-lookup"><span data-stu-id="36de2-125">MaxEarlyDialogs</span></span></p></td>
<td><p><span data-ttu-id="36de2-126">Die maximale Anzahl von gegabelten Antworten, die ein PSTN-Gateway, eine IP-Nebenstellenanlage oder ein SBC (Session Border Controller) des Dienstanbieters auf an den Vermittlungsserver gesendete Einladungen empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="36de2-126">The maximum number of forked responses a PSTN gateway, IP-PBX, or SBC at the service provider can receive to an Invite that it sent to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-127">Unterstützte Verschlüsselungsstufe</span><span class="sxs-lookup"><span data-stu-id="36de2-127">Encryption support level</span></span></p></td>
<td><p><span data-ttu-id="36de2-128">SRTPMode</span><span class="sxs-lookup"><span data-stu-id="36de2-128">SRTPMode</span></span></p></td>
<td><p><span data-ttu-id="36de2-129">Legt den Umfang der Unterstützung zum Schutz von Mediendatenverkehr zwischen dem Vermittlungsserver und dem PSTN-Gateway, der IP-Nebenstellenanlage oder dem SBC (Session Border Controller) des Dienstanbieters fest.</span><span class="sxs-lookup"><span data-stu-id="36de2-129">Indicates the level of support for protecting media traffic between the Mediation Server and the PSTN Gateway, IP-PBX, or SBC at the service provider.</span></span> <span data-ttu-id="36de2-130">Bei der Medienumgehung muss dieser Wert mit der Einstellung „EncryptionLevel“ in der Medienkonfiguration kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="36de2-130">For media bypass cases, this value must be compatible with the EncryptionLevel setting in the media configuration.</span></span> <span data-ttu-id="36de2-131">Die Medienkonfiguration wird mithilfe der Cmdlets <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> und <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">CsMediaConfiguration</a> gesetzt.</span><span class="sxs-lookup"><span data-stu-id="36de2-131">Media configuration is set by using the <a href="https://docs.microsoft.com/powershell/module/skype/New-CsMediaConfiguration">New-CsMediaConfiguration</a> and <a href="https://docs.microsoft.com/powershell/module/skype/Set-CsMediaConfiguration">Set-CsMediaConfiguration</a> cmdlets.</span></span></p>
<p><span data-ttu-id="36de2-132">Zulässige Werte:</span><span class="sxs-lookup"><span data-stu-id="36de2-132">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="36de2-133">Erforderlich: Die SRTP-Verschlüsselung muss verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36de2-133">Required: SRTP encryption must be used.</span></span></p></li>
<li><p><span data-ttu-id="36de2-134">Optional: SRTP wird verwendet, wenn es vom Gateway unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="36de2-134">Optional: SRTP will be used if the gateway supports it.</span></span></p></li>
<li><p><span data-ttu-id="36de2-135">Nicht unterstützt: Die SRTP-Verschlüsselung wird nicht unterstützt und daher auch nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="36de2-135">Not Supported: SRTP encryption is not supported and therefore will not be used.</span></span></p></li>
</ul>
<p><span data-ttu-id="36de2-p105">„SRTPMode“ wird nur verwendet, wenn das Gateway zur Verwendung von TLS (Transport Layer Security) konfiguriert ist. Wenn das Gateway mit dem Transportprotokoll TCP (Transmission Control Protocol) konfiguriert ist, wird „SRTPMode“ intern auf „Nicht unterstützt“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="36de2-p105">SRTPMode is used only if the gateway is configured to use Transport Layer Security (TLS). If the gateway is configured with Transmission Control Protocol (TCP) as the transport, SRTPMode is internally set to Not Supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-138">Support melden</span><span class="sxs-lookup"><span data-stu-id="36de2-138">Refer support</span></span></p></td>
<td><p><span data-ttu-id="36de2-139">Enable3pccRefer</span><span class="sxs-lookup"><span data-stu-id="36de2-139">Enable3pccRefer</span></span></p>
<p><span data-ttu-id="36de2-140">EnableReferSupport</span><span class="sxs-lookup"><span data-stu-id="36de2-140">EnableReferSupport</span></span></p></td>
<td><p><span data-ttu-id="36de2-141">Mit der Einstellung <strong>Senden der Weiterleitung an Gateway aktivieren</strong> unterstützt der Trunk den Empfang von Weiterleitungsanforderungen vom Vermittlungsserver.</span><span class="sxs-lookup"><span data-stu-id="36de2-141">If set to <strong>Enable sending refer to the gateway</strong>, indicates that the trunk supports receiving Refer requests from the Mediation Server.</span></span></p>
<p><span data-ttu-id="36de2-142">Mit der Einstellung <strong>Weiterleitung mithilfe von Drittanbieteranrufsteuerung aktivieren</strong> kann das 3pcc-Protokoll verwendet werden, damit weitergeleitete Anrufe den gehosteten Standort umgehen können.</span><span class="sxs-lookup"><span data-stu-id="36de2-142">If set to <strong>Enable refer using third-party call control</strong>, indicates that the 3pcc protocol can be used to allow transferred calls to bypass the hosted site.</span></span> <span data-ttu-id="36de2-143">3PCC wird auch als &quot; Steuerung von Drittanbietern bezeichnet &quot; und tritt auf, wenn eine Drittpartei verwendet wird, um ein paar von Anrufern zu verbinden (beispielsweise einen Operator, der einen Anruf von Person a an Person B anlegt).</span><span class="sxs-lookup"><span data-stu-id="36de2-143">3pcc is also known as &quot;third party control,&quot; and occurs when a third-party is used to connect a pair of callers (for example, an operator placing a call from person A to person B).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-144">Medienumgehung aktivieren</span><span class="sxs-lookup"><span data-stu-id="36de2-144">Enable media bypass</span></span></p></td>
<td><p><span data-ttu-id="36de2-145">EnableBypass</span><span class="sxs-lookup"><span data-stu-id="36de2-145">EnableBypass</span></span></p></td>
<td><p><span data-ttu-id="36de2-p107">Gibt an, ob die Medienumgehung für diesen Trunk aktiviert ist. Die Medienumgehung kann nur aktiviert werden, wenn auch <strong>Zentralisierte Medienverarbeitung</strong> aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="36de2-p107">Indicates whether media bypass is enabled for this trunk. Media bypass can only be enabled if <strong>Centralized media processing</strong> is also enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-148">Zentralisierte Medienverarbeitung</span><span class="sxs-lookup"><span data-stu-id="36de2-148">Centralized media processing</span></span></p></td>
<td><p><span data-ttu-id="36de2-149">ConcentratedTopology</span><span class="sxs-lookup"><span data-stu-id="36de2-149">ConcentratedTopology</span></span></p></td>
<td><p><span data-ttu-id="36de2-p108">Gibt an, ob ein bekannter Medienendpunkt vorhanden ist. (Ein Beispiel für einen bekannten Medienendpunkt ist ein PSTN-Gateway, bei dem der Medienendpunkt dieselbe IP-Adresse hat wie der Signaldatenverkehrendpunkt.)</span><span class="sxs-lookup"><span data-stu-id="36de2-p108">Indicates whether there is a well-known media termination point. (An example of a well-known media termination point would be a PSTN gateway where the media termination has the same IP as the signaling termination.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-152">RTP-Verriegelung aktivieren</span><span class="sxs-lookup"><span data-stu-id="36de2-152">Enable RTP latching</span></span></p></td>
<td><p><span data-ttu-id="36de2-153">EnableRTPLatching</span><span class="sxs-lookup"><span data-stu-id="36de2-153">EnableRTPLatching</span></span></p></td>
<td><p><span data-ttu-id="36de2-p109">Gibt an, ob SIP-Trunks die RTP-Verriegelung unterstützen oder nicht. Die RTP-Verriegelung ist eine Technologie, die RTP-/RTCP-Verbindungen über NAT (Network Address Translator, Netzwerkadressenübersetzung) oder eine Firewall ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="36de2-p109">Indicates whether or not the SIP trunks support RTP latching. RTP latching is a technology that enables RTP/RTCP connectivity through a NAT (network address translator) device or firewall.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-156">Weiterleitung der Anrufliste aktivieren</span><span class="sxs-lookup"><span data-stu-id="36de2-156">Enable forward call history</span></span></p></td>
<td><p><span data-ttu-id="36de2-157">ForwardCallHistory</span><span class="sxs-lookup"><span data-stu-id="36de2-157">ForwardCallHistory</span></span></p></td>
<td><p><span data-ttu-id="36de2-158">Gibt an, ob Informationen zum Anrufverlauf durch den Trunk weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="36de2-158">Indicates whether call history information will be forwarded through the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-159">Weiterleitung von P-Asserted-Identity-Daten aktivieren</span><span class="sxs-lookup"><span data-stu-id="36de2-159">Enable forward P-Asserted-Identity data</span></span></p></td>
<td><p><span data-ttu-id="36de2-160">ForwardPAI</span><span class="sxs-lookup"><span data-stu-id="36de2-160">ForwardPAI</span></span></p></td>
<td><p><span data-ttu-id="36de2-p110">Gibt an, ob der PAI-Header (P-Asserted-Identity) zusammen mit dem Anruf weitergeleitet wird. Der PAI-Header bietet eine Möglichkeit, die Identität des Anrufers zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="36de2-p110">Indicates whether the P-Asserted-Identity (PAI) header will be forwarded along with the call. The PAI header provides a way to verify the identity of the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-163">Failovertimer für Ausgangsrouting aktivieren</span><span class="sxs-lookup"><span data-stu-id="36de2-163">Enable outbound routing failover timer</span></span></p></td>
<td><p><span data-ttu-id="36de2-164">EnableFastFailoverTimer</span><span class="sxs-lookup"><span data-stu-id="36de2-164">EnableFastFailoverTimer</span></span></p></td>
<td><p><span data-ttu-id="36de2-p111">Gibt an, ob ausgehende Anrufe, die vom Gateway nicht innerhalb von 10 Sekunden beantwortet werden, an den nächsten verfügbaren Trunk weitergeleitet werden. Wenn keine weiteren Trunks verfügbar sind, wird der Anruf automatisch beendet. In einer Organisation mit langsamen Netzwerk- und Gatewayreaktionen könnte dies dazu führen, dass Anrufe unnötigerweise beendet werden.</span><span class="sxs-lookup"><span data-stu-id="36de2-p111">Indicates whether outbound calls that are not answered by the gateway within 10 seconds will be routed to the next available trunk; if there are no additional trunks then the call will automatically be dropped. In an organization with slow networks and gateway responses, that could potentially result in calls being dropped unnecessarily.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-167">Zugeordnete PSTN-Verwendungen</span><span class="sxs-lookup"><span data-stu-id="36de2-167">Associated PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="36de2-168">PSTNUsages</span><span class="sxs-lookup"><span data-stu-id="36de2-168">PSTNUsages</span></span></p></td>
<td><p><span data-ttu-id="36de2-169">Dem Trunk zugewiesene Auflistung von PSTN-Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="36de2-169">Collection of PSTN usages assigned to the trunk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-170">Übersetzte Nummer zum Testen</span><span class="sxs-lookup"><span data-stu-id="36de2-170">Translated number to test</span></span></p></td>
<td><p><span data-ttu-id="36de2-171">-</span><span class="sxs-lookup"><span data-stu-id="36de2-171">N/A</span></span></p></td>
<td><p><span data-ttu-id="36de2-172">Eine Telefonnummer, die für Ad-hoc-Tests der Trunkkonfigurationseinstellungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="36de2-172">Phone number that can be used to do an ad hoc test of the trunk configuration settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-173">Zugehörige Übersetzungsregeln</span><span class="sxs-lookup"><span data-stu-id="36de2-173">Associated translation rules</span></span></p></td>
<td><p><span data-ttu-id="36de2-174">OutboundTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="36de2-174">OutboundTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="36de2-175">Sammlung an Regeln für die Telefonnummernübersetzung für Anrufe, die per Ausgangsrouting verarbeitet werden (Anrufe, die an Ziele in Nebenstellenanlagen oder im Telefonfestnetz weitergeleitet werden).</span><span class="sxs-lookup"><span data-stu-id="36de2-175">Collection of phone number translation rules that apply to calls handled by Outbound Routing (calls routed to PBX or PSTN destinations).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-176">Übersetzungsregeln für die gewählte Nummer</span><span class="sxs-lookup"><span data-stu-id="36de2-176">Called number translation rules</span></span></p></td>
<td><p><span data-ttu-id="36de2-177">OutboundCallingNumberTranslationRulesList</span><span class="sxs-lookup"><span data-stu-id="36de2-177">OutboundCallingNumberTranslationRulesList</span></span></p></td>
<td><p><span data-ttu-id="36de2-178">Dem Trunk zugewiesene Auflistung von ausgehenden Übersetzungsregeln für Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="36de2-178">Collection of outbound calling number translation rules assigned to the trunk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-179">Testtelefonnummer</span><span class="sxs-lookup"><span data-stu-id="36de2-179">Phone number to test</span></span></p></td>
<td><p><span data-ttu-id="36de2-180">-</span><span class="sxs-lookup"><span data-stu-id="36de2-180">N/A</span></span></p></td>
<td><p><span data-ttu-id="36de2-181">Eine Telefonnummer, die für Ad-hoc-Tests der Übersetzungsregeln verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="36de2-181">Phone number that can be used to do an ad hoc test of the translation rules.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36de2-182">Anrufende Nummer</span><span class="sxs-lookup"><span data-stu-id="36de2-182">Calling number</span></span></p></td>
<td><p><span data-ttu-id="36de2-183">-</span><span class="sxs-lookup"><span data-stu-id="36de2-183">N/A</span></span></p></td>
<td><p><span data-ttu-id="36de2-184">Gibt an, dass die zu testende Telefonnummer die Telefonnummer des Anrufers ist.</span><span class="sxs-lookup"><span data-stu-id="36de2-184">Indicates that the phone number to test is the phone number of the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36de2-185">Angerufene Nummer</span><span class="sxs-lookup"><span data-stu-id="36de2-185">Called number</span></span></p></td>
<td><p><span data-ttu-id="36de2-186">-</span><span class="sxs-lookup"><span data-stu-id="36de2-186">N/A</span></span></p></td>
<td><p><span data-ttu-id="36de2-187">Gibt an, dass die zu testende Telefonnummer die Telefonnummer der Person ist, die angerufen wird.</span><span class="sxs-lookup"><span data-stu-id="36de2-187">Indicates that the phone number to test is the phone number of the person being called.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="36de2-188">Die lync Server CsTrunkConfiguration-Cmdlets unterstützen zusätzliche Eigenschaften, die in der lync Server-Systemsteuerung nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="36de2-188">The Lync Server CsTrunkConfiguration cmdlets support additional properties not shown in Lync Server Control Panel.</span></span> <span data-ttu-id="36de2-189">Weitere Informationen finden Sie im Hilfethema zum Cmdlet <A href="https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration">New-CsTrunkConfiguration</A> .</span><span class="sxs-lookup"><span data-stu-id="36de2-189">For more information, see the help topic for the <A href="https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration">New-CsTrunkConfiguration</A> cmdlet.</span></span>



</div>

<div>

## <a name="to-create-new-trunk-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="36de2-190">So erstellen Sie neue trunk-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="36de2-190">To create new trunk configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="36de2-191">Klicken Sie in der lync Server-Systemsteuerung auf **VoIP-Routing**, und klicken Sie dann auf **trunk-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="36de2-191">In Lync Server Control Panel, click **Voice Routing**, and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="36de2-192">Klicken Sie auf der Registerkarte **Trunkkonfiguration** auf **Neu** und dann auf **Standorttrunk**, um die neuen Einstellungen für den Standortbereich zu erstellen, oder klicken Sie auf **Pooltrunk**, um die neuen Einstellungen für den Dienstbereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36de2-192">On the **Trunk Configuration** tab, click **New**, and then click **Site trunk** to create the new settings at the site scope, or **Pool trunk** to create the new settings at the service scope.</span></span>

3.  <span data-ttu-id="36de2-p113">Wählen Sie im Dialogfeld **Standort auswählen** oder im Dialogfeld **Dienst auswählen** (das angezeigte Dialogfeld ist abhängig davon, ob Sie Einstellungen für den Standort- oder den Dienstbereich vornehmen) den Standort für die neuen Konfigurationseinstellungen aus und klicken Sie auf **OK**. Wenn das Dialogfeld leer ist, können Sie keine neuen Einstellungen erstellen. Wenn beispielsweise das Dialogfeld **Standort auswählen** leer ist, bedeutet dies, dass allen Standorten bereits eine Sammlung von Trunkkonfigurationsstandorten zugewiesen wurde. An jedem Standort (und in jedem Dienst) kann jedoch nur eine solche Sammlung gehostet werden. In diesem Fall können Sie die bestehende Sammlung löschen und eine neue erstellen oder Sie können die bestehende Sammlung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="36de2-p113">In the **Select a Site** or the **Select a Service** dialog box (the dialog box that appears will depend on whether you are creating site-scoped or service-scoped settings) select the location for the new configuration settings and then click **OK**. If the dialog box is blank, that means there is no place to create the new settings; for example, if the **Select a Site** dialog box is blank that means that all of your sites have already been assigned a collection of trunk configuration sites, and each site (and each service) can only host one such collection. In that case, you can either delete the existing collection and create a new collection, or simply modify the existing collection.</span></span>

4.  <span data-ttu-id="36de2-196">Nehmen Sie im Dialogfeld **Neue Trunkkonfiguration** die gewünschten Einstellungen vor und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="36de2-196">In the **New Trunk Configuration** dialog, make the appropriate selections and then click **OK**.</span></span>

5.  <span data-ttu-id="36de2-p114">Die Eigenschaft **State** für die Sammlung wird als **Commit nicht ausgeführt** angezeigt. Um die Änderungen zu übernehmen und die Sammlung zu löschen, klicken Sie auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**.</span><span class="sxs-lookup"><span data-stu-id="36de2-p114">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

6.  <span data-ttu-id="36de2-199">Klicken Sie im Dialogfeld **VoIP-Konfigurationseinstellungen, für die kein Commit ausgeführt wurde** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="36de2-199">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

7.  <span data-ttu-id="36de2-200">Klicken Sie im Dialogfeld **Microsoft lync Server 2013-System** Steuerung auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="36de2-200">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

<span data-ttu-id="36de2-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36de2-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

