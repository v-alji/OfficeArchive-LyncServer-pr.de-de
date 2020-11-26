---
title: Hinzufügen eines Zweigstellenstandorts mit einer Lync Server 2013 Survivable Branch Appliance zu einer Topologie
description: Fügen Sie Ihrer Topologie die Niederlassungs Website der lync Server 2013 Survivable Branch Appliance hinzu.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add Lync Server 2013 Survivable Branch Appliance branch site to your topology
ms:assetid: d3142a37-4606-456d-8ea9-6cc0e51e55f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721896(v=OCS.15)
ms:contentKeyID: 49733830
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b50c03dd53c7637fcf0914db290b3e452b64b83
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439310"
---
# <a name="add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology"></a><span data-ttu-id="950b1-103">Hinzufügen eines Zweigstellenstandorts mit einer Lync Server 2013 Survivable Branch Appliance zu einer Topologie</span><span class="sxs-lookup"><span data-stu-id="950b1-103">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="950b1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="950b1-104">

<span> </span></span></span>

<span data-ttu-id="950b1-105">_**Letztes Änderungsdatum des Themas:** 2012-10-07_</span><span class="sxs-lookup"><span data-stu-id="950b1-105">_**Topic Last Modified:** 2012-10-07_</span></span>

<span data-ttu-id="950b1-106">Microsoft lync Server 2013 Survivor-Branch-Appliances (SBA) können einem Microsoft lync Server 2010-Front-End-Pool nicht als Sicherungs Registrierungsstelle zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="950b1-106">Microsoft Lync Server 2013 Survivable Branch Appliances (SBA) cannot be associated to a Microsoft Lync Server 2010 Front End pool as a backup Registrar.</span></span> <span data-ttu-id="950b1-107">Die SBA muss einem Microsoft lync Server 2013-Front-End-Pool zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="950b1-107">The SBA must be associated with a Microsoft Lync Server 2013 Front End pool.</span></span> <span data-ttu-id="950b1-108">Bei diesen Schritten wird von einem Microsoft lync Server 2013 SBA ausgegangen.</span><span class="sxs-lookup"><span data-stu-id="950b1-108">These steps assume a Microsoft Lync Server 2013 SBA.</span></span> <span data-ttu-id="950b1-109">Führen Sie dieses Verfahren am zentralen Standort aus.</span><span class="sxs-lookup"><span data-stu-id="950b1-109">Perform this procedure at the central site.</span></span>

<div>

## <a name="to-add-branch-sites-with-microsoft-lync-server-2013-sba-to-your-topology"></a><span data-ttu-id="950b1-110">So fügen Sie Ihrer Topologie Verzweigungs Websites mit Microsoft lync Server 2013 SBA hinzu</span><span class="sxs-lookup"><span data-stu-id="950b1-110">To add branch sites with Microsoft Lync Server 2013 SBA to your topology</span></span>

1.  <span data-ttu-id="950b1-111">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="950b1-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="950b1-112">Erweitern Sie in der Konsolenstruktur die zentrale Website, erweitern Sie **Verzweigungs Standorte**, und klicken Sie dann auf **neue Verzweigungs Website**.</span><span class="sxs-lookup"><span data-stu-id="950b1-112">In the console tree, expand the central site, expand **Branch Sites**, and then click **New Branch Site**.</span></span>

3.  <span data-ttu-id="950b1-113">Klicken Sie im Dialogfeld **neue Verzweigungs Website definieren** auf **Name**, und geben Sie dann einen Namen für die neue Verzweigungs Website ein.</span><span class="sxs-lookup"><span data-stu-id="950b1-113">In the **Define New Branch Site** dialog box, click **Name**, and then type a name for the new branch site.</span></span>

4.  <span data-ttu-id="950b1-114">Optional Klicken Sie auf **Beschreibung**, und geben Sie eine aussagekräftige Beschreibung für die Verzweigungs Website ein.</span><span class="sxs-lookup"><span data-stu-id="950b1-114">(Optional) Click **Description**, and then type a meaningful description for the branch site.</span></span>

5.  <span data-ttu-id="950b1-115">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="950b1-115">Click **Next**.</span></span>

