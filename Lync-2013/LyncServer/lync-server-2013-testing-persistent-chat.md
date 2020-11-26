---
title: 'Lync Server 2013: Testen des beständigen Chats'
description: 'Lync Server 2013: Testen des beständigen Chats.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing persistent chat
ms:assetid: d351b6f2-bc31-42e0-9e8d-c347713d6b4a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727313(v=OCS.15)
ms:contentKeyID: 63969651
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8b1dc4eef1870f1287dacdc1852ab1e24edd169
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440997"
---
# <a name="testing-persistent-chat-in-lync-server-2013"></a><span data-ttu-id="6f36c-103">Testen des beständigen Chats in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f36c-103">Testing persistent chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f36c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f36c-104">

<span> </span></span></span>

<span data-ttu-id="6f36c-105">_**Letztes Änderungsdatum des Themas:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="6f36c-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f36c-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="6f36c-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="6f36c-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="6f36c-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f36c-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="6f36c-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="6f36c-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="6f36c-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f36c-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="6f36c-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="6f36c-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="6f36c-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="6f36c-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsPersistentChatMessage-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="6f36c-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsPersistentChatMessage</strong> cmdlet.</span></span> <span data-ttu-id="6f36c-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="6f36c-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPersistentChatMessage&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="6f36c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f36c-114">Description</span></span>

<span data-ttu-id="6f36c-115">Das Cmdlet **Test-CsPersistentChatMessage** überprüft, ob ein paar Testbenutzer Nachrichten mithilfe des beständigen Chat Diensts austauschen können.</span><span class="sxs-lookup"><span data-stu-id="6f36c-115">The **Test-CsPersistentChatMessage** cmdlet verifies that a pair of test users can exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="6f36c-116">Zu diesem Zweck protokolliert das Cmdlet die beiden Benutzer in lync Server 2013, verbindet die Benutzer mit einem beständigen Chatroom, tauscht ein paar Nachrichten aus, beendet den Chatroom und loggt sich von den beiden Benutzern ab.</span><span class="sxs-lookup"><span data-stu-id="6f36c-116">To do this, the cmdlet logs the two users on to Lync Server 2013, connects the users to a persistent Chat room, exchanges a pair of messages, then exits the chat room and logs off the two users.</span></span> <span data-ttu-id="6f36c-117">Beachten Sie, dass beim Aufrufen dieses Cmdlets ein Fehler auftritt, wenn Sie keine Chatrooms erstellt haben oder wenn den beiden Testbenutzerkonten keine Richtlinie für beständigen Chat zugewiesen wird, die Ihnen den Zugriff auf den beständigen Chatdienst gewährt.</span><span class="sxs-lookup"><span data-stu-id="6f36c-117">Note that calls to this cmdlet will fail if you have not created any chat rooms or if the two test user accounts are not assigned a Persistent Chat policy that gives them access to the Persistent Chat service.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="6f36c-118">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="6f36c-118">Running the test</span></span>

