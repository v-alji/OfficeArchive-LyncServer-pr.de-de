---
title: 'Lync Server 2013: Ermitteln von DNS-Anforderungen'
description: 'Lync Server 2013: Ermitteln der DNS-Anforderungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Determine DNS requirements
ms:assetid: 95777017-6282-44c0-a685-f246af0501b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398758(v=OCS.15)
ms:contentKeyID: 48184839
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a4bfe682314fa4f91826f4bf85f8eac36ea91d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395031"
---
# <a name="determine-dns-requirements-for-lync-server-2013"></a><span data-ttu-id="94d88-103">Ermitteln von DNS-Anforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="94d88-103">Determine DNS requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="94d88-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="94d88-104">

<span> </span></span></span>

<span data-ttu-id="94d88-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="94d88-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="94d88-106">Mithilfe des folgenden Flussdiagramms können Sie DNS-Anforderungen (Domain Name System) ermitteln.</span><span class="sxs-lookup"><span data-stu-id="94d88-106">Use the following flow chart to determine Domain Name System (DNS) requirements.</span></span> <span data-ttu-id="94d88-107">Die Änderungen für die kumulativen Updates für lync Server 2013: Februar 2013 werden an deren Anwendung notiert.</span><span class="sxs-lookup"><span data-stu-id="94d88-107">Changes for the Cumulative Updates for Lync Server 2013: February 2013 are noted where they apply.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="94d88-108">Microsoft lync Server 2013 unterstützt die Verwendung der IPv6-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="94d88-108">Microsoft Lync Server 2013 supports the use of IPv6 addressing.</span></span> <span data-ttu-id="94d88-109">Um IPv6-Adressen verwenden zu können, müssen Sie auch IPv6-DNS unterstützen und DNS-Host AAAA-Datensätze (so genannte "Quad-A") konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="94d88-109">To use IPv6 addresses, you must also provide support for IPv6 DNS and configure DNS host AAAA (known as “quad-A”) records.</span></span> <span data-ttu-id="94d88-110">In Bereitstellungen, in denen sowohl IPv4 als auch IPv6 verwendet werden, empfiehlt es sich, sowohl Host A Records für IPv4 als auch Host AAAA für IPv6 zu konfigurieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="94d88-110">In deployments where both IPv4 and IPv6 are being used, it is best to configure and maintain both host A records for IPv4 and host AAAA for IPv6.</span></span> <span data-ttu-id="94d88-111">Auch wenn Ihre Bereitstellung vollständig auf IPv6 umgestellt wurde, sind möglicherweise IPv4-DNS-Hosteinträge erforderlich, wenn externe Benutzer weiterhin IPv4 verwenden.</span><span class="sxs-lookup"><span data-stu-id="94d88-111">Even if your deployment has transitioned fully to IPv6, IPv4 DNS host records may still be required when external users are still using IPv4.</span></span>



</div>

<span data-ttu-id="94d88-112">**Ermitteln des Flussdiagramms für DNS-Anforderungen**</span><span class="sxs-lookup"><span data-stu-id="94d88-112">**Determining DNS Requirements Flow Chart**</span></span>

