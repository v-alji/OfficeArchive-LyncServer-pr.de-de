---
title: Entfernen von BackCompatSite
description: Entfernen Sie BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440307"
---
# <a name="remove-backcompatsite"></a><span data-ttu-id="37641-103">Entfernen von BackCompatSite</span><span class="sxs-lookup"><span data-stu-id="37641-103">Remove BackCompatSite</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37641-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37641-104">

<span> </span></span></span>

<span data-ttu-id="37641-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="37641-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="37641-106">Nachdem alle Pools deaktiviert und alle Edgeserver deinstalliert wurden, führen Sie den Assistenten zum Zusammenführen des Topologie-Generators aus, um den **BackCompatSite** zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="37641-106">After all pools are deactivated and all Edge Servers have been uninstalled, run the Topology Builder Merge wizard to remove the **BackCompatSite**.</span></span>

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a><span data-ttu-id="37641-107">So entfernen Sie die backcompat-Website aus dem Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="37641-107">To remove BackCompat site from Topology Builder</span></span>

1.  <span data-ttu-id="37641-108">Öffnen Sie eine vorhandene Bereitstellung vom Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="37641-108">Open an existing deployment from Topology Builder.</span></span>

2.  <span data-ttu-id="37641-109">Klicken Sie im Menü **Aktion** auf **2007 R2-Topologie zusammenführen**.</span><span class="sxs-lookup"><span data-stu-id="37641-109">In the **Action** menu, click **Merge 2007 R2 Topology**.</span></span>

3.  <span data-ttu-id="37641-110">Klicken Sie auf **Weiter**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="37641-110">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="37641-111">Stellen Sie auf der Seite **Legacy Edge angeben** sicher, dass die Liste der Edgeserver leer ist.</span><span class="sxs-lookup"><span data-stu-id="37641-111">On the **Specify Legacy Edge** page, ensure that list of Edge Servers is empty.</span></span> <span data-ttu-id="37641-112">Wenn die Liste nicht leer ist, verwenden Sie die Schaltfläche **Entfernen** , um alle Legacy-Edgeserver zu entfernen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="37641-112">If the list is not empty, use the **Remove** button to remove all the legacy Edge Servers, and then click **Next**.</span></span>
    
    <span data-ttu-id="37641-113">![Assistenten für die Zusammenführungs Topologie, Seite "Edge-Setup" angeben](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Assistenten für die Zusammenführungs Topologie, Seite "Edge-Setup" angeben")</span><span class="sxs-lookup"><span data-stu-id="37641-113">![Merge Topology Wizard, Specify Edge Setup page](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Merge Topology Wizard, Specify Edge Setup page")</span></span>  

5.  <span data-ttu-id="37641-114">Klicken Sie auf der Seite **interne SIP-Porteinstellung angeben** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="37641-114">On the **Specify Internal SIP port setting** page, click **Next**.</span></span>

6.  <span data-ttu-id="37641-115">Klicken Sie auf der Seite **Zusammenfassung** auf **weiter** , um mit dem Zusammenführen der Topologien zu beginnen, um die Legacy Website zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="37641-115">On the **Summary** page, click **Next** to begin merging the topologies to remove the legacy site.</span></span>

7.  <span data-ttu-id="37641-116">Überprüfen Sie in der Spalte **Status** , ob der Wert **erfolgreich** ist, und klicken Sie dann auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="37641-116">In the **Status** column, verify that the value is **Success** and then click **Finish** to close the wizard.</span></span>

8.  <span data-ttu-id="37641-117">Erweitern Sie im linken Bereich des Topologie-Generators die BackCompatSite, und stellen Sie sicher, dass keine Server aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="37641-117">In the left pane of Topology Builder, expand the BackCompatSite and ensure no servers are listed.</span></span>

9.  <span data-ttu-id="37641-118">Klicken Sie mit der rechten Maustaste auf das **BackCompatSite**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="37641-118">Right-click the **BackCompatSite**, and then click **Delete**.</span></span>

10. <span data-ttu-id="37641-119">Wählen Sie im **Topologie-Generator** den **lync-Server** mit dem höchsten Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="37641-119">In **Topology Builder**, select the top-most node **Lync Server**.</span></span>

11. <span data-ttu-id="37641-120">Wählen Sie im Menü **Aktion** die Option **Topologie veröffentlichen** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="37641-120">From the **Action** menu, select **Publish Topology** and then click **Next**.</span></span>

12. <span data-ttu-id="37641-121">Klicken Sie nach Abschluss des **Veröffentlichungs-Assistenten** auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="37641-121">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

<span data-ttu-id="37641-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37641-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

