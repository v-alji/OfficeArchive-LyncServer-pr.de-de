---
title: Zuweisen eines Server-zu-Server-Authentifizierungszertifikats zu lync Server 2013
description: Zuweisen eines Server-zu-Server-Authentifizierungszertifikats zu lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013
ms:assetid: c7413954-2504-47f4-a073-44548aff1c0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205253(v=OCS.15)
ms:contentKeyID: 48185367
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 042158167f89dc2b6e743e8db94149d4f1cbc1a2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438323"
---
# <a name="assigning-a-server-to-server-authentication-certificate-to-microsoft-lync-server-2013"></a><span data-ttu-id="bc731-103">Zuweisen eines Server-zu-Server-Authentifizierungszertifikats zu Microsoft lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc731-103">Assigning a server-to-server authentication certificate to Microsoft Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc731-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc731-104">

<span> </span></span></span>

<span data-ttu-id="bc731-105">_**Letztes Änderungsdatum des Themas:** 2013-10-24_</span><span class="sxs-lookup"><span data-stu-id="bc731-105">_**Topic Last Modified:** 2013-10-24_</span></span>

<span data-ttu-id="bc731-106">Führen Sie den folgenden Befehl in der lync Server 2013-Verwaltungsshell aus, um zu ermitteln, ob ein Server-zu-Server-Authentifizierungszertifikat bereits Microsoft lync Server 2013 zugewiesen wurde:</span><span class="sxs-lookup"><span data-stu-id="bc731-106">To determine whether or not a server-to-server authentication certificate has already been assigned to Microsoft Lync Server 2013, run the following command from the Lync Server 2013 Management Shell:</span></span>

    Get-CsCertificate -Type OAuthTokenIssuer

<span data-ttu-id="bc731-107">Wenn keine Zertifikatinformationen zurückgegeben werden, müssen Sie ein Token-Ausstellerzertifikat zuweisen, bevor Sie die Server-zu-Server-Authentifizierung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bc731-107">If no certificate information is returned you must assign a token issuer certificate before you can use server-to-server authentication.</span></span> <span data-ttu-id="bc731-108">In der Regel kann jedes lync Server 2013-Zertifikat als OAuthTokenIssuer-Zertifikat verwendet werden. So kann beispielsweise das Standardzertifikat von lync Server 2013 auch als OAuthTokenIssuer-Zertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc731-108">As a general rule, any Lync Server 2013 certificate can be used as your OAuthTokenIssuer certificate; for example, your Lync Server 2013 default certificate can also be used as the OAuthTokenIssuer certificate.</span></span> <span data-ttu-id="bc731-109">(Das OAUthTokenIssuer-Zertifikat kann auch ein beliebiges Webserverzertifikat sein, das den Namen Ihrer SIP-Domäne im Feld Betreff enthält.) Die primären beiden Anforderungen für das für die Server-zu-Server-Authentifizierung verwendete Zertifikat sind: 1) dasselbe Zertifikat muss auf allen Front-End-Servern als OAuthTokenIssuer-Zertifikat konfiguriert sein. und 2) das Zertifikat muss mindestens 2048 Bits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bc731-109">(The OAUthTokenIssuer certificate can also be any Web server certificate that includes the name of your SIP domain in the Subject field.) The primary two requirements for the certificate used for server-to-server authentication are these: 1)the same certificate must be configured as the OAuthTokenIssuer certificate on all of your Front End Servers; and, 2) the certificate must be at least 2048 bits.</span></span>

<span data-ttu-id="bc731-110">Wenn Sie über kein Zertifikat verfügen, das für die Server-zu-Server-Authentifizierung verwendet werden kann, können Sie ein neues Zertifikat beziehen, das neue Zertifikat importieren und anschließend für die Server-zu-Server-Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc731-110">If you do not have a certificate that can be used for server-to-server authentication you can obtain a new certificate, import the new certificate, and then use that certificate for server-to-server authentication.</span></span> <span data-ttu-id="bc731-111">Nachdem Sie das neue Zertifikat angefordert und erhalten haben, können Sie sich bei einem der Front-End-Server anmelden und einen Windows PowerShell-Befehl wie den folgenden verwenden, um das Zertifikat zu importieren und zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="bc731-111">After you have requested and obtained the new certificate you can then log on to any one of your Front End Servers and use a Windows PowerShell command similar to this one to import and assign that certificate:</span></span>

    Import-CsCertificate -Identity global -Type OAuthTokenIssuer -Path C:\Certificates\ServerToServerAuth.pfx  -Password "P@ssw0rd"

