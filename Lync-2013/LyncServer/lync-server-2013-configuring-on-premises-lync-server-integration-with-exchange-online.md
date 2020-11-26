---
title: Konfigurieren der lokalen lync-Server Integration in Exchange Online
description: Konfigurieren der lokalen lync Server-Integration in Exchange Online
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring on-premises Lync Server integration with Exchange Online
ms:assetid: 95a20117-2064-43c4-94fe-cac892cadb6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh533880(v=OCS.15)
ms:contentKeyID: 48184900
ms.date: 03/30/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 59c612bcdcdf4803bd6f9f2b38f1f9bb7dbad016
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432835"
---
# <a name="configuring-on-premises-lync-server-2013-integration-with-exchange-online"></a><span data-ttu-id="87b13-103">Konfigurieren der lokalen lync Server 2013-Integration in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="87b13-103">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87b13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87b13-104">

<span> </span></span></span>

<span data-ttu-id="87b13-105">_**Letztes Änderungsdatum des Themas:** 2018-03-30_</span><span class="sxs-lookup"><span data-stu-id="87b13-105">_**Topic Last Modified:** 2018-03-30_</span></span>

<span data-ttu-id="87b13-106">Kunden, die lokale lync Server 2013-Bereitstellungen verwenden, können in einem Hybrid Bereitstellungsmodus die Interoperabilität mit Microsoft Outlook Web App in Microsoft Exchange Online konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="87b13-106">Customers who are using on-premises Lync Server 2013 deployments can configure interoperability with Microsoft Outlook Web App in Microsoft Exchange Online in a hybrid deployment mode.</span></span> <span data-ttu-id="87b13-107">Zu den Interoperabilitätsfunktionen gehören einmaliges Anmelden (SSO) und Sofortnachrichten sowie die Anwesenheitsintegration in die Outlook Web App-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="87b13-107">Interoperability features include single sign on and instant messaging (IM) and presence integration with the Outlook Web App interface.</span></span> <span data-ttu-id="87b13-108">Um diese Integration zu aktivieren, müssen Sie den Edgeserver in Ihrer lokalen lync Server-Bereitstellung konfigurieren, indem Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="87b13-108">To enable this integration, you must configure the Edge Server in your on-premises Lync Server deployment by completing the following tasks:</span></span>

  - <span data-ttu-id="87b13-109">Konfigurieren eines freigegebenen SIP-Adressraums</span><span class="sxs-lookup"><span data-stu-id="87b13-109">Configure a shared SIP address space</span></span>

  - <span data-ttu-id="87b13-110">Konfigurieren eines Hostinganbieter auf dem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="87b13-110">Configure a hosting provider on the Edge Server</span></span>

  - <span data-ttu-id="87b13-111">Überprüfen der Replikation des aktualisierten zentralen Verwaltungsspeichers</span><span class="sxs-lookup"><span data-stu-id="87b13-111">Verify replication of the updated Central Management store</span></span>

<span data-ttu-id="87b13-112">Wenn lync Server 2013 in Exchange Online integriert ist, wird ein Benutzer, der versucht, sich bei Chat von OWA anzumeldet, als Remote-oder externer Benutzer betrachtet.</span><span class="sxs-lookup"><span data-stu-id="87b13-112">If Lync Server 2013 is integrated with Exchange Online, a user who is trying to sign in to IM from OWA is considered a remote or external user.</span></span> <span data-ttu-id="87b13-113">In diesem Szenario muss für diesen Benutzer eine Richtlinie für den externen Zugriff zugewiesen sein, auf der die folgende Option ausgewählt ist:</span><span class="sxs-lookup"><span data-stu-id="87b13-113">In this scenario, this user must have an external access policy assigned that has the following option selected:</span></span>

<span data-ttu-id="87b13-114">**Aktivieren der Kommunikation mit Remotebenutzern**</span><span class="sxs-lookup"><span data-stu-id="87b13-114">**Enable communications with remote users**</span></span>

<span data-ttu-id="87b13-115">Aktivieren Sie diese Option, wenn Sie möchten, dass Benutzer in Ihrer Organisation, die sich außerhalb Ihrer Firewall befinden, wie Telecommuter und Benutzer, die unterwegs sind, eine Verbindung mit lync Server über das Internet herstellen können.</span><span class="sxs-lookup"><span data-stu-id="87b13-115">Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

