---
title: 'Lync Server 2013: Testen von Nachrichten mithilfe von XMPP'
description: 'Lync Server 2013: Testen von Nachrichten mithilfe von xmpp.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing messaging using XMPP
ms:assetid: ae5305ba-e5fc-4ca0-a805-872b4ebaf981
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727312(v=OCS.15)
ms:contentKeyID: 63969641
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 06faeae0a6104351f9102de31c76b2424a140deb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441004"
---
# <a name="testing-messaging-using-xmpp-in-lync-server-2013"></a><span data-ttu-id="c60c4-103">Testen von Nachrichten mithilfe von xmpp in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c60c4-103">Testing messaging using XMPP in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c60c4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c60c4-104">

<span> </span></span></span>

<span data-ttu-id="c60c4-105">_**Letztes Änderungsdatum des Themas:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="c60c4-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c60c4-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="c60c4-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c60c4-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="c60c4-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c60c4-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="c60c4-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c60c4-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c60c4-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c60c4-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="c60c4-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c60c4-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="c60c4-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="c60c4-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsXmppIM-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="c60c4-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsXmppIM</strong> cmdlet.</span></span> <span data-ttu-id="c60c4-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="c60c4-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsXmppIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c60c4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c60c4-114">Description</span></span>

<span data-ttu-id="c60c4-115">Das Extensible Messaging and Presence Protocol (XMPP) ist ein Standardkommunikationsprotokoll (basierend auf XML), das für das Senden von Nachrichten über das Internet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c60c4-115">The Extensible Messaging and Presence Protocol (XMPP) is a standard communications protocol (based on XML) used for sending messages across the Internet.</span></span> <span data-ttu-id="c60c4-116">XMPP wurde ursprünglich Jabber genannt und wird von verschiedenen Internet-Messaging-und Kommunikationsanwendungen wie Google Talk und Facebook-Chat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c60c4-116">XMPP was originally named Jabber, and is supported by several Internet messaging and communication applications, such as Google Talk and Facebook Chat.</span></span> <span data-ttu-id="c60c4-117">Das Cmdlet **Test-CsXmppIM** überprüft, ob ein Benutzer Sofortnachrichten mit einem Benutzer in einem XMPP-Netzwerk austauschen kann.</span><span class="sxs-lookup"><span data-stu-id="c60c4-117">The **Test-CsXmppIM** cmdlet verifies that a user can exchange instant messages with a user on an XMPP network.</span></span> <span data-ttu-id="c60c4-118">Beachten Sie, dass Sie für diesen Test erfolgreich sein müssen, wenn Sie über eine gültige SIP-Adresse für den XMPP-Benutzer verfügen und diese SIP-Adresse in einem Netzwerk vorhanden sein muss, das als zugelassener XMPP-Partner konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c60c4-118">Note that, for this test to succeed, you must have a valid SIP address for the XMPP user, and that SIP address must be on a network that was configured as an allowed XMPP partner.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c60c4-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="c60c4-119">Running the test</span></span>

<span data-ttu-id="c60c4-120">Im folgenden Beispiel werden die Funktionen des XMPP-Chats für den Pool ATL-CS-001.litwareinc.com überprüft.</span><span class="sxs-lookup"><span data-stu-id="c60c4-120">The following example verifies the XMPP instant messaging capabilities for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="c60c4-121">Dieser Befehl funktioniert nur, wenn Testbenutzer für den Pool ATL-CS-001.litwareinc.com definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c60c4-121">This command will work only if test users are defined for the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="c60c4-122">Wenn ja, bestimmt der Befehl, ob der erste Testbenutzer eine XMPP-Sofortnachricht an einen Benutzer senden kann, der über die SIP-Adresse adelaney@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="c60c4-122">If they have, then the command will determine whether the first test user can send an XMPP instant message to a user who has the SIP address adelaney@contoso.com.</span></span>

