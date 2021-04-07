---
title: 'Lync Server 2013: Einrichten eines Lync-Partnerverbunds'
description: 'Lync Server 2013: Einrichten des Lync-Verbunds.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395067"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a><span data-ttu-id="37fd4-103">Einrichten eines Lync-Partnerverbunds in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37fd4-103">Setting up Lync federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37fd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37fd4-104">

<span> </span></span></span>

<span data-ttu-id="37fd4-105">_**Thema Zuletzt geändert:** 27.03.2014_</span><span class="sxs-lookup"><span data-stu-id="37fd4-105">_**Topic Last Modified:** 2014-03-27_</span></span>

<span data-ttu-id="37fd4-106">Wenn Sie Sie bereits edgeserver oder -server bereitgestellt haben, wird das Hinzufügen der Features für Verbundszenarien sofort ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-106">If you have already deployed you Edge server or servers, adding the federated scenarios features is straight forward.</span></span> <span data-ttu-id="37fd4-107">Wenn Sie keine Edgeserver eingerichtet haben, müssen Sie dies zuerst tun.</span><span class="sxs-lookup"><span data-stu-id="37fd4-107">If you have not set up Edge Servers, you must do that first.</span></span> <span data-ttu-id="37fd4-108">Ausführliche Informationen finden Sie unter Planen des Externen [Benutzerzugriffs in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in der Planungsdokumentation und Bereitstellen des externen Benutzerzugriffs in Lync Server [2013](lync-server-2013-deploying-external-user-access.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="37fd4-108">For details, see: [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation and [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in the Deployment documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="37fd4-109">Wenn Sie eine beliebige Kombination aus XMPP-Verbund, Lync-Verbund oder öffentlicher Chatverbindung einrichten möchten, können Sie diese gleichzeitig oder gleichzeitig bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="37fd4-109">If you intend to setup any combination of XMPP federation, Lync Federation, or public instant messaging connectivity, you can deploy them concurrently or one at a time.</span></span> <span data-ttu-id="37fd4-110">Wenn Sie die Optionen über den Topologie-Generator und die Lync Server-Verwaltungsshell konfigurieren und dann den Bereitstellungs-Assistenten auf dem Edgeserver ausführen, nachdem Sie die Optionen für einen, zwei oder alle drei Verbundtypen konfiguriert haben, können Sie die Anzahl der erforderlichen Schritte verringern.</span><span class="sxs-lookup"><span data-stu-id="37fd4-110">If you configure the options through the Topology Builder and the Lync Server Management shell, then run the Deployment Wizard at the Edge server after configuring the options for one, two or all three federation types, you can reduce the number of steps required.</span></span>



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a><span data-ttu-id="37fd4-111">Einrichten des Lync-Verbunds im Topologie-Generator und im Bereitstellungs-Assistenten</span><span class="sxs-lookup"><span data-stu-id="37fd4-111">Setting Up Lync Federation in Topology Builder and the Deployment Wizard</span></span>

1.  <span data-ttu-id="37fd4-112">Öffnen Sie auf einem Front -End-Server den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="37fd4-112">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="37fd4-113">Erweitern Sie Edgepools, und klicken Sie dann mit der rechten Maustaste auf Ihren Edgeserver oder Edgeserverpool.</span><span class="sxs-lookup"><span data-stu-id="37fd4-113">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="37fd4-114">Wählen Sie Eigenschaften bearbeiten aus.</span><span class="sxs-lookup"><span data-stu-id="37fd4-114">Select Edit properties.</span></span>

2.  <span data-ttu-id="37fd4-115">Wählen Sie unter Eigenschaften bearbeiten unter Allgemein die Option Verbund für diesen Edgepool aktivieren (Port 5061) aus.</span><span class="sxs-lookup"><span data-stu-id="37fd4-115">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="37fd4-116">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="37fd4-116">Click OK.</span></span>

