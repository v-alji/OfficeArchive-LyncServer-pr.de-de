---
title: 'Lync Server 2013: Unterstützte Active Directory-Topologien'
description: 'Lync Server 2013: Unterstützte Active Directory-Topologien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported Active Directory topologies
ms:assetid: 0c76b778-7652-4eb0-b161-86f2d4a94ccf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398173(v=OCS.15)
ms:contentKeyID: 48183391
ms.date: 10/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ce820a36cb033933b423e01deb5a3049ed3ea2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441534"
---
# <a name="supported-active-directory-topologies-in-lync-server-2013"></a><span data-ttu-id="e5e73-103">Unterstützte Active Directory-Topologien in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5e73-103">Supported Active Directory topologies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5e73-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5e73-104">

<span> </span></span></span>

<span data-ttu-id="e5e73-105">_**Letztes Änderungsdatum des Themas:** 2014-10-02_</span><span class="sxs-lookup"><span data-stu-id="e5e73-105">_**Topic Last Modified:** 2014-10-02_</span></span>

<span data-ttu-id="e5e73-106">Lync Server 2013 unterstützt dieselben Active Directory-Domänendienste-Topologien wie Microsoft lync Server 2010 und Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="e5e73-106">Lync Server 2013 supports the same Active Directory Domain Services topologies as Microsoft Lync Server 2010 and Microsoft Office Communications Server 2007 R2.</span></span> <span data-ttu-id="e5e73-107">Die folgenden Topologien werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="e5e73-107">The following topologies are supported:</span></span>

  - <span data-ttu-id="e5e73-108">Einzelne Gesamtstruktur mit einzelner Domäne</span><span class="sxs-lookup"><span data-stu-id="e5e73-108">Single forest with single domain</span></span>

  - <span data-ttu-id="e5e73-109">Einzelne Gesamtstruktur mit einer Struktur und mehreren Domänen</span><span class="sxs-lookup"><span data-stu-id="e5e73-109">Single forest with a single tree and multiple domains</span></span>

  - <span data-ttu-id="e5e73-110">Einzelne Gesamtstruktur mit mehreren Strukturen und nicht zusammenhängenden Namespaces</span><span class="sxs-lookup"><span data-stu-id="e5e73-110">Single forest with multiple trees and disjoint namespaces</span></span>

  - <span data-ttu-id="e5e73-111">Mehrere Gesamtstrukturen in einer Topologie mit zentraler Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="e5e73-111">Multiple forests in a central forest topology</span></span>

  - <span data-ttu-id="e5e73-112">Mehrere Gesamtstrukturen in einer Topologie mit Ressourcengesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="e5e73-112">Multiple forests in a resource forest topology</span></span>

  - <span data-ttu-id="e5e73-113">Mehrere Gesamtstrukturen in einer lync-Ressourcengesamtstruktur-Topologie mit Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e5e73-113">Multiple forests in a Lync resource forest topology with Exchange Online</span></span>

<span data-ttu-id="e5e73-114">In der folgenden Abbildung sind die Symbole aufgeführt, die in den Illustrationen in diesem Abschnitt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-114">The following figure identifies the icons used in the illustrations in this section.</span></span>

<span data-ttu-id="e5e73-115">**Schlüssel zu Topologie-Illustrationen**</span><span class="sxs-lookup"><span data-stu-id="e5e73-115">**Key to topology illustrations**</span></span>

<span data-ttu-id="e5e73-116">![Schlüssel zu Topologie-Illustrationen](images/Gg398173.0c3cc89f-6c43-4bc8-b2ec-61d89e391ee9(OCS.15).jpg "Schlüssel zu Topologie-Illustrationen")</span><span class="sxs-lookup"><span data-stu-id="e5e73-116">![Key to topology illustrations](images/Gg398173.0c3cc89f-6c43-4bc8-b2ec-61d89e391ee9(OCS.15).jpg "Key to topology illustrations")</span></span>

<div>

