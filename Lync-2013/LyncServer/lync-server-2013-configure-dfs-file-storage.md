---
title: 'Lync Server 2013: Konfigurieren des Dateispeichers'
description: 'Lync Server 2013: Konfigurieren des DFS-Dateispeichers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DFS file storage
ms:assetid: a985be20-5a00-4f38-b45b-83dc82de3827
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205150(v=OCS.15)
ms:contentKeyID: 48185037
ms.date: 05/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d70ae93db188ec51d04dd33d6c3cb5659db5a2c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395150"
---
# <a name="configure-dfs-file-storage-for-lync-server-2013"></a><span data-ttu-id="04665-103">Konfigurieren des Dateispeichers für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="04665-103">Configure DFS file storage for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="04665-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="04665-104">

<span> </span></span></span>

<span data-ttu-id="04665-105">_**Letztes Änderungsdatum des Themas:** 2016-05-23_</span><span class="sxs-lookup"><span data-stu-id="04665-105">_**Topic Last Modified:** 2016-05-23_</span></span>

<span data-ttu-id="04665-106">Lync Server 2013 unterstützt die Verwendung von Dateifreigaben in einem verteilten Datei System (DFS).</span><span class="sxs-lookup"><span data-stu-id="04665-106">Lync Server 2013 supports using file shares on a Distributed File System (DFS).</span></span> <span data-ttu-id="04665-107">Ausführliche Informationen zu DFS für Windows Server 2008 finden Sie in der schrittweisen Anleitung zu DFS für Windows Server 2008 unter [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) . Um ein DFS zu verwenden, benötigt lync Server 2013 Folgendes:</span><span class="sxs-lookup"><span data-stu-id="04665-107">For details about DFS for Windows Server 2008, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).To use a DFS, Lync Server 2013 requires the following:</span></span>

  - <span data-ttu-id="04665-108">Namespaces sind Domänen basiert</span><span class="sxs-lookup"><span data-stu-id="04665-108">Namespaces are domain based</span></span>

  - <span data-ttu-id="04665-109">Auf allen Namespaceservern wird ein minimales Windows 2008 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04665-109">All namespace servers are running a minimum of Windows 2008</span></span>

<span data-ttu-id="04665-110">Das Setup von lync Server 2013 erfordert, dass Berechtigungen für den freigegebenen Ordner den vollständigen Zugriff auf den Administrator ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="04665-110">Lync Server 2013 setup requires that permissions on shared folder allow full access to Administrator.</span></span> <span data-ttu-id="04665-111">Lync Server 2013 verwendet dann NTFS-Dateiberechtigungen, um die Ordner zu ACL.</span><span class="sxs-lookup"><span data-stu-id="04665-111">Lync Server 2013 will then use NTFS file permissions to ACL the folders.</span></span> <span data-ttu-id="04665-112">Geerbte DFS-Freigabeberechtigungen werden nicht verwendet, um den Zugriff zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="04665-112">Inherited DFS share permissions will not be used to restrict access.</span></span>

<span data-ttu-id="04665-113">Weitere Informationen zu den Anforderungen an Dateifreigaben finden Sie unter unter [Stützung von Dateispeicher in lync Server 2013](lync-server-2013-file-storage-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="04665-113">For more details about File Share requirements, see [File storage support in Lync Server 2013](lync-server-2013-file-storage-support.md) in the Supportability documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="04665-114">Möglicherweise suchen Sie nach Informationen zum Konfigurieren einer nicht DFS-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="04665-114">You may be looking for information on configuring a non-DFS share.</span></span> <span data-ttu-id="04665-115">Wenn dies der Fall ist, lesen Sie <A href="lync-server-2013-hardware-setup.md">Hardware-Setup für lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="04665-115">If so, check out <A href="lync-server-2013-hardware-setup.md">Hardware setup for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="04665-116">Im folgenden Verfahren wird beschrieben, wie Sie die Berechtigungen für freigegebene Ordner mithilfe des DFS-Namespace-Assistenten richtig konfigurieren (wie im DFS-Setup Handbuch beschrieben).</span><span class="sxs-lookup"><span data-stu-id="04665-116">The following procedure describes how to correctly configure shared folder permissions using the DFS Namespace Wizard (as described in DFS setup guide).</span></span>

<div>

## <a name="to-configure-shared-folder-permissions"></a><span data-ttu-id="04665-117">So konfigurieren Sie Berechtigungen für freigegebene Ordner</span><span class="sxs-lookup"><span data-stu-id="04665-117">To configure shared folder permissions</span></span>

1.  <span data-ttu-id="04665-118">Klicken Sie auf **Start**, zeigen Sie auf **Alle Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **DFS-Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="04665-118">Click **Start**, point to **All Programs**, point to **Administrative Tools**, and then click **DFS Management**.</span></span>

2.  <span data-ttu-id="04665-119">Klicken Sie in der Konsolenstruktur des DFS-Verwaltungs-Snap-Ins mit der rechten Maustaste auf den Namespaceserver (beispielsweise filesrv1.contoso.com), und klicken Sie dann auf **Einstellungen bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="04665-119">In the console tree of the DFS Management snap-in, right-click the namespace server (for example filesrv1.contoso.com), and then click **Edit Settings**.</span></span>

3.  <span data-ttu-id="04665-120">Wählen Sie **Berechtigungen für freigegebene Ordner** aus.</span><span class="sxs-lookup"><span data-stu-id="04665-120">Select **Shared Folder Permissions**.</span></span>

4.  <span data-ttu-id="04665-121">Wählen Sie **benutzerdefinierte Berechtigungen verwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="04665-121">Select **Use Custom Permissions**.</span></span>

5.  <span data-ttu-id="04665-122">Wählen Sie für die Gruppe Administratoren unter **zulassen** die folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="04665-122">For the Administrator group, select the following under **Allow**:</span></span>
    
      - <span data-ttu-id="04665-123">**Vollzugriff**</span><span class="sxs-lookup"><span data-stu-id="04665-123">**Full Control**</span></span>
    
      - <span data-ttu-id="04665-124">**Änderung**</span><span class="sxs-lookup"><span data-stu-id="04665-124">**Change**</span></span>
    
      - <span data-ttu-id="04665-125">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="04665-125">**Read**</span></span>

6.  <span data-ttu-id="04665-126">Klicken Sie auf über **nehmen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="04665-126">Click **Apply**, and then click **OK**.</span></span>

<span data-ttu-id="04665-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="04665-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

