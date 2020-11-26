---
title: 'Lync Server 2013: Übersicht über die Anrufsteuerung'
description: 'Lync Server 2013: Übersicht über die Anrufsteuerung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of call admission control
ms:assetid: 6fda0195-4c89-4dea-82e8-624f03e3d062
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398529(v=OCS.15)
ms:contentKeyID: 48184474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0fe2fc75ea9bc887709b7dbe1c2128513fcff6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424775"
---
# <a name="overview-of-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="ac07c-103">Übersicht über die Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac07c-103">Overview of call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac07c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac07c-104">

<span> </span></span></span>

<span data-ttu-id="ac07c-105">_**Letztes Änderungsdatum des Themas:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="ac07c-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="ac07c-106">Echtzeitkommunikation ist sensibel für Latenz-und Paketverluste, die in überlasteten Netzwerken auftreten können.</span><span class="sxs-lookup"><span data-stu-id="ac07c-106">Real-time communications are sensitive to the latency and packet loss that can occur on congested networks.</span></span> <span data-ttu-id="ac07c-107">Der Anrufsteuerungsdienst ermittelt anhand der verfügbaren Netzwerkbandbreite, ob Kommunikationssitzungen (beispielsweise Sprach- oder Videoanrufe) in Echtzeit eingerichtet werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-107">Call admission control (CAC) determines, based on available network bandwidth, whether to allow real-time communications sessions such as voice or video calls to be established.</span></span> <span data-ttu-id="ac07c-108">Das CAC-Design in lync Server 2013 bietet vier Hauptattribute:</span><span class="sxs-lookup"><span data-stu-id="ac07c-108">The CAC design in Lync Server 2013 offers four main attributes:</span></span>

  - <span data-ttu-id="ac07c-109">Sie lässt sich problemlos bereitstellen und verwalten, ohne dass zusätzliche Geräte (z. B. speziell konfigurierte Router) erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ac07c-109">It is simple to deploy and manage without requiring additional equipment, such as specially configured routers.</span></span>

  - <span data-ttu-id="ac07c-p102">Sie eignet sich für wichtige Unified Communications-Anwendungsfälle, z. B. für Roamingbenutzer und für die Anmeldung auf mehreren Geräten. Anrufsteuerungsrichtlinien werden nicht abhängig davon erzwungen, wo der Benutzer verwaltet wird, sondern basierend auf dem Standort des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="ac07c-p102">It addresses critical unified communications use cases, such as roaming users and multiple points of presence. CAC policies are enforced according to where the endpoint is located, not where the user is homed.</span></span>

  - <span data-ttu-id="ac07c-112">Zusätzlich zu VoIP-Anrufen kann die Anrufsteuerung auf andere Typen von Datenverkehr angewendet werden, z. B. auf Videoanrufe und Audio/Video-Konferenzsitzungen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-112">In addition to voice calls, it can be applied to other traffic, such as video calls and audio/video conferencing sessions.</span></span>

  - <span data-ttu-id="ac07c-113">Dies bietet die Flexibilität, verschiedene Arten von Netzwerktopologien darstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac07c-113">Provides the flexibility to enable representation of various kinds of network topologies.</span></span> <span data-ttu-id="ac07c-114">Beispiele finden Sie unter [Komponenten und Topologien für CAC in lync Server 2013](lync-server-2013-components-and-topologies-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="ac07c-114">For examples, see [Components and topologies for CAC in Lync Server 2013](lync-server-2013-components-and-topologies-for-cac.md).</span></span>

<span data-ttu-id="ac07c-115">Wenn eine neue VoIP- oder Videositzung die festgelegten Bandbreiteneinschränkungen einer WAN-Leitung überschreitet, wird die Sitzung entweder blockiert oder (dies gilt nur für Telefonanrufe) an das Festnetz umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ac07c-115">If a new voice or video session exceeds the bandwidth limits that you have set on a WAN link, the session is either blocked or (for phone calls only) rerouted to the PSTN.</span></span>

<span data-ttu-id="ac07c-p104">Mit der Anrufsteuerung wird lediglich Echtzeitdatenverkehr für VoIP- und Videoanrufe gesteuert. Anderer Datenverkehr wird nicht gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ac07c-p104">CAC controls real-time traffic for voice and video only. It does not control data traffic.</span></span>

