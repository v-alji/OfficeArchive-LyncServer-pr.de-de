---
title: 'Lync Server 2013: Ändern der Webdienste-URL'
description: 'Lync Server 2013: Ändern der Webdienste-URL'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change the Web Services URL
ms:assetid: 4cee37c0-3b99-4207-997f-bf4229d760c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520992(v=OCS.15)
ms:contentKeyID: 48184063
ms.date: 11/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78a7a9b70d475aa952a43d215a8e5cd2068911e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435155"
---
# <a name="change-the-web-services-url-in-lync-server-2013"></a><span data-ttu-id="98f3f-103">Ändern der Webdienste-URL in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98f3f-103">Change the Web Services URL in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98f3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98f3f-104">

<span> </span></span></span>

<span data-ttu-id="98f3f-105">_**Letztes Änderungsdatum des Themas:** 2015-11-16_</span><span class="sxs-lookup"><span data-stu-id="98f3f-105">_**Topic Last Modified:** 2015-11-16_</span></span>

<span data-ttu-id="98f3f-106">Wenn Sie Ihre Front-End-Pools und Standard Edition-Server einrichten, haben Sie die Möglichkeit, einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) und zugeordnete Ports für eine externe Webfarm zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="98f3f-106">When you set up your Front End pools and Standard Edition servers, you have the option to configure an external Web farm fully qualified domain name (FQDN) and associated ports.</span></span> <span data-ttu-id="98f3f-107">Wenn Sie diese URL beim Ausführen des lync Server-Bereitstellungs-Assistenten nicht konfiguriert haben, müssen Sie diese Einstellungen manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="98f3f-107">If you did not configure this URL when you ran the Lync Server Deployment Wizard, you need to manually configure these settings.</span></span> <span data-ttu-id="98f3f-108">Ein Administrator muss diese Einstellungen in der Regel nicht ändern, da es sich hierbei um die empfohlenen und Standardanschlüsse handelt.</span><span class="sxs-lookup"><span data-stu-id="98f3f-108">An administrator typically does not need to modify these settings, as these are the recommended and default ports.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="98f3f-109">Der folgende Screenshot wurde beim Konfigurieren eines Standard Edition-Servers ausgeführt, sodass die Option "FQDN überschreiben" deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="98f3f-109">The following screen shot was taken while configuring a Standard Edition server, so the Override FQDN option is disabled.</span></span> <span data-ttu-id="98f3f-110">Diese Option ist bei der Konfiguration eines Enterprise Edition-Servers in einem Front-End-Pool aktiviert.</span><span class="sxs-lookup"><span data-stu-id="98f3f-110">That option is enabled when configuring an Enterprise Edition server in a Front End pool.</span></span>



</div>

<span data-ttu-id="98f3f-111">![Bearbeiten von Webdienste-Pool Einstellungen](images/Gg520992.fbdf5cc9-479a-463f-bb1d-53575ecdfc9d(OCS.15).jpg "Bearbeiten von Webdienste-Pool Einstellungen")</span><span class="sxs-lookup"><span data-stu-id="98f3f-111">![Edit Web Services Pool Settings](images/Gg520992.fbdf5cc9-479a-463f-bb1d-53575ecdfc9d(OCS.15).jpg "Edit Web Services Pool Settings")</span></span>

<div>

## <a name="to-configure-web-services"></a><span data-ttu-id="98f3f-112">So konfigurieren Sie Webdienste</span><span class="sxs-lookup"><span data-stu-id="98f3f-112">To configure web services</span></span>

1.  <span data-ttu-id="98f3f-113">Melden Sie sich auf dem Computer, auf dem der Topologie-Generator installiert ist, als Mitglied der Gruppe "Domänen-Admins" oder "RTCUniversalServerAdmins" an.</span><span class="sxs-lookup"><span data-stu-id="98f3f-113">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="98f3f-114">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="98f3f-114">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

