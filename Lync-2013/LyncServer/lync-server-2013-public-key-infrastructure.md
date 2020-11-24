---
title: 'Lync Server 2013: Infrastruktur öffentlicher Schlüssel'
description: 'Lync Server 2013: Infrastruktur öffentlicher Schlüssel'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public Key Infrastructure for Lync Server 2013
ms:assetid: 737c8a25-23e9-4494-ab76-5a7b729b44ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481131(v=OCS.15)
ms:contentKeyID: 59893870
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b8f2ee8c6b1524cec461ad90a4d4cb1a1003b51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394582"
---
# <a name="public-key-infrastructure-for-lync-server-2013"></a><span data-ttu-id="5b944-103">Infrastruktur öffentlicher Schlüssel für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5b944-103">Public Key Infrastructure for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5b944-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5b944-104">

<span> </span></span></span>

<span data-ttu-id="5b944-105">_**Letztes Änderungsdatum des Themas:** 2013-11-13_</span><span class="sxs-lookup"><span data-stu-id="5b944-105">_**Topic Last Modified:** 2013-11-13_</span></span>

<span data-ttu-id="5b944-106">Microsoft lync Server 2013 stützt sich auf Zertifikate für die Serverauthentifizierung und die Einrichtung einer Vertrauenskette zwischen Clients und Servern sowie zwischen den verschiedenen Serverrollen.</span><span class="sxs-lookup"><span data-stu-id="5b944-106">Microsoft Lync Server 2013 relies on certificates for server authentication and to establish a chain of trust between clients and servers and among the different server roles.</span></span> <span data-ttu-id="5b944-107">Der Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003 Public-Key-Infrastruktur (PKI) bietet die Infrastruktur für die Erstellung und Validierung dieser Vertrauenskette.</span><span class="sxs-lookup"><span data-stu-id="5b944-107">The Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008, and Windows Server 2003 Public Key Infrastructure (PKI) provides the infrastructure for establishing and validating this chain of trust.</span></span>

<span data-ttu-id="5b944-p102">Zertifikate sind digitale IDs. Sie identifizieren einen Server nach Namen und geben seine Eigenschaften an. Um sicherzustellen, dass die Informationen auf einem Zertifikat gültig sind, muss das Zertifikat von einer Zertifizierungsstelle ausgegeben sein, die für Clients und andere Server, die sich mit dem Server verbinden, vertrauenswürdig ist. Wenn sich der Server nur mit anderen Clients und Servern in einem privaten Netzwerk verbindet, kann die Zertifizierungsstelle eine Unternehmenszertifizierungsstelle sein. Wenn der Server mit Entitäten außerhalb des privaten Netzwerks interagiert, ist möglicherweise eine öffentliche Zertifizierungsstelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b944-p102">Certificates are digital IDs. They identify a server by name and specify its properties. To ensure that the information on a certificate is valid, the certificate must be issued by a CA that is trusted by clients or other servers that connect to the server. If the server connects only with other clients and servers on a private network, the CA can be an enterprise CA. If the server interacts with entities outside the private network, a public CA might be required.</span></span>

<span data-ttu-id="5b944-p103">Selbst wenn die Informationen auf dem Zertifikat gültig sind, muss es eine Möglichkeit zum Überprüfen geben, ob der Server, der das Zertifikat präsentiert, tatsächlich der Server ist, der von dem Zertifikat repräsentiert wird. Hier kommt die Windows PKI ins Spiel.</span><span class="sxs-lookup"><span data-stu-id="5b944-p103">Even if the information on the certificate is valid, there must be some way to verify that the server presenting the certificate is actually the one represented by the certificate. This is where the Windows PKI comes in.</span></span>