<span data-ttu-id="94d88-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span><span class="sxs-lookup"><span data-stu-id="94d88-113">![175782ac-363e-408a-912f-8991bf152970](images/Gg398758.175782ac-363e-408a-912f-8991bf152970(OCS.15).jpg "175782ac-363e-408a-912f-8991bf152970")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="94d88-114">Standardmäßig ist der Computername eines Computers, der nicht zu einer Domäne gehört, ein Hostname, nicht ein vollständig qualifizierter Domänenname (FQDN).</span><span class="sxs-lookup"><span data-stu-id="94d88-114">By default the computer name of a computer that is not joined to a domain is a host name, not a fully qualified domain name (FQDN).</span></span> <span data-ttu-id="94d88-115">Der Topologie-Generator verwendet FQDNs, keine Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="94d88-115">Topology Builder uses FQDNs, not host names.</span></span> <span data-ttu-id="94d88-116">Daher müssen Sie ein DNS-Suffix für den Namen des Computers konfigurieren, der als Edgeserver bereitgestellt werden soll und nicht Mitglied einer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="94d88-116">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="94d88-117"><STRONG>Verwenden Sie nur Standardzeichen</STRONG> (also A – Z, a – z, 0 – 9 und Bindestriche) beim Zuweisen von FQDNs der Server mit Lync Server, Edgeserver und Pools.</span><span class="sxs-lookup"><span data-stu-id="94d88-117"><STRONG>Use only standard characters</STRONG> (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="94d88-118">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="94d88-118">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="94d88-119">Andere als die genannten Zeichen in einem FQDN werden von externen DNS und öffentlichen Zertifizierungsstellen (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss) häufig nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94d88-119">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (that is, when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="94d88-120">Weitere Informationen finden Sie unter <A href="lync-server-2013-configure-dns-host-records.md">Konfigurieren von DNS-Host Einträgen für lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="94d88-120">For additional details, see <A href="lync-server-2013-configure-dns-host-records.md">Configure DNS Host records for Lync Server 2013</A></span></span>



</div>

<div>

## <a name="how-lync-clients-locate-services"></a><span data-ttu-id="94d88-121">Suchen nach Diensten durch lync-Clients</span><span class="sxs-lookup"><span data-stu-id="94d88-121">How Lync Clients Locate Services</span></span>

<span data-ttu-id="94d88-122">Microsoft lync 2010, lync 2013 und lync Mobile ähneln der Art und Weise, wie der Clientdienste in lync Server 2013 findet und zugreift.</span><span class="sxs-lookup"><span data-stu-id="94d88-122">Microsoft Lync 2010, Lync 2013, and Lync Mobile are similar in how the client finds and accesses services in Lync Server 2013.</span></span> <span data-ttu-id="94d88-123">Die wichtigste Ausnahme ist die lync Windows Store-App, die einen anderen Dienststandort Prozess verwendet.</span><span class="sxs-lookup"><span data-stu-id="94d88-123">The notable exception is the Lync Windows Store app that uses a different service location process.</span></span> <span data-ttu-id="94d88-124">In diesem Abschnitt werden zwei Szenarien erläutert, wie die Clients Dienste finden, zunächst die herkömmliche Methode, die eine Reihe von SRV-und a-Host Datensätzen verwendet, und zweitens nur die Datensätze des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="94d88-124">This section details two scenarios of how the clients locate services, first the traditional method using a series of SRV and A host records, second using only the Autodiscover service records.</span></span> <span data-ttu-id="94d88-125">Kumulative Updates für die Desktop Clients ändern den DNS-Standort Prozess von lync Server 2010 für alle Clients, der DNS-Abfrageprozess wird fortgesetzt, bis eine erfolgreiche Abfrage zurückgegeben wird oder die Liste der möglichen DNS-Einträge erschöpft ist, und der endgültige Fehler wird an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94d88-125">Cumulative updates to the desktop clients change the DNS location process from Lync Server 2010 For all clients, the DNS query process continues until a successful query is returned, or the list of possible DNS records is exhausted, and the final error is returned to the client.</span></span>

<span data-ttu-id="94d88-126">Für alle Clients **mit Ausnahme** der lync Windows Store-App während der DNS-Suche werden SRV-Einträge abgefragt und an den Client in der folgenden Reihenfolge zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="94d88-126">For all clients **except** for the Lync Windows Store app During DNS lookup, SRV records are queried and returned to the client in the following order:</span></span>

1.  <span data-ttu-id="94d88-127">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-127">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="94d88-128">Ein (Host)-Eintrag für den AutoErmittlungsdienst in den internen Webdiensten</span><span class="sxs-lookup"><span data-stu-id="94d88-128">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="94d88-129">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-129">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="94d88-130">Einen (Host)-Eintrag für den AutoErmittlungsdienst in den externen Webdiensten</span><span class="sxs-lookup"><span data-stu-id="94d88-130">A (host) record for the Autodiscover service on the external Web services</span></span>

3.  <span data-ttu-id="94d88-131">\_sipinternaltls. \_ TCP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-131">\_sipinternaltls.\_tcp.\<domain\></span></span>   <span data-ttu-id="94d88-132">SRV-Eintrag (Dienst Locator) für interne TLS-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="94d88-132">SRV (service locator) record for internal TLS connections</span></span>

4.  <span data-ttu-id="94d88-133">\_sipinternal. \_ TCP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-133">\_sipinternal.\_tcp.\<domain\></span></span>   <span data-ttu-id="94d88-134">SRV (Service Locator)-Eintrag für interne TCP-Verbindungen (nur ausgeführt, wenn TCP zulässig ist)</span><span class="sxs-lookup"><span data-stu-id="94d88-134">SRV (service locator) record for internal TCP connections (performed only if TCP is allowed)</span></span>

5.  <span data-ttu-id="94d88-135">\_SIP. \_ TLS.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-135">\_sip.\_tls.\<domain\></span></span>   <span data-ttu-id="94d88-136">SRV (Service Locator)-Eintrag für externe TLS-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="94d88-136">SRV (service locator) record for external TLS connections</span></span>

6.  <span data-ttu-id="94d88-137">sipinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-137">sipinternal.\<domain\></span></span>   <span data-ttu-id="94d88-138">Einen (Host-) Eintrag für den Front-End-Pool oder Director, der nur im internen Netzwerk aufgelöst werden kann</span><span class="sxs-lookup"><span data-stu-id="94d88-138">A (host) record for the Front End pool or Director, resolvable only on the internal network</span></span>

7.  <span data-ttu-id="94d88-139">sip.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-139">sip.\<domain\></span></span>   <span data-ttu-id="94d88-140">Einen (Host-) Eintrag für den Front-End-Pool oder Director im internen Netzwerk oder den Access Edge-Dienst, wenn der Client extern ist</span><span class="sxs-lookup"><span data-stu-id="94d88-140">A (host) record for the Front End pool or Director on the internal network, or the Access Edge service when the client is external</span></span>

8.  <span data-ttu-id="94d88-141">sipexternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-141">sipexternal.\<domain\></span></span>   <span data-ttu-id="94d88-142">Ein (Host)-Eintrag für den Access Edge-Dienst, wenn der Client extern ist</span><span class="sxs-lookup"><span data-stu-id="94d88-142">A (host) record for the Access Edge service when the client is external</span></span>

<span data-ttu-id="94d88-143">Die lync Windows Store-App ändert den Prozess vollständig, da zwei Datensätze verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="94d88-143">The Lync Windows Store app changes the process completely because it uses two records:</span></span>

1.  <span data-ttu-id="94d88-144">lyncdiscoverinternal.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-144">lyncdiscoverinternal.\<domain\></span></span>   <span data-ttu-id="94d88-145">Ein (Host)-Eintrag für den AutoErmittlungsdienst in den internen Webdiensten</span><span class="sxs-lookup"><span data-stu-id="94d88-145">A (host) record for the Autodiscover service on the internal Web services</span></span>

2.  <span data-ttu-id="94d88-146">lyncdiscover.\<domain\></span><span class="sxs-lookup"><span data-stu-id="94d88-146">lyncdiscover.\<domain\></span></span>   <span data-ttu-id="94d88-147">Einen (Host)-Eintrag für den AutoErmittlungsdienst in den externen Webdiensten</span><span class="sxs-lookup"><span data-stu-id="94d88-147">A (host) record for the Autodiscover service on the external Web services</span></span>

<span data-ttu-id="94d88-148">Es gibt keinen Fallback auf die anderen Datensatztypen.</span><span class="sxs-lookup"><span data-stu-id="94d88-148">There is no fallback to the other record types.</span></span>

<span data-ttu-id="94d88-149">Der Unterschied zwischen den Methoden, die für neuere Clients im Vergleich zu älteren Clients verwendet werden, besteht darin, dass der AutoErmittlungsdienst zur bevorzugten Methode zum Auffinden aller Dienste wird.</span><span class="sxs-lookup"><span data-stu-id="94d88-149">The difference between the methods used for newer clients as compared to older clients is that the Autodiscover service is becoming the preferred method to locate all services.</span></span>

<span data-ttu-id="94d88-150">Wenn eine Verbindung erfolgreich ist, gibt der AutoErmittlungsdienst alle Webdienste-URLs für den privaten Pool des Benutzers zurück, einschließlich des mobilitätsdiensts (bekannt als MCX durch das für den Dienst in IIS erstellte virtuelle Verzeichnis), Microsoft lync Web App und Web Scheduler-URLs.</span><span class="sxs-lookup"><span data-stu-id="94d88-150">When a connection is successful, the Autodiscover Service returns all the Web Services URLs for the user's home pool, including the Mobility Service (known as Mcx by the virtual directory created for the service in IIS), Microsoft Lync Web App and Web scheduler URLs.</span></span> <span data-ttu-id="94d88-151">Die URL für den internen Mobilitätsdienst und die URL für den externen Mobilitätsdienst sind jedoch mit dem FQDN der externen Webdienste verbunden.</span><span class="sxs-lookup"><span data-stu-id="94d88-151">However, both the internal Mobility Service URL and the external Mobility Service URL is associated with the external Web Services FQDN.</span></span> <span data-ttu-id="94d88-152">Unabhängig davon, ob ein mobiles Gerät intern oder extern für das Netzwerk ist, stellt das Gerät immer extern über den Reverse-Proxy eine Verbindung mit dem Mobilitätsdienst her.</span><span class="sxs-lookup"><span data-stu-id="94d88-152">Therefore, regardless of whether a mobile device is internal or external to the network, the device always connects to the Mobility Service externally through the reverse proxy.</span></span>

<span data-ttu-id="94d88-153">Wenn die kumulativen Updates für lync Server 2013: Februar 2013 installiert wurden, gibt der AutoErmittlungsdienst auch Verweise auf Internal/UCWA, External/UCWA und UCWA zurück.</span><span class="sxs-lookup"><span data-stu-id="94d88-153">If the Cumulative Updates for Lync Server 2013: February 2013 has been installed, the Autodiscover Service also returns references to Internal/UCWA, External/UCWA and UCWA.</span></span> <span data-ttu-id="94d88-154">Diese Einträge beziehen sich auf die Web-Komponente "Unified Communications Web API (UCWA)".</span><span class="sxs-lookup"><span data-stu-id="94d88-154">These entries refer to the Unified Communications Web API (UCWA) web component.</span></span> <span data-ttu-id="94d88-155">Derzeit wird nur der Eintrag UCWA verwendet, und es wird ein Verweis auf eine URL für die Webkomponente bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="94d88-155">Currently, only the entry UCWA is used and provides a reference to a URL for the web component.</span></span> <span data-ttu-id="94d88-156">UCWA wird von lync 2013-mobilen Clients anstelle des MCX-mobilitätsdiensts verwendet, der von den mobilen lync 2010-Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94d88-156">UCWA is used by Lync 2013 Mobile clients instead of the Mcx Mobility Service used by the Lync 2010 Mobile clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="94d88-157">Beim Erstellen von SRV-Einträgen ist zu beachten, dass Sie auf einen DNS-Eintrag in der gleichen Domäne verweisen müssen, in der der DNS-SRV-Eintrag erstellt wird (wenn Sie IPv6-Adressierung verwenden).</span><span class="sxs-lookup"><span data-stu-id="94d88-157">When creating SRV records, it is important to remember that they must point to a DNS A and AAAA (if you are using IPv6 addressing) record in the same domain in which the DNS SRV record is created.</span></span> <span data-ttu-id="94d88-158">Wenn sich der SRV-Eintrag beispielsweise in contoso.com befindet, wird in der a-und AAAA-Datei (bei Verwendung der IPv6-Adressierung) der Eintrag auf kann nicht in fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="94d88-158">For example, if the SRV record is in contoso.com, the A and AAAA (if you are using IPv6 addressing) record it points to cannot be in fabrikam.com.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="94d88-159">Die Standardkonfiguration besteht darin, den gesamten mobilen Client Datenverkehr über die externe Website zu leiten.</span><span class="sxs-lookup"><span data-stu-id="94d88-159">The default configuration is to direct all mobile client traffic through the external site.</span></span> <span data-ttu-id="94d88-160">Sie können Einstellungen so ändern, dass nur die interne URL zurückgegeben wird, wenn dies für Ihre Anforderungen vorzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="94d88-160">You can modify settings to return only the internal URL, if this is more preferable for your requirements.</span></span> <span data-ttu-id="94d88-161">Mit dieser Konfiguration können Benutzer lync Mobile-Anwendungen auf Ihren mobilen Geräten nur verwenden, wenn Sie sich im Unternehmensnetzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="94d88-161">With this configuration, users can use Lync mobile applications on their mobile devices only when they are inside the corporate network.</span></span> <span data-ttu-id="94d88-162">Zum Definieren dieser Konfiguration verwenden Sie das Cmdlet " <STRONG>Satz-CsMcxConfiguration</STRONG> ".</span><span class="sxs-lookup"><span data-stu-id="94d88-162">To define this configuration, you use the <STRONG>Set-CsMcxConfiguration</STRONG> cmdlet.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="94d88-163">Obwohl mobile Anwendungen auch eine Verbindung mit anderen lync Server 2013-Diensten herstellen können, wie etwa dem Adressbuchdienst, werden Webanforderungen für interne Mobile Webanwendungen nur für den Mobilitätsdienst an den externen Web-FQDN weiter verwendet.</span><span class="sxs-lookup"><span data-stu-id="94d88-163">Although mobile applications can also connect to other Lync Server 2013 services, such as Address Book Service, internal mobile application web requests go to the external web FQDN only for the Mobility Service.</span></span> <span data-ttu-id="94d88-164">Für andere Dienstanforderungen wie Adressbuch Anforderungen ist diese Konfiguration nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="94d88-164">Other service requests, such as Address Book requests, do not require this configuration.</span></span>



</div>

<span data-ttu-id="94d88-165">Mobile Geräte unterstützen die manuelle Ermittlung von Diensten.</span><span class="sxs-lookup"><span data-stu-id="94d88-165">Mobile devices support manual discovery of services.</span></span> <span data-ttu-id="94d88-166">In diesem Fall muss jeder Benutzer die Einstellungen für das Mobile Gerät mit den vollständigen internen und externen AutoErmittlungsdienst-URIs, einschließlich Protokoll und Pfad, wie folgt konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="94d88-166">In this case, each user must configure the mobile device settings with the full internal and external Autodiscover Service URIs, including the protocol and path, as follows:</span></span>

  - <span data-ttu-id="94d88-167"> https://- \<ExtPoolFQDN\> /autodiscover/autodiscoverservice.svc/root für externen Zugriff</span><span class="sxs-lookup"><span data-stu-id="94d88-167">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>

  - <span data-ttu-id="94d88-168"> https://- \<IntPoolFQDN\> /autodiscover/autodiscover.svc/root für internen Zugriff</span><span class="sxs-lookup"><span data-stu-id="94d88-168">https://\<IntPoolFQDN\>/AutoDiscover/AutoDiscover.svc/Root for internal access</span></span>

<span data-ttu-id="94d88-169">Es wird empfohlen, die automatische Ermittlung anstelle der manuellen Ermittlung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="94d88-169">We recommend that you use automatic discovery, rather than manual discovery.</span></span> <span data-ttu-id="94d88-170">Manuelle Einstellungen können jedoch bei der Behandlung von Problemen mit der mobilen Gerätekonnektivität hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="94d88-170">However, manual settings can be useful for troubleshooting mobile device connectivity issues.</span></span>

</div>

<div>

## <a name="configuring-split-brain-dns-with-lync-server"></a><span data-ttu-id="94d88-171">Konfigurieren Split-Brain DNS mit lync Server</span><span class="sxs-lookup"><span data-stu-id="94d88-171">Configuring Split-Brain DNS with Lync Server</span></span>

<span data-ttu-id="94d88-172">Das Split-Brain-DNS ist unter einer Reihe von Namen bekannt, beispielsweise Split-DNS oder Split-Horizon-DNS.</span><span class="sxs-lookup"><span data-stu-id="94d88-172">Split-brain DNS is known by a number of names, for example, split DNS or split-horizon DNS.</span></span> <span data-ttu-id="94d88-173">Sie beschreibt einfach eine DNS-Konfiguration, in der zwei DNS-Zonen mit dem gleichen Namespace vorhanden sind, aber nur interne Anforderungen für DNS-Zonen Dienste und die anderen nur für externe DNS-Zonen Dienste Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="94d88-173">Simply, it describes a DNS configuration where there are two DNS zones with the same namespace – but one DNS zone services internal-only requests, and the other DNS zone services external-only requests.</span></span> <span data-ttu-id="94d88-174">Viele der DNS-SRV-und A-Einträge, die im internen DNS enthalten sind, sind jedoch nicht im externen DNS enthalten, und umgekehrt ist auch der Fall.</span><span class="sxs-lookup"><span data-stu-id="94d88-174">However, many of the DNS SRV and A records contained in the internal DNS will not be contained in the external DNS, and the reverse is also true.</span></span> <span data-ttu-id="94d88-175">In Fällen, in denen derselbe DNS-Eintrag sowohl im internen als auch im externen DNS vorhanden ist (beispielsweise www.contoso.com), ist die zurückgegebene IP-Adresse abhängig davon, wo (intern oder extern) die Abfrage initiiert wurde, anders.</span><span class="sxs-lookup"><span data-stu-id="94d88-175">In cases where the same DNS record exists in both the internal and external DNS (for example, www.contoso.com), the IP address returned will be different based on where (internal or external) the query was initiated.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="94d88-176">Derzeit wird Split-Brain DNS für die Mobilität oder insbesondere für die DNS-Einträge LyncDiscover und LyncDiscoverInternal nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94d88-176">Currently, Split-Brain DNS is not supported for the mobility, or more specifically, the LyncDiscover and LyncDiscoverInternal DNS records.</span></span> <span data-ttu-id="94d88-177">LyncDiscover muss auf einem externen DNS-Server definiert sein, und LyncDiscoverInternal muss auf einem internen DNS-Server definiert sein.</span><span class="sxs-lookup"><span data-stu-id="94d88-177">LyncDiscover must be defined on an external DNS server and LyncDiscoverInternal must be defined on an internal DNS server.</span></span>



</div>

<span data-ttu-id="94d88-178">Für die Zwecke dieser Themen wird der Begriff "Split-Brain DNS" verwendet.</span><span class="sxs-lookup"><span data-stu-id="94d88-178">For the purposes of these topics, the term split-brain DNS will be used.</span></span>

<span data-ttu-id="94d88-179">Wenn Sie das Split-Brain-DNS konfigurieren, enthalten die folgenden internen und externen Zonen eine Zusammenfassung der Typen von DNS-Einträgen, die in den einzelnen Zonen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="94d88-179">If you are configuring split-brain DNS, the following internal and external zone contain a summary of the types of DNS records required in each zone.</span></span> <span data-ttu-id="94d88-180">Ausführliche Informationen finden Sie unter [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="94d88-180">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="94d88-181">**Interner DNS-Name:**</span><span class="sxs-lookup"><span data-stu-id="94d88-181">**Internal DNS:**</span></span>

  - <span data-ttu-id="94d88-182">Enthält eine DNS-Zone mit dem Namen "contoso.com", für die Sie autorisierend ist</span><span class="sxs-lookup"><span data-stu-id="94d88-182">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="94d88-183">Die interne contoso.com Zone enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94d88-183">The internal contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="94d88-184">DNS A und AAAA (wenn Sie die IPv6-Adressierung verwenden) und SRV-Einträge für die interne lync Server 2013-Client Autokonfiguration (optional)</span><span class="sxs-lookup"><span data-stu-id="94d88-184">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for internal Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="94d88-185">DNS A und AAAA (wenn Sie IPv6-Adressierung verwenden) oder CNAME-Einträge für die automatische Ermittlung von lync Server 2013-Webdiensten (optional)</span><span class="sxs-lookup"><span data-stu-id="94d88-185">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services (optional)</span></span>
    
      - <span data-ttu-id="94d88-186">DNS A und AAAA (wenn Sie IPv6-Adressierung verwenden) Datensätze für den Namen des Front-End-Pools, Director-oder Director-Poolname und alle internen Server, auf denen lync Server 2013 im Unternehmensnetzwerk ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="94d88-186">DNS A and AAAA (if you are using IPv6 addressing) records for Front End pool name, Director or Director pool name, and all internal servers running Lync Server 2013 in the corporate network</span></span>
    
      - <span data-ttu-id="94d88-187">DNS A und AAAA (bei Verwendung von IPv6-Adressierungs Datensätzen) für die interne Edge-Schnittstelle jedes lync Server 2013, Edgeserver im Umkreisnetzwerk</span><span class="sxs-lookup"><span data-stu-id="94d88-187">DNS A and AAAA (if you are using IPv6 addressing) records for the Edge internal interface of each Lync Server 2013, Edge Server in the perimeter network</span></span>
    
      - <span data-ttu-id="94d88-188">DNS A und AAAA (wenn Sie IPv6-Adressierung verwenden) für die interne Schnittstelle jedes Reverse-Proxyservers im Umkreisnetzwerk (optional für die Verwaltung des Reverse-Proxys)</span><span class="sxs-lookup"><span data-stu-id="94d88-188">DNS A and AAAA (if you are using IPv6 addressing) records for the internal interface of each reverse proxy server in the perimeter network (optional for management of reverse proxy)</span></span>
    
      - <span data-ttu-id="94d88-189">Alle lync Server 2013-Edgeserver-Schnittstellen im Umkreisnetzwerk verwenden die interne DNS-Zone zum Auflösen von Abfragen in contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-189">All Lync Server 2013  Edge Server internal edge interfaces in the perimeter network use the internal DNS zone for resolving queries to contoso.com</span></span>
    
      - <span data-ttu-id="94d88-190">Alle Server mit lync Server 2013 und Clients, auf denen lync 2013 im Unternehmensnetzwerk ausgeführt wird, verweisen auf die internen DNS-Server zum Auflösen von Abfragen an contoso.com oder auf die Verwendung der Hosts-Datei auf jedem Edgeserver sowie auf Listen A und AAAA (wenn Sie IPv6-Adressierung verwenden) für den Next Hop-Server, insbesondere den Director oder Director VIP, Front-End-Pool VIP oder Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="94d88-190">All servers running Lync Server 2013 and clients running Lync 2013 in the corporate network point to the internal DNS servers for resolving queries to contoso.com, or use of HOSTS file on each Edge server and list A and AAAA (if you are using IPv6 addressing) records for next hop server, specifically the Director or Director VIP, Front End pool VIP, or Standard Edition server</span></span>

<span data-ttu-id="94d88-191">**Externer DNS-Name:**</span><span class="sxs-lookup"><span data-stu-id="94d88-191">**External DNS:**</span></span>

  - <span data-ttu-id="94d88-192">Enthält eine DNS-Zone mit dem Namen "contoso.com", für die Sie autorisierend ist</span><span class="sxs-lookup"><span data-stu-id="94d88-192">Contains a DNS zone called contoso.com for which it is authoritative</span></span>

  - <span data-ttu-id="94d88-193">Die externe contoso.com Zone enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94d88-193">The external contoso.com zone contains:</span></span>
    
      - <span data-ttu-id="94d88-194">DNS A und AAAA (wenn Sie die IPv6-Adressierung verwenden) und SRV-Einträge für die Autokonfiguration des lync Server 2013-Clients (optional)</span><span class="sxs-lookup"><span data-stu-id="94d88-194">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for Lync Server 2013 client autoconfiguration (optional)</span></span>
    
      - <span data-ttu-id="94d88-195">DNS A und AAAA (wenn Sie eine IPv6-Adressierung verwenden) oder CNAME-Einträge für die automatische Erkennung von lync Server 2013-Webdiensten zur Verwendung mit Mobility</span><span class="sxs-lookup"><span data-stu-id="94d88-195">DNS A and AAAA (if you are using IPv6 addressing) or CNAME records for automatic discovery of Lync Server 2013 Web Services for use with mobility</span></span>
    
      - <span data-ttu-id="94d88-196">DNS A und AAAA (wenn Sie die IPv6-Adressierung verwenden) und SRV-Einträge für die externe Edge-Schnittstelle jeder lync Server 2013, Edgeserver oder des Hardware-Lastenausgleichsmoduls (Virtual IP (VIP)) im Umkreisnetzwerk</span><span class="sxs-lookup"><span data-stu-id="94d88-196">DNS A and AAAA (if you are using IPv6 addressing) and SRV records for the Edge external interface of each Lync Server 2013, Edge Server or hardware load balancer virtual IP (VIP) in the perimeter network</span></span>
    
      - <span data-ttu-id="94d88-197">DNS a und AAAA (wenn Sie IPv6-Adressierung verwenden) Einträge für die externe Schnittstelle des Reverse Proxyservers oder VIP für einen Pool von Reverse-Proxyservern im Umkreisnetzwerk</span><span class="sxs-lookup"><span data-stu-id="94d88-197">DNS A and AAAA (if you are using IPv6 addressing) records for the external interface of the reverse proxy server or VIP for a pool of reverse proxy servers in the perimeter network</span></span>

</div>

<div>

## <a name="automatic-configuration-without-split-brain-dns"></a><span data-ttu-id="94d88-198">Automatische Konfiguration ohne Split-Brain DNS</span><span class="sxs-lookup"><span data-stu-id="94d88-198">Automatic Configuration without Split-Brain DNS</span></span>

<span data-ttu-id="94d88-199">Bei Verwendung von Split-Brain-DNS kann ein lync Server 2013-Benutzer, der sich intern anmeldet, die automatische Konfiguration nutzen, wenn die interne DNS-Zone eine \_ sipinternaltls enthält. \_ TCP-SRV-Eintrag für jede verwendete SIP-Domäne</span><span class="sxs-lookup"><span data-stu-id="94d88-199">Using split-brain DNS, a Lync Server 2013 user that signs in internally can take advantage of automatic configuration if the internal DNS zone contains a \_sipinternaltls.\_tcp SRV record for each SIP domain in use.</span></span> <span data-ttu-id="94d88-200">Wenn Sie jedoch kein Split-Brain-DNS verwenden, funktioniert die interne automatische Konfiguration von Clients, auf denen lync ausgeführt wird, nicht, es sei denn, eine der in diesem Abschnitt weiter unten beschriebenen Problemumgehungen wird implementiert.</span><span class="sxs-lookup"><span data-stu-id="94d88-200">However, if you do not use split-brain DNS, internal automatic configuration of clients running Lync will not work unless one of the workarounds described in later in this section is implemented.</span></span> <span data-ttu-id="94d88-201">Dies liegt daran, dass für lync Server 2013 der SIP-URI des Benutzers mit der Domäne des Front-End-Pools übereinstimmt, der für die automatische Konfiguration vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="94d88-201">This is because Lync Server 2013 requires the user’s SIP URI to match the domain of the Front End pool designated for automatic configuration.</span></span> <span data-ttu-id="94d88-202">Dies war auch bei früheren Versionen von Communicator der Fall.</span><span class="sxs-lookup"><span data-stu-id="94d88-202">This was also the case with earlier versions of Communicator.</span></span>

<span data-ttu-id="94d88-203">Wenn Sie beispielsweise über zwei SIP-Domänen verfügen, müssen die folgenden DNS-Diensteinträge (SRV) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="94d88-203">For example, if you have two SIP domains in use, the following DNS service (SRV) records would be required:</span></span>

  - <span data-ttu-id="94d88-204">Wenn sich ein Benutzer als Bob@contoso.com anmeldet, funktioniert der folgende SRV-Eintrag für die automatische Konfiguration, da die SIP-Domäne (contoso.com) des Benutzers der Domäne des Front-End-Pools für die automatische Konfiguration entspricht:</span><span class="sxs-lookup"><span data-stu-id="94d88-204">If a user signs in as bob@contoso.com the following SRV record will work for automatic configuration because the user’s SIP domain (contoso.com) matches the domain of automatic configuration Front End pool):</span></span>
    
     <span data-ttu-id="94d88-205">\_sipinternaltls. \_ TCP.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="94d88-205">\_sipinternaltls.\_tcp.contoso.com.</span></span> <span data-ttu-id="94d88-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-206">86400 IN SRV 0 0 5061 pool01.contoso.com</span></span>

  - <span data-ttu-id="94d88-207">Wenn sich ein Benutzer als Alice@fabrikam.com anmeldet, funktioniert der folgende DNS-SRV-Eintrag für die automatische Konfiguration der zweiten SIP-Domäne.</span><span class="sxs-lookup"><span data-stu-id="94d88-207">If a user signs in as alice@fabrikam.com the following DNS SRV record will work for automatic configuration of the second SIP domain.</span></span>
    
     <span data-ttu-id="94d88-208">\_sipinternaltls. \_ TCP.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="94d88-208">\_sipinternaltls.\_tcp.fabrikam.com.</span></span> <span data-ttu-id="94d88-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="94d88-209">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="94d88-210">Zum Vergleich: Wenn sich ein Benutzer als Tim@litwareinc.com anmeldet, funktioniert der folgende DNS-SRV-Eintrag nicht für die automatische Konfiguration, da die SIP-Domäne (litwareinc.com) des Clients nicht der Domäne entspricht, in der sich der Pool befindet (fabrikam.com):</span><span class="sxs-lookup"><span data-stu-id="94d88-210">For comparison, if a user signs in as tim@litwareinc.com the following DNS SRV record will not work for automatic configuration, because the client’s SIP domain (litwareinc.com) does not match the domain that the pool is in (fabrikam.com):</span></span>

 <span data-ttu-id="94d88-211">\_sipinternaltls. \_ TCP.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="94d88-211">\_sipinternaltls.\_tcp.litwareinc.com.</span></span> <span data-ttu-id="94d88-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="94d88-212">86400 IN SRV 0 0 5061 pool01.fabrikam.com</span></span>

<span data-ttu-id="94d88-213">Wenn für Clients, die lync ausführen, die automatische Konfiguration erforderlich ist, wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="94d88-213">If automatic configuration is required for clients running Lync, select one of the following options:</span></span>

  - <span data-ttu-id="94d88-214">**Gruppenrichtlinienobjekte**   Verwenden Sie Gruppenrichtlinienobjekte (Group Policy Objects, GPOs), um die richtigen Server Werte aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="94d88-214">**Group Policy Objects**   Use Group Policy objects (GPOs) to populate the correct server values.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="94d88-215">Mit dieser Option wird die automatische Konfiguration nicht aktiviert, die manuelle Konfiguration wird jedoch automatisiert, sodass bei Verwendung dieses Ansatzes keine SRV-Einträge erforderlich sind, die der automatischen Konfiguration zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94d88-215">This option does not enable automatic configuration, but it does automate the process of manual configuration, so if this approach is used, the SRV records associated with automatic configuration are not required.</span></span>

    
    </div>

  - <span data-ttu-id="94d88-216">**Übereinstimmende interne Zone**   Erstellen Sie eine Zone im internen DNS, die der externen DNS-Zone entspricht (beispielsweise contoso.com), und erstellen Sie DNS a und AAAA (wenn Sie IPv6-Adressierung verwenden) Datensätze, die dem lync Server 2013-Pool entsprechen, der für die automatische Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94d88-216">**Matching internal zone**   Create a zone in the internal DNS that matches the external DNS zone (for example, contoso.com) and create DNS A and AAAA (if you are using IPv6 addressing) records corresponding to the Lync Server 2013 pool used for automatic configuration.</span></span> <span data-ttu-id="94d88-217">Wenn sich ein Benutzer beispielsweise in pool01.contoso.Net befindet, sich aber als Bob@contoso.com in lync befindet, erstellen Sie eine interne DNS-Zone namens Contoso.com, und erstellen Sie darin eine DNS-a-und AAAA-Aufzeichnung (wenn IPv6-Adressierung verwendet wird) für pool01.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="94d88-217">For example, if a user is homed on pool01.contoso.net but signs into Lync as bob@contoso.com, create an internal DNS zone called contoso.com and inside it, create a DNS A and AAAA (if IPv6 addressing is used) record for pool01.contoso.com.</span></span>

  - <span data-ttu-id="94d88-218">**Interne Pin-Punkt-Zone**   Wenn Sie eine gesamte Zone im internen DNS erstellen, ist keine Option, Sie können Pin-Point-(dedizierte) Zonen erstellen, die den SRV-Einträgen entsprechen, die für die automatische Konfiguration erforderlich sind, und diese Zonen mit dnscmd.exe auffüllen.</span><span class="sxs-lookup"><span data-stu-id="94d88-218">**Pin-point internal zone**   If you are creating an entire zone in the internal DNS is not an option, you can create pin-point (that is, dedicated) zones that correspond to the SRV records that are required for automatic configuration, and populate those zones using dnscmd.exe.</span></span> <span data-ttu-id="94d88-219">Dnscmd.exe ist erforderlich, da die DNS-Benutzeroberfläche das Erstellen von PIN-Punkt-Zonen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94d88-219">Dnscmd.exe is required because the DNS user interface does not support creation of pin-point zones.</span></span> <span data-ttu-id="94d88-220">Wenn beispielsweise die SIP-Domäne contoso.com ist und Sie über einen Front-End-Pool mit dem Namen pool01 verfügen, der zwei Front-End-Server enthält, benötigen Sie die folgenden Pin-Punkt Zonen und eine Datensätze in Ihrem internen DNS:</span><span class="sxs-lookup"><span data-stu-id="94d88-220">For example, if the SIP domain is contoso.com and you have a Front End pool called pool01 that contains two Front End Servers, you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.contoso.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.contoso.com. @ SRV 0 0 5061 pool01.contoso.com.
        dnscmd . /zoneadd pool01.contoso.com. /dsprimary
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.contoso.com. @ A 192.168.10.91 
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
    
    <span data-ttu-id="94d88-221">Wenn Ihre Umgebung eine zweite SIP-Domäne (beispielsweise fabrikam.com) enthält, benötigen Sie die folgenden Pin-Punkt Zonen und Datensätze in Ihrem internen DNS:</span><span class="sxs-lookup"><span data-stu-id="94d88-221">If your environment contains a second SIP domain (for example, fabrikam.com), you need the following pin-point zones and A records in your internal DNS:</span></span>
    
        dnscmd . /zoneadd _sipinternaltls._tcp.fabrikam.com. /dsprimary
        dnscmd . /recordadd _sipinternaltls._tcp.fabrikam.com. @ SRV 0 0 5061 pool01.fabrikam.com.
        dnscmd . /zoneadd pool01.fabrikam.com. /dsprimary
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.90
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>
        dnscmd . /recordadd pool01.fabrikam.com. @ A 192.168.10.91
        dnscmd . /recordadd pool01.contoso.com. @ AAAA <IPv6 address>

<div>


> [!NOTE]  
> <span data-ttu-id="94d88-222">Der FQDN des Front-End-Pools wird zweimal angezeigt, jedoch mit zwei unterschiedlichen IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="94d88-222">The Front End pool FQDN appears twice, but with two different IP addresses.</span></span> <span data-ttu-id="94d88-223">Dies liegt daran, dass der DNS-Lastenausgleich verwendet wird, aber wenn der Hardwarelastenausgleich verwendet wird, gibt es nur einen einzigen Front-End-Pool Eintrag.</span><span class="sxs-lookup"><span data-stu-id="94d88-223">This is because DNS load balancing is used, but if hardware load balancing is used, there would be only a single Front End pool entry.</span></span> <span data-ttu-id="94d88-224">Außerdem ändern sich die FQDN-Werte des Front-End-Pools zwischen dem contoso.com-Beispiel und dem fabrikam.com-Beispiel, aber die IP-Adressen bleiben identisch.</span><span class="sxs-lookup"><span data-stu-id="94d88-224">Also, the Front End pool FQDN values change between the contoso.com example and the fabrikam.com example, but the IP addresses remain the same.</span></span> <span data-ttu-id="94d88-225">Dies liegt daran, dass Benutzer, die sich über eine der SIP-Domänen anmelden, denselben Front-End-Pool für die automatische Konfiguration verwenden.</span><span class="sxs-lookup"><span data-stu-id="94d88-225">This is because users signing in from either SIP domain, use the same Front End pool for automatic configuration.</span></span>



</div>

<span data-ttu-id="94d88-226">Ausführliche Informationen finden Sie im DMTF-Blog Artikel "Automatische Communicator-Konfiguration und Split-Brain DNS" unter [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707) .</span><span class="sxs-lookup"><span data-stu-id="94d88-226">For details, see the DMTF blog article, "Communicator Automatic Configuration and Split-Brain DNS," at [https://go.microsoft.com/fwlink/p/?linkId=200707](https://go.microsoft.com/fwlink/p/?linkid=200707).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="94d88-227">Die Inhalte der Blogs und die zugehörige URL können ohne vorherige Ankündigung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="94d88-227">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

</div>

<div>

## <a name="configuring-the-domain-name-system-dns-for-disaster-recovery"></a><span data-ttu-id="94d88-228">Konfigurieren des DNS (Domain Name System) für die Disaster Recovery</span><span class="sxs-lookup"><span data-stu-id="94d88-228">Configuring the domain name system (DNS) for Disaster Recovery</span></span>

<span data-ttu-id="94d88-229">Um DNS so zu konfigurieren, dass der Web-Traffic von lync Server 2013 auf Ihre Disaster Recovery-und Failover-Websites umgeleitet wird, müssen Sie einen DNS-Anbieter verwenden, der GeoDNS unterstützt.</span><span class="sxs-lookup"><span data-stu-id="94d88-229">To configure DNS to redirect Lync Server 2013 Web traffic to your disaster recovery and failover sites, you must be using a DNS provider that supports GeoDNS.</span></span> <span data-ttu-id="94d88-230">Sie können Ihre DNS-Einträge für Web so einrichten, dass die Disaster Recovery unterstützt wird, damit Features, die Webdienste verwenden, weiterhin verwendet werden, auch wenn ein ganzer Front-End-Pool ausfällt.</span><span class="sxs-lookup"><span data-stu-id="94d88-230">You can set up your DNS records for Web to support disaster recovery, so that features that use Web services continue even if one entire Front End pool goes down.</span></span> <span data-ttu-id="94d88-231">Dieses Disaster Recovery-Feature unterstützt die AutoErmittlung (Lyncdiscover-URL), Besprechungen und Einwahl einfache URLs.</span><span class="sxs-lookup"><span data-stu-id="94d88-231">This disaster recovery feature supports the Autodiscover (Lyncdiscover URL), Meet and Dial-In simple URLs.</span></span>

<span data-ttu-id="94d88-232">Sie definieren und konfigurieren zusätzliche DNS-Hosteinträge (A und AAAA bei Verwendung von IPv6) für die interne und externe Auflösung von Webdiensten bei Ihrem GeoDNS-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="94d88-232">You define and configure additional DNS host (A and AAAA if using IPv6) records for internal and external resolution of Web services at your GeoDNS provider.</span></span> <span data-ttu-id="94d88-233">Bei den folgenden Details wird davon ausgegangen, dass gepaarte Pools, geografisch verteilte und GeoDNS von Ihrem Anbieter entweder mit Round-Robin-DNS unterstützt oder für die Verwendung von pool1 als primäres Gerät konfiguriert sind, und ein Failover auf Pool2 bei einem Kommunikationsverlust oder einem Hardwarefehler durchführen.</span><span class="sxs-lookup"><span data-stu-id="94d88-233">The following details assume paired pools, geographically dispersed, and GeoDNS supported by your provider with either round-robin DNS, or configured to use Pool1 as primary, and fail over to Pool2 in the event of communications loss or hardware failure.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94d88-234">GeoDNS-Eintrag (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="94d88-234">GeoDNS record (example)</span></span></th>
<th><span data-ttu-id="94d88-235">Pool Datensätze (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="94d88-235">Pool records (example)</span></span></th>
<th><span data-ttu-id="94d88-236">CNAME-Einträge (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="94d88-236">CNAME records (example)</span></span></th>
<th><span data-ttu-id="94d88-237">DNS-Einstellungen (wählen Sie eine Option aus)</span><span class="sxs-lookup"><span data-stu-id="94d88-237">DNS settings (select one option)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94d88-238">Meet-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-238">Meet-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-239">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-239">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-240">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-240">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-241">Meet.contoso.com-Alias für Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-241">Meet.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-242">Meet.contoso.com-Alias für Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-242">Meet.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-243">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-243">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-244">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-244">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d88-245">Meet-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-245">Meet-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-246">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-246">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-247">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-247">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-248">Meet.contoso.com-Alias für Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-248">Meet.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-249">Meet.contoso.com-Alias für Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-249">Meet.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-250">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-250">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-251">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-251">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d88-252">Dialin-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-252">Dialin-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-253">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-253">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-254">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-254">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-255">Dialin.contoso.com-Alias für Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-255">Dialin.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-256">Dialin.contoso.com-Alias für Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-256">Dialin.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-257">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-257">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-258">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-258">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d88-259">Dialin-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-259">Dialin-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-260">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-260">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-261">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-261">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-262">Dialin.contoso.com-Alias für Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-262">Dialin.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-263">Dialin.contoso.com-Alias für Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-263">Dialin.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-264">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-264">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-265">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-265">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d88-266">Lyncdiscoverint-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-266">Lyncdiscoverint-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-267">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-267">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-268">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-268">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-269">Lyncdiscoverinternal.contoso.com-Alias für Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-269">Lyncdiscoverinternal.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-270">Lyncdiscoverinternal.contoso.com-Alias für Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-270">Lyncdiscoverinternal.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-271">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-271">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-272">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-272">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d88-273">Lyncdiscover-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-273">Lyncdiscover-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-274">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-274">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-275">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-275">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-276">Lyncdiscover.contoso.com-Alias für Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-276">Lyncdiscover.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-277">Lyncdiscover.contoso.com-Alias für Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-277">Lyncdiscover.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-278">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-278">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-279">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-279">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94d88-280">Scheduler-int.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-280">Scheduler-int.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-281">Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-281">Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-282">Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-282">Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-283">Scheduler.contoso.com-Alias für Pool1InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-283">Scheduler.contoso.com alias to Pool1InternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-284">Scheduler.contoso.com-Alias für Pool2InternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-284">Scheduler.contoso.com alias to Pool2InternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-285">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-285">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-286">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-286">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94d88-287">Scheduler-ext.geolb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-287">Scheduler-ext.geolb.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-288">Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-288">Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-289">Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-289">Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-290">Scheduler.contoso.com-Alias für Pool1ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-290">Scheduler.contoso.com alias to Pool1ExternalWebFQDN.contoso.com</span></span></p>
<p><span data-ttu-id="94d88-291">Scheduler.contoso.com-Alias für Pool2ExternalWebFQDN.contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d88-291">Scheduler.contoso.com alias to Pool2ExternalWebFQDN.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="94d88-292">Roundrobin zwischen Pools</span><span class="sxs-lookup"><span data-stu-id="94d88-292">Round Robin between pools</span></span></p>
<p><span data-ttu-id="94d88-293">Verwenden von Primary, verbinden mit sekundärem, wenn Fehler</span><span class="sxs-lookup"><span data-stu-id="94d88-293">Use primary, connect to secondary if failure</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-load-balancing"></a><span data-ttu-id="94d88-294">DNS Load Balancing</span><span class="sxs-lookup"><span data-stu-id="94d88-294">DNS Load Balancing</span></span>

<span data-ttu-id="94d88-295">Der DNS-Lastenausgleich wird in der Regel auf Anwendungsebene implementiert.</span><span class="sxs-lookup"><span data-stu-id="94d88-295">DNS load balancing is typically implemented at the application level.</span></span> <span data-ttu-id="94d88-296">Die Anwendung (beispielsweise ein Client, auf dem lync ausgeführt wird) versucht, eine Verbindung mit einem Server in einem Pool herzustellen, indem eine Verbindung mit einer der IP-Adressen hergestellt wird, die von der DNS a-und AAAA-Daten Satz Abfrage (wenn IPv6-Adressierung verwendet wird) für den vollqualifizierten Domänennamen (FQDN) des Pools zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="94d88-296">The application (for example, a client running Lync), tries to connect to a server in a pool by connecting to one of the IP addresses returned from the DNS A and AAAA (if IPv6 addressing is used) record query for the pool fully qualified domain name (FQDN).</span></span>

<span data-ttu-id="94d88-297">Wenn beispielsweise drei Front-End-Server in einem Pool mit dem Namen pool01.contoso.com vorhanden sind, geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="94d88-297">For example, if there are three front end servers in a pool named pool01.contoso.com, the following will happen:</span></span>

  - <span data-ttu-id="94d88-298">Clients, auf denen lync Query DNS für pool01.contoso.com ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94d88-298">Clients running Lync query DNS for pool01.contoso.com.</span></span> <span data-ttu-id="94d88-299">Die Abfrage gibt drei IP-Adressen zurück und speichert Sie wie folgt (nicht unbedingt in dieser Reihenfolge):</span><span class="sxs-lookup"><span data-stu-id="94d88-299">The query returns three IP addresses and caches them as follows (not necessarily in this order):</span></span>
    
    <span data-ttu-id="94d88-300">pool01.contoso.com 192.168.10.90</span><span class="sxs-lookup"><span data-stu-id="94d88-300">pool01.contoso.com      192.168.10.90</span></span>
    
    <span data-ttu-id="94d88-301">pool01.contoso.com 192.168.10.91</span><span class="sxs-lookup"><span data-stu-id="94d88-301">pool01.contoso.com      192.168.10.91</span></span>
    
    <span data-ttu-id="94d88-302">pool01.contoso.com 192.168.10.92</span><span class="sxs-lookup"><span data-stu-id="94d88-302">pool01.contoso.com      192.168.10.92</span></span>

  - <span data-ttu-id="94d88-303">Der Client versucht, eine TCP-Verbindung (Transmission Control Protocol) mit einer der IP-Adressen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="94d88-303">The client attempts to establish a Transmission Control Protocol (TCP) connection to one of the IP addresses.</span></span> <span data-ttu-id="94d88-304">Wenn dies fehlschlägt, versucht der Client die nächste IP-Adresse im Cache.</span><span class="sxs-lookup"><span data-stu-id="94d88-304">If that fails, the client tries the next IP address in the cache.</span></span>

  - <span data-ttu-id="94d88-305">Bei erfolgreicher TCP-Verbindung handelt der Client die Verwendung von TLS zur Verbindungsherstellung mit der primären Registrierung in „pool01.contoso.com“ aus.</span><span class="sxs-lookup"><span data-stu-id="94d88-305">If the TCP connection succeeds, the client negotiates TLS to connect to the primary registrar on pool01.contoso.com.</span></span>

  - <span data-ttu-id="94d88-306">Wenn der Client alle zwischengespeicherten Einträge ohne erfolgreiche Verbindung versucht, wird der Benutzer benachrichtigt, dass zurzeit keine Server mit lync Server 2013 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="94d88-306">If the client tries all cached entries without a successful connection, the user is notified that no servers running Lync Server 2013 are available at the moment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="94d88-307">DNS-basierter Lastenausgleich unterscheidet sich von DNS-Round-Robin (DNS-RR), die sich normalerweise auf den Lastenausgleich bezieht, indem DNS eine andere Reihenfolge der IP-Adressen bereitstellt, die den Servern in einem Pool entsprechen.</span><span class="sxs-lookup"><span data-stu-id="94d88-307">DNS-based load balancing is different from DNS round robin (DNS RR) which typically refers to load balancing by relying on DNS to provide a different order of IP addresses corresponding to the servers in a pool.</span></span> <span data-ttu-id="94d88-308">In der Regel aktiviert DNS-RR nur die Lastverteilung, aktiviert aber kein Failover.</span><span class="sxs-lookup"><span data-stu-id="94d88-308">Typically DNS RR only enables load distribution, but does not enable failover.</span></span> <span data-ttu-id="94d88-309">Wenn beispielsweise die Verbindung mit der einzigen IP-Adresse, die von der DNS-Abfrage a und AAAA zurückgegeben wird (wenn Sie eine IPv6-Adressierung verwenden) fehlschlägt, schlägt die Verbindung fehl.</span><span class="sxs-lookup"><span data-stu-id="94d88-309">For example, if the connection to the one IP address returned by the DNS A and AAAA (if you are using IPv6 addressing) query fails, the connection fails.</span></span> <span data-ttu-id="94d88-310">Aus diesem Grund ist DNS Round Robin selbst weniger zuverlässig als DNS-basierter Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="94d88-310">Therefore, DNS round robin by itself is less reliable than DNS-based load balancing.</span></span> <span data-ttu-id="94d88-311">Sie können DNS Round Robin in Verbindung mit dem DNS-Lastenausgleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="94d88-311">You can use DNS round robin in conjunction with DNS load balancing.</span></span>



</div>

<span data-ttu-id="94d88-312">DNS-Lastenausgleich wird für Folgendes verwendet:</span><span class="sxs-lookup"><span data-stu-id="94d88-312">DNS load balancing is used for the following:</span></span>

  - <span data-ttu-id="94d88-313">Lastenausgleich von Server-zu-Server-SIP auf die Edgeserver</span><span class="sxs-lookup"><span data-stu-id="94d88-313">Load balancing server-to-server SIP to the Edge Servers</span></span>

  - <span data-ttu-id="94d88-314">Lastenausgleich für Unified Communications Application Services (UCAS)-Anwendungen wie automatische Konferenzzentrale, Reaktionsgruppe und Anruf Park</span><span class="sxs-lookup"><span data-stu-id="94d88-314">Load balancing Unified Communications Application Services (UCAS) applications such as Conferencing Auto Attendant, Response Group, and Call Park</span></span>

  - <span data-ttu-id="94d88-315">Verhindern neuer Verbindungen zu UCAS-Anwendungen (auch bekannt als "Draining")</span><span class="sxs-lookup"><span data-stu-id="94d88-315">Preventing new connections to UCAS applications (also known as "draining")</span></span>

  - <span data-ttu-id="94d88-316">Lastenausgleich für den gesamten Client-zu-Server-Datenverkehr zwischen Clients und Edgeserver</span><span class="sxs-lookup"><span data-stu-id="94d88-316">Load balancing all client-to-server traffic between clients and Edge Servers</span></span>

<span data-ttu-id="94d88-317">Der DNS-Lastenausgleich kann für Folgendes nicht verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="94d88-317">DNS load balancing cannot be used for the following:</span></span>

  - <span data-ttu-id="94d88-318">Client-zu-Server-Webverkehr an Director-oder Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="94d88-318">Client-to-server web traffic to Director or Front End Servers</span></span>

<span data-ttu-id="94d88-319">DNS-Load-Balancing und Federated-Traffic:</span><span class="sxs-lookup"><span data-stu-id="94d88-319">DNS load balancing and federated traffic:</span></span>

<span data-ttu-id="94d88-320">Wenn mehrere DNS-Einträge von einer DNS-SRV-Abfrage zurückgegeben werden, wählt der Access-Edgedienst immer den DNS-SRV-Eintrag mit der niedrigsten numerischen Priorität und dem höchsten numerischen Gewicht aus.</span><span class="sxs-lookup"><span data-stu-id="94d88-320">If multiple DNS records are returned by a DNS SRV query, the Access Edge service always picks the DNS SRV record with the lowest numeric priority and highest numeric weight.</span></span> <span data-ttu-id="94d88-321">Das Internet Engineering Task Force-Dokument "ein DNS-Eintrag für die Angabe des Standorts von Diensten (DNS SRV)" <http://www.ietf.org/rfc/rfc2782.txt> gibt an, dass, wenn mehrere DNS-SRV-Einträge definiert sind, Priorität zuerst verwendet wird, und dann Gewicht.</span><span class="sxs-lookup"><span data-stu-id="94d88-321">The Internet Engineering Task Force document “A DNS RR for specifying the location of services (DNS SRV)” <http://www.ietf.org/rfc/rfc2782.txt> specifies that if there are multiple DNS SRV records defined, priority is first used, then weight.</span></span> <span data-ttu-id="94d88-322">DNS-SRV-Eintrag a hat beispielsweise eine Gewichtung von 20 und eine Priorität von 40 und DNS-SRV-Eintrag B hat eine Gewichtung von 10 und eine Priorität von 50.</span><span class="sxs-lookup"><span data-stu-id="94d88-322">For example DNS SRV record A has a weight of 20 and a priority of 40 and DNS SRV record B has a weight of 10 and priority of 50.</span></span> <span data-ttu-id="94d88-323">DNS-SRV-Eintrag A mit Priorität 40 wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="94d88-323">DNS SRV record A with priority 40 will be selected.</span></span> <span data-ttu-id="94d88-324">Für die Auswahl des DNS-SRV-Eintrags gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="94d88-324">The following rules apply to DNS SRV record selection:</span></span>

  - <span data-ttu-id="94d88-325">Priorität wird zuerst berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="94d88-325">Priority is considered first.</span></span> <span data-ttu-id="94d88-326">Ein Client muss versuchen, den vom DNS-SRV-Eintrag definierten Ziel Host mit der niedrigsten nummerierten Priorität zu kontaktieren, die er erreichen kann.</span><span class="sxs-lookup"><span data-stu-id="94d88-326">A client MUST attempt to contact the target host defined by the DNS SRV record with the lowest numbered priority it can reach.</span></span> <span data-ttu-id="94d88-327">Ziele mit der gleichen Priorität sollten in einer Reihenfolge ausprobiert werden, die durch das gewichtungsfeld definiert ist.</span><span class="sxs-lookup"><span data-stu-id="94d88-327">Targets with the same priority SHOULD be tried in an order defined by the weight field.</span></span>

  - <span data-ttu-id="94d88-328">Das Feld "Gewichtung" gibt eine relative Gewichtung für Einträge mit der gleichen Priorität an.</span><span class="sxs-lookup"><span data-stu-id="94d88-328">The weight field specifies a relative weight for entries with the same priority.</span></span> <span data-ttu-id="94d88-329">Bei größeren gewichten sollte eine proportional höhere Wahrscheinlichkeit für die Auswahl angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94d88-329">Larger weights SHOULD be given a proportionately higher probability of being selected.</span></span> <span data-ttu-id="94d88-330">DNS-Administratoren sollten Weight 0 verwenden, wenn keine Serverauswahl vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="94d88-330">DNS administrators SHOULD use Weight 0 when there isn’t any server selection to do.</span></span> <span data-ttu-id="94d88-331">In Anwesenheit von Datensätzen mit einer Gewichtung von mehr als 0 sollten Datensätze mit der Gewichtung 0 eine sehr geringe Wahrscheinlichkeit haben, ausgewählt zu werden.</span><span class="sxs-lookup"><span data-stu-id="94d88-331">In the presence of records containing weights greater than 0, records with weight 0 should have a very small chance of being selected.</span></span>

<span data-ttu-id="94d88-332">Wenn mehrere DNS-SRV-Einträge mit gleicher Priorität und Gewichtung zurückgegeben werden, wählt der Access-Edgedienst den SRV-Eintrag aus, der zuerst vom DNS-Server empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="94d88-332">If multiple DNS SRV records with equal priority and weight are returned, the Access Edge service will select the SRV record that was received first from the DNS server.</span></span>

<span data-ttu-id="94d88-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="94d88-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

