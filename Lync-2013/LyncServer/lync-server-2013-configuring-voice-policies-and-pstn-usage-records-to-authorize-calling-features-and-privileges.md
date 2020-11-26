---
title: 'Lync Server 2013: Konfigurieren von VoIP-Richtlinien und PSTN-Verwendungsdatensätzen zum Autorisieren von Anruffunktionen und -berechtigungen'
description: 'Lync Server 2013: Konfigurieren von VoIP-Richtlinien und PSTN-Verwendungsdatensätzen zum Autorisieren von Anruffeatures und-Berechtigungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring voice policies and PSTN usage records to authorize calling features and privileges
ms:assetid: 63f22010-a3d7-4cbd-86e8-6fc0e13c2b84
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398450(v=OCS.15)
ms:contentKeyID: 48184307
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a12c9c64c3f02effba7c7709321eda91350ebb75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432394"
---
# <a name="configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges-in-lync-server-2013"></a><span data-ttu-id="36416-103">Konfigurieren von VoIP-Richtlinien und PSTN-Verwendungsdatensätzen zum Autorisieren von Anruffunktionen und -berechtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36416-103">Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="36416-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="36416-104">

<span> </span></span></span>

<span data-ttu-id="36416-105">_**Letztes Änderungsdatum des Themas:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="36416-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="36416-106">Eine *VoIP-Richtlinie* ermöglicht eine Reihe von Anruffunktionen und ordnet einen oder mehrere PSTN-Verwendungsdaten Sätze an, um die Anruffeatures und Berechtigungen von Benutzern zu definieren, denen die Richtlinie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="36416-106">A *voice policy* enables a set of calling features and associates one or more PSTN usage records to define the calling features and permissions of users who are assigned the policy.</span></span>

<span data-ttu-id="36416-107">Der VoIP-Richtlinienbereich kann entweder ein *Standort* sein (der die Standardfeatures und-Berechtigungen für eine Netzwerk Website definiert) oder ein *Benutzer* (der die Features und Berechtigungen definiert, die für einzelne Benutzer oder Gruppen zugewiesen werden sollen).</span><span class="sxs-lookup"><span data-stu-id="36416-107">Voice policy scope can be either *Site* (which defines the default features and permissions for a network site) or *User* (which defines the features and permissions to be assigned on a per-user or group basis).</span></span> <span data-ttu-id="36416-108">Benutzer, denen keine VoIP-Richtlinie zugewiesen ist, werden automatisch der globalen Richtlinie zugewiesen, bei der es sich um die Standard VoIP-Richtlinie handelt, die mit dem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="36416-108">Users not assigned to a voice policy will automatically be assigned to the global policy, which is the default voice policy that is installed with the product.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="36416-109">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-voice-policies.md">VoIP-Richtlinien in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="36416-109">For details, see <A href="lync-server-2013-voice-policies.md">Voice policies in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="36416-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="36416-110">In This Section</span></span>

  - [<span data-ttu-id="36416-111">Erstellen einer VoIP-Richtlinie und Konfigurieren von PSTN-Verwendungsdatensätzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36416-111">Create a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="36416-112">Ändern einer VoIP-Richtlinie und Konfigurieren von PSTN-Verwendungsdatensätzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36416-112">Modify a voice policy and configure PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-modify-a-voice-policy-and-configure-pstn-usage-records.md)

  - [<span data-ttu-id="36416-113">Konfigurieren von Voicemail-Escape in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="36416-113">Configuring voice mail escape in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-mail-escape.md)

<span data-ttu-id="36416-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="36416-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

