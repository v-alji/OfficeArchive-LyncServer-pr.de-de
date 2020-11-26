---
title: Beispiel für eine XMPP-Konfiguration – XMPP-Partnerverbund mit Google Talk
description: Beispiel für die XMPP-Konfiguration – XMPP Federation mit Google Talk.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428450"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a><span data-ttu-id="81d8c-103">Beispiel für eine XMPP-Konfiguration in Lync Server 2013 – XMPP-Partnerverbund mit Google Talk</span><span class="sxs-lookup"><span data-stu-id="81d8c-103">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81d8c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81d8c-104">

<span> </span></span></span>

<span data-ttu-id="81d8c-105">_**Letztes Änderungsdatum des Themas:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="81d8c-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="81d8c-106">Eine Beispielkonfiguration für die Bereitstellung des XMPP-Proxys definiert einen Verbund mit Google Talk.</span><span class="sxs-lookup"><span data-stu-id="81d8c-106">An example configuration for deploying the XMPP Proxy defines a federation with Google Talk.</span></span>

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a><span data-ttu-id="81d8c-107">Beispiel für eine XMPP-Konfiguration – XMPP-Partnerverbund mit Google Talk</span><span class="sxs-lookup"><span data-stu-id="81d8c-107">Example XMPP configuration – XMPP federation with Google Talk</span></span>

1.  <span data-ttu-id="81d8c-108">Öffnen Sie auf dem Front-End-Server den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="81d8c-108">On the Front End Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="81d8c-109">Klicken Sie auf **lync Server System** **Installieren** oder aktualisieren und dann auf **lync Server-Komponenten** **Einrichten** oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-109">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="81d8c-110">Klicken Sie **erneut auf Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-110">Click **Run Again**.</span></span>

2.  <span data-ttu-id="81d8c-111">Klicken Sie bei der **Installation von lync Server-Komponenten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-111">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="81d8c-112">Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81d8c-112">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="81d8c-113">Klicken Sie nach Abschluss der Bereitstellung auf **Protokoll anzeigen** , um die verfügbaren Protokolldateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-113">After the deployment is complete, click **View Log** to view available log files.</span></span> <span data-ttu-id="81d8c-114">Klicken Sie auf **Fertig stellen** , um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-114">Click **Finish** to complete the deployment.</span></span>

3.  <span data-ttu-id="81d8c-115">Öffnen Sie auf dem Edgeserver den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="81d8c-115">On the Edge Server, open the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="81d8c-116">Klicken Sie auf **lync Server System** **Installieren** oder aktualisieren und dann auf **lync Server-Komponenten** **Einrichten** oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-116">Click **Install** or **Update Lync Server System**, then click **Setup** or **Remove Lync Server Components**.</span></span> <span data-ttu-id="81d8c-117">Klicken Sie **erneut auf Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-117">Click **Run Again**.</span></span>

4.  <span data-ttu-id="81d8c-118">Als XMPP-Partner können Sie Google Talk hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-118">Add Google Talk as an XMPP allowed partner.</span></span> <span data-ttu-id="81d8c-119">Google Talk unterstützt derzeit nur unverschlüsselte TCP-Verbindungen für Server-zu-Server-XMPP-Föderationen und unterstützt nur Server-Dialback zur Identitätsüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="81d8c-119">Google Talk currently only supports unencrypted, TCP connections for server-to-server XMPP federation and only supports Server Dialback for identity verification.</span></span> <span data-ttu-id="81d8c-120">(Siehe <http://xmpp.org/extensions/xep-0220.html> ).</span><span class="sxs-lookup"><span data-stu-id="81d8c-120">(See <http://xmpp.org/extensions/xep-0220.html>).</span></span>
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  <span data-ttu-id="81d8c-121">Um Edge Federation zu aktivieren, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="81d8c-121">To enable Edge Federation, type the following:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  <span data-ttu-id="81d8c-122">Klicken Sie bei der **Installation von lync Server-Komponenten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-122">At **Setup Lync Server components**, click **Next**.</span></span> <span data-ttu-id="81d8c-123">Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81d8c-123">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="81d8c-124">Nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf **Protokoll anzeigen** , um die verfügbaren Protokolldateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-124">After the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="81d8c-125">Klicken Sie auf **Fertig stellen** , um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-125">Click **Finish** to complete the deployment.</span></span>