3.  <span data-ttu-id="98f3f-115">Wählen Sie im Topologie-Generator in der Konsolenstruktur unter **Standard Edition-Front-End-Server**, **Enterprise Edition-Front-End-Pools** und **Verzeichnis Pools** den Namen des Pools aus.</span><span class="sxs-lookup"><span data-stu-id="98f3f-115">In Topology Builder, in the console tree under **Standard Edition Front End Servers**, **Enterprise Edition Front End pools**, and **Directory pools**, select the pool name.</span></span> <span data-ttu-id="98f3f-116">Klicken Sie mit der rechten Maustaste auf den Namen, klicken Sie auf **Eigenschaften bearbeiten**, und klicken Sie dann auf **Webdienste**.</span><span class="sxs-lookup"><span data-stu-id="98f3f-116">Right-click the name, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="98f3f-117">Fügen Sie den **FQDN der externen Webdienste** hinzu, oder bearbeiten Sie ihn, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="98f3f-117">Add or edit the **External Web Services FQDN**, and then click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="98f3f-118">Wenn Sie über mehr als einen Front-End-Pool oder Front-End-Server verfügen, muss der FQDN der externen Webdienste eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-118">If you have more than one Front End pool or Front End Server the external Web services FQDN must be unique.</span></span> <span data-ttu-id="98f3f-119">Wenn Sie beispielsweise den FQDN eines externen Webdiensts eines Front-End-Servers als <STRONG>pool01.contoso.com</STRONG>definieren, können Sie <STRONG>pool01.contoso.com</STRONG> nicht für einen anderen Front-End-Pool oder Front-End-Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="98f3f-119">For example, if you define the external Web services FQDN of a Front End Server as <STRONG>pool01.contoso.com</STRONG>, you cannot use <STRONG>pool01.contoso.com</STRONG> for another Front End pool or Front End Server.</span></span> <span data-ttu-id="98f3f-120">Wenn Sie Directors auch bereitstellen, müssen die für Director-oder Director-Pools definierten externen Webdienst-FQDN für jeden anderen Director-oder Director-Pool sowie für jeden Front-End-Pool oder Front-End-Server eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-120">If you are also deploying Directors, the external Web services FQDN defined for any Director or Director pool must be unique from any other Director or Director pool as well as any Front End pool or Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="98f3f-121">Überprüfen Sie, ob die Überwachungs-und Veröffentlichungs Anschlüsse für Ihre Umgebung ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="98f3f-121">Verify the listening and published ports are configured correctly for your environment.</span></span>

6.  <span data-ttu-id="98f3f-122">Wiederholen Sie diese Schritte für alle Standard Edition-Server, Front-End-Pools und Director-Pools in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="98f3f-122">Repeat these steps for all Standard Edition servers, Front End Pools, and Director pools in your environment.</span></span>

7.  <span data-ttu-id="98f3f-123">Klicken Sie in der Konsolenstruktur auf **lync Server 2013**, und klicken Sie dann im Bereich **Aktionen** auf **Topologie veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="98f3f-123">In the console tree, click **Lync Server 2013**, and then, in the **Actions** pane, click **Publish Topology**.</span></span>

