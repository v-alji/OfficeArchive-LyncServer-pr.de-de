---
title: Testen der Funktionsfähigkeit der Kerberos-Authentifizierung und Erstellen eines Berichts
description: Testen und melden Sie die Funktionsbereitschaft für die Kerberos-Authentifizierung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test and report functional readiness for Kerberos authentication
ms:assetid: d52c39e5-747d-4f29-88aa-30fd6f26b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398925(v=OCS.15)
ms:contentKeyID: 48185519
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d32591a8cced7dce2e0bb78cc26189dce1900a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444301"
---
# <a name="test-and-report-functional-readiness-for-kerberos-authentication-in-lync-server-2013"></a><span data-ttu-id="ad980-103">Testen der Funktionsfähigkeit der Kerberos-Authentifizierung und Erstellen eines Berichts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad980-103">Test and report functional readiness for Kerberos authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad980-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad980-104">

<span> </span></span></span>

<span data-ttu-id="ad980-105">_**Letztes Änderungsdatum des Themas:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="ad980-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="ad980-106">Um dieses Verfahren erfolgreich abzuschließen, sollten Sie als Benutzer angemeldet sein, der Mitglied der RTCUniversalServerAdmins-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="ad980-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="ad980-107">Sie können das Windows PowerShell **-Cmdlet Test-CsKerberosAccountAssignment** verwenden, um die Funktionsbereitschaft einer Website Aufgabe für die Kerberos-Authentifizierung zu testen und zu melden.</span><span class="sxs-lookup"><span data-stu-id="ad980-107">You can use the **Test-CsKerberosAccountAssignment** Windows PowerShell cmdlet to test and report the functional readiness of a site assignment for Kerberos authentication.</span></span> <span data-ttu-id="ad980-108">Dieser Befehl fragt die im erforderlichen Identity-Parameter angegebene Website ab.</span><span class="sxs-lookup"><span data-stu-id="ad980-108">This command queries the site specified in the required Identity parameter.</span></span> <span data-ttu-id="ad980-109">Der optionale Berichtsparameter bewirkt, dass das Cmdlet einen HTML-Bericht in C:- \\ Protokolle auf dem Computer schreibt, auf dem der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad980-109">The optional Report parameter causes the cmdlet to write an HTML report to C:\\Logs on the computer on which the command is run.</span></span> <span data-ttu-id="ad980-110">Der optionale Verbose-Parameter meldet Aktivitätsinformationen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="ad980-110">The optional Verbose parameter reports activity information to the screen.</span></span>

<div>

## <a name="to-test-and-report-functional-readiness-for-kerberos-authentication-for-a-site"></a><span data-ttu-id="ad980-111">So testen und melden Sie die Funktionsbereitschaft für die Kerberos-Authentifizierung für eine Website</span><span class="sxs-lookup"><span data-stu-id="ad980-111">To test and report functional readiness for Kerberos authentication for a site</span></span>

1.  <span data-ttu-id="ad980-112">Melden Sie sich als Mitglied der RTCUniversalServerAdmins-Gruppe an einem Computer in der Domäne mit lync Server 2013 oder auf dem Computer an, auf dem die Verwaltungstools installiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad980-112">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to the computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="ad980-113">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="ad980-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="ad980-114">Führen Sie in der Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ad980-114">From the command line, run the following command:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:SiteName" -Report "c:\logs\FileName.htm" -Verbose
    
    <span data-ttu-id="ad980-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ad980-115">For example:</span></span>
    
        Test-CsKerberosAccountAssignment -Identity "site:Redmond" -Report "c:\logs\KerberosReport.htm" -Verbose

<span data-ttu-id="ad980-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad980-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

