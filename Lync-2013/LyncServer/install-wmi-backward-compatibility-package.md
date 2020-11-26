---
title: Installieren des WMI-abwärts Kompatibilitätspakets
description: Installieren Sie das WMI-abwärts Kompatibilitätspaket.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439579"
---
# <a name="install-wmi-backward-compatibility-package"></a><span data-ttu-id="ffec8-103">Installieren des WMI-abwärts Kompatibilitätspakets</span><span class="sxs-lookup"><span data-stu-id="ffec8-103">Install WMI Backward Compatibility package</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffec8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffec8-104">

<span> </span></span></span>

<span data-ttu-id="ffec8-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ffec8-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ffec8-106">Wenn Sie versuchen, den Zusammenführungs-Assistenten des Topologie-Generators auszuführen, ohne das WMI-abwärts Kompatibilitätspaket zu installieren, wird der folgende Fehler angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ffec8-106">If you attempt to run the Topology Builder Merge wizard without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="ffec8-107">![WMI-Fehlermeldung](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI-Fehlermeldung")</span><span class="sxs-lookup"><span data-stu-id="ffec8-107">![WMI error message](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI error message")</span></span>

<span data-ttu-id="ffec8-108">Wenn Sie versuchen, das **Merge-CsLegacytopology-** Cmdlet auszuführen, ohne das WMI-abwärts Kompatibilitätspaket zu installieren, wird der folgende Fehler angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ffec8-108">If you attempt to run the **Merge-CsLegacytopology** cmdlet without installing the WMI Backward Compatibility package, you will see the following error:</span></span>

<span data-ttu-id="ffec8-109">![Windows PowerShell-WMI-Anbieterfehler](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell-WMI-Anbieterfehler")</span><span class="sxs-lookup"><span data-stu-id="ffec8-109">![Windows PowerShell WMI Provider Error](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell WMI Provider Error")</span></span>

<span data-ttu-id="ffec8-110">So installieren Sie das WMI-abwärts Kompatibilitätspaket</span><span class="sxs-lookup"><span data-stu-id="ffec8-110">To install the WMI Backward Compatibility Package</span></span>

1.  <span data-ttu-id="ffec8-111">Navigieren Sie auf Ihrem Installationsmedium zu \\ Setup \\ amd64- \\ Setup \\OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="ffec8-111">From your installation media, navigate to \\SETUP\\AMD64\\SETUP\\OCSWMIBC.MSI.</span></span>

2.  <span data-ttu-id="ffec8-112">Installieren Sie OCSWMIBC.MSI.</span><span class="sxs-lookup"><span data-stu-id="ffec8-112">Install OCSWMIBC.MSI.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ffec8-113">OCSWMIBC.msi müssen auf dem Computer installiert sein, auf dem der Zusammenführungs-Assistent für Topologie-Builder ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffec8-113">OCSWMIBC.msi must be installed on the computer where the Topology Builder Merge wizard is run.</span></span> <span data-ttu-id="ffec8-114">Es wird jedoch empfohlen, OCSWMIBC.msi auf allen Front-End-Servern in Ihrer Topologie zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ffec8-114">However, we recommend installing OCSWMIBC.msi on all Front End servers in your topology.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ffec8-115">OCSWMIBC.msi kann auf jedem Computer in der Domäne installiert werden, auf dem die lync Server 2013-Core-Komponenten und die lync Server 2013-Verwaltungsshell installiert sind, und Sie können auf die Office Communications Server 2007 R2-Topologie (WMI-Anbieter für Active Directory-Domänendienste (AD DS) und SQL Server) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ffec8-115">OCSWMIBC.msi can be installed on any computer in the domain that has the Lync Server 2013 Core Components and the Lync Server 2013 Management Shell installed, and has access to the Office Communications Server 2007 R2 topology (WMI provider to Active Directory Domain Services (AD DS) and SQL Server).</span></span>

    
    <span data-ttu-id="ffec8-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffec8-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