<span data-ttu-id="ac07c-118">Administratoren definieren CAC-Richtlinien, die vom bandbreitenrichtliniendienst erzwungen werden, der mit jedem Front-End-Pool installiert wird.</span><span class="sxs-lookup"><span data-stu-id="ac07c-118">Administrators define CAC policies, which are enforced by the Bandwidth Policy Service that is installed with every Front End pool.</span></span> <span data-ttu-id="ac07c-119">Die CAC-Einstellungen werden automatisch an alle lync Server-Front-End-Server in Ihrem Netzwerk weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="ac07c-119">CAC settings are automatically propagated to all Lync Server Front End Servers in your network.</span></span>

<span data-ttu-id="ac07c-120">Bei Anrufen, die aufgrund von Anrufsteuerungsrichtlinien nicht erfolgreich durchgeführt werden können, gilt folgende Reihenfolge für die Anrufumleitung:</span><span class="sxs-lookup"><span data-stu-id="ac07c-120">For calls that fail because of CAC policies, the order of precedence for rerouting the call is as follows:</span></span>

1.  <span data-ttu-id="ac07c-121">Internet</span><span class="sxs-lookup"><span data-stu-id="ac07c-121">Internet</span></span>

2.  <span data-ttu-id="ac07c-122">Telefonfestnetz (PSTN)</span><span class="sxs-lookup"><span data-stu-id="ac07c-122">PSTN</span></span>

3.  <span data-ttu-id="ac07c-123">Voicemail</span><span class="sxs-lookup"><span data-stu-id="ac07c-123">Voice mail</span></span>

<span data-ttu-id="ac07c-p106">Bei der Aufzeichnung von Kommunikationsdatensätzen werden Informationen zu Anrufen erfasst, die an das Festnetz oder an einen Voicemaildienst umgeleitet werden. Da das Internet nicht als sekundäre Option, sondern als alternativer Pfad behandelt wird, werden bei der Aufzeichnung von Kommunikationsdatensätzen keine Informationen zu Anrufen erfasst, die an das Internet umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ac07c-p106">Call detail recording (CDR) captures information about calls that are rerouted to the PSTN or to voice mail. CDR does not capture information about calls that are rerouted to the Internet, because the Internet is treated as an alternate path rather than a secondary option.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ac07c-126">Das Hinterlassen von Voicemails wird aufgrund von Bandbreitenbeschränkungen nicht abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="ac07c-126">Voice mail deposits will not be denied because of bandwidth constraints.</span></span>



</div>

<span data-ttu-id="ac07c-p107">Der Bandbreitenrichtliniendienst generiert zwei Typen von Protokolldateien im CSV-Format (durch Trennzeichen getrennte Datei). In der Protokolldatei für **Fehler bei der Überprüfung** werden Informationen erfasst, wenn Bandbreitenanforderungen abgelehnt werden. In der Protokolldatei zur **Verbindungsauslastung** werden ein Snapshot der Netzwerktopologie sowie die Bandbreitenauslastung der WAN-Verbindung erfasst. Unter Verwendung dieser beiden Protokolldateien können Sie Ihre Anrufsteuerungsrichtlinien basierend auf der Auslastung optimieren.</span><span class="sxs-lookup"><span data-stu-id="ac07c-p107">The Bandwidth Policy Service generates two types of log files in comma separated values (CSV) format. The **check failures** log file captures information when bandwidth requests are denied. The **link utilization** log file captures a snapshot of the network topology and the WAN link bandwidth utilization. Both of these log files can assist you in fine-tuning your CAC policies based on utilization.</span></span>

<div>

## <a name="call-admission-control-considerations"></a><span data-ttu-id="ac07c-131">Überlegungen zur Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="ac07c-131">Call Admission Control Considerations</span></span>

