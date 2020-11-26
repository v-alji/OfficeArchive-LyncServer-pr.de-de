---
title: 'Lync Server 2013: Integritäts Konfiguration in lync Server'
description: 'Lync Server 2013: Integritäts Konfiguration in lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Health configuration in Lync Server 2013
ms:assetid: c00a8c8e-c2d2-4557-8c42-211c7cc96550
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205234(v=OCS.15)
ms:contentKeyID: 48185305
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 999a6d5401cb34382a4120f9255c91c846f72422
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427648"
---
# <a name="health-configuration-in-lync-server-2013"></a><span data-ttu-id="32409-103">Integritäts Konfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32409-103">Health configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32409-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32409-104">

<span> </span></span></span>

<span data-ttu-id="32409-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="32409-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="32409-106">Zwischen verschiedenen Websites, Microsoft Knowledge Base-Artikeln und lync Server Resource Kit-Tools sind Administratoren, die Probleme bei der Ausführung von lync Server haben, nie weit davon entfernt, diese Probleme zu lösen.</span><span class="sxs-lookup"><span data-stu-id="32409-106">Between various websites, Microsoft Knowledge Base articles, and Lync Server Resource Kit tools, administrators who encounter problems when running Lync Server are never far from a way to solve those problems.</span></span>

<span data-ttu-id="32409-107">Es gibt natürlich keine Möglichkeit, sicherzustellen, dass Sie nie Probleme mit lync Server 2013 haben, da lync Server von vielen Dingen wie Netzwerk abstürzen und Hardwarefehlern betroffen sein kann, die das Produkt selbst nicht kontrollieren kann.</span><span class="sxs-lookup"><span data-stu-id="32409-107">Obviously there is no way to guarantee that you will never encounter problems with Lync Server 2013 because Lync Server can be affected by many things—like network crashes and hardware failures—that the product itself cannot control.</span></span> <span data-ttu-id="32409-108">Durch die Implementierung der Integritätsüberwachung können Administratoren potenzielle Probleme erkennen, bevor Sie zu tatsächlichen Problemen werden.</span><span class="sxs-lookup"><span data-stu-id="32409-108">By implementing health monitoring, administrators can identify potential problems before they turn into actual problems.</span></span> <span data-ttu-id="32409-109">Administratoren können beispielsweise mithilfe der lync Server-Überwachung Trends und Tendenzen erkennen.</span><span class="sxs-lookup"><span data-stu-id="32409-109">For example, administrators can use Lync Server monitoring to identify trends and tendencies.</span></span> <span data-ttu-id="32409-110">Eine stetige Zunahme der Anzahl von Audio-und Videokonferenzen könnte beispielsweise darauf hindeuten, dass Kapazität hinzugefügt werden muss, bevor das System überladen wird.</span><span class="sxs-lookup"><span data-stu-id="32409-110">For example, a steady increase in the number of audio/video conferences might suggest a need to add capacity before the system becomes overloaded.</span></span>

