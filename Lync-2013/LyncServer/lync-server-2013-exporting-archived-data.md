---
title: 'Lync Server 2013: Exportieren von archivierten Daten'
description: 'Lync Server 2013: Exportieren von archivierten Daten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 656751f1a2d03b50f0c938a8501ba3e95e304cff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428335"
---
# <a name="exporting-archived-data-from-lync-server-2013"></a><span data-ttu-id="3f324-103">Exportieren von archivierten Daten aus lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f324-103">Exporting archived data from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f324-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f324-104">

<span> </span></span></span>

<span data-ttu-id="3f324-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="3f324-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="3f324-106">Die in Archivierungsdatenbanken archivierten Daten liegen nicht in durchsuchbarem oder lesbarem Format vor. Sie können jedoch mit dem Cmdlet Export-CsArchivingData Datensätze aus der Datenbank extrahieren und als EML (Outlook Electronic Mail)-Datei speichern..</span><span class="sxs-lookup"><span data-stu-id="3f324-106">Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file.</span></span> <span data-ttu-id="3f324-107">Ausführliche Informationen zum Exportieren von archivierten Daten finden Sie unter [exportieren-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="3f324-107">For details about exporting archived data, see [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) in the Operations documentation.</span></span>

<span data-ttu-id="3f324-108">Wenn Sie die Microsoft Exchange-Integration aktivieren, werden die Daten in Exchange 2013-Stores archiviert.</span><span class="sxs-lookup"><span data-stu-id="3f324-108">If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores.</span></span> <span data-ttu-id="3f324-109">In Exchange 2013 archivierte Daten sind durchsuchbar und auffindbar.</span><span class="sxs-lookup"><span data-stu-id="3f324-109">Data archived in Exchange 2013 is searchable and discoverable.</span></span> <span data-ttu-id="3f324-110">Details zur Unterstützung der integrierten Kommunikation für Exchange 2013 und lync Server 2013 finden Sie unter Unterstützung für [Exchange Server und SharePoint-Integration in lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3f324-110">For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="3f324-111">Details zum Zugriff auf Daten, die in Exchange archiviert werden, finden Sie in der Exchange 2013-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3f324-111">For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.</span></span>

<div>

## <a name="exporting-archiving-data-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="3f324-112">Exportieren von Archivierungsdaten mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f324-112">Exporting Archiving Data by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="3f324-113">Archivierungsdaten können mithilfe des Export-CSArchivingData-Cmdlets exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="3f324-113">Archiving data can be exported by using the Export-CSArchivingData cmdlet.</span></span> <span data-ttu-id="3f324-114">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3f324-114">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="3f324-115">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="3f324-115">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<span data-ttu-id="3f324-116">**So exportieren Sie Archivierungsdaten**</span><span class="sxs-lookup"><span data-stu-id="3f324-116">**To export archiving data**</span></span>

  - <span data-ttu-id="3f324-117">Mit diesem Befehl werden alle Archivierungsdaten exportiert, die in die Archivierungsdatenbank ATL-SQL-001.litwareinc.com seit dem 1. Juni 2012 geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f324-117">This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012.</span></span> <span data-ttu-id="3f324-118">Die resultierende Ausgabedatei wird im Ordner C: ArchivingExports gespeichert \\ .</span><span class="sxs-lookup"><span data-stu-id="3f324-118">The resulting output file will be stored in the folder C:\\ArchivingExports.</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

<span data-ttu-id="3f324-119">**So exportieren Sie Archivierungsdaten für einen einzelnen Benutzer**</span><span class="sxs-lookup"><span data-stu-id="3f324-119">**To export archiving data for a single user**</span></span>

  - <span data-ttu-id="3f324-120">Mit dem folgenden Befehl werden Archivierungsdaten für einen einzelnen Benutzer exportiert: kenmyer@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="3f324-120">The following command exports archiving data for a single user: kenmyer@litwareinc.com.</span></span> <span data-ttu-id="3f324-121">Hierzu wird der Parameter „UserUri“, gefolgt von der SIP-Adresse des Benutzers, eingefügt.</span><span class="sxs-lookup"><span data-stu-id="3f324-121">This is done by including the UserUri parameter followed by the user’s SIP address.</span></span> <span data-ttu-id="3f324-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3f324-122">For example:</span></span>
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

<span data-ttu-id="3f324-123">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) .</span><span class="sxs-lookup"><span data-stu-id="3f324-123">For more information, see the help topic for the [Export-CsArchivingData](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3f324-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f324-124">See Also</span></span>


[<span data-ttu-id="3f324-125">Unterstützung der Integration von Exchange Server und SharePoint in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3f324-125">Exchange Server and SharePoint integration support in Lync Server 2013</span></span>](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[<span data-ttu-id="3f324-126">Export-CsArchivingData</span><span class="sxs-lookup"><span data-stu-id="3f324-126">Export-CsArchivingData</span></span>](https://docs.microsoft.com/powershell/module/skype/Export-CsArchivingData)  
[<span data-ttu-id="3f324-127">Verwalten der Lync Server 2013-Archivierung</span><span class="sxs-lookup"><span data-stu-id="3f324-127">Managing Lync Server 2013 Archiving</span></span>](lync-server-2013-managing-archiving.md)  
  

<span data-ttu-id="3f324-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f324-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

