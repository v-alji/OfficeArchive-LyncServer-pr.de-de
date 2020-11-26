---
title: Migrieren vorhandener Besprechungen und Besprechungsinhalte
description: Migrieren vorhandener Besprechungen und Besprechungsinhalte
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d94dd35063a121a057a218c27fdb36e42a155b77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443804"
---
# <a name="migrate-existing-meetings-and-meeting-content"></a><span data-ttu-id="8a35c-103">Migrieren vorhandener Besprechungen und Besprechungsinhalte</span><span class="sxs-lookup"><span data-stu-id="8a35c-103">Migrate existing meetings and meeting content</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a35c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a35c-104">

<span> </span></span></span>

<span data-ttu-id="8a35c-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="8a35c-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="8a35c-106">Wenn ein Benutzerkonto von lync Server 2010 auf einen lync Server 2013-Server verschoben wird, werden die folgenden Informationen mit diesem Benutzerkonto verschoben:</span><span class="sxs-lookup"><span data-stu-id="8a35c-106">When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:</span></span>

  - <span data-ttu-id="8a35c-107">**Besprechungen, die der Benutzer bereits geplant** hat.</span><span class="sxs-lookup"><span data-stu-id="8a35c-107">**Meetings already scheduled by the user**.</span></span> <span data-ttu-id="8a35c-108">Dazu gehören das Verschieben von Konferenz Verzeichnissen und Konferenzdaten.</span><span class="sxs-lookup"><span data-stu-id="8a35c-108">This includes moving the conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="8a35c-109">**Persönliche Identifikationsnummer (PIN) des Benutzers**.</span><span class="sxs-lookup"><span data-stu-id="8a35c-109">**User’s personal identification number (PIN)**.</span></span> <span data-ttu-id="8a35c-110">Die aktuelle PIN des Benutzers funktioniert weiterhin, bis er abläuft oder der Benutzer eine neue PIN anfordert.</span><span class="sxs-lookup"><span data-stu-id="8a35c-110">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="8a35c-111">Die folgenden Benutzerkontoinformationen werden nicht auf den neuen Server verschoben.</span><span class="sxs-lookup"><span data-stu-id="8a35c-111">The following user account information does not move to the new server.</span></span>

  - <span data-ttu-id="8a35c-112">**Besprechungsinhalt**.</span><span class="sxs-lookup"><span data-stu-id="8a35c-112">**Meeting content**.</span></span> <span data-ttu-id="8a35c-113">Verwenden Sie den Parameter **-MoveConferenceData** als Teil des Cmdlets **Move-CsUser** , um den während einer Besprechung freigegebenen Inhalt zu verschieben, beispielsweise PowerPoint, Whiteboard, Anlagen oder Umfragedaten.</span><span class="sxs-lookup"><span data-stu-id="8a35c-113">In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.</span></span>

<span data-ttu-id="8a35c-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a35c-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

