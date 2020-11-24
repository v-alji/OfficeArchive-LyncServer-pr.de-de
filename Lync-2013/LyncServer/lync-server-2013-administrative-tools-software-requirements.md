---
title: 'Lync Server 2013: Softwareanforderungen für Verwaltungstools'
description: 'Lync Server 2013: Softwareanforderungen für Verwaltungstools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administrative tools software requirements
ms:assetid: 2fb172c3-7b84-4e49-981c-2a17e7a00a29
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg195653(v=OCS.15)
ms:contentKeyID: 48183740
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c723d56cbda0c171fab206e3bcd3b2da0cc5b4b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393863"
---
# <a name="administrative-tools-software-requirements-in-lync-server-2013"></a><span data-ttu-id="2c12b-103">Softwareanforderungen für Verwaltungstools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c12b-103">Administrative tools software requirements in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2c12b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2c12b-104">

<span> </span></span></span>

<span data-ttu-id="2c12b-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="2c12b-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="2c12b-106">In diesem Thema wird die Software beschrieben, die für die Installation und Verwendung von lync Server 2013-Verwaltungstools zusätzlich zu den Betriebssystemanforderungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2c12b-106">This topic describes the software required to install and use Lync Server 2013 administrative tools in addition to the operating system requirements.</span></span>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="2c12b-107">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="2c12b-107">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="2c12b-108">Die 64-Bit-Version von Microsoft .NET Framework 4,5 ist für lync Server 2013 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c12b-108">The 64-bit edition of Microsoft .NET Framework 4.5 is required for Lync Server 2013.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="2c12b-109">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="2c12b-109">Windows PowerShell 3.0</span></span>

<span data-ttu-id="2c12b-110">Windows PowerShell 3,0 ist für die Ausführung einer beliebigen Komponente von Microsoft lync Server 2013 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c12b-110">Windows PowerShell 3.0 is required for running any component of Microsoft Lync Server 2013.</span></span> <span data-ttu-id="2c12b-111">Weitere Informationen finden Sie unter [Installieren von Windows PowerShell 3,0 für lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="2c12b-111">For more information, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="windows-installer-version-45"></a><span data-ttu-id="2c12b-112">Windows Installer, Version 4,5</span><span class="sxs-lookup"><span data-stu-id="2c12b-112">Windows Installer Version 4.5</span></span>

<span data-ttu-id="2c12b-113">Lync Server 2013 verwendet die Windows Installer-Technologie, um verschiedene Server Rollen zu installieren, zu deinstallieren und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="2c12b-113">Lync Server 2013 uses Windows Installer technology to install, uninstall, and maintain various server roles.</span></span> <span data-ttu-id="2c12b-114">Windows Installer, Version 4,5, steht als verteilbare Komponente für das Windows Server-Betriebssystem zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2c12b-114">Windows Installer version 4.5 is available as a redistributable component for the Windows Server operating system.</span></span> <span data-ttu-id="2c12b-115">Windows Installer 4,5 wird mit Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2 ausgeliefert, was bedeutet, dass Sie das Dienstprogramm nicht für einen Computer herunterladen müssen, auf dem lync Server 2013 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c12b-115">Windows Installer 4.5 ships with Windows Server 2012 R2, Windows Server 2012, and Windows Server 2008 R2 meaning that you do not need to download the utility for any computer that is running Lync Server 2013.</span></span> <span data-ttu-id="2c12b-116">(Lync Server 2013 kann nur auf Computern mit Windows Server 2012 R2, Windows Server 2012 oder Windows Server 2008 R2 installiert werden.)</span><span class="sxs-lookup"><span data-stu-id="2c12b-116">(Lync Server 2013 can only be installed on computers running Windows Server 2012 R2, Windows Server 2012 or Windows Server 2008 R2.)</span></span>

<span data-ttu-id="2c12b-117">Wenn Sie jedoch die lync Server-Verwaltungsshell oder den lync Server Topology Builder auf einer Administratorarbeitsstation installieren möchten, müssen Sie möglicherweise Windows Installer 4,5 herunterladen.</span><span class="sxs-lookup"><span data-stu-id="2c12b-117">However, if you want to install Lync Server Management Shell or Lync Server Topology Builder on an administrator workstation you might need to download Windows Installer 4.5.</span></span> <span data-ttu-id="2c12b-118">Dieses Dienstprogramm wird mit Windows 7 und Windows 2008 R2 ausgeliefert, jedoch nicht mit früheren Versionen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="2c12b-118">That utility ships with Windows 7 and Windows 2008 R2 but not with any previous versions of the Windows operating system.</span></span> <span data-ttu-id="2c12b-119">Sie können Windows Installer 4,5 aus dem Microsoft Download Center herunterladen <https://go.microsoft.com/fwlink/p/?linkid=197395> .</span><span class="sxs-lookup"><span data-stu-id="2c12b-119">You can download Windows Installer 4.5 from the Microsoft Download Center at <https://go.microsoft.com/fwlink/p/?linkid=197395>.</span></span>

</div>

<div>

## <a name="microsoft-silverlight-5-browser-plug-in"></a><span data-ttu-id="2c12b-120">Microsoft Silverlight 5-Browser-Plug-in</span><span class="sxs-lookup"><span data-stu-id="2c12b-120">Microsoft Silverlight 5 browser plug-in</span></span>

<span data-ttu-id="2c12b-121">Die lync Server 2013-Systemsteuerung ist ein webbasiertes Tool und erfordert, dass Sie die neueste Version des Microsoft Silverlight 5-Browser-Plug-ins installieren.</span><span class="sxs-lookup"><span data-stu-id="2c12b-121">Lync Server 2013 Control Panel is a web-based tool and requires that you install the latest version of Microsoft Silverlight 5 browser plug-in.</span></span> <span data-ttu-id="2c12b-122">Wenn Sie die lync Server 2013-Systemsteuerung starten, wenn diese Software nicht installiert ist oder wenn eine frühere Version installiert ist, werden Sie in der Systemsteuerung von lync Server 2013 aufgefordert, die erforderliche Version zu installieren.</span><span class="sxs-lookup"><span data-stu-id="2c12b-122">When you start Lync Server 2013 Control Panel, if this software is not installed or if an earlier version is installed, Lync Server 2013 Control Panel prompts you to install the required version.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2c12b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c12b-123">See Also</span></span>


[<span data-ttu-id="2c12b-124">Betriebssystemunterstützung für Server und Tools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c12b-124">Server and tools operating system support in Lync Server 2013</span></span>](lync-server-2013-server-and-tools-operating-system-support.md)  


[<span data-ttu-id="2c12b-125">Infrastrukturanforderungen für Verwaltungstools in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c12b-125">Administrative tools infrastructure requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-infrastructure-requirements.md)  
[<span data-ttu-id="2c12b-126">Erforderliche Administratorrechte und Gruppenmitgliedschaften für die Installation und Verwaltung von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2c12b-126">Administrator rights and permissions required for setup and administration of Lync Server 2013</span></span>](lync-server-2013-administrator-rights-and-permissions-required-for-setup-and-administration.md)  
  

<span data-ttu-id="2c12b-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2c12b-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

