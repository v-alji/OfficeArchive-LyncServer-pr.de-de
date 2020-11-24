---
title: 'Lync Server 2013: Unterstützung der Active Directory-Domänendienste'
description: 'Lync Server 2013: Unterstützung für Active Directory-Domänendienste.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory Domain Services support
ms:assetid: aeb62d5e-e424-473a-b795-9452150c98dd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412831(v=OCS.15)
ms:contentKeyID: 48185136
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb2a85bab90557c28c4802721d4202f6188cb3f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393882"
---
# <a name="active-directory-domain-services-support-in-lync-server-2013"></a><span data-ttu-id="305a3-103">Unterstützung der Active Directory-Domänendienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="305a3-103">Active Directory Domain Services support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="305a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="305a3-104">

<span> </span></span></span>

<span data-ttu-id="305a3-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="305a3-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="305a3-106">Lync Server 2013 verwendet den zentralen Verwaltungsspeicher, um Konfigurationsdaten für Server und Dienste zu speichern, anstatt sich wie in der Vergangenheit auf die Active Directory-Domänendienste für diese Informationen zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="305a3-106">Lync Server 2013 uses the Central Management store to store configuration data for servers and services, instead of relying on Active Directory Domain Services for this information, as in the past.</span></span> <span data-ttu-id="305a3-107">Lync Server 2013 speichert weiterhin die folgenden in AD DS:</span><span class="sxs-lookup"><span data-stu-id="305a3-107">Lync Server 2013 still stores the following in AD DS:</span></span>

  - <span data-ttu-id="305a3-108">**Schemaerweiterungen**</span><span class="sxs-lookup"><span data-stu-id="305a3-108">**Schema extensions**</span></span>
    
      - <span data-ttu-id="305a3-109">Benutzerobjekterweiterungen</span><span class="sxs-lookup"><span data-stu-id="305a3-109">User object extensions</span></span>
    
      - <span data-ttu-id="305a3-110">Erweiterungen für lync Server 2010 und Office Communications Server 2007 R2-Klassen zum aufrecht erhalten der Abwärtskompatibilität mit vorherigen unterstützten Versionen</span><span class="sxs-lookup"><span data-stu-id="305a3-110">Extensions for Lync Server 2010 and Office Communications Server 2007 R2 classes to maintain backward compatibility with previous supported versions</span></span>

  - <span data-ttu-id="305a3-111">**Daten** (im erweiterten Schema von lync Server 2013 und in vorhandenen Klassen gespeichert)</span><span class="sxs-lookup"><span data-stu-id="305a3-111">**Data** (stored in Lync Server 2013 extended schema and in existing classes)</span></span>
    
      - <span data-ttu-id="305a3-112">Der Benutzer-SIP-URI und andere Einstellungen</span><span class="sxs-lookup"><span data-stu-id="305a3-112">User SIP URI and other user settings</span></span>
    
      - <span data-ttu-id="305a3-113">Kontaktobjekte für Anwendungen (beispielsweise die Anwendung "Reaktionsgruppe" und die Anwendung "Conferencing Attendant")</span><span class="sxs-lookup"><span data-stu-id="305a3-113">Contact objects for applications (for example, the Response Group application and the Conferencing Attendant application)</span></span>
    
      - <span data-ttu-id="305a3-114">Aus Gründen der Abwärtskompatibilität veröffentlichte Daten</span><span class="sxs-lookup"><span data-stu-id="305a3-114">Data published for backward compatibility</span></span>
    
      - <span data-ttu-id="305a3-115">Einen Dienst Kontrollpunkt (Service Control Point, SCP) für den zentralen Verwaltungsspeicher</span><span class="sxs-lookup"><span data-stu-id="305a3-115">A service control point (SCP) for the Central Management store</span></span>
    
      - <span data-ttu-id="305a3-116">Kerberos-Authentifizierungs Konto (ein optionales Computerobjekt)</span><span class="sxs-lookup"><span data-stu-id="305a3-116">Kerberos Authentication Account (an optional computer object)</span></span>