<span data-ttu-id="5b944-p104">Jedes Zertifikat ist mit einem öffentlichen Schlüssel verbunden. Der auf dem Zertifikat benannte Server verfügt über einen entsprechenden privaten Schlüssel, der nur ihm bekannt ist. Ein sich verbindender Client oder Server verwendet den öffentlichen Schlüssel, um eine beliebige Information zu verschlüsseln und sendet diese an den Server. Wenn der Server die Information entschlüsselt und als Klartext zurückgibt, kann die sich verbindende Entität sicher sein, dass der Server über den privaten Schlüssel zum Zertifikat verfügt und es sich daher um den auf dem Zertifikat benannten Server handelt.</span><span class="sxs-lookup"><span data-stu-id="5b944-p104">Each certificate is linked to a public key. The server named on the certificate holds a corresponding private key that only it knows. A connecting client or server uses the public key to encrypt a random piece of information and sends it to the server. If the server decrypts the information and returns it as plain text, the connecting entity can be sure that the server holds the private key to the certificate and therefore is the server named on the certificate.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5b944-119">Nicht alle öffentlichen CAS erfüllen die Anforderungen von lync Server 2013-Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="5b944-119">Not all public CAs comply with the requirements of Lync Server 2013 certificates.</span></span> <span data-ttu-id="5b944-120">Wir empfehlen Ihnen, für öffentliche Zertifikate auf die Auflistung von zertifizierten öffentlichen Zertifizierungsstellenanbietern zurückzugreifen.</span><span class="sxs-lookup"><span data-stu-id="5b944-120">We recommend that you refer to the listing of certified Public CA vendors for your public certificate needs.</span></span> <span data-ttu-id="5b944-121">Ausführliche Informationen finden Sie unter Unified Communications Certificate Partners unter <A href="https://go.microsoft.com/fwlink/p/?linkid=140898">https://go.microsoft.com/fwlink/p/?LinkId=140898</A> .</span><span class="sxs-lookup"><span data-stu-id="5b944-121">For details, see Unified Communications Certificate Partners at <A href="https://go.microsoft.com/fwlink/p/?linkid=140898">https://go.microsoft.com/fwlink/p/?LinkId=140898</A>.</span></span>



</div>

<div>

## <a name="crl-distribution-points"></a><span data-ttu-id="5b944-122">CRL-Verteilungspunkte</span><span class="sxs-lookup"><span data-stu-id="5b944-122">CRL Distribution Points</span></span>

<span data-ttu-id="5b944-123">Lync Server 2013 erfordert, dass alle Server Zertifikate mindestens einen CRL-Verteilungspunkt (Certificate Revocation List) enthalten.</span><span class="sxs-lookup"><span data-stu-id="5b944-123">Lync Server 2013 requires all server certificates to contain one or more Certificate Revocation List (CRL) distribution points.</span></span> <span data-ttu-id="5b944-124">Sperrlisten-Verteilungspunkte sind Standorte, von denen Zertifikatsperrlisten heruntergeladen werden können, um zu prüfen, ob das Zertifikat seit dem Zeitpunkt, an dem es ausgestellt wurde, gesperrt wurde und es sich noch im Gültigkeitszeitraum befindet.</span><span class="sxs-lookup"><span data-stu-id="5b944-124">CRL distribution points (CDPs) are locations from which CRLs can be downloaded for purposes of verifying that the certificate has not been revoked since the time it was issued and the certificate is still within the validity period.</span></span> <span data-ttu-id="5b944-125">Ein Sperrlisten-Verteilungspunkt wird in den Eigenschaften des Zertifikats als URL aufgeführt und ist normalerweise sicheres HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b944-125">A CRL distribution point is noted in the properties of the certificate as a URL, and is typically secure HTTP.</span></span>

</div>

<div>

## <a name="enhanced-key-usage"></a><span data-ttu-id="5b944-126">Erweiterte Schlüsselverwendung</span><span class="sxs-lookup"><span data-stu-id="5b944-126">Enhanced Key Usage</span></span>

<span data-ttu-id="5b944-127">Lync Server 2013 erfordert, dass alle Serverzertifikate zur Unterstützung der erweiterten Schlüsselverwendung (EKU) für die Serverauthentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b944-127">Lync Server 2013 requires all server certificates to support Enhanced Key Usage (EKU) for the purpose of server authentication.</span></span> <span data-ttu-id="5b944-128">Die Konfiguration des EKU-Felds für die Serverauthentifizierung bedeutet, dass das Zertifikat für den Zweck der Serverauthentifizierung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5b944-128">Configuring the EKU field for server authentication means that the certificate is valid for the purpose of authenticating servers.</span></span> <span data-ttu-id="5b944-129">Diese EKU ist wesentlich für MTLS.</span><span class="sxs-lookup"><span data-stu-id="5b944-129">This EKU is essential for MTLS.</span></span> <span data-ttu-id="5b944-130">Es ist möglich, mehr als einen Eintrag in der EKU zu haben und damit das Zertifikat für mehrere Zwecke zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b944-130">It is possible to have more than one entry in the EKU, enabling the certificate for more than one purpose.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5b944-131">Die EKU für die Client Authentifizierung ist für ausgehende MTLS-Verbindungen von Live Communications Server 2003 und Live Communications Server 2005 erforderlich, aber nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5b944-131">The Client Authentication EKU is required for outbound MTLS connections from Live Communications Server 2003 and Live Communications Server 2005, but it is no longer required.</span></span> <span data-ttu-id="5b944-132">Diese EKU muss jedoch auf Edgeserver vorhanden sein, die mithilfe öffentlicher Chat Verbindungen mit AOL verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="5b944-132">However, this EKU must be present on Edge Servers that connect to AOL by means of public IM connectivity.</span></span>



<span data-ttu-id="5b944-133"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5b944-133"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

