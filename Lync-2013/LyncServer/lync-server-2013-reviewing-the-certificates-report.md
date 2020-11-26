---
title: 'Lync Server 2013: Überprüfen des Zertifikats Berichts'
description: 'Lync Server 2013: Überprüfen des Zertifikats Berichts'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reviewing the Certificates Report
ms:assetid: 549cfc9b-3cc5-4483-a93c-fc0738c7f622
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558651(v=OCS.15)
ms:contentKeyID: 51541477
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2133e2f70c78217788d84251c2035a9115bc3283
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442463"
---
# <a name="reviewing-the-certificates-report-in-lync-server-2013"></a><span data-ttu-id="f6c38-103">Überprüfen des Berichts "Zertifikate" in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6c38-103">Reviewing the Certificates Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f6c38-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f6c38-104">

<span> </span></span></span>

<span data-ttu-id="f6c38-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="f6c38-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="f6c38-106">Der Bericht Zertifikate enthält alle Zertifikate, die in der empfohlenen lync Server 2013-Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f6c38-106">The Certificates Report contains all certificates that are required in the recommended Lync Server 2013 deployment.</span></span> <span data-ttu-id="f6c38-107">Das Planungs Tool berücksichtigt die eingegebenen Antragstellernamen und alternativen Subjektnamen.</span><span class="sxs-lookup"><span data-stu-id="f6c38-107">The Planning Tool accounts for the subject names and subject alternative names that are entered.</span></span> <span data-ttu-id="f6c38-108">Nicht bearbeiteter Standardtext kann eine Herausforderung für das Team darstellen, das für das Anfordern und Ausstellen der Zertifikate verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="f6c38-108">Default text that is left unedited may represent a potential challenge for the team responsible for requesting and issuing the certificates.</span></span> <span data-ttu-id="f6c38-109">In den Zertifikatinformationen ist zudem angegeben, durch welche Stelle das Zertifikat typischerweise ausgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6c38-109">Certificate information also contains information about where the certificate can typically be issued from.</span></span> <span data-ttu-id="f6c38-110">Wenn die Infrastruktur nicht über eine interne Public Key-Infrastruktur (PKI) verfügt, können sämtliche Zertifikate über einen öffentlichen Zertifikatanbieter angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f6c38-110">If the infrastructure does not have an internal public key infrastructure (PKI) in place, all certificates can be requested through a public certificate provider.</span></span> <span data-ttu-id="f6c38-111">Die Felder „Erweiterte Schlüsselverwendungen“ und „Zuweisen zu“ des Berichts sind äußerst nützlich und liefern Informationen zu Zweck und Speicherort der einzelnen Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="f6c38-111">Extended key usages (EKU) and Assign To fields in the report are very helpful in understanding what the purpose and location for each certificate should be.</span></span>

<span data-ttu-id="f6c38-112">![Zertifikatverwaltungsbericht](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Zertifikatverwaltungsbericht")</span><span class="sxs-lookup"><span data-stu-id="f6c38-112">![Certificates Admin Report](images/Gg558651.63a29335-d9e4-41ae-97ec-3c9d9fd30d8a(OCS.15).jpg "Certificates Admin Report")</span></span>

<span data-ttu-id="f6c38-113">Überprüfen Sie die Verwendung und den Zweck der einzelnen Zertifikate innerhalb der Bereitstellung sorgfältig und stellen Sie sicher, dass Sie diese Informationen verstanden haben.</span><span class="sxs-lookup"><span data-stu-id="f6c38-113">Carefully review, and be sure to understand, the use and purpose of each certificate in the deployment.</span></span> <span data-ttu-id="f6c38-114">Wenn Sie Fragen zum Zweck eines Zertifikats haben, ermitteln Sie, welcher Server oder Dienst mit welcher Komponente kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="f6c38-114">If there is a question about what a certificate does, determine which server or service is talking to what.</span></span> <span data-ttu-id="f6c38-115">Zertifikate in lync Server 2013 werden für zwei primäre Zwecke verwendet:</span><span class="sxs-lookup"><span data-stu-id="f6c38-115">Certificates in Lync Server 2013 are used for two primary purposes:</span></span>

  - <span data-ttu-id="f6c38-p103">Mutual Transport Layer Security (MTLS) – Die Computer, die miteinander kommunizieren, belegen ihre Identität gegenüber den anderen Computern mithilfe eines Zertifikats. Dieser Vorgang wird als Serverauthentifizierung bezeichnet. Die Kommunikation ist erst möglich, wenn sämtliche Computer die Identität der anderen Computer als vertrauenswürdig eingestuft haben.</span><span class="sxs-lookup"><span data-stu-id="f6c38-p103">Mutual Transport Layer Security (MTLS) – The computers involved in the communication each present a certificate that proves their identity to another computer. This is known as server authentication. Communication cannot begin until each computer trusts the other computer’s identity.</span></span>

  - <span data-ttu-id="f6c38-119">Verschlüsselung – Die Verschlüsselung (Secure Sockets Layer, SSL, und Transport Layer Security, TLS) ist eine wichtige Methode, um eine sichere Kommunikation und die Einhaltung von Datenschutzrichtlinien zu gewährleisten sowie ein vertrauenswürdiges System für Kommunikation und Zusammenarbeit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6c38-119">Encryption – Encryption (Secure Sockets Layer, or SSL, and Transport Layer Security, or TLS) is a critical means to help secure communications, help ensure privacy, and to create a trusted communications and collaboration system.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="f6c38-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6c38-120">See Also</span></span>


[<span data-ttu-id="f6c38-121">Überprüfen der Administratorberichte in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f6c38-121">Reviewing the Administrator Reports in Lync Server 2013</span></span>](lync-server-2013-reviewing-the-administrator-reports.md)  
  

<span data-ttu-id="f6c38-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f6c38-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

