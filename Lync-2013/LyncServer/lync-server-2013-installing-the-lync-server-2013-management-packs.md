---
title: 'Lync Server 2013: Installieren der lync Server 2013-Verwaltungspakete'
description: 'Lync Server 2013: Installieren der lync Server 2013-Verwaltungspakete'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426928"
---
# <a name="installing-the-lync-server-2013-management-packs"></a><span data-ttu-id="c948a-103">Installieren der lync Server 2013-Verwaltungspakete</span><span class="sxs-lookup"><span data-stu-id="c948a-103">Installing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c948a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c948a-104">

<span> </span></span></span>

<span data-ttu-id="c948a-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="c948a-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="c948a-106">System Center Operations Manager kann nur einen kleinen Teil des Windows-Betriebssystems überwachen.</span><span class="sxs-lookup"><span data-stu-id="c948a-106">By itself, System Center Operations Manager has the ability to monitor only a small portion of the Windows operating system.</span></span> <span data-ttu-id="c948a-107">Sie können die Funktionen von System Center Operations Manager jedoch erweitern, indem Sie Management Packs installieren, Software, die festlegt, welche Elemente von System Center Operations Manager überwacht werden können, einschließlich der Art und Weise, wie diese Elemente überwacht werden sollen und wie Benachrichtigungen ausgelöst und gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c948a-107">However, you can extend the capabilities of System Center Operations Manager by installing management packs, software that dictates which items System Center Operations Manager can monitor, including how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="c948a-108">Microsoft lync Server 2013 umfasst zwei System Center Operations Manager-Verwaltungspakete, die die folgenden Funktionen bieten:</span><span class="sxs-lookup"><span data-stu-id="c948a-108">Microsoft Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="c948a-109">Das Komponenten-und Benutzer Verwaltungspaket (Microsoft.ls.2013.Monitoring.ComponentAndUser.MP) verfolgt lync-Server Probleme, die in Ereignisprotokollen aufgezeichnet, von Leistungsindikatoren registriert oder in den Anruf Detaildatensätzen (CDR) oder den QoE-Datenbanken (Quality of Experience) protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="c948a-109">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="c948a-110">Bei kritischen Problemen kann System Center Operations Manager so konfiguriert werden, dass Administratoren sofort per e-Mail, Sofortnachricht oder SMS-Messaging benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c948a-110">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="c948a-111">SMS ist die Technologie, die verwendet wird, um Textnachrichten von einem mobilen Gerät an ein anderes zu senden.</span><span class="sxs-lookup"><span data-stu-id="c948a-111">SMS is the technology used to send text messages from one mobile device to another.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c948a-112">Weitere Informationen zum Konfigurieren der Operations Manager-Benachrichtigung finden Sie unter Konfigurieren der Benachrichtigung in der TechNet-Bibliothek unter <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> .</span><span class="sxs-lookup"><span data-stu-id="c948a-112">For more information on configuring Operations Manager notification, see Configuring Notification in the TechNet Library at <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="c948a-113">Das aktive Überwachungspaket (Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP) testet proaktiv wichtige lync Server-Komponenten wie die Anmeldung am System, den Austausch von Sofortnachrichten oder das tätigen von Anrufen an ein Telefon, das sich im öffentlichen Telefonnetz (PSTN) befindet.</span><span class="sxs-lookup"><span data-stu-id="c948a-113">The Active Monitoring Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="c948a-114">Diese Tests werden mithilfe der Cmdlets für synthetische lync Server-Transaktionen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c948a-114">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="c948a-115">Zum Beispiel wird das **Test-CsIM**-Cmdlet verwendet, um eine Sofortnachrichtenunterhaltung zwischen zwei Testbenutzern zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="c948a-115">For example, the **Test-CsIM** cmdlet is used to simulate an instant messaging conversation between a pair of test users.</span></span> <span data-ttu-id="c948a-116">Wenn diese simulierte Nachrichten Unterhaltung fehlschlägt, wird eine Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="c948a-116">If this simulated messaging conversation fails an alert will be generated.</span></span>

