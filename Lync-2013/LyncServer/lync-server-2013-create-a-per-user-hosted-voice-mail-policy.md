---
title: 'Lync Server 2013: Erstellen einer pro Benutzer gehosteten Voicemail-Richtlinie'
description: 'Lync Server 2013: Erstellen einer pro Benutzer gehosteten Voicemail-Richtlinie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a per-user hosted voice mail policy
ms:assetid: 39018a7c-e0c3-46a2-be4e-05604ec67a50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425867(v=OCS.15)
ms:contentKeyID: 48183902
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de528ceb9bc01114948c276c27f99039658aee38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432128"
---
# <a name="create-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="4cd54-103">Erstellen einer pro Benutzer gehosteten Voicemail-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cd54-103">Create a per-user hosted voice mail policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4cd54-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4cd54-104">

<span> </span></span></span>

<span data-ttu-id="4cd54-105">_**Letztes Änderungsdatum des Themas:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="4cd54-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="4cd54-106">Eine Richtlinie *pro Benutzer* kann nur Auswirkungen auf einzelne Benutzer, Gruppen und Kontaktobjekte haben.</span><span class="sxs-lookup"><span data-stu-id="4cd54-106">A *per-user* policy can only impact individual users, groups, and contact objects.</span></span> <span data-ttu-id="4cd54-107">Wenn Sie eine Richtlinie pro Benutzer bereitstellen möchten, müssen Sie die Richtlinie explizit einem oder mehreren Benutzern, Gruppen oder Kontaktobjekten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4cd54-107">To deploy a per-user policy, you must explicitly assign the policy to one or more users, groups, or contact objects.</span></span> <span data-ttu-id="4cd54-108">Ausführliche Informationen finden Sie unter [Zuweisen einer pro Benutzer gehosteten Voicemail-Richtlinie in lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).</span><span class="sxs-lookup"><span data-stu-id="4cd54-108">For details, see [Assign a per-user hosted voice mail policy in Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).</span></span>

<span data-ttu-id="4cd54-109">Ausführliche Informationen zum Arbeiten mit Richtlinien für gehostete Voicemail pro Benutzer finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4cd54-109">For details about working with per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="4cd54-110">Neu – CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd54-110">New-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="4cd54-111">Satz-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd54-111">Set-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy)

  - [<span data-ttu-id="4cd54-112">Get-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="4cd54-112">Get-CsHostedVoicemailPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsHostedVoicemailPolicy)

<div>

## <a name="to-create-a-per-user-hosted-voice-mail-policy"></a><span data-ttu-id="4cd54-113">So erstellen Sie eine pro Benutzer gehostete Voicemail-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4cd54-113">To create a per-user hosted voice mail policy</span></span>

1.  <span data-ttu-id="4cd54-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4cd54-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4cd54-115">Führen Sie das New-CsHostedVoicemailPolicy-Cmdlet aus, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4cd54-115">Run the New-CsHostedVoicemailPolicy cmdlet to create the policy.</span></span> <span data-ttu-id="4cd54-116">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="4cd54-116">For example, run:</span></span>
    
        New-CsHostedVoicemailPolicy -Identity ExRedmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for Redmond users." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    <span data-ttu-id="4cd54-117">Im vorherigen Beispiel wird eine gehostete Voicemail-Richtlinie mit benutzerspezifischem Bereich erstellt, und die folgenden Parameter werden festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4cd54-117">The previous example creates a hosted voice mail policy with per-user scope, and sets the following parameters:</span></span>
    
      - <span data-ttu-id="4cd54-118">**Identity** gibt einen eindeutigen Bezeichner für die Richtlinie an, der den Bereich umfasst.</span><span class="sxs-lookup"><span data-stu-id="4cd54-118">**Identity** specifies a unique identifier for the policy, which includes the scope.</span></span> <span data-ttu-id="4cd54-119">Bei einer Richtlinie mit benutzerspezifischem Gültigkeitsbereich wird dieser Parameterwert als einfache Zeichenfolge angegeben, beispielsweise "" "," "".</span><span class="sxs-lookup"><span data-stu-id="4cd54-119">For a policy with per-user scope, this parameter value is specified as a simple string, for example, ExRedmond.</span></span>
    
      - <span data-ttu-id="4cd54-120">**Ziel** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des gehosteten Exchange um-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="4cd54-120">**Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service.</span></span> <span data-ttu-id="4cd54-121">Dieser Parameter ist optional, aber wenn Sie versuchen, einen Benutzer für gehostete Voicemail zu aktivieren, und die zugewiesene Richtlinie des Benutzers keinen Zielwert hat, schlägt die Aktivierung fehl.</span><span class="sxs-lookup"><span data-stu-id="4cd54-121">This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.</span></span>
    
      - <span data-ttu-id="4cd54-122">**Beschreibung** enthält optionale beschreibende Informationen zur Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4cd54-122">**Description** provides optional descriptive information about the policy.</span></span>
    
      - <span data-ttu-id="4cd54-123">**Organisation** gibt eine durch trennzeichengetrennte Liste der Exchange-Mandanten an, die lync Server 2013-Benutzer sind.</span><span class="sxs-lookup"><span data-stu-id="4cd54-123">**Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users.</span></span> <span data-ttu-id="4cd54-124">Jeder Mandant muss als FQDN dieses Mandanten für den gehosteten Exchange um-Dienst angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4cd54-124">Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4cd54-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd54-125">See Also</span></span>


[<span data-ttu-id="4cd54-126">Zuweisen einer pro Benutzer gehosteten Voicemail-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4cd54-126">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)  
  

<span data-ttu-id="4cd54-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4cd54-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

