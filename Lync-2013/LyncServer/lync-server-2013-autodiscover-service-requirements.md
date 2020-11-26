---
title: 'Lync Server 2013: Anforderungen für den AutoErmittlungsdienst'
description: 'Lync Server 2013: Dienstanforderungen für Auto Ermittlungsdienste.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Autodiscover service requirements
ms:assetid: 0ac5dbf7-9acd-4d25-b21a-932022b8b983
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690012(v=OCS.15)
ms:contentKeyID: 48183368
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 61e963bc9e921cc0a571f63d4be50f09d237c2dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438127"
---
# <a name="autodiscover-service-requirements-for-lync-server-2013"></a><span data-ttu-id="a6632-103">Anforderungen für den AutoErmittlungsdienst für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6632-103">Autodiscover service requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6632-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6632-104">

<span> </span></span></span>

<span data-ttu-id="a6632-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="a6632-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="a6632-106">Der Microsoft lync Server 2013-AutoErmittlungsdienst wird auf den Director-und Front-End-Pool Servern ausgeführt und kann bei Veröffentlichung in DNS von mobilen Geräten, auf denen lync Mobile ausgeführt wird, verwendet werden, um Mobilitätsdienste zu finden.</span><span class="sxs-lookup"><span data-stu-id="a6632-106">The Microsoft Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by mobile devices running Lync Mobile to locate mobility services.</span></span> <span data-ttu-id="a6632-107">Bevor Mobile Geräte, auf denen lync Mobile ausgeführt wird, die automatische Ermittlung nutzen können, müssen Sie die Listen für alternative Namen für Zertifikats Subjekte auf jedem Director-und Front-End-Server ändern, auf dem der AutoErmittlungsdienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6632-107">Before mobile devices running Lync Mobile can take advantage of automatic discovery, you need to modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="a6632-108">Darüber hinaus ist es möglicherweise erforderlich, die Listen Betreff alternativer Name auf Zertifikaten zu ändern, die für externe Webdienst Veröffentlichungsregeln für umgekehrte Proxys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6632-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="a6632-109">Details zu den Einträgen des alternativen betreffs, die für Directors, Front-End-Server und Reverse-Proxies erforderlich sind, finden Sie unter [Technische Voraussetzungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md) bei der Planung für Mobilität.</span><span class="sxs-lookup"><span data-stu-id="a6632-109">For details about the subject alternative name entries that are required for Directors, Front End Servers, and reverse proxies, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md) in Planning for Mobility.</span></span>

<span data-ttu-id="a6632-110">Die Entscheidung über die Verwendung von Listen für alternative namens Subjekte in umgekehrten Proxys basiert darauf, ob Sie den AutoErmittlungsdienst auf Port 80 oder auf Port 443 veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="a6632-110">The decision about using subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="a6632-111">**Veröffentlicht auf Port 80**   Wenn die ursprüngliche Abfrage des AutoErmittlungsdiensts über Port 80 erfolgt, sind keine Zertifikat Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a6632-111">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="a6632-112">Dies liegt daran, dass Mobile Geräte, auf denen lync ausgeführt wird, auf den Reverse-Proxy auf Port 80 extern zugreifen und dann intern auf Port 8080 an einen Director oder Front-End-Server umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6632-112">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be redirected to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="a6632-113">Ausführliche Informationen finden Sie weiter unten in diesem Thema im Abschnitt "ursprünglicher Auto Ermittlungsprozess mit Port 80".</span><span class="sxs-lookup"><span data-stu-id="a6632-113">For details, see the “Initial Autodiscover Process Using Port 80” section later in this topic.</span></span>

  - <span data-ttu-id="a6632-114">**Veröffentlicht auf Port 443**   Die Liste Subject Alternative Name für Zertifikate, die von der externen Webdienste-Veröffentlichungsregel verwendet werden, muss eine *lyncdiscover enthalten. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="a6632-114">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="a6632-115">Eintrag für jede SIP-Domäne innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="a6632-115">entry for each SIP domain within your organization.</span></span>

