---
title: 'Lync Server 2013: Übersicht über Best Practices Analyzer'
description: 'Lync Server 2013: Übersicht über Best Practices Analyzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Best Practices Analyzer
ms:assetid: c5fcaa05-eb1c-4092-90ad-177b127e795b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591349(v=OCS.15)
ms:contentKeyID: 48185364
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0ea48e88b26fa1081e5770fef2ac24efc21b74cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445155"
---
# <a name="overview-of-best-practices-analyzer-in-lync-server-2013"></a><span data-ttu-id="70666-103">Übersicht über Best Practices Analyzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70666-103">Overview of Best Practices Analyzer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70666-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70666-104">

<span> </span></span></span>

<span data-ttu-id="70666-105">_**Letztes Änderungsdatum des Themas:** 2012-09-19_</span><span class="sxs-lookup"><span data-stu-id="70666-105">_**Topic Last Modified:** 2012-09-19_</span></span>

<span data-ttu-id="70666-106">Sie können lync Server 2013, Best Practices Analyzer verwenden, um Probleme mit der Bereitstellung von lync Server 2013 zu identifizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="70666-106">You can use Lync Server 2013, Best Practices Analyzer to identify and resolve problems with your Lync Server 2013 deployment.</span></span> <span data-ttu-id="70666-107">Der lync Server 2013, Best Practices Analyzer, sammelt Konfigurationsinformationen aus lync Server 2013-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="70666-107">The Lync Server 2013, Best Practices Analyzer gathers configuration information from Lync Server 2013 components.</span></span>

<span data-ttu-id="70666-108">Mit dem richtigen Netzwerkzugriff kann der Best Practices Analyzer Server untersuchen, die Active Directory-Domänendienste, Exchange Server Unified Messaging (um) und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="70666-108">With the proper network access, the Best Practices Analyzer can examine servers running Active Directory Domain Services, Exchange Server Unified Messaging (UM), and Lync Server 2013.</span></span> <span data-ttu-id="70666-109">Sie können Best Practices Analyzer verwenden, um folgende Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="70666-109">You can use Best Practices Analyzer to do the following:</span></span>

  - <span data-ttu-id="70666-110">Proaktive Prüfungen durchführen und überprüfen, ob die Konfiguration entsprechend den empfohlenen bewährten Methoden festgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="70666-110">Proactively perform checks, verifying that the configuration is set according to recommended best practices.</span></span>

  - <span data-ttu-id="70666-111">Sie müssen die erforderlichen Updates für lync Server 2013 automatisch erkennen.</span><span class="sxs-lookup"><span data-stu-id="70666-111">Automatically detect required updates to Lync Server 2013.</span></span>

  - <span data-ttu-id="70666-112">Erstellen Sie eine Liste der Probleme, wie etwa suboptimale Konfigurationseinstellungen, nicht unterstützte Optionen, fehlende Updates oder Methoden, die wir nicht empfehlen.</span><span class="sxs-lookup"><span data-stu-id="70666-112">Generate a list of issues, such as suboptimal configuration settings, unsupported options, missing updates, or practices that we do not recommend.</span></span>

  - <span data-ttu-id="70666-113">Hilft Ihnen bei der Behebung und Behebung spezifischer Probleme.</span><span class="sxs-lookup"><span data-stu-id="70666-113">Help you troubleshoot and fix specific problems.</span></span>

<span data-ttu-id="70666-114">Best Practices Analyzer bietet die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="70666-114">Best Practices Analyzer provides the following features:</span></span>

  - <span data-ttu-id="70666-115">Minimale Installationsvoraussetzungen.</span><span class="sxs-lookup"><span data-stu-id="70666-115">Minimal installation prerequisites.</span></span>

  - <span data-ttu-id="70666-116">Online Dokumentation zu gemeldeten Problemen, einschließlich Tipps zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="70666-116">Online documentation about reported issues, including troubleshooting tips.</span></span>

  - <span data-ttu-id="70666-117">Konfigurationsinformationen, die Sie für eine spätere Überprüfung speichern können.</span><span class="sxs-lookup"><span data-stu-id="70666-117">Configuration information that you can save for later review.</span></span>

  - <span data-ttu-id="70666-118">Modernste Systemanalyse.</span><span class="sxs-lookup"><span data-stu-id="70666-118">State-of-the-art system analysis.</span></span>

<span data-ttu-id="70666-119">Best Practices Analyzer verwendet eine Reihe von XML-Konfigurationsdateien, um die Informationen zu ermitteln, die von ihrer lync Server 2013-Umgebung gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="70666-119">Best Practices Analyzer uses a set of XML configuration files to determine the information to gather from your Lync Server 2013 environment.</span></span> <span data-ttu-id="70666-120">Neben der Überprüfung der Active Directory-Domänendienste werden Quellen wie die Registrierung des Windows Server-Betriebssystems und die Einstellungen in Windows-Verwaltungsinstrumentation (WMI) überprüft.</span><span class="sxs-lookup"><span data-stu-id="70666-120">In addition to checking Active Directory Domain Services, it checks sources such as the Windows Server operating system registry and settings in Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="70666-121">Best Practices Analyzer vergleicht die gesammelten Daten mit einer Reihe vordefinierter Regeln für die Einstellungen und Konfigurationen von lync Server 2013-Bereitstellungen.</span><span class="sxs-lookup"><span data-stu-id="70666-121">Best Practices Analyzer compares the data it gathers with a set of predefined rules for the settings and configurations of Lync Server 2013 deployments.</span></span>

<span data-ttu-id="70666-122">Nach dem Vergleich der gesammelten Daten mit den vordefinierten Regeln meldet das Tool Probleme.</span><span class="sxs-lookup"><span data-stu-id="70666-122">After comparing the collected data with the predefined rules, the tool reports issues.</span></span> <span data-ttu-id="70666-123">Für jedes von ihm gemeldete Problem bietet Best Practices Analyzer Informationen dazu, was in der gescannten lync Server 2013-Umgebung und der empfohlenen Konfiguration gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="70666-123">For every issue that it reports, Best Practices Analyzer provides information about what was found in the scanned Lync Server 2013 environment and the recommended configuration.</span></span> <span data-ttu-id="70666-124">Best Practices Analyzer enthält auch Links zu ausführlicheren Informationen zu den spezifischen Problemen.</span><span class="sxs-lookup"><span data-stu-id="70666-124">Best Practices Analyzer also provides links to more detailed information about the specific issues.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="70666-125">Der lync Server 2013, Best Practices Analyzer, sammelt Konfigurationsinformationen nur von lync Server 2013-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="70666-125">The Lync Server 2013, Best Practices Analyzer gathers configuration information only from Lync Server 2013 components.</span></span> <span data-ttu-id="70666-126">Sie können die vorherigen Versionen des Tools verwenden, um frühere Umgebungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="70666-126">You can use the previous versions of the tool to scan previous environments.</span></span> <span data-ttu-id="70666-127">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Voraussetzungen für die Ausführung von Best Practices Analyzer in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="70666-127">For details, see <A href="lync-server-2013-requirements-for-running-best-practices-analyzer.md">Requirements for running Best Practices Analyzer in Lync Server 2013</A>.</span></span>



<span data-ttu-id="70666-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70666-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

