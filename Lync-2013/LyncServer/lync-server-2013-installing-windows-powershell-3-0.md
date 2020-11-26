---
title: 'Lync Server 2013: Installieren von Windows PowerShell 3.0'
description: 'Lync Server 2013: Installieren von Windows PowerShell 3,0'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Windows PowerShell 3.0
ms:assetid: d87bf21e-0a43-41cb-8fdc-626cedec8538
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205328(v=OCS.15)
ms:contentKeyID: 48185621
ms.date: 06/28/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4605231f4e73f6aada4fb34de895cdeb883d82b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426900"
---
# <a name="installing-windows-powershell-30-for-lync-server-2013"></a><span data-ttu-id="290c3-103">Installieren von Windows PowerShell 3.0 für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="290c3-103">Installing Windows PowerShell 3.0 for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="290c3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="290c3-104">

<span> </span></span></span>

<span data-ttu-id="290c3-105">_**Letztes Änderungsdatum des Themas:** 2014-06-27_</span><span class="sxs-lookup"><span data-stu-id="290c3-105">_**Topic Last Modified:** 2014-06-27_</span></span>

<span data-ttu-id="290c3-106">Damit Sie lync Server 2013 erfolgreich bereitstellen können, benötigen Sie Windows PowerShell 3,0 auf jedem Computer, der Teil ihrer lync Server-Topologie ist.</span><span class="sxs-lookup"><span data-stu-id="290c3-106">To deploy Lync Server 2013 successfully, you’ll need Windows PowerShell 3.0 on each computer that’s part of your Lync Server topology.</span></span>

<span data-ttu-id="290c3-107">Bei Systemen, auf denen Windows Server 2012 oder Windows Server 2012 R2 ausgeführt wird, müssen Sie jetzt nichts tun, und Sie können den nächsten Bereitstellungsschritt fortführen, da PowerShell 3,0 in diesen Betriebssystemen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="290c3-107">Now, for systems running Windows Server 2012 or Windows Server 2012 R2, you don’t need to do anything here, and can go ahead to the next stage of deployment, because PowerShell 3.0 is included with those operating systems.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="290c3-108">Bei Systemen, auf denen Windows Server 2008 R2 SP1 ausgeführt wird, müssen Sie jedoch PowerShell 3,0 als Voraussetzung installieren, bevor Sie lync Server 2013 installieren, oder es funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="290c3-108">But for systems running Windows Server 2008 R2 SP1, you’ll need to install PowerShell 3.0 as a prerequisite before you install Lync Server 2013, or things won’t work.</span></span> <span data-ttu-id="290c3-109">Informationen zum Installieren von PowerShell 3,0 finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3,0</A>.</span><span class="sxs-lookup"><span data-stu-id="290c3-109">To install PowerShell 3.0, see <A href="https://go.microsoft.com/fwlink/p/?linkid=329800">Windows Management Framework 3.0</A>.</span></span> <span data-ttu-id="290c3-110">Hierbei handelt es sich um einen direkten Link zur PowerShell 3,0-Download Seite sowie Informationen zur erfolgreichen Installation.</span><span class="sxs-lookup"><span data-stu-id="290c3-110">This is a direct link to the PowerShell 3.0 download page, along with information relating to installing it successfully.</span></span>



</div>

<span data-ttu-id="290c3-111">Nachdem Sie die Installation abgeschlossen haben, oder wenn Sie nur überprüfen möchten, bevor Sie mit der lync Server-Bereitstellung fortfahren, können Sie sicherstellen, dass sich PowerShell 3,0 auf einem Server befindet, wenn Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="290c3-111">Once you’ve done the install, or if you just want to check and be sure before continuing with the Lync Server deployment, confirming that PowerShell 3.0 is on a server is pretty straightforward if you do this:</span></span>

1.  <span data-ttu-id="290c3-112">Wählen Sie auf dem Server, den Sie überprüfen möchten, **Start** aus, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie auf **Windows PowerShell**, und klicken Sie dann auf **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="290c3-112">On the server you want to check, choose **Start**, click **All Programs**, click **Accessories**, click **Windows PowerShell**, and then click **Windows PowerShell**.</span></span>

2.  <span data-ttu-id="290c3-113">Geben Sie in der Windows PowerShell-Konsole an der Eingabeaufforderung den folgenden Befehl ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="290c3-113">In the Windows PowerShell console, type the following command at the command prompt, and then press ENTER:</span></span>
    
        Get-Host | Select-Object Version

3.  <span data-ttu-id="290c3-114">Wenn Windows PowerShell 3,0 installiert ist, wird die Ausgabe wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="290c3-114">If Windows PowerShell 3.0 is installed you’ll see output that looks like this:</span></span>
    
        Version
        -------
        3.0

<span data-ttu-id="290c3-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="290c3-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