<span data-ttu-id="a6632-116">Das erneute Ausstellen von Zertifikaten unter Verwendung einer internen Zertifizierungsstelle ist in der Regel ein einfacher Vorgang, für öffentliche Zertifikate, die für die Veröffentlichungsregel des Webdiensts verwendet werden, kann das Hinzufügen mehrerer Alternativen Betreff-Namen zu kostspielig werden</span><span class="sxs-lookup"><span data-stu-id="a6632-116">Reissuing certificates using an internal certificate authority is typically a simple process but for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="a6632-117">Um dieses Problem zu umgehen, unterstützen wir die anfängliche automatische Ermittlungs Verbindung über Port 80, die dann auf Port 8080 auf dem Director-oder Front-End-Server umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a6632-117">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<span data-ttu-id="a6632-118">Nehmen wir beispielsweise an, dass ein mobiler Client, auf dem lync Mobile ausgeführt wird, für die Anmeldung bei lync Server 2013 mit dem automatischen Ermittlungs Feature unter Verwendung von http für die ursprüngliche Anforderung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="a6632-118">For example, assume that a mobile client running Lync Mobile is configured to sign in to Lync Server 2013 using the automatic discovery feature using HTTP for the initial request.</span></span>

<div>

## <a name="initial-autodiscover-process-for-mobile-devices-using-port-80"></a><span data-ttu-id="a6632-119">Erster Auto Ermittlungsprozess für mobile Geräte mit Port 80</span><span class="sxs-lookup"><span data-stu-id="a6632-119">Initial Autodiscover Process for Mobile Devices Using Port 80</span></span>

1.  <span data-ttu-id="a6632-120">Mobiles Gerät mit lync Mobile sucht lyncdiscover.contoso.com mithilfe von DNS, wobei ein A-Eintrag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a6632-120">Mobile device running Lync Mobile looks up lyncdiscover.contoso.com using DNS, where an A record exists.</span></span>

2.  <span data-ttu-id="a6632-121">Externer DNS gibt die IP-Adresse für die externen Webdienste an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="a6632-121">External DNS returns the IP address for the external web services to the client.</span></span>

3.  <span data-ttu-id="a6632-122">Mobiles Gerät mit lync Mobile sendet eine Anforderung http://lyncdiscover.contoso.com?sipuri=lyncUser1@contoso.com an den Reverse-Proxy</span><span class="sxs-lookup"><span data-stu-id="a6632-122">Mobile device running Lync Mobile sends request http://lyncdiscover.contoso.com?sipuri=lyncUser1@contoso.com to the reverse proxy</span></span>

4.  <span data-ttu-id="a6632-123">Die Webveröffentlichungsregel überbrückt die Anforderung von Port 80 extern zu Port 8080 intern, wodurch Sie an einen Director oder Front-End-Server weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a6632-123">The web publishing rule will bridge the request from port 80 externally to port 8080 internally, which will then route it to either a Director or Front End Server.</span></span>
    
    <span data-ttu-id="a6632-124">Da es sich bei der Anforderung um http und nicht um HTTPS handelt, sind keine Änderungen an dem Zertifikat in der Veröffentlichungsregel für externe Web Services erforderlich, um den AutoErmittlungsdienst zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a6632-124">Since the request is HTTP and not HTTPS, no modifications are needed to the certificate on the external web service publishing rule to support the Autodiscover Service.</span></span>

5.  <span data-ttu-id="a6632-125">Der AutoErmittlungsdienst gibt die URLs des externen Webdiensts (im HTTPS-Format) zurück.</span><span class="sxs-lookup"><span data-stu-id="a6632-125">The Autodiscover Service returns the external web service URLs (in HTTPS format).</span></span>