<span data-ttu-id="bc731-112">Im vorangehenden Befehl stellt der path-Parameter den vollständigen Pfad zur Zertifikatsdatei dar, und der Parameter Password steht für das Kennwort, das dem Zertifikat zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="bc731-112">In the preceding command the Path parameter represents the full path to the certificate file, and the Password parameter represents the password that was assigned to the certificate.</span></span> <span data-ttu-id="bc731-113">Diese Vorgehensweisesollte nur einmal ausgeführt werden: der Replikationsdienst von lync Server erstellt dann automatisch einen Satz von geplanten Aufgaben, mit denen das Zertifikat entschlüsselt und auf allen Front-End-Servern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bc731-113">This procedure should be run just one time: Lync Server's replication service will then automatically create a set of scheduled tasks that will decrypt and deploy the certificate to all your Front End Servers.</span></span>

<span data-ttu-id="bc731-114">Alternativ können Sie ein vorhandenes Zertifikat als Server-zu-Server-Authentifizierungszertifikat verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc731-114">Alternatively, you can use an existing certificate as your server-to-server authentication certificate.</span></span> <span data-ttu-id="bc731-115">(Wie bereits erwähnt, kann das Standardzertifikat als Server-zu-Server-Authentifizierungszertifikat verwendet werden.) Das folgende Paar von Windows PowerShell-Befehlen Ruft den Wert der Eigenschaft "Fingerabdruck" des Standardzertifikats ab und verwendet diesen Wert, um das Standardzertifikat zum Server-zu-Server-Authentifizierungszertifikat zu machen:</span><span class="sxs-lookup"><span data-stu-id="bc731-115">(As noted, the default certificate can be used as the server-to-server authentication certificate.) The following pair of Windows PowerShell commands retrieve the value of the default certificate's Thumbprint property, then use that value to make the default certificate the server-to-server authentication certificate:</span></span>

    $x = (Get-CsCertificate -Type Default).Thumbprint
    Set-CsCertificate -Identity global -Type OAuthTokenIssuer -Thumbprint $x

<span data-ttu-id="bc731-116">Im vorhergehenden Befehl ist das abgerufene Zertifikat so konfiguriert, dass es als globales Server-zu-Server-Authentifizierungszertifikat dient. Das bedeutet, dass das Zertifikat an alle Ihre Front-End-Server repliziert und von diesen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc731-116">In the preceding command, the retrieved certificate is configured to function as the global server-to-server authentication certificate; that means that the certificate will be replicated to, and used by, all your Front End Servers.</span></span> <span data-ttu-id="bc731-117">Dieser Befehl sollte erneut nur einmal und nur auf einem der Front-End-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc731-117">Again, this command should only be run one time, and only on one of your Front End Servers.</span></span> <span data-ttu-id="bc731-118">Obwohl alle Front-End-Server dasselbe Zertifikat verwenden müssen, sollten Sie das OAuthTokenIssuer-Zertifikat nicht auf jedem Front-End-Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="bc731-118">Although all Front End Servers must use the same certificate, you should not configure the OAuthTokenIssuer certificate on each Front End Server.</span></span> <span data-ttu-id="bc731-119">Konfigurieren Sie stattdessen das Zertifikat einmal, und lassen Sie den Replikationsserver von lync Server dafür sorgen, dass das Zertifikat auf jeden Server kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc731-119">Instead, configure the certificate once, then let Lync Server's replication server take care of copying that certificate to each server.</span></span>