<span data-ttu-id="c948a-117">Zu den beiden in lync Server 2013 enthaltenen Management Packs gehören eine große Anzahl von Verbesserungen hinsichtlich der Management Packs, die mit Microsoft lync Server 2010 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c948a-117">The two management packs included with Lync Server 2013 include a large number of enhancements over the management packs used with Microsoft Lync Server 2010.</span></span> <span data-ttu-id="c948a-118">Das lync Server 2013-Komponenten-Management Pack ist beispielsweise nicht darauf limitiert, lync Server selbst zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c948a-118">For example, the Lync Server 2013 Component Management Pack is not limited to monitoring Lync Server itself.</span></span> <span data-ttu-id="c948a-119">Neben dem Überwachen von Ereignisprotokollen und Leistungsindikatoren für lync Server kann das Komponenten-Management Pack auch die Leistung von wichtigen Elementen wie:</span><span class="sxs-lookup"><span data-stu-id="c948a-119">In addition to monitoring event logs and performance counters for Lync Server, the Component Management pack can also track the performance of, and issue alerts for, crucial items such as:</span></span>

  - <span data-ttu-id="c948a-120">**Internet Informationsdienste (IIS)**   Benachrichtigungen werden ausgegeben, wenn Internet-Informationsdienste offline geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="c948a-120">**Internet Information Services (IIS)**   Alerts will be issued if Internet Information Services goes offline.</span></span> <span data-ttu-id="c948a-121">Dies ist wichtig, da die lync Server-Webdienste von IIS abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c948a-121">This is important, because the Lync Server web services rely on IIS.</span></span>

  - <span data-ttu-id="c948a-122">**Prozessnutzung**   Benachrichtigungen werden ausgegeben, wenn Systemressourcen (wie verfügbarer Arbeitsspeicher) langsam ablaufen.</span><span class="sxs-lookup"><span data-stu-id="c948a-122">**Process usage**   Alerts will be issued if system resources (such as available memory) begin to run low.</span></span> <span data-ttu-id="c948a-123">Diese Benachrichtigungen werden selbst dann ausgestellt, wenn lync Server nicht für die Verwendung des Systems mit großem Nutzen verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="c948a-123">These alerts will be issued even if Lync Server is not responsible for the high system usage.</span></span>

  - <span data-ttu-id="c948a-124">**Computer Fehlerereignisse**   Benachrichtigungen werden im Fall eines Hardware-oder Softwareproblems ausgestellt, das die Lebensfähigkeit eines Servers gefährdet.</span><span class="sxs-lookup"><span data-stu-id="c948a-124">**Computer failure events**   Alerts will be issued in case of a hardware or software issue that threatens the viability of a server.</span></span> <span data-ttu-id="c948a-125">Lync Server-Administratoren werden beispielsweise benachrichtigt, wenn ein Server den Eindruck hat, dass ein Festplattenfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c948a-125">For example, Lync Server administrators will be notified if a server appears to be in danger of experiencing a hard disk failure.</span></span>

<span data-ttu-id="c948a-126">Die neuen Management Packs verfügen auch über eine verbesserte Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="c948a-126">The new management packs also feature enhanced reporting.</span></span> <span data-ttu-id="c948a-127">Zu den neuen Berichten für lync Server 2013 gehören:</span><span class="sxs-lookup"><span data-stu-id="c948a-127">New reports for Lync Server 2013 include:</span></span>

  - <span data-ttu-id="c948a-128">**Bericht "End-to-End-Szenario-Verfügbarkeit**   "   Dieser Bericht enthält Informationen zur Verfügbarkeit/Uptime für wichtige lync Server-Dienste wie Registrierung oder Anwesenheit.</span><span class="sxs-lookup"><span data-stu-id="c948a-128">**End to End Scenario Availability Report**   This report details the availability/uptime for key Lync Server services such as registration or presence.</span></span>

  - <span data-ttu-id="c948a-129">**Kapazitäts Bericht**   In diesem Bericht werden mithilfe von Leistungsindikatorinformationen Trends für Systemkomponenten wie Speicherverfügbarkeit und Prozessorauslastung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c948a-129">**Capacity Report**   Using performance counter information, this report shows trends for system components such as memory availability and processor usage.</span></span>

  - <span data-ttu-id="c948a-130">**Komponentenbericht**   Dieser Bericht listet die obersten Warnungs Generatoren auf, die nach lync Server-Komponente gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="c948a-130">**Component Report**   This report lists the top alert generators grouped by Lync Server component.</span></span>