## <a name="single-forest-single-domain"></a><span data-ttu-id="e5e73-117">Einzelne Gesamtstruktur, einzelne Domäne</span><span class="sxs-lookup"><span data-stu-id="e5e73-117">Single Forest, Single Domain</span></span>

<span data-ttu-id="e5e73-118">Die einfachste Active Directory-Topologie, die von lync Server, einer einzelnen Domänengesamtstruktur, unterstützt wird, ist eine allgemeine Topologie.</span><span class="sxs-lookup"><span data-stu-id="e5e73-118">The simplest Active Directory topology supported by Lync Server, a single domain forest, is a common topology.</span></span>

<span data-ttu-id="e5e73-119">Die folgende Abbildung zeigt eine lync Server-Bereitstellung in einer einzelnen Active Directory-Domänentopologie.</span><span class="sxs-lookup"><span data-stu-id="e5e73-119">The following figure illustrates a Lync Server deployment in a single domain Active Directory topology.</span></span>

<span data-ttu-id="e5e73-120">**Topologie mit einer einzelnen Domäne**</span><span class="sxs-lookup"><span data-stu-id="e5e73-120">**Single domain topology**</span></span>

<span data-ttu-id="e5e73-121">![Topologie mit einer einzelnen Domäne](images/Gg398173.258b3b3f-0558-4a36-a4c2-031be7299668(OCS.15).jpg "Topologie mit einer einzelnen Domäne")</span><span class="sxs-lookup"><span data-stu-id="e5e73-121">![Single domain topology](images/Gg398173.258b3b3f-0558-4a36-a4c2-031be7299668(OCS.15).jpg "Single domain topology")</span></span>

</div>

<div>

## <a name="single-forest-multiple-domains"></a><span data-ttu-id="e5e73-122">Einzelne Gesamtstruktur, mehrere Domänen</span><span class="sxs-lookup"><span data-stu-id="e5e73-122">Single Forest, Multiple Domains</span></span>

<span data-ttu-id="e5e73-123">Eine andere von lync Server unterstützte Active Directory-Topologie ist eine einzelne Gesamtstruktur, die aus einer Stammdomäne und einer oder mehreren untergeordneten Domänen besteht.</span><span class="sxs-lookup"><span data-stu-id="e5e73-123">Another Active Directory topology supported by Lync Server is a single forest that consists of a root domain and one or more child domains.</span></span> <span data-ttu-id="e5e73-124">Bei dieser Art von Active Directory-Topologie kann sich die Domäne, in der Sie Benutzer erstellen, von der Domäne unterscheiden, in der Sie lync Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-124">In this type of Active Directory topology, the domain where you create users can be different from the domain where you deploy Lync Server.</span></span> <span data-ttu-id="e5e73-125">Wenn Sie jedoch einen Front-End-Pool bereitstellen, müssen Sie alle Front-End-Server im Pool innerhalb einer einzigen Domäne bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-125">However, if you deploy a Front End pool, you must deploy all the Front End Servers in the pool within a single domain.</span></span> <span data-ttu-id="e5e73-126">Die lync Server-Unterstützung für universelle Windows-Administratorgruppen ermöglicht die domänenübergreifende Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="e5e73-126">Lync Server support for Windows universal administrator groups enables cross-domain administration.</span></span>