7.  <span data-ttu-id="81d8c-126">Klicken Sie auf dem Edgeserver im lync Server-Bereitstellungs-Assistenten neben **Schritt 3: anfordern, installieren oder Zuweisen von Zertifikaten** auf **erneut ausführen**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-126">On the Edge Server, in the Lync Server Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="81d8c-127">Wenn Sie den Edgeserver zum ersten Mal bereitstellen, wird Run anstelle von Run erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81d8c-127">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

8.  <span data-ttu-id="81d8c-128">Klicken Sie auf der Seite **Verfügbare Zertifikataufgaben** auf **Neue Zertifikatsanforderung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-128">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

9.  <span data-ttu-id="81d8c-129">Klicken Sie auf der Seite **Zertifikatanforderung** auf **externes Zertifikat**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-129">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

10. <span data-ttu-id="81d8c-130">Aktivieren Sie auf der Seite **verzögerte oder sofortige Anforderung** das Kontrollkästchen **Anforderung jetzt vorbereiten, aber später senden** .</span><span class="sxs-lookup"><span data-stu-id="81d8c-130">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

11. <span data-ttu-id="81d8c-131">Geben Sie auf der Seite **Zertifikatanforderungsdatei** den vollständigen Pfad und den Dateinamen der Datei ein, in der die Anforderung gespeichert werden soll (beispielsweise c: CERT, " \\ \_ \_ Edge. cer").</span><span class="sxs-lookup"><span data-stu-id="81d8c-131">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

12. <span data-ttu-id="81d8c-132">Aktivieren Sie auf der Seite **Alternative Zertifikatvorlage angeben** für das Kontrollkästchen **Alternative Zertifikatvorlage für die ausgewählte Zertifizierungsstelle verwenden** , um eine andere Vorlage als die standardmäßige Webservervorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="81d8c-132">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

13. <span data-ttu-id="81d8c-133">Gehen Sie auf der Seite **Name und Sicherheitseinstellungen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="81d8c-133">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="81d8c-134">Geben Sie unter **Anzeigename einen** Anzeigenamen für das Zertifikat ein.</span><span class="sxs-lookup"><span data-stu-id="81d8c-134">In **Friendly name**, type a display name for the certificate</span></span>
    
    2.  <span data-ttu-id="81d8c-135">Geben Sie in **Bit length** die Bit-Länge an (in der Regel der Standardwert von **2048**).</span><span class="sxs-lookup"><span data-stu-id="81d8c-135">In **Bit length**, specify the bit length (typically, the default of **2048**)</span></span>
    
    3.  <span data-ttu-id="81d8c-136">Überprüfen, ob das Kontrollkästchen " **Zertifikat privater Schlüssel als exportierbar kennzeichnen** " aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="81d8c-136">Verify that the **Mark certificate private key as exportable** check box is selected</span></span>

14. <span data-ttu-id="81d8c-137">Geben Sie auf der Seite **Organisationsinformationen** den Namen für die Organisation und die Organisationseinheit ein (beispielsweise eine Abteilung oder Abteilung).</span><span class="sxs-lookup"><span data-stu-id="81d8c-137">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department)</span></span>

15. <span data-ttu-id="81d8c-138">Geben Sie auf der Seite **geographische Informationen** die Standortinformationen an.</span><span class="sxs-lookup"><span data-stu-id="81d8c-138">On the **Geographical Information** page, specify the location information</span></span>

