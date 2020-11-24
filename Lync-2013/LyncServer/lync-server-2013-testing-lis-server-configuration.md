---
title: 'Lync Server 2013: Testen der LIS-Serverkonfiguration'
description: 'Lync Server 2013: Testen der LIS-Serverkonfiguration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing LIS server configuration
ms:assetid: 6b06e7ab-522f-41a2-878b-e89cd4e3c6da
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690129(v=OCS.15)
ms:contentKeyID: 63969614
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4d16d2ce48e3e5bb89e863f02902d05ce77bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394502"
---
# <a name="testing-lis-server-configuration-in-lync-server-2013"></a><span data-ttu-id="a8d1a-103">Testen der LIS-Serverkonfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8d1a-103">Testing LIS server configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8d1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8d1a-104">

<span> </span></span></span>

<span data-ttu-id="a8d1a-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="a8d1a-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8d1a-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="a8d1a-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="a8d1a-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="a8d1a-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8d1a-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="a8d1a-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="a8d1a-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8d1a-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8d1a-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a8d1a-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="a8d1a-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="a8d1a-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsLisConfiguration-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsLisConfiguration cmdlet.</span></span> <span data-ttu-id="a8d1a-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="a8d1a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8d1a-114">Description</span></span>

<span data-ttu-id="a8d1a-115">Das Test-CsLisConfiguration-Cmdlet überprüft Ihre Fähigkeit, den LIS-Webdienst zu kontaktieren.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-115">The Test-CsLisConfiguration cmdlet verifies your ability to contact the LIS web service.</span></span> <span data-ttu-id="a8d1a-116">Wenn der Webdienst kontaktiert werden kann, wird der Test als Erfolg betrachtet, unabhängig davon, ob bestimmte Speicherorte gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-116">If the web service can be contacted, then the test will be considered a success, regardless of whether any specific locations can be found.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="a8d1a-117">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="a8d1a-117">Running the test</span></span>