6.  <span data-ttu-id="950b1-116">Optional Führen Sie im nächsten Dialogfeld **neue Verzweigungs Website definieren** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="950b1-116">(Optional) In the next **Define New Branch Site** dialog box, do any of the following:</span></span>
    
      - <span data-ttu-id="950b1-117">Klicken Sie auf **Stadt**, und geben Sie dann den Namen des Orts ein, in dem sich die Zweigstelle befindet.</span><span class="sxs-lookup"><span data-stu-id="950b1-117">Click **City**, and then type the name of the city in which the branch site is located.</span></span>
    
      - <span data-ttu-id="950b1-118">Klicken Sie auf **Bundesland/Region**, und geben Sie dann den Namen des Bundeslands oder der Region ein, in dem sich die Verzweigungs Website befindet.</span><span class="sxs-lookup"><span data-stu-id="950b1-118">Click **State/Region**, and then type the name of the state or region in which the branch site is located.</span></span>
    
      - <span data-ttu-id="950b1-119">Klicken Sie auf **Landesvorwahl**, und geben Sie dann den zweistelligen anrufcode für das Land/die Region ein, in dem sich die Zweigstelle befindet.</span><span class="sxs-lookup"><span data-stu-id="950b1-119">Click **Country Code**, and then type the two-digit calling code for the country/region in which the branch site is located.</span></span>

7.  <span data-ttu-id="950b1-120">Klicken Sie auf **weiter**, und führen Sie dann eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="950b1-120">Click **Next**, and then do one of the following:</span></span>
    
      - <span data-ttu-id="950b1-121">Wenn Sie eine Survivable Branch-Appliance oder einen Survivable Branch-Server an diesem Standort verwenden, stellen Sie sicher, dass das Kontrollkästchen neuen überlebensfähigen **Assistenten öffnen, wenn dieser Assistent geschlossen** wird, aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="950b1-121">If you are using a Survivable Branch Appliance or Survivable Branch Server at this site, be sure that the **Open the New Survivable Wizard when this wizard closes** check box is selected.</span></span>
    
      - <span data-ttu-id="950b1-122">Wenn Sie auf dieser Website keine überlebensfähige Branch Appliance oder einen Survivable Branch-Server verwenden, deaktivieren Sie das Kontrollkästchen **neuen Überlebenden Assistenten öffnen, wenn dieser Assistent geschlossen** wird.</span><span class="sxs-lookup"><span data-stu-id="950b1-122">If you are not using a Survivable Branch Appliance or Survivable Branch Server at this site, clear the **Open the New Survivable Wizard when this wizard closes** check box.</span></span>
    
      - <span data-ttu-id="950b1-123">Klicken Sie auf **Fertig stellen**, und folgen Sie dann den Anweisungen im Assistenten, der geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="950b1-123">Click **Finish**, and then follow the directions in the wizard that opens.</span></span> <span data-ttu-id="950b1-124">Informationen zu Assistenten Elementen finden Sie unter Definieren einer überlebensfähigen [Verzweigungs Einheit oder eines Servers in lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span><span class="sxs-lookup"><span data-stu-id="950b1-124">For information about wizard items, see [Define a Survivable Branch Appliance or Server in Lync Server 2013](lync-server-2013-define-a-survivable-branch-appliance-or-server.md).</span></span>

8.  <span data-ttu-id="950b1-125">Wiederholen Sie die vorherigen Schritte für jede Verzweigungs Website, die Sie zur Topologie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="950b1-125">Repeat the previous steps for each branch site that you want to add to the topology.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="950b1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="950b1-126">See Also</span></span>


[<span data-ttu-id="950b1-127">Definieren einer Survivable Branch Appliance oder eines Survivable Branch Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="950b1-127">Define a Survivable Branch Appliance or Server in Lync Server 2013</span></span>](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)  
[<span data-ttu-id="950b1-128">Definieren eines PSTN-Gateways für eine Zweigstelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="950b1-128">Define a PSTN gateway for a branch site in Lync Server 2013</span></span>](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)  
[<span data-ttu-id="950b1-129">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="950b1-129">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[<span data-ttu-id="950b1-130">Konfigurieren eines Trunks ohne medienumgehung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="950b1-130">Configure a trunk without media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-without-media-bypass.md)  
  

<span data-ttu-id="950b1-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="950b1-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

