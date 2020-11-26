---
title: 'Lync Server 2013: Anzeigen von trunk-Konfigurationsinformationen'
description: 'Lync Server 2013: Anzeigen von trunk-Konfigurationsinformationen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View trunk configuration information
ms:assetid: ebe10e14-08c2-4797-9254-9ed89516d5cd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721927(v=OCS.15)
ms:contentKeyID: 49733862
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b4e1d3063d65f8c27ad231f063249748046f759
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444028"
---
# <a name="view-trunk-configuration-information-in-lync-server-2013"></a><span data-ttu-id="f5eff-103">Anzeigen von trunk-Konfigurationsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5eff-103">View trunk configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5eff-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5eff-104">

<span> </span></span></span>

<span data-ttu-id="f5eff-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="f5eff-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="f5eff-106">SIP Trunk-Konfigurationseinstellungen definieren die Beziehungen und Funktionen zwischen einem Vermittlungs Server und dem PSTN-Gateway (Public Switched Telephone Network), einer IP-Public Branch Exchange (PBX) oder einem Session Border Controller (SBC) beim Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f5eff-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="f5eff-107">Diese Einstellungen geben unter anderem Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="f5eff-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="f5eff-108">Ob Medienumgehung für die Trunks aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5eff-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="f5eff-109">Die Bedingungen, unter denen RTCP-Pakete (Real-Time Transport Control Protocol) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5eff-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="f5eff-110">Ob die SRTP-Verschlüsselung (Secure Real-Time Protocol) für jeden trunk erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5eff-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="f5eff-111">Wenn Sie Microsoft lync Server 2013 installieren, wird eine globale Sammlung von SIP-Trunk-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="f5eff-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="f5eff-112">Darüber hinaus können Administratoren benutzerdefinierte Auflistungen mit Einstellungen auf Standort- oder Dienstebene erstellen (nur für den PSTN-Gatewaydienst).</span><span class="sxs-lookup"><span data-stu-id="f5eff-112">In addition, administrators can create custom setting collections at the site scope or at the service scope (for the PSTN gateway service, only).</span></span>

<div>

## <a name="to-view-sip-trunk-configuration-information-by-using-lync-server-control-panel"></a><span data-ttu-id="f5eff-113">So zeigen Sie SIP-Trunk-Konfigurationsinformationen mithilfe der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="f5eff-113">To view SIP trunk configuration information by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="f5eff-114">Klicken Sie in der lync Server-Systemsteuerung auf **VoIP-Routing** , und klicken Sie dann auf **trunk-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f5eff-114">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="f5eff-115">Auf dem Reiter " **trunk Configuration** " sehen Sie eine Liste aller ihrer trunk Configuration Settings-Sammlung. für jede Sammlung werden Werte für die Eigenschaften **Name**, **Scope**, **State** und **Media Bypass** sowie die Anzahl der **PSTN-Nutzungen**, **Regeln** für die Rufnummernanzeige und **benannte Nummern Regeln** für die Sammlung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5eff-115">On the **Trunk Configuration** tab you will see a list of all your trunk configuration settings collection; for each collection you will see values for the **Name**, **Scope**, **State**, and **Media bypass** properties, along with the number of **PSTN usages**, **Calling number rules**, and **Called number rules** associated with the collection.</span></span> <span data-ttu-id="f5eff-116">Wenn Sie weitere Details zu einer Sammlung von trunk-Konfigurationseinstellungen anzeigen möchten, klicken Sie auf die Sammlung von Interesse, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="f5eff-116">To see additional details about a collection of trunk configuration settings, click the collection of interest, click **Edit**, and then click **Show details**.</span></span> <span data-ttu-id="f5eff-117">Beachten Sie, dass Sie detaillierte Informationen nur für eine Sammlung von trunk-Konfigurationseinstellungen gleichzeitig anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="f5eff-117">Note that you can view detailed information only for one collection of trunk configuration settings at a time.</span></span>

</div>

<div>

## <a name="viewing-sip-trunk-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="f5eff-118">Anzeigen von SIP-Trunk-Konfigurationsinformationen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f5eff-118">Viewing SIP Trunk Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="f5eff-119">Die Konfigurationseinstellungen für den SIP-Trunk können mithilfe der lync Server PowerShell und des Get-CsTrunkConfiguration-Cmdlets angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5eff-119">SIP trunk configuration settings can be viewed by using Lync Server PowerShell and the Get-CsTrunkConfiguration cmdlet.</span></span> <span data-ttu-id="f5eff-120">Dieses Cmdlet kann entweder über die lync Server 2013-Verwaltungsshell oder über eine Windows PowerShell-Remotesitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f5eff-120">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session Windows PowerShell.</span></span> <span data-ttu-id="f5eff-121">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="f5eff-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-sip-trunk-configuration-information"></a><span data-ttu-id="f5eff-122">So zeigen Sie die SIP-Trunk-Konfigurationsinformationen an</span><span class="sxs-lookup"><span data-stu-id="f5eff-122">To view SIP trunk configuration information</span></span>

  - <span data-ttu-id="f5eff-123">Wenn Sie Informationen zu allen Ihren SIP-Trunk-Konfigurationseinstellungen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="f5eff-123">To view information about all your SIP trunk configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsTrunkConfiguration
    
    <span data-ttu-id="f5eff-124">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="f5eff-124">That will return information similar to this:</span></span>
    
        Identity                                  : Global
        OutboundTranslationRulesList              : {}
        SipResponseCodeTranslationRulesList       : {}
        OutboundCallingNumberTranslationRulesList : {}
        PstnUsages                                : {}
        Description                               :
        ConcentratedTopology                      : True
        EnableBypass                              : False
        EnableMobileTrunkSupport                  : False
        EnableReferSupport                        : True
        EnableSessionTimer                        : False
        EnableSignalBoost                         : False
        MaxEarlyDialogs                           : 20
        RemovePlusFromUri                         : False
        RTCPActiveCalls                           : True
        RTCPCallsOnHold                           : True
        SRTPMode                                  : Required
        EnablePIDFLOSupport                       : False
        EnableRTPLatching                         : False
        EnableOnlineVoice                         : False
        ForwardCallHistory                        : False
        Enable3pccRefer                           : False
        ForwardPAI                                : False
        EnableFastFailoverTimer                   : True

</div>

<span data-ttu-id="f5eff-125">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="f5eff-125">For more information, see the help topic for the [Get-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsTrunkConfiguration) cmdlet.</span></span>

<span data-ttu-id="f5eff-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5eff-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

