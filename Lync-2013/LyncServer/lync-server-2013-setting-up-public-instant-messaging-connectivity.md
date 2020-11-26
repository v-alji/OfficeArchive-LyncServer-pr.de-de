---
title: 'Lync Server 2013: Einrichten der öffentlichen Chatkonnektivität'
description: 'Lync Server 2013: Einrichten der öffentlichen Instant Messaging-Konnektivität'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up public instant messaging connectivity
ms:assetid: 816dea2a-96fa-4a36-b6c2-a9402675868b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205041(v=OCS.15)
ms:contentKeyID: 48184661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2f11c5e01de697b97395b6bc52815fadedff5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441704"
---
# <a name="setting-up-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="e3f03-103">Einrichten der öffentlichen Chatkonnektivität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e3f03-103">Setting up public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e3f03-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e3f03-104">

<span> </span></span></span>

<span data-ttu-id="e3f03-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="e3f03-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="e3f03-106">Wenn Ihre Organisation Öffentliche Instant Messaging-Verbindungen (im) mit AOL unterstützen möchte, können Sie den lync Server-Bereitstellungs-Assistenten nicht verwenden, um das Zertifikat anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e3f03-106">If your organization wants to support public instant messaging (IM) connectivity with AOL, you cannot use the Lync Server Deployment Wizard to request the certificate.</span></span> <span data-ttu-id="e3f03-107">Führen Sie stattdessen die Schritte im folgenden Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="e3f03-107">Instead, perform the steps in the following procedure.</span></span>

<div>

## <a name="setting-up-public-instant-messaging-connectivity"></a><span data-ttu-id="e3f03-108">Einrichten der öffentlichen Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="e3f03-108">Setting Up Public Instant Messaging Connectivity</span></span>

1.  <span data-ttu-id="e3f03-109">Öffnen Sie auf einem Front-End-Server den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="e3f03-109">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="e3f03-110">Erweitern Sie Edge-Pools, und klicken Sie dann mit der rechten Maustaste auf den Edgeserver oder den Edge-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="e3f03-110">Expand Edge pools, then right click your Edge server or Edge server pool.</span></span> <span data-ttu-id="e3f03-111">Wählen Sie Eigenschaften bearbeiten aus.</span><span class="sxs-lookup"><span data-stu-id="e3f03-111">Select Edit properties.</span></span>

2.  <span data-ttu-id="e3f03-112">Wählen Sie in Eigenschaften bearbeiten unter Allgemein die Option Föderation für diesen Edge-Pool aktivieren (Port 5061) aus.</span><span class="sxs-lookup"><span data-stu-id="e3f03-112">In Edit Properties under General, select Enable federation for this Edge pool (Port 5061).</span></span> <span data-ttu-id="e3f03-113">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="e3f03-113">Click OK.</span></span>

3.  <span data-ttu-id="e3f03-114">Klicken Sie auf Aktion, wählen Sie Topologie aus, und wählen Sie veröffentlichen aus.</span><span class="sxs-lookup"><span data-stu-id="e3f03-114">Click Action, select Topology, select Publish.</span></span> <span data-ttu-id="e3f03-115">Wenn Sie dazu aufgefordert werden, die Topologie zu veröffentlichen, klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="e3f03-115">When prompted on Publish the topology, click Next.</span></span> <span data-ttu-id="e3f03-116">Wenn der Veröffentlichungsvorgang abgeschlossen ist, klicken Sie auf Fertig stellen.</span><span class="sxs-lookup"><span data-stu-id="e3f03-116">When the Publish is finished, click Finish.</span></span>

4.  <span data-ttu-id="e3f03-117">Öffnen Sie auf dem Edgeserver den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="e3f03-117">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="e3f03-118">Klicken Sie auf lync Server System installieren oder aktualisieren und dann auf lync Server-Komponenten einrichten oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="e3f03-118">Click Install or Update Lync Server System, then click Setup or Remove Lync Server Components.</span></span> <span data-ttu-id="e3f03-119">Klicken Sie erneut auf ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3f03-119">Click Run Again.</span></span>

5.  <span data-ttu-id="e3f03-120">Klicken Sie bei der Installation von lync Server-Komponenten auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="e3f03-120">At Setup Lync Server components, click Next.</span></span> <span data-ttu-id="e3f03-121">Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e3f03-121">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="e3f03-122">Nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf Protokoll anzeigen, um die verfügbaren Protokolldateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e3f03-122">Once the deployment is done, click View Log to view available log files.</span></span> <span data-ttu-id="e3f03-123">Klicken Sie auf Fertig stellen, um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e3f03-123">Click Finish to complete the deployment.</span></span>

</div>

<div>

## <a name="to-create-a-certificate-request-for-the-external-interface-of-the-edge-server-to-support-public-im-connectivity-with-aol"></a><span data-ttu-id="e3f03-124">So erstellen Sie eine Zertifikatanforderung für die externe Schnittstelle des Edge-Servers zur Unterstützung öffentlicher Chat Verbindungen mit AOL</span><span class="sxs-lookup"><span data-stu-id="e3f03-124">To create a certificate request for the external interface of the Edge Server to support public IM connectivity with AOL</span></span>

1.  <span data-ttu-id="e3f03-125">Wenn die erforderliche Vorlage für die Zertifizierungsstelle verfügbar ist, verwenden Sie das folgende Windows PowerShell-Cmdlet auf dem Edgeserver, um das Zertifikat anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e3f03-125">When the required template is available to the CA, use the following Windows PowerShell cmdlet from at the Edge Server to request the certificate</span></span>
    
        Request-CsCertificate -New -Type AccessEdgeExternal  -Output C:\ <certfilename.txt or certfilename.csr>  -ClientEku $true -Template <template name>
    
    <span data-ttu-id="e3f03-126">Der Standardzertifikat Name der für lync Server verwendeten Vorlage ist Web Server.</span><span class="sxs-lookup"><span data-stu-id="e3f03-126">The default certificate name of the template used for Lync Server is Web Server.</span></span> <span data-ttu-id="e3f03-127">Geben Sie nur das an \<template name\> , wenn Sie eine Vorlage verwenden möchten, die von der Standardvorlage abweicht.</span><span class="sxs-lookup"><span data-stu-id="e3f03-127">Only specify the \<template name\> if you need to use a template that is different from the default template.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e3f03-128">Wenn Ihre Organisation öffentliche Chat Verbindungen mit AOL unterstützen möchte, müssen Sie anstelle des Zertifikat-Assistenten Windows PowerShell verwenden, um das Zertifikat anzufordern, das dem externen Edge für den Access Edge-Dienst zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3f03-128">If your organization wants to support public IM connectivity with AOL, you must use Windows PowerShell instead of the Certificate Wizard to request the certificate to be assigned to the external edge for the Access Edge service.</span></span> <span data-ttu-id="e3f03-129">Der Grund hierfür ist, dass die vom Zertifikat-Assistenten zum Anfordern eines Zertifikats verwendete Zertifikat Zertifizierungsstellen-Webservervorlage die Client-EKU-Konfiguration nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3f03-129">This is because the Certificate Authority (CA) Web Server template that the Certificate Wizard uses to request a certificate does not support client EKU configuration.</span></span> <span data-ttu-id="e3f03-130">Bevor Sie Windows PowerShell zum Erstellen des Zertifikats verwenden, muss der CA-Administrator eine neue Vorlage erstellen und bereitstellen, die die Client-EKU unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3f03-130">Before using Windows PowerShell to create the certificate, the CA administrator must create and deploy a new template that supports client EKU.</span></span>

    
    <span data-ttu-id="e3f03-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e3f03-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

