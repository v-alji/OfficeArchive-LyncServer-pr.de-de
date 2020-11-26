---
title: 'Lync Server 2013: Verschlüsselung'
description: 'Lync Server 2013: Verschlüsselung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Encryption for Lync Server 2013
ms:assetid: d18c74a6-385b-407b-98eb-0d525fa38fea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481135(v=OCS.15)
ms:contentKeyID: 59893874
ms.date: 09/14/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ab2c46af16cfdbb9a01631777e65219acb2ceb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428720"
---
# <a name="encryption-for-lync-server-2013"></a><span data-ttu-id="552c8-103">Verschlüsselung für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="552c8-103">Encryption for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="552c8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="552c8-104">

<span> </span></span></span>

<span data-ttu-id="552c8-105">_**Letztes Änderungsdatum des Themas:** 2017-09-14_</span><span class="sxs-lookup"><span data-stu-id="552c8-105">_**Topic Last Modified:** 2017-09-14_</span></span>

<span data-ttu-id="552c8-106">Microsoft lync Server 2013 verwendet TLS und MTLS zum Verschlüsseln von Sofortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="552c8-106">Microsoft Lync Server 2013 uses TLS and MTLS to encrypt instant messages.</span></span> <span data-ttu-id="552c8-107">Der gesamte Server-zu-Server-Datenverkehr erfordert MTLS – unabhängig davon, ob der Datenverkehr auf das interne Netzwerk beschränkt ist oder den internen Netzwerkperimeter überschreitet.</span><span class="sxs-lookup"><span data-stu-id="552c8-107">All server-to-server traffic requires MTLS, regardless of whether the traffic is confined to the internal network or crosses the internal network perimeter.</span></span> <span data-ttu-id="552c8-108">TLS ist optional, wird aber dringend zwischen dem Vermittlungs Server und dem Mediengateway empfohlen.</span><span class="sxs-lookup"><span data-stu-id="552c8-108">TLS is optional but strongly recommended between the Mediation Server and media gateway.</span></span> <span data-ttu-id="552c8-109">Wenn TLS auf dieser Verbindung konfiguriert ist, ist MTLS erforderlich.</span><span class="sxs-lookup"><span data-stu-id="552c8-109">If TLS is configured on this link, MTLS is required.</span></span> <span data-ttu-id="552c8-110">Daher muss das Gateway mit einem Zertifikat von einer Zertifizierungsstelle konfiguriert werden, die vom Vermittlungs Server als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="552c8-110">Therefore, the gateway must be configured with a certificate from a CA that is trusted by the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="552c8-111">Im Jahr 2014 wurde eine Sicherheitsempfehlung zu SSL 3.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="552c8-111">A security advisory regarding SSL 3.0 was published in 2014.</span></span> <span data-ttu-id="552c8-112">Das Deaktivieren von SSL 3,0 in lync Server 2013 ist eine unterstützte Option.</span><span class="sxs-lookup"><span data-stu-id="552c8-112">Disabling SSL 3.0 in Lync Server 2013 is a supported option.</span></span> <span data-ttu-id="552c8-113">Weitere Informationen zur Sicherheitsempfehlung finden Sie unter <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A> .</span><span class="sxs-lookup"><span data-stu-id="552c8-113">To learn more about the security advisory, see <A class=uri href="https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/">https://blogs.technet.microsoft.com/uclobby/2014/10/22/disabling-ssl-3-0-in-lync-server-2013/</A>.</span></span>



</div>

<div>

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="Sicherheits" alt="security" /><span data-ttu-id="552c8-115">Sicherheitshinweis:</span><span class="sxs-lookup"><span data-stu-id="552c8-115">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="552c8-116">Um sicherzustellen, dass das stärkste kryptografische Protokoll verwendet wird, bietet lync Server 2013 TLS-Verschlüsselungsprotokolle in der folgenden Reihenfolge für Clients an: <strong>TLS 1,2</strong> , <strong>TLS 1,1</strong>, <strong>TLS 1,0</strong>.</span><span class="sxs-lookup"><span data-stu-id="552c8-116">To ensure the strongest cryptographic protocol is used, Lync Server 2013 will offer TLS encryption protocols in the following order to clients: <strong>TLS 1.2</strong> , <strong>TLS 1.1</strong>, <strong>TLS 1.0</strong>.</span></span> <span data-ttu-id="552c8-117">TLS ist ein wichtiger Aspekt von lync Server 2013 und daher erforderlich, um eine unterstützte Umgebung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="552c8-117">TLS is a critical aspect of Lync Server 2013 and thus it is required in order to maintain a supported environment.</span></span></td>
</tr>
</tbody>
</table>


</div>

