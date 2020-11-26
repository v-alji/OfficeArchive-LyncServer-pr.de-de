---
title: Testen der Konfiguration des einem Standort zugewiesenen Kerberos-Kontos
description: Testen der Konfiguration des einem Standort zugewiesenen Kerberos-Kontos
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing configuration of the Kerberos account assigned to a site
ms:assetid: a087d77e-c59e-44f5-9caa-ccfd41be7276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743837(v=OCS.15)
ms:contentKeyID: 63969637
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0eab1618474a19753a4c6064d59aa4f8a856fceb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441067"
---
# <a name="testing-configuration-of-the-kerberos-account-assigned-to-a-site-in-lync-server-2013"></a><span data-ttu-id="e3360-103">Testen der Konfiguration des einem Standort zugewiesenen Kerberos-Kontos in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3360-103">Testing configuration of the Kerberos account assigned to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3360-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3360-104">

<span> </span></span></span>

<span data-ttu-id="e3360-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="e3360-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3360-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="e3360-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="e3360-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="e3360-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3360-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="e3360-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="e3360-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e3360-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3360-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e3360-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="e3360-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="e3360-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="e3360-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsKerberosAccountAssignment-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="e3360-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsKerberosAccountAssignment cmdlet.</span></span> <span data-ttu-id="e3360-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="e3360-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsKerberosAccountAssignment&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="e3360-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3360-114">Description</span></span>

<span data-ttu-id="e3360-115">Mit dem Test-CsKerberosAccountAssignment-Cmdlet können Sie überprüfen, ob ein Kerberos-Konto einer bestimmten Website zugeordnet ist, ob dieses Konto ordnungsgemäß konfiguriert ist und ob das Konto wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e3360-115">The Test-CsKerberosAccountAssignment cmdlet enables you to verify that a Kerberos account is associated with a given site, that this account is configured correctly, and that the account is working as expected.</span></span> <span data-ttu-id="e3360-116">Kerberos-Konten sind Computerkonten, die als Authentifizierungs Prinzipal für alle Computer in einer Website fungieren können, auf denen Internet Information Server (IIS) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3360-116">Kerberos accounts are computer accounts that can serve as the authentication principal for all the computers in a site that are running Internet Information Server (IIS).</span></span> <span data-ttu-id="e3360-117">Da diese Konten das Kerberos-Authentifizierungsprotokoll verwenden, werden die Konten als Kerberos-Konten bezeichnet, und der neue Authentifizierungsprozess wird als Kerberos-Webauthentifizierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e3360-117">Because these accounts use the Kerberos authentication protocol, the accounts are known as Kerberos accounts, and the new authentication process is known as Kerberos web authentication.</span></span> <span data-ttu-id="e3360-118">Auf diese Weise können Sie alle IIS-Server mithilfe eines einzelnen Kontos verwalten.</span><span class="sxs-lookup"><span data-stu-id="e3360-118">This enables you to manage all IIS servers by using a single account.</span></span>

<span data-ttu-id="e3360-119">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="e3360-119">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="e3360-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="e3360-120">Running the Test</span></span>

<span data-ttu-id="e3360-121">Standardmäßig werden Test-CsKerberosAccountAssignment auf dem Bildschirm nur sehr wenig ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e3360-121">By default, Test-CsKerberosAccountAssignment displays very little output on-screen.</span></span> <span data-ttu-id="e3360-122">Stattdessen werden vom Cmdlet zurückgegebene Informationen in eine HTML-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3360-122">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="e3360-123">Aus diesem Grund empfehlen wir, dass Sie den Verbose-Parameter und den Berichtsparameter jederzeit einfügen, wenn Sie Test-CsKerberosAccountAssignment ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3360-123">Because of that, we recommend that you include the Verbose parameter and the Report parameter any time that you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="e3360-124">Der Verbose-Parameter bietet eine etwas detailliertere Ausgabe auf dem Bildschirm, während das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3360-124">The Verbose parameter will provide slightly more detailed output on-screen while the cmdlet runs.</span></span> <span data-ttu-id="e3360-125">Mit dem Parameter Report können Sie einen Dateipfad und einen Dateinamen für die von Test-CsKerberosAccountAssignment generierte HTML-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="e3360-125">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="e3360-126">Wenn Sie den Berichtsparameter nicht angeben, wird die HTML-Datei automatisch in Ihrem Ordner "Benutzer" gespeichert, und Sie erhalten einen ähnlichen Namen wie den folgenden: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="e3360-126">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="e3360-127">Sie müssen auch eine Websiteidentität angeben, wenn Sie Test-CsKerberosAccountAssignment ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3360-127">You must also specify a site Identity when you run Test-CsKerberosAccountAssignment.</span></span> <span data-ttu-id="e3360-128">Kerberos-Konten werden im Website Bereich zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e3360-128">Kerberos accounts are assigned at the site scope.</span></span>