<span data-ttu-id="ac07c-132">Der Administrator wählt aus, dass der Bandbreitenrichtliniendienst auf dem ersten Pool am zentralen Standort konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ac07c-132">The administrator selects to install the Bandwidth Policy Service on the first pool configured in the central site.</span></span> <span data-ttu-id="ac07c-133">Da es pro Netzwerkregion einen einzelnen zentralen Standort gibt, gibt es pro Netzwerkregion auch nur einen einzigen Bandbreitenrichtliniendienst, der die Bandbreitenrichtlinien für die entsprechende Region, die zugeordneten Standorte und die Links zu diesen Standorten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ac07c-133">Since there is a single central site per network region, there is only one Bandwidth Policy Service per network region, which manages bandwidth policy for that region, its associated sites and the links to those sites.</span></span> <span data-ttu-id="ac07c-134">Der bandbreitenrichtliniendienst wird als Teil der Front-End-Server ausgeführt, und daher ist eine höhere Verfügbarkeit innerhalb dieses Pools integriert.</span><span class="sxs-lookup"><span data-stu-id="ac07c-134">The Bandwidth Policy Service runs as part of the Front End Servers, and therefore high availability is built-in within that pool.</span></span> <span data-ttu-id="ac07c-135">Der bandbreitenrichtliniendienst, der auf jedem Front-End-Server ausgeführt wird, synchronisiert alle 15 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ac07c-135">The Bandwidth Policy Service running on each Front End Server synchronizes every 15 seconds.</span></span> <span data-ttu-id="ac07c-136">Wenn der Front-End-Pool ausfällt, werden die CAC-Richtlinien für diese Website erst dann erzwungen, wenn der Front-End-Pool und damit der bandbreitenrichtliniendienst wieder in Betrieb genommen wird.</span><span class="sxs-lookup"><span data-stu-id="ac07c-136">If the Front End pool fails, CAC policies are no longer enforced for that site until the Front End pool and consequently the Bandwidth Policy Service becomes operational again.</span></span> <span data-ttu-id="ac07c-137">Das bedeutet, dass während der Zeit, in der der Bandbreitenrichtliniendienst ausfällt, alle Anrufe durchgehen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-137">This implies that all calls will go through for the duration the Bandwidth Policy Service is out of service.</span></span> <span data-ttu-id="ac07c-138">Aus diesem Grund besteht in diesem Zeitraum die Möglichkeit einer zu hohen Bandbreitenbelegung Ihrer Links.</span><span class="sxs-lookup"><span data-stu-id="ac07c-138">Therefore there is the possibility of bandwidth oversubscription of your links during this period</span></span>

<span data-ttu-id="ac07c-139">Der bandbreitenrichtliniendienst bietet eine große Verfügbarkeit innerhalb eines Front-End-Pools. Es bietet jedoch keine Redundanz über Front-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="ac07c-139">The Bandwidth Policy Service provides high availability within a Front End pool; however, it does not provide redundancy across Front End pools.</span></span> <span data-ttu-id="ac07c-140">Der bandbreitenrichtliniendienst kann nicht von einem Front-End-Pool zu einem anderen Failover.</span><span class="sxs-lookup"><span data-stu-id="ac07c-140">The Bandwidth Policy Service cannot failover from one Front End pool to another.</span></span> <span data-ttu-id="ac07c-141">Nachdem der Service für den Front-End-Pool wiederhergestellt wurde, wird der bandbreitenrichtliniendienst fortgesetzt und kann die Überprüfung der Bandbreitenrichtlinien erneut erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-141">Once service to the Front End pool is restored, the Bandwidth Policy Service is resumed and can enforce bandwidth policy checks again.</span></span>

<div>

## <a name="network-considerations"></a><span data-ttu-id="ac07c-142">Überlegungen zum Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ac07c-142">Network Considerations</span></span>

<span data-ttu-id="ac07c-143">Obwohl die Bandbreitenbeschränkung für Audio und Video vom bandbreitenrichtliniendienst in lync Server 2013 erzwungen wird, wird diese Einschränkung beim Netzwerkrouter nicht erzwungen (Layer 2 und 3).</span><span class="sxs-lookup"><span data-stu-id="ac07c-143">Although bandwidth restriction for audio and video is enforced by the Bandwidth Policy Service in Lync Server 2013, this restriction is not enforced at the network router (layer 2 and 3).</span></span> <span data-ttu-id="ac07c-144">Lync Server 2010 CAC kann eine Daten Anwendung beispielsweise nicht daran hindern, die gesamte Netzwerkbandbreite einer WAN-Verbindung zu nutzen, einschließlich der Bandbreite, die von ihrer CAC-Richtlinie für Audio und Video reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="ac07c-144">Lync Server 2010 CAC cannot prevent a data application, for example, from consuming the entire network bandwidth on a WAN link, including the bandwidth that is reserved for audio and video by your CAC policy.</span></span> <span data-ttu-id="ac07c-145">Um sicherzustellen, dass die erforderliche Bandbreite in Ihrem Netzwerk reserviert wird, können Sie ein QoS-Protokoll (Quality of Service) wie Differenzierte Dienste (DiffServ) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-145">To protect the necessary bandwidth on your network, you can deploy a Quality of Service (QoS) protocol such as Differentiated Services (DiffServ).</span></span> <span data-ttu-id="ac07c-146">Daher empfiehlt es sich, die definierten Bandbreitenrichtlinien der Anrufsteuerung auf QoS-Einstellungen abzustimmen, die Sie gegebenenfalls bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ac07c-146">Therefore, a best practice is to coordinate the CAC bandwidth policies you define with any QoS settings that you might deploy.</span></span>

