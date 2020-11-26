---
title: 'Lync Server 2013: Notfallwiederherstellungstest'
description: 'Lync Server 2013: Disaster Recovery-Test.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Disaster recovery test
ms:assetid: 04f5e747-d837-4350-9fc0-8605dbf025a7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747887(v=OCS.15)
ms:contentKeyID: 63969571
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa22abd37f656134c54381d63f29d3160ff85257
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437833"
---
# <a name="disaster-recovery-test-in-lync-server-2013"></a><span data-ttu-id="2ddc4-103">Notfallwiederherstellungstest in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ddc4-103">Disaster recovery test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ddc4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ddc4-104">

<span> </span></span></span>

<span data-ttu-id="2ddc4-105">_**Letztes Änderungsdatum des Themas:** 2015-01-26_</span><span class="sxs-lookup"><span data-stu-id="2ddc4-105">_**Topic Last Modified:** 2015-01-26_</span></span>

<span data-ttu-id="2ddc4-106">Führen Sie eine Systemwiederherstellung für einen lync Server 2013-Pool Server aus, um Ihren dokumentierten Disaster Recovery-Prozess zu testen.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-106">Perform a system recovery for a Lync Server 2013 pool server to test your documented disaster recovery process.</span></span> <span data-ttu-id="2ddc4-107">Mit diesem Test wird ein vollständiger Hardwarefehler für einen Server simuliert, und es wird sichergestellt, dass die Ressourcen, Pläne und Daten für die Wiederherstellung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-107">This test will simulate a complete hardware failure for one server, and will help guarantee that the resources, plans, and data is available for recovery.</span></span> <span data-ttu-id="2ddc4-108">Versuchen Sie, den Fokus des Tests monatlich zu drehen, damit Ihre Organisation den Fehler eines anderen Servers oder eines anderen Geräts jedes Mal testet.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-108">Try to rotate the focus of the test each month so that your organization tests the failure of a different server or other piece of equipment every time.</span></span>

<span data-ttu-id="2ddc4-p102">Beachten Sie, dass der Zeitplan, nach dem Organisationen Notfallwiederherstellungstests durchführen, unterschiedlich ist. Es ist sehr wichtig, dass Notfallwiederherstellungstests nicht ignoriert oder vernachlässigt werden.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-p102">Note that the schedule by which organizations perform Disaster Recovery testing will vary. It is very important that disaster recovery testing is not ignored or neglected.</span></span>

<div>


<span data-ttu-id="2ddc4-111">Exportieren Sie Ihre lync Server 2013-Topologie,-Richtlinien und-Konfigurationseinstellungen in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-111">Export your Lync Server 2013 topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="2ddc4-112">Unter anderem kann diese Datei nach einem Upgrade, einem Hardwareausfall oder einem anderen Problem, das zu Datenverlust geführt hat, zum Wiederherstellen dieser Informationen im zentralen Verwaltungsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-112">Among other things, this file can then be used to restore this information to the Central Management store after an upgrade, a hardware failure, or some other issue has resulted in data loss.</span></span>

<span data-ttu-id="2ddc4-113">Importieren Sie Ihre lync Server 2013-Topologie,-Richtlinien und-Konfigurationseinstellungen entweder in den zentralen Verwaltungsspeicher oder auf den lokalen Computer, wie in den folgenden Befehlen gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2ddc4-113">Import your Lync Server 2013 topology, policies, and configuration settings to either the Central Management store or to the local computer as shown in the following commands:</span></span>