6.  <span data-ttu-id="a6632-126">Das Mobile Gerät mit lync Mobile kann dann erneut eine Verbindung mit dem Reverse Proxy auf Port 443 herstellen und wird über 4443 an den Mobilitätsdienst weitergeleitet, der im Home-Pool des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6632-126">The mobile device running Lync Mobile can then reconnect to the reverse proxy on port 443 and is redirected over 4443 to the mobility service running on the user’s home pool.</span></span>
    
    <span data-ttu-id="a6632-127">Da es sich bei der HTTPS-Abfrage um die URL des externen Webdiensts und die AutoErmittlungsdienst-URL handelt, ist Sie erfolgreich, da das Zertifikat bereits Einträge für alternative Namen für externe Webdienste enthält, die vollständig qualifizierte Domänennamen (FQDNs) sind.</span><span class="sxs-lookup"><span data-stu-id="a6632-127">Since the HTTPS query is to the external web services URL vs. the Autodiscover Service URL, it succeeds because the certificate will already contain subject alternative name entries for the external web services fully qualified domain names (FQDNs).</span></span>
    
    <span data-ttu-id="a6632-128">In diesem Szenario sind keine Zertifikat Änderungen erforderlich, um die Mobilität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a6632-128">In this scenario, there are no certificate changes required to support mobility.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a6632-129">Wenn der Zielwebserver über ein Zertifikat verfügt, das keinen übereinstimmenden Wert für "lyncdiscover.contoso.com" als "Subject Alternative Name"-Listenwert aufweist:</span><span class="sxs-lookup"><span data-stu-id="a6632-129">If the target web server has a certificate that does not have a matching value for lyncdiscover.contoso.com as a subject alternative name list value:</span></span><BR><span data-ttu-id="a6632-130">a. &nbsp; &nbsp; &nbsp; Web Server antwortet mit einem "Server Hello" und ohne Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a6632-130">a.&nbsp;&nbsp;&nbsp;Web server responds with a “Server Hello” and no certificate.</span></span><BR><span data-ttu-id="a6632-131">b. &nbsp; &nbsp; &nbsp; Mobiles Gerät, auf dem lync Mobile ausgeführt wird, beendet die Sitzung sofort.</span><span class="sxs-lookup"><span data-stu-id="a6632-131">b.&nbsp;&nbsp;&nbsp;Mobile device running Lync Mobile immediately terminates the session.</span></span><BR><span data-ttu-id="a6632-132">Wenn der Zielwebserver über ein Zertifikat verfügt, das lyncdiscover.contoso.com als Namen Listenwert für Subjekt Alternativen enthält:</span><span class="sxs-lookup"><span data-stu-id="a6632-132">If the target web server has a certificate that includes lyncdiscover.contoso.com as a subject alternative name list value:</span></span><BR><span data-ttu-id="a6632-133">a. &nbsp; &nbsp; &nbsp; Web Server antwortet mit einem "Server Hello" und einem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a6632-133">a.&nbsp;&nbsp;&nbsp;Web server responds with a “Server hello” and a certificate.</span></span><BR><span data-ttu-id="a6632-134">b. &nbsp; &nbsp; &nbsp; Mobiles Gerät, auf dem lync Mobile ausgeführt wird, überprüft das Zertifikat und schließt den Handshake ab.</span><span class="sxs-lookup"><span data-stu-id="a6632-134">b.&nbsp;&nbsp;&nbsp;Mobile device running Lync Mobile validates the certificate and completes the handshake.</span></span>

    
    </div>

<span data-ttu-id="a6632-135">Wenn Sie eine anfängliche Verbindung mit dem AutoErmittlungsdienst mithilfe von Port 80 auf dem Reverse-Proxy Server unterstützen möchten, können Sie eine HTTP-Veröffentlichungsregel ähnlich wie in diesem Beispiel für eine Forefront Threat Management Gateway 2010 Reverse Proxy Web-Veröffentlichungsregel erstellen:</span><span class="sxs-lookup"><span data-stu-id="a6632-135">To support an initial connection to the Autodiscover Service using port 80 on your reverse proxy server, you can create an http publishing rule similar to this example for a Forefront Threat Management Gateway 2010 reverse proxy web publishing rule:</span></span>

1.  <span data-ttu-id="a6632-136">Erstellen Sie eine neue Webveröffentlichungsregel (beispielsweise die **lync Server-AutoErmittlung (http)**).</span><span class="sxs-lookup"><span data-stu-id="a6632-136">Create a new web publishing rule (for example, **Lync Server Autodiscover (HTTP)**).</span></span>

2.  <span data-ttu-id="a6632-137">Geben Sie in **Öffentlicher Name** lyncdiscover.contoso.com ein.</span><span class="sxs-lookup"><span data-stu-id="a6632-137">In **Public Name**, enter lyncdiscover.contoso.com.</span></span>

3.  <span data-ttu-id="a6632-138">Wählen Sie auf der Registerkarte **Bridging** nur die Option aus, um Anforderungen von Port 80 auf Port 8080 zu überbrücken.</span><span class="sxs-lookup"><span data-stu-id="a6632-138">On the **Bridging** tab, select only the option to bridge requests from Port 80 to Port 8080.</span></span>

4.  <span data-ttu-id="a6632-139">Wählen Sie auf der Registerkarte **Authentifizierung** die Option **keine Authentifizierung** aus, und der **Client kann sich nicht direkt authentifizieren**.</span><span class="sxs-lookup"><span data-stu-id="a6632-139">On the **Authentication** tab, select **No authentication**, and **Client cannot authenticate directly**.</span></span>