</div>

<div>

## <a name="media-and-signaling-paths-over-vpn"></a><span data-ttu-id="ac07c-147">Medien- und Signalpfade über ein VPN</span><span class="sxs-lookup"><span data-stu-id="ac07c-147">Media and Signaling Paths over VPN</span></span>

<span data-ttu-id="ac07c-p111">Wenn Ihr Unternehmen die Medienübermittlung über ein VPN unterstützt, müssen Sie sicherstellen, dass sowohl der Medien- als auch der Signaldatenstrom über das VPN verarbeitet werden bzw. beide Datenströme über das Internet geroutet werden. In der Standardeinstellung werden die Medien- und Signaldatenströme durch den VPN-Tunnel verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ac07c-p111">If your enterprise supports media through VPN, ensure that either both the media stream and the signaling stream go through the VPN or both are routed through the internet. By default, the media and signaling streams go through the VPN tunnel.</span></span>

</div>

<div>

## <a name="call-admission-control-of-outside-users"></a><span data-ttu-id="ac07c-150">Anrufsteuerung für externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="ac07c-150">Call Admission Control of Outside Users</span></span>

<span data-ttu-id="ac07c-151">Die Anrufsteuerung wird nicht für Remotebenutzer erzwungen, bei denen der Netzwerkdatenverkehr über das Internet fließt.</span><span class="sxs-lookup"><span data-stu-id="ac07c-151">Call admission control is not enforced for remote users where the network traffic flows through the Internet.</span></span> <span data-ttu-id="ac07c-152">Da der Mediendatenverkehr das Internet durchläuft, das nicht von lync Server verwaltet wird, kann CAC nicht angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac07c-152">Because the media traffic is traversing the Internet, which is not managed by Lync Server, CAC cannot be applied.</span></span> <span data-ttu-id="ac07c-153">Für den Teil des Anrufs, der über das Unternehmensnetzwerk fließt, werden jedoch CAC-Prüfungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac07c-153">CAC checks will be performed, however, on the portion of the call that flows through the enterprise network.</span></span>

</div>

<div>

## <a name="call-admission-control-of-pstn-connections"></a><span data-ttu-id="ac07c-154">Anrufsteuerung für PSTN-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="ac07c-154">Call Admission Control of PSTN Connections</span></span>

<span data-ttu-id="ac07c-155">Die Anrufsteuerung ist auf dem Vermittlungs Server unabhängig davon durchsetzbar, ob Sie mit einer IP/PBX-Anlage, einem PSTN-Gateway oder einem SIP-Trunk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ac07c-155">Call admission control is enforceable on the Mediation Server regardless of whether it is connected to an IP/PBX, a PSTN gateway, or a SIP trunk.</span></span> <span data-ttu-id="ac07c-156">Da es sich bei dem Vermittlungs Server um einen Back-to-Back-Benutzer-Agent (B2BUA) handelt, wird der Mediendienst beendet.</span><span class="sxs-lookup"><span data-stu-id="ac07c-156">Because the Mediation Server is a back-to-back user agent (B2BUA), it terminates media.</span></span> <span data-ttu-id="ac07c-157">Es hat zwei Verbindungsseiten: eine Seite, die mit dem lync-Server verbunden ist, und eine Gatewayseite, die mit PSTN-Gateways, IP/PBX-Anlagen oder SIP-Stämmen verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ac07c-157">It has two connection sides: a side that is connected to Lync Server and a gateway side, which is connected to PSTN gateways, IP/PBXs, or SIP trunks.</span></span> <span data-ttu-id="ac07c-158">Details zu PSTN-Verbindungen finden Sie unter [Planen der PSTN-Konnektivität in lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md).</span><span class="sxs-lookup"><span data-stu-id="ac07c-158">For details about PSTN connections, see [Planning for PSTN connectivity in Lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md).</span></span>

