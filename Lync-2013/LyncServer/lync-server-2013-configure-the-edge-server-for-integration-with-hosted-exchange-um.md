---
title: Konfigurieren des Edgeservers für die Integration in gehostete Exchange UM-Dienste
description: Konfigurieren Sie den Edgeserver für die Integration in gehostete Exchange UM.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Edge Server for integration with hosted Exchange UM
ms:assetid: ede3f2f9-f412-418e-a705-8d8ec98176c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399075(v=OCS.15)
ms:contentKeyID: 48185745
ms.date: 01/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1a2eb55df172e6df0bacef0c468a235cb00c3f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433647"
---
# <a name="configure-the-edge-server-for-integration-with-hosted-exchange-um"></a><span data-ttu-id="98114-103">Konfigurieren des Edgeservers für die Integration in gehostete Exchange UM-Dienste</span><span class="sxs-lookup"><span data-stu-id="98114-103">Configure the Edge Server for integration with hosted Exchange UM</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98114-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98114-104">

<span> </span></span></span>

<span data-ttu-id="98114-105">_**Thema Zuletzt geändert:** 23.01.2015_</span><span class="sxs-lookup"><span data-stu-id="98114-105">_**Topic Last Modified:** 2015-01-23_</span></span>

<span data-ttu-id="98114-106">Wenn Sie Ihren Lync Server 2013-Benutzern Voicemailfunktionen für gehostete Exchange Unified Messaging (UM) bereitstellen möchten, müssen Sie die folgenden Konfigurationsaufgaben auf dem Edgeserver ausführen:</span><span class="sxs-lookup"><span data-stu-id="98114-106">To provide your Lync Server 2013 users with voice mail capabilities on hosted Exchange Unified Messaging (UM), you must perform the following configuration tasks on the Edge Server:</span></span>

  - <span data-ttu-id="98114-107">Konfigurieren Sie den Edgeserver für einen Partnerverbund.</span><span class="sxs-lookup"><span data-stu-id="98114-107">Configure the Edge Server for federation.</span></span>

  - <span data-ttu-id="98114-108">Replizieren Sie Daten aus dem Zentralen Verwaltungsspeicher auf den Edgeserver, und überprüfen Sie die Replikation.</span><span class="sxs-lookup"><span data-stu-id="98114-108">Replicate Central Management store data to the Edge Server and verify the replication.</span></span>

  - <span data-ttu-id="98114-109">Erstellen Sie auf dem Edgeserver einen Hostinganbieter.</span><span class="sxs-lookup"><span data-stu-id="98114-109">Create a hosting provider on the Edge Server.</span></span>

<span data-ttu-id="98114-110">Ausführliche Informationen finden Sie in der Dokumentation zur Lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="98114-110">For details, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="98114-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="98114-111">[Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))</span></span>

  - <span data-ttu-id="98114-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="98114-112">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="98114-113">Vor dem Ausführen dieser Schritte müssen Sie einen externen DNS-SRV-Eintrag zum Hosten des Exchange-Diensts erstellen.</span><span class="sxs-lookup"><span data-stu-id="98114-113">You must create an external DNS SRV record for the hosting Exchange service before you perform these steps.</span></span> <span data-ttu-id="98114-114">Details finden Sie unter <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Erstellen eines DNS SRV-Eintrags für die Integration in gehostete Exchange UM.</A></span><span class="sxs-lookup"><span data-stu-id="98114-114">For details, see <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Create a DNS SRV record for integration with hosted Exchange UM</A>.</span></span>



</div>

<div>

## <a name="to-configure-the-edge-server-for-federation"></a><span data-ttu-id="98114-115">So konfigurieren Sie den Edgeserver für einen Partnerverbund</span><span class="sxs-lookup"><span data-stu-id="98114-115">To configure the Edge Server for federation</span></span>