16. <span data-ttu-id="81d8c-139">Auf der Seite **Betreffname/Subject Alternative** Names werden die Informationen angezeigt, die automatisch vom Assistenten ausgefüllt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-139">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="81d8c-140">Wenn zusätzliche Alternative Namen für Subjekte benötigt werden, geben Sie diese in den nächsten beiden Schritten an.</span><span class="sxs-lookup"><span data-stu-id="81d8c-140">If additional subject alternative names are needed, you specify them in the next two steps</span></span>

17. <span data-ttu-id="81d8c-141">Aktivieren Sie in der **SIP-Domäneneinstellung auf der Seite Subject Alternate Names (SANs)** das Kontrollkästchen Domäne, um einen SIP hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-141">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.</span></span> <span data-ttu-id="81d8c-142">\<sipdomain\> Eintrag in die Liste der alternativen Subjektnamen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-142">\<sipdomain\> entry to the subject alternative names list.</span></span>

18. <span data-ttu-id="81d8c-143">Geben Sie auf der Seite **configure additional Subject Alternative Names** alle zusätzlichen alternativen Subjektnamen an, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="81d8c-143">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="81d8c-144">Wenn der XMPP-Proxy installiert ist, wird standardmäßig der Domänenname (wie contoso.com) in den San-Einträgen ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="81d8c-144">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="81d8c-145">Wenn Sie weitere Einträge benötigen, fügen Sie Sie in diesem Schritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="81d8c-145">If you require more entries, add them in this step.</span></span>

    
    </div>

19. <span data-ttu-id="81d8c-146">Überprüfen Sie auf der Seite **Anforderungszusammenfassung** die Zertifikatinformationen, die zum Generieren der Anforderung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-146">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

20. <span data-ttu-id="81d8c-147">Nachdem die Befehle ausgeführt wurden, können Sie das **Protokoll anzeigen** oder auf **weiter** klicken, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="81d8c-147">After the commands finish running, you can **View Log**, or click **Next** to continue.</span></span>

21. <span data-ttu-id="81d8c-148">Auf der Seite **Zertifikatanforderungsdatei** können Sie die generierte CSR-Datei (Certificate Signing Request) anzeigen, indem Sie auf **Fertig stellen** **klicken oder den** Zertifikat-Assistenten verlassen.</span><span class="sxs-lookup"><span data-stu-id="81d8c-148">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

22. <span data-ttu-id="81d8c-149">Kopieren Sie die Anforderungsdatei, und senden Sie Sie an Ihre öffentliche Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="81d8c-149">Copy the request file and submit to your public certification authority.</span></span>

23. <span data-ttu-id="81d8c-150">Nachdem Sie das öffentliche Zertifikat empfangen, importiert und zugewiesen haben, müssen Sie die Edgeserver-Dienste beenden und neu starten.</span><span class="sxs-lookup"><span data-stu-id="81d8c-150">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="81d8c-151">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="81d8c-151">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**..</span></span> <span data-ttu-id="81d8c-152">Geben Sie in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="81d8c-152">In the Lync Server Management Shell, type:</span></span>
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. <span data-ttu-id="81d8c-153">Zum Konfigurieren von DNS für die XMPP-Föderation fügen Sie den folgenden SRV-Eintrag zu externem DNS hinzu: \_ XMPP-Server. \_ TCP.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="81d8c-153">To configure DNS for XMPP federation, you add the following SRV record to external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="81d8c-154">Der SRV-Eintrag wird in den Access-Edge-FQDN des Edge-Servers aufgelöst, wobei der Portwert 5269</span><span class="sxs-lookup"><span data-stu-id="81d8c-154">The SRV record will resolve to the access edge FQDN of the Edge server, with a port value of 5269</span></span>

25. <span data-ttu-id="81d8c-155">Konfigurieren Sie eine neue Richtlinie für den externen Zugriff, um alle Benutzer zu aktivieren, indem Sie die lync Server-Verwaltungsshell auf einem Front-End-Server öffnen und Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="81d8c-155">Configure a new External Access Policy to enable all users by opening the Lync Server Management Shell on a Front End Server and typing:</span></span>
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

<span data-ttu-id="81d8c-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81d8c-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