<span data-ttu-id="e3360-129">Der folgende Befehl führt Test-CsKerberosAccountAssignment und speichert die Ausgabe in einer Datei mit dem Namen C: \\ Logs \\KerberosTest.html:</span><span class="sxs-lookup"><span data-stu-id="e3360-129">The following command runs Test-CsKerberosAccountAssignment and saves the output to a file that is named C:\\Logs\\KerberosTest.html:</span></span>

    Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "C:\Logs\KerberosTest.html" -Verbose

<span data-ttu-id="e3360-130">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="e3360-130">For more information, see the Help documentation for the [Test-CsKerberosAccountAssignment](https://technet.microsoft.com/library/Gg425938(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="e3360-131">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="e3360-131">Determining Success or Failure</span></span>

<span data-ttu-id="e3360-132">Das Test-CsKerberosAccountAssignment-Cmdlet gibt keinen einfachen Hinweis auf Erfolg oder Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e3360-132">The Test-CsKerberosAccountAssignment cmdlet does not return a simple indication of success or failure.</span></span> <span data-ttu-id="e3360-133">Stattdessen müssen Sie die generierte HTML-Datei mit Internet Explorer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3360-133">Instead, you must view the generated HTML file by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="e3360-134">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="e3360-134">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="e3360-135">Im folgenden finden Sie einige häufige Gründe, warum Test-CsKerberosAccountAssignment fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="e3360-135">Here are some common reasons why Test-CsKerberosAccountAssignment might fail:</span></span>

  - <span data-ttu-id="e3360-136">Sie haben möglicherweise eine falsche Websiteidentität angegeben.</span><span class="sxs-lookup"><span data-stu-id="e3360-136">You might have specified an incorrect site Identity.</span></span> <span data-ttu-id="e3360-137">Wenn Sie eine Liste der gültigen Websiteidentität zurückgeben möchten, verwenden Sie diesen Befehl:</span><span class="sxs-lookup"><span data-stu-id="e3360-137">To return a list of valid site Identity, use this command:</span></span>
    
        Get-CsSite | Select-Identity Identity
    
    <span data-ttu-id="e3360-138">Eine Websiteidentität sieht in der Regel wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="e3360-138">A site Identity typically looks as follows:</span></span>
    
    <span data-ttu-id="e3360-139">Website: Redmond</span><span class="sxs-lookup"><span data-stu-id="e3360-139">site:Redmond</span></span>

  - <span data-ttu-id="e3360-140">Der angegebenen Website ist möglicherweise kein Kerberos-Konto zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e3360-140">The specified site might not have a Kerberos account assigned to it.</span></span> <span data-ttu-id="e3360-141">Sie können feststellen, ob einem Standort ein Kerberos-Konto zugewiesen ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="e3360-141">You can determine whether or not a Kerberos account is assigned to a site by running a command similar to this:</span></span>
    
        Get-CsKerberosAccountAssignment -Identity "site:Redmond"

  - <span data-ttu-id="e3360-142">Ihr Kerberos-Konto hat möglicherweise ein Kennwort, das nicht gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e3360-142">Your Kerberos account might have a password that isn't valid.</span></span> <span data-ttu-id="e3360-143">Wenn die folgende Fehlermeldung im Bericht angezeigt wird, müssen Sie wahrscheinlich das Kennwort für das Kerberos-Konto zurücksetzen:</span><span class="sxs-lookup"><span data-stu-id="e3360-143">If you receive the following error message in report, you'll probably have to reset the Kerberos account password:</span></span>
    
    <span data-ttu-id="e3360-144">InvalidKerberosConfiguration: die Kerberos-Konfiguration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3360-144">InvalidKerberosConfiguration: The Kerberos configuration is invalid.</span></span>
    
    <span data-ttu-id="e3360-145">InvalidKerberosConfiguration: die Kerberos-Konfiguration für ATL-cs001.litwareinc.com ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3360-145">InvalidKerberosConfiguration: The Kerberos configuration on atl-cs001.litwareinc.com is invalid.</span></span> <span data-ttu-id="e3360-146">Das erwartete zugewiesene Konto ist "litwareinc \\ kerberostest.</span><span class="sxs-lookup"><span data-stu-id="e3360-146">The expected assigned account is litwareinc\\kerberostest.</span></span> <span data-ttu-id="e3360-147">Stellen Sie sicher, dass das Konto nicht abgelaufen ist und das konfigurierte Kennwort auf dem Computer dem Active Directory-Kennwort des Kontos entspricht.</span><span class="sxs-lookup"><span data-stu-id="e3360-147">Ensure that the account has not expired, and the configured password on the machine matches the Active Directory password of the account.</span></span>
    
    <span data-ttu-id="e3360-148">Sie können das Kennwort mit dem Cmdlet " [Satz-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3360-148">You can set the password using the [Set-CsKerberosAccountPassword](https://technet.microsoft.com/library/Gg398659(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="e3360-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3360-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