<span data-ttu-id="c60c4-123">Wenn Testbenutzer nicht definiert sind, schlägt der Befehl fehl, da er nicht weiß, zu welchem Benutzer Sie sich anmelden müssen.</span><span class="sxs-lookup"><span data-stu-id="c60c4-123">If test users are not defined, then the command will fail because it won't know which user to log on as.</span></span> <span data-ttu-id="c60c4-124">Wenn Sie für einen Pool keine Testbenutzer definiert haben, müssen Sie den "usersipaddress"-Parameter und die Anmeldeinformationen des Benutzers einbeziehen, der beim Versuch, sich anzumelden, verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c60c4-124">If you have not defined test users for a pool, then you must include the UserSipAddress parameter and the credentials of the user who the command should use when trying to log on.</span></span>

    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com"

<span data-ttu-id="c60c4-125">Die im nächsten Beispiel gezeigten Befehle testen die Möglichkeit eines bestimmten Benutzers ("litwareinc \\ Pilar), sich anzumelden, um eine XMPP-Sofortnachricht an den Benutzer adelaney@contoso.com zu senden.</span><span class="sxs-lookup"><span data-stu-id="c60c4-125">The commands shown in the next example test the ability of a specific user (litwareinc\\pilar) to log on to send an XMPP instant message to the user adelaney@contoso.com.</span></span> <span data-ttu-id="c60c4-126">Dazu wird im ersten Befehl im Beispiel das Get-Credential-Cmdlet verwendet, um ein Windows PowerShell-Befehlszeilen-Schnittstellen Anmeldeinformationsobjekt zu erstellen, das den Namen und das Kennwort des Benutzers Pilar Ackerman enthält.</span><span class="sxs-lookup"><span data-stu-id="c60c4-126">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="c60c4-127">(Da der Anmeldename "litwareinc \\ Pilar als Parameter enthalten war, erfordert das Windows PowerShell-Dialogfeld Anmelde Informationsanforderung nur den Administrator, das Kennwort für das Pilar Ackerman-Konto einzugeben.) Das resultierende Anmeldeinformationsobjekt wird dann in einer Variablen mit dem Namen $cred 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c60c4-127">(Because the logon name litwareinc\\pilar was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credential object is then stored in a variable named $cred1.</span></span>

<span data-ttu-id="c60c4-128">Der zweite Befehl überprüft dann, ob sich dieser Benutzer beim Pool ATL-CS-001.litwareinc.com anmelden und die XMPP-Sofortnachricht senden kann.</span><span class="sxs-lookup"><span data-stu-id="c60c4-128">The second command then checks whether this user can log on to the pool atl-cs-001.litwareinc.com and send the XMPP instant message.</span></span> <span data-ttu-id="c60c4-129">Zum Ausführen dieser Aufgabe wird das Cmdlet **Test-CsXmppIm** zusammen mit vier Parametern aufgerufen: TargetFqdn (der FQDN des registrierungspools); Receiver (die SIP-Adresse des Benutzers, an den die Nachricht adressiert wird) UserCredential (das Windows PowerShell-Objekt, das die Benutzeranmeldeinformationen von Pilar Ackerman enthält); und "usersipaddress" (die SIP-Adresse, die den angegebenen Benutzeranmeldeinformationen entspricht).</span><span class="sxs-lookup"><span data-stu-id="c60c4-129">To run this task, the **Test-CsXmppIm** cmdlet is called, together with four parameters: TargetFqdn (the FQDN of the Registrar pool); Receiver (the SIP address of the user the message is being addressed to); UserCredential (the Windows PowerShell object that contains Pilar Ackerman’s user credentials); and UserSipAddress (the SIP address that corresponds to the supplied user credentials).</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    
    Test-CsXmppIM -TargetFqdn "atl-cs-001.litwareinc.com" -Receiver "adelany@contoso.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c60c4-130">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="c60c4-130">Determining success or failure</span></span>

<span data-ttu-id="c60c4-131">Wenn XMPP Instant Messaging ordnungsgemäß konfiguriert ist, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="c60c4-131">If XMPP instant messaging is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="c60c4-132">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c60c4-132">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c60c4-133">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="c60c4-133">Result : Success</span></span>

<span data-ttu-id="c60c4-134">Latenz: 00:00:02.5361946</span><span class="sxs-lookup"><span data-stu-id="c60c4-134">Latency : 00:00:02.5361946</span></span>

<span data-ttu-id="c60c4-135">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="c60c4-135">Error Message :</span></span>

