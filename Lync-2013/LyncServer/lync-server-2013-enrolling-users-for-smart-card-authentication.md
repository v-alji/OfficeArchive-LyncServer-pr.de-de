---
title: 'Lync Server 2013: Registrieren von Benutzern für die Smartcard-Authentifizierung'
description: 'Lync Server 2013: Registrieren von Benutzern für die Smartcard-Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enrolling users for smart card authentication
ms:assetid: a6445a83-a94b-423f-ba2a-12b5f84c5d75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308570(v=OCS.15)
ms:contentKeyID: 54973691
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d67994d2152ac344934d093a1b6f7d482a7933a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428636"
---
# <a name="enrolling-users-for-smart-card-authentication-in-lync-server-2013"></a><span data-ttu-id="98feb-103">Registrieren von Benutzern für die Smartcard-Authentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98feb-103">Enrolling users for smart card authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98feb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98feb-104">

<span> </span></span></span>

<span data-ttu-id="98feb-105">_**Letztes Änderungsdatum des Themas:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="98feb-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="98feb-p101">Allgemein bestehen zwei Verfahren für das Registrieren von Benutzern für die SmartCard-Authentifizierung. Das einfachere Verfahren sieht die direkte Registrierung der Benutzer für die SmartCard-Authentifizierung mithilfe der Webregistrierung vor, während bei der komplexeren Methode ein Enrollment Agent verwendet wird. Dieses Thema legt den Schwerpunkt auf die Selbstregistrierung der Benutzer für SmartCard-Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="98feb-p101">There are generally two methods for enrolling users for smart card authentication. The easier method involves having users enroll directly for smart card authentication using web enrollment, while the more complex method involves using an enrollment agent. This topic focuses on self-enrollment for smartcard certificates.</span></span>

