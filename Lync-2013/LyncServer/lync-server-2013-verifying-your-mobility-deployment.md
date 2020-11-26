---
title: 'Lync Server 2013: Überprüfen der Mobilitätsbereitstellung'
description: 'Lync Server 2013: Überprüfen Ihrer Mobilitätsbereitstellung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verifying your mobility deployment
ms:assetid: 72f9b4d3-57b0-4705-9480-cfdca313a70c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690024(v=OCS.15)
ms:contentKeyID: 48184477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eadda35438961e469fdd5fa7976762141b26a385
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438876"
---
# <a name="verifying-your-mobility-deployment-in-lync-server-2013"></a><span data-ttu-id="f13a1-103">Überprüfen der Mobilitätsbereitstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f13a1-103">Verifying your mobility deployment in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f13a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f13a1-104">

<span> </span></span></span>

<span data-ttu-id="f13a1-105">_**Letztes Änderungsdatum des Themas:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="f13a1-105">_**Topic Last Modified:** 2013-02-12_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="f13a1-106">Nachdem Sie den lync Server-Mobilitätsdienst und den lync Server-AutoErmittlungsdienst bereitgestellt haben, führen Sie eine Testtransaktion aus, um sicherzustellen, dass Ihre Bereitstellung ordnungsgemäß funktioniert</span><span class="sxs-lookup"><span data-stu-id="f13a1-106">After you deploy the Lync Server Mobility Service and Lync Server Autodiscover Service, run a test transaction to verify that your deployment works correctly.</span></span> <span data-ttu-id="f13a1-107">Sie können **Test-CsUcwaConference** ausführen, um die Fähigkeit zweier Benutzer zu testen, die lync 2013 Mobile-Clients verwenden, um eine Konferenz zu erstellen, teilzunehmen und zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f13a1-107">You can run **Test-CsUcwaConference** to test the ability of two users who are using Lync 2013 Mobile clients to create, join and communicate in a conference.</span></span> <span data-ttu-id="f13a1-108">Um diese Testtransaktion zu verwenden, benötigen Sie zwei tatsächliche Benutzer oder Testbenutzer sowie Ihre vollständigen Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="f13a1-108">To use this test transaction, you need two actual users or test users, and their full credentials.</span></span>

<span data-ttu-id="f13a1-109">Sie verwenden **Test-CsMcxP2PIM** , um das Senden einer Chatnachricht zwischen zwei Benutzern zu testen, die lync 2010 Mobile verwenden.</span><span class="sxs-lookup"><span data-stu-id="f13a1-109">You use **Test-CsMcxP2PIM** to test sending an instant message between two users who are using Lync 2010 Mobile.</span></span> <span data-ttu-id="f13a1-110">Ähnlich wie bei **Test-CsUcwaConference** verwenden Sie zwei tatsächliche Benutzer oder zwei vordefinierte Testbenutzer.</span><span class="sxs-lookup"><span data-stu-id="f13a1-110">Similar to **Test-CsUcwaConference**, you use two actual users or two predefined test users.</span></span>

<div>

## <a name="to-test-conferencing-for-lync-2013-mobile-clients"></a><span data-ttu-id="f13a1-111">So testen Sie Konferenzen für Mobile lync 2013-Clients</span><span class="sxs-lookup"><span data-stu-id="f13a1-111">To test conferencing for Lync 2013 Mobile clients</span></span>

1.  <span data-ttu-id="f13a1-112">Melden Sie sich als Benutzer mit der Rolle CsAdministrator bei einem Computer an, auf dem die Lync Server-Verwaltungsshell und Ocscore installiert sind.</span><span class="sxs-lookup"><span data-stu-id="f13a1-112">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="f13a1-113">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="f13a1-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f13a1-114">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="f13a1-114">At the command line, type:</span></span>
    
        Test-CsUcwaConference -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -OrganizerSipAddress sip:<SIP address of test user 1> -OrganizerCredential <test user 1 credentials> -ParticipantSipAddress sip:<SIP address of test user 2> -ParticipantCredential <test user 2 credentials> -v
    
    <span data-ttu-id="f13a1-115">Sie können Anmeldeinformationen in einem Skript einrichten und an das Test-Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="f13a1-115">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="f13a1-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f13a1-116">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $testuser1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $testuser2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsUcwaConference -TargetFqdn pool01.contoso.com -Authentication Negotiate -OrganizerSipAddress sip:UserName1@contoso.com -OrganizerCredential $testuser1 -ParticipantSipAddress sip:UserName2@contoso.com -ParticipantCredential $testuser2 -v

</div>

<div>

## <a name="to-test-person-to-person-instant-messaging-im-for-lync-2010-mobile"></a><span data-ttu-id="f13a1-117">So testen Sie die Chat Unterhaltung von Personen zu Personen für lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="f13a1-117">To test person-to-person instant messaging (IM) for Lync 2010 Mobile</span></span>

1.  <span data-ttu-id="f13a1-118">Melden Sie sich als Benutzer mit der Rolle CsAdministrator bei einem Computer an, auf dem die Lync Server-Verwaltungsshell und Ocscore installiert sind.</span><span class="sxs-lookup"><span data-stu-id="f13a1-118">Log on as a member of the CsAdministrator role on any computer where Lync Server Management Shell and Ocscore are installed.</span></span>

2.  <span data-ttu-id="f13a1-119">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="f13a1-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="f13a1-120">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="f13a1-120">At the command line, type:</span></span>
    
        Test-CsMcxP2PIM -TargetFqdn <FQDN of Front End pool> -Authentication <TrustedServer | Negotiate | ClientCertificate | LiveID> -SenderSipAddress sip:<SIP address of test user 1> -SenderCredential <test user 1 credentials> -ReceiverSipAddress sip:<SIP address of test user 2> -ReceiverCredential <test user 2 credentials> -v
    
    <span data-ttu-id="f13a1-121">Sie können Anmeldeinformationen in einem Skript einrichten und an das Test-Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="f13a1-121">You can set credentials in a script and pass them to the test cmdlet.</span></span> <span data-ttu-id="f13a1-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f13a1-122">For example:</span></span>
    
        $passwd1 = ConvertTo-SecureString "Password01" -AsPlainText -Force
        $passwd2 = ConvertTo-SecureString "Password02" -AsPlainText -Force
        $tuc1 = New-Object Management.Automation.PSCredential("contoso\UserName1", $passwd1)
        $tuc2 = New-Object Management.Automation.PSCredential("contoso\UserName2", $passwd2)
        Test-CsMcxP2PIM -TargetFqdn pool01.contoso.com -Authentication Negotiate -SenderSipAddress sip:UserName1@contoso.com -SenderCredential $tuc1 -ReceiverSipAddress sip:UserName2@contoso.com -ReceiverCredential $tuc2 -v

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f13a1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f13a1-123">See Also</span></span>


[<span data-ttu-id="f13a1-124">Test-CsMcxP2PIM</span><span class="sxs-lookup"><span data-stu-id="f13a1-124">Test-CsMcxP2PIM</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM)  
[<span data-ttu-id="f13a1-125">Test-CsUcwaConference</span><span class="sxs-lookup"><span data-stu-id="f13a1-125">Test-CsUcwaConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsUcwaConference)  
  

<span data-ttu-id="f13a1-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f13a1-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

