---
title: 'Lync Server 2013: Konfigurieren von Netzwerkstandort Links'
description: 'Lync Server 2013: Konfigurieren von Netzwerkstandort Links.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network site links
ms:assetid: 7e9147ae-e727-46c8-8c1a-6c13201f09be
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521023(v=OCS.15)
ms:contentKeyID: 48184622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68b4ecce15b8f3ba5a5717c73a8f97f8a0633b58
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432893"
---
# <a name="configuring-network-site-links-in-lync-server-2013"></a><span data-ttu-id="19629-103">Konfigurieren von Netzwerkstandort Links in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19629-103">Configuring network site links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19629-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19629-104">

<span> </span></span></span>

<span data-ttu-id="19629-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="19629-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="19629-106">Innerhalb einer Anruf Steuerungskonfiguration können Sie netzwerkübergreifende Richtlinien erstellen, die Bandbreiteneinschränkungen zwischen Websites definieren, die direkt verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="19629-106">Within a call admission control (CAC) configuration, you can create network inter-site policies that define bandwidth limitations between sites that are directly linked.</span></span> <span data-ttu-id="19629-107">Wenn Netzwerk Websites einen direkten Link verwenden, können Bandbreiteneinschränkungen für Audio-und Videoverbindungen zwischen diesen beiden Websites definiert werden.</span><span class="sxs-lookup"><span data-stu-id="19629-107">When network sites share a direct link, bandwidth limitations for audio and video connections can be defined between those two sites.</span></span> <span data-ttu-id="19629-108">Sie können die lync Server-Systemsteuerung nicht zum Konfigurieren von Netzwerk Website Richtlinien verwenden, dies kann nur mithilfe von Cmdlets aus der lync Server-Verwaltungsshell erfolgen.</span><span class="sxs-lookup"><span data-stu-id="19629-108">You cannot use the Lync Server Control Panel to configure network site policies, this can be done only by using cmdlets from the Lync Server Management Shell.</span></span> <span data-ttu-id="19629-109">Sie können einen Netzwerkstandort Link (auch bekannt als netzwerkübergreifende Website Richtlinie) aus der lync Server-Verwaltungsshell erstellen, ändern und entfernen.</span><span class="sxs-lookup"><span data-stu-id="19629-109">You can create, modify, and remove a network site link (also known as a network inter-site policy) from the Lync Server Management Shell.</span></span>

<div>

## <a name="to-create-a-network-site-link"></a><span data-ttu-id="19629-110">So erstellen Sie einen Netzwerkstandort Link</span><span class="sxs-lookup"><span data-stu-id="19629-110">To create a network site link</span></span>

1.  <span data-ttu-id="19629-111">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19629-111">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="19629-112">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="19629-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="19629-113">Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, und ersetzen Sie Werte, die für Ihre Konfiguration gültig sind:</span><span class="sxs-lookup"><span data-stu-id="19629-113">From the command prompt, type the following command, substituting values that are valid for your configuration:</span></span>
    
        New-CsNetworkInterSitePolicy -Identity Reno_Portland -NetworkSiteID1 Reno -NetworkSiteID2 Portland -BWPolicyProfileID LowBWLimits
    
    <span data-ttu-id="19629-114">In diesem Beispiel wird eine neue netzwerkstandortverknüpfung namens Reno \_ Portland erstellt, die Bandbreiteneinschränkungen zwischen den Netzwerkstandorten Reno und Portland festlegt.</span><span class="sxs-lookup"><span data-stu-id="19629-114">This example creates a new network site link named Reno\_Portland that sets bandwidth limitations between the Reno and Portland network sites.</span></span> <span data-ttu-id="19629-115">Die Netzwerk Websites und das bandbreitenrichtlinienprofil müssen bereits vorhanden sein, bevor Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="19629-115">The network sites and the bandwidth policy profile must already exist before running this command.</span></span>