<span data-ttu-id="ac07c-159">CAC kann auf beiden Seiten des Vermittlungsservers erzwungen werden, es sei denn, die medienumgehung ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac07c-159">CAC can be enforced on both sides of the Mediation Server unless media bypass is enabled.</span></span> <span data-ttu-id="ac07c-160">Wenn die medienumgehung aktiviert ist, wird der Mediendatenverkehr nicht durch den Vermittlungs Server durchlaufen, sondern direkt zwischen dem lync-Client und dem Gateway.</span><span class="sxs-lookup"><span data-stu-id="ac07c-160">If media bypass is enabled, the media traffic doesn’t traverse the Mediation Server but instead flows directly between the Lync client and the gateway.</span></span> <span data-ttu-id="ac07c-161">In diesem Fall wird die Anrufsteuerung nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="ac07c-161">In this case, CAC is not needed.</span></span> <span data-ttu-id="ac07c-162">Ausführliche Informationen finden Sie unter [Planen der medienumgehung in lync Server 2013](lync-server-2013-planning-for-media-bypass.md).</span><span class="sxs-lookup"><span data-stu-id="ac07c-162">For details, see [Planning for media bypass in Lync Server 2013](lync-server-2013-planning-for-media-bypass.md).</span></span>

<span data-ttu-id="ac07c-163">Die folgende Abbildung zeigt, wie die Anrufsteuerung für PSTN-Verbindungen mit und ohne Medienumgehung erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="ac07c-163">The following figure illustrates how CAC is enforced on PSTN connections with and without media bypass enabled.</span></span>

<span data-ttu-id="ac07c-164">**Erzwingen der Anrufsteuerung für Verbindungen mit dem PSTN**</span><span class="sxs-lookup"><span data-stu-id="ac07c-164">**Call admission control enforcement on connections to the PSTN**</span></span>

<span data-ttu-id="ac07c-165">![Voice CAC Media Bypass-Verbindungserzwingung](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass-Verbindungserzwingung")</span><span class="sxs-lookup"><span data-stu-id="ac07c-165">![Voice CAC Media Bypass Connection Enforcement](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass Connection Enforcement")</span></span>

</div>

<div>

## <a name="compatibility-of-call-admission-control-with-earlier-versions-of-office-communications-server"></a><span data-ttu-id="ac07c-166">Kompatibilität der Anrufsteuerung mit früheren Versionen von Office Communications Server</span><span class="sxs-lookup"><span data-stu-id="ac07c-166">Compatibility of Call Admission Control with Earlier Versions of Office Communications Server</span></span>

<span data-ttu-id="ac07c-167">Die Anrufsteuerung kann nur auf Endpunkten aktiviert werden, die für lync Server 2010 und höher aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ac07c-167">Call admission control can be enabled only on endpoints that are enabled for Lync Server 2010 and later.</span></span>

<span data-ttu-id="ac07c-168">Die Anrufsteuerung kann auf Endpunkten mit Office Communicator 2007 R2 oder früheren Versionen nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ac07c-168">Call admission control cannot be enabled on endpoints running Office Communicator 2007 R2 or earlier.</span></span>

<span data-ttu-id="ac07c-169">**Anwendung von CAC in verschiedenen lync Server-Versionen**</span><span class="sxs-lookup"><span data-stu-id="ac07c-169">**Application of CAC on different Lync Server versions**</span></span>

<span data-ttu-id="ac07c-170">![Sprach-CAC-Versionsvergleichs Diagramm](images/Gg398529.fdbfee7e-15fc-445b-949d-8d61e61ac350(OCS.15).jpg "Sprach-CAC-Versionsvergleichs Diagramm")</span><span class="sxs-lookup"><span data-stu-id="ac07c-170">![Voice CAC Version Comparison diagram](images/Gg398529.fdbfee7e-15fc-445b-949d-8d61e61ac350(OCS.15).jpg "Voice CAC Version Comparison diagram")</span></span>

<span data-ttu-id="ac07c-171"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac07c-171"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

