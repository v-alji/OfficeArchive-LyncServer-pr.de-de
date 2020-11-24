---
title: Konfigurieren des XMPP-Gateways auf lync Server 2013
description: Konfigurieren des XMPP-Gateways auf lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure XMPP gateway on Lync Server 2013
ms:assetid: c70282e0-b502-47e2-a0be-a32eb1faf99d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721881(v=OCS.15)
ms:contentKeyID: 49733816
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 78765237e737dea29d77230d6b0eecdb0348cb41
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394431"
---
# <a name="configure-xmpp-gateway-on-lync-server-2013"></a><span data-ttu-id="9f1eb-103">Konfigurieren des XMPP-Gateways auf lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f1eb-103">Configure XMPP gateway on Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f1eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f1eb-104">

<span> </span></span></span>

<span data-ttu-id="9f1eb-105">_**Letztes Änderungsdatum des Themas:** 2013-10-28_</span><span class="sxs-lookup"><span data-stu-id="9f1eb-105">_**Topic Last Modified:** 2013-10-28_</span></span>

<span data-ttu-id="9f1eb-106">Die letzten Schritte für die Migration Ihres XMPP-Gateways bestehen darin, Zertifikate für den lync Server 2013 Edge-Server zu konfigurieren, das lync Server 2013 XMPP-Gateway bereitzustellen und die DNS-Einträge für das XMPP-Gateway zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-106">The final steps for migrating your XMPP Gateway are to configure certificates for the Lync Server 2013 Edge Server, deploy the Lync Server 2013 XMPP Gateway, and update the DNS records for the XMPP Gateway.</span></span> <span data-ttu-id="9f1eb-107">Diese Schritte sollten parallel ausgeführt werden, um die Ausfallzeit Ihres XMPP-Gateways zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-107">These steps should be performed in parallel to minimize the down time of your XMPP Gateway.</span></span> <span data-ttu-id="9f1eb-108">Bevor Sie diese Schritte ausführen können, müssen alle Benutzer in Ihre Microsoft lync Server 2013-Bereitstellung verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-108">All users must be moved to your Microsoft Lync Server 2013 deployment before performing these steps.</span></span>

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="9f1eb-109">Die XMPP-Föderation wird für Benutzer nicht unterstützt, die sich auf Überlebenden Branch-Appliances befinden.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-109">XMPP federation is not supported for users who are homed on survivable branch appliances.</span></span> <span data-ttu-id="9f1eb-110">Dies gilt sowohl für das Anzeigen von Anwesenheitsinformationen als auch für den Austausch von Chatnachrichten.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-110">This applies to both seeing presence information and exchanging IM messages.</span></span>



</div>

<div>

## <a name="configure-xmpp-gateway-certificates-on-the-lync-server-2013-edge-server"></a><span data-ttu-id="9f1eb-111">Konfigurieren von XMPP-Gateway-Zertifikaten auf dem lync Server 2013-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="9f1eb-111">Configure XMPP Gateway Certificates on the Lync Server 2013 Edge Server</span></span>

1.  <span data-ttu-id="9f1eb-112">Klicken Sie auf dem Edgeserver im Bereitstellungs-Assistenten neben **Schritt 3: anfordern, installieren oder Zuweisen von Zertifikaten** auf **erneut ausführen**.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-112">On the Edge Server, in the Deployment Wizard, next to **Step 3: Request, Install, or Assign Certificates**, click **Run again**.</span></span>
    
    <div class=" ">
    

    > [!TIP]  
    > <span data-ttu-id="9f1eb-113">Wenn Sie den Edgeserver zum ersten Mal bereitstellen, wird Run anstelle von Run erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-113">If you are deploying the Edge Server for the first time, you will see Run instead of Run Again.</span></span>

    
    </div>

2.  <span data-ttu-id="9f1eb-114">Klicken Sie auf der Seite **Verfügbare Zertifikataufgaben** auf **Neue Zertifikatsanforderung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-114">On the **Available Certificate Tasks** page, click **Create a new certificate request**.</span></span>

3.  <span data-ttu-id="9f1eb-115">Klicken Sie auf der Seite **Zertifikatanforderung** auf **externes Zertifikat**.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-115">On the **Certificate Request** page, click **External Edge Certificate**.</span></span>

4.  <span data-ttu-id="9f1eb-116">Aktivieren Sie auf der Seite **verzögerte oder sofortige Anforderung** das Kontrollkästchen **Anforderung jetzt vorbereiten, aber später senden** .</span><span class="sxs-lookup"><span data-stu-id="9f1eb-116">On the **Delayed or Immediate Request** page, select the **Prepare the request now, but send it later** check box.</span></span>