<span data-ttu-id="32409-111">Auf ähnliche Weise können Administratoren System Center Operations Manager verwenden, um in Echtzeit Warnungen zu erhalten, wenn bestimmte Ereignisse auftreten, und synthetische Transaktionen auszuführen, die das System proaktiv testen.</span><span class="sxs-lookup"><span data-stu-id="32409-111">In a similar fashion, administrators can use System Center Operations Manager to do such things as issue real-time alerts when specified events occur, and to run synthetic transactions that proactively test the system.</span></span> <span data-ttu-id="32409-112">Synthetische Transaktionen werden in lync Server verwendet, um sicherzustellen, dass Benutzer häufige Aufgaben wie die Anmeldung am System, den Austausch von Sofortnachrichten oder Anrufe an ein Telefon im öffentlichen Telefonnetz (PSTN) erfolgreich durchführen können.</span><span class="sxs-lookup"><span data-stu-id="32409-112">Synthetic transactions are used in Lync Server to verify that users are able to successfully complete common tasks such as logging on to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="32409-113">So können Sie beispielsweise in regelmäßigen Abständen mithilfe dieser Tests auf mögliche Probleme bei der Anmeldung von Benutzern bei lync Server hingewiesen werden, und Sie erhalten eine Möglichkeit, das Problem zu beheben, bevor das Support Team mit Anrufen von Benutzern überflutet wird, die keine Verbindung herstellen können.</span><span class="sxs-lookup"><span data-stu-id="32409-113">For example, periodically running these tests can alert you to potential problems with users logging on to Lync Server, and give you a chance to correct the problem before your support team is flooded with calls from users unable to make a connection.</span></span> <span data-ttu-id="32409-114">Durch die Verwendung von System Center Operations Manager zum Ausführen dieser synthetischen Transaktionen können Administratoren ihre Bereitstellung von lync Server täglich 24 Stunden lang kontinuierlich überwachen, ohne über eine Antwort auf mögliche Warnungen zu verfügen, die möglicherweise ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="32409-114">By using System Center Operations Manager to run these synthetic transactions, administrators can routinely monitor their deployment of Lync Server continuously for 24 hours every day without having to do much of anything beyond responding to any alerts that might be issued.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="32409-115">Für lync Server 2013 ist das Management Pack für System Center Operations Manager auch in der Lage, "externe" Probleme zu erkennen, die sich negativ auf lync Server auswirken können.</span><span class="sxs-lookup"><span data-stu-id="32409-115">For Lync Server 2013, the Management Pack for System Center Operations Manager is also able to detect "external" issues that can adversely affect Lync Server.</span></span> <span data-ttu-id="32409-116">Beispielsweise können Administratoren benachrichtigt werden, wenn Internet Informationsdienste (IIS) offline geschaltet werden, Systemressourcen auf einem lync Server-Computer unter einen bestimmten Betrag fallen oder ein Hardwarefehler bei einem lync Server-Computer auftritt.</span><span class="sxs-lookup"><span data-stu-id="32409-116">For example, administrators can be notified if Internet Information Services (IIS) goes offline, system resources on a Lync Server computer fall below a specified amount, or a Lync Server computer experiences a hardware failure.</span></span>



</div>

