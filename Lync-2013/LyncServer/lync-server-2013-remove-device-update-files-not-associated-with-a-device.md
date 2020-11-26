---
title: 'Lync Server 2013: Entfernen von Geräteaktualisierungsdateien, die keinem Gerät zugeordnet sind'
description: 'Lync Server 2013: Entfernen von Geräteaktualisierungsdateien, die keinem Gerät zugeordnet sind.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove Device Update files not associated with a device
ms:assetid: ecebbf73-b456-4990-a91d-308b84d39404
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994084(v=OCS.15)
ms:contentKeyID: 51803996
ms.date: 12/12/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8338f7274d1d27e2290d822324986238f4856fe4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436405"
---
# <a name="remove-device-update-files-not-associated-with-a-device-in-lync-server-2013"></a><span data-ttu-id="a04f4-103">Entfernen von Geräteaktualisierungsdateien, die nicht mit einem Gerät in lync Server 2013 verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="a04f4-103">Remove Device Update files not associated with a device in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a04f4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a04f4-104">

<span> </span></span></span>

<span data-ttu-id="a04f4-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="a04f4-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="a04f4-106">Jedes Mal, wenn neue Geräte Updates in das System hochgeladen werden, wird eine entsprechende geräteaktualisierungsregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="a04f4-106">Each time new device updates are uploaded to the system, a corresponding device update rule is created.</span></span> <span data-ttu-id="a04f4-107">Standardmäßig werden diese neuen geräteaktualisierungsregeln dem Status "Ausstehend" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a04f4-107">By default, these new device update rules are assigned to the Pending state.</span></span> <span data-ttu-id="a04f4-108">Das bedeutet, dass die Regeln auf Testgeräten heruntergeladen und installiert werden können, aber nicht auf Produktionsgeräten, sodass Sie die Updates testen können, bevor Sie Sie für Benutzer verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="a04f4-108">This means that the rules can be downloaded and installed on test devices, but not on production devices, which enables you to test the updates before making them available to users.</span></span> <span data-ttu-id="a04f4-109">Basierend auf den Tests können Sie das Update entweder annehmen und bereitstellen oder ablehnen und löschen.</span><span class="sxs-lookup"><span data-stu-id="a04f4-109">Based on the tests, you either accept and deploy or reject and delete the update.</span></span> <span data-ttu-id="a04f4-110">Wenn Sie ein Update ablehnen, wird das Geräteupdate von seiner geräteaktualisierungsregel nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a04f4-110">When you reject an update, the device update is disassociated from its device update rule.</span></span>

<div>


<span data-ttu-id="a04f4-111">Geräteaktualisierungsdateien, die keinem Gerät mehr zugeordnet sind, können mithilfe von Windows PowerShell und dem Cmdlet " **Clear-CsDeviceUpdateFile** " entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a04f4-111">Device update files that are no longer associated with a device can be removed by using Windows PowerShell and the **Clear-CsDeviceUpdateFile** cmdlet.</span></span> <span data-ttu-id="a04f4-112">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a04f4-112">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a04f4-113">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="a04f4-113">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


  - <span data-ttu-id="a04f4-114">Mit dem folgenden Befehl werden beispielsweise alle geräteaktualisierungsregeln auf dem Webserver ATL-CS-001.litwareinc.com entfernt, die keinem Gerät mehr zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="a04f4-114">For example, the following command removes any device update rules on the Web server atl-cs-001.litwareinc.com that are no longer associated with a device:</span></span>
    
        Clear-CsDeviceUpdateFile -Identity "service:WebServer:atl-cs-001.litwareinc.com"

</div>

<span data-ttu-id="a04f4-115">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet " [Clear-CsDeviceUpdateFile](https://docs.microsoft.com/powershell/module/skype/Clear-CsDeviceUpdateFile) ".</span><span class="sxs-lookup"><span data-stu-id="a04f4-115">For details, see the Help topic for the [Clear-CsDeviceUpdateFile](https://docs.microsoft.com/powershell/module/skype/Clear-CsDeviceUpdateFile) cmdlet.</span></span>

<span data-ttu-id="a04f4-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a04f4-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

