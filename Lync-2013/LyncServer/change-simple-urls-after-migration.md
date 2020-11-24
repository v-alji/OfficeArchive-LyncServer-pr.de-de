---
title: Ändern einfacher URLs nach der Migration
description: Ändern Sie einfache URLs nach der Migration.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Change simple URLs after migration
ms:assetid: addb0dc8-8324-42b1-9a00-f4bd14fdf5c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721844(v=OCS.15)
ms:contentKeyID: 49733777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b2f9974106d28bcfdc64c2255337baf721a937e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394247"
---
# <a name="change-simple-urls-after-migration"></a><span data-ttu-id="b1bca-103">Ändern einfacher URLs nach der Migration</span><span class="sxs-lookup"><span data-stu-id="b1bca-103">Change simple URLs after migration</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1bca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1bca-104">

<span> </span></span></span>

<span data-ttu-id="b1bca-105">_**Letztes Änderungsdatum des Themas:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="b1bca-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="b1bca-106">Lync Server unterstützt drei einfache URLs:</span><span class="sxs-lookup"><span data-stu-id="b1bca-106">Lync Server supports three simple URLs:</span></span>

  - <span data-ttu-id="b1bca-107">**Meet** wird als Basis-URL für alle Konferenzen auf der Website oder Organisation verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1bca-107">**Meet** is used as the base URL for all conferences in the site or organization.</span></span> <span data-ttu-id="b1bca-108">Mit der einfachen URL für Besprechungen sind Links zu Besprechungen einfach zu verstehen und einfach zu kommunizieren und zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="b1bca-108">With the Meet simple URL, links to join meetings are easy to comprehend, and easy to communicate and distribute.</span></span>

  - <span data-ttu-id="b1bca-109">**Einwahl** ermöglicht den Zugriff auf die Webseite für Einwahlkonferenzeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b1bca-109">**Dial-in** enables access to the Dial-in Conferencing Settings webpage.</span></span> <span data-ttu-id="b1bca-110">Die Einwahl einfache URL ist in allen Besprechungseinladungen enthalten, damit Benutzer, die sich in die Besprechung einwählen möchten, auf die erforderlichen Telefonnummern und PIN-Informationen zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b1bca-110">The Dial-in simple URL is included in all meeting invitations so that users who want to dial in to the meeting can access the necessary phone number and PIN information.</span></span>

  - <span data-ttu-id="b1bca-111">Der **Administrator** ermöglicht den schnellen Zugriff auf die lync Server-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="b1bca-111">**Admin** enables quick access to the Lync Server Control Panel.</span></span> <span data-ttu-id="b1bca-112">Die einfache Admin-URL dient der internen Verwendung in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="b1bca-112">The Admin simple URL is internal to your organization.</span></span>

<span data-ttu-id="b1bca-113">Nach der Migration zu lync Server 2013 müssen Sie wissen, wie sich die Änderung auf Ihre DNS-Einträge und Zertifikate für einfache URLs auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b1bca-113">After migrating to Lync Server 2013, you must be aware of how the change impacts your DNS records and certificates for simple URLs.</span></span> <span data-ttu-id="b1bca-114">Wenn der Legacy-lync Server 2010-Director in der Topologie weiterhin verwendet wird, sind keine Änderungen an ihren einfachen URLs erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1bca-114">If the legacy Lync Server 2010 Director remains in use in the topology, no changes to your simple URLs are required.</span></span> <span data-ttu-id="b1bca-115">Wenn der lync Server 2010-Director nach der Migration aus der Topologie entfernt wird, müssen die einfachen URL-DNS-Einträge so aktualisiert werden, dass Sie auf einen der lync Server 2013-Pools verweisen.</span><span class="sxs-lookup"><span data-stu-id="b1bca-115">If the Lync Server 2010 Director is removed from the topology after migration, the simple URL DNS records must be updated to point to one of the Lync Server 2013 pools.</span></span> <span data-ttu-id="b1bca-116">Wenn Sie jedoch einen einfachen URL-Namen ändern, müssen Sie Enable-CsComputer auf jedem Director und Front-End-Server ausführen, um die Änderung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b1bca-116">Whenever you change a simple URL name, however, you must run Enable-CsComputer on each Director and Front End Server to register the change.</span></span>

<div>

## <a name="changing-simple-urls-after-migration"></a><span data-ttu-id="b1bca-117">Ändern einfacher URLs nach der Migration</span><span class="sxs-lookup"><span data-stu-id="b1bca-117">Changing Simple URLs after Migration</span></span>

<span data-ttu-id="b1bca-118">**So aktualisieren Sie die einfache URL für Besprechungen**</span><span class="sxs-lookup"><span data-stu-id="b1bca-118">**To update the Meet simple URL**</span></span>

1.  <span data-ttu-id="b1bca-119">Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den obersten Knoten **lync Server**, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b1bca-119">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="b1bca-120">Wählen Sie im linken Bereich und dann unter Besprechungs- **URLs** **einfache URLs** aus: Wählen Sie die URL erfüllen aus, und klicken Sie dann auf **URL bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b1bca-120">Select **Simple URLs** in the left pane, then below **Meeting URLs:** select the Meet URL and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="b1bca-121">Aktualisieren Sie die URL auf den gewünschten Wert, und klicken Sie dann auf **OK** , um die bearbeitete URL zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b1bca-121">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span>

<span data-ttu-id="b1bca-122">**So aktualisieren Sie die einfache Administrator-URL**</span><span class="sxs-lookup"><span data-stu-id="b1bca-122">**To update the Admin simple URL**</span></span>

1.  <span data-ttu-id="b1bca-123">Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den obersten Knoten **lync Server**, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b1bca-123">In Topology Builder, right-click the top node **Lync Server**, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="b1bca-124">Wählen Sie im linken Bereich **einfache URLs** aus, und geben Sie dann unter **Administratorzugriff-URL** die einfache URL ein, die Sie für den administrativen Zugriff auf die lync Server 2013-Systemsteuerung benötigen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1bca-124">Select **Simple URLs** in the left pane, then below **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="b1bca-125">Es wird empfohlen, die einfachstmögliche URL als Verwaltungs-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1bca-125">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="b1bca-126">Die einfachste Option ist <STRONG> https://admin .</STRONG> &lt; Domäne aus &gt; .</span><span class="sxs-lookup"><span data-stu-id="b1bca-126">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b1bca-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1bca-127">See Also</span></span>


[<span data-ttu-id="b1bca-128">Planung für einfache URLs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1bca-128">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="b1bca-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1bca-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