<span data-ttu-id="32409-117">Die Integritäts Konfiguration in lync Server 2013 basiert auf System Center Operations Manager und der Verwendung von lync Server-Verwaltungs Paketen.</span><span class="sxs-lookup"><span data-stu-id="32409-117">Health configuration in Lync Server 2013 is built around System Center Operations Manager and the use of Lync Server Management Packs.</span></span> <span data-ttu-id="32409-118">Diese Management Packs umfassen eine Reihe neuer Features und Verbesserungen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="32409-118">These Management Packs include a number of new features and enhancements, including:</span></span>

  - <span data-ttu-id="32409-119">**Verfügbarkeit von Szenarien von einem beliebigen Ort aus.**</span><span class="sxs-lookup"><span data-stu-id="32409-119">**Scenario availability from any location.**</span></span> <span data-ttu-id="32409-120">Das lync Server 2010-Management Pack hat das Konzept der Überwachung der Verfügbarkeit von Endbenutzerszenarien mit synthetischen Transaktionen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="32409-120">The Lync Server 2010 Management Pack introduced the concept of monitoring end user scenario availability with synthetic transactions.</span></span> <span data-ttu-id="32409-121">In lync Server 2013 verfügen diese Agents über mehr synthetische Transaktionen und können von einer Vielzahl von Speicherorten innerhalb des Unternehmens, von Remote-geografischen Standorten außerhalb des Unternehmens, mit Zweigstellen-Appliances und gegen lync Server 2010-Bereitstellungen ausgeführt werden, um eine Abdeckung für Legacy-Edge-Bereitstellungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="32409-121">In Lync Server 2013, these agents have more synthetic transactions and can be run from a variety of locations inside the enterprise, from remote geographic locations outside of the enterprise, against branch office appliances and against Lync Server 2010 deployments to add coverage to legacy Edge deployments.</span></span>

  - <span data-ttu-id="32409-122">**Synthetische Transaktionsprotokolle.**</span><span class="sxs-lookup"><span data-stu-id="32409-122">**Synthetic transaction logs.**</span></span> <span data-ttu-id="32409-123">Wenn eine synthetische Transaktion fehlschlägt, können Administratoren auf HTML-Protokolle zugreifen, um zu ermitteln, welche Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="32409-123">When a synthetic transaction fails, administrators have access to HTML logs to help determine what failed.</span></span> <span data-ttu-id="32409-124">Dies umfasst das Verständnis der fehlgeschlagenen Aktion, die Latenz der einzelnen Aktionen, die für die Ausführung des Tests verwendete Befehlszeile und der aufgetretene Fehler.</span><span class="sxs-lookup"><span data-stu-id="32409-124">This includes understanding which action failed, the latency of each action, the command-line used to run the test, and the error that was encountered.</span></span>

  - <span data-ttu-id="32409-125">**Erhöhte Anruf Zuverlässigkeit.**</span><span class="sxs-lookup"><span data-stu-id="32409-125">**Increased call reliability coverage.**</span></span> <span data-ttu-id="32409-126">Das lync Server 2010-Management Pack führte zu einer Anruf Zuverlässigkeits Warnung, um schwerwiegende Verbindungsprobleme zu erkennen, die sich auf die Audioanrufe von Endbenutzern auswirken.</span><span class="sxs-lookup"><span data-stu-id="32409-126">The Lync Server 2010 Management Pack introduced call reliability alerting to detect severe connectivity issues that affect the audio calls of end users.</span></span> <span data-ttu-id="32409-127">Die lync Server 2013-Verwaltungspakete bieten eine Abdeckung für Peer-to-Peer-Instant Messaging (im) und andere grundlegende Konferenzfeatures, um die Abdeckung zu maximieren und gleichzeitig Rauschen zu verringern.</span><span class="sxs-lookup"><span data-stu-id="32409-127">The Lync Server 2013 Management Packs add coverage for peer-to-peer instant messaging (IM) and other basic conferencing features to maximize coverage while reducing noise.</span></span>

  - <span data-ttu-id="32409-128">**Abhängigkeitsüberwachung.**</span><span class="sxs-lookup"><span data-stu-id="32409-128">**Dependency monitoring.**</span></span> <span data-ttu-id="32409-129">Lync Server-Szenarien können aufgrund einer Vielzahl externer Faktoren, wie IIS offline, begrenzte CPU-und Speicherressourcen sowie Datenträgerprobleme, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="32409-129">Lync Server scenarios can fail due to a variety of external factors such as IIS being offline, limited CPU and memory resources, and disk issues.</span></span> <span data-ttu-id="32409-130">Die neuen Management Packs überprüfen verschiedene kritische Abhängigkeiten, um sicherzustellen, dass Administratoren sich ihrer Auswirkungen bewusst sind.</span><span class="sxs-lookup"><span data-stu-id="32409-130">The new management packs check several critical dependencies to ensure administrators are aware of their impact.</span></span>

  - <span data-ttu-id="32409-131">**Verbesserte Berichterstellung.**</span><span class="sxs-lookup"><span data-stu-id="32409-131">**Enhanced reporting.**</span></span> <span data-ttu-id="32409-132">Eine Reihe von Berichten, die Administratoren dabei helfen, die Verfügbarkeit von Szenarien zu schätzen, Kapazitätspläne zu planen und zu sehen, welche Komponenten die meisten Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="32409-132">A set of reports to help administrators estimate scenario availability, plan for capacity, and see which components are experiencing the most issues.</span></span>

<span data-ttu-id="32409-133">Die Management Packs beinhalten auch eine Reihe von Funktionen, die Ihnen helfen, den Status Ihrer lync Server-Bereitstellung in Echtzeit zu erkennen und zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="32409-133">The Management Packs also include a variety of features to help detect and diagnose provide real-time visibility into the health your Lync Server deployment.</span></span> <span data-ttu-id="32409-134">Diese Features sind in der folgenden Tabelle aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="32409-134">These features are listed in the following table.</span></span>