<span data-ttu-id="98f3f-124">Wenn Sie die Überwachungs-und Veröffentlichungs Anschlüsse konfigurieren möchten, müssen Sie einige Anforderungen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="98f3f-124">There are a few requirements you should be aware of when configuring the Listening and Publishing ports:</span></span>

  - <span data-ttu-id="98f3f-125">Die angezeigten Ports sind die Ports, die auf jedem Front-End-Server für Internet Information Server (IIS) konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="98f3f-125">The listening ports shown are the ports that are configured for Internet Information Server (IIS) on each Front End Server.</span></span>

  - <span data-ttu-id="98f3f-126">Die internen und externen Überwachungsanschlüsse müssen für IIS unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-126">The internal and external listening ports must be different for IIS.</span></span> <span data-ttu-id="98f3f-127">Bei den externen Überwachungs Anschlüssen sind diese normalerweise identisch, da Sie den Hardwarelastenausgleich für den internen Webverkehr darstellen und einer der Reverse-Proxy Server für externen Webverkehr darstellt.</span><span class="sxs-lookup"><span data-stu-id="98f3f-127">For the external listening ports, these are typically the same because one represents the hardware load balancer for internal web traffic and one represents the reverse proxy server for external web traffic.</span></span>

  - <span data-ttu-id="98f3f-128">Sie können die internen Webdienste in einem Front-End-Pool, einem Director oder einem Director-Pool außer Kraft setzen und ihren eigenen FQDN definieren.</span><span class="sxs-lookup"><span data-stu-id="98f3f-128">You can override the Internal web services on a Front End pool, Director or a Director pool and define your own FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="98f3f-129">Wenn Sie sich entscheiden, die internen Webdienste mit einem selbst definierten FQDN zu überschreiben, muss jeder FQDN für jeden anderen Front-End-Pool, Director oder Director-Pool eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-129">If you decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

  - <span data-ttu-id="98f3f-130">Die veröffentlichten Ports müssen auf dem Reverse Proxy oder Hardware Load Balancer als Abhör Anschlüsse konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-130">The published ports must be configured on the reverse proxy or hardware load balancer as listening ports.</span></span>

  - <span data-ttu-id="98f3f-131">Bei einem Front-End-Pool (nicht im Beispiel dargestellt) muss sich der FQDN des internen SIP-Pools vom internen Webdienst-FQDN unterscheiden, da Webdatenverkehr über das Hardwarelastenausgleich-Modul erfolgt und der interne SIP-Pool-Datenverkehr über das DNS Load Balancer erfolgt.</span><span class="sxs-lookup"><span data-stu-id="98f3f-131">For an Front End pool (not shown in the example), the internal SIP pool FQDN must be different from the internal web services FQDN, because web traffic comes through the hardware load balancer and the internal SIP pool traffic travels comes through the DNS load balancer.</span></span> <span data-ttu-id="98f3f-132">Diese Anforderung muss erfüllt sein.</span><span class="sxs-lookup"><span data-stu-id="98f3f-132">This requirement must be met.</span></span>

  - <span data-ttu-id="98f3f-133">Eine lync Server Standard Edition-Bereitstellung muss nicht überschrieben werden, damit ein interner FQDN des Webdiensts nicht überschrieben werden kann, da dieser Server nicht Lastenausgleich erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="98f3f-133">A Lync Server Standard Edition deployment does not need or allow an internal web services FQDN to be overridden because this server cannot be load balanced.</span></span>

  - <span data-ttu-id="98f3f-134">Wenn Sie in Ihrer Umgebung über ein Hardware-Lastenausgleichsmodul verfügen, das Sie sowohl für den internen SIP-als auch für den Webverkehr verwenden, kann der Topologie-Generator die Unterscheidung nicht durchführen.</span><span class="sxs-lookup"><span data-stu-id="98f3f-134">If you have a hardware load balancer in your environment that you use for both internal SIP and web traffic, the Topology Builder cannot make the distinction.</span></span>
    
    <span data-ttu-id="98f3f-135">Webdienst-FQDNs sollten problemlos voneinander unterschieden werden. Dadurch wird sichergestellt, dass die URL-Umleitung Clients auf den entsprechenden Server verweist.</span><span class="sxs-lookup"><span data-stu-id="98f3f-135">Web service FQDNs should be easily-differentiated from one another; that helps to ensure that URL redirection points clients towards the appropriate server.</span></span> <span data-ttu-id="98f3f-136">Wenn Sie beispielsweise über zwei FQDNs verfügen, sollten Sie einen Meeting.contoso.com und den anderen Conferencing.contoso.com benennen.</span><span class="sxs-lookup"><span data-stu-id="98f3f-136">For example, if you have two FQDNs you might consider naming one meeting.contoso.com and the other conferencing.contoso.com.</span></span> <span data-ttu-id="98f3f-137">Wenn Sie FQDNs mit ähnlichen Namen wie "meet1.contoso.com" und "meet2.contoso.com" haben, können Sie möglicherweise zu Umleitungs Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="98f3f-137">You could potentially run into redirection issues if you have FQDNs with more similar names, such as meet1.contoso.com and meet2.contoso.com.</span></span>