<span data-ttu-id="bc731-120">Das Set-CsCertificate-Cmdlet übernimmt das fragliche Zertifikat und konfiguriert dieses Zertifikat sofort so, dass es als Aktuelles OAuthTokenIssuer-Zertifikat fungiert.</span><span class="sxs-lookup"><span data-stu-id="bc731-120">The Set-CsCertificate cmdlet takes the certificate in question and immediately configures that certificate to act as the current OAuthTokenIssuer certificate.</span></span> <span data-ttu-id="bc731-121">(Lync Server 2013 speichert zwei Kopien eines Zertifikatstyps: das aktuelle Zertifikat und das vorherige Zertifikat.) Wenn das neue Zertifikat sofort als OAuthTokenIssuer-Zertifikat fungieren soll, sollten Sie das Set-CsCertificate-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc731-121">(Lync Server 2013 keeps two copies of a certificate type: the current certificate and the previous certificate.) If you need the new certificate to immediately begin to act as the OAuthTokenIssuer certificate then you should use the Set-CsCertificate cmdlet.</span></span>

<span data-ttu-id="bc731-122">Sie können auch das Set-CsCertificate-Cmdlet verwenden, um ein neues Zertifikat zu "Rollen".</span><span class="sxs-lookup"><span data-stu-id="bc731-122">You can also use the Set-CsCertificate cmdlet to "roll" a new certificate.</span></span> <span data-ttu-id="bc731-123">Das "Rollen" eines Zertifikats bedeutet einfach, dass Sie ein neues Zertifikat so konfigurieren, dass es zu einem bestimmten Zeitpunkt zum aktuellen OAuthTokenIssuer-Zertifikat wird.</span><span class="sxs-lookup"><span data-stu-id="bc731-123">"Rolling" a certificate simply means that you configure a new certificate to become the current OAuthTokenIssuer certificate at a specified point in time.</span></span> <span data-ttu-id="bc731-124">Mit diesem Befehl wird beispielsweise das Standardzertifikat abgerufen und dann dieses Zertifikat so konfiguriert, dass es vom 1. Juli 2012 als Aktuelles OAuthTokenIssuer-Zertifikat übertragen wird:</span><span class="sxs-lookup"><span data-stu-id="bc731-124">For example, this command retrieves the default certificate and then configure that certificate to take over as the current OAuthTokenIssuer certificate as of July 1, 2012:</span></span>

    $x = (Get-CsCertificate -Type Default).Thumbprint
    Set-CsCertificate -Identity global -Type OAuthTokenIssuer -Thumbprint $x -EffectiveDate "7/1/2012" -Roll

<span data-ttu-id="bc731-125">Am 1. Juli 2012 wird das neue Zertifikat als Aktuelles OAuthTokenIssuer-Zertifikat konfiguriert, und das "alte" OAuthTokenIssuer-Zertifikat wird als Vorheriges Zertifikat konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bc731-125">On July 1, 2012 the new certificate will be configured as the current OAuthTokenIssuer certificate and the "old" OAuthTokenIssuer certificate will be configured as the previous certificate.</span></span>

<span data-ttu-id="bc731-126">Wenn Sie Windows PowerShell nicht verwenden möchten, können Sie auch die MMC-Konsole Zertifikate verwenden, um ein Zertifikat von einem Front-End-Server zu exportieren und dieses Zertifikat dann auf allen anderen Front-End-Servern zu importieren.</span><span class="sxs-lookup"><span data-stu-id="bc731-126">If you do not want to use Windows PowerShell you can also use the Certificates MMC console to export a certificate from one Front End Server and then import that same certificate on all your other Front End Servers.</span></span> <span data-ttu-id="bc731-127">Dabei müssen Sie unbedingt den privaten Schlüssel zusammen mit dem Zertifikat selbst exportieren.</span><span class="sxs-lookup"><span data-stu-id="bc731-127">If you do this, make sure that you export the private key along with the certificate itself.</span></span>

<div>


> [!WARNING]
> <span data-ttu-id="bc731-128">In diesem Fall muss die Prozedur auf jedem Front-End-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc731-128">In this case, the procedure must be performed on each Front End Server.</span></span> <span data-ttu-id="bc731-129">Wenn Sie Zertifikate auf diese Weise exportieren und importieren, repliziert lync Server 2013 dieses Zertifikat nicht auf jeden Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="bc731-129">When exporting and importing certificates in this manner Lync Server 2013 will not replicate that certificate to each Front End Server.</span></span>



