---
title: 'Lync Server 2013: Testen der Rechte der Administrator Topologie'
description: 'Lync Server 2013: Testen der Rechte der Administrator Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin topology rights
ms:assetid: 0c03b7fd-449a-47ad-8263-ce811164cbce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767943(v=OCS.15)
ms:contentKeyID: 63969575
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22d713297d0e944c7acbc5efcb11b21ea1b26639
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441277"
---
# <a name="test-admin-topology-rights-in-lync-server-2013"></a><span data-ttu-id="0b049-103">Testen der Rechte der Administrator Topologie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0b049-103">Test admin topology rights in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0b049-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0b049-104">

<span> </span></span></span>

<span data-ttu-id="0b049-105">_**Letztes Änderungsdatum des Themas:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="0b049-105">_**Topic Last Modified:** 2016-12-08_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b049-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="0b049-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="0b049-107">Nach der ersten lync Server-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0b049-107">After initial Lync Server deployment.</span></span> <span data-ttu-id="0b049-108">Bei Bedarf, wenn berechtigungsbezogene Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="0b049-108">As needed if permission-related issues arise.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b049-109">Test Tool</span><span class="sxs-lookup"><span data-stu-id="0b049-109">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="0b049-110">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b049-110">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b049-111">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="0b049-111">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="0b049-112">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="0b049-112">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="0b049-113">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsSetupPermission-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="0b049-113">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="0b049-114">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="0b049-114">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsSetupPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="0b049-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0b049-115">Description</span></span>