<span data-ttu-id="98f3f-138">Die externen Webdienste funktionieren in Verbindung mit einem Reverse-Proxy im Umkreisnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="98f3f-138">The external web services works in conjunction with a reverse proxy in the perimeter network.</span></span> <span data-ttu-id="98f3f-139">Es bietet Clients externen Zugriff auf die Verwendung dieser Webdienste.</span><span class="sxs-lookup"><span data-stu-id="98f3f-139">It provides clients external access to by using these web services.</span></span> <span data-ttu-id="98f3f-140">Die hier konfigurierten FQDNs werden an Clients gesendet, wenn Sie sich anmelden, und werden verwendet, um eine HTTPS-Verbindung zurück zum Reverse-Proxy herzustellen, wenn eine Remoteverbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="98f3f-140">The FQDNs configured here are sent to clients when they log on, and are used to make an HTTPS connection back to the reverse proxy when connecting remotely.</span></span> <span data-ttu-id="98f3f-141">Der Reverse-Proxy-Server leitet den FQDN des externen Webdiensts an ein internes Hardware-Lastenausgleichsmodul oder direkt an den Pool weiter.</span><span class="sxs-lookup"><span data-stu-id="98f3f-141">The reverse-proxy server forwards the external web service FQDN to an internal hardware load balancer, or directly to the pool.</span></span> <span data-ttu-id="98f3f-142">Der Reverse-Proxy muss den FQDN der externen Webdienste in die IP-Adresse des internen Webservers auflösen können.</span><span class="sxs-lookup"><span data-stu-id="98f3f-142">The reverse proxy must be able to resolve the external web services FQDN to the IP address of the internal Web server.</span></span> <span data-ttu-id="98f3f-143">Die externen Webdienste-FDQN müssen im öffentlichen Internet aufgelöst werden können.</span><span class="sxs-lookup"><span data-stu-id="98f3f-143">The external web services FDQN must be resolvable in the public Internet.</span></span>

<span data-ttu-id="98f3f-144">Wenn es sich bei dem internen Server um einen Standard Edition-Server handelt, handelt es sich bei dem internen FQDN um den FQDN des Standard Edition-Servers.</span><span class="sxs-lookup"><span data-stu-id="98f3f-144">If your internal server is a Standard Edition server, the internal FQDN is the Standard Edition server FQDN.</span></span> <span data-ttu-id="98f3f-145">Wenn es sich bei dem internen Server um einen Front-End-Pool handelt, handelt es sich bei dem FQDN um einen Hardware-Lastenausgleichsmodul (Virtual IP, VIP), mit dem die internen Webfarmserver ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="98f3f-145">If your internal server is a Front End pool, the FQDN is a hardware load balancer virtual IP (VIP) that load balances the internal web farm servers.</span></span> <span data-ttu-id="98f3f-146">Ein Hardware-Lastenausgleichsmodul ist in einem Front-End-Pool mit mehr als einem Enterprise Edition-Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98f3f-146">A hardware load balancer is required in a Front End pool with more than one Enterprise Edition server.</span></span> <span data-ttu-id="98f3f-147">Ein Lastenausgleichsmodul ist für einen Standard Edition-Server oder einen einzelnen Enterprise Edition-Front-End-Server nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98f3f-147">A load balancer is not required for a Standard Edition server or a single Enterprise Edition Front End Server.</span></span>

<span data-ttu-id="98f3f-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98f3f-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

