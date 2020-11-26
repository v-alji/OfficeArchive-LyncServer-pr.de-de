---
title: Erstellen eines DNS-SRV-Eintrags für die Integration in gehostete Exchange UM-Dienste
description: Erstellen Sie einen DNS-SRV-Eintrag für die Integration in gehostete Exchange um.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432233"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="00ed9-103">Erstellen eines DNS-SRV-Eintrags für die Integration in gehostete Exchange UM-Dienste</span><span class="sxs-lookup"><span data-stu-id="00ed9-103">Create a DNS SRV record for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="00ed9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="00ed9-104">

<span> </span></span></span>

<span data-ttu-id="00ed9-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="00ed9-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="00ed9-106">In diesem Thema wird beschrieben, wie Sie den DNS-SRV-Eintrag (Domain Name System) konfigurieren, der für einen lync Server 2013-Edgeserver zur Weiterleitung an einen gehosteten Exchange-Dienst wie Microsoft Exchange Online erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="00ed9-106">This topic describes how to configure the Domain Name System (DNS) SRV record that is required for a Lync Server 2013 Edge Server to route to a hosted Exchange service such as Microsoft Exchange Online.</span></span>

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a><span data-ttu-id="00ed9-107">So erstellen Sie einen externen DNS-SRV-Eintrag für den gehosteten Exchange-Dienst</span><span class="sxs-lookup"><span data-stu-id="00ed9-107">To create an external DNS SRV record for the hosted Exchange service</span></span>

1.  <span data-ttu-id="00ed9-108">Melden Sie sich beim externen DNS-Server als Mitglied der DnsAdmins-Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="00ed9-108">Log on to the external DNS server as a member of the DnsAdmins group.</span></span>

2.  <span data-ttu-id="00ed9-109">Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="00ed9-109">Click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

3.  <span data-ttu-id="00ed9-110">Erweitern Sie in der Konsolenstruktur ihrer SIP-Domäne **Forward-Lookupzonen**, und wählen Sie die SIP-Domäne aus, in der lync Server 2013 installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="00ed9-110">In the console tree for your SIP domain, expand **Forward Lookup Zones**, and select the SIP domain in which Lync Server 2013 will be installed.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="00ed9-111">Sie müssen den DNS-SRV-Eintrag in der SIP-Domäne erstellen, in der lync Server installiert ist oder installiert wird.</span><span class="sxs-lookup"><span data-stu-id="00ed9-111">You must create the DNS SRV record in the SIP domain in which Lync Server is or will be installed.</span></span> <span data-ttu-id="00ed9-112">Wenn Sie den SRV-Eintrag erstellen, muss der für den Host mit diesem Dienst Feld verwendete FQDN der externe FQDN des Edge-Pools sein.</span><span class="sxs-lookup"><span data-stu-id="00ed9-112">When you create the SRV record, the FQDN used for the Host offering this service field must be the external FQDN of the Edge pool.</span></span> <span data-ttu-id="00ed9-113">Wenn beispielsweise der externe FQDN Ihres Edge-Pools Edge01.contoso.net lautet, geben Sie diesen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="00ed9-113">For example, if the external FQDN of your Edge pool is edge01.contoso.net, enter that value.</span></span> <span data-ttu-id="00ed9-114">Dieser muss sich ebenfalls in der gleichen Domäne wie der DNS-Hosteintrag (A) befinden.</span><span class="sxs-lookup"><span data-stu-id="00ed9-114">This must also be in the same domain as the DNS Hosts (A) record.</span></span>

    
    </div>

4.  <span data-ttu-id="00ed9-115">Klicken Sie mit der rechten Maustaste auf die ausgewählte Domäne, und klicken Sie dann auf **Weitere neue Einträge**.</span><span class="sxs-lookup"><span data-stu-id="00ed9-115">Right-click the selected domain, and then click **Other New Records**.</span></span>

5.  <span data-ttu-id="00ed9-116">Klicken Sie unter **Ressourceneintragstyp** auf **Dienststandort (SRV)**, und klicken Sie dann auf **Datensatz erstellen**.</span><span class="sxs-lookup"><span data-stu-id="00ed9-116">In **Resource Record Type**, click **Service Location (SRV)**, and then click **Create Record**.</span></span>

6.  <span data-ttu-id="00ed9-117">Klicken Sie im **neuen Ressourceneintrag** auf **Dienst**, und geben Sie **\_ sipfederationtls** ein.</span><span class="sxs-lookup"><span data-stu-id="00ed9-117">In **New Resource Record**, click **Service**, and then type **\_sipfederationtls**.</span></span>

7.  <span data-ttu-id="00ed9-118">Klicken Sie auf **Protokoll**, und geben Sie dann **\_ TCP** ein.</span><span class="sxs-lookup"><span data-stu-id="00ed9-118">Click **Protocol**, and then type **\_tcp**.</span></span>

8.  <span data-ttu-id="00ed9-119">Klicken Sie auf **Portnummer** und geben Sie **5061** ein.</span><span class="sxs-lookup"><span data-stu-id="00ed9-119">Click **Port Number**, and then type **5061**.</span></span>

9.  <span data-ttu-id="00ed9-120">Klicken Sie auf **Host mit diesem Dienst**, und geben Sie dann den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des lync Server 2013-Edge-Pools ein, der Zugriff auf Ihr lync Server 2013-System für vertrauenswürdige externe Clients bietet.</span><span class="sxs-lookup"><span data-stu-id="00ed9-120">Click **Host offering this service**, and then type the fully qualified domain name (FQDN) of the Lync Server 2013 Edge pool that provides access to your Lync Server 2013 system for trusted external clients.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="00ed9-121">Die Domäne muss auch als autorisierende, akzeptierte Domäne in Ihren Exchange Online-Einstellungen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="00ed9-121">The domain must also be set up as an authoritative, accepted domain in your Exchange Online settings.</span></span> <span data-ttu-id="00ed9-122">Ausführliche Informationen finden Sie unter Erstellen von akzeptierten Domänen unter <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> .</span><span class="sxs-lookup"><span data-stu-id="00ed9-122">For details, see Create Accepted Domains at <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A>.</span></span>

    
    </div>

10. <span data-ttu-id="00ed9-123">Klicken Sie auf **OK** und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="00ed9-123">Click **OK**, and then click **Done**.</span></span>

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a><span data-ttu-id="00ed9-124">So überprüfen Sie, ob der DNS-SRV-Eintrag erfolgreich erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="00ed9-124">To verify that the DNS SRV record was created successfully</span></span>

1.  <span data-ttu-id="00ed9-125">Melden Sie sich bei einem Clientcomputer in der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="00ed9-125">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="00ed9-126">Klicken Sie auf  **Start** und dann auf  **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="00ed9-126">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="00ed9-127">Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="00ed9-127">At the command prompt, run the following command:</span></span>
    
        nslookup <FQDN Lync Edge Pool>

4.  <span data-ttu-id="00ed9-128">Überprüfen Sie, ob Sie eine Antwort erhalten, die in die entsprechende IP-Adresse für den FQDN aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="00ed9-128">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="00ed9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00ed9-129">See Also</span></span>


[<span data-ttu-id="00ed9-130">Erstellen von DNS-Einträgen für Reverseproxyserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="00ed9-130">Create DNS records for reverse proxy servers in Lync Server 2013</span></span>](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

<span data-ttu-id="00ed9-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="00ed9-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

