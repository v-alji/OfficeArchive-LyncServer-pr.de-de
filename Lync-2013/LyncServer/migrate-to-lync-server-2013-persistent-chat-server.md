---
title: Migration von Lync Server 2010-Gruppenchat oder Office Communications Server 2007 R2-Gruppenchat zu Lync Server 2013 Persistent Chat Server
description: Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013, beständiger Chat Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446857"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="c369c-103">Migration von Lync Server 2010-Gruppenchat oder Office Communications Server 2007 R2-Gruppenchat zu Lync Server 2013 Persistent Chat Server</span><span class="sxs-lookup"><span data-stu-id="c369c-103">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c369c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c369c-104">

<span> </span></span></span>

<span data-ttu-id="c369c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="c369c-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="c369c-106">Die Themen in diesem Abschnitt führen Sie durch den Vorgang zum Migrieren von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server.</span><span class="sxs-lookup"><span data-stu-id="c369c-106">The topics in this section guide you through the process of migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="c369c-107">Wenn Sie beabsichtigen, dass die Bereitstellung 2013 des beständigen Chat Servers mit einer lync Server 2010-, Gruppen-Chat-oder Office Communications Server 2007 R2-Gruppen-Chat-Bereitstellung koexistieren soll, enthält dieser Leitfaden auch einige wichtige Informationen zum Betrieb in dieser gemischten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c369c-107">If you intend for your Lync Server 2013, Persistent Chat Server deployment to coexist with a Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat deployment, this guide also includes some essential information for operating in this mixed environment.</span></span> <span data-ttu-id="c369c-108">Dieser Leitfaden befasst sich in erster Linie mit der Datenmigration für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="c369c-108">This guide primarily focuses on data migration for Persistent Chat Server.</span></span> <span data-ttu-id="c369c-109">Informationen zu Benutzern, die von älteren Versionen von lync Server zu lync Server 2013 migrieren, finden Sie unter [Migration von lync Server 2010 zu lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) und [Migration von Office Communications Server 2007 R2 zu lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="c369c-109">For users who are migrating from legacy versions of Lync Server to Lync Server 2013, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c369c-110">In diesem Thema wird davon ausgegangen, dass Sie lync Server 2013 bereits in Koexistenz mit lync Server 2010 oder Office Communications Server 2007 R2 installiert haben.</span><span class="sxs-lookup"><span data-stu-id="c369c-110">This topic assumes that you have already installed Lync Server 2013 in coexistence with Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c369c-111">In diesem Leitfaden werden die Schritte beschrieben, die in der Regel für die einzelnen Migrationsphasen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c369c-111">This guide describes the steps generally required to accomplish each phase of migration.</span></span> <span data-ttu-id="c369c-112">Sie bezieht sich nicht auf jede mögliche Legacy Bereitstellungstopologie oder alle möglichen Migrationsszenarien.</span><span class="sxs-lookup"><span data-stu-id="c369c-112">It does not address every possible legacy deployment topology or every possible migration scenario.</span></span> <span data-ttu-id="c369c-113">Daher müssen Sie möglicherweise nicht alle beschriebenen Schritte ausführen, oder Sie müssen abhängig von Ihrer Bereitstellung möglicherweise zusätzliche Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="c369c-113">Therefore, you may not need to perform every step that is described, or you may need to perform additional steps, depending on your deployment.</span></span> <span data-ttu-id="c369c-114">Der Leitfaden enthält auch Beispiele für Überprüfungsschritte.</span><span class="sxs-lookup"><span data-stu-id="c369c-114">The guide also provides examples of verification steps.</span></span> <span data-ttu-id="c369c-115">Diese Überprüfungsschritte werden bereitgestellt, um Ihnen zu verdeutlichen, was Sie suchen müssen, um sicherzustellen, dass jede Phase erfolgreich abgeschlossen wird, während Sie Ihre Migration fortführen.</span><span class="sxs-lookup"><span data-stu-id="c369c-115">These verification steps are provided to help you understand what you need to look for to be sure that each phase completes successfully as you progress through your migration.</span></span> <span data-ttu-id="c369c-116">Sie können diese Überprüfungsschritte für Ihren spezifischen Migrationsprozess ändern.</span><span class="sxs-lookup"><span data-stu-id="c369c-116">You can modify these verification steps to your specific migration process.</span></span>



</div>

<span data-ttu-id="c369c-117">Dieses Handbuch enthält Informationen, die speziell für das Upgrade Ihrer vorhandenen Bereitstellung gelten.</span><span class="sxs-lookup"><span data-stu-id="c369c-117">This guide provides information specific to upgrading your existing deployment.</span></span> <span data-ttu-id="c369c-118">Es wird nicht erläutert, wie Sie Ihre vorhandene Topologie ändern.</span><span class="sxs-lookup"><span data-stu-id="c369c-118">It does not explain how to change your existing topology.</span></span> <span data-ttu-id="c369c-119">In diesem Leitfaden wird die Implementierung neuer Features nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="c369c-119">This guide does not cover the implementation of new features.</span></span> <span data-ttu-id="c369c-120">Wenn eine detaillierte Prozedur an anderer Stelle dokumentiert wird, werden Sie in diesem Leitfaden zu dem entsprechenden Dokument-oder Dokumentabschnitt weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="c369c-120">When a detailed procedure is documented elsewhere, this guide directs you to the appropriate document or document section.</span></span>

