---
title: 'Lync Server 2013: Active Directory-Schemaerweiterungen, -Klassen und -Attribute, die von Lync Server verwendet werden'
description: 'Lync Server 2013: Active Directory-Schemaerweiterungen,-Klassen und-Attribute, die von lync Server verwendet werden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory schema extensions, classes, and attributes used by Lync Server 2013
ms:assetid: 579bfa5a-9443-46dd-9a8e-07d00ba2824d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398379(v=OCS.15)
ms:contentKeyID: 48184188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: beac778d3315573f4d5cc6cb9c827a3a2fce9d0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393870"
---
# <a name="active-directory-schema-extensions-classes-and-attributes-used-by-lync-server-2013"></a><span data-ttu-id="ac91e-103">Active Directory-Schemaerweiterungen, -Klassen und -Attribute, die von Lync Server 2013 verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ac91e-103">Active Directory schema extensions, classes, and attributes used by Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ac91e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ac91e-104">

<span> </span></span></span>

<span data-ttu-id="ac91e-105">_**Letztes Änderungsdatum des Themas:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="ac91e-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="ac91e-106">Dieser Referenzabschnitt enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="ac91e-106">This reference section includes the following information:</span></span>

  - <span data-ttu-id="ac91e-107">Active Directory-Schemaerweiterungen, die neu sind oder für lync Server 2013 geändert wurden</span><span class="sxs-lookup"><span data-stu-id="ac91e-107">Active Directory schema extensions that are new or changed for Lync Server 2013</span></span>
    
    <span data-ttu-id="ac91e-108">Das Active Directory-Schema enthält formale Definitionen jeder Objektklasse, die in einer Active Directory-Gesamtstruktur erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="ac91e-108">The Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="ac91e-109">Das Schema enthält auch formale Definitionen für alle Attribute, die für ein Active Directory-Objekt vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="ac91e-109">The schema also contains formal definitions of every attribute that can exist on an Active Directory object.</span></span> <span data-ttu-id="ac91e-110">Der globale Active Directory-Katalog enthält Replikate aller Objekte für die Gesamtstruktur sowie eine Teilmenge der Attribute für jedes Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac91e-110">The Active Directory global catalog contains replicas of all the objects for the forest, along with a subset of the attributes for each object.</span></span> <span data-ttu-id="ac91e-111">In diesem Abschnitt werden die Klassen und Attribute beschrieben, die in lync Server 2013 neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac91e-111">This section describes the classes and attributes that are new or changed in Lync Server 2013.</span></span>

  - <span data-ttu-id="ac91e-112">Alle von lync Server verwendeten Klassen mit einer Beschreibung der einzelnen Klassen</span><span class="sxs-lookup"><span data-stu-id="ac91e-112">All the classes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="ac91e-113">Alle von lync Server verwendeten Attribute mit einer Beschreibung der einzelnen Attribute</span><span class="sxs-lookup"><span data-stu-id="ac91e-113">All the attributes used by Lync Server, with a description of each</span></span>

  - <span data-ttu-id="ac91e-114">Eine Liste der von lync Server verwendeten Klassen mit den Attributen, die jeweils enthalten können</span><span class="sxs-lookup"><span data-stu-id="ac91e-114">A list of the classes used by Lync Server, with the attributes each may contain</span></span>

  - <span data-ttu-id="ac91e-115">Globale Einstellungen und Objekte, zusätzlich zu den universellen Dienst-und Verwaltungsgruppen, die während der Gesamtstrukturvorbereitung erstellt werden</span><span class="sxs-lookup"><span data-stu-id="ac91e-115">Global settings and objects, in addition to the universal service and administration groups that are created during forest preparation</span></span>

  - <span data-ttu-id="ac91e-116">Zugriffssteuerungseinträge (ACEs), die im Domänenstamm und in den integrierten Containern während der Domänenvorbereitung erstellt werden</span><span class="sxs-lookup"><span data-stu-id="ac91e-116">Access control entries (ACEs) that are created on the domain root and built-in containers during domain preparation</span></span>

  - <span data-ttu-id="ac91e-117">Änderungen, die an einer Active Directory-Organisationseinheit (OU) durch das Grant \_ CsSetupPermission-Cmdlet vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="ac91e-117">Changes that are made on an Active Directory organizational unit (OU) by the Grant\_CsSetupPermission cmdlet.</span></span>

  - <span data-ttu-id="ac91e-118">Änderungen, die an einer Active Directory-OU durch das Grant \_ CsOUPermission-Cmdlet vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="ac91e-118">Changes that are made on an Active Directory OU by the Grant\_CsOUPermission cmdlet.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ac91e-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ac91e-119">In This Section</span></span>

  - [<span data-ttu-id="ac91e-120">Schema Änderungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac91e-120">Schema changes in Lync Server 2013</span></span>](lync-server-2013-schema-changes-in-lync-server-2013.md)

  - [<span data-ttu-id="ac91e-121">Schema Klassen und Beschreibungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac91e-121">Schema classes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-classes-and-descriptions.md)

  - [<span data-ttu-id="ac91e-122">Schema Attribute und Beschreibungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac91e-122">Schema attributes and descriptions in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-and-descriptions.md)

  - [<span data-ttu-id="ac91e-123">Schema Attribute nach Klasse in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ac91e-123">Schema attributes by class in Lync Server 2013</span></span>](lync-server-2013-schema-attributes-by-class.md)

  - [<span data-ttu-id="ac91e-124">Änderungen, die von der Gesamtstrukturvorbereitung in lync Server 2013 vorgenommen wurden</span><span class="sxs-lookup"><span data-stu-id="ac91e-124">Changes made by forest preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-forest-preparation.md)

  - [<span data-ttu-id="ac91e-125">Von der Domänenvorbereitung in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="ac91e-125">Changes made by domain preparation in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-domain-preparation.md)

  - [<span data-ttu-id="ac91e-126">Von Grant-CsSetupPermission in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="ac91e-126">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission)

  - [<span data-ttu-id="ac91e-127">Von Grant-CsOUPermission in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="ac91e-127">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>](lync-server-2013-changes-made-by-https://docs.microsoft.com/powershell/module/skype/Grant-CsOUPermission)

<span data-ttu-id="ac91e-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ac91e-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

