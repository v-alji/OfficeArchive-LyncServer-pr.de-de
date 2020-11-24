---
title: Konfigurieren der SCOM-Überwachung
description: Konfigurieren der SCOM-Überwachung
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure SCOM monitoring
ms:assetid: 4003d225-2a33-448c-abd9-571750661140
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688033(v=OCS.15)
ms:contentKeyID: 49733624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c93e10c705a1a1e08972d7534e00a33c472d23a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394107"
---
# <a name="configure-scom-monitoring"></a><span data-ttu-id="6ac1f-103">Konfigurieren der SCOM-Überwachung</span><span class="sxs-lookup"><span data-stu-id="6ac1f-103">Configure SCOM monitoring</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ac1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ac1f-104">

<span> </span></span></span>

<span data-ttu-id="6ac1f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="6ac1f-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="6ac1f-106">Nach der Migration zu Microsoft lync Server 2013 müssen Sie einige Aufgaben ausführen, um lync Server 2013 für die Zusammenarbeit mit System Center Operations Manager zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-106">After migrating to Microsoft Lync Server 2013, you must complete a few tasks to configure Lync Server 2013 to work with System Center Operations Manager.</span></span>

  - <span data-ttu-id="6ac1f-107">Wenden Sie lync Server 2010-Updates auf einen Server an, der zum Verwalten der zentralen Ermittlungslogik gewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-107">Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.</span></span>

  - <span data-ttu-id="6ac1f-108">Aktualisieren Sie den Registrierungsschlüssel des zentralen Discovery Candidate-Servers.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-108">Update the central discovery candidate server registry key.</span></span>

  - <span data-ttu-id="6ac1f-109">Konfigurieren Sie Ihren primären System Center Operations Manager-Verwaltungsserver so, dass er den Kandidaten für die zentrale Ermittlung außer Kraft setzt.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-109">Configure your primary System Center Operations Manager management server to override the candidate central discovery node.</span></span>

<span data-ttu-id="6ac1f-110">Nachfolgend finden Sie Anweisungen zur Durchführung der einzelnen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-110">Instructions for carrying out each of these tasks are provided below.</span></span>

<span data-ttu-id="6ac1f-111">**Wenden Sie lync Server 2010-Updates auf einen Server an, der zum Verwalten der zentralen Ermittlungslogik gewählt wurde.**</span><span class="sxs-lookup"><span data-stu-id="6ac1f-111">**Apply Lync Server 2010 updates to a server elected to manage the central discovery logic.**</span></span>

1.  <span data-ttu-id="6ac1f-112">Wählen Sie einen Server aus, auf dem die System Center Operations Manager-Agentdateien installiert sind und als Knoten für die Kandidaten Ermittlung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-112">Elect a server that has the System Center Operations Manager agent files installed and is configured as a candidate discovery node.</span></span>

2.  <span data-ttu-id="6ac1f-113">Wenden Sie lync Server 2010-Updates auf diesen Server an.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-113">Apply Lync Server 2010 updates to this server.</span></span> <span data-ttu-id="6ac1f-114">Lesen Sie das Thema [Anwenden von lync Server 2010-Updates](apply-lync-server-2010-updates.md).</span><span class="sxs-lookup"><span data-stu-id="6ac1f-114">See the topic [Apply Lync Server 2010 updates](apply-lync-server-2010-updates.md).</span></span>

<span data-ttu-id="6ac1f-115">**Aktualisieren Sie den Registrierungsschlüssel des zentralen Discovery Candidate-Servers.**</span><span class="sxs-lookup"><span data-stu-id="6ac1f-115">**Update the central discovery candidate server registry key.**</span></span>

1.  <span data-ttu-id="6ac1f-116">Öffnen Sie auf dem Server, der zum Verwalten der zentralen Ermittlungslogik gewählt wurde, ein Windows PowerShell-Befehlsfenster.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-116">On the server elected to manage the central discovery logic, open a Windows PowerShell command window.</span></span>

2.  <span data-ttu-id="6ac1f-117">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="6ac1f-117">At the command line, type the following:</span></span>
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health"
       ```
    
       ```PowerShell
        New-Item -Path "HKLM:\Software\Microsoft\Real-Time Communications\Health\CentralDiscoveryCandidate"
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="6ac1f-118">Wenn Sie die Registrierung bearbeiten, tritt möglicherweise ein Fehler auf, dass der Befehl fehlgeschlagen ist, wenn der Registrierungsschlüssel bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-118">Whenever you edit the registry, you may experience an error that the command failed if the registry key already exists.</span></span> <span data-ttu-id="6ac1f-119">Wenn Sie dies erleben, können Sie den Fehler bedenkenlos ignorieren.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-119">If you experience this, you can safely ignore the error.</span></span>

    
    </div>

<span data-ttu-id="6ac1f-120">**Konfigurieren Sie Ihren primären System Center Operations Manager-Verwaltungsserver so, dass er den Kandidaten für den Central Discovery Watcher-Knoten außer Kraft setzt.**</span><span class="sxs-lookup"><span data-stu-id="6ac1f-120">**Configure your primary System Center Operations Manager management server to override the candidate central discovery watcher node.**</span></span>

1.  <span data-ttu-id="6ac1f-121">Erweitern Sie auf einem Computer, auf dem die System Center Operations Manager-Konsole installiert wurde, **Management Pack-Objekte** , und wählen Sie dann **Objektermittlungen** aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-121">On a computer where the System Center Operations Manager console has been installed, expand **Management Pack Objects** and then select **Object Discoveries**.</span></span>

2.  <span data-ttu-id="6ac1f-122">Klicken Sie auf **Bereich ändern...**</span><span class="sxs-lookup"><span data-stu-id="6ac1f-122">Click **Change Scope...**</span></span>

3.  <span data-ttu-id="6ac1f-123">Wählen Sie auf der Seite **Objekte des Bereichs Management Packs** die Option **ls Discovery Candidate** aus.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-123">From the **Scope Management Pack Objects** page, select **LS Discovery Candidate**.</span></span>

4.  <span data-ttu-id="6ac1f-124">Überschreiben Sie den Wert für den **effektiven ls-Ermittlungs Kandidaten** auf den Namen des Kandidaten Servers, der im vorherigen Verfahren gewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-124">Override the **LS Discovery Candidate Effective Value** to the name of the candidate server elected in the earlier procedure.</span></span>

<span data-ttu-id="6ac1f-125">Um Ihre Änderungen abzuschließen, starten Sie den Integritätsdienst auf dem System Center Operations Manager-Stamm Verwaltungs Server erneut.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-125">Lastly, to finalize your changes, restart the health service on the System Center Operations Manager Root Management Server.</span></span>

<span data-ttu-id="6ac1f-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ac1f-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

