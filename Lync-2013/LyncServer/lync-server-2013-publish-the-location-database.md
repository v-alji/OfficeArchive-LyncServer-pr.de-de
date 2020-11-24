---
title: 'Lync Server 2013: Veröffentlichen der Standortdatenbank'
description: 'Lync Server 2013: Veröffentlichen der Standortdatenbank'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26892429c7bf5fd9cbfebd0d7ac62482767a541e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394563"
---
# <a name="publish-the-location-database-from-lync-server-2013"></a><span data-ttu-id="72b27-103">Veröffentlichen der Standortdatenbank aus lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72b27-103">Publish the location database from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72b27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72b27-104">

<span> </span></span></span>

<span data-ttu-id="72b27-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="72b27-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="72b27-106">Die neuen Standorte, die Sie der Standortdatenbank hinzugefügt haben, stehen dem Client erst nach der Veröffentlichung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="72b27-106">The new locations that you added to the location database will not be made available to the client until they have been published.</span></span>

<span data-ttu-id="72b27-107">Ausführliche Informationen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für das folgende Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="72b27-107">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="72b27-108">**Publish-CsLisConfiguration**</span><span class="sxs-lookup"><span data-stu-id="72b27-108">**Publish-CsLisConfiguration**</span></span>

<span data-ttu-id="72b27-109">Wenn Sie ELIN-Gateways (Emergency Location Identification Number) verwenden, müssen Sie die ELINs auch in die ALI (Automatic Location Identification)-Datenbank Ihres PSTN-Betreibers hochladen.</span><span class="sxs-lookup"><span data-stu-id="72b27-109">If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database.</span></span> <span data-ttu-id="72b27-110">Ihr PSTN-Betreiber verlangt möglicherweise, dass Sie ein bestimmtes Format für die ELIN-Einträge verwenden.</span><span class="sxs-lookup"><span data-stu-id="72b27-110">Your PSTN carrier may require you to use a specific format for the ELIN records.</span></span> <span data-ttu-id="72b27-111">Weitere Informationen erhalten Sie von Ihrem PSTN-Betreiber.</span><span class="sxs-lookup"><span data-stu-id="72b27-111">Contact your PSTN carrier for details.</span></span> <span data-ttu-id="72b27-112">Sie können die Datensätze aus der Datenbank des Standort Informationsdiensts exportieren und diese nach Bedarf formatieren.</span><span class="sxs-lookup"><span data-stu-id="72b27-112">You can export the records from the Location Information service database and format them as required.</span></span>

<div>

## <a name="to-publish-the-location-database"></a><span data-ttu-id="72b27-113">So veröffentlichen Sie die Standortdatenbank</span><span class="sxs-lookup"><span data-stu-id="72b27-113">To publish the location database</span></span>

  - <span data-ttu-id="72b27-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="72b27-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

  - <span data-ttu-id="72b27-115">Führen Sie das folgende Cmdlet aus, um die Standortdatenbank zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="72b27-115">Run the following cmdlet to publish the location database.</span></span>
    
        Publish-CsLisConfiguration

<span data-ttu-id="72b27-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72b27-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

