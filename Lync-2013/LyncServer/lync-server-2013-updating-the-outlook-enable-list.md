---
title: 'Lync Server 2013: Aktualisieren der Outlook-Aktivierungs Liste'
description: 'Lync Server 2013: Aktualisieren der Outlook-Aktivierungs Liste'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Updating the Outlook enable list
ms:assetid: 5db120dc-52f9-4dde-acb9-3824ae245086
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215438(v=OCS.15)
ms:contentKeyID: 48242739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 96edc327fa1b63d5da95eb6ea36a2296659910d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394842"
---
# <a name="updating-the-outlook-enable-list-in-lync-server-2013"></a><span data-ttu-id="9df90-103">Aktualisieren der Outlook-Aktivierungs Liste in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9df90-103">Updating the Outlook enable list in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9df90-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9df90-104">

<span> </span></span></span>

<span data-ttu-id="9df90-105">_**Letztes Änderungsdatum des Themas:** 2013-01-07_</span><span class="sxs-lookup"><span data-stu-id="9df90-105">_**Topic Last Modified:** 2013-01-07_</span></span>

<span data-ttu-id="9df90-106">Sie können sicherstellen, dass das Online Besprechungs-Add-in für Microsoft lync 2013 für Benutzer immer aktiviert bleibt, indem Sie eine Richtlinie erstellen, die Sie in die Add-in-Verwaltungsliste für Outlook einfügt.</span><span class="sxs-lookup"><span data-stu-id="9df90-106">You can ensure that Online Meeting Add-in for Microsoft Lync 2013 always remains enabled for users by creating a policy that includes it in the Add-in Management List for Outlook.</span></span> <span data-ttu-id="9df90-107">Die Richtlinie für Add-in-Verwaltungs Listen ist in den Office administrative Template-Dateien für die Gruppenrichtlinien-Verwaltungskonsole enthalten.</span><span class="sxs-lookup"><span data-stu-id="9df90-107">The Add-in Management List policy is included in the Office administrative template files for the Group Policy Management Console.</span></span> <span data-ttu-id="9df90-108">Sie erstellt einen Registrierungsschlüssel unter HKCU \\ \\ -Software Richtlinien \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ Resilienz \\ -Add-in.</span><span class="sxs-lookup"><span data-stu-id="9df90-108">It creates a registry key under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList.</span></span> <span data-ttu-id="9df90-109">Sie können diesem Schlüssel einen Wert für den ucaddin.dll hinzufügen und den ucaddin.dll Wert so konfigurieren, dass er immer aktiviert ist und die Benutzer ihn nicht manuell deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="9df90-109">You can add a value for the ucaddin.dll to this key, and configure the ucaddin.dll value so that it is always enabled and so that users cannot manually disable it</span></span>

<div>

## <a name="to-add-ucaddindll-to-the-outlook-add-in-list"></a><span data-ttu-id="9df90-110">So fügen Sie der Outlook-Add-in-Liste ucaddin.dll hinzu</span><span class="sxs-lookup"><span data-stu-id="9df90-110">To Add ucaddin.dll to the Outlook Add-in List</span></span>

  - <span data-ttu-id="9df90-111">Fügen Sie dem Registrierungsschlüssel addinlist unter HKCU- \\ Software \\ Richtlinien, \\ Microsoft \\ Office \\ 15,0 \\ Outlook15 \\ -Flexibilitäts-Add-in \\ , den folgenden Wert hinzu:</span><span class="sxs-lookup"><span data-stu-id="9df90-111">To the AddinList registry key, located under HKCU\\Software\\Policies\\Microsoft\\Office\\15.0\\Outlook15\\Resiliency\\AddinList, add the following value:</span></span>
    
      - <span data-ttu-id="9df90-112">Registry Type = reg \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9df90-112">Registry Type = REG\_SZ</span></span>
    
      - <span data-ttu-id="9df90-113">Name = ucaddin.dll</span><span class="sxs-lookup"><span data-stu-id="9df90-113">Name = ucaddin.dll</span></span>
    
      - <span data-ttu-id="9df90-114">Wert = 1 (gibt an, dass das Add-in immer aktiviert ist und nicht vom Endbenutzer verwaltet werden kann)</span><span class="sxs-lookup"><span data-stu-id="9df90-114">Value = 1 (specifies that the add-in is always enabled and cannot be managed by the end user)</span></span>

<span data-ttu-id="9df90-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9df90-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

