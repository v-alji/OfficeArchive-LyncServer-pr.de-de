---
title: 'Lync Server 2013: Überprüfen der lync Server 2013-Serverzertifikate'
description: 'Lync Server 2013: Überprüfen Sie die lync Server 2013-Serverzertifikate.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check server certificates
ms:assetid: 7b0474e8-0efe-47f0-84eb-a1ba575dabfd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725210(v=OCS.15)
ms:contentKeyID: 63969620
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 641651cb425b4fe8bd820bcebfa277084233bb1d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435019"
---
# <a name="check-lync-server-2013-server-certificates"></a><span data-ttu-id="ee4a0-103">Überprüfen der lync Server 2013-Serverzertifikate</span><span class="sxs-lookup"><span data-stu-id="ee4a0-103">Check Lync Server 2013 server certificates</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee4a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee4a0-104">

<span> </span></span></span>

<span data-ttu-id="ee4a0-105">_**Letztes Änderungsdatum des Themas:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="ee4a0-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee4a0-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="ee4a0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="ee4a0-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="ee4a0-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee4a0-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="ee4a0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="ee4a0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee4a0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee4a0-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="ee4a0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="ee4a0-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="ee4a0-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Get-CsCertificate-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Get-CsCertificate cmdlet.</span></span> <span data-ttu-id="ee4a0-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Get-CsCertificate&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="ee4a0-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee4a0-114">Description</span></span>

<span data-ttu-id="ee4a0-115">Mit dem Get-CsCertificate-Cmdlet können Sie Informationen zu jedem ihrer lync Server-Zertifikate abrufen.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-115">The Get-CsCertificate cmdlet enables you to retrieve information about each of your Lync Server certificates.</span></span> <span data-ttu-id="ee4a0-116">Dies ist besonders wichtig, da Zertifikate ein integriertes Ablaufdatum aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-116">That’s especially important because certificates have a built-in expiration date.</span></span> <span data-ttu-id="ee4a0-117">So verfallen in der Regel privat ausgestellte Zertifikate nach 12 Monaten.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-117">For example,, privately-issued certificates typically expire after 12 months.</span></span> <span data-ttu-id="ee4a0-118">Wenn eines ihrer lync Server-Zertifikate abläuft, gehen die zugehörigen Funktionen verloren, bis das Zertifikat erneuert oder ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-118">If any of your Lync Server certificates expire then you'll lose the accompanying functionality until that certificate is renewed or replaced.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="ee4a0-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="ee4a0-119">Running the test</span></span>

<span data-ttu-id="ee4a0-120">Wenn Sie Informationen zu den einzelnen lync Server-Zertifikaten zurückgeben möchten, führen Sie einfach den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-120">To return information about each of your Lync Server certificates just run the following command:</span></span>

`Get-CsCertificate`

<span data-ttu-id="ee4a0-121">Alternativ können Sie die Rückgabe Zertifikatinformationen auf Grundlage des Ablaufdatums filtern.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-121">Or, you can filter the return certificate information based on expiration date.</span></span> <span data-ttu-id="ee4a0-122">Mit diesem Befehl werden beispielsweise die zurückgegebenen Daten auf Zertifikate begrenzt, die ablaufen (können nach) 1. Juni 2014 nicht verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-122">For example, this command limits the returned data to certificates that expire (cannot be used after) June 1, 2014:</span></span>

`Get-CsCertificate | Where-Object {$_.NotAfter -lt "6/1/2014"}`

<span data-ttu-id="ee4a0-123">Weitere Informationen finden Sie in der Hilfedokumentation für das Cmdlet "Get-CsCertificate".</span><span class="sxs-lookup"><span data-stu-id="ee4a0-123">For more information, see the Help documentation for the Get-CsCertificate cmdlet.</span></span>

<span data-ttu-id="ee4a0-124">Beachten Sie, dass das Test-CsCertificateConfiguration-Cmdlet zwar vorhanden ist, aber für Administratoren nicht sehr hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-124">Note that, although the Test-CsCertificateConfiguration cmdlet exists, it is not very useful to administrators.</span></span> <span data-ttu-id="ee4a0-125">(Stattdessen wird dieses Cmdlet in erster Linie vom Zertifikat-Assistenten verwendet.) Obwohl das Cmdlet funktioniert, sind die zurückgegebenen Informationen von minimalem Wert, wie im folgenden Ausgabebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-125">(Instead, that cmdlet is primarily used by the Certificate wizard.) Although the cmdlet works, the information that it returns is of minimal value as shown in the following output example:</span></span>

