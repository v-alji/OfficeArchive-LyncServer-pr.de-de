---
title: 'Lync Server 2013: Konfigurieren eines sekundären Standort Informationsdiensts'
description: 'Lync Server 2013: Konfigurieren eines sekundären Standort Informationsdiensts'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure a secondary Location Information service
ms:assetid: 083ffbc6-7c18-4141-85f9-8825b62c3d10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398138(v=OCS.15)
ms:contentKeyID: 48183334
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1721299a0c70535dff8dd05e31712ee6a8d93691
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434214"
---
# <a name="configure-a-secondary-location-information-service-in-lync-server-2013"></a><span data-ttu-id="fbe2b-103">Konfigurieren eines sekundären Standort Informationsdiensts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbe2b-103">Configure a secondary Location Information service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbe2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbe2b-104">

<span> </span></span></span>

<span data-ttu-id="fbe2b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="fbe2b-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="fbe2b-106">Lync Server 2013 stellt eine Webdienstschnittstelle bereit, die Sie verwenden können, um den standortinformationsdienst auf eine SLS-Datenbank (Secondary Location Source) zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-106">Lync Server 2013 provides a web service interface that you can use to point the Location Information service to a Secondary Location Source (SLS) database.</span></span> <span data-ttu-id="fbe2b-107">Die Webdienstschnittstelle, die eine Verbindung mit der SLS-Datenbank herstellt, muss dem Location Information Service-WSDL entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-107">The web service interface that connects to the SLS database must conform to Location Information service WSDL.</span></span> <span data-ttu-id="fbe2b-108">Wenn sowohl eine Standortdatenbank als auch eine sekundäre Standortdatenbank konfiguriert sind, fragt der standortinformationsdienst zuerst die Standortdatenbank ab, und wenn keine Übereinstimmung gefunden wird, sendet die standortanforderung vom Client an die SLS-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-108">If both a location database and secondary location database are configured, the Location Information service first queries the location database, and if no match is found, sends the location request from the client to the SLS database.</span></span> <span data-ttu-id="fbe2b-109">Wenn der Standort im SLS vorhanden ist, sendet der standortinformationsdienst den Standort dann zurück an den Client.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-109">If the location exists in the SLS, the Location Information service then sends the location back to the client.</span></span>

<span data-ttu-id="fbe2b-110">Ausführliche Informationen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für das folgende Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="fbe2b-110">For details, see the Lync Server Management Shell documentation for the following cmdlet:</span></span>

  - <span data-ttu-id="fbe2b-111">**Satz-CsWebServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="fbe2b-111">**Set-CsWebServiceConfiguration**</span></span>

<div>

## <a name="to-configure-secondary-location-database"></a><span data-ttu-id="fbe2b-112">So konfigurieren Sie die sekundäre Standortdatenbank</span><span class="sxs-lookup"><span data-stu-id="fbe2b-112">To configure Secondary Location database</span></span>

1.  <span data-ttu-id="fbe2b-113">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="fbe2b-114">Führen Sie das folgende Cmdlet aus, um die URL für den Speicherort der SLS-Datenbank zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fbe2b-114">Run the following cmdlet to configure the URL for the location of the secondary location database.</span></span>
    
        Set-CsWebServiceConfiguration -SecondaryLocationSourceURL "<web service url>" 

<span data-ttu-id="fbe2b-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbe2b-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

