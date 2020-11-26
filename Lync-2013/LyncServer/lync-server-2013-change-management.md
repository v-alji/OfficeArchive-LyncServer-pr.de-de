---
title: 'Lync Server 2013: Änderungsverwaltung'
description: 'Lync Server 2013: Änderungsverwaltung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Change management
ms:assetid: 73c774f5-c12f-4c72-be73-e07dc745b994
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720336(v=OCS.15)
ms:contentKeyID: 63969618
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69ea019f6366528c40b60a39ca8b646b49b336b0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435126"
---
# <a name="change-management-in-lync-server-2013"></a><span data-ttu-id="d0c3c-103">Änderungsverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d0c3c-103">Change management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d0c3c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d0c3c-104">

<span> </span></span></span>

<span data-ttu-id="d0c3c-105">_**Letztes Änderungsdatum des Themas:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="d0c3c-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="d0c3c-106">Änderungen an der IT-Umgebung sind unvermeidlich.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-106">Changes to the IT environment are unavoidable.</span></span> <span data-ttu-id="d0c3c-107">Zu den Änderungen gehören neue Technologien, Systeme, Anwendungen, Hardware, Tools, Prozesse und Änderungen an Rollen und Zuständigkeiten.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-107">Changes include new technologies, systems, applications, hardware, tools, processes, and changes in roles and responsibilities.</span></span> <span data-ttu-id="d0c3c-108">Mit einem effektiven Änderungsverwaltungssystem können Sie Änderungen an der IT-Umgebung schnell und mit minimaler Dienstunterbrechung einführen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-108">An effective change management system lets you introduce changes to the IT environment quickly and with minimal service disruption.</span></span> <span data-ttu-id="d0c3c-109">Ein Change Management System führt die Teams zusammen, die an der Änderung eines Systems beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-109">A change management system brings together the teams involved in changing a system.</span></span> <span data-ttu-id="d0c3c-110">Beispielsweise die Entscheidung, die Vorteile der Office Web Apps zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-110">For example, deciding to take advantage of the Office Web Apps.</span></span> <span data-ttu-id="d0c3c-111">Hierbei handelt es sich um eine integrierte lync-Dienstanwendung, mit der Benutzer Dokumente in einem Browser lesen und bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-111">This is an integrated Lync Service application that enables users to read and edit documents in a browser.</span></span> <span data-ttu-id="d0c3c-112">Die Implementierung dieses Diensts erfordert, nachdem Sie die Produktion durchlaufen haben, die Einbindung mehrerer Teams:</span><span class="sxs-lookup"><span data-stu-id="d0c3c-112">The implementation of this service, after you have gone into production, requires the involvement of several teams:</span></span>

  - <span data-ttu-id="d0c3c-113">**Test Team**   Diese Team Auslastung testet die Office Web Apps auf einem Testserver, wobei Informationen zu den erwarteten Verwendungsmustern und der erwarteten Leistung der Produktionsserver bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-113">**Test Team**   This team load-tests the Office Web Apps on a test server, in the process providing information about the expected usage patterns and expected performance of the production servers.</span></span>

  - <span data-ttu-id="d0c3c-114">**Lync-Administratoren**   Dieses Team ermittelt die Bereitstellungsstrategie und erstellt Skripts für die Installation, sofern dies möglich war.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-114">**Lync Administrators**   This team determines the deployment strategy and scripts the installation where it was possible.</span></span> <span data-ttu-id="d0c3c-115">Das Team ist dafür verantwortlich, sicherzustellen, dass die Änderung in der Produktionsumgebung bereitgestellt wird, und ist danach für die Verwaltung verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-115">The team is responsible for making sure that the change is deployed on the production environment, and it is responsible for administration afterward.</span></span> <span data-ttu-id="d0c3c-116">Das Team muss die Auswirkungen der Änderungen verstehen und in Verfahren einbeziehen, bevor die Änderungen in die Produktion übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-116">The team must understand the effect of the changes and incorporate them in procedures before the changes are put into production</span></span>

  - <span data-ttu-id="d0c3c-117">**Netzwerk Team**   Dieses Team ist für Änderungen an Firewallregeln verantwortlich, die den Zugriff aus dem Internet auf die internen lync-Pool Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-117">**Network Team**   This team is responsible for changes to firewall rules that allow access from the Internet to the internal Lync pool servers.</span></span> <span data-ttu-id="d0c3c-118">Das Team ist auch für die Zusammenarbeit mit den lync-Administratoren verantwortlich, um sicherzustellen, dass die verfügbare Bandbreite die zusätzliche Last unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-118">The team is also responsible in working with the Lync administrators for making sure that the available bandwidth can support the additional load.</span></span>

  - <span data-ttu-id="d0c3c-119">**Sicherheits Team**   Dieses Team bewertet die Sicherheit und minimiert Risiken.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-119">**Security Team**   This team assesses security and minimizes risks.</span></span> <span data-ttu-id="d0c3c-120">Das Sicherheitsteam muss bekannte Sicherheitsanfälligkeiten überprüfen und sicherstellen, dass Sicherheitsrisiken minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-120">The security team must review known vulnerabilities and help ensure that security risks are minimized.</span></span>

  - <span data-ttu-id="d0c3c-121">**Benutzerakzeptanz Team**   Dieses Team besteht aus Benutzern, die bereit sind, das System zu testen und Feedback zu Verbesserungen anzubieten.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-121">**User Acceptance Team**   This team is composed of users who are willing to test the system and offer feedback for improvements.</span></span>

