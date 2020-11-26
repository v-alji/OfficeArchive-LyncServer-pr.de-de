---
title: 'Lync Server 2013: Erstellen und Überprüfen von DNS-SRV-Einträgen'
description: 'Lync Server 2013: Erstellen und Überprüfen von DNS-SRV-Einträgen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create and verify DNS SRV records
ms:assetid: 86888c7e-1401-458f-9a7b-08ac726deeec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398680(v=OCS.15)
ms:contentKeyID: 48184714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a71c876d0b26b9305feed7146fa6321a3983588d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432016"
---
# <a name="create-and-verify-dns-srv-records-in-lync-server-2013"></a><span data-ttu-id="627a0-103">Erstellen und Überprüfen von DNS-SRV-Einträgen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="627a0-103">Create and verify DNS SRV records in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="627a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="627a0-104">

<span> </span></span></span>

<span data-ttu-id="627a0-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="627a0-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="627a0-106">Um dieses Verfahren erfolgreich durchführen zu können, sollten Sie am Server oder in der Domäne minimal als Mitglied der Gruppe der Domänenadministratoren oder als Mitglied der DnsAdmins-Gruppe angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="627a0-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="627a0-107">In diesem Thema wird beschrieben, wie Sie die DNS-Einträge (Domain Name System) konfigurieren, die Sie in lync Server 2013-Bereitstellungen erstellen müssen, und die für die automatische Clientanmeldung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="627a0-107">This topic describes how to configure the Domain Name System (DNS) records that you are required to create in Lync Server 2013 deployments and those required for automatic client sign in.</span></span> <span data-ttu-id="627a0-108">Wenn Sie einen Front-End-Pool erstellen, erstellt Setup Active Directory-Objekte und-Einstellungen für den Pool, einschließlich des vollqualifizierten Domänennamens (Fully Qualified Domain Name, FQDN) des Pools.</span><span class="sxs-lookup"><span data-stu-id="627a0-108">When you create a Front End pool, Setup creates Active Directory objects and settings for the pool, including the pool fully qualified domain name (FQDN).</span></span> <span data-ttu-id="627a0-109">Ähnliche Objekte und Einstellungen werden für einen Standard Edition-Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="627a0-109">Similar objects and settings are created for a Standard Edition server.</span></span> <span data-ttu-id="627a0-110">Damit Clients eine Verbindung mit dem Pool oder dem Standard Edition-Server herstellen können, muss der FQDN des Pools oder Standard Edition-Servers in DNS registriert sein.</span><span class="sxs-lookup"><span data-stu-id="627a0-110">For clients to be able to connect to the pool or Standard Edition server, the FQDN of the pool or Standard Edition server must be registered in DNS.</span></span> <span data-ttu-id="627a0-111">Sie müssen DNS-SRV-Einträge in Ihrem internen DNS für jede SIP-Domäne erstellen.</span><span class="sxs-lookup"><span data-stu-id="627a0-111">You must create DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="627a0-112">Bei diesem Verfahren wird davon ausgegangen, dass Ihr interner DNS Zonen für Ihre SIP-Benutzerdomänen aufweist.</span><span class="sxs-lookup"><span data-stu-id="627a0-112">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<div>

## <a name="to-configure-a-dns-srv-record"></a><span data-ttu-id="627a0-113">So konfigurieren Sie einen DNS-SRV-Eintrag</span><span class="sxs-lookup"><span data-stu-id="627a0-113">To configure a DNS SRV record</span></span>

1.  <span data-ttu-id="627a0-114">Klicken Sie auf dem DNS-Server auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="627a0-114">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="627a0-115">Erweitern Sie in der Konsolenstruktur ihrer SIP-Domäne **Forward-Lookupzonen**, und klicken Sie dann mit der rechten Maustaste auf die SIP-Domäne, in der lync Server 2013 installiert wird.</span><span class="sxs-lookup"><span data-stu-id="627a0-115">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and then right-click the SIP domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="627a0-116">Klicken Sie auf **andere neue Datensätze**.</span><span class="sxs-lookup"><span data-stu-id="627a0-116">Click **Other New Records**.</span></span>

4.  <span data-ttu-id="627a0-117">Klicken Sie unter **Wählen Sie einen Ressourceneintragstyp** auf **Dienstidentifizierung (SRV)** und dann auf **Eintrag erstellen**.</span><span class="sxs-lookup"><span data-stu-id="627a0-117">In **Select a resource record type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

5.  <span data-ttu-id="627a0-118">Klicken Sie auf **Dienst**, und geben Sie **\_ sipinternaltls** ein.</span><span class="sxs-lookup"><span data-stu-id="627a0-118">Click **Service**, and then type **\_sipinternaltls**.</span></span>

6.  <span data-ttu-id="627a0-119">Klicken Sie auf **Protokoll**, und geben Sie dann **\_ TCP** ein.</span><span class="sxs-lookup"><span data-stu-id="627a0-119">Click **Protocol**, and then type **\_tcp**.</span></span>

7.  <span data-ttu-id="627a0-120">Klicken Sie auf **Portnummer** und geben Sie **5061** ein.</span><span class="sxs-lookup"><span data-stu-id="627a0-120">Click **Port Number**, and then type **5061**.</span></span>

8.  <span data-ttu-id="627a0-121">Klicken Sie auf **Host, der diesen Dienst anbietet** und geben Sie den FQDN des Pools bzw. des Standard Edition-Servers ein.</span><span class="sxs-lookup"><span data-stu-id="627a0-121">Click **Host offering this service**, and then type the FQDN of the pool or Standard Edition server.</span></span>

