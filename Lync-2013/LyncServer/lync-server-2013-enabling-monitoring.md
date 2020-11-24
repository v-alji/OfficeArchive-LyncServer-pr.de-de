---
title: 'Lync Server 2013: Aktivieren der Überwachung'
description: 'Lync Server 2013: Aktivieren der Überwachung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling monitoring
ms:assetid: 244df419-d0a8-4b1d-aedd-a92114172ab6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687994(v=OCS.15)
ms:contentKeyID: 49733584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d8995042bdc9b121dc5253940104bb167567ddcc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394726"
---
# <a name="enabling-monitoring-in-lync-server-2013"></a><span data-ttu-id="d31d6-103">Aktivieren der Überwachung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d31d6-103">Enabling monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d31d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d31d6-104">

<span> </span></span></span>

<span data-ttu-id="d31d6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="d31d6-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="d31d6-106">Obwohl die Unified Data Collection-Agents automatisch auf jedem Front-End-Server installiert und aktiviert werden, bedeutet dies nicht, dass Sie automatisch mit dem Sammeln von Überwachungsdaten beginnen, sobald Sie die Installation von Microsoft lync Server 2013 abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="d31d6-106">Although the unified data collection agents are automatically installed and activated on each Front End server, that does not mean that you will automatically begin to collect monitoring data the moment you finish installing Microsoft Lync Server 2013.</span></span> <span data-ttu-id="d31d6-107">Stattdessen müssen Sie zwei Schritte ausführen: Sie müssen Ihre Front-End-Server/Front-End-Pools mit einer Überwachungsdatenbank verknüpfen, und Sie müssen die Überwachung der Anrufdetailaufzeichnung (CDR) und/oder der Quality of Experience (QoE) auf globaler Ebene und/oder im Bereich der Website aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-107">Instead, you must do two things: you must associate your Front End servers/Front End pools with a monitoring database, and you must enable call detail recording (CDR) and/or Quality of Experience (QoE) monitoring at the global scope and/or the site scope.</span></span>

<span data-ttu-id="d31d6-108">Eine Schritt-für-Schritt-Anleitung zum Zuordnen von Front-End-Servern oder Front-End-Pools zu einer Überwachungsdatenbank finden Sie unter dem Thema [Zuordnen eines überwachungsspeichers zu einem Front-End-Pool in lync Server 2013](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) im Bereitstellungshandbuch.</span><span class="sxs-lookup"><span data-stu-id="d31d6-108">For step-by-step instructions on associating Front End servers or Front End pools with a monitoring database, see the topic [Associating a monitoring store with a Front End pool in Lync Server 2013](lync-server-2013-associating-a-monitoring-store-with-a-front-end-pool.md) in the Deployment guide.</span></span> <span data-ttu-id="d31d6-109">Nachdem diese Zuordnungen vorgenommen wurden und nachdem die neue lync Server-Topologie veröffentlicht wurde, können Sie weiterhin keine Überwachungsdaten sammeln.</span><span class="sxs-lookup"><span data-stu-id="d31d6-109">After these associations have been made, and after your new Lync Server topology has been published, you will still not be able to collect monitoring data.</span></span> <span data-ttu-id="d31d6-110">Das liegt daran, dass die Datensammlung für CDR und QoE standardmäßig deaktiviert ist, wenn Sie lync Server 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-110">That's because, by default, both CDR and QoE data collection is disabled when you install Lync Server 2013.</span></span>

<span data-ttu-id="d31d6-111">Um mit der Datensammlung beginnen zu können, müssen Sie die CDR-und/oder QoE-Überwachung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-111">In order to begin data collection you will need to enable CDR and/or QoE monitoring.</span></span> <span data-ttu-id="d31d6-112">(Beachten Sie, dass Sie nicht sowohl die CDR-als auch die QoE-Überwachung aktivieren müssen; Wenn Sie möchten, können Sie eine Art von Überwachung aktivieren, während der andere Typ deaktiviert bleibt.) Führen Sie den folgenden Befehl in der lync Server-Verwaltungsshell aus, um die CDR-Überwachung im globalen Bereich zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="d31d6-112">(Note that you do not have to enable both CDR and QoE monitoring; if you prefer, you can enable one type of monitoring while leaving the other type disabled.) To enable CDR monitoring at the global scope run the following command from within the Lync Server Management Shell:</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $True