<span data-ttu-id="c948a-131">Zusätzlich zu diesen vordefinierten Berichten melden die Management Packs für lync Server 2013 automatisch Warnungen für die Zuverlässigkeit von Anrufen (Metriken, die mit der Anruf Detail Aufzeichnung gemessen werden) und QoE-Zustände (Metriken, die nach der Qualität der Erfahrung gemessen werden).</span><span class="sxs-lookup"><span data-stu-id="c948a-131">In addition to these predesigned reports, the management packs for Lync Server 2013 automatically report alerts for both Call Reliability (metrics measured by Call Detail Recording) and QoE states (metrics measured by Quality of Experience).</span></span> <span data-ttu-id="c948a-132">Wenn Sie die Anruf Detail Aufzeichnung aktiviert haben, können Sie die Zuverlässigkeits Benachrichtigungen für Anrufe überprüfen, indem Sie die folgenden Schritte in der System Center Operations Manager-Konsole ausführen:</span><span class="sxs-lookup"><span data-stu-id="c948a-132">If you have enabled Call Detail Recording, you can review Call Reliability alerts by completing the following procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="c948a-133">Erweitern Sie **Überwachung**, erweitern Sie **Microsoft lync Server 2013 Health**, erweitern Sie die **Anruf Zuverlässigkeit und die Medienqualität**, und klicken Sie dann auf **Anruf Zuverlässigkeit**.</span><span class="sxs-lookup"><span data-stu-id="c948a-133">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then click **Call Reliability**.</span></span>

<span data-ttu-id="c948a-134">Führen Sie die folgenden Schritte über die System Center Operations Manager-Konsole aus, um die Benachrichtigung über die Qualität der Erfahrung anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="c948a-134">To view Quality of Experience alerts, complete this procedure from the System Center Operations Manager console:</span></span>

  - <span data-ttu-id="c948a-135">Erweitern Sie **Überwachung**, erweitern Sie **Microsoft lync Server 2013 Health**, erweitern Sie die **Anruf Zuverlässigkeit und Medienqualität**, und erweitern Sie dann **Medienqualität**.</span><span class="sxs-lookup"><span data-stu-id="c948a-135">Expand **Monitoring**, expand **Microsoft Lync Server 2013 Health**, expand **Call Reliability and Media Quality**, and then expand **Media Quality**.</span></span>

<span data-ttu-id="c948a-136">Die Management Packs für lync Server 2013 verwenden jetzt die Ermittlung auf Computerebene anstelle des zentralen Ermittlungsmechanismus, der in Microsoft lync Server 2010 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c948a-136">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism used in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="c948a-137">Dies bedeutet, dass sich jeder System Center-Agent im wesentlichen selbst erkennt und seine Existenz dem zentralen Verwaltungs Server meldet.</span><span class="sxs-lookup"><span data-stu-id="c948a-137">This means that each System Center agent essentially discovers itself and reports its existence to the Central Management Server.</span></span> <span data-ttu-id="c948a-138">Die Verwendung der Ermittlung auf Computerebene vereinfacht die Verwaltung ihrer System Center-Infrastruktur und ermöglicht auch die Koexistenz unterschiedlicher Versionen der lync Server-Management Packs (beispielsweise Management Packs für lync Server 2010 und Management Packs für lync Server 2013).</span><span class="sxs-lookup"><span data-stu-id="c948a-138">Using machine-level discovery simplifies administration of your System Center infrastructure and also allows different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist.</span></span>

<span data-ttu-id="c948a-139"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c948a-139"></div>

<span> </span>

</div>

</div>

</span></span></div>

