---
title: Definieren der Benutzeroberfläche für den manuellen Erwerb eines Standorts
description: Definieren der Benutzeroberfläche für den manuellen Erwerb eines Standorts
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining the user experience for manually acquiring a location
ms:assetid: d37f67d3-e248-483b-b64c-3986559ef357
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398912(v=OCS.15)
ms:contentKeyID: 48185435
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74e4a399e8010cfc22430216ef6e3c11fc9a7bdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430945"
---
# <a name="defining-the-user-experience-for-manually-acquiring-a-location-in-lync-server-2013"></a><span data-ttu-id="153e2-103">Definieren der Benutzeroberfläche für den manuellen Erwerb eines Speicherorts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="153e2-103">Defining the user experience for manually acquiring a location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="153e2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="153e2-104">

<span> </span></span></span>

<span data-ttu-id="153e2-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="153e2-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="153e2-p101">Wenn ein Client sich außerhalb des Netzwerks oder in einem nicht definierten Subnetz befindet, kann der Benutzer manuell einen Standort eingeben. Bei einem Notruf wird der Anruf jedoch zuerst an ein nationales/regionales Telefoncenter für Notrufe (Emergency Call Response Center, ECRC) und erst anschließend an eine Rettungsleitstelle (Public Safety Answering Point, PSAP) weitergeleitet. Der Anrufer wird vom ECRC zur Angabe seines Standorts aufgefordert und anschließend wird der Notruf anhand der bereitgestellten Informationen an die entsprechende Rettungsleitstelle weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="153e2-p101">If a client is located outside the network, or in an undefined subnet, the user can manually enter a location. But during an emergency call, the call will first be routed to a national/regional E9-1-1 Emergency Call Response Center (ECRC) dispatcher before being routed to a Public Safety Answering Point (PSAP). The ECRC will verbally query the caller for a location and then forward the call to the appropriate PSAP, based on the information provided.</span></span>

  - <span data-ttu-id="153e2-109">**Sollten Benutzer zur Eingabe eines Speicherorts aufgefordert werden, wenn Sie nicht automatisch vom standortinformationsdienst bereitgestellt werden?**</span><span class="sxs-lookup"><span data-stu-id="153e2-109">**Should users be prompted to enter a location when one is not automatically provided by the Location Information service?**</span></span>  
    <span data-ttu-id="153e2-110">Wenn ein Client sich beispielsweise in einem nicht definierten Subnetz, zu Hause, in einem Hotel oder an einem anderen Standort außerhalb des Netzwerks befindet, sollte der Benutzer zur Eingabe eines Standorts aufgefordert werden?</span><span class="sxs-lookup"><span data-stu-id="153e2-110">For example, if a client is located in an undefined subnet, at home, in a hotel, or anywhere else outside the network, should the user be required to enter a location?</span></span>
    
    <span data-ttu-id="153e2-p102">Sie können die Einstellung **Standort erforderlich** in der Standortrichtlinie konfigurieren, um das Clientverhalten zu definieren. Lautet die Einstellung „Nein“, wird der Benutzer nicht zur Eingabe eines Standorts aufgefordert. Lautet die Einstellung „Ja“, wird der Benutzer zur Eingabe eines Standorts aufgefordert, kann die Eingabeaufforderung jedoch verwerfen. Mit der Einstellung „Haftungsausschluss“ wird der Benutzer zur Eingabe eines Standorts aufgefordert. Wenn er dann versucht, diese Aufforderung zu verwerfen, wird ein Haftungsausschluss angezeigt. In allen Fällen kann der Benutzer den Client weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="153e2-p102">You can configure the **Location Required** setting in the location policy to define the client behavior. Setting this value to No means that the user will not be prompted for a location. Setting this value to Yes means that the user will be prompted for a location, but can dismiss the prompt. Setting this value to Disclaimer means that the user will be prompted for a location, and will be shown a disclaimer if they try to dismiss the prompt. In all cases, the user can continue to use the client as usual.</span></span>

<span data-ttu-id="153e2-116">Wenn ein Benutzer einen Standort manuell eingibt, wird dieser basierend auf der MAC-Adresse des Standardgateways des Clientnetzwerks zugeordnet und in einer benutzerspezifischen Tabelle auf dem Client gespeichert.</span><span class="sxs-lookup"><span data-stu-id="153e2-116">When a user manually enters a location, the location is mapped to the MAC address of the default gateway of the client’s network, and is stored in a per-user table located on the client.</span></span> <span data-ttu-id="153e2-117">Wenn der Benutzer zu einem zuvor gespeicherten Speicherort zurückkehrt, legt sich der lync-Client automatisch an diesen Speicherort fest.</span><span class="sxs-lookup"><span data-stu-id="153e2-117">When the user returns to any previously stored location, the Lync client automatically sets itself to that location.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="153e2-118">Sie können nur den aktuellen Standort Ihres Clients ändern. Darüber hinaus können Sie jeden Standort, der in der Tabelle des lokalen Benutzers gespeichert ist, löschen.</span><span class="sxs-lookup"><span data-stu-id="153e2-118">You can modify only the current location of your client, but you can also delete any location stored in the local user’s table.</span></span>



<span data-ttu-id="153e2-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="153e2-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

