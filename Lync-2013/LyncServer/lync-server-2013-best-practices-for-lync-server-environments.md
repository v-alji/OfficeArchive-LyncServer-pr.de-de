---
title: 'Lync Server 2013: bewährte Methoden für lync Server-Umgebungen'
description: 'Lync Server 2013: bewährte Methoden für lync Server-Umgebungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436062"
---
# <a name="best-practices-for-lync-server-2013-environments"></a><span data-ttu-id="5fb76-103">Bewährte Methoden für lync Server 2013-Umgebungen</span><span class="sxs-lookup"><span data-stu-id="5fb76-103">Best practices for Lync Server 2013 environments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5fb76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5fb76-104">

<span> </span></span></span>

<span data-ttu-id="5fb76-105">_**Letztes Änderungsdatum des Themas:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="5fb76-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="5fb76-106">Die folgenden allgemeinen Grundsätze sollten auf den laufenden Betrieb Ihres Systems angewendet werden:</span><span class="sxs-lookup"><span data-stu-id="5fb76-106">The following general principles should be applied to ongoing operations of your system:</span></span>

  - <span data-ttu-id="5fb76-107">**Verstehen und Verwenden von MOF**   MOF ist eine Sammlung von bewährten Methoden, Prinzipien und Modellen, die Unternehmen technische Anleitungen zur Verwaltung von IT-Ressourcen bereitstellen, beispielsweise tägliche lync Server 2013-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="5fb76-107">**Understand and utilize MOF**   MOF is a collection of best practices, principles, and models that provide organizations technical guidance about the management of IT assets, such as daily Lync Server 2013 operations.</span></span> <span data-ttu-id="5fb76-108">Die folgenden MOF-Richtlinien können Ihnen dabei helfen, unternehmenskritische Produktionssystem Zuverlässigkeit, Verfügbarkeit, Unterstützung und Verwaltbarkeit für Microsoft-Produkte zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="5fb76-108">Following MOF guidelines can help you achieve mission-critical production system reliability, availability, supportability, and manageability for Microsoft products.</span></span> <span data-ttu-id="5fb76-109">Weitere Informationen finden Sie unter [Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939).</span><span class="sxs-lookup"><span data-stu-id="5fb76-109">For more information, see [Microsoft Operations Framework 4.0](https://go.microsoft.com/fwlink/p/?linkid=40939).</span></span>

  - <span data-ttu-id="5fb76-110">Informationen **zu bewährten Methoden für lync Server 2013**   Wir empfehlen, praktische und bewährte Verfahren zum Verwalten von lync Server 2013 zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5fb76-110">**Learn about best practices for Lync Server 2013**   We recommend that you implement practical and proven procedures to manage Lync Server 2013.</span></span> <span data-ttu-id="5fb76-111">Durch die Verwendung von erprobten, getesteten und dokumentierten Methoden zur Verwaltung von Vorgängen ist es möglicherweise effizienter als die Entwicklung eigener Methoden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-111">By using tried, tested, and documented methods of managing operations may be more efficient than developing your own methods.</span></span>

  - <span data-ttu-id="5fb76-112">**Getrennte Vorgänge in tägliche, wöchentliche und monatliche Prozesse**   Dokumentieren Sie die erforderlichen operativen Aufgaben, die Sie regelmäßig ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-112">**Separate operations into daily, weekly, and monthly processes**   Document the required operational tasks that you'll regularly perform.</span></span> <span data-ttu-id="5fb76-113">Wenn Sie dokumentieren, wie Sie Aufgaben durchführen, können Sie sicherstellen, dass Ihre Informationen beibehalten werden, wenn sich Ihre Betriebsumgebung ändert, beispielsweise wenn neue Technologien bereitgestellt werden oder Mitarbeiter Änderungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="5fb76-113">Documenting how you perform tasks helps make sure that your information is preserved when there is a change in your operational environment such as when new technologies are deployed or staff changes occur.</span></span> <span data-ttu-id="5fb76-114">Wir empfehlen, dass operative Aufgaben in verwaltbare Arbeitslasten aufgeteilt werden, bei denen Aufgaben täglich, wöchentlich und monatlich durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-114">We recommend that operational tasks be separated into manageable workloads where tasks are performed daily, weekly, and monthly.</span></span> <span data-ttu-id="5fb76-115">Tägliche Aufgaben konzentrieren sich auf die Funktionsweise eines Systems, während sich die monatlichen Aufgaben mehr auf die Gewährleistung der langfristigen Gesundheit eines Systems konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="5fb76-115">Daily tasks would focus efforts on the functioning of a system, and monthly tasks would focus more on ensuring the long-term health of a system.</span></span>
    
    <span data-ttu-id="5fb76-116">Dieses Dokument kann in Umgebungen verwendet werden, in denen nur Instant Messaging/Anwesenheits Komponenten (im/p) bereitgestellt werden, oder im/p mit Enterprise-VoIP.</span><span class="sxs-lookup"><span data-stu-id="5fb76-116">This document can be used in environments deploying only instant messaging/presence (IM/P) components or IM/P with Enterprise Voice.</span></span> <span data-ttu-id="5fb76-117">Wenn Aufgaben oder Checklisten Elemente für Enterprise-VoIP spezifisch sind, wird dies erwähnt, und wenn Ihre Umgebung keine Enterprise-VoIP umfasst, kann der Teil übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-117">When tasks or checklist items are specific to Enterprise Voice, this is mentioned and if your environment does not include Enterprise Voice the portion may be skipped.</span></span>

  - <span data-ttu-id="5fb76-118">**Bereitstellen der für den Betrieb von lync Server 2013 erforderlichen Tools**   Es stehen viele Tools zur Verfügung, mit denen Sie Probleme behandeln, Aufgaben automatisieren und die lync Server 2013-Umgebung überwachen und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="5fb76-118">**Deploy the tools that are required for operating Lync Server 2013**   Many tools are available to help troubleshoot issues, automate tasks, and help monitor and maintain the Lync Server 2013 environment.</span></span> <span data-ttu-id="5fb76-119">Definieren Sie einen Standardsatz von Tools für Ihre Organisation, damit die Aufgaben, die vom Operations Team ausgeführt werden, genau, effizient, konsistent und auf kontrollierte Weise ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-119">Define a standard set of tools for your organization so the tasks that are performed by the operations team are performed accurately, efficiently, consistently, and in a controlled manner.</span></span> <span data-ttu-id="5fb76-120">Darüber hinaus sollten Sie Prozesse implementieren, um Vorfälle und wichtige Konfigurationsänderungen nachverfolgen zu können.</span><span class="sxs-lookup"><span data-stu-id="5fb76-120">You should also implement processes to track incidents and major configuration changes.</span></span>

<div>

## <a name="reference"></a><span data-ttu-id="5fb76-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="5fb76-121">Reference</span></span>

<span data-ttu-id="5fb76-122">Zugunsten der Leser, die nicht bereits mit den Grundlagen der Serververwaltung im allgemeinen vertraut sind, bieten wir eine Übersicht über Server Verwaltungsmethoden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-122">For the benefit of readers not already familiar with the basics of server management in general, we provide an overview of server management practices.</span></span> <span data-ttu-id="5fb76-123">Leser, die bereits mit der Serververwaltung vertraut sind, können diesen Abschnitt überspringen.</span><span class="sxs-lookup"><span data-stu-id="5fb76-123">Readers already familiar with server management may choose to skip this section.</span></span>

<span data-ttu-id="5fb76-124">Bewährte Methoden sind Empfehlungen, die auf dem Wissen und der Erfahrung basieren, die IT-Experten in vielen Umgebungen erworben haben.</span><span class="sxs-lookup"><span data-stu-id="5fb76-124">Best practices are recommendations that are based on the knowledge and experience that IT professionals have gained across many environments.</span></span> <span data-ttu-id="5fb76-125">Sie bieten Standardverfahren für typische Aufgaben, die von ihren lync Server-Administratoren täglich ausgeführt werden müssen, und listet die Tools auf, die Sie zum Verwalten einer lync Server-Umgebung verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="5fb76-125">They provide standard procedures for typical tasks that your Lync Server administrators must perform daily, and list the tools that they should use to manage a Lync Server environment.</span></span>

<span data-ttu-id="5fb76-126">Zu den typischen Aufgaben für lync-Administratoren gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5fb76-126">Typical tasks for Lync administrators include the following:</span></span>

  - <span data-ttu-id="5fb76-127">**Kapazitäts-und Verfügbarkeitsverwaltung**   Definieren Sie, wie und was gemessen werden soll, um zukünftige Kapazitätsanforderungen vorherzusagen und über die Kapazität, Zuverlässigkeit und Verfügbarkeit Ihrer Systeme zu berichten.</span><span class="sxs-lookup"><span data-stu-id="5fb76-127">**Capacity and Availability Management**   Define how and what to measure to predict future capacity requirements and to report about the capacity, reliability, and availability of your systems.</span></span> <span data-ttu-id="5fb76-128">Sie müssen sicherstellen, dass die Server, auf denen lync Server ausgeführt wird, für die Verarbeitung der Auslastung des Systems ausgelegt sind und dass ungeplante Ausfallzeiten unter den in der Vereinbarung zum Service Level (SLA) definierten Ebenen aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-128">You must verify that servers that are running Lync Server are sized to handle the load on the system, and that unplanned downtime is kept under the levels defined in the service level agreement (SLA).</span></span> <span data-ttu-id="5fb76-129">Darüber hinaus müssen Sie Hardware aktualisieren, um die definierten Anforderungen weiterhin erfüllen zu können.</span><span class="sxs-lookup"><span data-stu-id="5fb76-129">Additionally, you'll have to upgrade hardware to continue to meet the defined requirements.</span></span>

  - <span data-ttu-id="5fb76-130">**Change Management und Konfigurationsverwaltung**   Steuern Sie, wie Änderungen an IT-Systemen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-130">**Change Management and Configuration Management**   Control how changes are made to IT systems.</span></span> <span data-ttu-id="5fb76-131">Dies sollte Tests, Anwendungs Feedback und Notfallpläne, die Dokumentation aller Änderungen und die Genehmigung der Verwaltung umfassen, wenn Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="5fb76-131">This should include testing, application feedback and contingency plans, documentation of all changes, and approval from management if issues occur.</span></span> <span data-ttu-id="5fb76-132">Speichern Sie Ihre Software-und Hardwareressourcen sowie deren Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="5fb76-132">Keep a record of your software and hardware assets and their configurations.</span></span>

  - <span data-ttu-id="5fb76-133">**System Verwaltung**   Gliedern Sie die Standardmethoden für administrative Aufgaben wie Datenbankverwaltung und Websiteverwaltung.</span><span class="sxs-lookup"><span data-stu-id="5fb76-133">**System Administration**   Outline standard methods for doing administrative tasks such as database administration and site administration.</span></span>

  - <span data-ttu-id="5fb76-134">**Sicherheitsverwaltung**   Sie verfügen über eine detaillierte Richtlinie und einen Plan, mit dem Datenvertraulichkeit, Datenintegrität und Datenverfügbarkeit der IT-Infrastruktur geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="5fb76-134">**Security Administration**   Have a detailed policy and plan that protects data confidentiality, data integrity, and data availability of the IT infrastructure.</span></span> <span data-ttu-id="5fb76-135">Dazu gehören alltägliche Aktivitäten und Aufgaben im Zusammenhang mit der Verwaltung und Anpassung der IT-Sicherheitsinfrastruktur.</span><span class="sxs-lookup"><span data-stu-id="5fb76-135">This includes day-to-day activities and tasks that are related to maintaining and adjusting the IT security infrastructure.</span></span>

  - <span data-ttu-id="5fb76-136">**System Problembehandlung**   Gliedern von Methoden zum Umgang mit unerwarteten Problemen, einschließlich der Schritte zum verhindern ähnlicher Probleme in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="5fb76-136">**System Troubleshooting**   Outline methods for dealing with unexpected issues, including steps to prevent similar issues in the future.</span></span>

  - <span data-ttu-id="5fb76-137">**Service Level Agreements**   Verwalten Sie eine Reihe von Zielen für die Leistung der IT-Systeme, und Messen Sie die Leistung regelmäßig mit diesen Zielen.</span><span class="sxs-lookup"><span data-stu-id="5fb76-137">**Service Level Agreements**   Maintain a set of goals for the performance of the IT systems and regularly measure performance against these goals.</span></span>

  - <span data-ttu-id="5fb76-138">**Dokumentation**   Dokumentieren Sie Standardverfahren wie Konfigurationsinformationen und gelernte Lektionen, und stellen Sie Sie den Mitarbeitern zur Verfügung, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="5fb76-138">**Documentation**   Document standard procedures, such as configuration information and lessons learned, and make them available to the staff members that need them.</span></span> <span data-ttu-id="5fb76-139">Wenn Änderungen an der Konfiguration vorgenommen wurden, aktualisieren Sie die Dokumentation entsprechend.</span><span class="sxs-lookup"><span data-stu-id="5fb76-139">As changes to the configuration are made, update the documentation accordingly.</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="5fb76-140">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="5fb76-140">Related Sections</span></span>

<span data-ttu-id="5fb76-141">Lesen Sie die folgenden Themen zu Systemvorgängen, bevor Sie fortfahren:</span><span class="sxs-lookup"><span data-stu-id="5fb76-141">Review the following topics concerning system operations before proceeding:</span></span>

  - [<span data-ttu-id="5fb76-142">Kapazitäts-und Verfügbarkeitsverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-142">Capacity and availability management in Lync Server 2013</span></span>](lync-server-2013-capacity-and-availability-management.md)

  - [<span data-ttu-id="5fb76-143">Änderungsverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-143">Change management in Lync Server 2013</span></span>](lync-server-2013-change-management.md)

  - [<span data-ttu-id="5fb76-144">Konfigurationsverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-144">Configuration management in Lync Server 2013</span></span>](lync-server-2013-configuration-management.md)

  - [<span data-ttu-id="5fb76-145">System Verwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-145">System administration in Lync Server 2013</span></span>](lync-server-2013-system-administration.md)

  - [<span data-ttu-id="5fb76-146">Service Level Agreements in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-146">Service level agreements in Lync Server 2013</span></span>](lync-server-2013-service-level-agreements.md)

  - [<span data-ttu-id="5fb76-147">Dokumentation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-147">Documentation in Lync Server 2013</span></span>](lync-server-2013-documentation.md)

  - [<span data-ttu-id="5fb76-148">Standard Verfahren in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-148">Standard procedures in Lync Server 2013</span></span>](lync-server-2013-standard-procedures.md)

  - [<span data-ttu-id="5fb76-149">Notfallverfahren in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5fb76-149">Emergency procedures in Lync Server 2013</span></span>](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5fb76-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb76-150">See Also</span></span>


[<span data-ttu-id="5fb76-151">Microsoft Operations Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="5fb76-151">Microsoft Operations Framework 4.0</span></span>](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

<span data-ttu-id="5fb76-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5fb76-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