<span data-ttu-id="552c8-118">Die Anforderungen für Client-zu-Client-Datenverkehr hängen davon ab, ob der Datenverkehr die interne Unternehmensfirewall überschreitet.</span><span class="sxs-lookup"><span data-stu-id="552c8-118">Requirements for client-to-client traffic depend on whether that traffic crosses the internal corporate firewall.</span></span> <span data-ttu-id="552c8-119">Rein interner Datenverkehr kann entweder TLS verwenden, in diesem Fall wird die Sofortnachricht verschlüsselt, oder TCP, in diesem Fall nicht.</span><span class="sxs-lookup"><span data-stu-id="552c8-119">Strictly internal traffic can use either TLS, in which case the instant message is encrypted, or TCP, in which case it is not.</span></span>

<span data-ttu-id="552c8-120">In der folgenden Tabelle sind die Protokollanforderungen für jeden Datenverkehrstyp zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="552c8-120">The following table summarizes the protocol requirements for each type of traffic.</span></span>

### <a name="traffic-protection"></a><span data-ttu-id="552c8-121">Datenverkehrsschutz</span><span class="sxs-lookup"><span data-stu-id="552c8-121">Traffic Protection</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="552c8-122">Datenverkehrstyp</span><span class="sxs-lookup"><span data-stu-id="552c8-122">Traffic type</span></span></th>
<th><span data-ttu-id="552c8-123">Geschützt durch</span><span class="sxs-lookup"><span data-stu-id="552c8-123">Protected by</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="552c8-124">Server-zu-Server</span><span class="sxs-lookup"><span data-stu-id="552c8-124">Server-to-server</span></span></p></td>
<td><p><span data-ttu-id="552c8-125">MTLS</span><span class="sxs-lookup"><span data-stu-id="552c8-125">MTLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="552c8-126">Client-zu-Server</span><span class="sxs-lookup"><span data-stu-id="552c8-126">Client-to-server</span></span></p></td>
<td><p><span data-ttu-id="552c8-127">TLS</span><span class="sxs-lookup"><span data-stu-id="552c8-127">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="552c8-128">Chat und Anwesenheit</span><span class="sxs-lookup"><span data-stu-id="552c8-128">Instant messaging and presence</span></span></p></td>
<td><p><span data-ttu-id="552c8-129">TLS (falls für TLS konfiguriert)</span><span class="sxs-lookup"><span data-stu-id="552c8-129">TLS (if configured for TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="552c8-130">Audio und Video und Desktopfreigaben von Medien</span><span class="sxs-lookup"><span data-stu-id="552c8-130">Audio and video and desktop sharing of media</span></span></p></td>
<td><p><span data-ttu-id="552c8-131">SRTP</span><span class="sxs-lookup"><span data-stu-id="552c8-131">SRTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="552c8-132">Desktopfreigabe (Signal)</span><span class="sxs-lookup"><span data-stu-id="552c8-132">Desktop sharing (signaling)</span></span></p></td>
<td><p><span data-ttu-id="552c8-133">TLS</span><span class="sxs-lookup"><span data-stu-id="552c8-133">TLS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="552c8-134">Webkonferenzen</span><span class="sxs-lookup"><span data-stu-id="552c8-134">Web conferencing</span></span></p></td>
<td><p><span data-ttu-id="552c8-135">TLS</span><span class="sxs-lookup"><span data-stu-id="552c8-135">TLS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="552c8-136">Herunterladen von Besprechungsinhalten, Herunterladen des Adressbuchs, Erweiterung der Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="552c8-136">Meeting content download, address book download, distribution group expansion</span></span></p></td>
<td><p><span data-ttu-id="552c8-137">HTTPS</span><span class="sxs-lookup"><span data-stu-id="552c8-137">HTTPS</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="media-encryption"></a><span data-ttu-id="552c8-138">Medienverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="552c8-138">Media Encryption</span></span>

<span data-ttu-id="552c8-139">Mediendatenverkehr wird über Secure RTP (SRTP) verschlüsselt, ein Profil von RTP (Real-Time Transport-Protokoll), das Vertraulichkeit, Authentifizierung und Schutz vor Replay-Angriffen für RTP-Datenverkehr bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="552c8-139">Media traffic is encrypted using Secure RTP (SRTP), a profile of Real-Time Transport Protocol (RTP) that provides confidentiality, authentication, and replay attack protection to RTP traffic.</span></span> <span data-ttu-id="552c8-140">Darüber hinaus werden Medien, die in beide Richtungen zwischen dem Vermittlungsserver und seinem internen nächsten Hop übertragen werden, ebenfalls über SRTP verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="552c8-140">In addition, media flowing in both directions between the Mediation Server and its internal next hop is also encrypted using SRTP.</span></span> <span data-ttu-id="552c8-141">Medien, die in beide Richtungen zwischen dem Vermittlungs Server und einem Mediengateway fließen, werden standardmäßig nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="552c8-141">Media flowing in both directions between the Mediation Server and a media gateway is not encrypted by default.</span></span> <span data-ttu-id="552c8-142">Der Vermittlungsserver kann die Verschlüsselung an das Mediengateway unterstützen, aber das Gateway muss MTLS und das Speichern eines Zertifikats unterstützen.</span><span class="sxs-lookup"><span data-stu-id="552c8-142">The Mediation Server can support encryption to the media gateway, but the gateway must support MTLS and storage of a certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="552c8-143">Audio/Video (A/V) wird mit der neuen Version von Windows Live Messenger unterstützt.</span><span class="sxs-lookup"><span data-stu-id="552c8-143">Audio/Video (A/V) is supported with the new version of Windows Live Messenger.</span></span> <span data-ttu-id="552c8-144">Wenn Sie einen/V-Verbund mit Windows Live Messenger implementieren, müssen Sie auch die lync Server-Verschlüsselungsstufe ändern.</span><span class="sxs-lookup"><span data-stu-id="552c8-144">If you are implementing A/V federation with Windows Live Messenger, you must also modify the Lync Server encryption level.</span></span> <span data-ttu-id="552c8-145">Standardmäßig ist die Verschlüsselungsstufe auf „Erforderlich“ eingestellt.</span><span class="sxs-lookup"><span data-stu-id="552c8-145">By default, the encryption level is Required.</span></span> <span data-ttu-id="552c8-146">Sie müssen diese Einstellung mithilfe der lync Server-Verwaltungsshell in unterstützt ändern.</span><span class="sxs-lookup"><span data-stu-id="552c8-146">You must change this setting to Supported by using the Lync Server Management Shell.</span></span> <span data-ttu-id="552c8-147">Weitere Informationen finden Sie unter <A href="lync-server-2013-deploying-external-user-access.md">Bereitstellen des Zugriffs auf externe Benutzer in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="552c8-147">For more information, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="552c8-148">Der Datenverkehr für Audio-und Video Medien wird zwischen Microsoft lync 2013 und Windows Live-Clients nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="552c8-148">Audio and video media traffic is not encrypted between Microsoft Lync 2013 and Windows Live clients.</span></span>

</div>

<div>

## <a name="fips"></a><span data-ttu-id="552c8-149">FIPS</span><span class="sxs-lookup"><span data-stu-id="552c8-149">FIPS</span></span>

<span data-ttu-id="552c8-150">Lync Server 2013 und Microsoft Exchange Server 2013 arbeiten mit Unterstützung für FIPS (Federal Information Processing Standard) 140-2-Algorithmen, wenn die Windows Server-Betriebssysteme so konfiguriert sind, dass Sie die FIPS 140-2-Algorithmen für die Systemkryptografie verwenden.</span><span class="sxs-lookup"><span data-stu-id="552c8-150">Lync Server 2013 and Microsoft Exchange Server 2013 operate with support for Federal Information Processing Standard (FIPS) 140-2 algorithms if the Windows Server operating systems are configured to use the FIPS 140-2 algorithms for system cryptography.</span></span> <span data-ttu-id="552c8-151">Zum Implementieren der FIPS-Unterstützung müssen Sie jeden Server mit lync Server 2013 so konfigurieren, dass er unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="552c8-151">To implement FIPS support, you must configure each server running Lync Server 2013 to support it.</span></span> <span data-ttu-id="552c8-152">Details zur Verwendung von FIPS-kompatiblen Algorithmen und zur Implementierung der FIPS-Unterstützung finden Sie im Microsoft Knowledge Base-Artikel 811833, die Auswirkungen der Aktivierung der Sicherheitseinstellung "System Kryptographie: FIPS-kompatible Algorithmen für Verschlüsselung, Hashing und Signierung" in Windows XP und späteren Windows-Versionen unter [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833) .</span><span class="sxs-lookup"><span data-stu-id="552c8-152">For details about the use of FIPS-compliant algorithms and how to implement FIPS support, see Microsoft Knowledge Base article 811833, The effects of enabling the “System cryptography: Use FIPS compliant algorithms for encryption, hashing, and signing" security setting in Windows XP and in later versions of Windows at [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=811833](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=811833).</span></span> <span data-ttu-id="552c8-153">Ausführliche Informationen zu FIPS 140-2-Unterstützung und Einschränkungen in Exchange 2010 finden Sie unter Exchange 2010 SP1 und Unterstützung für FIPS-konforme Algorithmen unter [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335) .</span><span class="sxs-lookup"><span data-stu-id="552c8-153">For details about FIPS 140-2 support and limitations in Exchange 2010, see Exchange 2010 SP1 and Support for FIPS Compliant Algorithms at [https://go.microsoft.com/fwlink/p/?LinkId=205335](https://go.microsoft.com/fwlink/p/?linkid=205335).</span></span>

<span data-ttu-id="552c8-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="552c8-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

