---
title: Herunterladen der Topologie aus einer vorhandenen Bereitstellung
description: Topologie aus vorhandener Bereitstellung herunterladen.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Download topology from existing deployment
ms:assetid: e39065a2-d4b0-4f27-8c49-f56be78fa55b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721913(v=OCS.15)
ms:contentKeyID: 49733847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c22d746f8faf3fdf14a44e751eeb3c88bf3eef4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394387"
---
# <a name="download-topology-from-existing-deployment"></a><span data-ttu-id="05602-103">Herunterladen der Topologie aus einer vorhandenen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="05602-103">Download topology from existing deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05602-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05602-104">

<span> </span></span></span>

<span data-ttu-id="05602-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="05602-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="05602-106">Beim Erstellen eines lync Server 2013-Pools verwenden Sie den zentralen Verwaltungsspeicher, der lync Server 2010 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="05602-106">When creating a Lync Server 2013 pool, you will use the Central Management Store that is associated with Lync Server 2010.</span></span> <span data-ttu-id="05602-107">Wenn Sie den Topologie-Generator bei der ersten Verwendung und nachfolgenden Bearbeitungssitzungen starten, werden Sie aufgefordert, den Speicherort anzugeben, an dem der Topologie-Generator das aktuelle Konfigurationsdokument laden soll.</span><span class="sxs-lookup"><span data-stu-id="05602-107">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="05602-108">Da Sie bereits eine lync Server 2010-Topologie definiert haben und den zentralen Verwaltungsspeicher eingerichtet haben, sollten Sie eine Topologie aus einer vorhandenen Bereitstellung herunterladen.</span><span class="sxs-lookup"><span data-stu-id="05602-108">Because you already have a Lync Server 2010 topology defined and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="05602-109">Der Topologie-Generator liest die Datenbank und ruft die aktuelle Definition ab.</span><span class="sxs-lookup"><span data-stu-id="05602-109">Topology Builder will read the database and retrieve the current definition.</span></span>

<span data-ttu-id="05602-110">**So laden Sie eine Topologie aus einer vorhandenen Bereitstellung herunter**</span><span class="sxs-lookup"><span data-stu-id="05602-110">**To download a topology from an existing deployment**</span></span>

1.  <span data-ttu-id="05602-111">Öffnen Sie den **lync Server-Bereitstellungs-Assistenten**.</span><span class="sxs-lookup"><span data-stu-id="05602-111">Open the **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="05602-112">Klicken Sie auf der Seite **lync Server 2013 – Deployment-Assistent** auf **Verwaltungs Tools installieren**.</span><span class="sxs-lookup"><span data-stu-id="05602-112">From the **Lync Server 2013 – Deployment Wizard** page, click **Install Administrative Tools**.</span></span>

3.  <span data-ttu-id="05602-113">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013** , und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="05602-113">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013** , and then click **Lync Server Topology Builder**.</span></span>

4.  <span data-ttu-id="05602-114">Wählen Sie **Topologie aus vorhandener Bereitstellung herunterladen aus**.</span><span class="sxs-lookup"><span data-stu-id="05602-114">Select **Download Topology from existing deployment**.</span></span>
    
    <span data-ttu-id="05602-115">![Einstellungen des Bereitstellungs-Assistenten für Topologie-Generator](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Einstellungen des Bereitstellungs-Assistenten für Topologie-Generator")</span><span class="sxs-lookup"><span data-stu-id="05602-115">![Deployment Wizard Topology Builder settings](images/JJ721913.d5b39fd9-3c13-422e-a06c-25d2568fe781(OCS.15).jpg "Deployment Wizard Topology Builder settings")</span></span>

5.  <span data-ttu-id="05602-116">Wählen Sie einen Dateinamen aus, und speichern Sie die Topologie mit dem standardmäßigen tbxml-Dateityp.</span><span class="sxs-lookup"><span data-stu-id="05602-116">Choose a file name and save the topology with the default .tbxml file type.</span></span>

6.  <span data-ttu-id="05602-117">Erweitern Sie den lync Server-Knoten, wie hier gezeigt, um die verschiedenen Server Rollen in der Bereitstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="05602-117">Expand the Lync Server node, as shown, to reveal the various server roles in the deployment.</span></span>
    
    <span data-ttu-id="05602-118">![Allgemeine Eigenschaften des Topology Builder-Servers](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Allgemeine Eigenschaften des Topology Builder-Servers")</span><span class="sxs-lookup"><span data-stu-id="05602-118">![Topology Builder server role general properties](images/JJ721913.af99ead3-676b-47fd-8369-5a5f9717383f(OCS.15).jpg "Topology Builder server role general properties")</span></span>

<span data-ttu-id="05602-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05602-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

