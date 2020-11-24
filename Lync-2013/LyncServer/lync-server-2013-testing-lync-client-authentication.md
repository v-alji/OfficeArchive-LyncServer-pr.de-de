---
title: 'Lync Server 2013: Testen der lync-Client Authentifizierung'
description: 'Lync Server 2013: Testen der lync-Client Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Lync Client authentication
ms:assetid: e22114cb-4456-4e5f-93ab-51592c4a8209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn689120(v=OCS.15)
ms:contentKeyID: 63969659
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03694b7fd56d7847d8d493304b97af335d2a5b4d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394487"
---
# <a name="testing-lync-client-authentication-in-lync-server-2013"></a><span data-ttu-id="b8ea5-103">Testen der lync-Client Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8ea5-103">Testing Lync Client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8ea5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8ea5-104">

<span> </span></span></span>

<span data-ttu-id="b8ea5-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="b8ea5-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8ea5-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="b8ea5-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b8ea5-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="b8ea5-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ea5-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="b8ea5-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b8ea5-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8ea5-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ea5-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b8ea5-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b8ea5-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b8ea5-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsClientAuth-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="b8ea5-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsClientAuth&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b8ea5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8ea5-114">Description</span></span>

<span data-ttu-id="b8ea5-115">Mithilfe des Test-CsClientAuth-Cmdlets können Sie ermitteln, ob ein Benutzer sich mit einem Clientzertifikat am lync-Server anmelden kann, indem Sie das Test-CsClientAuth-Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-115">The Test-CsClientAuth cmdlet enables you to determine whether a user can log on to the Lync Server by using a client certificate, you can run the Test-CsClientAuth cmdlet.</span></span> <span data-ttu-id="b8ea5-116">Nach dem Aufruf von Test-CsClientAuth wird das Cmdlet mit dem Dienst für die Zertifikatbereitstellung Kontakt aufnehmen und eine Kopie aller Clientzertifikate für den angegebenen Benutzer herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-116">After calling Test-CsClientAuth, the cmdlet will contact the certificate provisioning service and download a copy of any client certificates for the specified user.</span></span> <span data-ttu-id="b8ea5-117">Wenn ein Clientzertifikat gefunden und heruntergeladen werden kann, versucht Test-CsClientAuth, sich mit diesem Zertifikat anzumelden.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-117">If a client certificate can be found and downloaded, Test-CsClientAuth will then attempt to log on by using that certificate.</span></span> <span data-ttu-id="b8ea5-118">Wenn die Anmeldung erfolgreich ist, wird sich Test-CsClientAuth abmelden und melden, dass der Test erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-118">If logon succeeds, Test-CsClientAuth will log off and report that the test succeeded.</span></span> <span data-ttu-id="b8ea5-119">Wenn ein Zertifikat nicht gefunden oder heruntergeladen werden kann oder wenn sich das Cmdlet nicht mit diesem Zertifikat anmelden kann, meldet Test-CsClientAuth, dass der Test fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-119">If a certificate cannot be found or downloaded, or if the cmdlet is unable to logon using that certificate, then Test-CsClientAuth will report that the test failed.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b8ea5-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="b8ea5-120">Running the test</span></span>

