---
title: 'Lync Server 2013: Konfigurieren von Zertifikaten für den Director'
description: 'Lync Server 2013: Konfigurieren Sie Zertifikate für den Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure certificates for the Director
ms:assetid: 22988186-15ae-43b1-92f4-0adb3b75a7fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398296(v=OCS.15)
ms:contentKeyID: 48183612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cadc3f51b036120e21c3f1e6201f872aacafef69
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434011"
---
# <a name="configure-certificates-for-the-director-in-lync-server-2013"></a><span data-ttu-id="a0258-103">Konfigurieren von Zertifikaten für den Director in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0258-103">Configure certificates for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0258-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0258-104">

<span> </span></span></span>

<span data-ttu-id="a0258-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="a0258-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a0258-106">Wenn Sie den Zertifikat-Assistenten ausführen, stellen Sie sicher, dass Sie mit einem Konto angemeldet sind, das Mitglied einer Gruppe ist, der die entsprechenden Berechtigungen für den Typ der Zertifikatvorlage zugewiesen wurden, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="a0258-106">When you run the Certificate Wizard, ensure that you are logged in using an account that is a member of a group that has been assigned the appropriate permissions for the type of certificate template you will use.</span></span> <span data-ttu-id="a0258-107">Standardmäßig verwendet eine lync Server 2013-Zertifikatanforderung die Webserverzertifikatvorlage.</span><span class="sxs-lookup"><span data-stu-id="a0258-107">By default, a Lync Server 2013 certificate request will use the Web Server certificate template.</span></span> <span data-ttu-id="a0258-108">Wenn Sie ein Konto verwenden, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist, um ein Zertifikat mithilfe dieser Vorlage anzufordern, stellen Sie sicher, dass der Gruppe die für die Verwendung dieser Vorlage erforderlichen Registrierungsberechtigungen zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="a0258-108">If you use an account that is a member of the RTCUniversalServerAdmins group to request a certificate using this template, verify that the group has been assigned the Enroll permissions required to use that template.</span></span>



</div>

<span data-ttu-id="a0258-109">Für jeden Director ist ein Standardzertifikat, ein webinternes Zertifikat und ein externes Webzertifikat erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0258-109">Each Director requires a default certificate, a web internal certificate, and a web external certificate.</span></span> <span data-ttu-id="a0258-110">Details zu den Zertifikatanforderungen für Directors finden Sie unter [Zertifikatanforderungen für interne Server in lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="a0258-110">For details about the certificate requirements for Directors, see [Certificate requirements for internal servers in Lync Server 2013](lync-server-2013-certificate-requirements-for-internal-servers.md) in the Planning documentation.</span></span>

<span data-ttu-id="a0258-111">Gehen Sie wie folgt vor, um Director-Zertifikate zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a0258-111">Use the following procedure to configure Director certificates.</span></span> <span data-ttu-id="a0258-112">Wiederholen Sie den Vorgang für jeden Director.</span><span class="sxs-lookup"><span data-stu-id="a0258-112">Repeat the procedure for each Director.</span></span> <span data-ttu-id="a0258-113">In den Schritten dieses Verfahrens wird beschrieben, wie Sie ein Zertifikat von einer internen Unternehmensstammzertifizierungsstelle, die von Ihrer Organisation bereitgestellt wird, und mit der Offline Anforderungsverarbeitung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a0258-113">The steps of this procedure describe how to configure a certificate from an Internal Enterprise Root certification authority (CA) deployed by your organization and with offline request processing.</span></span> <span data-ttu-id="a0258-114">Informationen zum Abrufen von Zertifikaten von einer externen Zertifizierungsstelle erhalten Sie von Ihrem Support Team.</span><span class="sxs-lookup"><span data-stu-id="a0258-114">For details about obtaining certificates from an external CA, contact your support team.</span></span>

<div>

## <a name="to-configure-certificates-for-the-director-or-director-pool"></a><span data-ttu-id="a0258-115">So konfigurieren Sie Zertifikate für den Director-oder Director-Pool</span><span class="sxs-lookup"><span data-stu-id="a0258-115">To configure certificates for the Director or Director pool</span></span>

1.  <span data-ttu-id="a0258-116">Klicken Sie im lync Server-Bereitstellungs-Assistenten neben **Schritt 3: anfordern, installieren oder Zuweisen von Zertifikaten** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="a0258-116">In the Lync Server Deployment Wizard, next to **Step 3: Request, Install or Assign Certificates**, click **Run**.</span></span>

2.  <span data-ttu-id="a0258-117">Klicken Sie auf der Seite **Zertifikat-Assistent** auf **Anfordern**.</span><span class="sxs-lookup"><span data-stu-id="a0258-117">On the **Certificate Wizard** page, click **Request**.</span></span>

3.  <span data-ttu-id="a0258-118">Klicken Sie auf der Seite **Zertifikatanforderung** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-118">On the **Certificate Request** page, click **Next**.</span></span>

4.  <span data-ttu-id="a0258-119">Übernehmen Sie auf der Seite **verzögerte oder sofortige Anforderungen** die Option Standard **Anforderung sofort an eine Onlinezertifizierungsstelle senden** , und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-119">On the **Delayed or Immediate Requests** page, accept the default **Send the request immediately to an online certification authority** option, and then click **Next**.</span></span>

