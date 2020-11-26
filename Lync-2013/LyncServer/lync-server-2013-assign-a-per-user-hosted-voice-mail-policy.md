---
title: 'Lync Server 2013: Zuweisen einer pro Benutzer gehosteten Voicemail-Richtlinie'
description: 'Lync Server 2013: Zuweisen einer pro Benutzer gehosteten Voicemail-Richtlinie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user hosted voice mail policy
ms:assetid: d44c71a0-4407-4ab4-b7e0-d671dde3425f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398919(v=OCS.15)
ms:contentKeyID: 48185456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 071d504c452b4d3adb1b636cb5c4ff8835200107
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440521"
---
# <a name="assign-a-per-user-hosted-voice-mail-policy-in-lync-server-2013"></a><span data-ttu-id="547c7-103">Zuweisen einer pro Benutzer gehosteten Voicemail-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="547c7-103">Assign a per-user hosted voice mail policy in Lync Server 2013</span></span>

 


<span data-ttu-id="547c7-104">Das Bereitstelleneiner oder mehrerer pro Benutzer gehosteter Voicemail-Richtlinien ist optional.</span><span class="sxs-lookup"><span data-stu-id="547c7-104">Deploying one or more per-user hosted voice mail policies is optional.</span></span> <span data-ttu-id="547c7-105">Wenn Sie Richtlinien für einzelne Benutzer bereitstellen, müssen Sie diese explizit Benutzern, Gruppen oder Kontaktobjekten zuweisen.</span><span class="sxs-lookup"><span data-stu-id="547c7-105">If you do deploy per-user policies, you must explicitly assign them to users, groups, or contact objects.</span></span>

<span data-ttu-id="547c7-106">Details zum Zuweisen oder Entfernen der Zuweisung von Richtlinien für gehostete Voicemail pro Benutzer finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="547c7-106">For details about assigning or removing the assignment of per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="547c7-107">Grant-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="547c7-107">Grant-CsHostedVoicemailPolicy</span></span>

  - <span data-ttu-id="547c7-108">Remove-CsHostedVoicemailPolicy</span><span class="sxs-lookup"><span data-stu-id="547c7-108">Remove-CsHostedVoicemailPolicy</span></span>

## <a name="to-assign-a-per-user-hosted-voice-mail-policy"></a><span data-ttu-id="547c7-109">So weisen Sie eine pro Benutzer gehostete Voicemail-Richtlinie zu</span><span class="sxs-lookup"><span data-stu-id="547c7-109">To assign a per-user hosted voice mail policy</span></span>

1.  <span data-ttu-id="547c7-110">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="547c7-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="547c7-111">Führen Sie das Grant-CsHostedVoicemailPolicy-Cmdlet aus, um die Richtlinie für pro Benutzer gehostete Voicemail einzelnen Benutzern, Gruppen und Kontaktobjekten zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="547c7-111">Run the Grant-CsHostedVoicemailPolicy cmdlet to assign the per-user hosted voice mail policy to individual users, groups, and contact objects.</span></span> <span data-ttu-id="547c7-112">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="547c7-112">For example, run:</span></span>
    
        Grant-CsHostedVoicemailPolicy -Identity "Ken Myer" -PolicyName ExRedmond
    
    <span data-ttu-id="547c7-113">In diesem Beispiel wurde dem Benutzer Ken Myers die Richtlinie für die gehostete Voicemail-e-Mail zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="547c7-113">This example assigned the ExRedmond hosted voice mail policy to user Ken Myer.</span></span>
    
    <span data-ttu-id="547c7-114">**Identity** gibt das zu ändernde Benutzerkonto an.</span><span class="sxs-lookup"><span data-stu-id="547c7-114">**Identity** specifies the user account to be modified.</span></span> <span data-ttu-id="547c7-115">Der Identity-Wert kann mit einem der folgenden Formate angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="547c7-115">The Identity value can be specified using any of the following formats:</span></span>
    
      - <span data-ttu-id="547c7-116">Die SIP-Adresse des Benutzers</span><span class="sxs-lookup"><span data-stu-id="547c7-116">The user's SIP address</span></span>
    
      - <span data-ttu-id="547c7-117">Name des Active Directory-Benutzerprinzipals des Benutzers</span><span class="sxs-lookup"><span data-stu-id="547c7-117">The user's Active Directory User-Principal-Name</span></span>
    
      - <span data-ttu-id="547c7-118">Der Domänen \\ Anmeldename des Benutzers (beispielsweise contoso \\ kenmyer)</span><span class="sxs-lookup"><span data-stu-id="547c7-118">The user's domain\\logon name (for example, contoso\\kenmyer)</span></span>
    
      - <span data-ttu-id="547c7-119">Die Active Directory-Domänendienste des Benutzers Display-Name (beispielsweise Ken Myers).</span><span class="sxs-lookup"><span data-stu-id="547c7-119">The user's Active Directory Domain Services Display-Name (for example, Ken Myer).</span></span> <span data-ttu-id="547c7-120">Wenn Sie die Display-Name als Identitätswert verwenden, können Sie das \* Platzhalterzeichen Sternchen () verwenden.</span><span class="sxs-lookup"><span data-stu-id="547c7-120">If using the Display-Name as the Identity value, you can use the asterisk (\*) wildcard character.</span></span> <span data-ttu-id="547c7-121">Die Identität " \* Smith" gibt beispielsweise alle Benutzer zurück, die eine Display-Name haben, die mit dem Zeichenfolgenwert "Smith" endet.</span><span class="sxs-lookup"><span data-stu-id="547c7-121">For example, the Identity "\* Smith" returns all the users who have a Display-Name that ends with the string value "Smith".</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="547c7-122">Der Name des Active Directory-SAM-Kontos des Benutzers kann nicht als Identitätswert verwendet werden, da der Name des SAM-Kontos in der Gesamtstruktur nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="547c7-122">The user’s Active Directory SAM-Account-Name cannot be used as the Identity value because the SAM-Account-Name is not necessarily unique in the forest.</span></span>