<span data-ttu-id="98feb-109">Weitere Informationen zur Registrierung für Benutzer als Registrierungs-Agent finden Sie unter Registrieren für Zertifikate im Auftrag anderer Benutzer unter [https://go.microsoft.com/fwlink/p/?LinkID=313367](https://go.microsoft.com/fwlink/p/?linkid=313367) .</span><span class="sxs-lookup"><span data-stu-id="98feb-109">For more information on enrolling on behalf of users as an enrollment agent, see Enroll for Certificates on Behalf of Other Users at [https://go.microsoft.com/fwlink/p/?LinkID=313367](https://go.microsoft.com/fwlink/p/?linkid=313367).</span></span>

<div>

## <a name="to-enroll-users-for-smart-card-authentication"></a><span data-ttu-id="98feb-110">So registrieren Sie Benutzer für die SmartCard-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="98feb-110">To Enroll Users for Smart Card Authentication</span></span>

1.  <span data-ttu-id="98feb-111">Melden Sie sich mit den Anmeldeinformationen eines lync-fähigen Benutzers bei der Windows 8-Workstation an.</span><span class="sxs-lookup"><span data-stu-id="98feb-111">Log in to the Windows 8 workstation using the credentials of a Lync-enabled user.</span></span>

2.  <span data-ttu-id="98feb-112">Starten Sie Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="98feb-112">Launch Internet Explorer.</span></span>

3.  <span data-ttu-id="98feb-113">Navigieren Sie zur **Website Registrierungsseite für die Zertifizierungsstelle** ( https://MyCA.contoso.com/certsrv) z. b.</span><span class="sxs-lookup"><span data-stu-id="98feb-113">Browse to the **Certificate Authority Web Enrollment** page (e.g. https://MyCA.contoso.com/certsrv).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="98feb-114">Wenn Sie Internet Explorer 10 verwenden, müssen Sie diese Website möglicherweise im Kompatibilitätsmodus anzeigen.</span><span class="sxs-lookup"><span data-stu-id="98feb-114">If you are using Internet Explorer 10, you may need to view this website in Compatibility Mode.</span></span>

    
    </div>

4.  <span data-ttu-id="98feb-115">Wählen Sie auf der Seite **Willkommen** die Option **Zertifikat anfordern** aus.</span><span class="sxs-lookup"><span data-stu-id="98feb-115">On the **Welcome** Page, select **Request a certificate**.</span></span>

5.  <span data-ttu-id="98feb-116">Wählen Sie im nächsten Schritt **Erweiterte Anforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="98feb-116">Next, select **Advanced Request**.</span></span>

6.  <span data-ttu-id="98feb-117">Wählen Sie **Eine Anforderung an diese Zertifizierungsstelle erstellen und einreichen** aus.</span><span class="sxs-lookup"><span data-stu-id="98feb-117">Select **Create and submit a request to this CA**.</span></span>

7.  <span data-ttu-id="98feb-118">Wählen Sie im Abschnitt **Zertifikatvorlage** den Eintrag **SmartCard-Benutzer** aus und füllen Sie die erweiterte Zertifikatanforderung mit den folgenden Werten aus:</span><span class="sxs-lookup"><span data-stu-id="98feb-118">Select **Smartcard User** under the **Certificate Template** section and complete the advanced certificate request with the following values:</span></span>
    
      - <span data-ttu-id="98feb-119">**Schlüsseloptionen** – bestätigen Sie die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="98feb-119">**Key Options** confirm he following settings:</span></span>
        
          - <span data-ttu-id="98feb-120">Aktivieren Sie das Optionsfeld **Neuen Schlüsselsatz erstellen**</span><span class="sxs-lookup"><span data-stu-id="98feb-120">Select the **Create new key set** radio button</span></span>
        
          - <span data-ttu-id="98feb-121">Wählen Sie für **CSP** die Option **Microsoft Basis-SmartCard-Krypto-Anbieter**</span><span class="sxs-lookup"><span data-stu-id="98feb-121">For **CSP**, select **Microsoft Base Smart Card Crypto Provider**</span></span>
        
          - <span data-ttu-id="98feb-122">Wählen Sie für **Schlüsselverwendung** den Wert **Exchange** aus (dies ist die einzige verfügbare Option).</span><span class="sxs-lookup"><span data-stu-id="98feb-122">For **Key Usage**, select **Exchange** (this is the only option available).</span></span>
        
          - <span data-ttu-id="98feb-123">Geben Sie unter **Schlüsselgröße** den Wert **2048** ein</span><span class="sxs-lookup"><span data-stu-id="98feb-123">For **Key Size**, enter **2048**</span></span>
        
          - <span data-ttu-id="98feb-124">Überprüfen Sie, ob **Automatischer Schlüsselcontainername** aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="98feb-124">Confirm that **Automatic key container name** is selected</span></span>
        
          - <span data-ttu-id="98feb-125">Lassen Sie die anderen Felder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="98feb-125">Leave the other boxes unchecked.</span></span>
    
      - <span data-ttu-id="98feb-126">Bestätigen Sie unter **Weitere Optionen** die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="98feb-126">Under **Additional Options** confirm the following values:</span></span>
        
          - <span data-ttu-id="98feb-127">Wählen Sie für **Anforderungsformat** den Wert **CMC** aus.</span><span class="sxs-lookup"><span data-stu-id="98feb-127">For **Request Format** select **CMC**.</span></span>
        
          - <span data-ttu-id="98feb-128">Wählen Sie für **Hashalgorithmus** den Wert **sha1** aus.</span><span class="sxs-lookup"><span data-stu-id="98feb-128">For **Hash Algorithm** select **sha1**.</span></span>
        
          - <span data-ttu-id="98feb-129">Geben Sie als **Anzeigename** den Wert **Smardcard Certificate** ein.</span><span class="sxs-lookup"><span data-stu-id="98feb-129">For **Friendly Name** enter **Smardcard Certificate**.</span></span>

8.  <span data-ttu-id="98feb-130">Wenn Sie ein physisches Smartcard-Lesegerät verwenden, setzen Sie die SmartCard in das Gerät ein.</span><span class="sxs-lookup"><span data-stu-id="98feb-130">If you are using a physical smartcard reader, insert the smart card into the device.</span></span>

9.  <span data-ttu-id="98feb-131">Klicken Sie auf **Senden**, um die Zertifikatanforderung einzureichen.</span><span class="sxs-lookup"><span data-stu-id="98feb-131">Click **Submit** to submit the certificate request.</span></span>

10. <span data-ttu-id="98feb-132">Wenn Sie dazu aufgefordert werden, geben Sie die PIN ein, die zum Erstellen der virtuellen SmartCard verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="98feb-132">When prompted, enter the PIN that was used to create the virtual smart card.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="98feb-133">Der Standardwert der PIN für virtuelle SmartCards ist „12345678“.</span><span class="sxs-lookup"><span data-stu-id="98feb-133">The default virtual smart card PIN value is ‘12345678’.</span></span>

    
    </div>

11. <span data-ttu-id="98feb-134">Nachdem das Zertifikat ausgestellt wurde, klicken Sie auf **Dieses Zertifikat installieren**, um den Registrierungsvorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="98feb-134">Once the certificate has been issued, click **Install this certificate** to complete the enrollment process.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="98feb-135">Wenn bei der Zertifikatanforderung ein Fehler mit der Meldung „Der Webbrowser unterstützt nicht die Generierung von Zertifikatanforderungen“ auftritt, kann das Problem auf drei verschiedene Weisen gelöst werden:</span><span class="sxs-lookup"><span data-stu-id="98feb-135">If your certificate request fails with the error “This Web browser does not support the generation of certificate requests,” there are three possible ways to resolve the issue:</span></span> 
    > <OL>
    > <LI>
    > <P><span data-ttu-id="98feb-136">Aktivieren Sie in Internet Explorer die Kompatibilitätsansicht</span><span class="sxs-lookup"><span data-stu-id="98feb-136">Enable Compatibility View in Internet Explorer</span></span></P>
    > <LI>
    > <P><span data-ttu-id="98feb-137">Aktivieren Sie die Option „Intraneteinstellungen einschalten“ in Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="98feb-137">Enable the Turn on Intranet settings option in Internet Explorer</span></span></P>
    > <LI>
    > <P><span data-ttu-id="98feb-138">Aktivieren Sie in den Internet Explorer-Optionen auf der Registerkarte „Sicherheit“ die Einstellung „Alle Zonen auf Standardstufe zurücksetzen“.</span><span class="sxs-lookup"><span data-stu-id="98feb-138">Select the Reset all zones to default level setting under the Security tab in the Internet Explorer options menu.</span></span></P></LI></OL><span data-ttu-id="98feb-139">

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98feb-139">

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