5.  <span data-ttu-id="9f1eb-117">Geben Sie auf der Seite **Zertifikatanforderungsdatei** den vollständigen Pfad und den Dateinamen der Datei ein, in der die Anforderung gespeichert werden soll (beispielsweise c: CERT, " \\ \_ \_ Edge. cer").</span><span class="sxs-lookup"><span data-stu-id="9f1eb-117">On the **Certificate Request File** page, type the full path and file name of the file to which the request is to be saved (for example, c:\\cert\_exernal\_edge.cer).</span></span>

6.  <span data-ttu-id="9f1eb-118">Aktivieren Sie auf der Seite **Alternative Zertifikatvorlage angeben** für das Kontrollkästchen **Alternative Zertifikatvorlage für die ausgewählte Zertifizierungsstelle verwenden** , um eine andere Vorlage als die standardmäßige Webservervorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-118">On the **Specify Alternate Certificate Template** page, to use a template other than the default WebServer template, select the **Use alternative certificate template for the selected certification authority** check box.</span></span>

7.  <span data-ttu-id="9f1eb-119">Gehen Sie auf der Seite **Name und Sicherheitseinstellungen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-119">On the **Name and Security Settings** page, do the following:</span></span>
    
    1.  <span data-ttu-id="9f1eb-120">Geben Sie unter Anzeige **Name** einen Anzeigenamen für das Zertifikat ein.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-120">In **Friendly name**, type a display name for the certificate.</span></span>
    
    2.  <span data-ttu-id="9f1eb-121">Geben Sie in **Bit length** die Bittiefe (in der Regel den Standardwert von 2048) an.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-121">In **Bit length**, specify the bit length (typically, the default of 2048).</span></span>
    
    3.  <span data-ttu-id="9f1eb-122">Überprüfen Sie, ob das Kontrollkästchen **Zertifikat privater Schlüssel als exportierbar kennzeichnen** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-122">Verify that the **Mark certificate private key as exportable** check box is selected.</span></span>

8.  <span data-ttu-id="9f1eb-123">Geben Sie auf der Seite **Organisationsinformationen** den Namen für die Organisation und die Organisationseinheit ein (beispielsweise eine Abteilung oder Abteilung).</span><span class="sxs-lookup"><span data-stu-id="9f1eb-123">On the **Organization Information** page, type the name for the organization and the organizational unit (for example, a division or department).</span></span>

9.  <span data-ttu-id="9f1eb-124">Geben Sie auf der Seite **geographische Informationen** die Standortinformationen an.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-124">On the **Geographical Information** page, specify the location information.</span></span>

10. <span data-ttu-id="9f1eb-125">Auf der Seite **Betreffname/Subject Alternative** Names werden die Informationen angezeigt, die automatisch vom Assistenten ausgefüllt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-125">On the **Subject Name/Subject Alternate Names** page, the information to be automatically populated by the wizard is displayed.</span></span> <span data-ttu-id="9f1eb-126">Wenn zusätzliche Alternative Namen für Subjekte benötigt werden, geben Sie diese in den nächsten beiden Schritten an.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-126">If additional subject alternative names are needed, you specify them in the next two steps.</span></span>

11. <span data-ttu-id="9f1eb-127">Aktivieren Sie in der **SIP-Domäneneinstellung auf der Seite Subject Alternate Names (SANs)** das Kontrollkästchen Domäne, um einen SIP hinzuzufügen.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="9f1eb-127">On the **SIP Domain Setting on Subject Alternate Names (SANs)** page, select the domain check box to add a sip.\<sipdomain\></span></span> <span data-ttu-id="9f1eb-128">Eintrag in die Liste der alternativen Subjektnamen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-128">entry to the subject alternative names list.</span></span>

12. <span data-ttu-id="9f1eb-129">Geben Sie auf der Seite **configure additional Subject Alternative Names** alle zusätzlichen alternativen Subjektnamen an, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-129">On the **Configure Additional Subject Alternate Names** page, specify any additional subject alternative names that are required.</span></span>
    
    <div class=" ">
    

    > [!TIP]  
    > <span data-ttu-id="9f1eb-130">Wenn der XMPP-Proxy installiert ist, wird standardmäßig der Domänenname (wie contoso.com) in den San-Einträgen ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-130">If the XMPP proxy is installed, by default the domain name (such as contoso.com) is populated in the SAN entries.</span></span> <span data-ttu-id="9f1eb-131">Wenn Sie weitere Einträge benötigen, fügen Sie Sie in diesem Schritt hinzu.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-131">If you require more entries, add them in this step.</span></span>

    
    </div>

