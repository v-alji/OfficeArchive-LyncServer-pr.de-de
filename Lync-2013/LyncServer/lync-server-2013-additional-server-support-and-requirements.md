---
title: 'Lync Server 2013: Zusätzliche Serverunterstützung und Anforderungen'
description: 'Lync Server 2013: zusätzliche Server Unterstützung und-Anforderungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional server support and requirements
ms:assetid: 7622986b-abd6-4f45-8b5b-d5e2368521e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398577(v=OCS.15)
ms:contentKeyID: 48184535
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3af9b3489ba62b3b2dc7cf4fa16cabfe80003e1e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440010"
---
# <a name="additional-server-support-and-requirements-in-lync-server-2013"></a><span data-ttu-id="b34fc-103">Zusätzliche Serverunterstützung und Anforderungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b34fc-103">Additional server support and requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b34fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b34fc-104">

<span> </span></span></span>

<span data-ttu-id="b34fc-105">_**Letztes Änderungsdatum des Themas:** 2013-12-09_</span><span class="sxs-lookup"><span data-stu-id="b34fc-105">_**Topic Last Modified:** 2013-12-09_</span></span>

<span data-ttu-id="b34fc-106">Zusätzlich zu der Softwareunterstützung, die in den anderen Abschnitten dieser Dokumentation zur unter Stützungs Dokumentation beschrieben wird, weist lync Server 2013 die folgenden Supporteinschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="b34fc-106">In addition to the software support described in the other sections of this Supportability documentation, Lync Server 2013 has the following support limitations:</span></span>

  - <span data-ttu-id="b34fc-107">Lync Server 2013 unterstützt DNS (Domain Name System) und den Hardwarelastenausgleich für bestimmte Server Rollen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-107">Lync Server 2013 supports Domain Name System (DNS) and hardware load balancing for specific server roles.</span></span> <span data-ttu-id="b34fc-108">Sie unterstützt auch den Anwendungslastenausgleich für Vermittlungsserver, falls dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="b34fc-108">It also supports application load balancing for Mediation Servers, where appropriate.</span></span> <span data-ttu-id="b34fc-109">Einzelheiten zur Verwendung der einzelnen Informationen finden Sie in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b34fc-109">For details about when to use each, see the Planning documentation.</span></span>

  - <span data-ttu-id="b34fc-110">Lync Server 2013 verwendet das dlx (Distribution List Expansion Protocol) zum Erweitern von Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-110">Lync Server 2013 uses the Distribution List Expansion Protocol (DLX) to expand distribution lists.</span></span> <span data-ttu-id="b34fc-111">Dieses Protokoll gibt auch die Webdienstmethode an, die zum Abrufen der Mitgliedschaft einer Verteilerliste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-111">This protocol also specifies the web service method that is used to get the membership of a distribution list.</span></span> <span data-ttu-id="b34fc-112">Microsoft Exchange Server unterstützt dynamische Gruppen, denen keine Mitglieder statisch zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="b34fc-112">Microsoft Exchange Server supports dynamic groups that do not have members statically assigned to them.</span></span> <span data-ttu-id="b34fc-113">Stattdessen werden Abfragen gespeichert, die ausgewertet werden, wenn die Gruppe erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-113">Instead, they store queries that are evaluated when the group is expanded.</span></span> <span data-ttu-id="b34fc-114">DLX unterstützt keine dynamischen Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-114">DLX does not support dynamic distribution lists.</span></span> <span data-ttu-id="b34fc-115">Diese dlx-Einschränkung gilt für alle Versionen von lync Server.</span><span class="sxs-lookup"><span data-stu-id="b34fc-115">This DLX limitation applies to all versions of Lync Server.</span></span>

  - <span data-ttu-id="b34fc-116">Der Assistent zum Aktivieren des Benutzers unterstützt keine automatische Konvertierung von nicht englischen Zeichen in einen SIP-kompatiblen URI, daher müssen Sie die SIP-Adresse manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="b34fc-116">The Enable User Wizard does not support automatic conversion of non-English characters to a SIP-compliant URI, so you must modify the SIP address manually.</span></span>

  - <span data-ttu-id="b34fc-117">Informationen zu Servern, auf denen Antivirus-Software ausgeführt wird, finden Sie unter [Ausschlüsse für Antivirus-Scans für lync Server 2013](lync-server-2013-antivirus-scanning-exclusions.md) für vorgeschlagene Viren Ausschlüsse und andere sicherheitsrelevante Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-117">For servers running antivirus software, refer to [Antivirus scanning exclusions for Lync Server 2013](lync-server-2013-antivirus-scanning-exclusions.md) for suggested virus exclusions and other security related recommendations.</span></span>

  - <span data-ttu-id="b34fc-118">Wenn Sie IPSec verwenden, empfiehlt es sich, IPSec über die für Audio-und Videodatenverkehr verwendeten Portbereiche zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b34fc-118">If you use IPsec, we recommend disabling IPsec over the port ranges used for audio and video traffic.</span></span> <span data-ttu-id="b34fc-119">Ausführliche Informationen finden Sie unter [IPsec-Ausnahmen in lync Server 2013](lync-server-2013-ipsec-exceptions.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b34fc-119">For details, see [IPsec exceptions in Lync Server 2013](lync-server-2013-ipsec-exceptions.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="b34fc-120">Wenn Ihre Organisation eine QoS-Infrastruktur (Quality of Service) verwendet, wird das Mediensubsystem auf den Betrieb innerhalb der vorhandenen Infrastruktur ausgelegt.</span><span class="sxs-lookup"><span data-stu-id="b34fc-120">If your organization uses a Quality of Service (QoS) infrastructure, the media subsystem is designed to work within this existing infrastructure.</span></span> <span data-ttu-id="b34fc-121">Ausführliche Informationen zum Implementieren von QoS finden Sie unter [Verwalten von Quality of Service (QoS) in lync Server 2013](lync-server-2013-managing-quality-of-service-qos.md) in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b34fc-121">For details about implementing QoS, see [Managing Quality of Service (QoS) in Lync Server 2013](lync-server-2013-managing-quality-of-service-qos.md) in the Operations documentation.</span></span>

  - <span data-ttu-id="b34fc-122">Die Verwendung der Firewall des Betriebssystems wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b34fc-122">Use of the operating system firewall is supported.</span></span> <span data-ttu-id="b34fc-123">Lync Server 2013 verwaltet die Firewall-Ausnahmen für die Betriebssystem Firewall, mit Ausnahme der Microsoft SQL Server-Datenbanksoftware.</span><span class="sxs-lookup"><span data-stu-id="b34fc-123">Lync Server 2013 manages the firewall exceptions for the operating system firewall, except for Microsoft SQL Server database software.</span></span> <span data-ttu-id="b34fc-124">Details zu den Anforderungen der SQL Server-Firewall finden Sie in der SQL Server-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="b34fc-124">For details about SQL Server firewall requirements, see the SQL Server documentation.</span></span>

  - <span data-ttu-id="b34fc-125">Die externen Schnittstellen, die zum Implementieren der Unterstützung für den Zugriff durch externe Benutzer verwendet werden, müssen sich in einem separaten Subnetz befinden, *nicht* im gleichen Netzwerk wie die internen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-125">The external interfaces used to implement support for external user access must be on a separate subnet, *not* on the same network as the internal interfaces.</span></span>

  - <span data-ttu-id="b34fc-p106">Die XMPP-Fähigkeit von Lync Server 2013 wird von Microsoft für den Instant-Messaging-Partnerverbund mit Google Talk getestet und unterstützt. Wenden Sie sich bei anderen XMPP-Systemen an den Drittanbieter, um zu überprüfen, ob dieser den Partnerverbund mit Lync Server 2013 unterstützt, und Empfehlungen bei Bereitstellung und Problembehandlung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-p106">The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.</span></span>

  - <span data-ttu-id="b34fc-128">Mit der Veröffentlichung von lync Server 2013 kumulativen Updates: Juli 2013 unterstützt lync Server 2013 jetzt die zweistufige Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="b34fc-128">With the release of Lync Server 2013 Cumulative Updates: July 2013, Lync Server 2013 now supports two-factor authentication.</span></span> <span data-ttu-id="b34fc-129">Weitere Informationen finden Sie unter [zweistufige Authentifizierung in lync Server 2013](lync-server-2013-planning-for-and-deploying-two-factor-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="b34fc-129">For more information, see [Two-factor authentication in Lync Server 2013](lync-server-2013-planning-for-and-deploying-two-factor-authentication.md).</span></span>

  - <span data-ttu-id="b34fc-130">Für die meisten internen Server ist ein Zertifikattyp erforderlich, der als **Open Authentication** (OAuth) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b34fc-130">Most internal servers require a certificate type defined as **Open Authentication** (OAuth).</span></span> <span data-ttu-id="b34fc-131">Sie müssen während der **Anforderungs-, Installations-und** Zertifikat Phase des lync Server-Bereitstellungs-Assistenten ein OAuth-Zertifikat anfordern und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b34fc-131">You are required to request and assign an OAuth certificate during the **Request, Install and Assign Certificates** phase of the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="b34fc-132">Die Mindestgröße für einen OAuth-Zertifikatschlüssel lautet 1024-Bits.</span><span class="sxs-lookup"><span data-stu-id="b34fc-132">The minimum size for an OAuth certificate key is 1024 bits.</span></span> <span data-ttu-id="b34fc-133">Eine Warnung wird möglicherweise angezeigt, wenn Sie ein Zertifikat mit einer Schlüssellänge von weniger als 2048 Bits anfordern.</span><span class="sxs-lookup"><span data-stu-id="b34fc-133">A warning may be displayed if you request a certificate with a key length less than 2048 bits in length.</span></span> <span data-ttu-id="b34fc-134">Um potenzielle Probleme zu vermeiden, falls eine Schlüssellänge von 2048 anstelle einer Warnung erzwungen wird, wird dringend empfohlen, immer eine Schlüssellänge von 2048 für OAuth-Zertifikate zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b34fc-134">To avoid potential problems in the event that a key length of 2048 is enforced instead of warned, it is strongly recommended to always use a key length of 2048 for OAuth certificates.</span></span>

  - <span data-ttu-id="b34fc-135">Lync Server 2013 und Microsoft Exchange Server 2010 Service Pack 1 (SP1) funktionieren mit Unterstützung für FIPS (Federal Information Processing Standard) 140-2-Algorithmen, wenn die Windows Server 2008 R2-Betriebssysteme so konfiguriert sind, dass Sie die FIPS 140-2-Algorithmen für die Systemkryptografie verwenden.</span><span class="sxs-lookup"><span data-stu-id="b34fc-135">Lync Server 2013 and Microsoft Exchange Server 2010 Service Pack 1 (SP1) operate with support for Federal Information Processing Standard (FIPS) 140-2 algorithms if the Windows Server 2008 R2 operating systems are configured to use the FIPS 140-2 algorithms for system cryptography.</span></span> <span data-ttu-id="b34fc-136">Zum Implementieren der FIPS-Unterstützung müssen Sie jeden Server mit lync Server 2013 so konfigurieren, dass er unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-136">To implement FIPS support, you must configure each server running Lync Server 2013 to support it.</span></span> <span data-ttu-id="b34fc-137">Ausführliche Informationen zu FIPS-kompatiblen Algorithmen und zur Implementierung der FIPS-Unterstützung finden Sie im Microsoft Knowledge Base-Artikel 811833, "System Kryptographie: Verwenden von FIPS-kompatiblen Algorithmen für Verschlüsselung, Hashing und Signatur Sicherheit in Windows XP und späteren Windows-Versionen unter [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833) .</span><span class="sxs-lookup"><span data-stu-id="b34fc-137">For details about FIPS-compliant algorithms and how to implement FIPS support, see Microsoft Knowledge Base article 811833, "System cryptography: Use FIPS compliant algorithms for encryption, hashing, and signing security setting in Windows XP and in later versions of Windows at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833).</span></span> <span data-ttu-id="b34fc-138">Details zu FIPS 140-2-Unterstützung und Einschränkungen in Exchange 2010 finden Sie unter "Exchange 2010 SP1 und Unterstützung für FIPS-konforme Algorithmen" unter [https://go.microsoft.com/fwlink/p/?linkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335) .</span><span class="sxs-lookup"><span data-stu-id="b34fc-138">For details about FIPS 140-2 support and limitations in Exchange 2010, see "Exchange 2010 SP1 and Support for FIPS Compliant Algorithms" at [https://go.microsoft.com/fwlink/p/?linkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335).</span></span>

<span data-ttu-id="b34fc-139">Lync Server 2013 erfordert die Installation anderer Software auf bestimmten Komponenten vor oder während der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="b34fc-139">Lync Server 2013 requires the installation of other software on specific components prior to or during deployment.</span></span> <span data-ttu-id="b34fc-140">Dazu gehören Software, die mit dem Betriebssystem, herunterladbarer Software und Software zur Verfügung steht, die während der Installation von lync Server 2013 automatisch installiert wird.</span><span class="sxs-lookup"><span data-stu-id="b34fc-140">This includes software that is available with the operating system, downloadable software, and software that is automatically installed during installation of Lync Server 2013.</span></span> <span data-ttu-id="b34fc-141">Im folgenden finden Sie eine Liste zusätzlicher Software, die erforderlich sein kann:</span><span class="sxs-lookup"><span data-stu-id="b34fc-141">Following is a list of additional software that can be required:</span></span>

  - <span data-ttu-id="b34fc-142">Windows Update</span><span class="sxs-lookup"><span data-stu-id="b34fc-142">Windows Update</span></span>

  - <span data-ttu-id="b34fc-143">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="b34fc-143">Windows Identity Foundation</span></span>

  - <span data-ttu-id="b34fc-144">Microsoft .NET 4,5-Framework</span><span class="sxs-lookup"><span data-stu-id="b34fc-144">Microsoft .NET 4.5 Framework</span></span>

  - <span data-ttu-id="b34fc-145">Microsoft Visual C++ 2012 Redistributable</span><span class="sxs-lookup"><span data-stu-id="b34fc-145">Microsoft Visual C++ 2012 Redistributable</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b34fc-146">Microsoft Visual C++ 2012 Redistributable wird automatisch installiert, wenn Sie lync Server 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="b34fc-146">Microsoft Visual C++ 2012 Redistributable is automatically installed when you install Lync Server 2013.</span></span> <span data-ttu-id="b34fc-147">Sie sollten keine andere Version installieren und verwenden.</span><span class="sxs-lookup"><span data-stu-id="b34fc-147">You should not install and use any other version.</span></span>

    
    </div>

  - <span data-ttu-id="b34fc-148">URL-umschreibungs Modul, Version 2,0, verteilbare</span><span class="sxs-lookup"><span data-stu-id="b34fc-148">URL Rewrite Module version 2.0 Redistributable</span></span>

  - <span data-ttu-id="b34fc-149">Windows Media Format-Laufzeitkomponente</span><span class="sxs-lookup"><span data-stu-id="b34fc-149">Windows Media Format Runtime</span></span>

  - <span data-ttu-id="b34fc-150">Windows PowerShell, Version 3,0</span><span class="sxs-lookup"><span data-stu-id="b34fc-150">Windows PowerShell version 3.0</span></span>

  - <span data-ttu-id="b34fc-151">Microsoft Silverlight 4-Browser-Plug-in (Silverlight-4.0.50524.0 oder die neueste Version der lync Server-Systemsteuerung)</span><span class="sxs-lookup"><span data-stu-id="b34fc-151">Microsoft Silverlight 4 browser plug-in (Silverlight 4.0.50524.0 or the latest version for Lync Server Control Panel)</span></span>

  - <span data-ttu-id="b34fc-152">Tools für Active Directory-Domänendienste</span><span class="sxs-lookup"><span data-stu-id="b34fc-152">Active Directory Domain Services tools</span></span>

<span data-ttu-id="b34fc-153">Einige dieser Softwareanforderungen gelten nur für bestimmte Serverrollen oder Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b34fc-153">Some of these software requirements only apply to specific server roles or components.</span></span> <span data-ttu-id="b34fc-154">Details zu diesen Softwareanforderungen finden Sie unter [zusätzliche Softwareanforderungen für lync Server 2013](lync-server-2013-additional-software-requirements.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b34fc-154">For details about these software requirements, see [Additional software requirements for Lync Server 2013](lync-server-2013-additional-software-requirements.md) in the Planning documentation.</span></span>

<span data-ttu-id="b34fc-155"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b34fc-155"></div>

<span> </span>

</div>

</div>

</span></span></div>

