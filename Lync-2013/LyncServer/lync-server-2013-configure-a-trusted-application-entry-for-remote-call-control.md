---
title: Konfigurieren eines Eintrags einer vertrauenswürdigen Anwendung für die Remoteanrufsteuerung
description: Konfigurieren Sie einen vertrauenswürdigen Anwendungseintrag für die Remoteanrufsteuerung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a trusted application entry for remote call control
ms:assetid: 37777f93-8b24-40cf-808e-7c6230eb2132
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558636(v=OCS.15)
ms:contentKeyID: 48183829
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa5341dc220853670cf000f5b0d5dc379c02fa51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434153"
---
# <a name="configure-a-trusted-application-entry-for-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="3824b-103">Konfigurieren eines Eintrags einer vertrauenswürdigen Anwendung für die Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3824b-103">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3824b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3824b-104">

<span> </span></span></span>

<span data-ttu-id="3824b-105">_**Letztes Änderungsdatum des Themas:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="3824b-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="3824b-106">Das SIP/CSTA-Gateway muss als vertrauenswürdige Anwendung konfiguriert sein, damit lync Server eine statische Route zum Weiterleiten von Anrufen an das Gateway anwenden kann.</span><span class="sxs-lookup"><span data-stu-id="3824b-106">The SIP/CSTA gateway must be configured as a trusted application in order for Lync Server to apply a static route to route calls to the gateway.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="3824b-107">Wenn Sie Benutzer aus einer früheren Version der lync Server-Bereitstellung migrieren, müssen Sie sicherstellen, dass Sie alle vorhandenen Einträge für vertrauenswürdige Anwendungen (zuvor als autorisierte Hosteinträge bezeichnet) entfernt haben, die Sie für das SIP/CSTA-Gateway erstellt haben, bevor Sie die Verfahren in diesem Thema ausführen.</span><span class="sxs-lookup"><span data-stu-id="3824b-107">If you're migrating users from a previous version of Lync Server deployment, be sure that you removed all existing trusted application entries (previously known as authorized host entries) you created for the SIP/CSTA gateway before following the procedures in this topic.</span></span> <span data-ttu-id="3824b-108">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Entfernen eines autorisierten Legacyhosts in lync Server 2013 (optional)</A>.</span><span class="sxs-lookup"><span data-stu-id="3824b-108">For details, see <A href="lync-server-2013-remove-a-legacy-authorized-host-optional.md">Remove a legacy authorized host in Lync Server 2013 (optional)</A>.</span></span><BR><span data-ttu-id="3824b-109">Wenn Sie beabsichtigen, eine neue Remoteanrufsteuerung mithilfe einer TCP-Verbindung (Transmission Control Protocol) bereitzustellen, müssen Sie sicherstellen, dass die <STRONG>Beschränkung der Dienstnutzung auf ausgewählte IP-Adressen</STRONG> auf vorhandenen vertrauenswürdigen Anwendungen und Pools festgelegt ist, wenn Sie denselben TCP-Port für die neue vertrauenswürdige Anwendung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3824b-109">If you plan to deploy new remote call control by using a Transmission Control Protocol (TCP) connection, you need to verify that <STRONG>Limit service usage to selected IP addresses</STRONG> should be set on existing trusted applications and pools, if you want to use the same TCP port for the new trusted application.</span></span>



</div>

<div>

## <a name="to-configure-a-trusted-application-entry-for-the-sipcsta-gateway"></a><span data-ttu-id="3824b-110">So konfigurieren Sie einen Eintrag für vertrauenswürdige Anwendungen für das SIP/CSTA-Gateway</span><span class="sxs-lookup"><span data-stu-id="3824b-110">To configure a trusted application entry for the SIP/CSTA gateway</span></span>

1.  <span data-ttu-id="3824b-111">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder einer rollenbasierten zugriffssteuerungsrolle (Role-Based Access Control, RBAC) installiert ist, der Sie das Cmdlet **New-CsTrustedApplicationPool** zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="3824b-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or a role-based access control (RBAC) role to which you have assigned the **New-CsTrustedApplicationPool** cmdlet.</span></span>

2.  <span data-ttu-id="3824b-112">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="3824b-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="3824b-113">Führen Sie zum Erstellen eines vertrauenswürdigen Anwendungseintrags eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="3824b-113">To create a trusted application entry, do one of the following:</span></span>
    
      - <span data-ttu-id="3824b-114">Bei einer TLS-Verbindung (Transport Layer Security) geben Sie Folgendes an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="3824b-114">For a Transport Layer Security (TLS) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="3824b-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3824b-115">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity rccgateway.contoso.net -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true
    
      - <span data-ttu-id="3824b-116">Bei einer TCP-Verbindung (Transmission Control Protocol) geben Sie Folgendes an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="3824b-116">For a Transmission Control Protocol (TCP) connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplicationPool -Identity <IP address or FQDN of the SIP/CSTA gateway> [-Registrar <Service ID or FQDN of the Registrar service>] -Site <Site ID for the site where you want to create the trusted application pool>
        
        <span data-ttu-id="3824b-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3824b-117">For example:</span></span>
        
            New-CsTrustedApplicationPool -Identity 192.168.0.240 -Registrar registrar1.contoso.net -Site co1 -TreatAsAuthenticated $true -ThrottleAsServer $true

4.  <span data-ttu-id="3824b-118">Führen Sie eine der folgenden Aktionen aus, um dem Pool die vertrauenswürdige Anwendung hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="3824b-118">To add the trusted application to the pool, do one of the following:</span></span>
    
      - <span data-ttu-id="3824b-119">Geben Sie bei einer TLS-Verbindung Folgendes an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="3824b-119">For a TLS connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway>
        
        <span data-ttu-id="3824b-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3824b-120">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn rccgateway.contoso.net -Port 5065
    
      - <span data-ttu-id="3824b-121">Geben Sie bei einer TCP-Verbindung Folgendes an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="3824b-121">For a TCP connection, type the following at the command prompt:</span></span>
        
            New-CsTrustedApplication -ApplicationID <application name> -TrustedApplicationPoolFqdn <IP address or FQDN of the SIP/CSTA gateway> -Port <SIP listening port on the gateway> -EnableTcp
        
        <span data-ttu-id="3824b-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3824b-122">For example:</span></span>
        
            New-CsTrustedApplication -ApplicationID RccGateway-1 -TrustedApplicationPoolFqdn 192.169.0.240 -Port 5065 -EnableTcp

5.  <span data-ttu-id="3824b-123">Geben Sie an der Eingabeaufforderung Folgendes ein, um die veröffentlichten Änderungen zu implementieren, die Sie an der Topologie vorgenommen haben:</span><span class="sxs-lookup"><span data-stu-id="3824b-123">To implement the published changes you have made to the topology, type the following at the command prompt:</span></span>
    
        Enable-CsTopology

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3824b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3824b-124">See Also</span></span>


[<span data-ttu-id="3824b-125">Konfigurieren einer statischen Route für die Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3824b-125">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)  
[<span data-ttu-id="3824b-126">Definieren der IP-Adresse für ein SIP/CSTA-Gateway in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3824b-126">Define a SIP/CSTA gateway IP address in Lync Server 2013</span></span>](lync-server-2013-define-a-sip-csta-gateway-ip-address.md)  
  

<span data-ttu-id="3824b-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3824b-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

