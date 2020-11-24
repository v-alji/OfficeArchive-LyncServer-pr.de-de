---
title: 'Lync Server 2013: Schritte zur Vorbereitung und Bereitstellung einer Lync Server-Hybridumgebung'
description: 'Lync Server 2013: Schritte zum Vorbereiten und Bereitstellen der lync Server-Hybridumgebung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Steps to prepare and deploy Lync Server 2013 hybrid environment
ms:assetid: a50d4f7b-63f4-4663-af63-56ca87e4e3e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205157(v=OCS.15)
ms:contentKeyID: 48185060
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ffb791a8a45b2220d8987c8d688f346447747c00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393946"
---
# <a name="steps-to-prepare-and-deploy-lync-server-2013-hybrid-environment"></a><span data-ttu-id="95b78-103">Schritte zur Vorbereitung und Bereitstellung einer Lync Server 2013-Hybridumgebung</span><span class="sxs-lookup"><span data-stu-id="95b78-103">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="95b78-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="95b78-104">

<span> </span></span></span>

<span data-ttu-id="95b78-105">_**Letztes Änderungsdatum des Themas:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="95b78-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="95b78-106">In der folgenden Tabelle sind die erforderlichen Schritte zum Vorbereiten Ihrer Umgebung für eine hybridbereitstellung mit Skype for Business Online und Microsoft Office 365 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="95b78-106">The following table lists the steps required to prepare your environment for a hybrid deployment with Skype for Business Online and Microsoft Office 365.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95b78-107">Abgeschlossen?</span><span class="sxs-lookup"><span data-stu-id="95b78-107">Completed?</span></span></th>
<th><span data-ttu-id="95b78-108">Schritt</span><span class="sxs-lookup"><span data-stu-id="95b78-108">Step</span></span></th>
<th><span data-ttu-id="95b78-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95b78-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="95b78-110">Erstellen eines Mandanten Kontos für Office 365 und Aktivieren von lync Online</span><span class="sxs-lookup"><span data-stu-id="95b78-110">Create a tenant account for Office 365 and enable Lync Online</span></span></p></td>
<td><p><span data-ttu-id="95b78-111">Informationen zu Office 365 und lync Online finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-111">Learn about Office 365 and Lync Online at <a href="https://go.microsoft.com/fwlink/p/?linkid=254980">Office 365</a>.</span></span></p>
<p><span data-ttu-id="95b78-112">Wenn Sie sicherstellen möchten, dass Ihre Umgebung für Office 365 bereit ist, lesen Sie die <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Anforderungen</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-112">To make sure that your environment is ready for Office 365, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=401408">System Requirements</a>.</span></span></p>
<p><span data-ttu-id="95b78-113">Details zum Einrichten von Office 365 finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Erste Schritte mit Office 365</a> und <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Einrichten von Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-113">For details about setting up Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254982">Getting Started with Office 365</a> and <a href="https://go.microsoft.com/fwlink/p/?linkid=254979">Set Up Office 365</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="95b78-114">Hinzufügen einer Domäne und Überprüfen des Domänenbesitzes</span><span class="sxs-lookup"><span data-stu-id="95b78-114">Add your domain and verify ownership</span></span></p></td>
<td><p><span data-ttu-id="95b78-115">Ihre Domäne wird manchmal auch als <em>Vanity-Domäne</em> bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="95b78-115">Your domain is sometimes also referred to as your <em>vanity domain</em>.</span></span> <span data-ttu-id="95b78-116">Sie müssen Ihre Domäne zu Ihrer Office 365-Organisation hinzufügen und dann die Schritte zum Überprüfen der Domäne mit Office 365 ausführen.</span><span class="sxs-lookup"><span data-stu-id="95b78-116">You must add your domain to your Office 365 organization, and then follow the steps to validate the domain with Office 365.</span></span> <span data-ttu-id="95b78-117">Anhand dieser Schritte soll bestätigt werden, dass Sie der Besitzer der Domäne sind.</span><span class="sxs-lookup"><span data-stu-id="95b78-117">This is to confirm that you are the owner of the domain.</span></span></p>
<p><span data-ttu-id="95b78-118">Wenn Sie Ihre Domäne zu Ihrer Office 365-Organisation hinzufügen möchten, führen Sie die unter <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Hinzufügen Ihrer Domäne zu Office 365</a>beschriebenen Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="95b78-118">To add your domain to your Office 365 organization, follow the steps described at <a href="https://go.microsoft.com/fwlink/p/?linkid=254983">Add your domain to Office 365</a>.</span></span></p>
<p><span data-ttu-id="95b78-119">Führen Sie alle Schritte in jedem Abschnitt des Themas aus, einschließlich &quot; Bearbeiten von DNS-Einträgen für Ihre Office 365-Dienste.&quot;</span><span class="sxs-lookup"><span data-stu-id="95b78-119">Complete all of the steps in each section in the topic, including &quot;Edit DNS records for your Office 365 services.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="95b78-120">Überprüfen der Umgebungs Bereitschaft</span><span class="sxs-lookup"><span data-stu-id="95b78-120">Verify environment readiness</span></span></p></td>
<td><p><span data-ttu-id="95b78-121">Sie können den Office 365-Setup-Assistenten verwenden, um die Bereitstellung von Office 365 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95b78-121">You can use the Office 365 Setup Assistant to help you deploy Office 365.</span></span> <span data-ttu-id="95b78-122">Weitere Informationen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Verwenden des Setup-Assistenten zum Ermitteln der Bereitschaft von Office 365</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-122">For more information, see <a href="https://go.microsoft.com/fwlink/p/?linkid=254985">Use Setup Assistant to determine Office 365 readiness</a>.</span></span></p>
<p><span data-ttu-id="95b78-123">Details zur Verwendung des Tools und zur Bereitstellung von Office 365 finden Sie im <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365-Bereitstellungshandbuch</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-123">For details about using the tool and deploying Office 365, see <a href="https://go.microsoft.com/fwlink/p/?linkid=257337">Office 365 deployment guide</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="95b78-124">Vorbereiten der Active Directory-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="95b78-124">Prepare for Active Directory synchronization</span></span></p></td>
<td><p><span data-ttu-id="95b78-125">Die Active Directory-Synchronisierung sorgt dafür, dass Ihr lokales Active Directory kontinuierlich mit Office 365 synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="95b78-125">Active Directory synchronization keeps your on-premises Active Directory continuously synchronized with Office 365.</span></span> <span data-ttu-id="95b78-126">Auf diese Weise können Sie synchronisierte Versionen der einzelnen Benutzerkonten und Gruppen erstellen und außerdem die Synchronisierung der globalen Adressliste (GAL) von Ihrer lokalen Microsoft Exchange Server-Umgebung zu Microsoft Exchange Online aktivieren.</span><span class="sxs-lookup"><span data-stu-id="95b78-126">This lets you create synchronized versions of each user account and group, and also enables global address list (GAL) synchronization from your local Microsoft Exchange Server environment to Microsoft Exchange Online.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="95b78-127">Sie müssen die Ad-Konten für alle lync-Benutzer in Ihrer Organisation zwischen Ihren lokalen und Online lync-Bereitstellungen synchronisieren, auch wenn Benutzer nicht nach lync Online verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="95b78-127">You need to synchronize the AD accounts for all Lync users in your organization between your on-premises and online Lync deployments, even if users are not moved to Lync Online.</span></span> <span data-ttu-id="95b78-128">Wenn Sie nicht alle Benutzer synchronisieren, funktioniert die Kommunikation zwischen lokalen und Onlinebenutzern in Ihrem Unternehmen möglicherweise nicht erwartungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="95b78-128">If you do not synchronize all users, communication between on-premises and online users in your organization may not work as expected.</span></span>


