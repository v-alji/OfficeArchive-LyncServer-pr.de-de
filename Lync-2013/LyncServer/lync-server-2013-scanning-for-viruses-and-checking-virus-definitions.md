---
title: 'Lync Server 2013: Scannen auf Viren und Überprüfen von Virendefinitionen'
description: 'Lync Server 2013: nach Viren suchen und Virendefinitionen überprüfen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scanning for viruses and checking virus definitions
ms:assetid: 287c0f43-82d1-4c1d-b08f-77112fcb5bfa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720909(v=OCS.15)
ms:contentKeyID: 63969589
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c06b08b5e902857e95cdefc206cdbfa860ef748c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445008"
---
# <a name="scanning-for-viruses-and-checking-virus-definitions-in-lync-server-2013"></a><span data-ttu-id="77daa-103">Scannen auf Viren und Überprüfen von Virendefinitionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77daa-103">Scanning for viruses and checking virus definitions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77daa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77daa-104">

<span> </span></span></span>

<span data-ttu-id="77daa-105">_**Letztes Änderungsdatum des Themas:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="77daa-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<span data-ttu-id="77daa-106">Wir empfehlen dringend die Installation eines Antivirus-Produkts auf chatebene.</span><span class="sxs-lookup"><span data-stu-id="77daa-106">We highly recommend installing an IM-level antivirus product.</span></span> <span data-ttu-id="77daa-107">Im ist eine bekannte Quelle für die schnelle Verbreitung von Viren und bösartiger Software in einem Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="77daa-107">IM is a well-known source for quickly spreading both virus and malicious software throughout an organization.</span></span> <span data-ttu-id="77daa-108">Microsoft Forefront® Security für lync Server bietet Multi-Engine-Scans mit Viren, bösartiger Software, Schutz vor Datei-und Schlüsselwortfiltern und nahtlose Integration in Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="77daa-108">Microsoft Forefront® Security for Lync Server provides multi-engine scanning with virus, malicious software, file and keyword filter protection and seamless integration with Office Communications Server.</span></span>

<span data-ttu-id="77daa-109">Zusätzlich zu Forefront Security für lync Server empfiehlt es sich, eine Antivirus-Lösung auf Dateiebene zu installieren, um das Dateisystem des Servers zu schützen.</span><span class="sxs-lookup"><span data-stu-id="77daa-109">In addition to Forefront Security for Lync Server, we also highly recommend installing a file-level, antivirus solution to protect the server’s file system.</span></span>

<span data-ttu-id="77daa-110">Das Aktualisieren von Scanner-Engines und Virendefinitionen ist sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="77daa-110">Keeping scanner engines and virus definitions updated is very important.</span></span> <span data-ttu-id="77daa-111">Durch Konfigurieren und Überwachen des Zustands der Updates wird sichergestellt, dass die aktuellsten Scaninformationen zum Schutz von Office Communications Server und Dateisystem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="77daa-111">Configuring and monitoring the health of the updates makes sure that the most current scanning information is being used to protect both Office Communications Server and file-system.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="77daa-112">Wenn Sie eine Antivirensoftware eines Drittanbieters auf einem Server verwenden, auf dem lync Server 2013 und Forefront Security für lync Server ausgeführt wird, stellen Sie sicher, dass die Ordner, in denen Forefront Security für lync Server und der lync-Server installiert sind, nicht gescannt werden, um deren Beschädigung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="77daa-112">When using a third-party, file-level antivirus software on a server that runs Lync Server 2013 and Forefront Security for Lync Server, make sure that the folders in which Forefront Security for Lync Server and the Lync Server are installed are not scanned, to prevent their corruption.</span></span> <span data-ttu-id="77daa-113">Eine vollständige Liste der Ausschlüsse finden Sie unter <A class=uri href="https://support.microsoft.com/kb/943620">https://support.microsoft.com/kb/943620</A> .</span><span class="sxs-lookup"><span data-stu-id="77daa-113">For the full list of exclusions, see <A class=uri href="https://support.microsoft.com/kb/943620">https://support.microsoft.com/kb/943620</A>.</span></span>



<span data-ttu-id="77daa-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77daa-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