1.  <span data-ttu-id="98114-116">Starten Sie die Lync Server-Verwaltungsshell: Klicken Sie auf **Start,** klicken Sie auf **Alle Programme,** klicken Sie auf **Microsoft Lync Server 2013,** und klicken Sie dann **auf Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="98114-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="98114-p102">Führen Sie das Cmdlet "Set-CsAccessEdgeConfiguration" aus, um den Server für einen Partnerverbund zu konfigurieren. Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="98114-p102">Run the Set-CsAccessEdgeConfiguration cmdlet to configure the server for federation. For example, run:</span></span>
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -AllowFederatedUsers 1 -EnablePartnerDiscovery 0
    
    <span data-ttu-id="98114-119">Im oben stehenden Beispiel werden folgende Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="98114-119">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="98114-120">**UseDnsSrvRouting** gibt an, dass Edgeserver beim Senden und Empfangen von Partnerverbundanforderungen auf DNS-SRV-Einträge zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="98114-120">**UseDnsSrvRouting** specifies that Edge Servers will rely on DNS SRV records when sending and receiving federation requests.</span></span>
    
      - <span data-ttu-id="98114-p103">**AllowFederatedUsers** gibt an, ob interne Benutzer mit Benutzern aus Partnerdomänen kommunizieren dürfen. Diese Eigenschaft legt außerdem fest, ob interne Benutzer mit Benutzern in einem Szenario mit getrennten Domänen kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="98114-p103">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains. This property also determines whether internal users can communicate with users in a split domain scenario.</span></span>
    
      - <span data-ttu-id="98114-123">**EnablePartnerDiscovery** gibt an, ob Lync Server DNS-Einträge verwendet, um Partnerdomänen zu ermitteln, die nicht in der Liste der zulässigen Active Directory-Domänen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="98114-123">**EnablePartnerDiscovery** specifies whether Lync Server will use DNS records to try to discover partner domains not listed in the Active Directory allowed domains list.</span></span> <span data-ttu-id="98114-124">Ist False, wird Lync Server 2013 nur mit Domänen in der Liste zulässiger Domänen in Verbindung stehen.</span><span class="sxs-lookup"><span data-stu-id="98114-124">If False, Lync Server 2013 will only federate with domains found on the allowed domains list.</span></span> <span data-ttu-id="98114-125">Dieser Parameter ist für die Verwendung von DNS-Dienstrouting erforderlich.</span><span class="sxs-lookup"><span data-stu-id="98114-125">This parameter is required if you use DNS service routing.</span></span> <span data-ttu-id="98114-126">In den meisten Bereitstellungen ist der Wert auf "False" gesetzt, um einen Partnerverbund mit allen Partnern zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="98114-126">In most deployments, the value is set to false to avoid opening up federation to all partners.</span></span>

</div>

<div>

## <a name="to-replicate-data-to-the-edge-server-and-verify-the-replication"></a><span data-ttu-id="98114-127">So replizieren Sie Daten auf den Edgeserver und überprüfen die Replikation</span><span class="sxs-lookup"><span data-stu-id="98114-127">To replicate data to the Edge Server and verify the replication</span></span>

  - <span data-ttu-id="98114-128">Überprüfen Sie, ob die Replikation auf den Edgeserver vollständig durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="98114-128">Verify that the replication to the Edge Server is complete.</span></span> <span data-ttu-id="98114-129">Das Verfahren finden Sie unter [Überprüfen der Konnektivität zwischen internen Servern und Edgeservern in Lync Server 2013.](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)</span><span class="sxs-lookup"><span data-stu-id="98114-129">For the procedure, see [Verify connectivity between internal servers and Edge Servers in Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md).</span></span>

</div>

<div>

## <a name="to-create-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="98114-130">So erstellen Sie auf dem Edgeserver einen Hostinganbieter</span><span class="sxs-lookup"><span data-stu-id="98114-130">To create a hosting provider on the Edge Server</span></span>