3.  <span data-ttu-id="37fd4-117">Klicken Sie auf Aktion, wählen Sie Topologie und dann Veröffentlichen aus.</span><span class="sxs-lookup"><span data-stu-id="37fd4-117">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="37fd4-118">Wenn Sie unter Topologie veröffentlichen aufgefordert werden, klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="37fd4-118">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="37fd4-119">Wenn die Veröffentlichung abgeschlossen ist, klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="37fd4-119">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="37fd4-120">Öffnen Sie auf dem Edgeserver den Lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="37fd4-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="37fd4-121">Klicken Sie auf Installieren oder Aktualisieren von Lync Server System, und klicken Sie dann auf Einrichten oder Entfernen von Lync Server-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="37fd4-121">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="37fd4-122">Klicken Sie auf Erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="37fd4-122">Click Run Again.</span></span>

5.  <span data-ttu-id="37fd4-123">Klicken Sie bei Setup von Lync Server-Komponenten auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="37fd4-123">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="37fd4-124">Im Zusammenfassungsbildschirm werden Aktionen angezeigt, während sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37fd4-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="37fd4-125">Nachdem die Bereitstellung erfolgt ist, klicken Sie auf Protokoll anzeigen, um die verfügbaren Protokolldateien anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="37fd4-125">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="37fd4-126">Klicken Sie auf Fertig stellen, um die Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="37fd4-126">Click Finish to complete the deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="37fd4-127">Sie können diese Option auswählen, aber nur ein Edgepool oder Edgeserver in Ihrer Organisation kann extern für den Verbund veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="37fd4-127">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="37fd4-128">Alle Zugriffe von Verbundbenutzern, einschließlich Der Benutzer von öffentlichen Chatnachrichten, werden über denselben Edgepool oder einen einzelnen Edgeserver ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-128">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="37fd4-129">Wenn Ihre Bereitstellung z. B. einen Edgepool oder einen einzelnen Edgeserver enthält, der in New York bereitgestellt wurde, und ein in London bereitgestellter Server und Sie die Verbundunterstützung für den New York Edge-Pool oder einen einzelnen Edgeserver aktivieren, wird der Signalverkehr für Verbundbenutzer über den New York Edge-Pool oder einen einzelnen Edgeserver ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-129">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="37fd4-130">Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.</span><span class="sxs-lookup"><span data-stu-id="37fd4-130">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a><span data-ttu-id="37fd4-131">Konfigurieren des Verbunds mit Partnern</span><span class="sxs-lookup"><span data-stu-id="37fd4-131">Configuring Federation with Partners</span></span>

