---
title: 'Lync Server 2013: Aktivieren von Benutzern für gehostete Voicemail'
description: 'Lync Server 2013: Aktivieren von Benutzern für gehostete Voicemail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437469"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a><span data-ttu-id="ea835-103">Aktivieren von Benutzern für gehostete Voicemail in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ea835-103">Enable users for hosted voice mail in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ea835-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ea835-104">

<span> </span></span></span>

<span data-ttu-id="ea835-105">_**Letztes Änderungsdatum des Themas:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="ea835-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="ea835-106">Führen Sie das Verfahren zum Aktivieren von lync Server 2013-Benutzern für Voicemail in einem gehosteten Exchange Unified Messaging (um)-Dienst aus.</span><span class="sxs-lookup"><span data-stu-id="ea835-106">Follow the procedure to enable Lync Server 2013 users for voice mail on a hosted Exchange Unified Messaging (UM) service.</span></span>

<span data-ttu-id="ea835-107">Ausführliche Informationen finden Sie unter [gehostete Exchange-Benutzerverwaltung in lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ea835-107">For details, see [Hosted Exchange user management in Lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="ea835-108">Details zum Cmdlet " [setCsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) " finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="ea835-108">For details about the [Set-CsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ea835-109">Bevor ein lync Server 2013-Benutzer für gehostete Voicemail aktiviert werden kann, muss eine gehostete Voicemail-Richtlinie bereitgestellt werden, die für Ihr Benutzerkonto gilt.</span><span class="sxs-lookup"><span data-stu-id="ea835-109">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to their user account must be deployed.</span></span> <span data-ttu-id="ea835-110">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-hosted-voice-mail-policies.md">Richtlinien für gehostete Voicemail in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ea835-110">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a><span data-ttu-id="ea835-111">So aktivieren Sie Benutzer für gehostete Voicemails</span><span class="sxs-lookup"><span data-stu-id="ea835-111">To enable users for hosted voice mail</span></span>

1.  <span data-ttu-id="ea835-112">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="ea835-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="ea835-113">Führen Sie das Set-CsUser-Cmdlet aus, um das Benutzerkonto für gehostete Voicemail zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ea835-113">Run the Set-CsUser cmdlet to configure the user account for hosted voice mail.</span></span> <span data-ttu-id="ea835-114">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ea835-114">For example, run:</span></span>
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    <span data-ttu-id="ea835-115">Im oben stehenden Beispiel werden folgende Parameter festgelegt:</span><span class="sxs-lookup"><span data-stu-id="ea835-115">The preceding example sets the following parameters:</span></span>
    
      - <span data-ttu-id="ea835-116">**HostedVoiceMail** ermöglicht es, dass die Voicemail-Anrufe eines Benutzers an den Hosted Exchange um weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ea835-116">**HostedVoiceMail** enables a user’s voice mail calls to be routed to hosted Exchange UM.</span></span> <span data-ttu-id="ea835-117">Außerdem signalisiert Microsoft lync 2013, dass die Anzeige "Voicemail anrufen" leuchtet.</span><span class="sxs-lookup"><span data-stu-id="ea835-117">It also signals Microsoft Lync 2013 to light up the “call voice mail” indicator.</span></span>
    
      - <span data-ttu-id="ea835-118">**Identity** gibt das zu ändernde Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="ea835-118">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="ea835-119">Der Identity-Wert kann mit einem der folgenden Formate angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="ea835-119">The Identity value can be specified using any of the following formats:</span></span>
        
          - <span data-ttu-id="ea835-120">Die SIP-Adresse des Benutzers</span><span class="sxs-lookup"><span data-stu-id="ea835-120">The user's SIP address</span></span>
        
          - <span data-ttu-id="ea835-121">Name des Active Directory-Benutzerprinzipals des Benutzers</span><span class="sxs-lookup"><span data-stu-id="ea835-121">The user's Active Directory User-Principal-Name</span></span>
        
          - <span data-ttu-id="ea835-122">Der Domänen \\ Anmeldename des Benutzers (beispielsweise contoso \\ kenmyer)</span><span class="sxs-lookup"><span data-stu-id="ea835-122">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
        
          - <span data-ttu-id="ea835-123">Die Active Directory-Domänendienste des Benutzers Display-Name (beispielsweise Ken Myers).</span><span class="sxs-lookup"><span data-stu-id="ea835-123">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="ea835-124">Wenn Sie die Display-Name als Identitätswert verwenden, können Sie das \* Platzhalterzeichen Sternchen () verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea835-124">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="ea835-125">Die Identität " \* Smith" gibt beispielsweise alle Benutzer zurück, die eine Display-Name haben, die mit dem Zeichenfolgenwert "Smith" endet.</span><span class="sxs-lookup"><span data-stu-id="ea835-125">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="ea835-126">Der Name des Active Directory-SAM-Kontos des Benutzers kann nicht als Identitätswert verwendet werden, da der Name des SAM-Kontos in der Gesamtstruktur nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="ea835-126">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>

        
        <span data-ttu-id="ea835-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ea835-127"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