<span data-ttu-id="e5e73-127">Die folgende Abbildung zeigt eine Bereitstellung in einer einzelnen Gesamtstruktur mit mehreren Domänen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-127">The following figure illustrates a deployment in a single forest with multiple domains.</span></span> <span data-ttu-id="e5e73-128">In dieser Abbildung zeigt ein Benutzersymbol die Domäne an, in der sich das Benutzerkonto befindet, und der Pfeil verweist auf die Domäne, in der sich der lync-Server Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="e5e73-128">In this figure, a user icon shows the domain where the user account is homed, and the arrow points to the domain where the Lync Server pool resides.</span></span> <span data-ttu-id="e5e73-129">Zu den Benutzerkonten gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="e5e73-129">User accounts include the following:</span></span>

  - <span data-ttu-id="e5e73-130">Benutzerkonten innerhalb der gleichen Domäne wie der lync-Server Pool</span><span class="sxs-lookup"><span data-stu-id="e5e73-130">User accounts within the same domain as the Lync Server pool</span></span>

  - <span data-ttu-id="e5e73-131">Benutzerkonten in einer anderen Domäne als dem lync-Server Pool</span><span class="sxs-lookup"><span data-stu-id="e5e73-131">User accounts in a different domain from the Lync Server pool</span></span>

  - <span data-ttu-id="e5e73-132">Benutzerkonten in einer untergeordneten Domäne der Domäne mit dem lync-Server Pool</span><span class="sxs-lookup"><span data-stu-id="e5e73-132">User accounts in a child domain of the domain with the Lync Server pool</span></span>

<span data-ttu-id="e5e73-133">**Einzelne Gesamtstruktur mit mehreren Domänen**</span><span class="sxs-lookup"><span data-stu-id="e5e73-133">**Single forest with multiple domains**</span></span>

<span data-ttu-id="e5e73-134">![Einzelne Gesamtstruktur mit mehreren Domänen](images/Gg398173.2b809c72-c3cd-4fad-afe6-8c2dae779750(OCS.15).jpg "Einzelne Gesamtstruktur mit mehreren Domänen")</span><span class="sxs-lookup"><span data-stu-id="e5e73-134">![Single forest with multiple domains](images/Gg398173.2b809c72-c3cd-4fad-afe6-8c2dae779750(OCS.15).jpg "Single forest with multiple domains")</span></span>

</div>

<div>

## <a name="single-forest-multiple-trees"></a><span data-ttu-id="e5e73-135">Einzelne Gesamtstruktur, mehrere Strukturen</span><span class="sxs-lookup"><span data-stu-id="e5e73-135">Single Forest, Multiple Trees</span></span>

<span data-ttu-id="e5e73-136">Eine Topologie mit mehreren Strukturen besteht aus zwei oder mehr Domänen, die unabhängige Struktur Strukturen und separate Active Directory-Namespaces definieren.</span><span class="sxs-lookup"><span data-stu-id="e5e73-136">A multiple-tree forest topology consists of two or more domains that define independent tree structures and separate Active Directory namespaces.</span></span>

<span data-ttu-id="e5e73-137">Die folgende Abbildung zeigt eine einzelne Gesamtstruktur mit mehreren Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-137">The following figure illustrates a single forest with multiple trees.</span></span> <span data-ttu-id="e5e73-138">In dieser Abbildung zeigt ein Benutzersymbol die Domäne an, in der sich das Benutzerkonto befindet, eine durchgezogene Linie verweist auf einen lync-Serverpool, der sich in derselben oder einer anderen Domäne befindet, und eine gestrichelte Linie verweist auf den lync-Serverpool, der sich in einer anderen Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="e5e73-138">In this figure, a user icon shows the domain where the user account is homed, a solid line points to a Lync Server pool that resides in the same or a different domain, and a dashed line points to Lync Server pool that resides in a different tree.</span></span> <span data-ttu-id="e5e73-139">Zu den Benutzerkonten gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="e5e73-139">User accounts include the following:</span></span>

  - <span data-ttu-id="e5e73-140">Benutzerkonten innerhalb der gleichen Domäne wie der lync-Server Pool</span><span class="sxs-lookup"><span data-stu-id="e5e73-140">User accounts within the same domain as the Lync Server pool</span></span>

  - <span data-ttu-id="e5e73-141">Benutzerkonten in einer anderen Domäne als der lync-Server Pool (aber dieselbe Struktur wie)</span><span class="sxs-lookup"><span data-stu-id="e5e73-141">User accounts in a different domain from (but the same tree as) the Lync Server pool</span></span>

  - <span data-ttu-id="e5e73-142">Benutzerkonten in einer anderen Struktur aus dem lync-Server Pool</span><span class="sxs-lookup"><span data-stu-id="e5e73-142">User accounts in a different tree from the Lync Server pool</span></span>

