---
title: 'Lync Server 2013: Erstellen einer Hosted Voicemail-Richtlinie auf Websiteebene'
description: 'Lync Server 2013: Erstellen einer Hosted Voicemail-Richtlinie auf Websiteebene'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a site-level hosted voice mail policy
ms:assetid: 145892c8-a6ca-45fb-9e83-786f709dd775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398216(v=OCS.15)
ms:contentKeyID: 48183481
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8cd578359a8d20562e8887b61b86d53332e6f8d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432114"
---
# <a name="create-a-site-level-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="de662-103">Erstellen einer gehosteten Voicemail-Richtlinie auf Websiteebene in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de662-103">Create a site-level hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de662-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de662-104">

<span> </span></span></span>

<span data-ttu-id="de662-105">_**Letztes Änderungsdatum des Themas:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="de662-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="de662-106">Eine *Website* Richtlinie kann sich auf alle Benutzer auswirken, die sich auf der Website befinden, für die die Richtlinie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="de662-106">A *site* policy can impact all users that are homed on the site for which the policy is defined.</span></span> <span data-ttu-id="de662-107">Wenn ein Benutzer für den gehosteten Exchange um-Zugriff konfiguriert ist und keiner Richtlinie pro Benutzer zugewiesen wurde, gilt die Website Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="de662-107">If a user is configured for hosted Exchange UM access and has not been assigned a Per-user policy, the site policy applies.</span></span> <span data-ttu-id="de662-108">Wenn Sie keine Website Richtlinie bereitgestellt haben, gilt die globale Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="de662-108">If you have not deployed a site policy, the global policy applies.</span></span>

<span data-ttu-id="de662-109">Details zum Konfigurieren von Website Richtlinien finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="de662-109">For details about configuring site policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="de662-110">Neu – CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="de662-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="de662-111">Satz-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="de662-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="de662-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="de662-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-site-hosted-voice-mail-policy"></a><span data-ttu-id="de662-113">So erstellen Sie eine von der Website gehostete Voicemail-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="de662-113">To create a site hosted voice mail policy</span></span>

1.  <span data-ttu-id="de662-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="de662-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="de662-115">Führen Sie das New-CsHostedVoicemailPolicy-Cmdlet aus, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="de662-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="de662-116">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="de662-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity site:Redmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for the Redmond site." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="de662-117">In diesem Beispiel wird eine gehostete Voicemail-Richtlinie mit Website Bereich erstellt, und die folgenden Parameter werden festgelegt:</span><span class="sxs-lookup"><span data-stu-id="de662-117">This example creates a hosted voice mail policy with site scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="de662-118">**Identity** gibt einen eindeutigen Bezeichner für die Richtlinie an, der den Bereich umfasst.</span><span class="sxs-lookup"><span data-stu-id="de662-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="de662-119">Bei einer Richtlinie mit Website Bereich muss der Parameterwert Identity im Format angegeben werden `site:` *\<name\>* , beispielsweise `site:Redmond` .</span><span class="sxs-lookup"><span data-stu-id="de662-119">For a policy with site scope, the Identity parameter value must be specified in the format `site:`*\<name\>*, for example, `site:Redmond`.</span></span>
    
      - <span data-ttu-id="de662-120">**Ziel** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des gehosteten Exchange um-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="de662-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="de662-121">Dieser Parameter ist optional, aber wenn Sie versuchen, einen Benutzer für gehostete Voicemail zu aktivieren, und die zugewiesene Richtlinie des Benutzers keinen Zielwert hat, schlägt die Aktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="de662-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="de662-122">**Beschreibung** enthält optionale beschreibende Informationen zur Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="de662-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="de662-123">**Organisation** gibt eine durch trennzeichengetrennte Liste der Exchange-Mandanten an, die lync Server 2013-Benutzer sind.</span><span class="sxs-lookup"><span data-stu-id="de662-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="de662-124">Jeder Mandant muss als FQDN dieses Mandanten für den gehosteten Exchange um-Dienst angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de662-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

<span data-ttu-id="de662-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de662-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