</div>

<span data-ttu-id="bc731-130">Nachdem das Zertifikat auf alle Ihre Front-End-Server importiert wurde, kann dieses Zertifikat mithilfe des lync Server-Bereitstellungs-Assistenten anstelle von Windows PowerShell zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="bc731-130">After the certificate has been imported to all your Front End Servers, that certificate can then be assigned by using the Lync Server Deployment Wizard instead of Windows PowerShell.</span></span> <span data-ttu-id="bc731-131">Führen Sie zum Zuweisen eines Zertifikats mithilfe des Bereitstellungs-Assistenten die folgenden Schritte auf einem Computer aus, auf dem der Bereitstellungs-Assistent installiert wurde:</span><span class="sxs-lookup"><span data-stu-id="bc731-131">To assign a certificate by using the Deployment Wizard, complete the following steps on a computer where the Deployment Wizard has been installed:</span></span>

1.  <span data-ttu-id="bc731-132">Klicken Sie auf Start, klicken Sie auf alle Programme, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Bereitstellungs-Assistent**.</span><span class="sxs-lookup"><span data-stu-id="bc731-132">Click Start, click All Programs, click **Microsoft Lync Server 2013**, and then click **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="bc731-133">Klicken Sie im Bereitstellungs-Assistenten auf **lync Server System installieren oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="bc731-133">In the Deployment Wizard, click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="bc731-134">Klicken Sie auf der Microsoft lync Server 2013-Seite unter der Überschrift **Schritt 3: anfordern, installieren oder Zuweisen von Zertifikaten** auf die Schaltfläche **Ausführen** .</span><span class="sxs-lookup"><span data-stu-id="bc731-134">On the Microsoft Lync Server 2013 page, click the **Run** button under the heading **Step 3: Request, Install or Assign Certificates**.</span></span> <span data-ttu-id="bc731-135">(Hinweis: Falls Sie auf diesem Computer bereits Zertifikate installiert haben, heißt die Schaltfläche nicht **Ausführen**, sondern **Erneut ausführen**.)</span><span class="sxs-lookup"><span data-stu-id="bc731-135">(Note: If you have already installed certificates on this computer then the **Run** button will be labeled **Run Again**.)</span></span>

4.  <span data-ttu-id="bc731-136">Wählen Sie im Zertifikat-Assistenten das Zertifikat **OAuthTokenIssuer** aus und klicken Sie auf **Zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="bc731-136">In the Certificate Wizard, select the **OAuthTokenIssuer** certificate and then click **Assign**.</span></span>

5.  <span data-ttu-id="bc731-137">Klicken Sie im Zertifikatzuweisungs-Assistenten auf der Seite **Zertifikatzuweisung** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bc731-137">In the Certificate Assignment wizard, on the **Certificate Assignment** page, click **Next**.</span></span>

6.  <span data-ttu-id="bc731-138">Wählen Sie auf der Seite **Zertifikatspeicher** das Zertifikat aus, das für die Server-zu-Server-Authentifizierung verwendet werden soll und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bc731-138">On the **Certificate Store** page, select the certificate to be used for server-to-server authentication and then click **Next**.</span></span>

7.  <span data-ttu-id="bc731-139">Klicken Sie auf der Seite für die Zusammenfassung der Zertifikatzuweisung auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bc731-139">On the Certificate Assignment Summary page, click **Next**.</span></span>

8.  <span data-ttu-id="bc731-140">Klicken Sie auf der Seite „Befehle ausführen“ auf **Fertigstellen**.</span><span class="sxs-lookup"><span data-stu-id="bc731-140">On the Executing Commands page, click **Finish**.</span></span>

9.  <span data-ttu-id="bc731-141">Schließen Sie den Zertifikat-Assistenten und den Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="bc731-141">Close the Certificate Wizard and the Deployment Wizard.</span></span>

<span data-ttu-id="bc731-142"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc731-142"></div>

<span> </span>

</div>

</div>

</span></span></div>

