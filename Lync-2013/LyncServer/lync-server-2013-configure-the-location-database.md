---
title: 'Lync Server 2013: Konfigurieren der Standortdatenbank'
description: 'Lync Server 2013: Konfigurieren der Standortdatenbank'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the location database
ms:assetid: 8544be31-6958-47ef-b926-fdc80d56191c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398679(v=OCS.15)
ms:contentKeyID: 48184704
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 877c83976ca0db9abc3a9e57d4a1cf5adaa1291a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433612"
---
# <a name="configure-the-location-database-in-lync-server-2013"></a><span data-ttu-id="7def9-103">Configure the location database in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7def9-103">Configure the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7def9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7def9-104">

<span> </span></span></span>

<span data-ttu-id="7def9-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="7def9-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="7def9-106">Sie müssen zunächst die Standortdatenbank konfigurieren, um Clients für die automatische Ermittlung ihres Standorts innerhalb eines Netzwerks zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7def9-106">To enable clients to automatically detect their location within a network, you first need to configure the location database.</span></span> <span data-ttu-id="7def9-107">Wenn Sie eine Standortdatenbank nicht konfigurieren und der Standort, der in der Standortrichtlinie **erforderlich** ist, auf **Ja** oder **Disclaimer** eingestellt ist, wird der Benutzer aufgefordert, einen Standort manuell einzugeben.</span><span class="sxs-lookup"><span data-stu-id="7def9-107">If you do not configure a location database, and **Location Required** in the location policy is set to **Yes** or **Disclaimer**, the user will be prompted to manually enter a location.</span></span>

<span data-ttu-id="7def9-108">Um die Standortdatenbank zu konfigurieren, führen Sie die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="7def9-108">To configure the location database, you will perform the following tasks:</span></span>

1.  <span data-ttu-id="7def9-109">Füllen Sie die Datenbank mit einer Zuordnung von Netzwerkelementen zu Standorten auf.</span><span class="sxs-lookup"><span data-stu-id="7def9-109">Populate the database with a mapping of network elements to locations.</span></span> <span data-ttu-id="7def9-110">Wenn Sie ein Notfall Standort-Identifikationsnummer (Elin)-Gateway verwenden, müssen Sie das Elin in das \<CompanyName\> Feld einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="7def9-110">If you use an Emergency Location Identification Number (ELIN) gateway, you need to include the ELIN in the \<CompanyName\> field.</span></span>

2.  <span data-ttu-id="7def9-111">Überprüfen Sie die Adressen anhand der MSAG-Daten (Master Street Address Guide), die vom Dienstanbieter für E9-1-1 verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7def9-111">Validate the addresses against the master street address guide (MSAG) that is maintained by the E9-1-1 service provider.</span></span>

3.  <span data-ttu-id="7def9-112">Veröffentlichen Sie die aktualisierte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="7def9-112">Publish the updated database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7def9-113">Alternativ können Sie eine sekundäre Standort Quelldatenbank definieren, die für die Position der Standortdatenbank verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7def9-113">Alternately, you can define a secondary location source database that can be used in placed of the location database.</span></span> <span data-ttu-id="7def9-114">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Konfigurieren eines sekundären Standort Informationsdiensts in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7def9-114">For details, see <A href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7def9-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7def9-115">In This Section</span></span>

  - [<span data-ttu-id="7def9-116">Auffüllen der Standortdatenbank in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7def9-116">Populate the location database in Lync Server 2013</span></span>](lync-server-2013-populate-the-location-database.md)

  - [<span data-ttu-id="7def9-117">Überprüfen von Adressen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7def9-117">Validate addresses in Lync Server 2013</span></span>](lync-server-2013-validate-addresses.md)

  - [<span data-ttu-id="7def9-118">Veröffentlichen der Standortdatenbank aus lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7def9-118">Publish the location database from Lync Server 2013</span></span>](lync-server-2013-publish-the-location-database.md)

<span data-ttu-id="7def9-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7def9-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