<span data-ttu-id="0b049-116">Standardmäßig können nur Domänenadministratoren eine lync Server-Topologie aktivieren und große Änderungen an der lync Server-Infrastruktur vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0b049-116">By default, only domain administrators can enable a Lync Server topology and make large changes to the Lync Server infrastructure.</span></span> <span data-ttu-id="0b049-117">Dies ist kein Problem, solange Ihre Domänenadministratoren und ihre lync Server-Administratoren identisch sind. In vielen Organisationen verfügen lync Server-Administratoren nicht über Administratorrechte für die gesamte Domäne.</span><span class="sxs-lookup"><span data-stu-id="0b049-117">This won't be a problem as long as your domain administrators and your Lync Server administrators are one and the same.In many organizations Lync Server administrators do not hold administrative rights to the whole domain.</span></span> <span data-ttu-id="0b049-118">Standardmäßig bedeutet dies, dass diese Administratoren (als Mitglieder der RTCUniversalServerAdmins-Gruppe definiert) keine Änderungen an der lync Server-Topologie vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="0b049-118">By default, that means that these administrators (defined as members of the RTCUniversalServerAdmins group) can't make Lync Server topology changes.</span></span> <span data-ttu-id="0b049-119">Um Mitgliedern der RTCUniversalServerAdmins-Gruppe das Recht zu geben, Topologie-Änderungen vorzunehmen, müssen Sie mithilfe des Cmdlets [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) die erforderlichen Active Directory-Berechtigungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0b049-119">To give members of the RTCUniversalServerAdmins group the right to make topology changes, you must assign the required Active Directory permissions by using the [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="0b049-120">Das Test-CsSetupPermission-Cmdlet überprüft, ob die erforderlichen Berechtigungen zum Installieren von lync Server oder einer seiner Komponenten für den angegebenen Active Directory-Container konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="0b049-120">The Test-CsSetupPermission cmdlet verifies that the required permissions that are needed to install Lync Server or one of its components are configured on the specified Active Directory container.</span></span> <span data-ttu-id="0b049-121">Wenn die Berechtigungen nicht zugewiesen sind, können Sie das Grant-CsSetupPermission-Cmdlet ausführen, um Mitgliedern der RTCUniversalServerAdmins-Gruppe das Recht zu gewähren, lync Server zu installieren und zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0b049-121">If the permissions are not assigned, you can then run the Grant-CsSetupPermission cmdlet to give members of the RTCUniversalServerAdmins group the right to install and enable Lync Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0b049-122">Eine detaillierte Liste der von Grant-CsSetupPermission zugewiesenen Berechtigungen finden Sie im Blogbeitrag <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission und Grant-CsOUPermission</A>.</span><span class="sxs-lookup"><span data-stu-id="0b049-122">For a detailed list of permissions assigned by Grant-CsSetupPermission, see the blog post <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission and Grant-CsOUPermission</A>.</span></span>



</div>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="0b049-123">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="0b049-123">Running the test</span></span>

<span data-ttu-id="0b049-124">Rufen Sie das Test-CsSetupPermission-Cmdlet auf, um zu ermitteln, ob Setup Berechtigungen für einen Active Directory-Container zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0b049-124">To determine whether setup permissions are assigned for an Active Directory container, call the Test-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="0b049-125">Geben Sie den Distinguished Name des Containers an, der überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b049-125">Specify the distinguished name of the container to be checked.</span></span> <span data-ttu-id="0b049-126">Dieser Befehl überprüft beispielsweise die Setup Berechtigungen für den Container ou = CsServers, DC = "litwareinc, DC = com:</span><span class="sxs-lookup"><span data-stu-id="0b049-126">For example, this command verifies setup permissions on the container ou=CsServers,dc=litwareinc,dc=com:</span></span>

    Test-CsSetupPermission -ComputerOU "ou=CsServers,dc=litwareinc,dc=com"

<span data-ttu-id="0b049-127">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="0b049-127">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="0b049-128">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="0b049-128">Determining success or failure</span></span>

<span data-ttu-id="0b049-129">Wenn Test-CsSetupPermission feststellt, dass die erforderlichen Berechtigungen bereits für einen Active Directory-Container festgelegt wurden, gibt das Cmdlet den Wert "true" zurück:</span><span class="sxs-lookup"><span data-stu-id="0b049-129">If Test-CsSetupPermission determines that the required permissions have already been set on an Active Directory container then the cmdlet will return the value True:</span></span>

<span data-ttu-id="0b049-130">Wahr</span><span class="sxs-lookup"><span data-stu-id="0b049-130">True</span></span>

<span data-ttu-id="0b049-131">Wenn Berechtigungen nicht festgelegt werden, gibt Test-CsSetupPermission den Wert false zurück.</span><span class="sxs-lookup"><span data-stu-id="0b049-131">If permissions are not set, Test-CsSetupPermission will return the value False.</span></span> <span data-ttu-id="0b049-132">Beachten Sie, dass dieser Wert in der Regel in viele Warnmeldungen eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0b049-132">Note that this value will typically be enclosed in many warning messages.</span></span> <span data-ttu-id="0b049-133">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0b049-133">For example:</span></span>

<span data-ttu-id="0b049-134">Warnung: Zugriffssteuerungseintrag (ACE) ATL-CS-001 \\ RTCUniversalServerAdmins; Ermöglichen ExtendedRight; Keine Keine 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span><span class="sxs-lookup"><span data-stu-id="0b049-134">WARNING: Access control entry (ACE) atl-cs-001\\RTCUniversalServerAdmins; Allow; ExtendedRight; None; None; 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2</span></span>

<span data-ttu-id="0b049-135">Warnung: die Zugriffssteuerungseinträge (ACEs) für das Objekt "CN = Computers, DC =" litwareinc, DC = com "sind nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="0b049-135">WARNING: The access control entries (ACEs) on the object "CN=Computers,DC=litwareinc,DC=com" are not ready.</span></span>

<span data-ttu-id="0b049-136">Falsch</span><span class="sxs-lookup"><span data-stu-id="0b049-136">False</span></span>

<span data-ttu-id="0b049-137">Warnung: die Verarbeitung von "Test-CsSetupPermission" wurde mit Warnungen abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0b049-137">WARNING: "Test-CsSetupPermission" processing has completed with warnings.</span></span> <span data-ttu-id="0b049-138">"2"-Warnungen wurden während dieser Ausführung aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0b049-138">"2" warnings were recorded during this run.</span></span>

<span data-ttu-id="0b049-139">Warnung: detaillierte Ergebnisse finden Sie unter "C: \\ Benutzer \\ Administrator \\ AppData \\ local \\ Temp \\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span><span class="sxs-lookup"><span data-stu-id="0b049-139">WARNING: Detailed results can be found at "C:\\Users\\Admin\\AppData\\Local\\Temp\\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="0b049-140">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="0b049-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="0b049-141">Es gibt zwar seltene Ausnahmen, wenn Test-CsSetupPermission fehlschlägt, bedeutet dies in der Regel, dass dem angegebenen Active Directory-Container keine Setup Berechtigungen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0b049-141">Although there are rare exceptions, if Test-CsSetupPermission fails that typically means that setup permissions are not assigned for the specified Active Directory container.</span></span> <span data-ttu-id="0b049-142">Diese Berechtigungen können mithilfe des Grant-CsSetupPermission-Cmdlets zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0b049-142">Those permissions can be assigned by using the Grant-CsSetupPermission cmdlet.</span></span> <span data-ttu-id="0b049-143">Beispielsweise gewährt dieser Befehl dem Container "Computer" im Domänen litwareinc.com Setup Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="0b049-143">For example, this command grants setup permissions to the Computers container in the domain litwareinc.com:</span></span>

    Grant-CsSetupPermission -ComputerOU "cn=Computers,dc=litwareinc,dc=com"

<span data-ttu-id="0b049-144">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .</span><span class="sxs-lookup"><span data-stu-id="0b049-144">For more information, see the help topic for the [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) cmdlet.</span></span>

<span data-ttu-id="0b049-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0b049-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

