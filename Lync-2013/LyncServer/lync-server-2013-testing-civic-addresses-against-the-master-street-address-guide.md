---
title: Testen von Civic addresses mit dem Master Street Address Guide
description: Testen von bürgerlichen Adressen mit dem Leitfaden zur Master Street-Adresse.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439828"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a><span data-ttu-id="74a63-103">Testen von bürgerlichen Adressen mit dem Leitfaden zur Master Street-Adresse in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74a63-103">Testing civic addresses against the master street address guide in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74a63-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74a63-104">

<span> </span></span></span>

<span data-ttu-id="74a63-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="74a63-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74a63-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="74a63-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="74a63-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="74a63-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74a63-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="74a63-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="74a63-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="74a63-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74a63-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="74a63-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="74a63-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="74a63-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="74a63-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsRegistration-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="74a63-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="74a63-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="74a63-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="74a63-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74a63-114">Description</span></span>

<span data-ttu-id="74a63-115">Das Test-CsLisCivicAddress-Cmdlet wird verwendet, um die Speicherorte zu überprüfen, die Ihrer Datenbank für den standortinformationsdienst (LIS) hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="74a63-115">The Test-CsLisCivicAddress cmdlet is used to verify locations that were added to your Location Information service (LIS) database.</span></span> <span data-ttu-id="74a63-116">Das Cmdlet vergleicht Speicherorte mit den Speicherorten im Master Street Address Guide (MSAG), die zu Ihrem E9-1-1-Netzwerk Routing Anbieter gehören.</span><span class="sxs-lookup"><span data-stu-id="74a63-116">The cmdlet works by comparing locations against the locations found in the Master Street Address Guide (MSAG) that belongs to your E9-1-1 Network Routing Provider.</span></span> <span data-ttu-id="74a63-117">Wenn Sie nicht über einen Netzwerkrouting Anbieter verfügen oder der Anbieter nicht erreicht werden kann, treten bei den Tests Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="74a63-117">If you do not have a network routing provider or if the provider cannot be reached, then your tests will fail.</span></span>

<span data-ttu-id="74a63-118">Wenn Sie den optionalen Schalterparameter UpdateValidationStatus zu Ihrem Befehl hinzufügen, wird die entsprechende MSAGValid-Datenbankeigenschaft für jede Adresse, die den Test übergibt, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74a63-118">If you add the optional switch parameter UpdateValidationStatus to your command, then the corresponding MSAGValid database property will be set to True for each address passing the test.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="74a63-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="74a63-119">Running the test</span></span>

<span data-ttu-id="74a63-120">Das Test-CsLisCivicAddress-Cmdlet kann zum Testen einzelner Adressen oder zum Testen mehrerer Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74a63-120">The Test-CsLisCivicAddress cmdlet can be used to test individual addresses or to test multiple addresses.</span></span> <span data-ttu-id="74a63-121">Dieser Befehl testet beispielsweise eine einzelne Adresse, die sich in Redmond, WA befindet:</span><span class="sxs-lookup"><span data-stu-id="74a63-121">For example, this command tests a single address located in Redmond, WA:</span></span>

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

<span data-ttu-id="74a63-122">Im Vergleich dazu testet dieser Befehl alle Adressen, die sich derzeit in ihrer LIS-Datenbank befinden:</span><span class="sxs-lookup"><span data-stu-id="74a63-122">By comparison, this command tests all the addresses currently in your LIS database:</span></span>

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

<span data-ttu-id="74a63-123">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="74a63-123">For more information, see the Help documentation for the [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="74a63-124">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="74a63-124">Determining success or failure</span></span>

<span data-ttu-id="74a63-125">Test-CsLisCivicAddress meldet den Erfolg oder Misserfolg der angegebenen Adressen zurück.</span><span class="sxs-lookup"><span data-stu-id="74a63-125">Test-CsLisCivicAddress will report back Success or Failure for the supplied addresses.</span></span> <span data-ttu-id="74a63-126">Bei einem Adress Test tritt ein Fehler auf, wenn die Adresse nicht gefunden werden kann oder wenn der Dienstanbieter nicht kontaktiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74a63-126">An address test will fail if the address cannot be found or if the service provider cannot be contacted.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="74a63-127">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="74a63-127">Reasons why the test might have failed</span></span>

<span data-ttu-id="74a63-128">Im folgenden finden Sie einige häufige Gründe, warum Test-CsLisCivicAddress fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="74a63-128">Here are some common reasons why Test-CsLisCivicAddress might fail:</span></span>

  - <span data-ttu-id="74a63-129">Der LIS-Dienstanbieter steht möglicherweise nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="74a63-129">The LIS service provider might not be available.</span></span> <span data-ttu-id="74a63-130">Sie können die URL Ihres LIS-Dienstanbieters abrufen, indem Sie das Get-CsLisConfiguration-Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="74a63-130">You can retrieve the URL of your LIS service provider by running the Get-CsLisConfiguration cmdlet:</span></span>
    
        Get-CsLisConfiguration 
    
    <span data-ttu-id="74a63-131">Anschließend können Sie die URL anpingen, um zu überprüfen, ob der Dienstanbieter verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="74a63-131">You can then ping that URL to verify that the service provider is available.</span></span>

<span data-ttu-id="74a63-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74a63-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