5.  <span data-ttu-id="a0258-120">Klicken Sie auf der Seite **Zertifizierungsstelle auswählen** auf die interne Windows-Zertifizierungsstelle, die Sie verwenden möchten, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-120">On the **Choose a Certification Authority (CA)** page, click the internal Windows certification authority that you want to use, and then click **Next**.</span></span>

6.  <span data-ttu-id="a0258-121">Geben Sie auf der Seite **zertifizierungsstellenkonto** die zu verwendenden alternativen Anmeldeinformationen an, wenn das Konto, mit dem Sie angemeldet sind, nicht über die erforderlichen Berechtigungen zum Anfordern des Zertifikats verfügt, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-121">On the **Certification Authority Account** page, specify alternate credentials to be used if the account you are logged on with does not have sufficient authority to request the certificate, and then click **Next**.</span></span>

7.  <span data-ttu-id="a0258-122">Klicken Sie auf der Seite **Alternative Zertifikatvorlage angeben** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-122">On the **Specify Alternate Certificate Template** page, click **Next**.</span></span>

8.  <span data-ttu-id="a0258-123">Auf der Seite **Name und Sicherheitseinstellungen** können Sie einen **Anzeigenamen** angeben, die 2048-Bit-Schlüssellänge akzeptieren und dann auf **weiter** klicken.</span><span class="sxs-lookup"><span data-stu-id="a0258-123">On the **Name and Security Settings** page, you can specify a **Friendly Name**, accept the 2048-bit key length, and then click **Next**.</span></span>

9.  <span data-ttu-id="a0258-124">Geben Sie auf der Seite **Organisationsinformationen** optional Organisationsinformationen an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-124">On the **Organization Information** page, optionally specify organization information, and then click **Next**.</span></span>

10. <span data-ttu-id="a0258-125">Geben Sie auf der Seite **geographische Informationen** optional geografische Informationen an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-125">On the **Geographical Information** page, optionally specify geographical information, and then click **Next**.</span></span>

11. <span data-ttu-id="a0258-126">Klicken Sie auf der Seite **Betreffname/Subject Alternative Names** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-126">On the **Subject Name / Subject Alternative Names** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a0258-127">Die Liste Subject Alternative Name sollte den Namen des Computers enthalten, auf dem Sie den Director installieren (falls ein einzelner Director) oder der Name des Director-Pools und die für die Organisation konfigurierten einfachen URL-Namen.</span><span class="sxs-lookup"><span data-stu-id="a0258-127">The subject alternative name list should contain the name of the computer on which you are installing the Director (if a single Director) or the Director pool name, and the simple URL names configured for the organization.</span></span>

    
    </div>

12. <span data-ttu-id="a0258-128">Wählen Sie in der **SIP-Domäneneinstellung auf der Seite Subject Alternate Names (SANs)** die **konfigurierten SIP-Domänen** für alle Domänen aus, die der Director behandeln soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-128">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the **Configured SIP Domains** for all domains that you want the Director to handle, and then click **Next**.</span></span>

13. <span data-ttu-id="a0258-129">Fügen Sie auf der Seite **configure additional Subject Alternative Names** alle weiteren erforderlichen alternativen Antragstellernamen hinzu, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-129">On the **Configure Additional Subject Alternative Names** page, add any additional required subject alternative names, and then click **Next**.</span></span>

14. <span data-ttu-id="a0258-130">Klicken Sie auf der Seite **Zusammenfassung der Zertifikatanforderung** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-130">On the **Certificate Request Summary** page, click **Next**.</span></span>

15. <span data-ttu-id="a0258-131">Klicken Sie auf der Seite **ausführende Befehle** auf **weiter** , nachdem die Befehle ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="a0258-131">On the **Executing Commands** page, click **Next** after the commands have finished running.</span></span>

16. <span data-ttu-id="a0258-132">Klicken Sie auf der Seite **Online Zertifikat Anforderungs Status** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="a0258-132">On the **Online Certificate Request Status** page, click **Finish**.</span></span>

17. <span data-ttu-id="a0258-133">Klicken Sie auf der Seite **zertifikatzuweisung** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-133">On the **Certificate Assignment** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a0258-134">Wenn Sie das Zertifikat anzeigen möchten, doppelklicken Sie in der Liste auf das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a0258-134">if you want to view the certificate, double-click the certificate in the list.</span></span>

    
    </div>

18. <span data-ttu-id="a0258-135">Klicken Sie auf der Seite **Zertifikat Zuordnungszusammenfassung** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="a0258-135">On the **Certificate Assignment Summary** page, click **Next**.</span></span>

19. <span data-ttu-id="a0258-136">Klicken Sie auf der Seite **Ausführungsbefehle** auf **Fertig stellen** , nachdem die Ausführung der Befehle abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a0258-136">On the **Executing Commands** page, click **Finish** after the commands have finished running.</span></span>

20. <span data-ttu-id="a0258-137">Klicken Sie auf der Seite des **Zertifikat-Assistenten** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="a0258-137">On the **Certificate Wizard** page, click **Close**.</span></span>

<span data-ttu-id="a0258-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0258-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