<span data-ttu-id="ee4a0-126">Fingerabdruck Verwendung</span><span class="sxs-lookup"><span data-stu-id="ee4a0-126">Thumbprint Use</span></span>

<span data-ttu-id="ee4a0-127">\---------- ---</span><span class="sxs-lookup"><span data-stu-id="ee4a0-127">\---------- ---</span></span>

<span data-ttu-id="ee4a0-128">A9D51A2911C74FABFF7F2A8A994B20857D399107-Standard</span><span class="sxs-lookup"><span data-stu-id="ee4a0-128">A9D51A2911C74FABFF7F2A8A994B20857D399107 Default</span></span>

</div>

<div>

## <a name="reviewing-the-output"></a><span data-ttu-id="ee4a0-129">Überprüfen der Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ee4a0-129">Reviewing the output</span></span>

<span data-ttu-id="ee4a0-130">Das Get-CsCertificate-Cmdlet gibt für jedes Ihrer lync Server-Zertifikate Informationen zurück, die den folgenden ähneln:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-130">The Get-CsCertificate cmdlet returns information similar to the following for each of your Lync Server certificates:</span></span>

<span data-ttu-id="ee4a0-131">Emittent: CN = FabrikamCA</span><span class="sxs-lookup"><span data-stu-id="ee4a0-131">Issuer : CN=FabrikamCA</span></span>

<span data-ttu-id="ee4a0-132">NotAfter: 12/28/2015 3:35:41 Uhr</span><span class="sxs-lookup"><span data-stu-id="ee4a0-132">NotAfter : 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="ee4a0-133">NotBefore: 1/2/2014 12:49:37 pm</span><span class="sxs-lookup"><span data-stu-id="ee4a0-133">NotBefore : 1/2/2014 12:49:37 PM</span></span>

<span data-ttu-id="ee4a0-134">Seriennummer: 611BB01200000000000C</span><span class="sxs-lookup"><span data-stu-id="ee4a0-134">SerialNumber : 611BB01200000000000C</span></span>

<span data-ttu-id="ee4a0-135">Betreff: CN = LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-135">Subject : CN=LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-136">AlternativeNames: {SIP.fabrikam.com, LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="ee4a0-136">AlternativeNames : {sip.fabrikam.com, LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="ee4a0-137">Meet.fabrikam.com, admin.fabrikam.com...}</span><span class="sxs-lookup"><span data-stu-id="ee4a0-137">meet.fabrikam.com, admin.fabrikam.com...}</span></span>

<span data-ttu-id="ee4a0-138">Daumenabdruck: A9D51A2911C74FABFF7F2A8A994B20857D399107</span><span class="sxs-lookup"><span data-stu-id="ee4a0-138">Thumbprint : A9D51A2911C74FABFF7F2A8A994B20857D399107</span></span>

<span data-ttu-id="ee4a0-139">Verwendung: Standard</span><span class="sxs-lookup"><span data-stu-id="ee4a0-139">Use : Default</span></span>

<span data-ttu-id="ee4a0-140">In der Regel beziehen sich die wichtigsten Probleme im Zusammenhang mit lync Server-Zertifikaten auf Datums-und Uhrzeitangaben, beispielsweise wenn Zertifikate wirksam werden (NotBefore) oder wenn Sie ablaufen (NotAfter).</span><span class="sxs-lookup"><span data-stu-id="ee4a0-140">As a rule, the top issues involving Lync Server certificates involve dates and times, such as when certificates take effect (NotBefore) or when they expire (NotAfter).</span></span> <span data-ttu-id="ee4a0-141">Da diese Datums-und Uhrzeitangaben so wichtig sind, möchten Sie möglicherweise die zurückgegebenen Daten auf Informationen wie die Zertifikatverwendung, die Seriennummer des Zertifikats und das Ablaufdatum des Zertifikats einschränken. Anschließend können Sie alle Zertifikate schnell überprüfen und ablaufen.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-141">Because these dates and times are so important, you might want to limit the returned data to information such as the certificate use, the certificate serial number, and the certificate expiration date; then you can quickly review all the certificates and when they will expire.</span></span> <span data-ttu-id="ee4a0-142">Wenn Sie nur diese Informationen zurückgeben möchten, verwenden Sie den Befehl zusammen mit den folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-142">To return just that information, use the command together with the options as shown:</span></span>