1.  <span data-ttu-id="37fd4-132">Wenn Sie einen erfolgreichen Verbund mit einem anderen Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 oder Office Communicator 2007 einrichten möchten, wählen Sie den Typ des Verbunds aus der folgenden Tabelle aus, definieren DNS SRV-Einträge, DNS-Host (A oder AAAA für IPv6) und konfigurieren Richtlinien, die für den Typ des Verbunds gelten:</span><span class="sxs-lookup"><span data-stu-id="37fd4-132">To setup a successful federation with another Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2, or Office Communicator 2007, select the type of federation from the following table and define DNS SRV records, DNS host (A or AAAA for IPv6) and configure policies applicable to the type of federation:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="37fd4-133">Verbundtyp</span><span class="sxs-lookup"><span data-stu-id="37fd4-133">Federation type</span></span></th>
    <th><span data-ttu-id="37fd4-134">DNS Records</span><span class="sxs-lookup"><span data-stu-id="37fd4-134">DNS Records</span></span></th>
    <th><span data-ttu-id="37fd4-135">Richtliniendefinition</span><span class="sxs-lookup"><span data-stu-id="37fd4-135">Policy Definition</span></span></th>
    <th><span data-ttu-id="37fd4-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37fd4-136">Notes</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="37fd4-137">Ermittelte Partnerdomäne</span><span class="sxs-lookup"><span data-stu-id="37fd4-137">Discovered Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="37fd4-138">Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne Wenn der Portwert für den SRV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="37fd4-138">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="37fd4-139">&lt;Name der externen &gt; Domäne – der FQDN Ihres Access Edge-Diensts.</span><span class="sxs-lookup"><span data-stu-id="37fd4-139">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="37fd4-140">Details zum Erstellen des SRV-Eintrags finden Sie unter Konfigurieren von DNS für Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-140">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="37fd4-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-141"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="37fd4-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Aktivieren oder Deaktivieren der Suche von Verbundpartnern in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-142"><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Enable or disable discovery of federation partners in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="37fd4-143">Frühere Versionen haben diesen Verbundtyp als <strong>Erweiterter Verbund öffnen bezeichnet.</strong></span><span class="sxs-lookup"><span data-stu-id="37fd4-143">Previous versions referred to this type of federation as <strong>Open Enhanced Federation</strong>.</span></span> <span data-ttu-id="37fd4-144">Die Erstellung des SRV-Eintrags ist für diesen Verbundtyp erforderlich und soll es anderen Partnern ermöglichen, Ihren Verbund zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="37fd4-144">The creation of the SRV record is required for this type of federation and is to allow other partners to discover your federation.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="37fd4-145">Zulässige Partnerdomäne</span><span class="sxs-lookup"><span data-stu-id="37fd4-145">Allowed Partner Domain</span></span></p></td>
    <td><p><span data-ttu-id="37fd4-146">Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne Wenn der Portwert für den SRV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="37fd4-146">Configure SRV record of the format _sipfederationtls._tcp.&lt;external domain name&gt;Where the port value for the SRV record is TCP 5061 and the <strong>Host offering this service</strong> is defined as sip.</span></span> <span data-ttu-id="37fd4-147">&lt;Name der externen &gt; Domäne – der FQDN Ihres Access Edge-Diensts.</span><span class="sxs-lookup"><span data-stu-id="37fd4-147">&lt;external domain name&gt; – the FQDN of your Access Edge service.</span></span> <span data-ttu-id="37fd4-148">Details zum Erstellen des SRV-Eintrags finden Sie unter Konfigurieren von DNS für Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-148">See <a href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</a> for details on creating the SRV record</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="37fd4-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-149"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="37fd4-150">Frühere Versionen bezeichneten diesen Verbundtyp als <strong>Erweiterter Verbund</strong>.</span><span class="sxs-lookup"><span data-stu-id="37fd4-150">Previous versions referred to this type of federation as <strong>Enhanced Federation</strong>.</span></span> <span data-ttu-id="37fd4-151">Die Erstellung des SRV-Eintrags ist für diese Art von Verbund optional und soll es anderen Partnern ermöglichen, Ihren Verbund zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="37fd4-151">The creation of the SRV record is optional for this type of federation and is to allow other partners to discover your federation.</span></span> <span data-ttu-id="37fd4-152">Natürlich handelt es sich dann um einen <strong>erweiterten Open Federation</strong>oder <strong>eine "Discovered Partner Domain".</strong></span><span class="sxs-lookup"><span data-stu-id="37fd4-152">Of course, this is then an <strong>Open Enhanced Federation</strong>, or <strong>Discovered Partner Domain</strong></span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="37fd4-153">Zulässiger Partnerserver</span><span class="sxs-lookup"><span data-stu-id="37fd4-153">Allowed Partner Server</span></span></p></td>
    <td><p><span data-ttu-id="37fd4-154">Konfigurieren des SIP-Domänennamens und des Partner Edge Server FQDNs als Verbundpartner in Richtlinien</span><span class="sxs-lookup"><span data-stu-id="37fd4-154">Configure the SIP domain name and the partner Edge Server FQDN as a federation partner in Policies</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="37fd4-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-155"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="37fd4-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Konfigurieren der Unterstützung für zulässige externe Domänen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-156"><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Configure support for allowed external domains in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="37fd4-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Konfigurieren der Unterstützung für blockierte externe Domänen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-157"><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Configure support for blocked external domains in Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="37fd4-158">Dieser Verbundtyp ist die Definition einer 1:1-Beziehung und ermöglicht keine Suche nach anderen Partnerverbundpartnern.</span><span class="sxs-lookup"><span data-stu-id="37fd4-158">This federation type is the definition of a one to one relationship and does not allow for discovery of other federation partners.</span></span> <span data-ttu-id="37fd4-159">Jeder Partnerverbund ist explizit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="37fd4-159">Each federation partner is configured explicitly.</span></span> <span data-ttu-id="37fd4-160">In früheren Versionen wurde dies als <strong>"Direkter Verbund"</strong></span><span class="sxs-lookup"><span data-stu-id="37fd4-160">In previous versions, this was known as <strong>Direct Federation</strong></span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="37fd4-161">Hostinganbieter und öffentlicher IM-Anbieter</span><span class="sxs-lookup"><span data-stu-id="37fd4-161">Hosting Provider and Public IM Provider</span></span></p></td>
    <td><p><span data-ttu-id="37fd4-162">Für diesen Verbundtyp sind keine speziellen DNS-Anforderungen definiert.</span><span class="sxs-lookup"><span data-stu-id="37fd4-162">No specific DNS requirements are defined for this type of federation</span></span></p></td>
    <td><ul>
    <li><p><span data-ttu-id="37fd4-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-163"><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Enable or disable federation and public IM connectivity in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="37fd4-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Erstellen oder Bearbeiten von öffentlichen SIP-Partnerverbundanbietern in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-164"><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Create or edit public SIP federated providers in Lync Server 2013</a></span></span></p></li>
    <li><p><span data-ttu-id="37fd4-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Erstellen oder Bearbeiten von gehosteten SIP-Verbundanbietern in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="37fd4-165"><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Create or edit hosted SIP federated providers Lync Server 2013</a></span></span></p></li>
    </ul></td>
    <td><p><span data-ttu-id="37fd4-166">Dieser Verbundtyp definiert Dienste und Hostinganbieter, die Sie für Ihre Benutzer konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="37fd4-166">This federation type defines services and hosting providers that you want to configure for your users.</span></span> <span data-ttu-id="37fd4-167">Typische Verwendungsmöglichkeiten sind die Konfiguration für öffentliche Windows Live Messenger, Yahoo!</span><span class="sxs-lookup"><span data-stu-id="37fd4-167">Typical uses include configuration for public IM providers like Windows Live Messenger, Yahoo!</span></span> <span data-ttu-id="37fd4-168">und AOL sowie Hostinganbieter wie Lync Online und Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="37fd4-168">and AOL, as well as hosting providers such as Lync Online and Microsoft 365</span></span></p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="37fd4-169">Seit dem 1. September 2012 steht die Microsoft Lync Public IM Connectivity User Subscription License ("PIC USL") für neue oder verlängernde Verträge nicht mehr zum Kauf zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="37fd4-169">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="37fd4-170">Kunden mit aktiven Lizenzen können weiterhin eine Zusammenarbeit mit Yahoo!</span><span class="sxs-lookup"><span data-stu-id="37fd4-170">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="37fd4-171">Messenger bis zum Herunterfahren des Diensts.</span><span class="sxs-lookup"><span data-stu-id="37fd4-171">Messenger until the service shut down date.</span></span> <span data-ttu-id="37fd4-172">Ende des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="37fd4-172">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="37fd4-173">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-173">has been announced.</span></span> <span data-ttu-id="37fd4-174">Details finden Sie unter <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support für die Konnektivität mit öffentlichen Chatnachrichten in Lync Server 2013.</A></span><span class="sxs-lookup"><span data-stu-id="37fd4-174">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="37fd4-175">Die PIC USL ist eine Abonnementlizenz pro Benutzer pro Monat, die erforderlich ist, damit Lync Server oder Office Communications Server mit Yahoo! zusammenarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="37fd4-175">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="37fd4-176">Messenger.</span><span class="sxs-lookup"><span data-stu-id="37fd4-176">Messenger.</span></span> <span data-ttu-id="37fd4-177">Die Fähigkeit von Microsoft, diesen Dienst zur Verfügung zu stellen, hängt von der Unterstützung von Yahoo! ab, der zugrunde liegenden Vereinbarung, für die der Vertrag geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="37fd4-177">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="37fd4-178">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Einzelpersonen auf der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-178">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="37fd4-179">Der Verbund mit Windows Live Messenger erfordert keine zusätzlichen Benutzer-/Gerätelizenzen über die Lync Standard CAL hinaus.</span><span class="sxs-lookup"><span data-stu-id="37fd4-179">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="37fd4-180">Der Skype-Verbund wird dieser Liste hinzugefügt, sodass Lync-Benutzer Hunderte von Millionen von Personen mit Chat und Sprache erreichen können.</span><span class="sxs-lookup"><span data-stu-id="37fd4-180">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  <span data-ttu-id="37fd4-181">Definieren und Konfigurieren der erforderlichen DNS-Host-Einträge (A oder AAAA für IPv6) und DNS SRV-Einträge</span><span class="sxs-lookup"><span data-stu-id="37fd4-181">Define and configure any required DNS host (A or AAAA for IPv6) and DNS SRV records</span></span>

