---
title: 'Lync Server 2013: Melden von Kerberos-Kontozuweisungen'
description: 'Lync Server 2013: Melden von Kerberos-Konto Zuweisungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Report Kerberos account assignments
ms:assetid: 523231f6-81b3-454b-996d-663d9bd5cf83
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398343(v=OCS.15)
ms:contentKeyID: 48184151
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23e40dddfc4538db70e2101b1bfcbbce2fe3fa8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442740"
---
# <a name="report-kerberos-account-assignments-in-lync-server-2013"></a><span data-ttu-id="52abe-103">Melden von Kerberos-Kontozuweisungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="52abe-103">Report Kerberos account assignments in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="52abe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="52abe-104">

<span> </span></span></span>

<span data-ttu-id="52abe-105">_**Letztes Änderungsdatum des Themas:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="52abe-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="52abe-106">Um dieses Verfahren erfolgreich abzuschließen, sollten Sie als Benutzer angemeldet sein, der Mitglied der RTCUniversalServerAdmins-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="52abe-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="52abe-107">Mit dem Cmdlet **Get-CsKerberosAccountAssignment** können Sie Informationen zu den Kerberos-Authentifizierungs Konto Zuweisungen Abfragen und Informationen zu den aktuellen Aufgaben in Ihrer Bereitstellung melden.</span><span class="sxs-lookup"><span data-stu-id="52abe-107">You can use the **Get-CsKerberosAccountAssignment** cmdlet to query information about the Kerberos authentication account assignments and report information about the current assignments in your deployment.</span></span>

<div>

## <a name="to-query-kerberos-authentication-account-assignments-for-a-site"></a><span data-ttu-id="52abe-108">So Abfragen Sie Kerberos-Authentifizierungs Konto Zuweisungen für eine Website</span><span class="sxs-lookup"><span data-stu-id="52abe-108">To query Kerberos authentication account assignments for a site</span></span>

1.  <span data-ttu-id="52abe-109">Melden Sie sich als Mitglied der RTCUniversalServerAdmins-Gruppe an einem Computer in der Domäne mit lync Server 2013 oder auf einem Computer an, auf dem die Verwaltungstools installiert sind.</span><span class="sxs-lookup"><span data-stu-id="52abe-109">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="52abe-110">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="52abe-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="52abe-111">Führen Sie in der Befehlszeile einen der folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="52abe-111">From the command line, run one of the following commands:</span></span>
    
      - <span data-ttu-id="52abe-112">Wenn Sie alle Kerberos-Authentifizierungs Konto Zuweisungen in Ihrer Organisation Abfragen und Zuordnungsinformationen zu den einzelnen Aufgaben zurückgeben möchten, führen Sie das Cmdlet ohne Parameter aus:</span><span class="sxs-lookup"><span data-stu-id="52abe-112">To query all Kerberos authentication account assignments in your organization and return assignment information about each of them, run the cmdlet without any parameters:</span></span>
        
            Get-CsKerberosAccountAssignment
    
      - <span data-ttu-id="52abe-113">Führen Sie das Cmdlet mit dem Parameter Identity aus, um alle Kerberos-Authentifizierungs Konto Zuweisungen in Ihrer Bereitstellung abzufragen und Websitezuordnungsinformationen zu diesen zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="52abe-113">To query all Kerberos authentication account assignments in your deployment and return site assignment information about each of them, run the cmdlet with the Identity parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:SiteName"
        
        <span data-ttu-id="52abe-114">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="52abe-114">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Identity "site:Redmond"
    
      - <span data-ttu-id="52abe-115">Führen Sie das Cmdlet mit dem Parameter Filter aus, um alle Kerberos-Authentifizierungs Konto Zuweisungen an einer einzigen Website abzufragen und Zuordnungsinformationen zu den einzelnen Websites zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="52abe-115">To query all Kerberos authentication account assignments in a single site and return assignment information about each of them, run the cmdlet with the Filter parameter:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "SiteName"
        
        <span data-ttu-id="52abe-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="52abe-116">For example:</span></span>
        
            Get-CsKerberosAccountAssignment -Filter "*Redmond"
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="52abe-117">Durch die Angabe von \* Sitename für den Filter-Parameter werden Informationen zu allen Websites zurückgegeben, die den angegebenen Websitenamen an einer beliebigen Stelle in der Website-ID enthalten (beispielsweise alle Websites, die die Zeichenfolge Redmond in der Website-ID enthalten).</span><span class="sxs-lookup"><span data-stu-id="52abe-117">Specifying \*SiteName for the Filter parameter returns information about all sites that contain the specified site name anywhere in the site identifier (for example, all sites that contain the string Redmond in the site identifier).</span></span>

        
        <span data-ttu-id="52abe-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="52abe-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