<span data-ttu-id="305a3-117">In diesem Abschnitt werden die AD DS-Supportanforderungen für lync Server 2013 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="305a3-117">This section describes the AD DS support requirements for Lync Server 2013.</span></span> <span data-ttu-id="305a3-118">Details zur Topologie-Unterstützung finden Sie unter unter [stützte Active Directory-Topologien in lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="305a3-118">For details about topology support, see [Supported Active Directory topologies in Lync Server 2013](lync-server-2013-supported-active-directory-topologies.md) in the Supportability documentation.</span></span>

<div>

## <a name="supported-domain-controller-operating-systems"></a><span data-ttu-id="305a3-119">Unterstützte Domänen Controller-Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="305a3-119">Supported Domain Controller Operating Systems</span></span>

<span data-ttu-id="305a3-120">Lync Server 2013 unterstützt Domänencontroller, auf denen die folgenden Betriebssysteme ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="305a3-120">Lync Server 2013 supports domain controllers running the following operating systems:</span></span>

  - <span data-ttu-id="305a3-121">Windows Server 2012 R2-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="305a3-121">Windows Server 2012 R2 operating system</span></span>

  - <span data-ttu-id="305a3-122">Betriebssystem Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="305a3-122">Windows Server 2012 operating system</span></span>

  - <span data-ttu-id="305a3-123">Windows Server 2008 R2-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="305a3-123">Windows Server 2008 R2 operating system</span></span>

  - <span data-ttu-id="305a3-124">Windows Server 2008-Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="305a3-124">Windows Server 2008 operating system</span></span>

  - <span data-ttu-id="305a3-125">Windows Server 2008 Enterprise 32-Bit</span><span class="sxs-lookup"><span data-stu-id="305a3-125">Windows Server 2008 Enterprise 32-Bit</span></span>

  - <span data-ttu-id="305a3-126">Die 32-Bit-oder 64-Bit-Versionen des Windows Server 2003 R2-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="305a3-126">The 32-bit or 64-bit versions of the Window Server 2003 R2 operating system</span></span>

  - <span data-ttu-id="305a3-127">Die 32-Bit-oder 64-Bit-Versionen des Windows Server 2003-Betriebssystems</span><span class="sxs-lookup"><span data-stu-id="305a3-127">The 32-bit or 64-bit versions of the Windows Server 2003 operating system</span></span>

</div>

<div>

## <a name="forest-and-domain-functional-level"></a><span data-ttu-id="305a3-128">Gesamtstruktur-und Domänenfunktionsebene</span><span class="sxs-lookup"><span data-stu-id="305a3-128">Forest and Domain Functional Level</span></span>

<span data-ttu-id="305a3-129">Sie müssen alle Domänen auslösen, in denen Sie lync Server 2013 auf einer Domänenfunktionsebene von Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 oder mindestens Windows Server 2003 bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="305a3-129">You must raise all domains in which you deploy Lync Server 2013 to a domain functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

<span data-ttu-id="305a3-130">Alle Gesamtstrukturen, in denen Sie lync Server 2013 bereitstellen, müssen auf eine Gesamtstrukturfunktionsebene von Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 oder mindestens Windows Server 2003 heraufgestuft werden.</span><span class="sxs-lookup"><span data-stu-id="305a3-130">All forests in which you deploy Lync Server 2013 must be raised to a forest functional level of Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, or at least Windows Server 2003.</span></span>

</div>

<div>

## <a name="support-for-read-only-domain-controllers"></a><span data-ttu-id="305a3-131">Unterstützung für Read-Only Domänencontroller</span><span class="sxs-lookup"><span data-stu-id="305a3-131">Support for Read-Only Domain Controllers</span></span>

<span data-ttu-id="305a3-132">Lync Server 2013 unterstützt die Bereitstellung von Active Directory-Domänendiensten mit schreibgeschützten Domänencontrollern oder schreibgeschützten globalen Katalogservern, sofern schreibbare Domänencontroller verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="305a3-132">Lync Server 2013 supports Active Directory Domain Services deployments that include read-only domain controllers or read-only global catalog servers, as long as there are writable domain controllers available.</span></span>

</div>

<div>

## <a name="domain-names"></a><span data-ttu-id="305a3-133">Domänennamen</span><span class="sxs-lookup"><span data-stu-id="305a3-133">Domain Names</span></span>

<span data-ttu-id="305a3-134">Lync Server unterstützt keine Single-Labeling-Domänen.</span><span class="sxs-lookup"><span data-stu-id="305a3-134">Lync Server does not support single-labeled domains.</span></span> <span data-ttu-id="305a3-135">Beispielsweise wird eine Gesamtstruktur mit einer Stammdomäne mit dem Namen **contoso. local** unterstützt, aber eine Stammdomäne mit dem Namen **local** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="305a3-135">For example, a forest with a root domain named **contoso.local** is supported, but a root domain named **local** is not supported.</span></span> <span data-ttu-id="305a3-136">Ausführliche Informationen finden Sie im Microsoft Knowledge Base-Artikel 300684, "Informationen zum Konfigurieren von Windows für Domänen mit DNS-Namen mit einer Bezeichnung" unter [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752) .</span><span class="sxs-lookup"><span data-stu-id="305a3-136">For details, see Microsoft Knowledge Base article 300684, “Information about configuring Windows for domains with single-label DNS names,” at [https://go.microsoft.com/fwlink/p/?linkId=143752](https://go.microsoft.com/fwlink/p/?linkid=143752).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="305a3-137">Lync Server unterstützt keine Umbenennung von Domänen.</span><span class="sxs-lookup"><span data-stu-id="305a3-137">Lync Server does not support renaming domains.</span></span> <span data-ttu-id="305a3-138">Wenn Sie eine Domäne umbenennen müssen, in der lync Server bereitgestellt wird, müssen Sie zunächst lync Server deinstallieren, dann die Domäne umbenennen und dann lync Server erneut installieren.</span><span class="sxs-lookup"><span data-stu-id="305a3-138">If you need to rename a domain where Lync Server is deployed, you need to first uninstall Lync Server, then rename the domain, and then reinstall Lync Server.</span></span>



</div>

</div>

<div>

## <a name="locked-down-ad-ds-environments"></a><span data-ttu-id="305a3-139">Gesperrte AD DS-Umgebungen</span><span class="sxs-lookup"><span data-stu-id="305a3-139">Locked Down AD DS Environments</span></span>

<span data-ttu-id="305a3-140">In einer gesperrten AD DS-Umgebung werden Benutzer und Computer Objekte häufig in bestimmten Organisationseinheiten (Organizational Units, OUs) mit deaktivierter Berechtigungsvererbung angeordnet, um eine sichere administrative Delegierung zu gewährleisten und die Verwendung von Gruppenrichtlinienobjekten (Group Policy Objects, GPOs) zu ermöglichen, um Sicherheitsrichtlinien durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="305a3-140">In a locked-down AD DS environment, Users and Computer objects are often placed in specific organizational units (OUs) with permissions inheritance disabled to help secure administrative delegation and to enable use of Group Policy objects (GPOs) to enforce security policies.</span></span> <span data-ttu-id="305a3-141">Lync Server 2013 kann in einer gesperrten Active Directory-Umgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="305a3-141">Lync Server 2013 can be deployed in a locked-down Active Directory environment.</span></span> <span data-ttu-id="305a3-142">Ausführliche Informationen dazu, was für die Bereitstellung von lync Server in einer gesperrten Umgebung erforderlich ist, finden Sie unter [Vorbereiten einer gesperrten Active Directory-Domänendienste in lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="305a3-142">For details about what is required to deploy Lync Server in a locked-down environment, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md) in the Deployment documentation.</span></span>

<span data-ttu-id="305a3-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="305a3-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