<span data-ttu-id="87b13-116">Weitere Informationen finden Sie unter [Verwalten von Richtlinien für den externen Zugriff in lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="87b13-116">For more information, see [Manage external access policy in Lync Server 2013](lync-server-2013-manage-external-access-policy-for-your-organization.md).</span></span>

<div>

## <a name="configure-a-shared-sip-address-space"></a><span data-ttu-id="87b13-117">Konfigurieren eines freigegebenen SIP-Adressraums</span><span class="sxs-lookup"><span data-stu-id="87b13-117">Configure a Shared SIP Address Space</span></span>

<span data-ttu-id="87b13-118">Zur Integration von lokalem lync Server 2013 in Exchange Online müssen Sie einen freigegebenen SIP-Adressraum konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="87b13-118">To integrate on-premises Lync Server 2013 with Exchange Online, you must configure a shared SIP address space.</span></span> <span data-ttu-id="87b13-119">Derselbe SIP-Domänen Adressraum wird sowohl von lync Server als auch vom Exchange Online-Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87b13-119">The same SIP domain address space is supported by both Lync Server and the Exchange Online service.</span></span>

<span data-ttu-id="87b13-120">Konfigurieren Sie mithilfe der lync Server-Verwaltungsshell den Edgeserver für Federation, indem Sie das Cmdlet " **csaccessedgeconfiguration nicht angeben** " mit den Parametern ausführen, die im folgenden Beispiel angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="87b13-120">Using the Lync Server Management Shell, configure the Edge Server for federation by running the **Set-CSAccessEdgeConfiguration** cmdlet, using the parameters that are displayed in the following example:</span></span>

    Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

  - <span data-ttu-id="87b13-121">**AllowFederatedUsers** gibt an, ob interne Benutzer mit Benutzern aus Partnerdomänen kommunizieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="87b13-121">**AllowFederatedUsers** specifies whether internal users are allowed to communicate with users from federated domains.</span></span> <span data-ttu-id="87b13-122">Diese Eigenschaft bestimmt auch, ob interne Benutzer mit Benutzern in einem freigegebenen SIP-Adressraum Szenario mit lync Server und Exchange Online kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="87b13-122">This property also determines whether internal users can communicate with users in a shared SIP address space scenario with Lync Server and Exchange Online.</span></span>

<span data-ttu-id="87b13-123">Ausführliche Informationen zur Verwendung der lync Server-Verwaltungsshell finden Sie unter [lync Server 2013-Verwaltungsshell](lync-server-2013-lync-server-management-shell.md).</span><span class="sxs-lookup"><span data-stu-id="87b13-123">For details about how to use the Lync Server Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md).</span></span>

</div>

<div>

## <a name="configure-a-hosting-provider-on-the-edge-server"></a><span data-ttu-id="87b13-124">Konfigurieren eines Hostinganbieters auf dem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="87b13-124">Configure a Hosting Provider on the Edge Server</span></span>

<span data-ttu-id="87b13-125">Verwenden Sie die lync Server-Verwaltungsshell, um einen Hostinganbieter auf dem Edgeserver zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="87b13-125">Use the Lync Server Management Shell to configure a hosting provider on the Edge Server.</span></span> <span data-ttu-id="87b13-126">Führen Sie dazu das Cmdlet **New-CsHostingProvider** aus, und verwenden Sie dazu die Parameter im folgenden Beispiel:</span><span class="sxs-lookup"><span data-stu-id="87b13-126">To do this, run the **New-CsHostingProvider** cmdlet, using the parameters in the following example:</span></span>

    New-CsHostingProvider -Identity "Exchange Online" -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFqdn "exap.um.outlook.com" -IsLocal $False -VerificationLevel UseSourceVerification

<div>


> [!NOTE]
> <span data-ttu-id="87b13-127">Wenn Sie Office 365 über 21Vianet in China nutzen, ersetzen Sie den Wert für den Parameter <STRONG>ProxyFqdn</STRONG> in diesem Beispiel („exap.um.outlook.com“) mit dem FQDN für den Dienst, der in China von 21Vianet bereitgestellt wird: „exap.um.partner.outlook.cn“.</span><span class="sxs-lookup"><span data-stu-id="87b13-127">If you are using Office 365 operated by 21Vianet in China, replace the value for the <STRONG>ProxyFqdn</STRONG> parameter in this example ("exap.um.outlook.com") with the FQDN for the service operated by 21Vianet: "exap.um.partner.outlook.cn".</span></span>



