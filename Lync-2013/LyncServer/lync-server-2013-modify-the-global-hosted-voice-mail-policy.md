---
title: 'Lync Server 2013: Ändern der Global Hosted Voicemail-Richtlinie'
description: 'Lync Server 2013: Ändern der globalen Richtlinie für gehostete Voicemail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the global hosted voice mail policy
ms:assetid: f059b3ce-a7d8-4ea9-b10b-0052222ec2ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412994(v=OCS.15)
ms:contentKeyID: 48185757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9cd5e16c78049ce79abd936a79b2025a14e45943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445701"
---
# <a name="modify-the-global-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="ac4df-103">Ändern der Global Hosted Voicemail-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac4df-103">Modify the global hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac4df-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac4df-104">

<span> </span></span></span>

<span data-ttu-id="ac4df-105">_**Letztes Änderungsdatum des Themas:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="ac4df-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="ac4df-106">Die *Global* Hosted Voicemail-Richtlinie wird mit lync Server 2013 installiert.</span><span class="sxs-lookup"><span data-stu-id="ac4df-106">The *global* hosted voice mail policy is installed with Lync Server 2013.</span></span> <span data-ttu-id="ac4df-107">Sie können Sie ändern, um Ihre Anforderungen zu erfüllen, aber Sie können Sie nicht umbenennen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="ac4df-107">You can modify it to meet your needs, but you cannot rename or delete it.</span></span> <span data-ttu-id="ac4df-108">Zum Ändern der globalen Richtlinie verwenden Sie das Set-CsHostedVoicemailPolicy-Cmdlet, um die Parameter auf die entsprechenden Werte für die jeweilige Bereitstellung zu setzen.</span><span class="sxs-lookup"><span data-stu-id="ac4df-108">To modify the global policy, you use the Set-CsHostedVoicemailPolicy cmdlet to set the parameters to appropriate values for your specific deployment.</span></span>

<span data-ttu-id="ac4df-109">Details zum Cmdlet " [setCsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) " finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="ac4df-109">For details about the [Set-CsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>

## <a name="to-modify-the-global-hosted-voice-mail-policy"></a><span data-ttu-id="ac4df-110">So ändern Sie die Global Hosted Voicemail-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="ac4df-110">To modify the global hosted voice mail policy</span></span>

1.  <span data-ttu-id="ac4df-111">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="ac4df-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ac4df-112">Führen Sie das Set-CsHostedVoicemailPolicy-Cmdlet aus, um die globalen Richtlinienparameter für Ihre Umgebung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ac4df-112">Run the Set-CsHostedVoicemailPolicy cmdlet to set the global policy parameters for your environment.</span></span> <span data-ttu-id="ac4df-113">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ac4df-113">For example, run:</span></span>
    
        Set-CsHostedVoicemailPolicy -Destination ExUM.fabrikam.com -Organization "corp1.litwareinc.com"
    
    <span data-ttu-id="ac4df-114">Da dieser Befehl den Identitätsparameter der Richtlinie nicht angibt, legt die Windows PowerShell-Befehlszeilenschnittstelle die folgenden Werte für die Global Hosted Voicemail-Richtlinie fest:</span><span class="sxs-lookup"><span data-stu-id="ac4df-114">Because this command does not specify the policy’s Identity parameter, Windows PowerShell command-line interface sets the following values on the global hosted voice mail policy:</span></span>
    
      - <span data-ttu-id="ac4df-115">**Ziel** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des gehosteten Exchange um-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="ac4df-115">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="ac4df-116">Dieser Parameter ist optional, aber wenn Sie versuchen, einen Benutzer für gehostete Voicemail zu aktivieren, und die zugewiesene Richtlinie des Benutzers keinen Zielwert hat, schlägt die Aktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="ac4df-116">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="ac4df-117">**Organisation** gibt eine durch trennzeichengetrennte Liste der Exchange-Mandanten an, die zu den lync Server-Benutzern werden.</span><span class="sxs-lookup"><span data-stu-id="ac4df-117">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server users.</span></span> <span data-ttu-id="ac4df-118">Jeder Mandant muss als FQDN dieses Mandanten für den gehosteten Exchange um-Dienst angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ac4df-118">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ac4df-119">Im vorherigen Beispiel-Cmdlet ersetzt der Wert "corp1.litwareinc.com" alle Werte, die möglicherweise bereits im Parameter Organization vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ac4df-119">In the previous example cmdlet, the value “corp1.litwareinc.com” replaces any value that might already be present in the Organization parameter.</span></span> <span data-ttu-id="ac4df-120">Wenn die Richtlinie beispielsweise bereits eine durch trennzeichengetrennte Liste von Organisationen enthält, wird die vollständige Liste ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ac4df-120">For example, if the policy already contains a comma-separated list of organizations, the full list would be replaced.</span></span> <span data-ttu-id="ac4df-121">Wenn Sie der Liste eine Organisation hinzufügen möchten, anstatt die gesamte Liste zu ersetzen, führen Sie einen Befehl wie den folgenden aus.</span><span class="sxs-lookup"><span data-stu-id="ac4df-121">If you want to add an organization to the list rather than replace the entire list, run a command similar to the following.</span></span>

    
    </div>
    
        $a = Get-CsHostedVoicemailPolicy
        $a.Organization += ",corp3.litwareinc.com"
        Set-CsHostedVoicemailPolicy -Organization $a.Organization

<span data-ttu-id="ac4df-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac4df-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