`Get-CsCertificate | Select-Object Use, SerialNumber, NotAfter | Sort-Object NotAfter`

<span data-ttu-id="ee4a0-143">Dieser Befehl gibt Daten ähnlich der folgenden zurück, wobei die Zertifikate in der Reihenfolgeihres Ablaufdatums sortiert sind:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-143">That command returns data similar to the following, with the certificates sorted in order of their expiration date:</span></span>

<span data-ttu-id="ee4a0-144">Verwenden von Seriennummer NotAfter</span><span class="sxs-lookup"><span data-stu-id="ee4a0-144">Use SerialNumber NotAfter</span></span>

<span data-ttu-id="ee4a0-145">\--- ------------ --------</span><span class="sxs-lookup"><span data-stu-id="ee4a0-145">\--- ------------ --------</span></span>

<span data-ttu-id="ee4a0-146">Standard 611BB01200000000000C 12/28/2015 3:35:41 pm</span><span class="sxs-lookup"><span data-stu-id="ee4a0-146">Default 611BB01200000000000C 12/28/2015 3:35:41 PM</span></span>

<span data-ttu-id="ee4a0-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 pm</span><span class="sxs-lookup"><span data-stu-id="ee4a0-147">WebServicesInteral 32980AA20BBB20000191 02/15/2016 2:16:12 PM</span></span>

<span data-ttu-id="ee4a0-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 Uhr</span><span class="sxs-lookup"><span data-stu-id="ee4a0-148">WebServicesExternal 0451B012003872651A0C 02/20/2016 7:11:58 AM</span></span>

<span data-ttu-id="ee4a0-149">Wenn Sie Probleme mit dem Zertifikat haben, empfiehlt es sich, die für ein Zertifikat konfigurierte AlternativeNames zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-149">If you have certificate problems, you might want to review the AlternativeNames configured for a certificate.</span></span> <span data-ttu-id="ee4a0-150">Auf den ersten Blick scheint das ein Problem zu sein.</span><span class="sxs-lookup"><span data-stu-id="ee4a0-150">At first glance, that seems to be a problem.</span></span> <span data-ttu-id="ee4a0-151">Standardmäßig können Get-CsCertificate, je nach Größe des Konsolenfensters, möglicherweise nicht alle Namen anzeigen:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-151">By default, and depending on the size of your console window, Get-CsCertificate might not be able to display all the names:</span></span>

<span data-ttu-id="ee4a0-152">AlternativeNames: {SIP.fabrikam.com, LYNC.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="ee4a0-152">AlternativeNames : {sip.fabrikam.com, LYNC.fabrikam.com,</span></span>

<span data-ttu-id="ee4a0-153">Meet.fabrikam.com, admin. Fabrika...}</span><span class="sxs-lookup"><span data-stu-id="ee4a0-153">meet.fabrikam.com, admin.fabrika...}</span></span>

<span data-ttu-id="ee4a0-154">Wenn Sie alle alternativen Namen anzeigen möchten, die einem Zertifikat zugewiesen sind, verwenden Sie einen Befehl ähnlich dem folgenden:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-154">To see all the alternative names assigned to a certificate use a command similar to this one:</span></span>

`Get-CsCertificate | Where-Object {$_.SerialNumber -eq "611BB01200000000000C"} | Select-Object -ExpandProperty AlternativeNames`

<span data-ttu-id="ee4a0-155">Damit sollten alle alternativen Namen auf dem Zertifikat angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="ee4a0-155">That should show you all of the alternative names on the certificate:</span></span>

<span data-ttu-id="ee4a0-156">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-156">sip.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-157">LYNC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-157">LYNC.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-158">meet.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-158">meet.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-159">admin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-159">admin.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-160">LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-160">LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="ee4a0-161">Dialin.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="ee4a0-161">Dialin.fabrikam.com</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ee4a0-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee4a0-162">See Also</span></span>


[<span data-ttu-id="ee4a0-163">Get-CsCertificate</span><span class="sxs-lookup"><span data-stu-id="ee4a0-163">Get-CsCertificate</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCertificate)  
  

<span data-ttu-id="ee4a0-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee4a0-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

