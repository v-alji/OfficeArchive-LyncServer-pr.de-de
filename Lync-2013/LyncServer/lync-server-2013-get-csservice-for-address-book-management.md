---
title: 'Lync Server 2013: Get-CsService für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: Get-CsService für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Get-CsService for Address Book management
ms:assetid: 373b717d-5efa-4c36-a899-a23a5bd922b4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429698(v=OCS.15)
ms:contentKeyID: 48183853
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e46173429988d87022c13fab33e3778279dd0e9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427985"
---
# <a name="get-csservice-for-address-book-management-in-lync-server-2013"></a><span data-ttu-id="42edd-103">Get-CsService für die Verwaltung von Adressbüchern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42edd-103">Get-CsService for Address Book management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42edd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42edd-104">

<span> </span></span></span>

<span data-ttu-id="42edd-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="42edd-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="42edd-106">Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen autorisiert, das Get-CsService-Cmdlet lokal auszuführen: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span><span class="sxs-lookup"><span data-stu-id="42edd-106">Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsService cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.</span></span> <span data-ttu-id="42edd-107">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):</span><span class="sxs-lookup"><span data-stu-id="42edd-107">To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsService"}

<span data-ttu-id="42edd-108">Get-CsService ist wertvoll, um die aktuelle Konfiguration der definierten Web Services Ihrer Infrastruktur abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="42edd-108">Get-CsService is valuable to retrieve and display the current configuration of your infrastructure’s defined Web Services.</span></span> <span data-ttu-id="42edd-109">Wenn Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Pools und den Parameter Webserver definieren, gibt das Cmdlet die webbasierten Dienste zurück, die von Ihrem Server angeboten werden, einschließlich des Adressbuch Handlers und der Erweiterungs-URIs der Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="42edd-109">By defining the pool’s fully qualified domain name (FQDN) and the parameter WebServer, the cmdlet returns the web-based services offered by your server, including the Address Book handler and distribution list expansion URIs.</span></span>

<span data-ttu-id="42edd-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42edd-110">For example:</span></span>

    Get-CsService -PoolFqdn "fe01.contoso.net" -WebServer

<span data-ttu-id="42edd-111">Dieses Cmdlet gibt Folgendes zurück:</span><span class="sxs-lookup"><span data-stu-id="42edd-111">This cmdlet returns the following:</span></span>

<span data-ttu-id="42edd-112">Identität: Webserver:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="42edd-112">Identity : WebServer:pool01.contoso.net</span></span>

<span data-ttu-id="42edd-113">Filestore: Filestore:DC01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="42edd-113">FileStore : FileStore:dc01.contoso.net</span></span>

<span data-ttu-id="42edd-114">UserServer: UserServer:pool01. contoso. net</span><span class="sxs-lookup"><span data-stu-id="42edd-114">UserServer : UserServer:pool01.contoso.net</span></span>

<span data-ttu-id="42edd-115">PrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="42edd-115">PrimaryHttpPort : 80</span></span>

<span data-ttu-id="42edd-116">PrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="42edd-116">PrimaryHttpsPort : 443</span></span>

<span data-ttu-id="42edd-117">ExternalHttpPort: 8080</span><span class="sxs-lookup"><span data-stu-id="42edd-117">ExternalHttpPort : 8080</span></span>

<span data-ttu-id="42edd-118">ExternalHttpsPort: 4443</span><span class="sxs-lookup"><span data-stu-id="42edd-118">ExternalHttpsPort : 4443</span></span>

<span data-ttu-id="42edd-119">PublishedPrimaryHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="42edd-119">PublishedPrimaryHttpPort : 80</span></span>

<span data-ttu-id="42edd-120">PublishedPrimaryHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="42edd-120">PublishedPrimaryHttpsPort : 443</span></span>

<span data-ttu-id="42edd-121">PublishedExternalHttpPort: 80</span><span class="sxs-lookup"><span data-stu-id="42edd-121">PublishedExternalHttpPort : 80</span></span>

<span data-ttu-id="42edd-122">PublishedExternalHttpsPort: 443</span><span class="sxs-lookup"><span data-stu-id="42edd-122">PublishedExternalHttpsPort : 443</span></span>

<span data-ttu-id="42edd-123">ReachPrimaryPsomServerPort: 8060</span><span class="sxs-lookup"><span data-stu-id="42edd-123">ReachPrimaryPsomServerPort : 8060</span></span>

<span data-ttu-id="42edd-124">ReachExternalPsomServerPort: 8061</span><span class="sxs-lookup"><span data-stu-id="42edd-124">ReachExternalPsomServerPort : 8061</span></span>

<span data-ttu-id="42edd-125">AppSharingPortStart: 49152</span><span class="sxs-lookup"><span data-stu-id="42edd-125">AppSharingPortStart : 49152</span></span>

<span data-ttu-id="42edd-126">AppSharingPortCount: 16383</span><span class="sxs-lookup"><span data-stu-id="42edd-126">AppSharingPortCount : 16383</span></span>

<span data-ttu-id="42edd-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-127">LIServiceInternalUri : https://internalweb.contoso.net/locationinformation/liservice.svc</span></span>

<span data-ttu-id="42edd-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span><span class="sxs-lookup"><span data-stu-id="42edd-128">ABHandlerInternalUri : https://internalweb.contoso.net/abs/handler</span></span>

