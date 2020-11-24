---
title: 'Lync Server 2013: Bereitstellen des einheitlichen Kontaktspeichers'
description: 'Lync Server 2013: Bereitstellen des einheitlichen Kontaktspeichers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying unified contact store
ms:assetid: 68959d58-ac8a-45de-afcd-b9de2c36799c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204963(v=OCS.15)
ms:contentKeyID: 48184373
ms.date: 06/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 056792d2e4ea66699b276d0d571e83c8a0256483
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393986"
---
# <a name="deploying-unified-contact-store-in-lync-server-2013"></a><span data-ttu-id="a05cd-103">Bereitstellen des einheitlichen Kontaktspeichers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a05cd-103">Deploying unified contact store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a05cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a05cd-104">

<span> </span></span></span>

<span data-ttu-id="a05cd-105">_**Letztes Änderungsdatum des Themas:** 2016-06-06_</span><span class="sxs-lookup"><span data-stu-id="a05cd-105">_**Topic Last Modified:** 2016-06-06_</span></span>

<span data-ttu-id="a05cd-106">Für die Aktivierung des Unified Contact Stores in lync Server 2013 sind keine topologieeinstellungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a05cd-106">Enabling unified contact store in Lync Server 2013 does not require any topology settings.</span></span> <span data-ttu-id="a05cd-107">Für die Aktivierung des Unified Contact Store für Benutzer ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="a05cd-107">Enabling unified contact store for users requires the following:</span></span>

  - <span data-ttu-id="a05cd-108">Die Richtlinie für den einheitlichen Kontaktspeicher muss aktiviert sein (was in der Standardeinstellung der Fall ist).</span><span class="sxs-lookup"><span data-stu-id="a05cd-108">Unified contact store policy is enabled (default is enabled).</span></span>

  - <span data-ttu-id="a05cd-109">Benutzer melden sich mindestens einmal mit lync 2013 an.</span><span class="sxs-lookup"><span data-stu-id="a05cd-109">Users log in with Lync 2013 at least once.</span></span>

<span data-ttu-id="a05cd-110">Nachdem die Kontakte eines Benutzers migriert wurden, was automatisch geschieht, wenn sich ein Benutzer mit lync 2013 anmeldet, kann der Benutzer über lync 2013, Outlook 2013 oder Outlook Web Access auf seine lync-Kontakte zugreifen und diese verwalten.</span><span class="sxs-lookup"><span data-stu-id="a05cd-110">After a user’s contacts have been migrated, which happens automatically when a user logs in with Lync 2013, the user can access and manage their Lync contacts from Lync 2013, Outlook 2013, or Outlook Web Access.</span></span> <span data-ttu-id="a05cd-111">Der Benutzer muss nicht bei lync angemeldet sein, um seine Kontakte aus Outlook oder Outlook Web Access zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a05cd-111">The user does not have to be logged in to Lync to manage their contacts from Outlook or Outlook Web Access.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a05cd-112">Wenn ein Benutzer sich nach der Migration von lync 2010 anmeldet, sind Kontakte und Gruppen verfügbar und auf dem neuesten Stand, aber der Benutzer kann diese Kontakte nicht verwalten (das heißt, Sie können diese Kontakte hinzufügen, löschen, verschieben, markieren, Markierung oder ändern).</span><span class="sxs-lookup"><span data-stu-id="a05cd-112">If a user logs in from Lync 2010 after migration, contacts and groups are available and up-to-date, but the user cannot manage (that is, add, delete, move, tag, untag, or modify) those contacts.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a05cd-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a05cd-113">In This Section</span></span>

  - [<span data-ttu-id="a05cd-114">Aktivieren von Benutzern für den einheitlichen Kontaktspeicher in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a05cd-114">Enable users for unified contact store in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-unified-contact-store.md)

  - [<span data-ttu-id="a05cd-115">Migrieren von Benutzern zum einheitlichen Kontaktspeicher in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a05cd-115">Migrate users to unified contact store in Lync Server 2013</span></span>](lync-server-2013-migrate-users-to-unified-contact-store.md)

  - [<span data-ttu-id="a05cd-116">Zurücksetzen von migrierten Benutzern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a05cd-116">Roll back migrated users in Lync Server 2013</span></span>](lync-server-2013-roll-back-migrated-users.md)

<span data-ttu-id="a05cd-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a05cd-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