1.  <span data-ttu-id="98114-131">Starten Sie die Lync Server-Verwaltungsshell: Klicken Sie auf **Start,** klicken Sie auf **Alle Programme,** klicken Sie auf **Microsoft Lync Server 2013,** und klicken Sie dann **auf Lync Server Management Shell**.</span><span class="sxs-lookup"><span data-stu-id="98114-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="98114-132">Führen Sie das **New-CsHostingProvider**-Cmdlet aus, um den Hostinganbieter zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="98114-132">Run the **New-CsHostingProvider** cmdlet to configure the hosting provider.</span></span> <span data-ttu-id="98114-133">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="98114-133">For example, run:</span></span>
    
        New-CsHostingProvider -Identity Fabrikam.com -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFQDN "proxyserver.fabrikam.com" -IsLocal $False -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="98114-134">Im oben stehenden Beispiel werden folgende Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="98114-134">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="98114-p107">**Identity** gibt einen eindeutigen Zeichenfolgenwert für den Hostinganbieter an, den Sie erstellen, in diesem Beispiel **Fabrikam.com**. Beachten Sie, dass der Befehl nicht erfolgreich ist, wenn bereits ein Anbieter mit dieser Identität konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="98114-p107">**Identity** specifies a unique string value identifier for the hosting provider you are creating, in this example, **Fabrikam.com**. Note that the command will fail if an existing provider has already been configured with that Identity.</span></span>
    
      - <span data-ttu-id="98114-p108">**Enabled** gibt an, ob die Netzwerkverbindung zwischen Ihrer Domäne und dem Hostinganbieter aktiviert ist. Der Nachrichtenaustausch zwischen zwei Organisationen ist erst möglich, wenn dieser Wert auf **True** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="98114-p108">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled. Messages cannot be exchanged between the two organizations until this value is set to **True**.</span></span>
    
      - <span data-ttu-id="98114-139">**EnabledSharedAddressSpace** gibt an, ob der Hostinganbieter in einem Szenario mit freigegebenem SIP-Adressraum (getrennte Domäne) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98114-139">**EnabledSharedAddressSpace** indicates whether the hosting provider is being used in a shared SIP address space (split domain) scenario.</span></span>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="98114-140">Versuchen Sie vor <CODE>EnableSharedAddressSpace</CODE> dem Festlegen von True, den SrV-Eintrag des Verbunds intern zu beheben.</span><span class="sxs-lookup"><span data-stu-id="98114-140">Before you set <CODE>EnableSharedAddressSpace</CODE> to True, try to resolve the Federation SRV record internally.</span></span> <span data-ttu-id="98114-141">Wenn dieser Datensatz nicht intern aufgelöst werden kann, müssen Sie die Datensätze erstellen, _sipfederationtls._tcp. &lt; domäne &gt; und _sip._tls. &lt; domäne &gt; im internen DNS.</span><span class="sxs-lookup"><span data-stu-id="98114-141">If this record cannot be resolved internally, then you need to create the records, _sipfederationtls._tcp.&lt;domain&gt; and _sip._tls.&lt;domain&gt; in the internal DNS.</span></span> <span data-ttu-id="98114-142">Diese Einträge müssen auf die externe IP-Adresse der Zugriffsschnittstelle des Edgeservers verweisen.</span><span class="sxs-lookup"><span data-stu-id="98114-142">These records should point to the external IP address of the Access Interface of the Edge Server.</span></span>

        
        </div>
    
      - <span data-ttu-id="98114-143">**HostsOCSUsers** gibt an, ob der Hostinganbieter zum Hosten von Lync Server 2013-Konten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98114-143">**HostsOCSUsers** indicates whether the hosting provider is used to host Lync Server 2013 accounts.</span></span> <span data-ttu-id="98114-144">Der Wert **False** gibt an, dass der Anbieter andere Kontotypen (z. B. Microsoft Exchange-Konten) hostet.</span><span class="sxs-lookup"><span data-stu-id="98114-144">If **False**, the provider hosts other account types, such as Microsoft Exchange accounts.</span></span>
    
      - <span data-ttu-id="98114-p111">**ProxyFQDN** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des vom Hostinganbieter verwendeten Proxyservers an, in diesem Beispiel **proxyserver.fabrikam.com**. Dieser Wert kann nicht geändert werden. Wenn der Hostinganbieter seinen Proxyserver ändert, muss der Eintrag für diesen Anbieter gelöscht und neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="98114-p111">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider, in this example, **proxyserver.fabrikam.com**. This value cannot be modified. If the hosting provider changes its proxy server you will need to delete and then recreate the entry for that provider.</span></span>
    
      - <span data-ttu-id="98114-148">**IsLocal** gibt an, ob der vom Hostinganbieter verwendete Proxyserver in Ihrer Lync Server 2013-Topologie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="98114-148">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server 2013 topology.</span></span>
    
      - <span data-ttu-id="98114-149">**VerificationLevel** gibt die Überprüfungsstufe an, die für Nachrichten zulässig ist, die an den und vom gehosteten Anbieter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="98114-149">**VerficationLevel** indicates the allowed verification level for messages sent to and from the hosted provider.</span></span> <span data-ttu-id="98114-150">Geben Sie den **UseSourceVerification**-Wert an, der von der Überprüfungsstufe in Nachrichten abhängt, die vom Hostinganbieter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="98114-150">Specify **UseSourceVerification**, which relies on the verification level included in messages sent from the hosting provider.</span></span> <span data-ttu-id="98114-151">Wenn diese Stufe nicht angegeben ist, wird die Nachricht als nicht überprüfbar eingestuft und abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="98114-151">If this level is not specified, then the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="98114-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98114-152">See Also</span></span>


[<span data-ttu-id="98114-153">Exportieren der Lync Server 2013-Topologie und Kopieren auf externe Medien zur Edgeinstallation</span><span class="sxs-lookup"><span data-stu-id="98114-153">Export your Lync Server 2013 topology and copy it to external media for edge installation</span></span>](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)  


[<span data-ttu-id="98114-154">Überprüfen der Konnektivität zwischen internen Servern und Edgeservern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98114-154">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)  


<span data-ttu-id="98114-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="98114-155">[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))</span></span>  
  

<span data-ttu-id="98114-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98114-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