<span data-ttu-id="42edd-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span><span class="sxs-lookup"><span data-stu-id="42edd-129">ABHandlerExternalUri : https://csweb.contoso.com/abs/handler</span></span>

<span data-ttu-id="42edd-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-130">DLExpansionInternalUri : https://internalweb.contoso.net/groupexpansion/service.svc</span></span>

<span data-ttu-id="42edd-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-131">DLExpansionExternalUri : https://csweb.contoso.com/groupexpansion/service.svc</span></span>

<span data-ttu-id="42edd-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-132">CAHandlerInternalUri : https://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="42edd-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-133">CAHandlerInternalAnonUri : http://internalweb.contoso.net/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="42edd-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span><span class="sxs-lookup"><span data-stu-id="42edd-134">CollabContentInternalUri : https://internalweb.contoso.net/CollabContent</span></span>

<span data-ttu-id="42edd-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span><span class="sxs-lookup"><span data-stu-id="42edd-135">CollabContentExternalUri : https://csweb.contoso.com/CollabContent</span></span>

<span data-ttu-id="42edd-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-136">CAHandlerExternalUri : https://csweb.contoso.com/CertProv/CertProvisioningService.svc</span></span>

<span data-ttu-id="42edd-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="42edd-137">DeviceUpdateDownloadInternalUri : https://internalweb.contoso.net/RequestHandler/ucdevice.upx</span></span>

<span data-ttu-id="42edd-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span><span class="sxs-lookup"><span data-stu-id="42edd-138">DeviceUpdateDownloadExternalUri : https://csweb.contoso.com/RequestHandlerExt/ucdevice.upx</span></span>

<span data-ttu-id="42edd-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span><span class="sxs-lookup"><span data-stu-id="42edd-139">DeviceUpdateStoreInternalUri : http://internalweb.contoso.net/RequestHandler/Files</span></span>

<span data-ttu-id="42edd-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span><span class="sxs-lookup"><span data-stu-id="42edd-140">DeviceUpdateStoreExternalUri : https://csweb.contoso.com/RequestHandlerExt/Files</span></span>

<span data-ttu-id="42edd-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-141">RgsAgentServiceInternalUri : https://internalweb.contoso.net/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="42edd-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-142">RgsAgentServiceExternalUri : https://csweb.contoso.com/RgsClients/AgentService.svc</span></span>

<span data-ttu-id="42edd-143">MeetExternalUri : https://csweb.contoso.com/Meet</span><span class="sxs-lookup"><span data-stu-id="42edd-143">MeetExternalUri : https://csweb.contoso.com/Meet</span></span>

<span data-ttu-id="42edd-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span><span class="sxs-lookup"><span data-stu-id="42edd-144">DialinExternalUri : https://csweb.contoso.com/Dialin</span></span>

<span data-ttu-id="42edd-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span><span class="sxs-lookup"><span data-stu-id="42edd-145">CscpInternalUri : https://internalweb.contoso.net/Cscp</span></span>

<span data-ttu-id="42edd-146">ReachExternalUri : https://csweb.contoso.com/Reach</span><span class="sxs-lookup"><span data-stu-id="42edd-146">ReachExternalUri : https://csweb.contoso.com/Reach</span></span>

<span data-ttu-id="42edd-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span><span class="sxs-lookup"><span data-stu-id="42edd-147">ReachInternalUri : https://internalweb.contoso.net/Reach</span></span>

<span data-ttu-id="42edd-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-148">WebTicketExternalUri : https://csweb.contoso.com/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="42edd-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="42edd-149">WebTicketInternalUri : https://internalweb.contoso.net/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="42edd-150">ExternalFqdn: csweb.contoso.com</span><span class="sxs-lookup"><span data-stu-id="42edd-150">ExternalFqdn : csweb.contoso.com</span></span>

<span data-ttu-id="42edd-151">InternalFqdn: internalweb.contoso.net</span><span class="sxs-lookup"><span data-stu-id="42edd-151">InternalFqdn : internalweb.contoso.net</span></span>

<span data-ttu-id="42edd-152">DependentServiceList: {Registrar:pool01. contoso. net, ConferencingServer:pool01. contoso. net}</span><span class="sxs-lookup"><span data-stu-id="42edd-152">DependentServiceList : {Registrar:pool01.contoso.net, ConferencingServer:pool01.contoso.net}</span></span>

<span data-ttu-id="42edd-153">Service-Nr: 1-Webdienste-1</span><span class="sxs-lookup"><span data-stu-id="42edd-153">ServiceId : 1-WebServices-1</span></span>

<span data-ttu-id="42edd-154">Website-Nr: Website: Redmond</span><span class="sxs-lookup"><span data-stu-id="42edd-154">SiteId : Site:Redmond</span></span>

<span data-ttu-id="42edd-155">PoolFqdn: pool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="42edd-155">PoolFqdn : pool01.contoso.net</span></span>

<span data-ttu-id="42edd-156">Version: 5</span><span class="sxs-lookup"><span data-stu-id="42edd-156">Version : 5</span></span>

<span data-ttu-id="42edd-157">Rolle: Webserver</span><span class="sxs-lookup"><span data-stu-id="42edd-157">Role : WebServer</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="42edd-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42edd-158">See Also</span></span>


[<span data-ttu-id="42edd-159">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="42edd-159">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
  

<span data-ttu-id="42edd-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42edd-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

