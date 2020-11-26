---
title: 'Lync Server 2013: Technische Anforderungen für die Ankündigungsanwendung'
description: 'Lync Server 2013: Technische Voraussetzungen für die Ankündigungs Anwendung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: adc5019408b79301bbcda3993ceb7d96ee4d9b7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444308"
---
# <a name="technical-requirements-for-the-announcement-application-in-lync-server-2013"></a><span data-ttu-id="e5454-103">Technische Anforderungen für die Ankündigungsanwendung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5454-103">Technical requirements for the Announcement application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5454-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5454-104">

<span> </span></span></span>

<span data-ttu-id="e5454-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="e5454-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="e5454-106">In diesem Abschnitt werden die folgenden technischen Voraussetzungen für die Ankündigungs Anwendung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="e5454-106">This section describes the following technical requirements for the Announcement application:</span></span>

  - <span data-ttu-id="e5454-107">Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-107">Hardware requirements</span></span>

  - <span data-ttu-id="e5454-108">Softwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-108">Software requirements</span></span>

  - <span data-ttu-id="e5454-109">Portanforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-109">Port requirements</span></span>

  - <span data-ttu-id="e5454-110">Audiodatei-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-110">Audio file requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="e5454-111">Hardware Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-111">Hardware Requirements</span></span>

<span data-ttu-id="e5454-112">Die Ankündigungs Anwendung hat die gleichen Hardwareanforderungen wie Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="e5454-112">The Announcement application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="e5454-113">Details zu den Hardwareanforderungen finden Sie unter [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="e5454-113">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="e5454-114">Software Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-114">Software Requirements</span></span>

<span data-ttu-id="e5454-115">Die Ankündigungs Anwendung verfügt über die gleichen Betriebssystemanforderungen und Softwarevoraussetzungen wie Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="e5454-115">The Announcement application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="e5454-116">Ausführliche Informationen zu den Softwareanforderungen finden Sie unter unter [Stützung von Server-und Tools-Betriebssystemen in lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="e5454-116">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="e5454-117">Auf allen Front-End-Servern oder Standard Edition-Servern, auf denen die Ankündigungs Anwendung ausgeführt wird, muss die Windows Media-Format Laufzeit für Server mit Windows Server 2008 R2 oder Microsoft Media Foundation für Server mit Windows Server 2012 oder Windows Server 2012 R2 installiert sein.</span><span class="sxs-lookup"><span data-stu-id="e5454-117">All Front End Servers or Standard Edition servers that run the Announcement application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="e5454-118">Bei Windows Server 2008 R2 wird die Windows Media-Format Laufzeit als Teil der Windows-Desktop Oberfläche installiert.</span><span class="sxs-lookup"><span data-stu-id="e5454-118">For Windows Server 2008 R2, the Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span> <span data-ttu-id="e5454-119">Windows Media Format Runtime oder Microsoft Media Foundation ist für Windows Media Audio-Dateien (WMA) erforderlich, die von der Ankündigungs Anwendung für Ankündigungen und Musik wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5454-119">Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that the Announcement application plays for announcements and music.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="e5454-120">Portanforderungen</span><span class="sxs-lookup"><span data-stu-id="e5454-120">Port Requirements</span></span>

<span data-ttu-id="e5454-121">Die Ankündigungs Anwendung verwendet den folgenden Port:</span><span class="sxs-lookup"><span data-stu-id="e5454-121">The Announcement application uses the following port:</span></span>

  - <span data-ttu-id="e5454-122">**Port 5071** Wird für SIP-Überwachungsanforderungen verwendet</span><span class="sxs-lookup"><span data-stu-id="e5454-122">**Port 5071**   Used for SIP listening requests</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e5454-123">Dieser Port ist die Standardeinstellung, kann aber mit dem Cmdlet <STRONG>Set-CsApplicationServer</STRONG> geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e5454-123">This port is the default setting, which you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="e5454-124">Details zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="e5454-124">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="e5454-125">Anforderungen für Audiodateien</span><span class="sxs-lookup"><span data-stu-id="e5454-125">Audio File Requirements</span></span>

<span data-ttu-id="e5454-126">Die Ankündigungs Anwendung unterstützt das Wave-Dateiformat (WAV) und das Windows Media Audio-Dateiformat (WMA) für Musik und Ankündigungen.</span><span class="sxs-lookup"><span data-stu-id="e5454-126">The Announcement application supports Wave (.wav) file format and Windows Media audio (.wma) file format for music and announcements.</span></span> <span data-ttu-id="e5454-127">Die Anforderungen an die Audiodateien für die Ankündigungs Anwendung sind identisch mit der Antwortgruppen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e5454-127">Audio file requirements for the Announcement application are the same as for the Response Group application.</span></span> <span data-ttu-id="e5454-128">Ausführliche Informationen finden Sie unter [Technische Voraussetzungen für die Reaktionsgruppe in lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span><span class="sxs-lookup"><span data-stu-id="e5454-128">For details, see [Technical requirements for Response Group in Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).</span></span>

<span data-ttu-id="e5454-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5454-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

