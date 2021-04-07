---
title: 'Lync Server 2013: Planen von Hybridbereitstellungen'
description: 'Lync Server 2013: Planen von Hybridbereitstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424548"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a><span data-ttu-id="efa1e-103">Planen von Lync Server 2013-Hybridbereitstellungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-103">Planning for Lync Server 2013 hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efa1e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efa1e-104">

<span> </span></span></span>

<span data-ttu-id="efa1e-105">_**Thema Zuletzt geändert:** 25.05.2016_</span><span class="sxs-lookup"><span data-stu-id="efa1e-105">_**Topic Last Modified:** 2016-05-25_</span></span>

<span data-ttu-id="efa1e-106">Bei der Planung einer Hybridbereitstellung sollten Sie die folgenden Anforderungen für Benutzer und Ihre Netzwerkinfrastruktur berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-106">You should consider the following requirements for users and your network infrastructure while planning for a hybrid deployment.</span></span>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="efa1e-107">Infrastrukturanforderungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-107">Infrastructure Requirements</span></span>

<span data-ttu-id="efa1e-108">Sie müssen folgendes in Ihrer Umgebung konfiguriert haben, um eine Hybridbereitstellung implementieren und bereitstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="efa1e-108">You must have the following configured in your environment in order to implement and deploy a hybrid deployment.</span></span>

  - <span data-ttu-id="efa1e-109">Eine Microsoft 365- oder Office 365-Organisation mit aktivierter Skype for Business Online-Funktion.</span><span class="sxs-lookup"><span data-stu-id="efa1e-109">A Microsoft 365 or Office 365 organization with Skype for Business Online enabled.</span></span> <span data-ttu-id="efa1e-110">Beachten Sie, dass Sie bei ihrer lokalen Bereitstellung nur einen einzigen Mandanten für eine Hybridkonfiguration verwenden können.</span><span class="sxs-lookup"><span data-stu-id="efa1e-110">Note that you can use only a single tenant for a hybrid configuration with your on-premises deployment.</span></span>

  - <span data-ttu-id="efa1e-111">Eine einzelne lokale Bereitstellung (Infrastruktur) von Skype for Business Server oder Lync Server, die in einer unterstützten Topologie bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-111">A single on-premises deployment (infrastructure) of Skype for Business Server or Lync Server that is deployed in a supported topology.</span></span> <span data-ttu-id="efa1e-112">Siehe Topologieanforderungen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-112">See Topology Requirements.</span></span>
    
    <span data-ttu-id="efa1e-113">Informationen zum Konfigurieren Ihrer Lync Server 2013- oder Lync Server 2010-Bereitstellung für hybride Bereitstellungen finden Sie unter Konfigurieren von [Lync Server 2013-Hybridbereitstellungen.](lync-server-2013-configuring-hybrid-deployments.md)</span><span class="sxs-lookup"><span data-stu-id="efa1e-113">For information about configuring your Lync Server 2013 or Lync Server 2010 deployment for hybrid, see [Configuring Lync Server 2013 hybrid deployments](lync-server-2013-configuring-hybrid-deployments.md).</span></span>

  - <span data-ttu-id="efa1e-114">Skype for Business Server 2015-Verwaltungstools.</span><span class="sxs-lookup"><span data-stu-id="efa1e-114">Skype for Business Server 2015 administrative tools.</span></span> <span data-ttu-id="efa1e-115">Wenn Sie Lync Server 2013 oder Lync Server 2010 verwenden, können Sie die Lync Server 2013-Verwaltungstools verwenden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-115">If you are using Lync Server 2013 or Lync Server 2010, you can use the Lync Server 2013 administrative tools.</span></span>

  - <span data-ttu-id="efa1e-116">Wenn Sie einmaliges Anmelden mit Microsoft 365 oder Office 365 unterstützen möchten, damit Benutzer dieselben Anmeldeinformationen für die Anmeldung bei Office verwenden können wie lokal, können Sie die Kennwortsynchronisierungsfunktionen von Azure Active Directory (AAD) Connect verwenden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-116">To support Single Sign-on with Microsoft 365 or Office 365 so that users can use the same login credentials for signing in to Office as they do on-premises, you can use the password sync features of Azure Active Directory (AAD) Connect.</span></span> <span data-ttu-id="efa1e-117">Sie können Active Directory Federation Services (AD FS) auch zum einmaligen Anmelden mit Microsoft 365 oder Office 365 verwenden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-117">You can also use Active Directory Federation Services (AD FS) for single sign-on with Microsoft 365 or Office 365.</span></span>
    
    <span data-ttu-id="efa1e-118">Weitere Informationen finden Sie unter [Integrieren Ihrer lokalen Identitäten in Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)</span><span class="sxs-lookup"><span data-stu-id="efa1e-118">For more information, see [Integrating your on-premises identities with Azure Active Directory](https://go.microsoft.com/fwlink/p/?linkid=619754).</span></span>

  - <span data-ttu-id="efa1e-119">Eine Lösung für die Verzeichnissynchronisierung, um ihre lokalen und Online-Active Directory-Objekte zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="efa1e-119">A single directory synchronization solution to keep your on-premises and online Active Directory objects synchronized.</span></span> <span data-ttu-id="efa1e-120">Details zur Verzeichnissynchronisierung finden Sie unter [Verzeichnisintegrationstools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span><span class="sxs-lookup"><span data-stu-id="efa1e-120">For details about Directory Synchronization, see [Directory Integration Tools](https://go.microsoft.com/fwlink/p/?linkid=530320).</span></span>

</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="efa1e-121">Lync-Clientsupport</span><span class="sxs-lookup"><span data-stu-id="efa1e-121">Lync Client Support</span></span>

<span data-ttu-id="efa1e-122">Es gibt einige Unterschiede bei den features, die in Lync-Clients unterstützt werden, sowie bei den Features, die in lokalen und Onlineumgebungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="efa1e-122">There are some differences in the features supported in Lync clients, as well as the features available in on-premises and online environments.</span></span> <span data-ttu-id="efa1e-123">Bevor Sie entscheiden, wo Benutzer in Ihrer Organisation zu Hause sein möchten, können Sie den Clientsupport für die verschiedenen Konfigurationen von Lync Server anzeigen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-123">Before you decide where you want to home users in your organization, you can view the client support for the various configurations of Lync Server.</span></span> <span data-ttu-id="efa1e-124">Die folgenden Clients werden von Skype for Business Online in einer Lync-Hybridbereitstellung unterstützt:</span><span class="sxs-lookup"><span data-stu-id="efa1e-124">The following clients are supported with Skype for Business Online in a Lync hybrid deployment:</span></span>

  - <span data-ttu-id="efa1e-125">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="efa1e-125">Lync 2010</span></span>

  - <span data-ttu-id="efa1e-126">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="efa1e-126">Lync 2013</span></span>

  - <span data-ttu-id="efa1e-127">Windows Store-App für Lync</span><span class="sxs-lookup"><span data-stu-id="efa1e-127">Lync Windows Store app</span></span>

  - <span data-ttu-id="efa1e-128">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="efa1e-128">Lync Web App</span></span>

  - <span data-ttu-id="efa1e-129">Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="efa1e-129">Lync Mobile</span></span>

  - <span data-ttu-id="efa1e-130">Lync für Mac 2011</span><span class="sxs-lookup"><span data-stu-id="efa1e-130">Lync for Mac 2011</span></span>

  - <span data-ttu-id="efa1e-131">Lync Room System</span><span class="sxs-lookup"><span data-stu-id="efa1e-131">Lync Room System</span></span>

  - <span data-ttu-id="efa1e-132">Lync Basic 2013</span><span class="sxs-lookup"><span data-stu-id="efa1e-132">Lync Basic 2013</span></span>

<span data-ttu-id="efa1e-133">Details zum Clientsupport finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="efa1e-133">For details about client support, see the following topics:</span></span>

  - [<span data-ttu-id="efa1e-134">Clients für Lync Online</span><span class="sxs-lookup"><span data-stu-id="efa1e-134">Clients for Lync Online</span></span>](https://go.microsoft.com/fwlink/?linkid=281902)

  - [<span data-ttu-id="efa1e-135">Clientvergleichstabellen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efa1e-135">Client comparison tables for Lync Server 2013</span></span>](lync-server-2013-desktop-client-comparison-tables.md)

  - [<span data-ttu-id="efa1e-136">Vergleichstabellen für mobile Clients für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efa1e-136">Mobile client comparison tables for Lync Server 2013</span></span>](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a><span data-ttu-id="efa1e-137">Anforderungen im Hinblick auf die Topologie</span><span class="sxs-lookup"><span data-stu-id="efa1e-137">Topology Requirements</span></span>

<span data-ttu-id="efa1e-138">Um Ihre Bereitstellung für die Hybridbereitstellung mit Skype for Business Online zu konfigurieren, benötigen Sie eine der folgenden unterstützten Topologien:</span><span class="sxs-lookup"><span data-stu-id="efa1e-138">To configure your deployment for hybrid with Skype for Business Online, you need to have one of the following supported topologies:</span></span>

  - <span data-ttu-id="efa1e-139">Eine Skype for Business Server 2015-Bereitstellung mit allen Servern, auf denen Skype for Business Server 2015 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-139">A Skype for Business Server 2015 deployment with all servers running Skype for Business Server 2015.</span></span>

  - <span data-ttu-id="efa1e-140">Eine Lync Server 2013-Bereitstellung mit allen Servern, auf denen Lync Server 2013 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-140">A Lync Server 2013 deployment with all servers running Lync Server 2013.</span></span>

  - <span data-ttu-id="efa1e-141">Eine Lync Server 2010-Bereitstellung mit allen Servern, auf denen Lync Server 2010 ausgeführt wird, mit den neuesten kumulativen Updates.</span><span class="sxs-lookup"><span data-stu-id="efa1e-141">A Lync Server 2010 deployment with all servers running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="efa1e-142">Der Edgeserver des Verbunds und der Server des nächsten Hops vom Edgeserver des Verbunds müssen Lync Server 2010 mit den neuesten kumulativen Updates ausführen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-142">The federation Edge Server and next hop server from the federation Edge Server must be running Lync Server 2010 with the latest cumulative updates.</span></span>
    
      - <span data-ttu-id="efa1e-143">Die Verwaltungstools für Skype for Business Server 2015 oder Lync Server 2013 müssen auf mindestens einem Server oder einer Verwaltungsarbeitsstation installiert sein.</span><span class="sxs-lookup"><span data-stu-id="efa1e-143">The Skype for Business Server 2015 or Lync Server 2013 Administrative Tools must be installed on at least one server or management workstation.</span></span>

  - <span data-ttu-id="efa1e-144">Eine gemischte Bereitstellung von Lync Server 2013 und Skype for Business Server 2015 mit den folgenden Serverrollen auf mindestens einer Website, auf der Skype for Business Server 2015 ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="efa1e-144">A mixed Lync Server 2013 and Skype for Business Server 2015 deployment with the following server roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="efa1e-145">Mindestens ein Enterprise-Pool- oder Standard Edition-Server </span><span class="sxs-lookup"><span data-stu-id="efa1e-145">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="efa1e-146">Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="efa1e-146">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="efa1e-147">Der dem SIP-Partnerverbund zugeordnete Edgepool</span><span class="sxs-lookup"><span data-stu-id="efa1e-147">The Edge Pool associated with SIP federation</span></span>

  - <span data-ttu-id="efa1e-148">Eine gemischte Bereitstellung von Lync Server 2010 und Skype for Business Server 2015 mit den folgenden Serverrollen auf mindestens einer Website, auf der Skype for Business Server 2015 ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="efa1e-148">A mixed Lync Server 2010 and Skype for Business Server 2015 deployment with the following servers roles in at least one site running Skype for Business Server 2015:</span></span>
    
      - <span data-ttu-id="efa1e-149">Mindestens ein Enterprise-Pool- oder Standard Edition-Server </span><span class="sxs-lookup"><span data-stu-id="efa1e-149">At least one Enterprise Pool or Standard Edition server</span></span>
    
      - <span data-ttu-id="efa1e-150">Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls vorhanden</span><span class="sxs-lookup"><span data-stu-id="efa1e-150">The Director Pool associated with SIP federation, if it exists</span></span>
    
      - <span data-ttu-id="efa1e-151">Der dem SIP-Partnerverbund zugeordnete Edgepool für den Standort</span><span class="sxs-lookup"><span data-stu-id="efa1e-151">The Edge Pool associated with SIP federation for the Site</span></span>

  - <span data-ttu-id="efa1e-152">Eine gemischte Lync Server 2010- und Lync Server 2013-Bereitstellung mit den folgenden Serverrollen auf mindestens einer Website, auf der Lync Server 2013 ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="efa1e-152">A mixed Lync Server 2010 and Lync Server 2013 deployment with the following server roles in at least one site running Lync Server 2013:</span></span>
    
      - <span data-ttu-id="efa1e-153">Mindestens ein Enterprise-Pool- oder Standard Edition-Server am Standort</span><span class="sxs-lookup"><span data-stu-id="efa1e-153">At least one Enterprise Pool or Standard Edition server in the site</span></span>
    
      - <span data-ttu-id="efa1e-154">Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls am Standort vorhanden</span><span class="sxs-lookup"><span data-stu-id="efa1e-154">The Director Pool associated with SIP federation, if it exists in the site</span></span>
    
      - <span data-ttu-id="efa1e-155">Der dem SIP-Partnerverbund zugeordnete Edgepool für den Standort</span><span class="sxs-lookup"><span data-stu-id="efa1e-155">The Edge Pool associated with SIP federation for the site</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="efa1e-156">Alle Benutzerverwaltungen, einschließlich der Benutzerbewegungen zwischen lokal und UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, müssen mit der neuesten installierten Version der Verwaltungstools durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-156">All user management, including user moves between on-premises and UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, needs to be done using the latest installed version of the administrative tools.</span></span> <span data-ttu-id="efa1e-157">Die Verwaltungstools müssen auf einem separaten Server installiert sein, der den Zugriff auf die vorhandene lokale Bereitstellung und das Internet verbindet.</span><span class="sxs-lookup"><span data-stu-id="efa1e-157">The administrative tools must be installed on a separate server that has connect access to the existing on-premises deployment and to the Internet.</span></span> <span data-ttu-id="efa1e-158">Das <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Cmdlet "Move-CsUser",</A> um Benutzer von Ihrer lokalen Bereitstellung in UNRESOLVED_TOKEN_VAL(skype16_online) zu verschieben, muss über die verwaltungstechnischen Tools ausgeführt werden, die mit Ihrer lokalen Bereitstellung verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="efa1e-158">The <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Move-CsUser</A> cmdlet to move users from your on-premises deployment to UNRESOLVED_TOKEN_VAL(skype16_online) must be run from the administrative tools connected to your on-premises deployment.</span></span>



</div>

<span data-ttu-id="efa1e-159">Weitere Informationen zu unterstützten Topologien finden Sie unter Unterstützte [Topologien in Lync Server 2013](lync-server-2013-supported-topologies.md)und [Lync Server 2013 Referenztopologien für Hybridbereitstellungen](https://go.microsoft.com/fwlink/p/?linkid=398709)in Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-159">For more information about supported topologies, see [Supported topologies in Lync Server 2013](lync-server-2013-supported-topologies.md), and [Lync Server 2013 Reference Topologies for Enterprise Hybrid Deployments](https://go.microsoft.com/fwlink/p/?linkid=398709).</span></span>

<span data-ttu-id="efa1e-160">Informationen zur Problembehandlung zu Hybridbereitstellungen und zum Verbinden von PowerShell mit Lync Online finden Sie unter [Lync Online: Lync PowerShell und Hybrid troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span><span class="sxs-lookup"><span data-stu-id="efa1e-160">For troubleshooting information about hybrid deployments and connecting PowerShell to Lync Online, see [Lync Online: Lync PowerShell and Hybrid Troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).</span></span>

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a><span data-ttu-id="efa1e-161">Anforderungen für "Verbund zugelassene/blockierte Listen"</span><span class="sxs-lookup"><span data-stu-id="efa1e-161">Requirements for Federation Allowed/Blocked Lists</span></span>

<span data-ttu-id="efa1e-p108">Die Liste der zugelassenen Domänen enthält Domänen, für die ein Partner-Edge-FQDN (vollqualifizierter Domänenname) konfiguriert ist. Diese werden mitunter als *zulässige Partnerserver* oder *direkte Verbundpartner* bezeichnet. Sie sollten mit dem Unterschied zwischen einem öffentlichen Partnerverbund und einem geschlossenen Partnerverbund vertraut sein, der in lokalen Bereitstellungen als *Partnerermittlung* bzw. *Liste der zulässigen Partnerdomänen* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-p108">The Allowed domains list includes domains that have a partner Edge fully qualified domain name (FQDN) configured. These are sometimes referred to as *allowed partner servers* or *direct federation partners*. You should be familiar with the difference between Open Federation and Closed Federation, referred to as *partner discovery* and *allowed partner domain list*, respectively, in on-premises deployments.</span></span>

<span data-ttu-id="efa1e-165">Die folgenden Anforderungen müssen erfüllt sein, um eine Hybridbereitstellung erfolgreich zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="efa1e-165">The following requirements must be met to successfully configure a hybrid deployment:</span></span>

  - <span data-ttu-id="efa1e-166">Der Domänenabgleich muss für Ihre lokale Bereitstellung und Ihre Microsoft 365- oder Office 365-Organisation identisch konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="efa1e-166">Domain matching must be configured the same for your on-premises deployment and your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="efa1e-167">Wenn die Partnerermittlung für die lokale Bereitstellung aktiviert ist, muss der öffentliche Partnerverbund für den Onlinemandaten konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="efa1e-167">If partner discovery is enabled on the on-premises deployment, then open federation must be configured for your online tenant.</span></span> <span data-ttu-id="efa1e-168">Wenn die Partnerermittlung nicht aktiviert ist, muss für den Onlinemandanten der geschlossene Partnerverbund konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="efa1e-168">If partner discovery is not enabled, then closed federation must be configured for your online tenant.</span></span>

  - <span data-ttu-id="efa1e-169">Die Liste der blockierten Domänen in der lokalen Bereitstellung muss genau mit der Liste der blockierten Domänen für den Onlinemandanten übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-169">The Blocked domains list in the on-premises deployment must exactly match the Blocked domains list for your online tenant.</span></span>

  - <span data-ttu-id="efa1e-170">Die Liste der zugelassenen Domänen in der lokalen Bereitstellung muss genau mit der Liste der zugelassenen Domänen für den Onlinemandanten übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-170">The Allowed domains list in the on-premises deployment must exactly match the Allowed domains list for your online tenant.</span></span>

  - <span data-ttu-id="efa1e-171">Der Verbund muss für die externe Kommunikation für den Online-Mandanten aktiviert sein, die mithilfe der Lync Online-Systemsteuerung konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-171">Federation must be enabled for the external communications for the online tenant, which is configured by using the Lync Online Control Panel.</span></span>

</div>

<div>

## <a name="dns-settings"></a><span data-ttu-id="efa1e-172">DNS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-172">DNS Settings</span></span>

<span data-ttu-id="efa1e-173">Beim Erstellen von DNS-Einträgen für Hybridbereitstellungen sollten alle externen Lync-DNS-Einträge auf die lokale Infrastruktur verweisen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-173">When creating DNS records for hybrid deployments, all Lync external DNS records should point to the on-premises infrastructure.</span></span> <span data-ttu-id="efa1e-174">Details zu den erforderlichen DNS-Einträgen finden Sie unter [Domänennamensystemanforderungen für Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="efa1e-174">For details on required DNS records, please refer to [Domain Name System (DNS) requirements for Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).</span></span>

<span data-ttu-id="efa1e-175">Darüber hinaus müssen Sie sicherstellen, dass die in der folgenden Tabelle erläuterte DNS-Auflösung in Ihrer lokalen Bereitstellung funktioniert:</span><span class="sxs-lookup"><span data-stu-id="efa1e-175">Additionally you need to ensure that the DNS resolution described in the following table works in your on-premises deployment:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-176">DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="efa1e-176">DNS record</span></span></p></td>
<td><p><span data-ttu-id="efa1e-177">Aufzulösen durch</span><span class="sxs-lookup"><span data-stu-id="efa1e-177">Resolvable by</span></span></p></td>
<td><p><span data-ttu-id="efa1e-178">DNS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="efa1e-178">DNS requirement</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efa1e-179">DNS SRV-Eintrag für _sipfederationtls._tcp. &lt; sipdomain.com &gt; für alle unterstützten SIP-Domänen, die auf externe ACCESS Edge-IP(n) aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="efa1e-179">DNS SRV record for _sipfederationtls._tcp.&lt;sipdomain.com&gt; for all supported SIP domains resolving to Access Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="efa1e-180">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="efa1e-180">Edge server(s)</span></span></p></td>
<td><p><span data-ttu-id="efa1e-p111">Aktivieren Sie Partnerverbundkommunikation in einer Hybridkonfiguration. Der Edgeserver muss wissen, wohin der Datenverkehr im Partnerverbund für die zwischen lokal und online aufgeteilte SIP-Domäne geleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efa1e-p111">Enable federated communication in a hybrid configuration. The Edge Server needs to know where to route federated traffic for the SIP domain that is split between on premises and online.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-183">DNS-A-Eintrag/Einträge für den Edge-Webkonferenzdienst-FQDN, zum Beispiel „webcon.contoso.com“, aufgelöst zu der externen IP/den IPs des Webkonferenzdienst-Edgeservers</span><span class="sxs-lookup"><span data-stu-id="efa1e-183">DNS A record(s) for Edge Web Conferencing Service FQDN, e.g. webcon.contoso.com resolving to Web Conferencing Edge external IP(s)</span></span></p></td>
<td><p><span data-ttu-id="efa1e-184">Über internes Unternehmensnetzwerk verbundene Benutzercomputer</span><span class="sxs-lookup"><span data-stu-id="efa1e-184">Internal corporate network connected users’ computers</span></span></p></td>
<td><p><span data-ttu-id="efa1e-p112">Versetzen Sie Onlinebenutzer in die Lage, in lokal gehosteten Besprechungen Inhalte zu präsentieren oder zu betrachten. Entsprechende Inhalte sind unter anderem PowerPoint-Dateien, Whiteboards, Umfragen und freigegebene Notizen. </span><span class="sxs-lookup"><span data-stu-id="efa1e-p112">Enable online users to present or view content in on-premises hosted meetings. Content includes PowerPoint files, whiteboards, polls, and shared notes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="efa1e-187">Je nachdem, wie DNS in Ihrer Organisation konfiguriert ist, müssen Sie möglicherweise der intern gehosteten DNS-Zone für die entsprechenden SIP-Domäne(n) diese Einträge hinzufügen, um die interne DNS-Auflösung dieser Datensätze zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="efa1e-187">Depending on how DNS is configured in your organization, you may need to add these records to the internal hosted DNS zone for the corresponding SIP domain(s) to provide internal DNS resolution to these records.</span></span>

</div>

<div>

## <a name="firewall-considerations"></a><span data-ttu-id="efa1e-188">Überlegungen zur Firewall</span><span class="sxs-lookup"><span data-stu-id="efa1e-188">Firewall Considerations</span></span>

<span data-ttu-id="efa1e-p113">Die Computer in Ihrem Netzwerk müssen Standard-Internet-DNS-Lookups ausführen können. Wenn diese Computer Standard-Internetwebsites erreichen können, erfüllt Ihr Netzwerk diese Anforderung.</span><span class="sxs-lookup"><span data-stu-id="efa1e-p113">Computers on your network must be able to perform standard Internet DNS lookups. If these computers can reach standard Internet sites, your network meets this requirement.</span></span>

<span data-ttu-id="efa1e-191">Je nach Standort ihres Microsoft Online Services-Rechenzentrums müssen Sie auch Ihre Netzwerkfirewallgeräte so konfigurieren, dass Verbindungen auf Der Grundlage von Platzhalterdomänennamen (z. B. der datenverkehr von \* .outlook.com) akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-191">Depending on the location of your Microsoft Online Services data center, you must also configure your network firewall devices to accept connections based on wildcard domain names (for example, all traffic from \*.outlook.com).</span></span> <span data-ttu-id="efa1e-192">Wenn die Firewalls Ihrer Organisation Konfigurationen mit Platzhalternamen nicht unterstützen, müssen Sie die IP-Adressbereiche, die Sie zulassen möchten, und die angegebenen Ports manuell festlegen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-192">If your organization’s firewalls do not support wildcard name configurations, you will have to manually determine the IP address ranges that you would like to allow and the specified ports.</span></span>

<span data-ttu-id="efa1e-193">Lesen Sie das Hilfethema [Office 365-URLs und IP-Adressbereiche.](https://go.microsoft.com/fwlink/p/?linkid=252942)</span><span class="sxs-lookup"><span data-stu-id="efa1e-193">Refer to the Help topic [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=252942).</span></span>

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a><span data-ttu-id="efa1e-194">Port- und Protokollanforderungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-194">Port and Protocol Requirements</span></span>

<span data-ttu-id="efa1e-195">Zusätzlich zu den Portanforderungen für die interne Lync Server 2013-Kommunikation müssen Sie auch die folgenden Ports konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="efa1e-195">In addition to the port requirements for internal Lync Server 2013 communication, you must also configure the following ports.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efa1e-196">Protokoll/Port</span><span class="sxs-lookup"><span data-stu-id="efa1e-196">Protocol / Port</span></span></th>
<th><span data-ttu-id="efa1e-197">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-197">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-198">TCP 443</span><span class="sxs-lookup"><span data-stu-id="efa1e-198">TCP 443</span></span></p></td>
<td><p><span data-ttu-id="efa1e-199">Eingehendes Öffnen</span><span class="sxs-lookup"><span data-stu-id="efa1e-199">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="efa1e-200">Active Directory Federation Services (Verbundserverrolle)</span><span class="sxs-lookup"><span data-stu-id="efa1e-200">Active Directory Federation Services (federation server role)</span></span></p>
<p><span data-ttu-id="efa1e-201">Weitere Informationen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Grundlegendes zu AD FS Role Services</a>.</span><span class="sxs-lookup"><span data-stu-id="efa1e-201">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Understanding AD FS Role Services</a>.</span></span></p></li>
<li><p><span data-ttu-id="efa1e-202">Active Directory Federation Services (Proxyserverrolle)</span><span class="sxs-lookup"><span data-stu-id="efa1e-202">Active Directory Federation Services (proxy server role)</span></span></p></li>
<li><p><span data-ttu-id="efa1e-203">Microsoft Online Services Portal</span><span class="sxs-lookup"><span data-stu-id="efa1e-203">Microsoft Online Services Portal</span></span></p></li>
<li><p><span data-ttu-id="efa1e-204">Mein Unternehmensportal</span><span class="sxs-lookup"><span data-stu-id="efa1e-204">My Company Portal</span></span></p></li>
<li><p><span data-ttu-id="efa1e-205">Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="efa1e-205">Outlook Web App</span></span></p></li>
<li><p><span data-ttu-id="efa1e-206">Lync-Client (Kommunikation mit Lync Online vom lokalen Lync Server)</span><span class="sxs-lookup"><span data-stu-id="efa1e-206">Lync client (communication to Lync Online from on-premises Lync Server)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efa1e-207">TCP 80 und 443</span><span class="sxs-lookup"><span data-stu-id="efa1e-207">TCP 80 and 443</span></span></p></td>
<td><p><span data-ttu-id="efa1e-208">Eingehendes Öffnen</span><span class="sxs-lookup"><span data-stu-id="efa1e-208">Open inbound</span></span></p>
<ul>
<li><p><span data-ttu-id="efa1e-209">Microsoft Online Services-Verzeichnissynchronisierungstool</span><span class="sxs-lookup"><span data-stu-id="efa1e-209">Microsoft Online Services Directory Synchronization Tool</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-210">TCP 5061</span><span class="sxs-lookup"><span data-stu-id="efa1e-210">TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="efa1e-211">Öffnen von Ein-/Ausgehend auf dem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="efa1e-211">Open inbound/outbound on the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efa1e-212">PSOM/TLS 443</span><span class="sxs-lookup"><span data-stu-id="efa1e-212">PSOM/TLS 443</span></span></p></td>
<td><p><span data-ttu-id="efa1e-213">Öffnen von Ein-/Ausgehend für Datenfreigabesitzungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-213">Open inbound/outbound for data sharing sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-214">STUN/TCP 443</span><span class="sxs-lookup"><span data-stu-id="efa1e-214">STUN/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="efa1e-215">Öffnen von eingehenden/ausgehenden Audio-, Video- und Anwendungsfreigabesitzungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-215">Open inbound/outbound for audio, video, application sharing sessions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efa1e-216">STUN/UDP 3478</span><span class="sxs-lookup"><span data-stu-id="efa1e-216">STUN/UDP 3478</span></span></p></td>
<td><p><span data-ttu-id="efa1e-217">Öffnen von Ein-/Ausgehend für Audio- und Videositzungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-217">Open inbound/outbound for audio and video sessions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efa1e-218">RTP/TCP 50000-59999</span><span class="sxs-lookup"><span data-stu-id="efa1e-218">RTP/TCP 50000-59999</span></span></p></td>
<td><p><span data-ttu-id="efa1e-219">Ausgehendes Öffnen für Audio- und Videositzungen</span><span class="sxs-lookup"><span data-stu-id="efa1e-219">Open outbound for audio and video sessions</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a><span data-ttu-id="efa1e-220">Benutzerkonten und Daten</span><span class="sxs-lookup"><span data-stu-id="efa1e-220">User Accounts and Data</span></span>

<span data-ttu-id="efa1e-221">In einer Lync Server 2013-Hybridbereitstellung muss jeder Benutzer, den Sie in Lync Online zu Hause haben möchten, zuerst in der lokalen Bereitstellung erstellt werden, damit das Benutzerkonto in Active Directory Domain Services erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-221">In a Lync Server 2013 hybrid deployment, any user that you want to home in Lync Online must first be created in the on-premises deployment, so that the user account is created in Active Directory Domain Services.</span></span> <span data-ttu-id="efa1e-222">Sie können den Benutzer dann zu Skype for Business Online verschieben, wodurch die Kontaktliste des Benutzers bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-222">You can then move the user to Skype for Business Online, which will move the user’s contact list.</span></span>

<span data-ttu-id="efa1e-223">Wenn Sie Benutzerkonten zwischen Ihren lokalen Lync- und Lync Online-Bereitstellungen mit AD FS und Dirsync synchronisieren, müssen Sie die AD-Konten für alle Lync-Benutzer in Ihrer Organisation zwischen Ihren lokalen und Online-Lync-Bereitstellungen synchronisieren, auch wenn Benutzer nicht nach Lync Online verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-223">When you synchronize user accounts between your Lync on-premises and Lync Online deployments with AD FS and Dirsync, you need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="efa1e-224">Wenn Sie nicht alle Benutzer synchronisieren, funktioniert die Kommunikation zwischen lokalen und Onlinebenutzern in Ihrem Unternehmen möglicherweise nicht erwartungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="efa1e-224">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="efa1e-225">Wenn der Benutzer mithilfe des Onlineportals für Microsoft 365 Admin Center erstellt wird, wird das Benutzerkonto nicht mit lokalem Active Directory synchronisiert, und der Benutzer ist im lokalen Active Directory nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-225">If the user is created by using the online portal for Microsoft 365 admin center, the user account will not be synchronized with on-premises Active Directory, and the user will not exist in the on-premises Active Directory.</span></span> <span data-ttu-id="efa1e-226">Wenn Sie bereits Benutzer in Lync Online erstellt haben und eine Hybridlösung mit einem lokalen Lync Server konfigurieren möchten, lesen Sie Verschieben von Benutzern von Lync Online zu Lync lokal <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">in Lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="efa1e-226">If you have already created users in Lync Online, and want to configure hybrid with an on-premises Lync Server, see <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">Moving users from Lync Online to Lync on-premises in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="efa1e-227">Sie sollten bei der Planung einer Hybridbereitstellung auch die folgenden benutzerbezogenen Aspekte berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="efa1e-227">You should also consider the following user-related issues when planning for a hybrid deployment.</span></span>

  - <span data-ttu-id="efa1e-228">**Benutzerkontakte**   Der Grenzwert für Kontakte für Lync Online-Benutzer beträgt 250.</span><span class="sxs-lookup"><span data-stu-id="efa1e-228">**User contacts**   The limit for contacts for Lync Online users is 250.</span></span> <span data-ttu-id="efa1e-229">Alle darüber hinausgehenden Kontakte werden aus der Kontaktliste des Benutzers entfernt, wenn das Konto nach Lync Online verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="efa1e-229">Any contacts beyond that number will be removed from the user’s contact list when the account is moved to Lync Online.</span></span>

  - <span data-ttu-id="efa1e-230">**Chat und Anwesenheit**   Benutzerkontaktlisten, Benutzergruppen und Zugriffssteuerungslisten (ACLs) werden mit dem Benutzerkonto migriert.</span><span class="sxs-lookup"><span data-stu-id="efa1e-230">**Instant Messaging and Presence**   User contact lists, groups, and access control lists (ACLs) are migrated with the user account.</span></span>

  - <span data-ttu-id="efa1e-231">**Konferenzdaten, Besprechungsinhalte und geplante Besprechungen**   Dieser Inhalt wird nicht mit dem Benutzerkonto migriert.</span><span class="sxs-lookup"><span data-stu-id="efa1e-231">**Conferencing data, meeting content, and scheduled meetings**   This content is not migrated with the user account.</span></span> <span data-ttu-id="efa1e-232">Benutzer müssen Besprechungen neu planen, nachdem ihre Konten zu Lync Online migriert wurden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-232">Users must reschedule meetings after their accounts are migrated to Lync Online.</span></span>

</div>

<div>

## <a name="user-policies-and-features"></a><span data-ttu-id="efa1e-233">Benutzerrichtlinien und -features</span><span class="sxs-lookup"><span data-stu-id="efa1e-233">User Policies and Features</span></span>

  - <span data-ttu-id="efa1e-234">In einer Lync Server 2013-Hybridumgebung können Benutzer für Chatnachrichten, Sprachnachrichten und Besprechungen lokal oder online aktiviert werden, jedoch nicht beide gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="efa1e-234">In a Lync Server 2013 hybrid environment, users can be enabled for Instant Messaging, voice, and meetings either on-premises or online, but not both simultaneously.</span></span>

  - <span data-ttu-id="efa1e-235">**Lync-Client**    Einige Benutzer benötigen möglicherweise eine neue Clientversion, wenn sie nach Lync Online verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-235">**Lync Client**    Some users may require a new client version when they are moved to Lync Online.</span></span> <span data-ttu-id="efa1e-236">Bei Office Communications Server 2007 R2 müssen Benutzer vor der Migration zu Lync Online in einen Lync Server 2013-Pool verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="efa1e-236">For Office Communications Server 2007 R2, users must be moved to a Lync Server 2013 pool prior to migration to Lync Online.</span></span>
    
    <span data-ttu-id="efa1e-237">Weitere Informationen zur Clientunterstützung finden Sie unter [Clients für Lync Online-](https://go.microsoft.com/fwlink/p/?linkid=281902) und [Unterstützte Lync-Clients und Netzwerkportkonfigurationen.](https://go.microsoft.com/fwlink/p/?linkid=281901)</span><span class="sxs-lookup"><span data-stu-id="efa1e-237">For more information about client support, see [Clients for Lync Online](https://go.microsoft.com/fwlink/p/?linkid=281902) and [Supported Lync clients and network port configurations](https://go.microsoft.com/fwlink/p/?linkid=281901).</span></span>

  - <span data-ttu-id="efa1e-238">**Lokale Richtlinien und Konfiguration (Nichtbenutzer)**   Online- und lokale Richtlinien erfordern eine separate Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="efa1e-238">**On-premises policies and configuration (non-user)**   Online and on-premises policies require separate configuration.</span></span> <span data-ttu-id="efa1e-239">Sie können keine globalen Richtlinien festlegen, die für beide Umgebungen gelten.</span><span class="sxs-lookup"><span data-stu-id="efa1e-239">You cannot set global policies that apply to both.</span></span>

<span data-ttu-id="efa1e-240"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efa1e-240"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