<span data-ttu-id="d0c3c-122">Der Change Management-Prozess definiert die Zuständigkeiten der einzelnen Teams und plant die auszuführende Arbeit, wobei die erforderlichen Prüfungen und Tests integriert werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-122">The change management process defines the responsibilities of each team and schedules the work to be performed, incorporating checks and tests where they are required.</span></span> <span data-ttu-id="d0c3c-123">Die Steuerelemente für Änderungen variieren abhängig von der Komplexität und dem erwarteten Effekt einer Änderung.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-123">Change controls will vary depending on the complexity and expected effect of a change.</span></span> <span data-ttu-id="d0c3c-124">Sie können von der automatischen Genehmigung für geringfügige Änderungen, über Änderungs Überprüfungs Besprechungen bis hin zu vollständigen Bewertungen auf Projektebene variieren.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-124">They can vary from automatic approval of minor changes, to change review meetings, to full project-level reviews.</span></span> <span data-ttu-id="d0c3c-125">Um dies besser zu erklären, werden die Gruppen von Änderungen in diesem Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-125">To explain this better, the groups of changes are discussed in this section.</span></span>

  - <span data-ttu-id="d0c3c-126">**Wichtige Änderungen**   Größere Änderungen haben eine globale Auswirkung auf das System und erfordern möglicherweise Eingaben von verschiedenen Teams.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-126">**Major Changes**   Major changes have a global effect on the system and may require input from various teams.</span></span> <span data-ttu-id="d0c3c-127">Ein Beispiel hierfür ist das Upgrade auf lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-127">An example of this is upgrading to Lync Server 2013.</span></span> <span data-ttu-id="d0c3c-128">Wichtige Änderungen betreffen viele Teams und möglicherweise andere Systeme.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-128">Major changes affect many teams and perhaps different systems.</span></span> <span data-ttu-id="d0c3c-129">Der Change Management-Prozess umfasst wahrscheinlich eine oder mehrere Änderungs Überprüfungs Besprechungen, um die Teams zu informieren, die an der Änderung beteiligt sind oder von der Änderung betroffen sein werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-129">The change management process will probably include one or more change review meetings to inform the teams that will be involved in the change or be affected by the change.</span></span>

  - <span data-ttu-id="d0c3c-130">**Signifikante Änderungen**   Wesentliche Änderungen erfordern erhebliche Ressourcen, um zu planen, zu erstellen und zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-130">**Significant Changes**   Significant changes require significant resources to plan, build, and implement.</span></span> <span data-ttu-id="d0c3c-131">Es sollten geeignete Änderungs Steuerelemente eingeführt werden, um sicherzustellen, dass die Auswirkungen der Änderung verstanden werden, Bereitstellungsverfahren getestet und die Rollback-und Notfallpläne bereit sind.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-131">Appropriate change controls should be introduced to help make ensure that the effect of the change is understood, deployment procedures are tested, and the rollback and contingency plans are ready.</span></span> <span data-ttu-id="d0c3c-132">Ein Beispiel für eine wesentliche Änderung ist die Bereitstellungeines neuen kumulativen Updates.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-132">An example of a significant change is deploying a new cumulative update.</span></span>

  - <span data-ttu-id="d0c3c-133">**Geringfügige Änderungen**   Geringfügige Änderungen haben keine nennenswerten Auswirkungen auf die IT-Umgebung, beispielsweise das Ändern bestimmter lync-Richtlinien über die Microsoft lync Server 2013-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-133">**Minor Changes**   Minor changes do not significantly affect the IT environment, for example, changing certain Lync policies via the Microsoft Lync Server 2013 Control Panel.</span></span>

  - <span data-ttu-id="d0c3c-134">**Standard Änderungen**   Standard Änderungen werden regelmäßig durchgeführt und sind gut verstanden und dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-134">**Standard Changes**   Standard changes are performed regularly and are well understood and documented.</span></span> <span data-ttu-id="d0c3c-135">Der Change Management-Prozess sollte alle Änderungen an den Prozeduren überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-135">The change management process should review all changes to the procedures.</span></span> <span data-ttu-id="d0c3c-136">Es sollte nicht für Routineänderungen wie das Erstellen einer Inhaltsdatenbank oder das Hinzufügen eines Benutzers benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-136">It should not be needed for routine changes like creating a content database or adding a user.</span></span>