3.  <span data-ttu-id="37fd4-182">Definieren und konfigurieren Sie alle Richtlinien mithilfe der Lync Server-Systemsteuerung oder mithilfe der Lync Server-Verwaltungsshell und der entsprechenden Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37fd4-182">Define and configure any policies using the Lync Server Control Panel or by using the Lync Server Management Shell and the appropriate cmdlets.</span></span> <span data-ttu-id="37fd4-183">Details zu den Lync Server Management Shell-Cmdlets finden Sie unter Verbund- und externe [Zugriffs-Cmdlets in Lync Server 2013.](https://docs.microsoft.com/powershell/module/skype/)</span><span class="sxs-lookup"><span data-stu-id="37fd4-183">For details on the Lync Server Management Shell cmdlets, see [Federation and external access cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="37fd4-184">Lync Room System (LRS) zeigt keine Teilnahmeschaltfläche für Besprechungen an, die von Organisatoren in Partnerpartnern von Lync gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="37fd4-184">Lync Room System (LRS) does not show join button for meetings sent by organizers in federated Lync partners.</span></span> <span data-ttu-id="37fd4-185">Damit ein Besprechungsverknüpfungslink auf LRS angezeigt wird, muss die sendende Organisation TNEF mithilfe des folgenden Cmdlets aktivieren:</span><span class="sxs-lookup"><span data-stu-id="37fd4-185">For a meeting join link to appear on LRS, the sending organization must enable TNEF by using the following cmdlet:</span></span><BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR><span data-ttu-id="37fd4-186">Beachten Sie, dass dies nicht LRS-spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="37fd4-186">Note that this is not LRS specific.</span></span> <span data-ttu-id="37fd4-187">Outlook und Lync würden in diesem Fall auch keine Verknüpfungen für die Teilnahme anzeigen, da die MAPI-Eigenschaften nicht transportiert werden, aber im Fall von Outlook kann der Benutzer die Besprechungs-Einladung öffnen und auf die Besprechungs-URL klicken.</span><span class="sxs-lookup"><span data-stu-id="37fd4-187">Outlook and Lync would also not show Join links in this case as MAPI properties are not transported, but in the Outlook case, the user can open up the meeting invite and click on the meeting URL.</span></span> <span data-ttu-id="37fd4-188">Wenn TNEFEnabled auf true festgelegt ist Exchange 2013 entfernt keine MAPI-Eigenschaften, einschließlich OnlineMeetingExternalLink, und die Schaltfläche Beitreten wird in der Erinnerung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37fd4-188">When TNEFEnabled is set to true Exchange 2013 does not strip MAPI properties including OnlineMeetingExternalLink and the Join button will be shown on the reminder.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="37fd4-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fd4-189">See Also</span></span>


[<span data-ttu-id="37fd4-190">Planen von SIP, XMPP-Verbund und öffentlichem Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37fd4-190">Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[<span data-ttu-id="37fd4-191">Verwalten von Partnerverbünden und externem Zugriff auf Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37fd4-191">Managing federation and external access to Lync Server 2013</span></span>](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

<span data-ttu-id="37fd4-192"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37fd4-192"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