</div>
<p><span data-ttu-id="95b78-129">Wenn Sie Ihre Umgebung für die Active Directory-Synchronisierung vorbereiten möchten, führen Sie die in der Roadmap für die <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Verzeichnissynchronisierung</a>beschriebenen Schritte aus, einschließlich der Einrichtung einer einmaligen Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="95b78-129">To prepare your environment for Active Directory synchronization, follow the steps described in <a href="https://go.microsoft.com/fwlink/p/?linkid=254988">Directory synchronization Roadmap</a>, including setting up single sign-on.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="95b78-130">Erstellen von Zertifikaten für Active Directory-Verbunddienste (AD FS)</span><span class="sxs-lookup"><span data-stu-id="95b78-130">Create certificates for Active Directory Federation Services (AD FS)</span></span></p></td>
<td><p><span data-ttu-id="95b78-131">Sie müssen die Zertifikate erstellen, die für den Identitätsverbund mit Office 365 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95b78-131">You will need to create the certificates that are used for identity federation with Office 365.</span></span> <span data-ttu-id="95b78-132">Weitere Informationen finden Sie im Abschnitt "Verbundserver Zertifikate" im Abschnitt Planen und Bereitstellen von AD FS für die Verwendung mit einmaligem Anmelden unter <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checkliste: Verwenden von AD FS zum Implementieren und Verwalten des einmaligen Anmeldens</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-132">For more information, see the “Federation server certificates” section of the Plan for and deploy AD FS for use with single sign-on topic at <a href="https://go.microsoft.com/fwlink/p/?linkid=285376">Checklist: Use AD FS to implement and manage single sign-on</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="95b78-133">Zuweisen von Zertifikaten für AD FS</span><span class="sxs-lookup"><span data-stu-id="95b78-133">Assign certificates for AD FS</span></span></p></td>
<td><p><span data-ttu-id="95b78-134">Nachdem Sie die für den Identitätsverbund mit Office 365 verwendeten Zertifikate erstellt haben, müssen Sie diese installieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="95b78-134">After you create the certificates that are used for identity federation with Office 365, you must install and assign them.</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="95b78-135">Verschieben von Pilotbenutzern in Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="95b78-135">Move pilot users to Skype for Business Online</span></span></p></td>
<td><p><span data-ttu-id="95b78-136">Nachdem Sie die Schritte zum Vorbereiten und Konfigurieren Ihrer Umgebung für Skype for Business Online abgeschlossen haben, können Sie mit dem Verschieben von Pilotbenutzern nach lync Online beginnen.</span><span class="sxs-lookup"><span data-stu-id="95b78-136">After you have completed the steps to prepare and configure your environment for Skype for Business Online, you can start moving pilot users to Lync Online.</span></span></p>
<p><span data-ttu-id="95b78-137">Informationen finden Sie unter <a href="lync-server-2013-move-users-to-lync-online.md">Verschieben von Benutzern nach lync Online in lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-137">See <a href="lync-server-2013-move-users-to-lync-online.md">Move users to Lync Online in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="95b78-138">Verwalten von Benutzern in einer Hybridbereitstellung</span><span class="sxs-lookup"><span data-stu-id="95b78-138">Administering users in a hybrid deployment</span></span></p></td>
<td><p><span data-ttu-id="95b78-139">Details zum Verwalten von Benutzern in einer hybridbereitstellung finden Sie unter Verwalten von <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Benutzern in einer hybriden lync Server 2013-Bereitstellung</a>.</span><span class="sxs-lookup"><span data-stu-id="95b78-139">For details about how to administer users in a hybrid deployment, see <a href="lync-server-2013-administering-users-in-a-hybrid-deployment.md">Administering users in a hybrid Lync Server 2013 deployment</a>.</span></span></p></td>
</tr><span data-ttu-id="95b78-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="95b78-140">
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