<span data-ttu-id="d31d6-113">Alternativ können Sie die CDR-Überwachung in der lync Server 2013-Systemsteuerung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-113">Alternatively, you can enable CDR monitoring from within the Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="d31d6-114">Führen Sie in der lync Server-Systemsteuerung die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d31d6-114">From within the Lync Server Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="d31d6-115">Klicken Sie auf **Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-115">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="d31d6-116">Doppelklicken Sie auf der Registerkarte **Aufzeichnung von Kommunikationsdatensätzen** auf die Einstellung **Global**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-116">On the **Call Detail Recording** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="d31d6-117">Wählen Sie im Bereich **KDS-Einstellungen (Aufzeichnung von Kommunikationsdatensätzen) bearbeiten** die Option **Überwachung von KDS-Aufzeichnungen aktivieren** aus und klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-117">In the **Edit Call Detail Recording (CDR) Setting** pane, select **Enable monitoring of CDRs** and then click **Commit**.</span></span>

<span data-ttu-id="d31d6-118">Um die QoE-Überwachung im globalen Bereich zu aktivieren, führen Sie diesen Befehl in der lync Server-Verwaltungsshell aus:</span><span class="sxs-lookup"><span data-stu-id="d31d6-118">To enable QoE monitoring at the global scope, run this command from within the Lync Server Management Shell:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnableQoE $True

<span data-ttu-id="d31d6-119">Wenn Sie möchten, können Sie auch die QoE-Überwachung in der lync Server-Systemsteuerung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-119">If you prefer, you can also enable QoE monitoring from within the Lync Server Control Panel.</span></span> <span data-ttu-id="d31d6-120">Führen Sie in der Systemsteuerung die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d31d6-120">From within the Control Panel, complete the following procedure:</span></span>

1.  <span data-ttu-id="d31d6-121">Klicken Sie auf **Überwachung**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-121">Click **Monitoring**.</span></span>

2.  <span data-ttu-id="d31d6-122">Doppelklicken Sie auf der Registerkarte **Quality of Experience-Daten** auf die Einstellung **Global**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-122">On the **Quality of Experience Data** tab, double-click the **Global** setting.</span></span>

3.  <span data-ttu-id="d31d6-123">Wählen Sie im Bereich **QoE-Einstellungen (Quality of Experience) bearbeiten** die Option **Überwachung von QoE-Daten aktivieren** aus und klicken Sie dann auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d31d6-123">In the **Edit Quality of Experience (QoE) Setting** pane, select **Enable monitoring of QoE data** and then click **Commit**.</span></span>

<span data-ttu-id="d31d6-124">Wie bereits erwähnt, ermöglichen die obigen Beispiele die Überwachung auf globaler Ebene; Das bedeutet, dass Sie die CDR-und QoE-Überwachung in Ihrer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-124">As noted, the preceding examples enable monitoring at the global scope; that is, they enable CDR and QoE monitoring throughout your organization.</span></span> <span data-ttu-id="d31d6-125">Alternativ können Sie separate CDR-und QoE-Konfigurationseinstellungen im Website Bereich erstellen und dann die Überwachung für jede Website selektiv aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-125">Alternatively, you can create separate CDR and QoE configuration settings at the site scope, and then selectively enable or disable monitoring for each site.</span></span> <span data-ttu-id="d31d6-126">So können Sie beispielsweise die CDR-Überwachung für Ihre Redmond-Website aktivieren und dennoch die CDR-Überwachung für Ihre Dublin-Website deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d31d6-126">For example, you could enable CDR monitoring for your Redmond site, yet disable CDR monitoring for your Dublin site.</span></span> <span data-ttu-id="d31d6-127">Weitere Informationen zum Verwalten ihrer Überwachungs Konfigurationseinstellungen finden Sie im Bereitstellungshandbuch unter [Konfigurieren der Einstellungen für die Anrufdetailaufzeichnung und der Qualität der Benutzerfreundlichkeit in lync Server 2013](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d31d6-127">For more information on managing your monitoring configuration settings, see the Deployment guide topic [Configuring call detail recording and Quality of Experience settings in Lync Server 2013](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md).</span></span>

<span data-ttu-id="d31d6-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d31d6-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

