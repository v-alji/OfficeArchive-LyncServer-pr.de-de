---
title: 'Lync Server 2013: bewährte Methoden für Ihre Kerninfrastruktur'
description: 'Lync Server 2013: bewährte Methoden für Ihre Kerninfrastruktur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for your core infrastructure in Lync Server 2013
ms:assetid: 44aff88d-536c-4613-a81e-5398c9c6a648
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518328(v=OCS.15)
ms:contentKeyID: 61071242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0ea7cb9c7685a3b6f7c04146ec5631bbac10fe6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436041"
---
# <a name="best-practices-for-your-core-infrastructure-in-lync-server-2013"></a><span data-ttu-id="eda76-103">Bewährte Methoden für Ihre Kerninfrastruktur in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eda76-103">Best practices for your core infrastructure in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eda76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eda76-104">

<span> </span></span></span>

<span data-ttu-id="eda76-105">_**Letztes Änderungsdatum des Themas:** 2014-01-27_</span><span class="sxs-lookup"><span data-stu-id="eda76-105">_**Topic Last Modified:** 2014-01-27_</span></span>

<span data-ttu-id="eda76-106">Sie haben wahrscheinlich bereits Schritte unternommen, um Fehlertoleranz in Ihrem System zu entwerfen, und Verfahren wie das Sicherstellen von Hardwareredundanz, Schutzmaßnahmen gegen Stromausfälle, Routineinstallation von Sicherheitsupdates und Antivirenmaßnahmen sowie Monitoring Server-Aktivitäten verwendet.</span><span class="sxs-lookup"><span data-stu-id="eda76-106">You have probably already taken steps to design fault tolerance in your system, using practices such as ensuring hardware redundancy, guarding against power loss, routinely installing security updates and antivirus measures, and Monitoring Server activity.</span></span> <span data-ttu-id="eda76-107">Diese Vorgehensweisen nutzen nicht nur Ihre Microsoft lync Server 2013-Infrastruktur, sondern auch Ihr gesamtes Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="eda76-107">These practices benefit not only your Microsoft Lync Server 2013 infrastructure, but also your entire network.</span></span> <span data-ttu-id="eda76-108">Wenn Sie diese Methoden nicht implementiert haben, empfiehlt es sich, dies vor der Bereitstellung von lync Server 2013 zu tun.</span><span class="sxs-lookup"><span data-stu-id="eda76-108">If you have not implemented these practices, we recommend that you do so before deploying Lync Server 2013.</span></span>

<span data-ttu-id="eda76-109">Gehen Sie wie folgt vor, um die Server in ihrer lync Server 2013-Bereitstellung vor versehentlichen oder zielgerichteten Verletzungen zu schützen, die zu Ausfallzeiten führen können:</span><span class="sxs-lookup"><span data-stu-id="eda76-109">To help protect the servers in your Lync Server 2013 deployment from accidental or purposeful harm that might result in downtime, take the following precautions:</span></span>

  - <span data-ttu-id="eda76-110">Halten Sie Ihre Server mit Sicherheitsupdates auf dem neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="eda76-110">Keep your servers up-to-date with security updates.</span></span> <span data-ttu-id="eda76-111">Mit einem Abonnement für den Microsoft Security Notification Service können Sie sicherstellen, dass Sie bei Veröffentlichungen von Sicherheitsbulletins für alle Microsoft-Produkte sofort benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="eda76-111">Subscribing to the Microsoft Security Notification Service helps ensure that you receive immediate notification of security bulletin releases for any Microsoft product.</span></span> <span data-ttu-id="eda76-112">Wenn Sie sich anmelden möchten, wechseln Sie zur Microsoft Technical Security Notifications-Website unter [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202) .</span><span class="sxs-lookup"><span data-stu-id="eda76-112">To subscribe, go to the Microsoft Technical Security Notifications website at [https://go.microsoft.com/fwlink/p/?LinkId=145202](https://go.microsoft.com/fwlink/p/?linkid=145202).</span></span>

  - <span data-ttu-id="eda76-113">Achten Sie darauf, dass Zugriffsrechte ordnungsgemäß eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="eda76-113">Ensure that access rights are set up correctly.</span></span>

  - <span data-ttu-id="eda76-p103">Stellen Sie Ihre Server in einer physischen Umgebung auf, die einen nicht autorisierten Zugriff verhindert. Stellen Sie sicher, dass angemessene Antivirensoftware auf allen Servern installiert ist. Halten Sie die Software mit den neuesten Virussignaturdateien auf dem neuesten Stand. Verwenden Sie die Funktion für automatische Updates Ihrer Antivirenanwendung, um die Virussignaturen aktuell zu halten.</span><span class="sxs-lookup"><span data-stu-id="eda76-p103">Keep your servers in a physical environment that prevents unauthorized access. Ensure that adequate antivirus software is installed on all your servers. Keep the software up-to-date with the latest virus signature files. Use the automatic update feature of your antivirus application to keep the virus signatures current.</span></span>

  - <span data-ttu-id="eda76-118">Wir empfehlen, dass Sie die Windows Server-Betriebssystemdienste deaktivieren, die auf den Computern, auf denen Sie lync Server 2013 installieren, nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eda76-118">We recommend that you disable the Windows Server operating system services that are not required on the computers where you install Lync Server 2013.</span></span>

  - <span data-ttu-id="eda76-119">Verschlüsseln Sie Betriebssysteme und Festplattenlaufwerke, auf denen Daten gespeichert sind, mit einem Verschlüsselungssystem für das gesamte Volume, es sei denn, Sie können eine beständige und vollständige Kontrolle der Server, vollkommene physische Isolation und das ordnungsgemäße und sichere Außerbetriebsetzen von ausgetauschten oder ausgefallenen Festplattenlaufwerken sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="eda76-119">Encrypt operating systems and disk drives where data is stored with a full-volume encryption system, unless you can guarantee constant and complete control of the servers, total physical isolation, and proper and secure decommissioning of replaced or failed disk drives.</span></span>

  - <span data-ttu-id="eda76-120">Deaktivieren Sie alle externen Ports für den direkten Speicherzugriff des Servers, es sei denn, Sie können eine sehr enge Kontrolle des physischen Zugriffs auf die Server sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="eda76-120">Disable all external Direct Memory Access (DMA) ports of the server, unless you can guarantee very tight control over the physical access to the servers.</span></span> <span data-ttu-id="eda76-121">Angriffe auf der Basis von direktem Speicher, die realtiv einfach initiiert werden können, könnten sehr vertrauliche Informationen wie private Verschlüsselungsschlüssel offenlegen.</span><span class="sxs-lookup"><span data-stu-id="eda76-121">DMA-based attacks, which can be initiated fairly easily, could expose very sensitive information, such as private encryption keys.</span></span>

<span data-ttu-id="eda76-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eda76-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