<span data-ttu-id="e5e73-143">**Einzelne Gesamtstruktur mit mehreren Strukturen**</span><span class="sxs-lookup"><span data-stu-id="e5e73-143">**Single forest with multiple trees**</span></span>

<span data-ttu-id="e5e73-144">![Einzelne Gesamtstruktur mit mehreren Strukturen](images/Gg398173.db30fa49-174a-4974-8695-41dd78e39432(OCS.15).jpg "Einzelne Gesamtstruktur mit mehreren Strukturen")</span><span class="sxs-lookup"><span data-stu-id="e5e73-144">![Single forest with multiple trees](images/Gg398173.db30fa49-174a-4974-8695-41dd78e39432(OCS.15).jpg "Single forest with multiple trees")</span></span>

</div>

<div>

## <a name="multiple-forests-central-forest"></a><span data-ttu-id="e5e73-145">Mehrere Gesamtstrukturen, zentrale Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="e5e73-145">Multiple Forests, Central Forest</span></span>

<span data-ttu-id="e5e73-146">Lync Server unterstützt mehrere Gesamtstrukturen, die in einer zentralen Gesamtstrukturtopologie konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="e5e73-146">Lync Server supports multiple forests that are configured in a central forest topology.</span></span> <span data-ttu-id="e5e73-147">Zentrale Gesamtstruktur Topologien verwenden Kontaktobjekte in der zentralen Gesamtstruktur, um Benutzer in den anderen Gesamtstrukturen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-147">Central forest topologies use contact objects in the central forest to represent users in the other forests.</span></span> <span data-ttu-id="e5e73-148">Die zentrale Gesamtstruktur hostet auch Benutzerkonten für alle Benutzer in dieser Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-148">The central forest also hosts user accounts for any users in this forest.</span></span> <span data-ttu-id="e5e73-149">Ein Verzeichnis Synchronisierungs Produkt wie Microsoft Identity Integration Server (MIIS) Microsoft Forefront Identity Manager (FIM) 2010 oder Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1) verwaltet den Lebenszyklus von Benutzerkonten innerhalb der Organisation: Wenn ein neues Benutzerkonto in einer der Gesamtstrukturen erstellt oder ein Benutzerkonto aus einer Gesamtstruktur gelöscht wird, synchronisiert das Verzeichnis Synchronisierungs Produkt den entsprechenden Kontakt in der zentralen Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-149">A directory synchronization product, such as Microsoft Identity Integration Server (MIIS), Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts within the organization: When a new user account is created in one of the forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding contact in the central forest.</span></span>

<span data-ttu-id="e5e73-150">Eine zentrale Gesamtstruktur bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="e5e73-150">A central forest has the following advantages:</span></span>

  - <span data-ttu-id="e5e73-151">Server mit lync Server werden innerhalb einer einzigen Gesamtstruktur zentralisiert.</span><span class="sxs-lookup"><span data-stu-id="e5e73-151">Servers running Lync Server are centralized within a single forest.</span></span>

  - <span data-ttu-id="e5e73-152">Benutzer können in jeder Gesamtstruktur nach anderen Benutzern suchen und mit Ihnen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="e5e73-152">Users can search for and communicate with other users in any forest.</span></span>

  - <span data-ttu-id="e5e73-153">Benutzer können die Anwesenheit anderer Benutzer in einer beliebigen Gesamtstruktur anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-153">Users can view presence of other users in any forest.</span></span>

  - <span data-ttu-id="e5e73-154">Das Verzeichnis Synchronisierungs Produkt automatisiert das Hinzufügen und Löschen von Kontaktobjekten in der zentralen Gesamtstruktur, wenn Benutzerkonten erstellt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-154">The directory synchronization product automates the addition and deletion of contact objects in the central forest as user accounts are created or removed.</span></span>