9.  <span data-ttu-id="627a0-122">Klicken Sie auf **OK** und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="627a0-122">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-the-creation-of-a-dns-srv-record"></a><span data-ttu-id="627a0-123">So überprüfen Sie die Erstellung eines DNS-SRV-Eintrags</span><span class="sxs-lookup"><span data-stu-id="627a0-123">To verify the creation of a DNS SRV record</span></span>

1.  <span data-ttu-id="627a0-124">Melden Sie sich mit einem Konto, das Mitglied der Gruppe der authentifizierten Benutzer ist oder über gleichwertige Berechtigungen verfügt, an einem Clientcomputer in der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="627a0-124">Log on to a client computer in the domain with an account that is a member of the Authenticated Users group or has equivalent permissions.</span></span>

2.  <span data-ttu-id="627a0-125">Klicken Sie auf  **Start** und dann auf  **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="627a0-125">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="627a0-126">Geben Sie im Feld **Öffnen** den **Befehl cmd** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="627a0-126">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="627a0-127">Geben Sie an der Eingabeaufforderung **nslookup** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="627a0-127">At the command prompt, type **nslookup**, and then press ENTER.</span></span>

5.  <span data-ttu-id="627a0-128">Geben Sie Type **= SRV** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="627a0-128">Type **set type=srv**, and then press ENTER.</span></span>

6.  <span data-ttu-id="627a0-129">Geben Sie **\_ sipinternaltls ein. \_ TCP.contoso.com**, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="627a0-129">Type **\_sipinternaltls.\_tcp.contoso.com**, and then press ENTER.</span></span> <span data-ttu-id="627a0-130">Die für den TLS-Eintrag (Transport Layer Security) angezeigte Ausgabe lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="627a0-130">The output displayed for the Transport Layer Security (TLS) record is as follows:</span></span>
    
    <span data-ttu-id="627a0-131">Server: \<dns server\> . contoso.com</span><span class="sxs-lookup"><span data-stu-id="627a0-131">Server: \<dns server\>.contoso.com</span></span>
    
    <span data-ttu-id="627a0-132">Adresse \<IP address of DNS server\></span><span class="sxs-lookup"><span data-stu-id="627a0-132">Address: \<IP address of DNS server\></span></span>
    
    <span data-ttu-id="627a0-133">Nicht autorisierende Antwort:</span><span class="sxs-lookup"><span data-stu-id="627a0-133">Non-authoritative answer:</span></span>
    
    <span data-ttu-id="627a0-134">\_sipinternaltls. \_ TCP.contoso.com SRV-Dienststandort:</span><span class="sxs-lookup"><span data-stu-id="627a0-134">\_sipinternaltls.\_tcp.contoso.com SRV service location:</span></span>
    
    <span data-ttu-id="627a0-135">Priorität = 0</span><span class="sxs-lookup"><span data-stu-id="627a0-135">priority = 0</span></span>
    
    <span data-ttu-id="627a0-136">Gewichtung = 0</span><span class="sxs-lookup"><span data-stu-id="627a0-136">weight = 0</span></span>
    
    <span data-ttu-id="627a0-137">Port = 5061</span><span class="sxs-lookup"><span data-stu-id="627a0-137">port = 5061</span></span>
    
    <span data-ttu-id="627a0-138">SVR Hostname = Poolname.contoso.com (oder Standard Edition Server A Record)</span><span class="sxs-lookup"><span data-stu-id="627a0-138">svr hostname = poolname.contoso.com (or Standard Edition server A record)</span></span>
    
    <span data-ttu-id="627a0-139">Poolname.contoso.com Internetadresse = \<virtual IP Address of the load balancer\> oder \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> oder \<IP address of the Standard Edition server\></span><span class="sxs-lookup"><span data-stu-id="627a0-139">poolname.contoso.com internet address = \<virtual IP Address of the load balancer\> or \<IP address of a single Enterprise Edition server for pools with only one Enterprise Edition server\> or \<IP address of the Standard Edition server\></span></span>

7.  <span data-ttu-id="627a0-140">Wenn Sie die Eingabeaufforderung beendet haben, geben Sie **Exit** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="627a0-140">When you are finished, at the command prompt, type **exit**, and then press ENTER.</span></span>

</div>

<div>

## <a name="to-verify-that-the-fqdn-of-the-front-end-pool-or-standard-edition-server-can-be-resolved"></a><span data-ttu-id="627a0-141">So überprüfen Sie, ob der FQDN des Front-End-Pools oder des Standard Edition-Servers aufgelöst werden kann</span><span class="sxs-lookup"><span data-stu-id="627a0-141">To verify that the FQDN of the Front End pool or Standard Edition server can be resolved</span></span>

1.  <span data-ttu-id="627a0-142">Melden Sie sich bei einem Clientcomputer in der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="627a0-142">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="627a0-143">Klicken Sie auf  **Start** und dann auf  **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="627a0-143">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="627a0-144">Geben Sie im Feld **Öffnen** den **Befehl cmd** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="627a0-144">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="627a0-145">Geben Sie an der Eingabeaufforderung **nslookup** \<FQDN of the Front End pool\> oder \<FQDN of the Standard Edition server\> ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="627a0-145">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="627a0-146">Überprüfen Sie, ob Sie eine Antwort erhalten, die in die entsprechende IP-Adresse für den FQDN aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="627a0-146">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="627a0-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="627a0-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