<span data-ttu-id="19629-116">Ausführliche Informationen zu den Parametern finden Sie unter [New-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy) in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="19629-116">For detailed parameter descriptions, see [New-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span> <span data-ttu-id="19629-117">Rufen Sie das Cmdlet **Get-CsNetworkBandwidthPolicyProfile** auf, um eine Liste der bandbreitenrichtlinienprofile abzurufen, die auf den Link Netzwerk Website angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="19629-117">To retrieve a list of bandwidth policy profiles that can be applied to the network site link, call the **Get-CsNetworkBandwidthPolicyProfile** cmdlet.</span></span> <span data-ttu-id="19629-118">Ausführliche Informationen finden Sie unter [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="19629-118">For details, see [Get-CsNetworkBandwidthPolicyProfile](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-modify-a-network-site-link"></a><span data-ttu-id="19629-119">So ändern Sie einen Link für eine Netzwerk Website</span><span class="sxs-lookup"><span data-stu-id="19629-119">To modify a network site link</span></span>

1.  <span data-ttu-id="19629-120">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19629-120">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="19629-121">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="19629-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="19629-122">Verwenden Sie das Cmdlet " **Satz-CsNetworkInterSitePolicy** ", um die Eigenschaften einer bestimmten netzwerkstandortverknüpfung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="19629-122">Use the **Set-CsNetworkInterSitePolicy** cmdlet to modify the properties of a given network site link.</span></span> <span data-ttu-id="19629-123">Sie können entweder (oder beide) oder die verbundenen Websites ändern, und Sie können das dem Link zugeordnete bandbreitenrichtlinienprofil ändern.</span><span class="sxs-lookup"><span data-stu-id="19629-123">You can modify either (or both) or the connected sites, and you can modify the bandwidth policy profile associated with the link.</span></span> <span data-ttu-id="19629-124">Nachfolgend finden Sie ein Beispiel für das Ändern des bandbreitenrichtlinienprofils einer Standortverknüpfung mit dem Namen Reno \_ Portland:</span><span class="sxs-lookup"><span data-stu-id="19629-124">Here is an example of modifying the bandwidth policy profile of a site link named Reno\_Portland:</span></span>
    
        Set-CsNetworkInterSitePolicy -Identity Reno_Portland -BWPolicyProfileID HighBWLimits

<span data-ttu-id="19629-125">Ausführliche Beschreibungen der Parameter finden Sie unter CsNetworkInterSitePolicy in der lync Server [-](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy) Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="19629-125">For detailed parameter descriptions, see [Set-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-delete-a-network-site-link"></a><span data-ttu-id="19629-126">So löschen Sie einen Netzwerkstandort Link</span><span class="sxs-lookup"><span data-stu-id="19629-126">To delete a network site link</span></span>

1.  <span data-ttu-id="19629-127">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19629-127">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="19629-128">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="19629-128">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="19629-129">Verwenden Sie das Cmdlet **Remove-CsNetworkInterSitePolicy** , um einen Netzwerkstandort Link zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="19629-129">Use the **Remove-CsNetworkInterSitePolicy** cmdlet to remove a network site link.</span></span> <span data-ttu-id="19629-130">Im folgenden Beispiel wird der Link zur Portland-Netzwerk Website von Reno gelöscht \_ :</span><span class="sxs-lookup"><span data-stu-id="19629-130">The following example deletes the Reno\_Portland network site link:</span></span>
    
        Remove-CsNetworkInterSitePolicy -Identity Reno_Portland

<span data-ttu-id="19629-131">Ausführliche Beschreibungen der Parameter finden Sie unter [Remove-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy) in der lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="19629-131">For detailed parameter descriptions, see [Remove-CsNetworkInterSitePolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy) in the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="19629-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19629-132">See Also</span></span>


[<span data-ttu-id="19629-133">Cmdlets für die Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="19629-133">Call admission control cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/)  


[<span data-ttu-id="19629-134">New-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="19629-134">New-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterSitePolicy)  
[<span data-ttu-id="19629-135">Set-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="19629-135">Set-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterSitePolicy)  
[<span data-ttu-id="19629-136">Remove-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="19629-136">Remove-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterSitePolicy)  
[<span data-ttu-id="19629-137">Get-CsNetworkInterSitePolicy</span><span class="sxs-lookup"><span data-stu-id="19629-137">Get-CsNetworkInterSitePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterSitePolicy)  
[<span data-ttu-id="19629-138">Get-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="19629-138">Get-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="19629-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19629-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