<span data-ttu-id="e5e73-155">Die folgende Abbildung veranschaulicht eine zentrale Gesamtstrukturtopologie.</span><span class="sxs-lookup"><span data-stu-id="e5e73-155">The following figure illustrates a central forest topology.</span></span> <span data-ttu-id="e5e73-156">In dieser Abbildung gibt es bidirektionale Vertrauensstellungen zwischen der Domäne, die lync Server hostet, die sich in der zentralen Gesamtstruktur befindet, und jeder Benutzerdomäne, die sich in einer separaten Gesamtstruktur befindet.</span><span class="sxs-lookup"><span data-stu-id="e5e73-156">In this figure, there are two-way trust relationships between the domain that hosts Lync Server, which is in the central forest, and each user-only domain, which is in a separate forest.</span></span> <span data-ttu-id="e5e73-157">Das Schema in den separaten Benutzergesamtstrukturen muss nicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-157">The schema in the separate user forests does not need to be extended.</span></span>

<span data-ttu-id="e5e73-158">**Zentrale Gesamtstrukturtopologie**</span><span class="sxs-lookup"><span data-stu-id="e5e73-158">**Central forest topology**</span></span>

<span data-ttu-id="e5e73-159">![Zentrale Gesamtstrukturtopologie](images/Gg398173.7feb049a-453b-4134-9128-873b83ee1755(OCS.15).jpg "Zentrale Gesamtstrukturtopologie")</span><span class="sxs-lookup"><span data-stu-id="e5e73-159">![Central forest topology](images/Gg398173.7feb049a-453b-4134-9128-873b83ee1755(OCS.15).jpg "Central forest topology")</span></span>

</div>

<div>

## <a name="multiple-forests-resource-forest"></a><span data-ttu-id="e5e73-160">Mehrere Gesamtstrukturen, Ressourcengesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="e5e73-160">Multiple Forests, Resource Forest</span></span>

<span data-ttu-id="e5e73-161">In einer Ressourcengesamtstruktur-Topologie ist eine Gesamtstruktur für die Ausführung von Serveranwendungen wie Microsoft Exchange Server und lync Server reserviert.</span><span class="sxs-lookup"><span data-stu-id="e5e73-161">In a resource forest topology, one forest is dedicated to running server applications, such as Microsoft Exchange Server and Lync Server.</span></span> <span data-ttu-id="e5e73-162">Die Ressourcengesamtstruktur hostet die Serveranwendungen und eine synchronisierte Darstellung des aktiven Benutzerobjekts, enthält jedoch keine Anmelde fähigen Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="e5e73-162">The resource forest hosts the server applications and a synchronized representation of the active user object, but it does not contain logon-enabled user accounts.</span></span> <span data-ttu-id="e5e73-163">Die Ressourcengesamtstruktur fungiert als Umgebung für gemeinsame Dienste für die anderen Gesamtstrukturen, in denen sich Benutzerobjekte befinden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-163">The resource forest acts as a shared services environment for the other forests where user objects reside.</span></span> <span data-ttu-id="e5e73-164">Die Benutzergesamtstrukturen verfügen über eine Vertrauensstellung auf Gesamtstrukturebene mit der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-164">The user forests have a forest-level trust relationship with the resource forest.</span></span> <span data-ttu-id="e5e73-165">Wenn Sie lync Server in dieser Art von Topologie bereitstellen, erstellen Sie für jedes Benutzerkonto in den Benutzergesamtstrukturen ein deaktiviertes Benutzerobjekt in der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-165">When you deploy Lync Server in this type of topology, you create one disabled user object in the resource forest for every user account in the user forests.</span></span> <span data-ttu-id="e5e73-166">Wenn Microsoft Exchange bereits in der Ressourcengesamtstruktur bereitgestellt wurde, sind die deaktivierten Benutzerkonten möglicherweise bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-166">If Microsoft Exchange is already deployed in the resource forest, the disabled user accounts might already exist.</span></span> <span data-ttu-id="e5e73-167">Ein Verzeichnis Synchronisierungs Produkt wie MIIS, Microsoft Forefront Identity Manager (FIM) 2010 oder Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1) verwaltet den Lebenszyklus von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="e5e73-167">A directory synchronization product, such as MIIS, Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts.</span></span> <span data-ttu-id="e5e73-168">Wenn ein neues Benutzerkonto in einer der Benutzergesamtstrukturen erstellt oder ein Benutzerkonto aus einer Gesamtstruktur gelöscht wird, synchronisiert das Verzeichnis Synchronisierungs Produkt die entsprechende Benutzerdarstellung in der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-168">When a new user account is created in one of the user forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding user representation in the resource forest.</span></span>

