---
title: 'Lync Server 2013: Anforderungen in Bezug auf die Zertifikatsinfrastruktur'
description: Anforderungen an die lync Server 2013-Zertifikatinfrastruktur.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate infrastructure requirements
ms:assetid: 0051aa23-0bbe-4e72-9f29-e01c6bcc6190
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398066(v=OCS.15)
ms:contentKeyID: 48183219
ms.date: 06/23/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 02c7e69f272c29f0ba9386f403db326b4d39bbff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435411"
---
# <a name="certificate-infrastructure-requirements-for-lync-server-2013"></a><span data-ttu-id="b6381-103">Anforderungen in Bezug auf die Zertifikatinfrastruktur für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6381-103">Certificate infrastructure requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b6381-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b6381-104">

<span> </span></span></span>

<span data-ttu-id="b6381-105">_**Letztes Änderungsdatum des Themas:** 2016-06-23_</span><span class="sxs-lookup"><span data-stu-id="b6381-105">_**Topic Last Modified:** 2016-06-23_</span></span>

<span data-ttu-id="b6381-106">Lync Server 2013 erfordert eine Public Key-Infrastruktur (PKI) zur Unterstützung von TLS-und MTLS-Verbindungen (Mutual TLS).</span><span class="sxs-lookup"><span data-stu-id="b6381-106">Lync Server 2013 requires a public key infrastructure (PKI) to support TLS and mutual TLS (MTLS) connections.</span></span>

<span data-ttu-id="b6381-107">Lync Server verwendet Zertifikate für die folgenden Zwecke:</span><span class="sxs-lookup"><span data-stu-id="b6381-107">Lync Server uses certificates for the following purposes:</span></span>

  - <span data-ttu-id="b6381-108">TLS-Verbindungen zwischen Client und Server</span><span class="sxs-lookup"><span data-stu-id="b6381-108">TLS connections between client and server</span></span>

  - <span data-ttu-id="b6381-109">MTLS-Verbindungen zwischen Servern</span><span class="sxs-lookup"><span data-stu-id="b6381-109">MTLS connections between servers</span></span>

  - <span data-ttu-id="b6381-110">Föderation mithilfe der automatischen DNS-Ermittlung von Partnern</span><span class="sxs-lookup"><span data-stu-id="b6381-110">Federation using automatic DNS discovery of partners</span></span>

  - <span data-ttu-id="b6381-111">Zugriff von Remotebenutzern auf Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="b6381-111">Remote user access for instant messaging (IM)</span></span>

  - <span data-ttu-id="b6381-112">Zugriff externer Benutzer auf Audio/Video-Sitzungen (A/V), Anwendungsfreigabe und Konferenzen</span><span class="sxs-lookup"><span data-stu-id="b6381-112">External user access to audio/video (A/V) sessions, application sharing, and conferencing</span></span>

  - <span data-ttu-id="b6381-113">Mobile Anforderungen mithilfe der automatischen Ermittlung von Webdiensten</span><span class="sxs-lookup"><span data-stu-id="b6381-113">Mobile requests using automatic discovery of Web Services</span></span>