13. <span data-ttu-id="9f1eb-132">Überprüfen Sie auf der Seite **Anforderungszusammenfassung** die Zertifikatinformationen, die zum Generieren der Anforderung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-132">On the **Request Summary** page, review the certificate information to be used to generate the request.</span></span>

14. <span data-ttu-id="9f1eb-133">Nachdem die Befehle ausgeführt wurden, können Sie das **Protokoll anzeigen** oder auf Weiter klicken, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-133">After the commands finish running, you can **View Log**, or click Next to continue.</span></span>

15. <span data-ttu-id="9f1eb-134">Auf der Seite **Zertifikatanforderungsdatei** können Sie die generierte CSR-Datei (Certificate Signing Request) anzeigen, indem Sie auf **Fertig stellen** **klicken oder den** Zertifikat-Assistenten verlassen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-134">On the **Certificate Request File** page, you can view the generated certificate signing request (CSR) file by clicking **View** or exit the Certificate Wizard by clicking **Finish**.</span></span>

16. <span data-ttu-id="9f1eb-135">Kopieren Sie die Anforderungsdatei, und senden Sie Sie an Ihre öffentliche Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-135">Copy the request file and submit to your public certification authority.</span></span>

17. <span data-ttu-id="9f1eb-136">Nachdem Sie das öffentliche Zertifikat empfangen, importiert und zugewiesen haben, müssen Sie die Edgeserver-Dienste beenden und neu starten.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-136">After receiving, importing and assigning the public certificate, you must stop and restart the Edge Server services.</span></span> <span data-ttu-id="9f1eb-137">Hierzu geben Sie in der lync Server-Verwaltungskonsole Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-137">You do this by typing in the Lync Server Management console:</span></span>
    
        Stop-CsWindowsService

      &nbsp;
    
        Start-CsWindowsService

</div>

<div>

## <a name="configure-a-new-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="9f1eb-138">Konfigurieren eines neuen lync Server 2013 XMPP-Gateways</span><span class="sxs-lookup"><span data-stu-id="9f1eb-138">Configure a new Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="9f1eb-139">Öffnen Sie die Lync Server-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-139">Open Lync Server Control Panel.</span></span>

2.  <span data-ttu-id="9f1eb-140">Klicken Sie in der linken Navigationsleiste auf **Föderation und externer Zugriff** , und klicken Sie dann auf **XMPP Federated Partners**.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-140">In the left navigation bar, click **Federation and External Access** and then click **XMPP Federated Partners**.</span></span>

3.  <span data-ttu-id="9f1eb-141">Wenn Sie eine neue Konfiguration erstellen möchten, klicken Sie auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-141">To create a new configuration, click **New**.</span></span>

4.  <span data-ttu-id="9f1eb-142">Definieren Sie die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-142">Define the following settings:</span></span>