<span data-ttu-id="d0c3c-137">Im folgenden Beispiel für die Änderungsverwaltung wird untersucht, wie verschiedene Teams interagieren und welche Aktionen ausgeführt werden, wenn ein neues Service Pack bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-137">The following example of change management examines how different teams interact and the actions that are performed when a new service pack is deployed.</span></span> <span data-ttu-id="d0c3c-138">Diese Aktionen werden vom Change Management-Prozess organisiert und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-138">These actions are organized and managed by the change management process.</span></span>

  - <span data-ttu-id="d0c3c-139">**Auslösen einer Änderungsanforderung**   Das Sicherheitsteam hat das neueste Service Pack bewertet und bestätigt, dass es eine mögliche Sicherheitsanfälligkeit im Produktionssystem behebt.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-139">**Raise a change request**   The security team has assessed the latest service pack and confirmed that it resolves a possible vulnerability in the production system.</span></span> <span data-ttu-id="d0c3c-140">Das Team löst eine Änderungsanforderung aus, damit das neue kumulative Update auf alle Server angewendet wird, auf denen lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-140">The team raises a change request to have the new cumulative update applied to all servers that are running Lync Server.</span></span>

  - <span data-ttu-id="d0c3c-141">**Übersicht über das Service Pack-Versionshinweise**   Das lync-Administrator Team überprüft die Service Pack-Versionshinweise, um die Auswirkungen auf das System zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-141">**Service pack release notes review**   The Lync administrator team reviews the service pack release notes to identify the effect on the system.</span></span>

  - <span data-ttu-id="d0c3c-142">**Eine Reihe von Lab-Tests wird durchgeführt**   Das lync-Administrator Team muss Test Updates auf einem Server in einer Testumgebung durchführen, um zu entscheiden, ob das Service Pack erfolgreich angewendet werden kann, ohne die installierten Anwendungen und Server Systeme zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-142">**A series of lab tests is performed**   The Lync administrator team must perform test updates on a server in a test environment to decide whether the service pack can be applied successfully without affecting any of the installed applications and server systems.</span></span> <span data-ttu-id="d0c3c-143">Wenn es sich um von Drittanbietern oder intern erstellte Anwendungen handelt, die eine Schnittstelle zu lync Server in einer Produktionsumgebung aufweisen, sollten diese ebenfalls getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-143">If there are third-party or internally created applications that interface with Lync Server in a production environment, these should be also tested.</span></span> <span data-ttu-id="d0c3c-144">Diese Tests können auch verwendet werden, um die Zeit zu schätzen, die für die Ausführung der Upgrades erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-144">These tests can also be used to estimate the time that is required to perform the upgrades.</span></span>

  - <span data-ttu-id="d0c3c-145">**Benutzer werden über den Ausfall informiert**   Das lync-Administrator Team, das Kommunikationsteam oder der Benutzer Helpdesk informiert alle betroffenen Benutzer über den geplanten Wartungszyklus und darüber, wie lange der Dienst nicht verfügbar sein wird.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-145">**Users are informed of the outage**   The Lync administrator team, communications team, or user help desk informs all affected users about the planned maintenance cycle and how long the service will be unavailable.</span></span>

  - <span data-ttu-id="d0c3c-146">**Vor dem Upgrade wird eine vollständige Sicherung von lync durchgeführt**   .   Das lync-Administrator Team muss überprüfen, ob eine gültige Sicherung vorhanden ist, die verwendet werden kann, um zum ursprünglichen Systemzustand zurückzukehren, wenn die Service Pack-Installation fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-146">**A full backup of Lync is performed before the upgrade**   The Lync administrator team must verify that there is a valid backup that can be used to revert to the original system state if the service pack installation fails.</span></span> <span data-ttu-id="d0c3c-147">Wir empfehlen, dass die Sicherung auf einem Standbyserver wiederhergestellt wird, damit dieses System bei Problemen problemlos zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-147">We recommend that the backup be restored to a standby server to have this system readily available if there are issues.</span></span>

  - <span data-ttu-id="d0c3c-148">**Das kumulative Update wird bereitgestellt**   .   Das lync-Administrator Team führt die Installation während des geplanten Wartungszyklus durch.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-148">**The cumulative update is deployed**   The Lync administrator team does the installation during the planned maintenance cycle.</span></span>

