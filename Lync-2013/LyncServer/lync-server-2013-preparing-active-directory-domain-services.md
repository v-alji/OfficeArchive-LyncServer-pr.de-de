---
title: 'Lync Server 2013: Vorbereiten der Active Directory-Domänendienste'
description: 'Lync Server 2013: Vorbereiten der Active Directory-Domänendienste'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing Active Directory Domain Services for Lync Server 2013
ms:assetid: 7e126464-5d29-4013-9c44-0ccc2fbdea0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398630(v=OCS.15)
ms:contentKeyID: 48184620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6ecfcffd55739bc6d1bf1b83a701a0fd515ec56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424219"
---
# <a name="preparing-active-directory-domain-services-for-lync-server-2013"></a><span data-ttu-id="f9b4c-103">Vorbereiten der Active Directory-Domänendienste für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-103">Preparing Active Directory Domain Services for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9b4c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9b4c-104">

<span> </span></span></span>

<span data-ttu-id="f9b4c-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f9b4c-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f9b4c-106">Vor der Bereitstellung und dem Betrieb von lync Server 2013 müssen Sie die Active Directory-Domänendienste vorbereiten, indem Sie das Schema erweitern und dann Objekte erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-106">Before you deploy and operate Lync Server 2013, you must prepare Active Directory Domain Services by extending the schema and then creating and configuring objects.</span></span> <span data-ttu-id="f9b4c-107">Die Schemaerweiterungen fügen die Active Directory-Klassen und-Attribute hinzu, die für lync Server erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-107">The schema extensions add the Active Directory classes and attributes that are required by Lync Server.</span></span>

<span data-ttu-id="f9b4c-108">In den Themen in diesem Abschnitt wird beschrieben, wie Sie AD DS für die Bereitstellung von lync Server vorbereiten und wie Sie Setup-und Organisations Einheits Berechtigungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f9b4c-108">The topics in this section describe how to prepare AD DS for deploying Lync Server and how to assign setup and organizational unit (OU) permissions.</span></span> <span data-ttu-id="f9b4c-109">Details zu den für lync Server erforderlichen Schemaänderungen finden Sie unter [Active Directory-Schemaerweiterungen,-Klassen und-Attribute, die von lync Server 2013 verwendet werden](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="f9b4c-109">For details about the schema changes required for Lync Server, see [Active Directory schema extensions, classes, and attributes used by Lync Server 2013](lync-server-2013-active-directory-schema-extensions-classes-and-attributes-used-by-lync-server.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f9b4c-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f9b4c-110">In This Section</span></span>

  - [<span data-ttu-id="f9b4c-111">Active Directory-Infrastrukturanforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-111">Active Directory infrastructure requirements for Lync Server 2013</span></span>](lync-server-2013-active-directory-infrastructure-requirements.md)

  - [<span data-ttu-id="f9b4c-112">Übersicht über die Vorbereitung der Active Directory-Domänendienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-112">Overview of Active Directory Domain Services preparation in Lync Server 2013</span></span>](lync-server-2013-overview-of-active-directory-domain-services-preparation.md)

  - [<span data-ttu-id="f9b4c-113">Vorbereiten der Active Directory-Domänendienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-113">Preparing Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-active-directory-domain-services.md)

  - [<span data-ttu-id="f9b4c-114">Vorbereiten gesperrter Active Directory-Domänendienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-114">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md)

  - [<span data-ttu-id="f9b4c-115">Gewähren von Berechtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b4c-115">Granting permissions in Lync Server 2013</span></span>](lync-server-2013-granting-permissions.md)

<span data-ttu-id="f9b4c-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9b4c-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

