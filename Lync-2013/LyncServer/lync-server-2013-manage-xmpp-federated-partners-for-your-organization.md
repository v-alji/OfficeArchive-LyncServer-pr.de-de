---
title: 'Lync Server 2013: Verwalten von XMPP-Verbundpartnern für Ihre Organisation'
description: 'Lync Server 2013: Verwalten von XMPP-Verbundpartnern für Ihre Organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage XMPP federated partners for your organization
ms:assetid: 48681433-725d-457f-926b-f91d95bcf082
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552450(v=OCS.15)
ms:contentKeyID: 48679561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37d6fb4104c35ffc7db9649656f7786568a48b61
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426025"
---
# <a name="manage-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="ee297-103">Verwalten von XMPP-Verbundpartnern für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee297-103">Manage XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee297-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee297-104">

<span> </span></span></span>

<span data-ttu-id="ee297-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="ee297-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="ee297-106">Diese Dokumentation ist vorläufig und kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ee297-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="ee297-107">Leere Themen sind als Platzhalter enthalten.</span><span class="sxs-lookup"><span data-stu-id="ee297-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="ee297-108">Zum Verwalten der Unterstützung für Benutzer von XMPP-Verbunddomänen müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="ee297-108">To manage support for users of XMPP federated domains, you need to do the following:</span></span>

  - <span data-ttu-id="ee297-109">Konfigurieren Sie eine oder mehrere Richtlinien für den externen Zugriff, um Benutzer von XMPP-Verbunddomänen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ee297-109">Configure one or more external access policies to support users of XMPP federated domains.</span></span>

  - <span data-ttu-id="ee297-110">Konfigurieren der Richtlinie für die Zugriffs-Edge-Konfiguration zur Unterstützung der Föderation</span><span class="sxs-lookup"><span data-stu-id="ee297-110">Configure Access Edge Configuration policy to support federation.</span></span>

  - <span data-ttu-id="ee297-111">Erstellen Sie Definitionen von XMPP-Verbundpartnern.</span><span class="sxs-lookup"><span data-stu-id="ee297-111">Create XMPP Federated Partners definitions.</span></span>

  - <span data-ttu-id="ee297-112">Grundlegendes zu den für XMPP Federation verfügbaren Aushandlungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ee297-112">Understand negotiation settings available for XMPP federation.</span></span>

<span data-ttu-id="ee297-113">Führen Sie die Verfahren in diesem Abschnitt aus, um diese Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ee297-113">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ee297-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ee297-114">In This Section</span></span>

  - [<span data-ttu-id="ee297-115">Erstellen oder Bearbeiten einer XMPP-Verbundpartnerkonfiguration in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee297-115">Create or edit XMPP partner configuration in Lync Server 2013</span></span>](lync-server-2013-create-or-edit-xmpp-partner-configuration.md)

  - [<span data-ttu-id="ee297-116">Aushandlungseinstellungen für XMPP-Verbundpartner in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee297-116">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md)

  - [<span data-ttu-id="ee297-117">Beispiel für eine XMPP-Konfiguration in Lync Server 2013 – XMPP-Partnerverbund mit Google Talk</span><span class="sxs-lookup"><span data-stu-id="ee297-117">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)

<span data-ttu-id="ee297-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee297-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