<span data-ttu-id="e5e73-169">Diese Topologie kann verwendet werden, um eine gemeinsame Infrastruktur für Dienste in Organisationen bereitzustellen, die mehrere Gesamtstrukturen verwalten, oder um die Verwaltung von Active Directory-Objekten von anderer Verwaltung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="e5e73-169">This topology can be used to provide a shared infrastructure for services in organizations that manage multiple forests or to separate the administration of Active Directory objects from other administration.</span></span> <span data-ttu-id="e5e73-170">Unternehmen, die die Active Directory-Verwaltung aus Sicherheitsgründen isolieren müssen, wählen diese Topologie häufig aus.</span><span class="sxs-lookup"><span data-stu-id="e5e73-170">Companies that need to isolate Active Directory administration for security reasons often choose this topology.</span></span>

<span data-ttu-id="e5e73-171">Diese Topologie bietet den Vorteil, dass die Erweiterung des Active Directory-Schemas auf eine einzelne Gesamtstruktur (also die Ressourcengesamtstruktur) eingeschränkt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e5e73-171">This topology provides the benefit of limiting the need to extend the Active Directory schema to a single forest (that is, the resource forest).</span></span>

<span data-ttu-id="e5e73-172">Das folgende Diagramm veranschaulicht eine Ressourcengesamtstruktur-Topologie.</span><span class="sxs-lookup"><span data-stu-id="e5e73-172">The following diagram illustrates a resource forest topology.</span></span>

<span data-ttu-id="e5e73-173">**Topologie der Ressourcengesamtstruktur**</span><span class="sxs-lookup"><span data-stu-id="e5e73-173">**Resource forest topology**</span></span>

<span data-ttu-id="e5e73-174">![Topologie der Active Directory-Ressourcengesamtstruktur](images/Gg398173.54ab82f1-e9e5-40f0-a54e-86e340b65c2a(OCS.15).jpg "Topologie der Active Directory-Ressourcengesamtstruktur")</span><span class="sxs-lookup"><span data-stu-id="e5e73-174">![Active Directory Resource Forest Topology](images/Gg398173.54ab82f1-e9e5-40f0-a54e-86e340b65c2a(OCS.15).jpg "Active Directory Resource Forest Topology")</span></span>

</div>

<div>

## <a name="multiple-forests-in-a-lync-resource-forest-topology-with-exchange-online"></a><span data-ttu-id="e5e73-175">Mehrere Gesamtstrukturen in einer lync-Ressourcengesamtstruktur-Topologie mit Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e5e73-175">Multiple forests in a Lync resource forest topology with Exchange Online</span></span>

