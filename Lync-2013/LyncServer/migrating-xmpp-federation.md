---
title: Migrieren eines XMPP-Partnerverbunds
description: Migrieren von XMPP-Föderation
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating XMPP federation
ms:assetid: b8d2b4b9-d0ed-4b48-820a-2c257fbdd2fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721861(v=OCS.15)
ms:contentKeyID: 49733794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e63c9f6fd3f1c1d45de77c27417987505678f74b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440360"
---
# <a name="migrating-xmpp-federation"></a><span data-ttu-id="3f41b-103">Migrieren eines XMPP-Partnerverbunds</span><span class="sxs-lookup"><span data-stu-id="3f41b-103">Migrating XMPP federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3f41b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3f41b-104">

<span> </span></span></span>

<span data-ttu-id="3f41b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="3f41b-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="3f41b-106">In früheren Versionen von lync Server und Office Communications Server wurde ein Extensible Messaging and Presence Protocol (XMPP)-Gateway bereitgestellt, das als separate Server Rolle bereitgestellt werden kann, um die Föderation mit XMPP-Bereitstellungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3f41b-106">Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments.</span></span> <span data-ttu-id="3f41b-107">In lync Server 2013 kann die XMPP-Funktion als Feature bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f41b-107">In Lync Server 2013, the XMPP functionality can be deployed as a feature.</span></span> <span data-ttu-id="3f41b-108">Die XMPP-Funktionalität ist in zwei Teilen installiert: als XMPP-Proxy, der auf dem lync Server 2013-Edgeserver ausgeführt wird, und dem XMPP-Gateway, das auf dem lync Server 2013-Front-End-Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f41b-108">XMPP functionality is installed in two parts: as an XMPP proxy that runs on the Lync Server 2013 Edge Server, and the XMPP Gateway that runs on the Lync Server 2013 Front End Server.</span></span>

<span data-ttu-id="3f41b-109">Aus Sicht der Migration kann ein lync Server-Benutzerkonto in einen lync Server 2013-Pool verschoben und weiterhin das Legacy-XMPP-Gateway verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f41b-109">From a migration perspective, a Lync Server user account can be moved to a Lync Server 2013 pool and continue to use the legacy XMPP gateway.</span></span> <span data-ttu-id="3f41b-110">Dies ist nur möglich, wenn der XMPP-Verbundpartner nicht in lync Server 2013 konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3f41b-110">This is possible only when the XMPP federated partner is not configured in Lync Server 2013.</span></span>

<span data-ttu-id="3f41b-111">Zusammenfassung: Wenn lync Server 2010 mit dem Office Communications Server 2007 R2 XMPP-Gateway bereitgestellt wurde und die XMPP-Föderation für Legacy-lync Server 2010-Benutzer aktiviert wurde, können Sie die XMPP-Föderation zu lync Server 2013 migrieren:</span><span class="sxs-lookup"><span data-stu-id="3f41b-111">In summary, if Lync Server 2010 has been deployed with the Office Communications Server 2007 R2 XMPP Gateway and XMPP federation has been enabled for legacy Lync Server 2010 users, to migrate the XMPP federation to Lync Server 2013:</span></span>

1.  <span data-ttu-id="3f41b-112">Bereitstellen eines lync Server 2013-Pools</span><span class="sxs-lookup"><span data-stu-id="3f41b-112">Deploy a Lync Server 2013 pool.</span></span>

2.  <span data-ttu-id="3f41b-113">Bereitstellen eines lync Server 2013-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="3f41b-113">Deploy a Lync Server 2013 Edge server.</span></span>

3.  <span data-ttu-id="3f41b-114">Verschieben aller Benutzer in den lync Server 2013-Pool</span><span class="sxs-lookup"><span data-stu-id="3f41b-114">Move all users to the Lync Server 2013 pool</span></span>

4.  <span data-ttu-id="3f41b-115">Erstellen Sie XMPP-Zugriffsrichtlinien und-Zertifikate für den Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="3f41b-115">Create XMPP access policies and certificates for the Edge Server.</span></span>

5.  <span data-ttu-id="3f41b-116">Aktivieren Sie die XMPP-Föderation in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3f41b-116">Enable XMPP federation in Lync Server 2013.</span></span> 

6.  <span data-ttu-id="3f41b-117">Aktualisieren Sie die DNS-Einträge so, dass Sie auf das lync Server 2013 XMPP-Gateway verweisen.</span><span class="sxs-lookup"><span data-stu-id="3f41b-117">Update the DNS entries to point to the Lync Server 2013 XMPP Gateway.</span></span>

<span data-ttu-id="3f41b-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3f41b-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

