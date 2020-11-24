---
title: 'Lync Server 2013: Konfigurieren von Wählplänen für Einwahlkonferenzen'
description: 'Lync Server 2013: Konfigurieren von Wählplänen für Einwahlkonferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure dial plans for dial-in conferencing
ms:assetid: a3e0958e-384f-43e5-b4c9-686b6ecac7ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412768(v=OCS.15)
ms:contentKeyID: 48185051
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28123f905288ce35b6f470168962a3d8e6faa22b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395127"
---
# <a name="configure-dial-plans-for-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="72185-103">Konfigurieren von Wählplänen für Einwahlkonferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72185-103">Configure dial plans for dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="72185-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="72185-104">

<span> </span></span></span>

<span data-ttu-id="72185-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="72185-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="72185-106">Bei der Bereitstellung von Einwahlkonferenzen müssen Sie einen oder mehrere Sätze mit Wähleinstellungen zum Routen von Zugriffsnummern für die Einwahl erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="72185-106">When you deploy dial-in conferencing, you need to create or modify one or more dial plans for routing dial-in access phone numbers.</span></span> <span data-ttu-id="72185-107">Stellen Sie sicher, dass mindestens eine Normalisierungsregel in den einzelnen Wähleinstellungen Telefonerweiterungen in vollständige Telefonnummern im E. 164-Format umwandelt.</span><span class="sxs-lookup"><span data-stu-id="72185-107">Make sure that at least one normalization rule in each dial plan converts telephone extensions into complete phone numbers in E.164 format.</span></span> <span data-ttu-id="72185-108">Benutzer von Einwahlkonferenzen nehmen an Konferenzen als authentifizierte Unternehmensbenutzer teil, indem sie ihre PIN und die Telefonnummer eingeben.</span><span class="sxs-lookup"><span data-stu-id="72185-108">Users of dial-in conferencing join conferences as authenticated enterprise users by entering their personal identification number (PIN) and their phone number.</span></span> <span data-ttu-id="72185-109">Sie benötigen eine Normalisierungsregel zum Konvertieren von Durchwahlen in vollständige Rufnummern, damit Benutzer bei Eingabe einer Durchwahl authentifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="72185-109">You need a normalization rule to convert extensions into complete phone numbers so that users can be authenticated when they enter just a telephone extension.</span></span>

<span data-ttu-id="72185-110">Gehen Sie wie folgt vor, um Wählpläne für Einwahlkonferenzen einzurichten:</span><span class="sxs-lookup"><span data-stu-id="72185-110">To set up dial plans for dial-in conferencing, do the following:</span></span>

  - <span data-ttu-id="72185-111">Unabhängig davon, ob Sie Enterprise-VoIP bereitstellen oder nicht, fügen Sie zu den Wähleinstellungen eine Region für Einwahlkonferenzen hinzu und stellen Sie sicher, dass Ihre Einwahlnummern einwandfrei von einer Normalisierungsregel umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="72185-111">Whether or not you deploy Enterprise Voice, modify the global dial plan to add a dial-in conferencing region and to make sure that a normalization rule accurately converts your dial-in access numbers.</span></span> <span data-ttu-id="72185-112">Ausführliche Anweisungen finden Sie unter [Ändern von Wähleinstellungen in lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="72185-112">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

  - <span data-ttu-id="72185-113">Wenn Sie Enterprise-VoIP nicht bereitstellen, erstellen Sie Wählpläne für Ihre Einwahlnummern.</span><span class="sxs-lookup"><span data-stu-id="72185-113">If you did not deploy Enterprise Voice, create dial plans for your dial-in conferencing access numbers.</span></span> <span data-ttu-id="72185-114">Fügen Sie auf jeden Fall eine Region für Einwahlkonferenzen hinzu.</span><span class="sxs-lookup"><span data-stu-id="72185-114">Be sure to include a dial-in conferencing region.</span></span> <span data-ttu-id="72185-115">Ausführliche Anweisungen finden Sie unter [Erstellen eines Wählplans in lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="72185-115">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

  - <span data-ttu-id="72185-116">Wenn Sie Enterprise-VoIP bereitgestellt haben, ändern Sie Enterprise-sprach Wählpläne nach Bedarf, um Regionen einzubeziehen und geeignete Normalisierungsregeln für Einwahl Zugriffsnummern zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="72185-116">If you deployed Enterprise Voice, modify Enterprise Voice dial plans as necessary to include regions and use appropriate normalization rules for dial-in access numbers.</span></span> <span data-ttu-id="72185-117">Ausführliche Anweisungen finden Sie unter [Ändern von Wähleinstellungen in lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="72185-117">For detailed instructions, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span> <span data-ttu-id="72185-118">Sie können auch dedizierte Wählpläne erstellen, die nur für Einwahl Zugriffsnummern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72185-118">You can also create dedicated dial plans that are used only for dial-in access numbers.</span></span> <span data-ttu-id="72185-119">Ausführliche Anweisungen finden Sie unter [Erstellen eines Wählplans in lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="72185-119">For detailed instructions, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<span data-ttu-id="72185-120">Details zu Planungsregionen finden Sie unter [Anforderungen für Einwahlkonferenzen in lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="72185-120">For details about planning regions, see [Dial-in conferencing requirements in Lync Server 2013](lync-server-2013-dial-in-conferencing-requirements.md) in the Planning documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="72185-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="72185-121">In This Section</span></span>

  - [<span data-ttu-id="72185-122">Anzeigen von Wähl Planinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72185-122">View dial plan information in Lync Server 2013</span></span>](lync-server-2013-view-dial-plan-information.md)

  - [<span data-ttu-id="72185-123">Erstellen eines Wählplans in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72185-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)

  - [<span data-ttu-id="72185-124">Ändern eines Wählplans in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72185-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)

  - [<span data-ttu-id="72185-125">Definieren von Normalisierungsregeln in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="72185-125">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)

<span data-ttu-id="72185-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="72185-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