5.  <span data-ttu-id="9f1eb-143">**Primäre Domäne**    (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="9f1eb-143">**Primary domain**    (Required).</span></span> <span data-ttu-id="9f1eb-144">Die primäre Domäne ist die Basisdomäne des XMPP-Partners.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-144">The primary domain is the base domain of the XMPP partner.</span></span> <span data-ttu-id="9f1eb-145">Geben Sie beispielsweise **Fabrikam.com** für den Namen der XMPP-Partnerdomäne ein.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-145">For example, you would enter **fabrikam.com** for the XMPP partner domain name.</span></span> <span data-ttu-id="9f1eb-146">Dies ist ein erforderlicher Eintrag.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-146">This is a required entry.</span></span>

6.  <span data-ttu-id="9f1eb-147">**Beschreibung**   Die Beschreibung ist für Notizen oder andere identifizierende Informationen für diese bestimmte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-147">**Description**   The description is for notes or other identifying information for this particular configuration.</span></span> <span data-ttu-id="9f1eb-148">Dieser Eintrag ist optional.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-148">This entry is optional.</span></span>

7.  <span data-ttu-id="9f1eb-149">**Zusätzliche Domänen**   Zusätzliche Domänen sind Domänen, die Teil der Domäne Ihres XMPP-Partners sind und als Teil der zulässigen XMPP-Kommunikation enthalten sein sollten.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-149">**Additional domains**   Additional domains are domains that are a part of your XMPP partner’s domain that should be included as part of the allowed XMPP communication.</span></span> <span data-ttu-id="9f1eb-150">Wenn es sich bei der primären Domäne beispielsweise um **Fabrikam.com** handelt, werden alle anderen Domänen aufgelistet, die unter fabrikam.com sind, mit denen Sie über XMPP kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-150">For example, if the primary domain is **fabrikam.com**, then you would list all other domains that are under fabrikam.com that you will communicate with by way of XMPP.</span></span>

8.  <span data-ttu-id="9f1eb-151">**Partnertyp**   Der **Partnertyp** ist eine erforderliche Einstellung.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-151">**Partner type**   The **Partner type** is a required setting.</span></span> <span data-ttu-id="9f1eb-152">Sie müssen eine der folgenden Optionen auswählen, um zu beschreiben und zu erzwingen, welche Kontakte hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-152">You must choose one of the following to describe and enforce what contacts can be added.</span></span> <span data-ttu-id="9f1eb-153">Sie können Folgendes auswählen:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-153">You can select from:</span></span>
    
      - <span data-ttu-id="9f1eb-154">**Federated**   Ein **Federated** -Partner-Typ stellt eine hohe Vertrauensebene zwischen der lync Server-Bereitstellung und dem XMPP-Partner dar.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-154">**Federated**   A **Federated** partner type represents a high level of trust between the Lync Server deployment and the XMPP partner.</span></span>  <span data-ttu-id="9f1eb-155">Dieser Partnertyp wird für die Föderation mit XMPP-Servern innerhalb desselben Unternehmens oder mit einer festgelegten Geschäftsbeziehung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-155">This partner type is recommended for federating with XMPP servers within the same enterprise or where there is an established business relationship.</span></span>  <span data-ttu-id="9f1eb-156">XMPP-Kontakte in Verbundpartnern können:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-156">XMPP contacts in Federated partners can:</span></span>
        
        1.  <span data-ttu-id="9f1eb-157">Fügen Sie lync-Kontakte hinzu, und zeigen Sie deren Anwesenheit ohne ausdrückliche Autorisierung des lync-Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-157">Add Lync contacts and view their presence without express authorization from the Lync user.</span></span>
        
        2.  <span data-ttu-id="9f1eb-158">Senden Sie Sofortnachrichten an lync-Kontakte, unabhängig davon, ob der lync-Benutzer Sie in seine Kontaktliste aufgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-158">Send instant messages to Lync contacts whether or not the Lync user has added them into their contact list.</span></span>
        
        3.  <span data-ttu-id="9f1eb-159">Anzeigen der Status Notizen eines lync-Benutzers</span><span class="sxs-lookup"><span data-stu-id="9f1eb-159">See a Lync user’s status notes.</span></span>
    
      - <span data-ttu-id="9f1eb-160">**Öffentlich bestätigt**   Ein **öffentlich überprüfter** Partner ist ein öffentlicher XMPP-Anbieter, der als vertrauenswürdig eingestuft wird, um die Identität seiner Benutzer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-160">**Public verified**   A **Public verified** partner is a public XMPP provider that is trusted to verify the identity of its users.</span></span>  <span data-ttu-id="9f1eb-161">XMPP-Kontakte in öffentlich überprüfte Netzwerke können lync-Kontakte hinzufügen und deren Anwesenheit anzeigen und Ihnen Sofortnachrichten senden, ohne die ausdrückliche Autorisierung der lync-Benutzer zu haben.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-161">XMPP contacts in Public Verified networks can add Lync contacts and view their presence and send instant messages to them without express authorization from the Lync users.</span></span>  <span data-ttu-id="9f1eb-162">Bei XMPP-Kontakten in öffentlich überprüften Netzwerken werden die Status Notizen der lync-Benutzer nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-162">XMPP contacts in public verified networks never see a Lync users’ status notes.</span></span>  <span data-ttu-id="9f1eb-163">Diese Einstellung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-163">This setting is not recommended.</span></span>
    
      - <span data-ttu-id="9f1eb-164">**Öffentliche nicht bestätigt**   Ein **öffentlicher, nicht überprüfter** Partner ist ein öffentlicher XMPP-Anbieter, der nicht als vertrauenswürdig eingestuft wird, um die Identität seiner Benutzer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-164">**Public unverified**   A **Public unverified** partner is a public XMPP provider that is not trusted to verify the identity of its users.</span></span>  <span data-ttu-id="9f1eb-165">XMPP-Benutzer in öffentlichen nicht überprüften Netzwerken können nicht mit lync-Benutzern kommunizieren, es sei denn, der lync-Benutzer hat Sie ausdrücklich autorisiert, indem Sie Sie der Kontaktliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-165">XMPP users on Public Unverified networks cannot communicate with Lync users unless the Lync user has expressly authorized them by adding them to the contact list.</span></span>  <span data-ttu-id="9f1eb-166">Für XMPP-Benutzer in öffentlichen nicht überprüften Netzwerken werden die Status Notizen von lync-Benutzern nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-166">XMPP users on public unverified networks never see Lync users’ status notes.</span></span>  <span data-ttu-id="9f1eb-167">Diese Einstellung wird für alle Föderationen mit öffentlichen XMPP-Anbietern wie Google Talk empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-167">This setting is recommended for any federation with public XMPP providers such as Google Talk.</span></span>

9.  <span data-ttu-id="9f1eb-168">**Verbindungstyp:** Definiert die verschiedenen Regeln und Dialback-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-168">**Connection Type:** Defines the various rules and dialback settings.</span></span>
    
      - <span data-ttu-id="9f1eb-169">**TLS-Aushandlung**   Definiert die TLS-Aushandlungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-169">**TLS Negotiation**   Defines the TLS negotiation rules.</span></span> <span data-ttu-id="9f1eb-170">Ein XMPP-Dienst kann TLS erfordern, kann TLS optional machen, oder Sie definieren, dass TLS nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-170">An XMPP service can require TLS, can make TLS optional, or you define that TLS is not supported.</span></span> <span data-ttu-id="9f1eb-171">Wenn Sie optional auswählen, bleibt die Anforderung dem XMPP-Dienst für eine obligatorische Aushandlungs Entscheidung überlassen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-171">Choosing Optional leaves the requirement up to the XMPP service for a mandatory-to-negotiate decision.</span></span> <span data-ttu-id="9f1eb-172">Informationen zum Anzeigen aller möglichen Einstellungen und Details für SASL-, TLS-und Dialback-Aushandlung – einschließlich Ungültiger und bekannter Fehler Konfigurationen – finden Sie unter [Aushandlungs Einstellungen für XMPP-Verbundpartner in lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="9f1eb-172">To view all possible settings and details for SASL, TLS and Dialback negotiation –including not valid and known error configurations - see [Negotiation settings for XMPP federated partners in Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-173">**Erforderlich**   Der XMPP-Dienst erfordert TLS-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-173">**Required**   The XMPP service requires TLS negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-174">**Optional**   Der XMPP-Dienst gibt an, dass TLS obligatorisch-zu-Negotiate ist.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-174">**Optional**   The XMPP service indicates that TLS is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-175">**Nicht unterstützt**   Der XMPP-Dienst unterstützt keine TLS-Funktion.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-175">**Not Supported**   The XMPP service does not support TLS.</span></span>
    
      - <span data-ttu-id="9f1eb-176">**SASL-Aushandlung**   Definiert die SASL-Aushandlungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-176">**SASL negotiation**   Defines the SASL negotiation rules.</span></span> <span data-ttu-id="9f1eb-177">Ein XMPP-Dienst kann SASL erfordern, kann SASL optional machen, oder Sie definieren, dass SASL nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-177">An XMPP service can require SASL, can make SASL optional, or you define that SASL is not supported.</span></span> <span data-ttu-id="9f1eb-178">Wenn Sie optional auswählen, bleibt die Anforderung dem Partner XMPP-Dienst für eine obligatorische-zu-Aushandlungs Entscheidung überlassen.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-178">Choosing Optional leaves the requirement up to the partner XMPP service for a mandatory-to-negotiate decision.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-179">**Erforderlich**   Der XMPP-Dienst erfordert SASL-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-179">**Required**   The XMPP service requires SASL negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-180">**Optional**   Der XMPP-Dienst gibt an, dass SASL obligatorisch-zu-Negotiate ist.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-180">**Optional**   The XMPP service indicates that SASL is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-181">**Nicht unterstützt**   SASL wird vom XMPP-Dienst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-181">**Not Supported**   The XMPP service does not support SASL.</span></span>
    
      - <span data-ttu-id="9f1eb-182">**Support Server-Dialback-Aushandlung** Der Dialback-Aushandlungsprozess für Support Server verwendet das Domain Name System (DNS) und einen autorisierenden Server, um zu überprüfen, ob die Anforderung von einem gültigen XMPP-Partner kam.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-182">**Support server dialback negotiation** The support server dialback negotiation process uses the domain name system (DNS) and an authoritative server to verify that the request came from a valid XMPP partner.</span></span> <span data-ttu-id="9f1eb-183">Zu diesem Zweck erstellt der ursprüngliche Server eine Nachricht eines bestimmten Typs mit einem generierten Dialback-Schlüssel und schlägt den empfangenden Server in DNS nach.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-183">To do this, the originating server creates a message of a specific type with a generated dialback key and looks up the receiving server in DNS.</span></span> <span data-ttu-id="9f1eb-184">Der ursprüngliche Server sendet den Schlüssel in einem XML-Datenstrom an den resultierenden DNS-Lookup, vermutlich den empfangenden Server.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-184">The originating server sends the key in an XML stream to the resulting DNS lookup, presumably the receiving server.</span></span> <span data-ttu-id="9f1eb-185">Nach Erhalt des Schlüssels über den XML-Datenstrom antwortet der empfangende Server nicht auf den ursprünglichen Server, sondern sendet den Schlüssel an einen bekannten autorisierenden Server.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-185">On receipt of the key over the XML stream, the receiving server does not respond to the originating server, but sends the key to a known authoritative server.</span></span> <span data-ttu-id="9f1eb-186">Der autorisierende Server überprüft, ob der Schlüssel entweder gültig oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-186">The authoritative server verifies that the key is either valid or not valid.</span></span> <span data-ttu-id="9f1eb-187">Wenn dies nicht der Fall ist, antwortet der empfangende Server nicht auf den ursprünglichen Server.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-187">If not valid, the receiving server does not respond to the originating server.</span></span> <span data-ttu-id="9f1eb-188">Wenn der Schlüssel gültig ist, informiert der empfangende Server den Ursprungsserver, dass Identität und Schlüssel gültig sind und die Konversation beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-188">If the key is valid, the receiving server informs the originating server that the identity and key is valid and the conversation can commence.</span></span>
        
        <span data-ttu-id="9f1eb-189">Es gibt zwei gültige Zustände für **Dialback-Aushandlung**:</span><span class="sxs-lookup"><span data-stu-id="9f1eb-189">There are two valid states for **Dialback negotiation**:</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-190">**True**   Der XMPP-Server ist für die Verwendung von Dialback-Aushandlung konfiguriert, wenn eine Anforderung von einem Ursprungsserver empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-190">**True**   The XMPP server is configured to use Dialback negotiation if a request should be received from an originating server.</span></span>
        
          - <span></span>  
            <span data-ttu-id="9f1eb-191">**False**   Der XMPP-Server ist nicht für die Verwendung von Dialback-Aushandlung konfiguriert, und wenn eine Anforderung von einem Ursprungsserver empfangen werden soll, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-191">**False**   The XMPP server is not configured to use Dialback negotiation and if a request should be received from an originating server, it will be ignored.</span></span>

10. <span data-ttu-id="9f1eb-192">Klicken Sie auf **Commit** , um Ihre Änderungen an der Website-oder Benutzerrichtlinie zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-192">Click **Commit** to save your changes to the site or user policy.</span></span>

</div>

<div>

## <a name="update-dns-records-for-lync-server-2013-xmpp-gateway"></a><span data-ttu-id="9f1eb-193">Aktualisieren von DNS-Einträgen für lync Server 2013 XMPP-Gateway</span><span class="sxs-lookup"><span data-stu-id="9f1eb-193">Update DNS Records for Lync Server 2013 XMPP Gateway</span></span>

1.  <span data-ttu-id="9f1eb-194">Zum Konfigurieren von DNS für die XMPP-Föderation fügen Sie den folgenden SRV-Eintrag zu Ihrem externen DNS hinzu: \_ XMPP-Server. \_ TCP.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="9f1eb-194">To configure DNS for XMPP federation, you add the following SRV record to your external DNS:\_xmpp-server.\_tcp.\<domain name\></span></span> <span data-ttu-id="9f1eb-195">Der SRV-Eintrag wird in den Access-Edge-FQDN des Edge-Servers aufgelöst, wobei der Portwert 5269 ist.</span><span class="sxs-lookup"><span data-stu-id="9f1eb-195">The SRV record will resolve to the Access Edge FQDN of the Edge server, with a port value of 5269.</span></span>

<span data-ttu-id="9f1eb-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f1eb-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