<div>

## <a name="managing-the-timing-of-changes"></a><span data-ttu-id="d0c3c-149">Verwalten der Anzeigedauer von Änderungen</span><span class="sxs-lookup"><span data-stu-id="d0c3c-149">Managing the timing of changes</span></span>

<span data-ttu-id="d0c3c-150">Wir empfehlen, dass Sie eine Vorgehensweise zum Planen von Änderungen implementieren, um Unterbrechungen in überlappenden Abschnitten ihrer Arbeit zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-150">We recommend that you implement a procedure for scheduling changes to avoid disruptions in overlapping sections of your work.</span></span> <span data-ttu-id="d0c3c-151">So können beispielsweise zwei Teams eine geringfügige Änderung an einem System planen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-151">For example, two teams may both be planning a minor change to a system.</span></span> <span data-ttu-id="d0c3c-152">Ein Team kann ein kumulatives Update in einem Pool anwenden, während ein anderes Team ältere Benutzer in diesen Pool migriert.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-152">One team may be applying a cumulative update on a pool while another team is migrating legacy users into that pool.</span></span> <span data-ttu-id="d0c3c-153">Keines der Teams ist von den Änderungen betroffen, die das andere Team plant, und jedes Team weiß möglicherweise nicht unbedingt, welche Änderungen das andere Team plant.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-153">Neither team is affected by the changes that the other team is planning, and each team may not necessarily know about changes that the other team is planning.</span></span> <span data-ttu-id="d0c3c-154">Wenn beide Änderungen gleichzeitig aufgetreten sind, gibt es möglicherweise Probleme beim Implementieren der Änderungen.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-154">If both changes occurred at the same time, there might be issues implementing the changes.</span></span> <span data-ttu-id="d0c3c-155">Wenn nach dem Anwenden der Änderungen Probleme auftreten, beispielsweise wenn die Benutzermigration fehlschlägt, ist es möglicherweise schwierig, zu entscheiden, welche Änderung zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-155">Also, if there are issues after the changes were applied, for example, if the user migration fails, it may be difficult to decide which change should be rolled back.</span></span> <span data-ttu-id="d0c3c-156">Es sollten regelmäßige Wartungszeiten zwischen IT und Verwaltung eingerichtet werden, um die Änderungen zu testen und zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d0c3c-156">There should be regular maintenance periods set up between IT and management to test the changes and accept them.</span></span>

<span data-ttu-id="d0c3c-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d0c3c-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