<span data-ttu-id="c60c4-136">Diagnose</span><span class="sxs-lookup"><span data-stu-id="c60c4-136">Diagnosis :</span></span>

<span data-ttu-id="c60c4-137">Wenn die angegebenen Benutzer keine XMPP-Sofortnachrichten verwenden können, wird das Ergebnis als **Fehler** angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="c60c4-137">If the specified users can't use XMPP instant messaging, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="c60c4-138">Warnung: Fehler beim Lesen der Registrierungsstellen-Portnummer für die angegebene vollqualifizierte</span><span class="sxs-lookup"><span data-stu-id="c60c4-138">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="c60c4-139">Domänenname (FQDN).</span><span class="sxs-lookup"><span data-stu-id="c60c4-139">domain name (FQDN).</span></span> <span data-ttu-id="c60c4-140">Verwenden der standardmäßigen Registrierungs Portnummer</span><span class="sxs-lookup"><span data-stu-id="c60c4-140">Using default Registrar port number.</span></span> <span data-ttu-id="c60c4-141">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="c60c4-141">Exception:</span></span>

<span data-ttu-id="c60c4-142">System. InvalidOperationException: kein übereinstimmender Cluster in der Topologie gefunden.</span><span class="sxs-lookup"><span data-stu-id="c60c4-142">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="c60c4-143">am</span><span class="sxs-lookup"><span data-stu-id="c60c4-143">at</span></span>

<span data-ttu-id="c60c4-144">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="c60c4-144">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="c60c4-145">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="c60c4-145">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="c60c4-146">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c60c4-146">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c60c4-147">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="c60c4-147">Result : Failure</span></span>

<span data-ttu-id="c60c4-148">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c60c4-148">Latency : 00:00:00</span></span>

<span data-ttu-id="c60c4-149">Fehlermeldung: 10060, Fehler bei einem Verbindungsversuch, weil die verbundene Partei</span><span class="sxs-lookup"><span data-stu-id="c60c4-149">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="c60c4-150">hat nach einer bestimmten Zeit nicht richtig reagiert, oder</span><span class="sxs-lookup"><span data-stu-id="c60c4-150">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="c60c4-151">Fehler beim Herstellen einer Verbindung, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="c60c4-151">established connection failed because connected host has</span></span>

<span data-ttu-id="c60c4-152">Fehler beim Antworten 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="c60c4-152">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="c60c4-153">Innere Ausnahme: ein Verbindungsversuch ist fehlgeschlagen, da die</span><span class="sxs-lookup"><span data-stu-id="c60c4-153">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="c60c4-154">die verbundene Partei hat nach einer gewissen Zeit nicht richtig reagiert</span><span class="sxs-lookup"><span data-stu-id="c60c4-154">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="c60c4-155">Zeit, oder die Verbindung konnte nicht hergestellt werden, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="c60c4-155">time, or established connection failed because connected host</span></span>

<span data-ttu-id="c60c4-156">Fehler beim Antworten 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="c60c4-156">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="c60c4-157">Diagnose</span><span class="sxs-lookup"><span data-stu-id="c60c4-157">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c60c4-158">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="c60c4-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="c60c4-159">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsXmppIM** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="c60c4-159">Here are some common reasons why **Test-CsXmppIM** might fail:</span></span>

  - <span data-ttu-id="c60c4-160">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c60c4-160">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c60c4-161">Wenn die optionalen Parameter verwendet werden, müssen Sie ordnungsgemäß konfiguriert sein, oder der Test schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="c60c4-161">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c60c4-162">Führen Sie den Befehl ohne die optionalen Parameter erneut aus, und überprüfen Sie, ob dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c60c4-162">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c60c4-163">Dieser Befehl schlägt fehl, wenn die XMPP-Gateway-Konfiguration falsch konfiguriert oder noch nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c60c4-163">This command will fail if XMPP gateway configuration is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c60c4-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c60c4-164">See Also</span></span>


[<span data-ttu-id="c60c4-165">Set-CsXmppGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="c60c4-165">Set-CsXmppGatewayConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsXmppGatewayConfiguration)  
  

<span data-ttu-id="c60c4-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c60c4-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

