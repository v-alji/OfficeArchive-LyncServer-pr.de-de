---
title: Verschieben von Lync Server 2010-Konferenzverzeichnissen zu Lync Server 2013
description: Verschieben von lync Server 2010-Konferenz Verzeichnissen nach lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move Conference Directories
ms:assetid: 659867e0-ce91-4a95-9787-b1c1566460a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727126(v=OCS.15)
ms:contentKeyID: 62387565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12ac58ac0ab6f1908e7eac3e5824bf2304256632
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440346"
---
# <a name="move-conference-directories"></a><span data-ttu-id="5ab50-103">Verschieben von Konferenzverzeichnissen</span><span class="sxs-lookup"><span data-stu-id="5ab50-103">Move Conference Directories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ab50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ab50-104">

<span> </span></span></span>

<span data-ttu-id="5ab50-105">_**Letztes Änderungsdatum des Themas:** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="5ab50-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="5ab50-106">Vor der Außerbetriebnahme eines Pools müssen Sie das folgende Verfahren für jedes Konferenzverzeichnis in Ihrem lync Server 2010-Pool ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ab50-106">Before decommissioning a pool you must perform the following procedure for each conference directory in your Lync Server 2010 pool.</span></span>

<div>

## <a name="to-move-a-conference-directory-to-lync-server-2013"></a><span data-ttu-id="5ab50-107">So verschieben Sie ein Konferenzverzeichnis in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ab50-107">To Move a Conference Directory to Lync Server 2013</span></span>

1.  <span data-ttu-id="5ab50-108">Öffnen Sie die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="5ab50-108">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="5ab50-109">Führen Sie den folgenden Befehl aus, um die Identität der Konferenzverzeichnisse in Ihrer Organisation zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="5ab50-109">To obtain the identity of the conference directories in your organization, run the following command:</span></span>
    
        Get-CsConferenceDirectory
    
    <span data-ttu-id="5ab50-110">Der vorhergehende Befehl gibt alle Konferenzverzeichnisse in Ihrer Organisation zurück.</span><span class="sxs-lookup"><span data-stu-id="5ab50-110">The preceding command returns all the conference directories in your organization.</span></span> <span data-ttu-id="5ab50-111">Aus diesem Grund sollten Sie die Ergebnisse auf den Pool beschränken, der außer Betrieb genommen wird.</span><span class="sxs-lookup"><span data-stu-id="5ab50-111">Because of that, you might want to limit the results to the pool being decommissioned.</span></span> <span data-ttu-id="5ab50-112">Wenn Sie beispielsweise den Pool mit dem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) pool01.contoso.net, verwenden Sie diesen Befehl, um die zurückgegebenen Daten auf Konferenzverzeichnisse aus diesem Pool zu begrenzen:</span><span class="sxs-lookup"><span data-stu-id="5ab50-112">For example, if you are decommissioning the pool with the fully qualified domain name (FQDN) pool01.contoso.net, use this command to limit the returned data to conference directories from that pool:</span></span>
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"}
    
    <span data-ttu-id="5ab50-113">Dieser Befehl gibt nur die Konferenzverzeichnisse zurück, in denen die Service-Eigenschaft den FQDN-pool01.contoso.NET enthält.</span><span class="sxs-lookup"><span data-stu-id="5ab50-113">That command returns only the conference directories where the ServiceID property contains the FQDN pool01.contoso.net.</span></span>

3.  <span data-ttu-id="5ab50-114">Führen Sie zum Verschieben von Konferenz Verzeichnissen den folgenden Befehl für jedes Konferenzverzeichnis im Pool aus:</span><span class="sxs-lookup"><span data-stu-id="5ab50-114">To move conference directories, run the following command for each conference directory in the pool:</span></span>
    
        Move-CsConferenceDirectory -Identity <Numeric identity of conference directory> -TargetPool <FQDN of pool where ownership is to be transitioned>
    
    <span data-ttu-id="5ab50-115">Wenn Sie beispielsweise das Konferenzverzeichnis 3 verschieben möchten, verwenden Sie diesen Befehl, um einen lync Server 2013-Pool als TargetPool anzugeben:</span><span class="sxs-lookup"><span data-stu-id="5ab50-115">For example, to move conference directory 3 use this command, specifying a Lync Server 2013 pool as the TargetPool:</span></span>
    
        Move-CsConferenceDirectory -Identity 3 -TargetPool "pool02.contoso.net"
    
    <span data-ttu-id="5ab50-116">Wenn Sie alle Konferenzverzeichnisse in einem Pool verschieben möchten, verwenden Sie einen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="5ab50-116">If you want to move all the conference directories on a pool then use a command similar to the following:</span></span>
    
        Get-CsConferenceDirectory | Where-Object {$_.ServiceID -match "pool01.contoso.net"} | Move-CsConferenceDirectory -TargetPool "pool02.contoso.net"

<span data-ttu-id="5ab50-117">[https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227)Ausführliche Schritt-für-Schritt-Anleitungen zur Außerbetriebnahme von lync 2010-Pools finden Sie im Dokument "Deinstallieren von Microsoft lync Server 2010 und Entfernen von Serverrollen" (das heruntergeladen werden kann).</span><span class="sxs-lookup"><span data-stu-id="5ab50-117">Please see the document "Uninstalling Microsoft Lync Server 2010 and Removing Server Roles" (which can be downloaded from [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227)) for comprehensive, step-by-step instructions on decommissioning Lync 2010 pools.</span></span>

<span data-ttu-id="5ab50-118">Beim Verschieben von Konferenz Verzeichnissen kann die folgende Fehlermeldung auftreten:</span><span class="sxs-lookup"><span data-stu-id="5ab50-118">When moving conference directories you might encounter the following error:</span></span>

    WARNING: Move operation failed for conference directory with ID "5". Cannot perform a rollback because data migration might have already started. Retry the operation.
    WARNING: Before using the -Force parameter, ensure that you have exported the conference directory data using DBImpExp.exe and imported the data on the target pool. Refer to the DBImpExp-Readme.htm file for more information.
    Move-CsConferenceDirectory : Unable to cast COM object of type 'System._ComObject' to interface type 'Microsoft.Rtc.Interop.User.IRtcConfDirManagement'. 
    This operation failed because the QueryInterface call on the COM component for the interface with SID '{4262B886-503F-4BEA-868C-04E8DF562CEB}' failed due to the following error: The specified module could not be found.

<span data-ttu-id="5ab50-119">Dieser Fehler tritt in der Regel auf, wenn die lync Server-Verwaltungsshell einen aktualisierten Satz von Active Directory-Berechtigungen erfordert, um eine Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="5ab50-119">This error typically occurs when the Lync Server Management Shell requires an updated set of Active Directory permissions in order to complete a task.</span></span> <span data-ttu-id="5ab50-120">Um das Problem zu beheben, schließen Sie die aktuelle Instanz der Verwaltungsshell, öffnen Sie dann eine neue Instanz der Shell, und führen Sie den Befehl erneut aus, um das Konferenzverzeichnis zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5ab50-120">To resolve the problem, close the current instance of the Management Shell, then open a new instance of the shell and re-run the command in order to move the conference directory.</span></span>

<span data-ttu-id="5ab50-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ab50-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