<span data-ttu-id="a8d1a-118">Das Test-CsLisConfguration-Cmdlet kann entweder mit einem vorkonfigurierten Test Konto ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder dem Konto eines beliebigen Benutzers, der für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-118">The Test-CsLisConfguration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="a8d1a-119">Um diese Überprüfung mit einem Testkonto auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools angeben.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-119">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="a8d1a-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-120">For example:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="a8d1a-121">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie zuerst ein Windows PowerShell-Anmeldeinformationsobjekt erstellen, das den Kontonamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-121">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="a8d1a-122">Sie müssen das Anmeldeinformationen-Objekt und die SIP-Adresse, die dem Konto zugewiesen ist, beim Aufrufen von Test-CsLisConfiguration einfügen:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-122">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsLisConfiguration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="a8d1a-123">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="a8d1a-123">For more information, see the Help documentation for the [Test-CsLisConfiguration](https://docs.microsoft.com/powershell/module/skype/Test-CsLisConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="a8d1a-124">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="a8d1a-124">Determining success or failure</span></span>

<span data-ttu-id="a8d1a-125">Wenn der LIS ordnungsgemäß konfiguriert ist, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="a8d1a-125">If the LIS is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="a8d1a-126">TargetUri https://atl-cs-001.litwareinc.com:443/locationinformation/</span><span class="sxs-lookup"><span data-stu-id="a8d1a-126">TargetUri : https://atl-cs-001.litwareinc.com:443/locationinformation/</span></span>

<span data-ttu-id="a8d1a-127">liservice. svc</span><span class="sxs-lookup"><span data-stu-id="a8d1a-127">liservice.svc</span></span>

<span data-ttu-id="a8d1a-128">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a8d1a-128">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a8d1a-129">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="a8d1a-129">Result : Success</span></span>

<span data-ttu-id="a8d1a-130">Latenz: 00:00:06.1616913</span><span class="sxs-lookup"><span data-stu-id="a8d1a-130">Latency : 00:00:06.1616913</span></span>

<span data-ttu-id="a8d1a-131">Fehler</span><span class="sxs-lookup"><span data-stu-id="a8d1a-131">Error :</span></span>

<span data-ttu-id="a8d1a-132">Diagnose</span><span class="sxs-lookup"><span data-stu-id="a8d1a-132">Diagnosis :</span></span>

<span data-ttu-id="a8d1a-133">Wenn sich der angegebene Benutzer nicht anmelden oder sich abmelden kann, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-133">If the specified user can't log on or log off, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="a8d1a-134">TargetUri</span><span class="sxs-lookup"><span data-stu-id="a8d1a-134">TargetUri :</span></span>

<span data-ttu-id="a8d1a-135">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="a8d1a-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="a8d1a-136">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="a8d1a-136">Result : Failure</span></span>

<span data-ttu-id="a8d1a-137">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="a8d1a-137">Latency : 00:00:00</span></span>

<span data-ttu-id="a8d1a-138">Fehler: 11004, der angeforderte Name ist gültig, aber keine Daten der angeforderten</span><span class="sxs-lookup"><span data-stu-id="a8d1a-138">Error : 11004, The requested name is valid but no data of the requested</span></span>

<span data-ttu-id="a8d1a-139">Typ wurde gefunden</span><span class="sxs-lookup"><span data-stu-id="a8d1a-139">type was found</span></span>

<span data-ttu-id="a8d1a-140">Diagnose</span><span class="sxs-lookup"><span data-stu-id="a8d1a-140">Diagnosis :</span></span>

<span data-ttu-id="a8d1a-141">Test-CsLisConfiguration: kein übereinstimmender Cluster in der Topologie gefunden.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-141">Test-CsLisConfiguration : No matching cluster found in topology.</span></span>

<span data-ttu-id="a8d1a-142">Die vorherige Ausgabe enthält beispielsweise die Notiz "kein übereinstimmender Cluster in Topologie gefunden".</span><span class="sxs-lookup"><span data-stu-id="a8d1a-142">For example, the previous output includes the note “No matching cluster found in topology.”</span></span> <span data-ttu-id="a8d1a-143">Dies weist in der Regel auf ein Problem mit dem Edgeserver hin: der LIS, der den Edgeserver verwendet, um eine Verbindung mit dem Dienstanbieter herzustellen und Adressen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-143">That typically indicates a problem with the Edge Server: the LIS using the Edge Server to connect to the service provider and validate addresses.</span></span>

<span data-ttu-id="a8d1a-144">Wenn Test-CsLisConfiguration fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-144">If Test-CsLisConfiguration fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsLisConfiguration -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="a8d1a-145">Wenn der Verbose-Parameter enthalten ist, gibt Test-CsLisConfiguration eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-145">When the Verbose parameter is included, Test-CsLisConfiguration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="a8d1a-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-146">For example:</span></span>

<span data-ttu-id="a8d1a-147">Standortinformationsdienst für Anrufe.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-147">Calling Location Information Service.</span></span>

<span data-ttu-id="a8d1a-148">Dienstpfad = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span><span class="sxs-lookup"><span data-stu-id="a8d1a-148">Service Path = https://atl-cs-001.litwareinc.com:443/locationinformation/liservice.svc</span></span>

<span data-ttu-id="a8d1a-149">Subnet =</span><span class="sxs-lookup"><span data-stu-id="a8d1a-149">Subnet =</span></span>

<span data-ttu-id="a8d1a-150">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="a8d1a-150">BssId = 5</span></span>

<span data-ttu-id="a8d1a-151">Fahrgestell-Nr =</span><span class="sxs-lookup"><span data-stu-id="a8d1a-151">ChassisId =</span></span>

<span data-ttu-id="a8d1a-152">Port-Nr =</span><span class="sxs-lookup"><span data-stu-id="a8d1a-152">PortId =</span></span>

<span data-ttu-id="a8d1a-153">PortIdSubType = undefined Type</span><span class="sxs-lookup"><span data-stu-id="a8d1a-153">PortIdSubType = Undefined Type</span></span>

<span data-ttu-id="a8d1a-154">Mac</span><span class="sxs-lookup"><span data-stu-id="a8d1a-154">Mac</span></span>

<span data-ttu-id="a8d1a-155">Eine Ausnahme "Standortinformationen-Webdienstanforderung ist mit einem Antwortcode-Item400 fehlgeschlagen."</span><span class="sxs-lookup"><span data-stu-id="a8d1a-155">An exception 'Location Information Web Service request has failed with a response code Item400.'</span></span> <span data-ttu-id="a8d1a-156">während des Workflows Microsoft. RTC. SyntheticTrsnactions. Workflows. STLisConfigurationWorkflow-Ausführung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-156">occurred during Workflow Microsoft.Rtc.SyntheticTrsnactions.Workflows.STLisConfigurationWorkflow execution.</span></span>

<span data-ttu-id="a8d1a-157">Wenn Sie die vorherige Ausgabe genau untersuchen, sehen Sie, dass das Cmdlet nach dem Versuch, den standortinformationsdienst aufzurufen, fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-157">If you examine the previous output closely, you’ll see that the cmdlet failed after it tried to call the Location Information Service.</span></span> <span data-ttu-id="a8d1a-158">Einer der Parameter, die in diesem Aufruf verwendet wurden, war:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-158">One of the parameters that were used in that call was this:</span></span>

<span data-ttu-id="a8d1a-159">BssId = 5</span><span class="sxs-lookup"><span data-stu-id="a8d1a-159">BssId = 5</span></span>

<span data-ttu-id="a8d1a-160">Dies ist kein gültiger Wert für die grundlegende Dienst Satz-ID (BssID).</span><span class="sxs-lookup"><span data-stu-id="a8d1a-160">That’s not a valid value for the Basic Service Set Identifier (BssID).</span></span> <span data-ttu-id="a8d1a-161">Stattdessen sollte eine BssID wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-161">Instead, a BssID should resemble this:</span></span>

<span data-ttu-id="a8d1a-162">12-34-56-78-90-ab</span><span class="sxs-lookup"><span data-stu-id="a8d1a-162">12-34-56-78-90-ab</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="a8d1a-163">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="a8d1a-163">Reasons why the test might have failed</span></span>

<span data-ttu-id="a8d1a-164">Im folgenden finden Sie einige häufige Gründe, warum Test-CsLisConfiguration fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="a8d1a-164">Here are some common reasons why Test-CsLisConfiguration might fail:</span></span>

  - <span data-ttu-id="a8d1a-165">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-165">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="a8d1a-166">Wie im vorherigen Beispiel gezeigt, müssen die optionalen Parameter richtig konfiguriert sein, oder der Test schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-166">As shown in the previous example, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="a8d1a-167">Führen Sie den Befehl ohne die optionalen Parameter erneut aus, und überprüfen Sie, ob dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a8d1a-167">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

<span data-ttu-id="a8d1a-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8d1a-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

