---
title: Aktualisieren von DNS SRV-Einträgen
description: Aktualisieren von DNS-SRV-Einträgen
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Update DNS SRV records
ms:assetid: 9542b91a-108c-4980-89ec-634905cbbf26
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688139(v=OCS.15)
ms:contentKeyID: 49733739
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24161074e8f3bcf7e296a957588eeb59d5f2ad1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446549"
---
# <a name="update-dns-srv-records"></a><span data-ttu-id="297d1-103">Aktualisieren von DNS SRV-Einträgen</span><span class="sxs-lookup"><span data-stu-id="297d1-103">Update DNS SRV records</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="297d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="297d1-104">

<span> </span></span></span>

<span data-ttu-id="297d1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="297d1-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="297d1-106">Um dieses Verfahren erfolgreich durchführen zu können, sollten Sie als Mitglied der Gruppe Domänenadministratoren oder als Mitglied der DnsAdmins-Gruppe am Server oder in der Domäne angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="297d1-106">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="297d1-107">In diesem Thema wird beschrieben, wie Sie die DNS-Einträge (Domain Name System) nach der Migration zu lync Server 2013 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="297d1-107">This topic describes how to update the Domain Name System (DNS) records after migrating to Lync Server 2013.</span></span> <span data-ttu-id="297d1-108">Nachdem alle Benutzer nach lync Server 2013 verschoben wurden, aber bevor der Legacy lync Server 2010-Pool oder-Director außer Betrieb genommen wird, müssen Sie die DNS-SRV-Einträge in Ihrem internen DNS für jede SIP-Domäne aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="297d1-108">After all users have been moved to Lync Server 2013, but before the legacy Lync Server 2010 pool or Director is decommissioned, you must update the DNS SRV records in your internal DNS for every SIP domain.</span></span> <span data-ttu-id="297d1-109">Bei diesem Verfahren wird davon ausgegangen, dass Ihr interner DNS Zonen für Ihre SIP-Benutzerdomänen aufweist.</span><span class="sxs-lookup"><span data-stu-id="297d1-109">This procedure assumes that your internal DNS has zones for your SIP user domains.</span></span>

<span data-ttu-id="297d1-110">**So konfigurieren Sie einen DNS-SRV-Eintrag**</span><span class="sxs-lookup"><span data-stu-id="297d1-110">**To configure a DNS SRV record**</span></span>

1.  <span data-ttu-id="297d1-111">Klicken Sie auf dem DNS-Server auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="297d1-111">On the DNS server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="297d1-112">Erweitern Sie in der Konsolenstruktur ihrer SIP-Domäne **Forward-Lookupzonen**, erweitern Sie die SIP-Domäne, in der lync Server 2013 installiert ist, und navigieren Sie zur **\_ TCP** -Einstellung.</span><span class="sxs-lookup"><span data-stu-id="297d1-112">In the console tree for your SIP domain, expand **Forward Lookup Zones**, expand the SIP domain in which Lync Server 2013 is installed, and navigate to the **\_tcp** setting.</span></span>

3.  <span data-ttu-id="297d1-113">Klicken Sie im rechten Bereich mit der rechten Maustaste auf **\_ sipinternaltls** , und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="297d1-113">In the right pane, right click **\_sipinternaltls** and select **Properties**.</span></span>

4.  <span data-ttu-id="297d1-114">Aktualisieren Sie im Host, der **diesen Dienst anbietet**, den FQDN des Hosts so, dass er auf den lync Server 2013-Pool verweist.</span><span class="sxs-lookup"><span data-stu-id="297d1-114">In **Host offering this service**, update the host FQDN to point to the Lync Server 2013 pool.</span></span>

5.  <span data-ttu-id="297d1-115">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="297d1-115">Click **OK**.</span></span>

<span data-ttu-id="297d1-116">**So überprüfen Sie, ob der FQDN des Front-End-Pools oder des Standard Edition-Servers aufgelöst werden kann**</span><span class="sxs-lookup"><span data-stu-id="297d1-116">**To verify that the FQDN of the Front End pool or Standard Edition server can be resolved**</span></span>

1.  <span data-ttu-id="297d1-117">Melden Sie sich bei einem Clientcomputer in der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="297d1-117">Log on to a client computer in the domain.</span></span>

2.  <span data-ttu-id="297d1-118">Klicken Sie auf  **Start** und dann auf  **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="297d1-118">Click **Start**, and then click **Run**.</span></span>

3.  <span data-ttu-id="297d1-119">Geben Sie im Feld **Öffnen** den **Befehl cmd** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="297d1-119">In the **Open** box, type **cmd**, and then click **OK**.</span></span>

4.  <span data-ttu-id="297d1-120">Geben Sie an der Eingabeaufforderung **nslookup** \<FQDN of the Front End pool\> oder \<FQDN of the Standard Edition server\> ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="297d1-120">At the command prompt, type **nslookup** \<FQDN of the Front End pool\> or \<FQDN of the Standard Edition server\>, and then press ENTER.</span></span>

5.  <span data-ttu-id="297d1-121">Überprüfen Sie, ob Sie eine Antwort erhalten, die in die entsprechende IP-Adresse für den FQDN aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="297d1-121">Verify that you receive a reply that resolves to the appropriate IP address for the FQDN.</span></span>

<span data-ttu-id="297d1-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="297d1-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

