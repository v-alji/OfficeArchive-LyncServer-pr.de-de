---
title: Ändern von VoIP-Routen zur Verwendung des neuen lync Server 2013-Vermittlungsservers
description: Ändern Sie die VoIP-Routen, um den neuen lync Server 2013-Vermittlungsserver zu verwenden.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change voice routes to use the new Lync Server 2013 Mediation Server
ms:assetid: acd487b3-377c-46bf-9f71-fe6152002664
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205162(v=OCS.15)
ms:contentKeyID: 48185069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef58ba61512b5de31a74b79e554dbb3f94b67d99
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394250"
---
# <a name="change-voice-routes-to-use-the-new-lync-server-2013-mediation-server"></a><span data-ttu-id="ee6fd-103">Ändern von VoIP-Routen zur Verwendung des neuen lync Server 2013-Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="ee6fd-103">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee6fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee6fd-104">

<span> </span></span></span>

<span data-ttu-id="ee6fd-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="ee6fd-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="ee6fd-106">Bei diesem Verfahren werden die VoIP-Routen so geändert, dass der lync Server 2013-Vermittlungsserver anstelle des Legacy Office Communications Server 2007 R2-Vermittlungsservers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-106">This procedure changes the voice routes to use the Lync Server 2013 Mediation Server, instead of the legacy Office Communications Server 2007 R2 Mediation Server.</span></span>

<div>

## <a name="to-change-the-voice-routes-to-use-the-new-mediation-server"></a><span data-ttu-id="ee6fd-107">So ändern Sie die VoIP-Routen zur Verwendung des neuen Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="ee6fd-107">To change the voice routes to use the new Mediation Server</span></span>

1.  <span data-ttu-id="ee6fd-108">Systemsteuerung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ee6fd-108">Lync Server 2013 Control Panel</span></span>

2.  <span data-ttu-id="ee6fd-109">Wählen Sie im linken Bereich die Option **VoIP-Routing** und dann **Route** aus.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-109">In the left pane, select **Voice Routing** and then **Route**.</span></span>

3.  <span data-ttu-id="ee6fd-110">Klicken Sie auf **neu** , um eine neue VoIP-Route zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-110">Click **New** to create a New Voice Route.</span></span>

4.  <span data-ttu-id="ee6fd-111">Füllen Sie die folgenden Felder aus:</span><span class="sxs-lookup"><span data-stu-id="ee6fd-111">Fill in the following fields:</span></span>
    
      - <span data-ttu-id="ee6fd-112">**Name**: Geben Sie einen aussagekräftigen Namen für die VoIP-Route ein.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-112">**Name**: Type a descriptive name of the voice route.</span></span> <span data-ttu-id="ee6fd-113">Für dieses Dokument werden wir **W15PSTNRoute** verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-113">For this document we will use **W15PSTNRoute**.</span></span>
    
      - <span data-ttu-id="ee6fd-114">**Beschreibung**: Geben Sie eine kurze Beschreibung der VoIP-Route ein.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-114">**Description**: Type a short description of the voice route.</span></span>

5.  <span data-ttu-id="ee6fd-115">Überspringen Sie alle verbleibenden Abschnitte, bis Sie **zugeordnete Gateways** erreichen.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-115">Skip all remaining sections until you reach **Associated gateways**.</span></span> <span data-ttu-id="ee6fd-116">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-116">Click **Add**.</span></span> <span data-ttu-id="ee6fd-117">Wählen Sie das neue Standardgateway aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-117">Select the new default gateway and click **OK**.</span></span>

6.  <span data-ttu-id="ee6fd-118">Klicken Sie unter **zugeordnete PSTN-Nutzungen** auf **auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-118">Under **Associated PSTN Usages**, click **Select**.</span></span>

7.  <span data-ttu-id="ee6fd-119">Wählen Sie auf der Seite **PSTN-Verwendungsdaten Satz auswählen** einen Datensatznamen aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-119">From the **Select PSTN Usage Record** page, select a record name and then click **OK**.</span></span>

8.  <span data-ttu-id="ee6fd-120">Klicken Sie auf der Seite **neue VoIP-Route** auf **OK** , um die **VoIP-Route** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-120">From the **New Voice Route** page, click **OK** to create the **Voice Route**.</span></span>

9.  <span data-ttu-id="ee6fd-121">Wählen Sie auf der Seite **VoIP-Routing** die Option **Route** aus.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-121">From the **Voice Routing** page, select **Route**.</span></span>

10. <span data-ttu-id="ee6fd-122">Verschieben Sie die neu erstellte Route an den Anfang der Liste, und wählen Sie dann **Commit** aus.</span><span class="sxs-lookup"><span data-stu-id="ee6fd-122">Move the newly created route to the top of the list and then select **Commit**.</span></span>

<span data-ttu-id="ee6fd-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee6fd-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

