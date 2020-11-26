---
title: 'Lync Server 2013: Definieren und Konfigurieren einer Topologie im Topologie-Generator'
description: 'Lync Server 2013: definieren und Konfigurieren einer Topologie im Topologie-Generator'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define and configure a topology in Topology Builder
ms:assetid: 99231ff5-1c21-432b-ad65-8675fcd484f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398788(v=OCS.15)
ms:contentKeyID: 48184953
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 83a1f29ec78cf7cfd3856d3f1aa87a22dc0bbe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431057"
---
# <a name="define-and-configure-a-topology-in-topology-builder-for-lync-server-2013"></a><span data-ttu-id="84311-103">Definieren und Konfigurieren einer Topologie für Lync Server 2013 im Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="84311-103">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="84311-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="84311-104">

<span> </span></span></span>

<span data-ttu-id="84311-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="84311-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="84311-106">Das Ausführen des Topologie-Generators zum Definieren einer neuen Topologie oder zum Ändern einer vorhandenen Topologie erfordert keine Mitgliedschaft in einem lokalen Administrator oder einer privilegierten Domänengruppe.</span><span class="sxs-lookup"><span data-stu-id="84311-106">Running Topology Builder to define a new topology or to modify an existing topology does not require membership in a local administrator or privileged domain group.</span></span> <span data-ttu-id="84311-107">Der Topologie-Generator führt Sie durch die Schritte, die erforderlich sind, um Ihre Topologie für einen Enterprise Edition-Front-End-Pool oder eine Standard Edition basierend auf Ihren Konfigurationsanforderungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="84311-107">Topology Builder guides you through the steps necessary to define your topology for an Enterprise Edition Front End pool or a Standard Edition, based on your configuration requirements.</span></span>

<span data-ttu-id="84311-108">Sie müssen den Topologie-Generator verwenden, um die Topologie abzuschließen und zu veröffentlichen, bevor Sie lync Server 2013 auf Servern installieren können.</span><span class="sxs-lookup"><span data-stu-id="84311-108">You must use Topology Builder to complete and publish the topology before you can install Lync Server 2013 on servers.</span></span> <span data-ttu-id="84311-109">Das folgende Verfahren enthält die erforderlichen Schritte zum Definieren einer neuen Topologie.</span><span class="sxs-lookup"><span data-stu-id="84311-109">The following procedure includes the steps required to define a new topology.</span></span>

<div>

## <a name="to-define-a-topology"></a><span data-ttu-id="84311-110">So definieren Sie eine Topologie</span><span class="sxs-lookup"><span data-stu-id="84311-110">To define a topology</span></span>

1.  <span data-ttu-id="84311-111">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="84311-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="84311-112">Wählen Sie im Topologie-Generator die Option **neue Topologie** aus.</span><span class="sxs-lookup"><span data-stu-id="84311-112">In Topology Builder, select **New Topology**.</span></span> <span data-ttu-id="84311-113">Sie werden aufgefordert, einen Speicherort und einen Dateinamen zum Speichern der Topologie einzugeben.</span><span class="sxs-lookup"><span data-stu-id="84311-113">You are prompted for a location and file name for saving the topology.</span></span> <span data-ttu-id="84311-114">Geben Sie der topologiedatei einen aussagekräftigen Namen, und übernehmen Sie die Standarderweiterung tbxml.</span><span class="sxs-lookup"><span data-stu-id="84311-114">Give the topology file a meaningful name and accept the default extension of .tbxml.</span></span> <span data-ttu-id="84311-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="84311-115">Click **OK**.</span></span>

3.  <span data-ttu-id="84311-116">Navigieren Sie zu dem Speicherort, an dem Sie die neue Topologie-XML-Datei speichern möchten, geben Sie einen Namen für die Datei ein, und klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="84311-116">Navigate to the location where you want to save the new topology XML file, enter a name for the file, and then click **Save**.</span></span>

4.  <span data-ttu-id="84311-117">Geben Sie auf der Seite **primäre Domäne definieren** den Namen der primären SIP-Domäne für Ihre Organisation ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="84311-117">On the **Define the primary domain** page, enter the name of the primary SIP domain for your organization, and then click **Next**.</span></span>

5.  <span data-ttu-id="84311-118">Geben Sie auf der Seite **zusätzliche unterstützte Domänen angeben** die Namen zusätzlicher Domänen ein, sofern vorhanden, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="84311-118">On the **Specify additional supported domains** page, enter the names of additional domains, if any, and then click **Next**.</span></span>

6.  <span data-ttu-id="84311-119">Geben Sie auf der Seite **erste Website definieren** einen Namen und eine Beschreibung für die erste Website ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="84311-119">On the **Define the first site** page, enter a name and a description for the first site, and then click **Next**.</span></span>

7.  <span data-ttu-id="84311-120">Geben Sie auf der Seite **Website Details angeben** die Standortinformationen für die Website ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="84311-120">On the **Specify site details** page, enter the location information for the site, and then click **Next**.</span></span>

8.  <span data-ttu-id="84311-121">Vergewissern Sie sich, dass auf der Seite **neue Topologie erfolgreich definiert** ist, das Kontrollkästchen **neuen Front-End-Assistenten öffnen, wenn dieser Assistent geschlossen** wird, aktiviert ist, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="84311-121">On the **New topology was successfully defined** page, make sure the **Open the New Front End Wizard when this wizard closes** check box is selected, and then click **Finish**.</span></span>

<span data-ttu-id="84311-122">Nachdem Sie die Topologie definiert und gespeichert haben, verwenden Sie den neuen Front-End-Assistenten, um einen Front-End-Pool oder Standard Edition-Server für Ihre Website zu definieren.</span><span class="sxs-lookup"><span data-stu-id="84311-122">After you’ve defined and saved the topology, use the New Front End Wizard to define a Front End pool or Standard Edition server for your site.</span></span> <span data-ttu-id="84311-123">Ausführliche Informationen finden Sie unter [definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers in lync Server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md).</span><span class="sxs-lookup"><span data-stu-id="84311-123">For details, see [Define and configure a Front End pool or Standard Edition server in Lync Server 2013](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md).</span></span>

<span data-ttu-id="84311-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="84311-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