<span data-ttu-id="b6381-114">Für lync Server gelten die folgenden allgemeinen Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="b6381-114">For Lync Server, the following common requirements apply:</span></span>

  - <span data-ttu-id="b6381-115">Alle Serverzertifikate müssen die Serverautorisierung (Enhanced Key Usage [EKU], erweiterte Schlüsselverwendung für Server) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b6381-115">All server certificates must support server authorization (Server EKU).</span></span>

  - <span data-ttu-id="b6381-116">Alle Serverzertifikate müssen einen Zertifikatsperrlisten-Verteilungspunkt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b6381-116">All server certificates must contain a CRL Distribution Point (CDP).</span></span>

  - <span data-ttu-id="b6381-117">Alle Zertifikate müssen mithilfe eines Signaturalgorithmus signiert werden, der vom Betriebssystem unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b6381-117">All certificates must be signed using a signing algorithm supported by the operating system.</span></span> <span data-ttu-id="b6381-118">Lync Server 2013 unterstützt die SHA-1-und SHA-2-Suite von Digest-Größen (224, 256, 384 und 512-Bit) und erfüllt oder überschreitet die Anforderungen des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="b6381-118">Lync Server 2013 supports the SHA-1 and SHA-2 suite of digest sizes (224, 256, 384 and 512-bit), and meets or exceeds the operating system requirements.</span></span> <span data-ttu-id="b6381-119">Informationen zur Unterstützung des Betriebssystems finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002) .</span><span class="sxs-lookup"><span data-stu-id="b6381-119">For operating system support, see [https://go.microsoft.com/fwlink/?LinkId=287002](https://go.microsoft.com/fwlink/?linkid=287002).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b6381-120">Die Verwendung des Signaturalgorithmus RSASSA-PSS wird nicht unterstützt und kann unter anderem zu Fehlern bei der Anmeldung und Problemen mit der Anrufweiterleitung führen. </span><span class="sxs-lookup"><span data-stu-id="b6381-120">Using the RSASSA-PSS signature algorithm is unsupported, and may lead to errors on login and call forwarding issues, among other problems.</span></span>

    
    </div>

  - <span data-ttu-id="b6381-121">Die automatische Registrierung wird für interne Server unterstützt, auf denen lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6381-121">Auto-enrollment is supported for internal servers running Lync Server.</span></span>

  - <span data-ttu-id="b6381-122">Die automatische Registrierung wird für lync Server Edge-Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6381-122">Auto-enrollment is not supported for Lync Server Edge Servers.</span></span>

  - <span data-ttu-id="b6381-123">Wenn Sie eine webbasierte Zertifikatanforderung an eine Windows Server 2003-Zertifizierungsstelle übermitteln, müssen Sie Sie von einem Computer übermitteln, auf dem Windows Server 2003 mit SP2 oder Windows XP ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6381-123">When you submit a web-based certificate request to a Windows Server 2003 CA, you must submit it from a computer running either Windows Server 2003 with SP2 or Windows XP.</span></span>
    
    <span data-ttu-id="b6381-124">Beachten Sie, dass KB922706 zwar Unterstützung für das Beheben von Problemen beim Registrieren von webzertifikaten für eine Windows Server 2003 Certificate Services-Webregistrierung bietet, es jedoch nicht möglich ist, Windows Server 2008, Windows Vista oder Windows 7 zum Anfordern eines Zertifikats von einer Windows Server 2003-Zertifizierungsstelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6381-124">Note that although KB922706 provides support for resolving issues with enrolling web certificates against a Windows Server 2003 Certificate Services web enrollment, it does not make it possible to use Windows Server 2008, Windows Vista, or Windows 7 to request a certificate from a Windows Server 2003 CA.</span></span>

  - <span data-ttu-id="b6381-125">Es werden Verschlüsselungsschlüssellängen von 1.024, 2.048 und 4.096 Bit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6381-125">Encryption key lengths of 1024, 2048, and 4096 are supported.</span></span> <span data-ttu-id="b6381-126">Empfohlen werden Schlüssellängen ab 2.048 Bit.</span><span class="sxs-lookup"><span data-stu-id="b6381-126">Key lengths of 2048 and greater are recommended.</span></span>

  - <span data-ttu-id="b6381-127">Der Standard-Digest-oder Hash-Signaturalgorithmus ist RSA.</span><span class="sxs-lookup"><span data-stu-id="b6381-127">The default digest, or hash signing, algorithm is RSA.</span></span> <span data-ttu-id="b6381-128">Die \_ Algorithmen ECDH P256, ECDH \_ P384 und ECDH \_ P521 werden ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b6381-128">The ECDH\_P256, ECDH\_P384, and ECDH\_P521 algorithms are also supported.</span></span> 

<div>

## <a name="in-this-section"></a><span data-ttu-id="b6381-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b6381-129">In This Section</span></span>

  - [<span data-ttu-id="b6381-130">Anforderungen an Zertifikate für interne Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6381-130">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="b6381-131">Zertifikatanforderungen für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6381-131">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="b6381-132">Zertifikatanforderungen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6381-132">Certificate requirements for Persistent Chat server in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="b6381-133">Zertifikatanforderungen für die Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b6381-133">Certificate requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-mobility.md)

<span data-ttu-id="b6381-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b6381-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