<span data-ttu-id="c369c-121">In diesem Dokument werden die in der folgenden Liste angegebenen Ausdrücke definiert.</span><span class="sxs-lookup"><span data-stu-id="c369c-121">This document defines terms as specified in the following list.</span></span>

  - <span data-ttu-id="c369c-122">*Migrations*</span><span class="sxs-lookup"><span data-stu-id="c369c-122">*migration*</span></span>  
    <span data-ttu-id="c369c-123">Verschieben der Bereitstellung aus einer früheren Version des beständigen Chat Servers (vormals als Gruppen-Chat Server bezeichnet) zu lync Server 2013, beständiger Chat Server</span><span class="sxs-lookup"><span data-stu-id="c369c-123">Moving your deployment from a previous version of Persistent Chat Server, formerly known as Group Chat Server, to Lync Server 2013, Persistent Chat Server.</span></span>

<!-- end list -->

  - <span data-ttu-id="c369c-124">*Upgrade*</span><span class="sxs-lookup"><span data-stu-id="c369c-124">*upgrade*</span></span>  
    <span data-ttu-id="c369c-125">Installieren einer neueren Software Version auf einem Server oder Clientcomputer</span><span class="sxs-lookup"><span data-stu-id="c369c-125">Installing a newer version of software on a server or client computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c369c-126">*Koexistenz*</span><span class="sxs-lookup"><span data-stu-id="c369c-126">*coexistence*</span></span>  
    <span data-ttu-id="c369c-127">Die temporäre Umgebung, die während der Migration vorhanden ist, wenn einige Funktionen zu lync Server 2013, beständiger Chat Server migriert wurden und andere Funktionen weiterhin auf einer früheren Version des Gruppen Chat Servers verbleiben.</span><span class="sxs-lookup"><span data-stu-id="c369c-127">The temporary environment that exists during migration, when some functionality has been migrated to Lync Server 2013, Persistent Chat Server, and other functionality still remains on a prior version of Group Chat Server.</span></span>

<span data-ttu-id="c369c-128">Der beständige Chat Server ist eine Erweiterung der lync Server 2013-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="c369c-128">Persistent Chat Server is an extension of the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="c369c-129">Je nach Topologie können Sie lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013-beständigen Chat Server migrieren.</span><span class="sxs-lookup"><span data-stu-id="c369c-129">Depending on your topology, you can migrate Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013 Persistent Chat Server.</span></span> <span data-ttu-id="c369c-130">Details zu verfügbaren Topologien und den technischen und Softwareanforderungen für die Migration des Gruppen-Chat Servers finden Sie unter [Planen des beständigen Chat Servers in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c369c-130">For details about available topologies and the technical and software requirements for migrating Group Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="c369c-131">Wenn Ihre Organisation Compliance-Unterstützung erfordert, wird Sie jetzt automatisch mit jedem beständigen Chat Server installiert.</span><span class="sxs-lookup"><span data-stu-id="c369c-131">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="c369c-132">Für die Compliance wird kein separater Server mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="c369c-132">A separate server is no longer needed for compliance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c369c-133">Der Server für beständigen Chat muss auf einem NTFS-Dateisystem installiert sein, um die Dateisystemsicherheit zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c369c-133">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="c369c-134">FAT32 ist kein unterstütztes Dateisystem für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="c369c-134">FAT32 is not a supported file system for Persistent Chat Server.</span></span><BR><span data-ttu-id="c369c-135">Wenn Ihre Organisation Compliance-Unterstützung erfordert, wird Sie jetzt automatisch mit jedem beständigen Chat Server installiert.</span><span class="sxs-lookup"><span data-stu-id="c369c-135">If your organization requires compliance support, it is now automatically installed with each Persistent Chat Server.</span></span> <span data-ttu-id="c369c-136">Für die Compliance wird kein separater Server mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="c369c-136">A separate server is no longer needed for compliance.</span></span> <span data-ttu-id="c369c-137">Weitere Informationen zu Änderungen in lync Server 2013 &nbsp; -Server für beständigen Chat finden Sie unter <A href="lync-server-2013-new-persistent-chat-server-features.md">neue beständige Chat Server Features in lync Server 2013</A> in der Dokumentation "erste Schritte".</span><span class="sxs-lookup"><span data-stu-id="c369c-137">For more details about changes in Lync Server 2013&nbsp;Persistent Chat Server, see <A href="lync-server-2013-new-persistent-chat-server-features.md">New Persistent Chat Server features in Lync Server 2013</A> in the Getting Started documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c369c-138">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c369c-138">In This Section</span></span>

  - [<span data-ttu-id="c369c-139">Standardmigrationsszenario – Übersicht</span><span class="sxs-lookup"><span data-stu-id="c369c-139">Standard migration scenario - high-level</span></span>](standard-migration-scenario-high-level.md)

  - [<span data-ttu-id="c369c-140">Migrationsprozess – Details</span><span class="sxs-lookup"><span data-stu-id="c369c-140">Migration process - details</span></span>](migration-process-details.md)

  - [<span data-ttu-id="c369c-141">Überlegungen zur Koexistenz</span><span class="sxs-lookup"><span data-stu-id="c369c-141">Coexistence considerations</span></span>](coexistence-considerations.md)

<span data-ttu-id="c369c-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c369c-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