<span data-ttu-id="e5e73-176">In dieser Topologie befinden sich eine oder mehrere Gesamtstrukturen lokal und sind für das Hosten von Active Directory-Benutzerkonten reserviert.</span><span class="sxs-lookup"><span data-stu-id="e5e73-176">In this topology, one or more forests are located on-premises and are dedicated to hosting Active Directory user accounts.</span></span> <span data-ttu-id="e5e73-177">Die Ressourcengesamtstruktur befindet sich außerhalb des Lokals und wird von einem externen Hostinganbieter verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e5e73-177">The resource forest is located off-premises and is maintained by a third-party hosting provider.</span></span> <span data-ttu-id="e5e73-178">Die Ressourcengesamtstruktur enthält nur die lync Server-Bereitstellung und eine synchronisierte Replikation der Benutzerkonten aus der lokalen Benutzerkontengesamtstruktur (en).</span><span class="sxs-lookup"><span data-stu-id="e5e73-178">The resource forest contains only the Lync Server deployment and a synchronized replication of the user accounts from the on-premises user accounts forest(s).</span></span> <span data-ttu-id="e5e73-179">Sie enthält keine Anmelde fähigen Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="e5e73-179">It does not contain logon-enabled user accounts.</span></span> <span data-ttu-id="e5e73-180">Exchange wird entweder in der lokalen Benutzerkonten-Gesamtstruktur (en) bereitgestellt, die zusammen mit Exchange Online (Hybrid) integriert ist, oder e-Mail-Dienste für die lokalen Benutzerkonten werden ausschließlich von Exchange Online bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e5e73-180">Exchange is deployed either in the on-premises user account forest(s) integrated along with Exchange Online (Hybrid), or email services for the on-premises user accounts are provided exclusively by Exchange Online.</span></span>

<span data-ttu-id="e5e73-181">Die Ressourcengesamtstruktur fungiert als Umgebung für gemeinsame Dienste für die lokalen Active Directory-Gesamtstrukturen, in denen sich Benutzerobjekte befinden.</span><span class="sxs-lookup"><span data-stu-id="e5e73-181">The resource forest acts as a shared services environment for the on-premises Active Directory forest(s) where user objects reside.</span></span> <span data-ttu-id="e5e73-182">Die Gesamtstruktur des Benutzerkontos verfügt über eine unidirektionale Vertrauensstellung auf Gesamtstrukturebene mit der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-182">The user account forest(s) have a one way forest-level trust relationship with the resource forest.</span></span> <span data-ttu-id="e5e73-183">Wenn Sie lync Server in dieser Art von Topologie bereitstellen, erstellen Sie für jedes Benutzerkonto in den Benutzergesamtstrukturen ein deaktiviertes Benutzerobjekt in der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-183">When you deploy Lync Server in this type of topology, you create one disabled user object in the resource forest for every user account in the user forests.</span></span> <span data-ttu-id="e5e73-184">Ein Verzeichnis Synchronisierungs Produkt wie MIIS, Microsoft Forefront Identity Manager (FIM) 2010 oder Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1) verwaltet den Lebenszyklus von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="e5e73-184">A directory synchronization product, such as MIIS, Microsoft Forefront Identity Manager (FIM) 2010, or Microsoft Identity Lifecycle Manager (ILM) 2007 Feature Pack 1 (FP1), manages the life cycle of user accounts.</span></span> <span data-ttu-id="e5e73-185">Wenn ein neues Benutzerkonto in einer der Benutzergesamtstrukturen erstellt oder ein Benutzerkonto aus einer Gesamtstruktur gelöscht wird, synchronisiert das Verzeichnis Synchronisierungs Produkt die entsprechende Benutzerdarstellung in der Ressourcengesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="e5e73-185">When a new user account is created in one of the user forests or a user account is deleted from a forest, the directory synchronization product synchronizes the corresponding user representation in the resource forest.</span></span> <span data-ttu-id="e5e73-186">Weitere Informationen zum Konfigurieren einer Bereitstellung mit mehreren Gesamtstrukturen finden Sie unter [Bereitstellen von lync in einer Architektur mit mehreren Gesamtstrukturen (Partner Hosted lync mit Exchange-Hybrid)](https://go.microsoft.com/fwlink/p/?linkid=513216).</span><span class="sxs-lookup"><span data-stu-id="e5e73-186">For more information about configuring a multi-forest deployment, see [Deploying Lync in a Multi-Forest Architecture (Partner Hosted Lync with Exchange Hybrid)](https://go.microsoft.com/fwlink/p/?linkid=513216).</span></span>

<span data-ttu-id="e5e73-187"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5e73-187"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

