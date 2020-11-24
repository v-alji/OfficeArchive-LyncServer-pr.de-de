---
title: 'Lync Server 2013: Bearbeiten oder Konfigurieren einfacher URLs'
description: 'Lync Server 2013: Bearbeiten oder konfigurieren einfacher URLs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393783"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a><span data-ttu-id="7d659-103">Bearbeiten oder Konfigurieren einfacher URLs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d659-103">Edit or configure simple URLs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d659-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d659-104">

<span> </span></span></span>

<span data-ttu-id="7d659-105">_**Letztes Änderungsdatum des Themas:** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="7d659-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="7d659-106">Für dieses Verfahren ist keine Mitgliedschaft in einem lokalen Administrator oder einer privilegierten Domänengruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d659-106">This procedure does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="7d659-107">Melden Sie sich als Standardbenutzer an einem Computer an.</span><span class="sxs-lookup"><span data-stu-id="7d659-107">You should log on to a computer as a standard user.</span></span>

<span data-ttu-id="7d659-108">Lync Server 2013 verwendet einfache URLs, um interne und externe Anrufe an Dienste auf dem Front-End-Server oder an den Director weiterzuleiten, falls einer bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d659-108">Lync Server 2013 uses simple URLs to direct internal and external calls to services on the Front End Server or on the Director, if one has been deployed.</span></span> <span data-ttu-id="7d659-109">Weitere Informationen zu einfachen URLs finden Sie unter [Planen einfacher URLs in lync Server 2013](lync-server-2013-planning-for-simple-urls.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7d659-109">For more information about simple URLs, see [Planning for simple URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md) in the Planning documentation.</span></span> <span data-ttu-id="7d659-110">Sie können das Format für ihre einfachen URLs aus verschiedenen Optionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="7d659-110">You can select the format for your simple URLs from several options.</span></span> <span data-ttu-id="7d659-111">Ausführliche Informationen zu diesen Optionen finden Sie unter [DNS-Anforderungen für einfache URLs in lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7d659-111">For details about these options, see [DNS requirements for simple URLs in Lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) in the Planning documentation.</span></span>

<span data-ttu-id="7d659-112">Standardmäßig werden einfache URLs in Form von (beispielsweise der Einwahl einfachen URL) https://dialin konfiguriert:\<SIP Domain\></span><span class="sxs-lookup"><span data-stu-id="7d659-112">By default, simple URLs will be configured in the form of (for example, the dial-in simple URL): https://dialin.\<SIP Domain\></span></span>

<div>

## <a name="to-configure-simple-urls"></a><span data-ttu-id="7d659-113">So konfigurieren Sie einfache URLs</span><span class="sxs-lookup"><span data-stu-id="7d659-113">To configure simple URLs</span></span>

1.  <span data-ttu-id="7d659-114">Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den **lync Server** -Knoten, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="7d659-114">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="7d659-115">Wählen Sie im Bereich **Einfache URLs** entweder **Telefonzugriff-URLs:** (Dialin) oder **Besprechungs-URLs:** (Meet) aus und klicken Sie anschließend auf **URL bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="7d659-115">In the **Simple URLs** pane, select either **Phone access URLs:** (Dial-in) or **Meeting URLs:** (Meet) to edit, and then click **Edit URL**.</span></span>

3.  <span data-ttu-id="7d659-116">Aktualisieren Sie die URL auf den gewünschten Wert, und klicken Sie dann auf **OK** , um die bearbeitete URL zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7d659-116">Update the URL to the value you want, and then click **OK** to save the edited URL.</span></span> <span data-ttu-id="7d659-117">Das hier gezeigte Beispiel hat die Einwahl-URL in geändert https://pool01.contoso.net/dialin .</span><span class="sxs-lookup"><span data-stu-id="7d659-117">The example shown here has modified the Dial-in URL to https://pool01.contoso.net/dialin.</span></span>

4.  <span data-ttu-id="7d659-118">Bearbeiten Sie ggf. auch die Besprechungs-URL, indem Sie dieselben Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d659-118">Edit the Meet URL by using the same steps, if necessary.</span></span>

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a><span data-ttu-id="7d659-119">So definieren Sie die optionale einfache URL für den administrativen Zugriff</span><span class="sxs-lookup"><span data-stu-id="7d659-119">To define the optional Admin simple URL</span></span>

1.  <span data-ttu-id="7d659-120">Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den **lync Server** -Knoten, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="7d659-120">In Topology Builder, right-click the **Lync Server** node, and then click **Edit Properties**.</span></span>

2.  <span data-ttu-id="7d659-121">Geben Sie im Feld **Administratorzugriff-URL** die einfache URL ein, die Sie für den administrativen Zugriff auf die lync Server 2013-Systemsteuerung benötigen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d659-121">In the **Administrative access URL** box, enter the simple URL you want for administrative access to Lync Server 2013 Control Panel, and then click **OK**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="7d659-122">Es wird empfohlen, die einfachstmögliche URL als Verwaltungs-URL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7d659-122">We recommend using the simplest possible URL for the Admin URL.</span></span> <span data-ttu-id="7d659-123">Die einfachste Option ist <STRONG> https://admin .</STRONG> &lt; Domäne aus &gt; .</span><span class="sxs-lookup"><span data-stu-id="7d659-123">The simplest option is <STRONG>https://admin.</STRONG>&lt;domain&gt;.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="7d659-124">Wenn Sie eine einfache URL nach der ersten Bereitstellung ändern, müssen Sie beachten, welche Änderungen sich auf Ihre DNS-Datensätze und -Zertifikate für einfache URLs auswirken.</span><span class="sxs-lookup"><span data-stu-id="7d659-124">If you change a simple URL after initial deployment, you must be aware of what changes impact your Domain Name System (DNS) records and certificates for simple URLs.</span></span> <span data-ttu-id="7d659-125">Wenn die Änderung Auswirkungen auf die Basis einer einfachen URL hat, müssen Sie auch die DNS-Einträge und Zertifikate ändern.</span><span class="sxs-lookup"><span data-stu-id="7d659-125">If the change impacts the base of a simple URL, then you must change the DNS records and certificates as well.</span></span> <span data-ttu-id="7d659-126">Wenn Sie beispielsweise https://lync.contoso.com/Meet https://meet.contoso.com die Basis-URL von lync.contoso.com in Meet.contoso.com ändern, müssen Sie die DNS-Einträge und Zertifikate so ändern, dass Sie auf Meet.contoso.com verweisen.</span><span class="sxs-lookup"><span data-stu-id="7d659-126">For example, changing from https://lync.contoso.com/Meet to https://meet.contoso.com changes the base URL from lync.contoso.com to meet.contoso.com, so you would need to change the DNS records and certificates to refer to meet.contoso.com.</span></span> <span data-ttu-id="7d659-127">Wenn Sie die einfache URL von in geändert haben https://lync.contoso.com/Meet https://lync.contoso.com/Meetings , bleibt die Basis-URL von lync.contoso.com unverändert, sodass keine DNS-oder Zertifikat Änderungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7d659-127">If you changed the simple URL from https://lync.contoso.com/Meet to https://lync.contoso.com/Meetings, the base URL of lync.contoso.com stays the same, so no DNS or certificate changes are needed.</span></span> <span data-ttu-id="7d659-128">Wenn Sie jedoch einen einfachen URL-Namen ändern, müssen Sie das Cmdlet <STRONG>enable-CsComputer</STRONG> auf jedem Director und Front-End-Server ausführen, um die Änderung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7d659-128">Whenever you change a simple URL name, however, you must run the <STRONG>Enable-CsComputer</STRONG> cmdlet on each Director and Front End Server to register the change.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7d659-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d659-129">See Also</span></span>


[<span data-ttu-id="7d659-130">Planung für einfache URLs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d659-130">Planning for simple URLs in Lync Server 2013</span></span>](lync-server-2013-planning-for-simple-urls.md)  
  

<span data-ttu-id="7d659-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d659-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

