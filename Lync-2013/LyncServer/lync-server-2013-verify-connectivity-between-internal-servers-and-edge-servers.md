---
title: Überprüfen der Konnektivität zwischen internen Servern und Edgeservern
description: Überprüfen Sie die Konnektivität zwischen internen Servern und Edge-Servern.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity between internal servers and Edge Servers
ms:assetid: 219f706e-2b8a-46c5-b394-c384240eef50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398292(v=OCS.15)
ms:contentKeyID: 48183602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f86f87428d7eaf91b8f70422cfee712584252fad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395059"
---
# <a name="verify-connectivity-between-internal-servers-and-edge-servers-in-lync-server-2013"></a><span data-ttu-id="8c5b6-103">Überprüfen der Konnektivität zwischen internen Servern und Edgeservern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c5b6-103">Verify connectivity between internal servers and Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c5b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c5b6-104">

<span> </span></span></span>

<span data-ttu-id="8c5b6-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="8c5b6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="8c5b6-106">In lync Server 2013 war ein separater Überprüfungs-Assistent verfügbar, der die Überprüfung der Konnektivität zwischen Edge-Servern und internen Servern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-106">In Lync Server 2013, a separate validation wizard was available to help validate connectivity between Edge Servers and internal servers.</span></span> <span data-ttu-id="8c5b6-107">In lync Server 2013 erfolgt die Überprüfung der Konnektivität automatisch, wenn Sie Ihre Edgeserver installieren.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-107">In Lync Server 2013 validation of connectivity is done automatically when you install your Edge Servers.</span></span>

<span data-ttu-id="8c5b6-108">Sie können die Replikation von Konfigurationsinformationen an den Edge überprüfen, indem Sie das Windows PowerShell-Cmdlet " **Get-CsManagementStoreReplicationStatus** " auf dem internen Computer ausführen, auf dem sich der zentrale Verwaltungsspeicher befindet (oder ein beliebiger Domänen verbundener Computer, auf dem lync Server 2013 Core Components (OcsCore.msi) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-108">You can validate the replication of configuration information to the edge by running the Windows PowerShell **Get-CsManagementStoreReplicationStatus** cmdlet on the internal computer on which the Central Management store is located (or any domain joined computer on which Lync Server 2013 Core Components (OcsCore.msi) is installed.</span></span> <span data-ttu-id="8c5b6-109">Anfängliche Ergebnisse können den Status "falsch" anstelle von "true" für die Replikation angeben.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-109">Initial results may indicate the status as "False" instead of "True" for replication.</span></span> <span data-ttu-id="8c5b6-110">Wenn dies der Fall ist, führen Sie das Cmdlet **Invoke-CsManagementStoreReplication** aus, und lassen Sie die Replikation Zeit, bevor **Sie die Get-CsManagementStoreReplicationStatus** erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-110">If so, run the **Invoke-CsManagementStoreReplication** cmdlet and allow time for the replication to complete before running the **Get-CsManagementStoreReplicationStatus** again.</span></span>

<span data-ttu-id="8c5b6-111">Sie können die Konnektivität externer Benutzer separat überprüfen, einschließlich der Verwendung von Office Communications Server-Remote Verbindungsanalyse, um die Remotebenutzerkonnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c5b6-111">You can verify external user connectivity separately, including using the Office Communications Server Remote Connectivity Analyzer to verify remote user connectivity.</span></span> <span data-ttu-id="8c5b6-112">Ausführliche Informationen finden Sie unter [Überprüfen der Konnektivität für externe Benutzer in lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span><span class="sxs-lookup"><span data-stu-id="8c5b6-112">For details, see [Verify connectivity for external users in Lync Server 2013](lync-server-2013-verify-connectivity-for-external-users.md).</span></span>

<span data-ttu-id="8c5b6-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c5b6-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