</div>

  - <span data-ttu-id="87b13-128">**Identity** gibt einen eindeutigen Zeichenfolgenwert für den Hostinganbieter an, den Sie erstellen (beispielsweise „Exchange Online“).</span><span class="sxs-lookup"><span data-stu-id="87b13-128">**Identity** specifies a unique string value identifier for the hosting provider that you are creating (for example, "Exchange Online").</span></span> <span data-ttu-id="87b13-129">Werte, die Leerzeichen enthalten, müssen in doppelten Anführungszeichen stehen.</span><span class="sxs-lookup"><span data-stu-id="87b13-129">Values that contain spaces must be in double quotation marks.</span></span>

  - <span data-ttu-id="87b13-130">**Enabled** gibt an, ob die Netzwerkverbindung zwischen Ihrer Domäne und dem Hostinganbieter aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87b13-130">**Enabled** indicates whether the network connection between your domain and the hosting provider is enabled.</span></span> <span data-ttu-id="87b13-131">Dies muss auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-131">This must be set to **True**.</span></span>

  - <span data-ttu-id="87b13-132">**EnabledSharedAddressSpace** gibt an, ob der Hostinganbieter in einem Szenario mit freigegebenem SIP-Adressraum verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87b13-132">**EnabledSharedAddressSpace** indicates whether the hosting provider will be used in a shared SIP address space scenario.</span></span> <span data-ttu-id="87b13-133">Dies muss auf " **true**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-133">This must be set to **True**.</span></span>

  - <span data-ttu-id="87b13-134">**HostsOCSUsers** gibt an, ob der Hostinganbieter zum Hosten von Office Communications Server oder lync Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87b13-134">**HostsOCSUsers** indicates whether the hosting provider is used to host Office Communications Server or Lync Server.</span></span> <span data-ttu-id="87b13-135">Dieser Wert muss auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-135">This must be set to **False**.</span></span>

  - <span data-ttu-id="87b13-136">**ProxyFQDN** gibt den vollqualifizierten Domänennamen (FQDN) des vom Hostinganbieter verwendeten Proxyservers an.</span><span class="sxs-lookup"><span data-stu-id="87b13-136">**ProxyFQDN** specifies the fully qualified domain name (FQDN) for the proxy server used by the hosting provider.</span></span> <span data-ttu-id="87b13-137">Für Exchange Online ist der FQDN „exap.um.outlook.com“.</span><span class="sxs-lookup"><span data-stu-id="87b13-137">For Exchange Online, the FQDN is exap.um.outlook.com.</span></span>

  - <span data-ttu-id="87b13-138">**IsLocal** gibt an, ob der vom Hostinganbieter verwendete Proxy Server in ihrer lync Server-Topologie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="87b13-138">**IsLocal** indicates whether the proxy server used by the hosting provider is contained within your Lync Server topology.</span></span> <span data-ttu-id="87b13-139">Dieser Wert muss auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-139">This must be set to **False**.</span></span>

  - <span data-ttu-id="87b13-140">**"Verificationlevel"** gibt die Überprüfungsstufe für Nachrichten an, die an den und vom gehosteten Anbieter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-140">**VerificationLevel** indicates the verification level allowed for messages that are sent to and from the hosted provider.</span></span> <span data-ttu-id="87b13-141">Geben Sie **UseSourceVerification**.</span><span class="sxs-lookup"><span data-stu-id="87b13-141">Specify **UseSourceVerification**.</span></span> <span data-ttu-id="87b13-142">Diese Option basiert auf der Überprüfungsstufe, die in Nachrichten enthalten ist, die vom Hostinganbieter gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-142">This option relies on the verification level that is included in messages that are sent from the hosting provider.</span></span> <span data-ttu-id="87b13-143">Wenn diese Ebene nicht angegeben wird, wird die Nachricht als nicht überprüfbar zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="87b13-143">If this level is not specified, the message will be rejected as being unverifiable.</span></span>

</div>

<div>

## <a name="verify-replication-of-the-updated-central-management-store"></a><span data-ttu-id="87b13-144">Überprüfen der Replikation des aktualisierten zentralen Verwaltungsspeichers</span><span class="sxs-lookup"><span data-stu-id="87b13-144">Verify Replication of the Updated Central Management Store</span></span>

<span data-ttu-id="87b13-145">Die Änderungen, die Sie mithilfe der Cmdlets in den vorhergehenden Abschnitten vorgenommen haben, werden automatisch auf den Edgeserver angewendet, und in der Regel dauert es weniger als eine Minute, bis Sie repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="87b13-145">The changes that you made by using the cmdlets in the preceding sections are automatically applied to the Edge Server, and generally take less than one minute to replicate.</span></span> <span data-ttu-id="87b13-146">Mithilfe der folgenden Cmdlets können Sie den Replikationsstatus überprüfen und die Änderungen auf den Edgeserver anwenden.</span><span class="sxs-lookup"><span data-stu-id="87b13-146">You can verify the replication status and that the changes were applied to your Edge Server by using the following cmdlets.</span></span>

<span data-ttu-id="87b13-147">Führen Sie das folgende Cmdlet aus, um Replikationsupdates auf einem internen Server in ihrer lync Server-Bereitstellung zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="87b13-147">To verify replication updates on a server internal in your Lync Server deployment, run the following cmdlet:</span></span>

    Get-CsManagementStoreReplicationStatus

<span data-ttu-id="87b13-148">Führen Sie das folgende Cmdlet auf dem Edgeserver aus, um zu überprüfen, ob die Änderungen übernommen wurden:</span><span class="sxs-lookup"><span data-stu-id="87b13-148">To verify that the changes were applied, run the following cmdlet on the Edge Server:</span></span>

    Get-CsHostingProvider -LocalStore

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="87b13-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87b13-149">See Also</span></span>


[<span data-ttu-id="87b13-150">Bereitstellen von Voicemail für Benutzer von Lync Server 2013 für gehostete Exchange Unified Messaging-Dienste</span><span class="sxs-lookup"><span data-stu-id="87b13-150">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)  
[<span data-ttu-id="87b13-151">Integration in gehostete Exchange Unified Messaging-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87b13-151">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-unified-messaging-integration.md)  
  

<span data-ttu-id="87b13-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87b13-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