<span data-ttu-id="6f36c-119">Mit den im folgenden Beispiel gezeigten Befehlen testen Sie die Fähigkeit eines Benutzer Paars ("litwareinc \\ Pilar und" litwareinc \\ kenmyer), sich bei lync Server 2013 anzumelden und dann Nachrichten mithilfe des beständigen Chat Diensts auszutauschen.</span><span class="sxs-lookup"><span data-stu-id="6f36c-119">The commands shown in the following example test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to log on to Lync Server 2013 and then exchange messages using the Persistent Chat service.</span></span> <span data-ttu-id="6f36c-120">Dazu verwendet der erste Befehl im Beispiel das Cmdlet " **Get-Credential** ", um ein Windows PowerShell-Anmeldeinformationsobjekt für die Befehlszeilenschnittstelle zu erstellen, das den Namen und das Kennwort des Benutzers Pilar Ackerman enthält.</span><span class="sxs-lookup"><span data-stu-id="6f36c-120">To do this, the first command in the example uses the **Get-Credential** cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="6f36c-121">(Da der Anmeldename, "litwareinc \\ Pilar, als Parameter enthalten war, erfordert das Dialogfeld Windows PowerShell-Anmeldeinformationen nur, dass der Administrator das Kennwort für das Pilar Ackerman-Konto eingegeben hat.) Das resultierende Credentials-Objekt wird dann in einer Variablen mit dem Namen $cred 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6f36c-121">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="6f36c-122">Der zweite Befehl führt dieselbe Aufgabe aus, wobei dieses Mal ein Anmeldeinformationsobjekt für das Ken Myers-Konto zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f36c-122">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="6f36c-123">Wenn die Anmeldeinformationsobjekte in der Hand sind, bestimmt der dritte Befehl, ob sich diese beiden Benutzer bei lync Server 2013 anmelden und Nachrichten mithilfe des beständigen Chats austauschen können.</span><span class="sxs-lookup"><span data-stu-id="6f36c-123">With the credential objects in hand, the third command determines whether these two users can log on to Lync Server 2013 and exchange messages using Persistent Chat.</span></span> <span data-ttu-id="6f36c-124">Um diese Aufgabe auszuführen, wird das Cmdlet **Test-CsPersistentChatMessage** mit den folgenden Parametern aufgerufen: TargetFqdn (der FQDN des registrierungspools); SenderSipAddress (die SIP-Adresse des ersten Testbenutzers); SenderCredential (das Windows PowerShell-Objekt, das die Anmeldeinformationen für denselben Benutzer enthält); ReceiverSipAddress (die SIP-Adresse des anderen Testbenutzers); und ReceiverCredential (das Windows PowerShell-Objekt, das die Anmeldeinformationen für den anderen Testbenutzer enthält).</span><span class="sxs-lookup"><span data-stu-id="6f36c-124">To perform this task, the **Test-CsPersistentChatMessage** cmdlet is called using the following parameters: TargetFqdn (the FQDN of the Registrar pool); SenderSipAddress (the SIP address for the first test user); SenderCredential (the Windows PowerShell object that contains the credentials for this same user); ReceiverSipAddress (the SIP address for the other test user); and ReceiverCredential (the Windows PowerShell object that contains the credentials for the other test user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    
    Test-CsPersistentChatMessage -TargetFqdn atl-persistentchat-001.litwareinc.com -SenderSipAddress "sip:pilar@litwareinc.com" -SenderCredential $cred1 -ReceiverSipAddress "sip:kenmyer@litwareinc.com" -ReceiverCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="6f36c-125">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="6f36c-125">Determining success or failure</span></span>

<span data-ttu-id="6f36c-126">Wenn der angegebene Benutzer über eine gültige Standortrichtlinie verfügt, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als **erfolgreich** markiert ist:</span><span class="sxs-lookup"><span data-stu-id="6f36c-126">If the specified user has a valid location policy, then you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="6f36c-127">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6f36c-127">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6f36c-128">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="6f36c-128">Result : Success</span></span>

<span data-ttu-id="6f36c-129">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="6f36c-129">Latency : 00:00:00</span></span>

<span data-ttu-id="6f36c-130">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="6f36c-130">Error Message :</span></span>

<span data-ttu-id="6f36c-131">Diagnose</span><span class="sxs-lookup"><span data-stu-id="6f36c-131">Diagnosis :</span></span>

<span data-ttu-id="6f36c-132">Wenn die angegebenen Benutzer Nachrichten nicht mithilfe des beständigen Chat Diensts austauschen können, wird das Ergebnis als **Fehler** angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="6f36c-132">If the specified users can't exchange messages using the Persistent Chat service, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="6f36c-133">Warnung: Fehler beim Lesen der Registrierungsstellen-Portnummer für die angegebene vollqualifizierte</span><span class="sxs-lookup"><span data-stu-id="6f36c-133">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="6f36c-134">Domänenname (FQDN).</span><span class="sxs-lookup"><span data-stu-id="6f36c-134">domain name (FQDN).</span></span> <span data-ttu-id="6f36c-135">Verwenden der standardmäßigen Registrierungs Portnummer</span><span class="sxs-lookup"><span data-stu-id="6f36c-135">Using default Registrar port number.</span></span> <span data-ttu-id="6f36c-136">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="6f36c-136">Exception:</span></span>

<span data-ttu-id="6f36c-137">System. InvalidOperationException: kein übereinstimmender Cluster in der Topologie gefunden.</span><span class="sxs-lookup"><span data-stu-id="6f36c-137">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="6f36c-138">am</span><span class="sxs-lookup"><span data-stu-id="6f36c-138">at</span></span>

<span data-ttu-id="6f36c-139">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="6f36c-139">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="6f36c-140">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="6f36c-140">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="6f36c-141">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="6f36c-141">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="6f36c-142">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="6f36c-142">Result : Failure</span></span>

<span data-ttu-id="6f36c-143">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="6f36c-143">Latency : 00:00:00</span></span>

<span data-ttu-id="6f36c-144">Fehlermeldung: 10060, Fehler bei einem Verbindungsversuch, weil die verbundene Partei</span><span class="sxs-lookup"><span data-stu-id="6f36c-144">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="6f36c-145">hat nach einer bestimmten Zeit nicht richtig reagiert, oder</span><span class="sxs-lookup"><span data-stu-id="6f36c-145">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="6f36c-146">Fehler beim Herstellen einer Verbindung, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="6f36c-146">established connection failed because connected host has</span></span>

<span data-ttu-id="6f36c-147">Fehler bei der Antwort \[ 2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="6f36c-147">failed to respond \[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="6f36c-148">Innere Ausnahme: ein Verbindungsversuch ist fehlgeschlagen, da die</span><span class="sxs-lookup"><span data-stu-id="6f36c-148">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="6f36c-149">die verbundene Partei hat nach einer gewissen Zeit nicht richtig reagiert</span><span class="sxs-lookup"><span data-stu-id="6f36c-149">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="6f36c-150">Zeit, oder die Verbindung konnte nicht hergestellt werden, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="6f36c-150">time, or established connection failed because connected host</span></span>

<span data-ttu-id="6f36c-151">hat nicht reagiert</span><span class="sxs-lookup"><span data-stu-id="6f36c-151">has failed to respond</span></span>

<span data-ttu-id="6f36c-152">\[2001:4898: E8: f39e: 5c9a: ad83:81b3:9944 \] : 5061</span><span class="sxs-lookup"><span data-stu-id="6f36c-152">\[2001:4898:e8:f39e:5c9a:ad83:81b3:9944\]:5061</span></span>

<span data-ttu-id="6f36c-153">Diagnose</span><span class="sxs-lookup"><span data-stu-id="6f36c-153">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="6f36c-154">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="6f36c-154">Reasons why the test might have failed</span></span>

<span data-ttu-id="6f36c-155">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsPersistentChatMessage** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="6f36c-155">Here are some common reasons why **Test-CsPersistentChatMessage** might fail:</span></span>

  - <span data-ttu-id="6f36c-156">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f36c-156">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="6f36c-157">Die erforderlichen Testkonten sind möglicherweise nicht vorhanden oder wurden ordnungsgemäß erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f36c-157">The required test accounts may not exist or have been correctly created.</span></span>

  - <span data-ttu-id="6f36c-158">Möglicherweise hat ein Netzwerkproblem zu einer unerwarteten Verzögerung geführt, bei der der Test zeitverzögert wurde.</span><span class="sxs-lookup"><span data-stu-id="6f36c-158">There may have been a network issue causing an unexpected delay which timed out the test.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f36c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f36c-159">See Also</span></span>


[<span data-ttu-id="6f36c-160">Grant-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="6f36c-160">Grant-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsPersistentChatPolicy)  
[<span data-ttu-id="6f36c-161">New-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="6f36c-161">New-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsPersistentChatPolicy)  
[<span data-ttu-id="6f36c-162">Set-CsPersistentChatPolicy</span><span class="sxs-lookup"><span data-stu-id="6f36c-162">Set-CsPersistentChatPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsPersistentChatPolicy)  
  

<span data-ttu-id="6f36c-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f36c-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