5.  <span data-ttu-id="a6632-140">Übernehmen Sie Änderungen, und verschieben Sie die Regel an den Anfang der Liste der lync-Regeln (zunächst in der Verarbeitungsreihenfolge).</span><span class="sxs-lookup"><span data-stu-id="a6632-140">Commit changes, and move the rule to the top of the list of Lync rules (first in processing order).</span></span>

</div>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="a6632-141">Mobilität für die Bereitstellung von geteilten Domänen</span><span class="sxs-lookup"><span data-stu-id="a6632-141">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="a6632-142">Ein freigegebener SIP-Adressraum, auch bekannt als " *Split-Domain*" oder eine *hybridbereitstellung* , ist eine Konfiguration, in der Benutzer über eine lokale Bereitstellung und eine Online Umgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a6632-142">A shared SIP address space, also known as a *split-domain*, or a *hybrid deployment* is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="a6632-143">Das gewünschte Ergebnis besteht darin, dass Sie einen Benutzer haben, unabhängig davon, wo sich der Home-Server befindet (lokal oder Online), um sich bei der Bereitstellung anzumelden und an den Standort Ihres Home-Servers weitergeleitet zu werden.</span><span class="sxs-lookup"><span data-stu-id="a6632-143">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), to log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="a6632-144">Um dies zu erreichen, wird das Feature AutoErmittlung von Microsoft lync Server 2013 verwendet, um den Online Benutzer zur Online Topologie umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="a6632-144">To accomplish this, the Autodiscover feature of Microsoft Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="a6632-145">Dies erfolgt durch die Konfiguration des Uniform Resource Locator (URL) für die AutoErmittlung mithilfe der lync Server-Verwaltungsshell und der Cmdlets **Get-CsHostingProvider** und **CsHostingProvider**.</span><span class="sxs-lookup"><span data-stu-id="a6632-145">This is done by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell and the cmdlets **Get-CsHostingProvider** and **Set-CsHostingProvider**.</span></span>

<span data-ttu-id="a6632-146">Sie müssen die folgenden bereitgestellten Attribute sammeln und aufzeichnen:</span><span class="sxs-lookup"><span data-stu-id="a6632-146">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="a6632-147">Geben Sie in der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="a6632-147">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="a6632-148">Suchen Sie in den Ergebnissen den Onlineanbieter mit dem Attribut **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="a6632-148">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="a6632-149">Beispiel: sipfed.online.lync.com</span><span class="sxs-lookup"><span data-stu-id="a6632-149">For example, sipfed.online.lync.com</span></span>

  - <span data-ttu-id="a6632-150">Aufzeichnen des Werts des ProxyFQDN</span><span class="sxs-lookup"><span data-stu-id="a6632-150">Record the value of the ProxyFQDN</span></span>

  - <span data-ttu-id="a6632-151">Aktivieren der Föderation in der lokalen lync Server-Systemsteuerung, wodurch die Föderation mit dem Onlineanbieter zugelassen wird</span><span class="sxs-lookup"><span data-stu-id="a6632-151">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider</span></span>

  - <span data-ttu-id="a6632-152">Aktivieren Sie den Verbund für den Onlineanbieter.</span><span class="sxs-lookup"><span data-stu-id="a6632-152">Enable federation for the online provider.</span></span> <span data-ttu-id="a6632-153">Standardmäßig sind alle Online Benutzer für den Domänen Verbund aktiviert und können mit allen Domänen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a6632-153">By default, all online users are enabled for domain federation and can communicate with all domains</span></span>

  - <span data-ttu-id="a6632-154">Wenn Sie blockierte und zulässige Domänen definieren, ermitteln Sie die Domänen, die explizit zugelassen oder explizit blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="a6632-154">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block</span></span>

  - <span data-ttu-id="a6632-155">Für die Online-Föderation müssen Sie Firewall-Ausnahmen, Zertifikate und DNS-Host (A oder AAAA, wenn Sie IPv6 verwenden) planen.</span><span class="sxs-lookup"><span data-stu-id="a6632-155">For online federation, you must plan for firewall exceptions, certificates and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="a6632-156">Darüber hinaus müssen Sie Verbund Richtlinien konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a6632-156">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="a6632-157">Ausführliche Informationen finden Sie unter [Planen von lync Server 2013 und Office Communications Server Federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md) .</span><span class="sxs-lookup"><span data-stu-id="a6632-157">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md)</span></span>

<span data-ttu-id="a6632-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6632-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