<span data-ttu-id="b8ea5-121">Das Test-CsClientAuth-Cmdlet wird mit dem Konto eines beliebigen Benutzers ausgeführt, der für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-121">The Test-CsClientAuth cmdlet is run by using the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="b8ea5-122">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie zuerst ein Windows PowerShell-Anmeldeinformationsobjekt erstellen, das den Kontonamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-122">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="b8ea5-123">Sie müssen dann das Anmeldeinformationsobjekt und die SIP-Adresse einbeziehen, die dem Konto zugewiesen ist, wenn das System Test-CsClientAuth aufruft:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-123">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsClientAuth:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="b8ea5-124">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8ea5-124">For more information, see the Help documentation for the [Test-CsClientAuth](https://technet.microsoft.com/library/gg398712\(v=ocs.14\).aspx) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b8ea5-125">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="b8ea5-125">Determining success or failure</span></span>

<span data-ttu-id="b8ea5-126">Wenn sich der angegebene Benutzer mit einem Clientzertifikat bei lync Server anmelden kann, wird die Ausgabe ähnlich wie diese angezeigt, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="b8ea5-126">If the specified user can log on to Lync Server by using a client certificate, you will receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="b8ea5-127">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b8ea5-127">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b8ea5-128">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="b8ea5-128">Result : Success</span></span>

<span data-ttu-id="b8ea5-129">Latenz: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="b8ea5-129">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="b8ea5-130">Fehler</span><span class="sxs-lookup"><span data-stu-id="b8ea5-130">Error :</span></span>

<span data-ttu-id="b8ea5-131">Diagnose</span><span class="sxs-lookup"><span data-stu-id="b8ea5-131">Diagnosis :</span></span>

<span data-ttu-id="b8ea5-132">Wenn der angegebene Benutzer sich nicht anmelden kann, wird das Ergebnis als Fehler angezeigt, und zusätzliche Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-132">If the specified user can not log on, the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="b8ea5-133">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="b8ea5-133">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="b8ea5-134">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="b8ea5-134">Result : Failure</span></span>

<span data-ttu-id="b8ea5-135">Latenz: 00:00:03.3645259</span><span class="sxs-lookup"><span data-stu-id="b8ea5-135">Latency : 00:00:03.3645259</span></span>

<span data-ttu-id="b8ea5-136">Fehler: Es konnte kein CS-Zertifikat für den angegebenen Benutzer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-136">Error : Could not download a CS Certificate for the given user.</span></span> <span data-ttu-id="b8ea5-137">Überprüfen Sie, ob</span><span class="sxs-lookup"><span data-stu-id="b8ea5-137">Check if</span></span>

<span data-ttu-id="b8ea5-138">der angegebene URI und die Anmeldeinformationen sind richtig.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-138">provided uri and credentials are correct.</span></span>

<span data-ttu-id="b8ea5-139">Diagnose</span><span class="sxs-lookup"><span data-stu-id="b8ea5-139">Diagnosis :</span></span>

<span data-ttu-id="b8ea5-140">In der vorherigen Ausgabe wird beispielsweise angegeben, dass der Test fehlgeschlagen ist, da für den angegebenen Benutzer kein gültiges Clientzertifikat gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-140">For example, the previous output states that the test failed because a valid client certificate couldn't be located for the specified user.</span></span> <span data-ttu-id="b8ea5-141">Sie können eine Liste der für einen Benutzer ausgestellten Clientzertifikate zurückgeben, indem Sie einen Befehl wie folgt ausführen:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-141">You can return a list of the client certificates issued to a user by running a command as follows:</span></span>

    Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="b8ea5-142">Wenn Test-CsClientAuth fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-142">If Test-CsClientAuth fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsClientAuth -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential -Verbose

<span data-ttu-id="b8ea5-143">Wenn der Verbose-Parameter enthalten ist, gibt Test-CsClientAuth eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-143">When the Verbose parameter is included, Test-CsClientAuth will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="b8ea5-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-144">For example:</span></span>

<span data-ttu-id="b8ea5-145">Versuch, ein CS-Zertifikat für Benutzer herunterzuladen: kenmyer@litwareinc.com-Endpunkt: Schritt-Nr</span><span class="sxs-lookup"><span data-stu-id="b8ea5-145">Trying to download a CS certificate for User : kenmyer@litwareinc.com endpoint : STEpid</span></span>

<span data-ttu-id="b8ea5-146">Webdienst-URL: https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span><span class="sxs-lookup"><span data-stu-id="b8ea5-146">Web Service url : https://atl-cs-001.litwareinc.com:443/CertProv/CertprovisioningService.svc</span></span>

<span data-ttu-id="b8ea5-147">CS-Zertifikat konnte nicht vom Webdienst heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-147">Could not download a CS certificate from web service.</span></span>

<span data-ttu-id="b8ea5-148">Kontroll</span><span class="sxs-lookup"><span data-stu-id="b8ea5-148">CHECK:</span></span>

<span data-ttu-id="b8ea5-149">\- Die Webdienst-URL ist gültig, und die Webdienste funktionieren.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-149">\- Web service url is valid and the web services are functional</span></span>

<span data-ttu-id="b8ea5-150">\-Wenn \\ \\ Sie die PhoneNo-Pin zur Authentifizierung verwenden, stellen Sie sicher, dass Sie mit dem Benutzer-URI übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="b8ea5-150">\- If using PhoneNo\\\\Pin to authenticate, make sure they match the user uri</span></span>

<span data-ttu-id="b8ea5-151">\- Stellen Sie bei Verwendung der NTLM \\ -Kerberos-Authentifizierung sicher, dass Sie gültige Anmeldeinformationen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-151">\- If using NTLM\\Kerberos auth, make sure you provided valid credentials</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b8ea5-152">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="b8ea5-152">Reasons why the test might have failed</span></span>

<span data-ttu-id="b8ea5-153">Im folgenden finden Sie einige häufige Gründe, warum Test-CsClientAuth fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-153">Here are some common reasons why Test-CsClientAuth might fail:</span></span>

  - <span data-ttu-id="b8ea5-154">Sie haben ein ungültiges Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-154">You specified a user account that was not valid.</span></span> <span data-ttu-id="b8ea5-155">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-155">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="b8ea5-156">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-156">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="b8ea5-157">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-157">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="b8ea5-158">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-158">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="b8ea5-159">Der Testbenutzer verfügt möglicherweise nicht über ein gültiges Clientzertifikat.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-159">The test user might not have a valid client certificate.</span></span> <span data-ttu-id="b8ea5-160">Sie können Informationen zu den einem Benutzer zugewiesenen Clientzertifikaten mithilfe eines Befehls zurückgeben, der dem folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="b8ea5-160">You can return information about the client certificates assigned to a user by using a command similar to this:</span></span>
    
        Get-CsClientCertificate -Identity "sip:kenmyer@litwareinc.com"

<span data-ttu-id="b8ea5-161"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8ea5-161"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