### <a name="management-pack-features"></a><span data-ttu-id="32409-135">Management Pack-Features</span><span class="sxs-lookup"><span data-stu-id="32409-135">Management Pack Features</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32409-136">Feature</span><span class="sxs-lookup"><span data-stu-id="32409-136">Feature</span></span></th>
<th><span data-ttu-id="32409-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32409-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32409-138">Synthetische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="32409-138">Synthetic Transactions</span></span></p></td>
<td><p><span data-ttu-id="32409-139">Windows PowerShell-Cmdlets, die von verschiedenen Speicherorten aus ausgeführt werden können, um sicherzustellen, dass Endbenutzerszenarien wie Anmeldung, Anwesenheit, Chat und Konferenz problemlos für Endbenutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32409-139">Windows PowerShell cmdlets that can be run from various locations to ensure that end user scenarios such as sign-in, presence, IM, and conferencing are readily available to end users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32409-140">Benachrichtigungen zur Anruf Zuverlässigkeit</span><span class="sxs-lookup"><span data-stu-id="32409-140">Call Reliability Alerts</span></span></p></td>
<td><p><span data-ttu-id="32409-141">Datenbankabfragen für Anruf Detail Datensätze (CDR).</span><span class="sxs-lookup"><span data-stu-id="32409-141">Database queries for Call Detail Records (CDR).</span></span> <span data-ttu-id="32409-142">Diese Einträge werden von Front-End-Servern geschrieben, um zu reflektieren, ob Endbenutzer eine Verbindung mit einem Anruf herstellen konnten oder warum ein Anruf beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="32409-142">These records are written by Front End Servers to reflect whether end users were able to connect to a call or why a call was terminated.</span></span> <span data-ttu-id="32409-143">Diese Abfragen führen zu Warnungen, die angeben, dass für eine breite Palette von Endbenutzern Verbindungsprobleme für Peer-to-Peer-Anrufe oder einfache Konferenzfunktionen auftreten.</span><span class="sxs-lookup"><span data-stu-id="32409-143">These queries result in alerts that indicate when a wide range of end users are experiencing connectivity issues for peer-to-peer calls or basic conferencing functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32409-144">Benachrichtigungen über Medienqualität</span><span class="sxs-lookup"><span data-stu-id="32409-144">Media Quality Alerts</span></span></p></td>
<td><p><span data-ttu-id="32409-145">Datenbankabfragen, die die von Kunden am Ende jedes Anrufs veröffentlichten QoE-Berichte (Quality of Experience) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="32409-145">Database queries that look at Quality of Experience (QoE) reports published by clients at the end of each call.</span></span> <span data-ttu-id="32409-146">Diese Abfragen führen zu Warnungen, in denen Szenarien lokalisiert werden, in denen Benutzer bei Anrufen und Konferenzen wahrscheinlich eine schlechte Medienqualität aufweisen.</span><span class="sxs-lookup"><span data-stu-id="32409-146">These queries result in alerts that pinpoint scenarios where users are likely to be experiencing poor media quality during calls and conferences.</span></span> <span data-ttu-id="32409-147">Die Daten basieren auf wichtigen Metriken wie Paket Latenz und-Verlust, Metriken, die bekanntermaßen direkt zur Anrufqualität beitragen.</span><span class="sxs-lookup"><span data-stu-id="32409-147">The data is built upon key metrics such as packet latency and loss, metrics that are known to directly contribute to call quality.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32409-148">Komponentenstatus</span><span class="sxs-lookup"><span data-stu-id="32409-148">Component Health</span></span></p></td>
<td><p><span data-ttu-id="32409-149">Einzelne Server Komponenten lösen Warnungen mithilfe von Ereignisprotokollen und Leistungsindikatoren aus.</span><span class="sxs-lookup"><span data-stu-id="32409-149">Individual server components raise alerts by using event logs and performance counters.</span></span> <span data-ttu-id="32409-150">Diese Warnungen zeigen Fehlerbedingungen an, die ein oder mehrere Endbenutzerszenarien stark beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="32409-150">These alerts indicate failure conditions that can severely impact one or more end user scenarios.</span></span> <span data-ttu-id="32409-151">Diese Benachrichtigungen können auch auf eine Vielzahl anderer Fehlerbedingungen hinweisen, einschließlich der nicht ausgeführten Dienste, der großen Fehlerraten, der großen Nachrichtenlatenz oder der Verbindungsprobleme.</span><span class="sxs-lookup"><span data-stu-id="32409-151">These alerts can also indicate a variety of other failure conditions, including services not running, high failure rates, high message latency, or connectivity issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32409-152">Abhängigkeitsstatus</span><span class="sxs-lookup"><span data-stu-id="32409-152">Dependency Health</span></span></p></td>
<td><p><span data-ttu-id="32409-153">Fehler können aus verschiedenen externen Gründen auftreten.</span><span class="sxs-lookup"><span data-stu-id="32409-153">Failures can occur for a variety of external reasons.</span></span> <span data-ttu-id="32409-154">Die Management Packs überwachen und sammeln nun Daten für einige der wichtigen externen Abhängigkeiten, die möglicherweise auf schwerwiegende Probleme hindeuten, einschließlich IIS-Verfügbarkeit, CPU-und Speicherauslastung von Servern und Prozessen sowie Datenträger Metrik.</span><span class="sxs-lookup"><span data-stu-id="32409-154">The management packs now monitor and collect data for some of the critical external dependencies that might indicate severe issues, including IIS availability, CPU and memory usage of servers and processes, and disk metrics.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32409-155">Die vom System ausgestellten Benachrichtigungen wurden in drei allgemeine Kategorien unterteilt:</span><span class="sxs-lookup"><span data-stu-id="32409-155">The alerts issued by the system have been classified into three general categories:</span></span>

  - <span data-ttu-id="32409-156">**Benachrichtigungen mit hoher Priorität.**</span><span class="sxs-lookup"><span data-stu-id="32409-156">**High-priority Alerts.**</span></span> <span data-ttu-id="32409-157">Diese Warnungen weisen auf Bedingungen hin, die zu Dienstunterbrechungen für große Benutzergruppen führen können.</span><span class="sxs-lookup"><span data-stu-id="32409-157">These alerts indicate conditions that will cause service outages for large groups of users.</span></span> <span data-ttu-id="32409-158">Beispielsweise ist ein Komponentenfehler auf einem einzelnen Computer keine Warnung mit hoher Priorität, da lync Server 2013 integrierte Funktionen für hohe Verfügbarkeit besitzt.</span><span class="sxs-lookup"><span data-stu-id="32409-158">For example, a component failure on a single machine is not a high-priority alert because Lync Server 2013 has built-in high availability features.</span></span> <span data-ttu-id="32409-159">Stattdessen stellen Benachrichtigungen mit hoher Priorität Probleme dar, die schwerwiegend genug sind, um Administratoren nachts zu wecken.</span><span class="sxs-lookup"><span data-stu-id="32409-159">Instead, high-priority alerts represent problems serious enough “to wake up administrators at night.”</span></span> <span data-ttu-id="32409-160">Ausfälle, die von synthetischen Transaktionen und Offline Diensten (beispielsweise Audio/Videokonferenzen) erkannt werden, werden als Benachrichtigungen mit hoher Priorität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32409-160">Outages detected by synthetic transactions and offline services (for example, audio/video conferencing) qualify as high-priority alerts.</span></span>

  - <span data-ttu-id="32409-161">**Benachrichtigungen mit mittlerer Priorität.**.</span><span class="sxs-lookup"><span data-stu-id="32409-161">**Medium-priority alerts.**.</span></span> <span data-ttu-id="32409-162">Diese Benachrichtigungen deuten auf Bedingungen hin, die sich auf eine Teilmenge von Benutzern auswirken oder auf die Verschlechterung der Anrufqualität hindeuten.</span><span class="sxs-lookup"><span data-stu-id="32409-162">These alerts indicate conditions that affect a subset of users or indicate call quality degradation.</span></span> <span data-ttu-id="32409-163">Dazu gehören Probleme wie Komponentenausfälle, Latenz in der Anrufeinrichtung oder beeinträchtigte Audioqualität bei anrufen.</span><span class="sxs-lookup"><span data-stu-id="32409-163">That includes problems such as component failures, latency in call establishment, or degraded audio quality in call.</span></span> <span data-ttu-id="32409-164">Benachrichtigungen in dieser Kategorie sind Stateful und geben den aktuellen Status des Problems an.</span><span class="sxs-lookup"><span data-stu-id="32409-164">Alerts in this category are stateful and indicate the current status of the issue.</span></span> <span data-ttu-id="32409-165">Nehmen wir beispielsweise an, dass Ihre Anrufzeiten den Warnungsschwellenwert überschreiten.</span><span class="sxs-lookup"><span data-stu-id="32409-165">For example, suppose your call establishment times exceed the alert threshold.</span></span> <span data-ttu-id="32409-166">Wenn die Zeiten der Anrufeinrichtung wieder normal sind, werden diese Benachrichtigungen in System Center Operations Manager automatisch aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="32409-166">If call establishment times return to normal, these alerts will be auto-resolved in System Center Operations Manager.</span></span> <span data-ttu-id="32409-167">Die Erwartung für diese Benachrichtigungen liegt darin, dass ein Administrator Sie am gleichen Arbeitstag ansieht.</span><span class="sxs-lookup"><span data-stu-id="32409-167">The expectation for these alerts is that an administrator will look at them on the same business day.</span></span>

  - <span data-ttu-id="32409-168">**Andere Benachrichtigungen.**</span><span class="sxs-lookup"><span data-stu-id="32409-168">**Other alerts.**</span></span> <span data-ttu-id="32409-169">Hierbei handelt es sich um Warnungen von Komponenten, die sich auf einen bestimmten Benutzer oder eine Teilmenge von Benutzern auswirken können.</span><span class="sxs-lookup"><span data-stu-id="32409-169">These are alerts from components that might affect a specific user or subset of users.</span></span> <span data-ttu-id="32409-170">Beispielsweise konnte der Adressbuchdienst den Active Directory-Eintrag eines bestimmten Benutzers nicht analysieren.</span><span class="sxs-lookup"><span data-stu-id="32409-170">For example, perhaps the Address Book service could not parse the Active Directory entry of a given user.</span></span> <span data-ttu-id="32409-171">Die Erwartung für diese Benachrichtigungen liegt darin, dass Administratoren darauf zugreifen können, wenn Ihnen Zeit zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="32409-171">The expectation for these alerts is that administrators will get to them when they have time available.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="32409-172">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="32409-172">In This Section</span></span>

  - [<span data-ttu-id="32409-173">Konfigurieren von lync Server 2013 für die Zusammenarbeit mit System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="32409-173">Configuring Lync Server 2013 to work with System Center Operations Manager</span></span>](lync-server-2013-configuring-lync-server-to-work-with-system-center-operations-manager.md)

  - [<span data-ttu-id="32409-174">Verwenden der umfangreichen Protokollierung für synthetische Transaktionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32409-174">Using rich logging for synthetic transactions in Lync Server 2013</span></span>](lync-server-2013-using-rich-logging-for-synthetic-transactions.md)

  - [<span data-ttu-id="32409-175">Verwenden von Microsoft SQL Server 2008 R2 als Ihre System Center Operations Manager-Datenbank für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32409-175">Using Microsoft SQL Server 2008 R2 as your System Center Operations Manager database for Lync Server 2013</span></span>](lync-server-2013-using-microsoft-sql-server-2008-r2-as-your-system-center-operations-manager-database.md)

<span data-ttu-id="32409-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32409-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

