---
title: 'Lync Server 2013: Erforderliche Software für Enterprise-VoIP'
description: 'Lync Server 2013: Software Voraussetzungen für Enterprise-VoIP'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Software prerequisites for Enterprise Voice
ms:assetid: 41172119-9631-46c7-9d9f-386d951c650b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425916(v=OCS.15)
ms:contentKeyID: 48183960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23d21f40e275431f0384448341aa25ecb628ebf9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441606"
---
# <a name="software-prerequisites-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="d27b7-103">Erforderliche Software für Enterprise-VoIP in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d27b7-103">Software prerequisites for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d27b7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d27b7-104">

<span> </span></span></span>

<span data-ttu-id="d27b7-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="d27b7-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="d27b7-106">Überprüfen Sie, ob die Infrastruktur, in der Sie Enterprise-VoIP bereitstellen möchten, die folgenden Softwarevoraussetzungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="d27b7-106">Verify that the infrastructure in which you intend to deploy Enterprise Voice meets the following software prerequisites:</span></span>

  - <span data-ttu-id="d27b7-107">Lync Server 2013 Standard Edition oder Enterprise Edition ist in Ihrem Netzwerk installiert und betriebsbereit.</span><span class="sxs-lookup"><span data-stu-id="d27b7-107">Lync Server 2013 Standard Edition or Enterprise Edition is installed and operational on your network.</span></span>

  - <span data-ttu-id="d27b7-108">Alle Edgeserver werden in Ihrem Umkreisnetzwerk bereitgestellt und in Betrieb genommen, einschließlich Edgeserver mit Access Edge-Dienst, a/V-Edgedienst, Webkonferenz-Edgedienst und einem Reverse-Proxy.</span><span class="sxs-lookup"><span data-stu-id="d27b7-108">All Edge Servers are deployed and operational in your perimeter network, including Edge Servers running Access Edge service, A/V Edge service, Web Conferencing Edge service, and a reverse proxy.</span></span>

  - <span data-ttu-id="d27b7-109">Entweder Microsoft Exchange Server 2007 Service Pack 3 (SP3), Microsoft Exchange Server 2010 oder Microsoft Exchange Server 2013 ist für die Integration von Exchange Unified Messaging mit lync Server erforderlich und bietet umfangreiche Benachrichtigungen und Anrufprotokoll Informationen für die lync-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="d27b7-109">Either Microsoft Exchange Server 2007 Service Pack 3 (SP3), Microsoft Exchange Server 2010 or Microsoft Exchange Server 2013 is required for integrating Exchange Unified Messaging with Lync Server and to provide rich notifications and call log information to the Lync endpoints.</span></span>

  - <span data-ttu-id="d27b7-110">Mindestens ein Benutzer wurde für lync Server erstellt und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d27b7-110">One or more users have been created and enabled for Lync Server.</span></span>

  - <span data-ttu-id="d27b7-111">Lync-Clients und-Geräte wurden erfolgreich bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d27b7-111">Lync clients and devices have been successfully deployed.</span></span>

  - <span data-ttu-id="d27b7-112">Der Topologie-Generator ist auf einem Server in Ihrem Netzwerk installiert.</span><span class="sxs-lookup"><span data-stu-id="d27b7-112">Topology Builder is installed on a server on your network.</span></span>

<div>

## <a name="next-steps-verify-security-and-configuration-prerequisites"></a><span data-ttu-id="d27b7-113">Nächste Schritte: Überprüfen der Voraussetzungen für Sicherheit und Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d27b7-113">Next Steps: Verify Security and Configuration Prerequisites</span></span>

<span data-ttu-id="d27b7-114">Nachdem Sie die Softwarevoraussetzungen für Enterprise-VoIP überprüft haben, können Sie die Dokumentation verwenden, um die Bereitstellung von Enterprise-VoIP weiter vorzubereiten:</span><span class="sxs-lookup"><span data-stu-id="d27b7-114">After verifying software prerequisites for Enterprise Voice, you can use the documentation to continue preparing for deploying Enterprise Voice:</span></span>

1.  <span data-ttu-id="d27b7-115">Überprüfen Sie die Sicherheits-, Benutzer-und Hardware Vergünstigungen, wie unter [Sicherheits-und Konfigurationsvoraussetzungen für Enterprise-VoIP in lync Server 2013](lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d27b7-115">Verify security, user configuration, and hardware perquisites, as described in [Security and configuration prerequisites for Enterprise Voice in Lync Server 2013](lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md).</span></span>

2.  <span data-ttu-id="d27b7-116">Installieren Sie den Vermittlungsserver, wie unter [Installieren der Dateien für den Vermittlungsserver in lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md)beschrieben, aber *nur* , wenn Sie einen eigenständigen Vermittlungsserver oder-Pool bereitstellen möchten, da Vermittlungsserver als Teil des Front-End-Pools oder des Standard Edition-Server Bereitstellungsprozesses installiert werden, wenn Sie zusammengestellt sind.</span><span class="sxs-lookup"><span data-stu-id="d27b7-116">Install the Mediation Server, as described in [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md), but *only* if you want to deploy a stand-alone Mediation Server or pool because Mediation Servers are installed as part of the Front End pool or Standard Edition server deployment process when collocated.</span></span>

3.  <span data-ttu-id="d27b7-117">Konfigurieren Sie trunk-Verbindungen, um PSTN-Konnektivität für Benutzer bereitzustellen, wie unter [Konfigurieren von Trunks in lync Server 2013](lync-server-2013-configuring-trunks.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d27b7-117">Configure trunk connections to provide PSTN connectivity for users, as described in [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md).</span></span>

<span data-ttu-id="d27b7-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d27b7-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