`Import-CsConfiguration -ByteInput <Byte[]> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

`Import-CsConfiguration -FileName <String> [-Force <SwitchParameter>] [-LocalStore <SwitchParameter>]`

<span data-ttu-id="2ddc4-114">So sichern Sie Production lync Server 2013-Daten:</span><span class="sxs-lookup"><span data-stu-id="2ddc4-114">To back up production Lync Server 2013 data:</span></span>

  - <span data-ttu-id="2ddc4-115">Sichern Sie die RTC-und LCSLog-Datenbanken mithilfe des standardmäßigen SQL Server-Sicherungsprozesses, um die Datenbank auf ein Datei-oder Bandspeicher Abbildgerät zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-115">Back up the RTC and LCSLog databases by using the standard SQL Server backup process to dump the database to a file or tape dump device.</span></span>

  - <span data-ttu-id="2ddc4-116">Verwenden Sie eine Sicherungsanwendung von einem Drittanbieter, um die Daten in einer Datei oder auf einem Band zu sichern.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-116">Use third-party backup application to back up the data to file or to tape.</span></span>

  - <span data-ttu-id="2ddc4-117">Verwenden Sie das Cmdlet „Export-CsUserData“, um einen XML-Export der gesamten RTC-Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-117">Use the Export-CsUserData cmdlet to create an XML export of the whole RTC database.</span></span>

  - <span data-ttu-id="2ddc4-118">Verwenden Sie die Dateisystemsicherung oder eine Drittanbieteranwendung, um Besprechungsinhalte und -kompatibilitätsprotokolle zu sichern.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-118">Use the file system backup or third-party to back up meeting content and compliance logs.</span></span>

  - <span data-ttu-id="2ddc4-119">Verwenden Sie das Befehlszeilentool Export-CsConfiguration, um die lync Server 2013-Einstellungen zu sichern.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-119">Use the Export-CsConfiguration command-line tool to back up Lync Server 2013 settings.</span></span>

<span data-ttu-id="2ddc4-120">Der erste Schritt in der Failoverprozedur besteht in einer erzwungenen Verschiebung von Benutzern aus dem Produktionspool in den Notfallwiederherstellungspool.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-120">The first step in the failover procedure includes a forced move of users from the production pool to the Disaster Recovery pool.</span></span>

<span data-ttu-id="2ddc4-121">Es handelt sich dabei um eine erzwungene Verschiebung, da der Produktionspool nicht verfügbar ist, um die Benutzerumsetzung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-121">This will be a forced move because the production pool won't be available to accept the user relocation.</span></span>

<span data-ttu-id="2ddc4-122">Der lync Server 2013 Move-Benutzerprozess ist eine Änderung an einem Attribut für das Benutzerkontoobjekt sowie eine Datensatzaktualisierung in der RTC SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-122">The Lync Server 2013 move user process is effectively a change to an attribute on the user account object in addition to a record update on the RTC SQL database.</span></span>

<span data-ttu-id="2ddc4-123">Diese Daten können mithilfe der folgenden zwei Prozesse wiederhergestellt werden:</span><span class="sxs-lookup"><span data-stu-id="2ddc4-123">This data can be restored through the following two processes:</span></span>

  - <span data-ttu-id="2ddc4-124">Die RTC-Datenbank kann vom ursprünglichen Sicherungsspeicher Abbild-Gerät aus dem Produktions-SQL Server mithilfe des Standard Wiederherstellungsprozesses von SQL Server oder mithilfe eines Sicherungs-/Wiederherstellungstools eines Drittanbieters wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-124">RTC database can be restored from the original backup dump device from the production SQL Server using the standard SQL Server restore process, or using a third-party backup/restore utility.</span></span>

  - <span data-ttu-id="2ddc4-125">Benutzerkontaktdaten können mit dem Hilfsprogramm DBIMPEXP.exe über die aus dem SQL Server-Produktionsexport erstellte XML-Datei wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-125">User contact data can be restored with the DBIMPEXP.exe utility using the XML file that was created from the production SQL Server export.</span></span>

<span data-ttu-id="2ddc4-126">Nach der Wiederherstellung dieser Daten können Benutzer eine Verbindung mit dem Disaster Recovery lync Server 2013-Pool herstellen und wie gewohnt funktionieren.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-126">After this data is restored, users can effectively connect to the Disaster Recovery Lync Server 2013 pool, and operate as usual.</span></span>

<span data-ttu-id="2ddc4-127">Damit Benutzer eine Verbindung mit dem Disaster Recovery lync Server 2013-Pool herstellen können, ist eine Änderung des DNS-Eintrags erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-127">To enable users to connect to the Disaster Recovery Lync Server 2013 pool, a DNS record change will be required.</span></span>

<span data-ttu-id="2ddc4-128">Clients, die die automatischen Konfigurations-und DNS-SRV-Einträge verwenden, werden auf den lync Server 2013-Produktionspool verwiesen:</span><span class="sxs-lookup"><span data-stu-id="2ddc4-128">The production Lync Server 2013 pool will be referenced by clients using the auto-configuration and DNS SRV records of:</span></span>

  - <span data-ttu-id="2ddc4-129">SRV: \_ SIP. \_ TLS.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-129">SRV: \_sip.\_tls.\<domain\></span></span> <span data-ttu-id="2ddc4-130">/CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-130">/CNAME: SIP.\<domain\></span></span>

  - <span data-ttu-id="2ddc4-131">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-131">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="2ddc4-132">/cvc-pool-1.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-132">/cvc-pool-1.\<domain\></span></span>

<span data-ttu-id="2ddc4-133">Zur Vereinfachung des Failovers muss dieser CNAME-Eintrag so aktualisiert werden, dass er auf den DROCSPool-FQDN verweist:</span><span class="sxs-lookup"><span data-stu-id="2ddc4-133">To facilitate the failover, this CNAME record must be updated to reference the DROCSPool FQDN:</span></span>

  - <span data-ttu-id="2ddc4-134">CNAME: SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-134">CNAME: SIP.\<domain\></span></span> <span data-ttu-id="2ddc4-135">/DROCSPool.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-135">/DROCSPool.\<domain\></span></span>

  - <span data-ttu-id="2ddc4-136">SIP.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-136">Sip.\<domain\></span></span>

  - <span data-ttu-id="2ddc4-137">AV.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-137">AV.\<domain\></span></span>

  - <span data-ttu-id="2ddc4-138">webconf.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-138">webconf.\<domain\></span></span>

  - <span data-ttu-id="2ddc4-139">OCSServices.\<domain\></span><span class="sxs-lookup"><span data-stu-id="2ddc4-139">OCSServices.\<domain\></span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2ddc4-140">Detaillierte Verwaltungs-und Verwaltungsverfahren finden Sie unter <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">Sichern und Wiederherstellen von lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="2ddc4-140">For detailed administration and management procedures, see <A href="lync-server-2013-backing-up-and-restoring-lync-server.md">Backing up and restoring Lync Server 2013</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2ddc4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ddc4-141">See Also</span></span>


[<span data-ttu-id="2ddc4-142">Planen der hohen Verfügbarkeit und der Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ddc4-142">Planning for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)  
[<span data-ttu-id="2ddc4-143">Cmdlets für Backup und höhere Verfügbarkeit in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ddc4-143">Backup and high availability cmdlets in Lync Server 2013</span></span>](https://docs.microsoft.com/powershell/module/skype/?view=skype-ps)  


[<span data-ttu-id="2ddc4-144">Importieren-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ddc4-144">Import-CsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsConfiguration)  
[<span data-ttu-id="2ddc4-145">Sichern und Wiederherstellen von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ddc4-145">Backing up and restoring Lync Server 2013</span></span>](lync-server-2013-backing-up-and-restoring-lync-server.md)  
[<span data-ttu-id="2ddc4-146">Verwalten der Notfallwiederherstellung, der hohen Verfügbarkeit und des Sicherungsdiensts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ddc4-146">Managing Lync Server 2013 disaster recovery, high availability, and Backup Service</span></span>](lync-server-2013-managing-lync-server-disaster-recovery-high-availability-and-backup-service.md)  
  

<span data-ttu-id="2ddc4-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ddc4-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

