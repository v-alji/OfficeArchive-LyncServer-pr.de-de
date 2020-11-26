---
title: 'Lync Server 2013: Erstellen oder Bearbeiten einer XMPP-Verbundpartnerkonfiguration'
description: 'Lync Server 2013: Erstellen oder Bearbeiten der XMPP-Partnerkonfiguration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or edit XMPP partner configuration
ms:assetid: 362dbe5e-8ee9-4aba-8c26-5907312b4a60
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552447(v=OCS.15)
ms:contentKeyID: 48679558
ms.date: 09/03/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19289df1920287984f104bb1bdfa214d6f83f5cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431855"
---
# <a name="create-or-edit-xmpp-partner-configuration-in-lync-server-2013"></a><span data-ttu-id="91ee6-103">Erstellen oder Bearbeiten einer XMPP-Verbundpartnerkonfiguration in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91ee6-103">Create or edit XMPP partner configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91ee6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91ee6-104">

<span> </span></span></span>

<span data-ttu-id="91ee6-105">_**Letztes Änderungsdatum des Themas:** 2014-09-03_</span><span class="sxs-lookup"><span data-stu-id="91ee6-105">_**Topic Last Modified:** 2014-09-03_</span></span>

<span data-ttu-id="91ee6-106">Microsoft lync Server 2013 integriert einen Extensible Messaging and Presence Protocol (XMPP)-Proxy auf dem Edgeserver und ein XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="91ee6-106">Microsoft Lync Server 2013 integrates an Extensible Messaging and Presence Protocol (XMPP) proxy on the Edge Server and an XMPP Gateway on the Front End Server or Front End pool.</span></span> <span data-ttu-id="91ee6-107">Damit Verbindungen von anderen XMPP-Bereitstellungen zugelassen werden, müssen Sie xmpp in der lync Server-Systemsteuerung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="91ee6-107">To allow connections from other XMPP deployments, you must configure XMPP in the Lync Server Control Panel.</span></span> <span data-ttu-id="91ee6-108">Sie konfigurieren die Einstellungen auf einer XMPP-Domänenbasis.</span><span class="sxs-lookup"><span data-stu-id="91ee6-108">You configure settings on an XMPP domain basis.</span></span> <span data-ttu-id="91ee6-109">Gehen Sie wie folgt vor, um eine neue Partnerzuordnung zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="91ee6-109">To create a new partner association, you do the following:</span></span>

<div>

## <a name="to-create-a-new-federated-partner-or-edit-an-existing-configuration"></a><span data-ttu-id="91ee6-110">So erstellen Sie einen neuen Föderationspartner oder bearbeiten eine vorhandene Konfiguration</span><span class="sxs-lookup"><span data-stu-id="91ee6-110">To create a new federated partner or edit an existing configuration</span></span>

1.  <span data-ttu-id="91ee6-111">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="91ee6-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="91ee6-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="91ee6-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="91ee6-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="91ee6-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="91ee6-114">Klicken Sie in der linken Navigationsleiste auf **Föderation und externer Zugriff**, und klicken Sie dann auf **XMPP Federated Partners**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-114">In the left navigation bar, click **Federation and External Access**, and then click **XMPP Federated Partners**.</span></span>

4.  <span data-ttu-id="91ee6-115">Wenn Sie eine neue Konfiguration erstellen möchten, klicken Sie auf **neu** .</span><span class="sxs-lookup"><span data-stu-id="91ee6-115">To create a new configuration, click **New**</span></span>

5.  <span data-ttu-id="91ee6-116">Wenn Sie eine vorhandene Konfiguration bearbeiten möchten, wählen Sie die Konfiguration aus, und klicken Sie auf **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="91ee6-116">To edit an existing configuration, select the configuration and click **Edit**</span></span>

6.  <span data-ttu-id="91ee6-117">Zum Erstellen oder Bearbeiten von Konfigurationen für **XMPP-Verbundpartner** definieren Sie die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="91ee6-117">To create or edit configurations for **XMPP Federated Partners**, you define the following settings:</span></span>

7.  <span data-ttu-id="91ee6-118">**Primäre Domäne** (erforderlich).</span><span class="sxs-lookup"><span data-stu-id="91ee6-118">**Primary domain** (Required).</span></span> <span data-ttu-id="91ee6-119">Die primäre Domäne ist die Basisdomäne des XMPP-Partners.</span><span class="sxs-lookup"><span data-stu-id="91ee6-119">The primary domain is the base domain of the XMPP partner.</span></span> <span data-ttu-id="91ee6-120">Geben Sie beispielsweise **Fabrikam.com** für den Namen der XMPP-Partnerdomäne ein.</span><span class="sxs-lookup"><span data-stu-id="91ee6-120">For example, you would enter **fabrikam.com** for the XMPP partner domain name.</span></span> <span data-ttu-id="91ee6-121">Dies ist ein erforderlicher Eintrag.</span><span class="sxs-lookup"><span data-stu-id="91ee6-121">This is a required entry.</span></span>

8.  <span data-ttu-id="91ee6-122">**Beschreibung** aus.</span><span class="sxs-lookup"><span data-stu-id="91ee6-122">**Description**.</span></span> <span data-ttu-id="91ee6-123">Die Beschreibung ist für Notizen oder andere identifizierende Informationen für diese bestimmte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="91ee6-123">The description is for notes or other identifying information for this particular configuration.</span></span> <span data-ttu-id="91ee6-124">Dieser Eintrag ist optional.</span><span class="sxs-lookup"><span data-stu-id="91ee6-124">This entry is optional.</span></span>

9.  <span data-ttu-id="91ee6-125">**Zusätzliche Domänen**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-125">**Additional domains**.</span></span> <span data-ttu-id="91ee6-126">Zusätzliche Domänen sind Domänen, die Teil der Domäne Ihres XMPP-Partners sind und als Teil der zulässigen XMPP-Kommunikation enthalten sein sollten.</span><span class="sxs-lookup"><span data-stu-id="91ee6-126">Additional domains are domains that are a part of your XMPP partner’s domain that should be included as part of the allowed XMPP communication.</span></span> <span data-ttu-id="91ee6-127">Wenn es sich bei der primären Domäne beispielsweise um **Fabrikam.com** handelt, werden alle anderen Domänen aufgelistet, die unter fabrikam.com sind, mit denen Sie über XMPP kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="91ee6-127">For example, if the primary domain is **fabrikam.com**, then you would list all other domains that are under fabrikam.com that you will communicate with by way of XMPP.</span></span> <span data-ttu-id="91ee6-128">So können Sie beispielsweise **Corp.fabrikam.com** und **IT.fabrikam.com** für die Unternehmens-XMPP-Domäne und die XMPP-Domäne Informationstechnologien unter der Haupt-XMPP-Domäne von fabrikam. com eingeben.</span><span class="sxs-lookup"><span data-stu-id="91ee6-128">For example, you might enter **corp.fabrikam.com** and **it.fabrikam.com** for the Corporate XMPP domain and the Information Technologies XMPP domain under fabrikam.com’s main XMPP domain.</span></span>

10. <span data-ttu-id="91ee6-129">**Partnertyp**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-129">**Partner type**.</span></span> <span data-ttu-id="91ee6-130">Der **Partnertyp** ist eine erforderliche Einstellung und bietet in einem Dropdownmenü drei Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="91ee6-130">The **Partner type** is a required setting and gives you a selection of three choices in a drop-down menu.</span></span> <span data-ttu-id="91ee6-131">Sie müssen eine der folgenden Optionen auswählen, um zu beschreiben und zu erzwingen, welche Kontakte hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="91ee6-131">You must choose one of the following to describe and enforce what contacts can be added.</span></span> <span data-ttu-id="91ee6-132">Sie können Folgendes auswählen:</span><span class="sxs-lookup"><span data-stu-id="91ee6-132">You can select from:</span></span>
    
      - <span data-ttu-id="91ee6-133">**Federated**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-133">**Federated**.</span></span> <span data-ttu-id="91ee6-134">Ein **Federated** -Partner-Typ ist eine vertrauenswürdige Verbindung zwischen einer lync Server-oder Office Communications Server 2007 R2-Partner Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="91ee6-134">A **Federated** partner type is a trusted connection between a Lync Server or Office Communications Server 2007 R2 partner deployment.</span></span>
    
      - <span data-ttu-id="91ee6-135">**Öffentlich verifiziert**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-135">**Public verified**.</span></span> <span data-ttu-id="91ee6-136">Ein **öffentlich überprüfter** Partner ist, wenn Kontakte, die Teil einer Bereitstellung sind, die vom Anbieter überprüft werden, der Kontaktliste des Benutzers hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="91ee6-136">A **Public verified** partner is when contacts that are part of a deployment that are verified by the provider can be added to your user’s list of contacts.</span></span> <span data-ttu-id="91ee6-137">Einladungen können vom lync-Benutzer gesendet werden, oder der lync-Benutzer kann Einladungen vom Partner Kontakt akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="91ee6-137">Invites can be sent from the Lync user or the Lync user can accept invites from the partner contact.</span></span>
    
      - <span data-ttu-id="91ee6-138">**Öffentlich nicht überprüft**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-138">**Public unverified**.</span></span> <span data-ttu-id="91ee6-139">Eine **öffentliche** nicht überprüfte Beziehung impliziert, dass es zwischen den beiden Bereitstellungen keinen festgelegten und überprüfbaren Status gibt.</span><span class="sxs-lookup"><span data-stu-id="91ee6-139">A **Public unverified** relationship implies that there is no established and verifiable status between the two deployments.</span></span> <span data-ttu-id="91ee6-140">Ein lync-Benutzer muss den nicht überprüften Kontakt für diesen Kontakt einladen, um den lync-Benutzer in seine Kontaktliste aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="91ee6-140">A Lync user must invite the unverified contact for that contact to be able to add the Lync user to his contact list.</span></span> <span data-ttu-id="91ee6-141">Beispielsweise ist Google Gtalk kein öffentlicher überprüfter XMPP-Dienst, da es sich um lync Server handelt.</span><span class="sxs-lookup"><span data-stu-id="91ee6-141">For example, Google GTalk is not a public verified XMPP service as it relates to Lync Server.</span></span> <span data-ttu-id="91ee6-142">Ein GTalk-Benutzer kann den lync-Benutzer nur dann als Kontakt hinzufügen, wenn eine explizite Einladung vom lync-Benutzer gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="91ee6-142">A GTalk user will not be able to add the Lync user as a contact unless there is an explicit invite sent from the Lync user.</span></span>

11. <span data-ttu-id="91ee6-143">Hinweise zur Datenstrom Aushandlung und den Sicherheitsmethoden Transport Layer Security (TLS) und Software Authentication and Security Layer (SASL):</span><span class="sxs-lookup"><span data-stu-id="91ee6-143">Notes on stream negotiation and the security methods Transport Layer Security (TLS) and Software Authentication and Security Layer (SASL):</span></span>
    
    <span data-ttu-id="91ee6-144">Die **XMPP Standards Foundation** (XSF) und die **Internet Engineering Task Force** (IETF) definieren einen Satz von Regeln und Standards für die Verwendung und Verwaltung von TLS-Clientzertifikaten, TLS-Serverzertifikaten und dem SASL-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="91ee6-144">The **XMPP Standards Foundation** (XSF) and the **Internet Engineering Task Force** (IETF) define a set of rules and standards for using and managing TLS client certificates, TLS server certificates, and the SASL mechanism.</span></span> <span data-ttu-id="91ee6-145">Die Verwendung von TLS und SASL ist der erforderliche Prozess zum Sichern des XMPP-Streams.</span><span class="sxs-lookup"><span data-stu-id="91ee6-145">Using TLS and SASL is the required process for securing the XMPP stream.</span></span> <span data-ttu-id="91ee6-146">Aus dem XMPP-Standarddokument **XEP-0178** gibt "einen empfohlenen Protokoll Fluss für die Verwendung des SASL-externen Mechanismus mit PKIX-Zertifikaten an, insbesondere dann, wenn ein XMPP-Dienst angibt, dass TLS obligatorisch-zu-Negotiate ist."</span><span class="sxs-lookup"><span data-stu-id="91ee6-146">From the XMPP Standards document **XEP-0178**, “specifies a recommended protocol flow for use of the SASL EXTERNAL mechanism with PKIX certificates, especially when an XMPP service indicates that TLS is mandatory-to-negotiate.”</span></span> <span data-ttu-id="91ee6-147">PKIX, wie in der XSF-Dokumentation angegeben, bezieht sich auf Infrastruktur öffentlicher Schlüssel, auch bekannt als PKI.</span><span class="sxs-lookup"><span data-stu-id="91ee6-147">PKIX, as stated in the XSF documentation, refers to public key infrastructure, also known as PKI.</span></span>
    
    <span data-ttu-id="91ee6-148">Weitere Informationen zu den XMPP-Anforderungen finden Sie im XSF-Dokument XEP-0178.</span><span class="sxs-lookup"><span data-stu-id="91ee6-148">Refer to the XSF document XEP-0178 for more details on the XMPP requirements.</span></span> <span data-ttu-id="91ee6-149">Einzelheiten hierzu finden Sie unter "XEP-0178: bewährte Methoden für die Verwendung von SASL External with Certificates".</span><span class="sxs-lookup"><span data-stu-id="91ee6-149">For details, refer to “XEP-0178: Best Practices for Use of SASL EXTERNAL with Certificates”.</span></span> <http://xmpp.org/extensions/xep-0178.html>
    
    <span data-ttu-id="91ee6-150">Weitere Informationen finden Sie im IETF-Dokument "Extensible Messaging and Presence Protocol (XMPP): Core", Abschnitt 5,0, STARTTLS-Aushandlung <https://tools.ietf.org/html/rfc6120> .</span><span class="sxs-lookup"><span data-stu-id="91ee6-150">Refer to the IETF document “Extensible Messaging and Presence Protocol (XMPP): Core“, Section 5.0, STARTTLS Negotiation <https://tools.ietf.org/html/rfc6120>.</span></span>
    
      - <span data-ttu-id="91ee6-151">**TLS-Aushandlung**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-151">**TLS Negotiation**.</span></span> <span data-ttu-id="91ee6-152">Definiert die TLS-Aushandlungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="91ee6-152">Defines the TLS negotiation rules.</span></span> <span data-ttu-id="91ee6-153">Ein XMPP-Dienst kann TLS erfordern, kann TLS optional machen, oder Sie definieren, dass TLS nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="91ee6-153">An XMPP service can require TLS, can make TLS optional, or you define that TLS is not supported.</span></span> <span data-ttu-id="91ee6-154">Wenn Sie optional auswählen, bleibt die Anforderung dem XMPP-Dienst für eine obligatorische Aushandlungs Entscheidung überlassen.</span><span class="sxs-lookup"><span data-stu-id="91ee6-154">Choosing Optional leaves the requirement up to the XMPP service for a mandatory-to-negotiate decision.</span></span> <span data-ttu-id="91ee6-155">Informationen zum Anzeigen aller möglichen Einstellungen und Details für SASL-, TLS-und Dialback-Aushandlung – einschließlich Ungültiger und bekannter Fehler Konfigurationen – finden Sie unter [Aushandlungs Einstellungen für XMPP-Verbundpartner in lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span><span class="sxs-lookup"><span data-stu-id="91ee6-155">To view all possible settings and details for SASL, TLS and Dialback negotiation –including not valid and known error configurations - see [Negotiation settings for XMPP federated partners in Lync Server 2013](lync-server-2013-negotiation-settings-for-xmpp-federated-partners.md).</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-156">**Erforderlich**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-156">**Required**.</span></span> <span data-ttu-id="91ee6-157">Der XMPP-Dienst erfordert TLS-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="91ee6-157">The XMPP service requires TLS negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-158">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-158">**Optional**.</span></span> <span data-ttu-id="91ee6-159">Der XMPP-Dienst gibt an, dass TLS obligatorisch-zu-Negotiate ist.</span><span class="sxs-lookup"><span data-stu-id="91ee6-159">The XMPP service indicates that TLS is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-160">**Nicht unterstützt**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-160">**Not Supported**.</span></span> <span data-ttu-id="91ee6-161">Der XMPP-Dienst unterstützt keine TLS-Funktion.</span><span class="sxs-lookup"><span data-stu-id="91ee6-161">The XMPP service does not support TLS.</span></span>
    
      - <span data-ttu-id="91ee6-162">**SASL-Aushandlung**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-162">**SASL negotiation**.</span></span> <span data-ttu-id="91ee6-163">Definiert die SASL-Aushandlungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="91ee6-163">Defines the SASL negotiation rules.</span></span> <span data-ttu-id="91ee6-164">Ein XMPP-Dienst kann SASL erfordern, kann SASL optional machen, oder Sie definieren, dass SASL nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="91ee6-164">An XMPP service can require SASL, can make SASL optional, or you define that SASL is not supported.</span></span> <span data-ttu-id="91ee6-165">Wenn Sie optional auswählen, bleibt die Anforderung dem Partner XMPP-Dienst für eine obligatorische-zu-Aushandlungs Entscheidung überlassen.</span><span class="sxs-lookup"><span data-stu-id="91ee6-165">Choosing Optional leaves the requirement up to the partner XMPP service for a mandatory-to-negotiate decision.</span></span>
        
        <div>
        

        > [!WARNING]  
        > <span data-ttu-id="91ee6-166">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="91ee6-166">SASL requires TLS.</span></span> <span data-ttu-id="91ee6-167">Um SASL verwenden zu können, muss TLS entweder erforderlich oder optional sein.</span><span class="sxs-lookup"><span data-stu-id="91ee6-167">To use SASL, TLS must either be required or optional.</span></span> <span data-ttu-id="91ee6-168">Jede Konfiguration, die SASL als erforderlich oder optional definiert, muss über TLS-Unterstützung verfügen.</span><span class="sxs-lookup"><span data-stu-id="91ee6-168">Any configuration that defines SASL as either required or optional must have TLS support.</span></span> <span data-ttu-id="91ee6-169">Wenn Sie auf <STRONG>Commit</STRONG> klicken, um Ihre Änderungen zu speichern, wenn Sie TLS nicht auf erforderlich oder optional festgesetzt haben, werden Sie gewarnt, dass SASL über TLS-Unterstützung verfügen muss und Ihre Änderungen nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="91ee6-169">When clicking <STRONG>Commit</STRONG> to save your changes, if you have not set TLS to required or optional, you will be warned that SASL must have TLS support and your changes are not saved.</span></span> <span data-ttu-id="91ee6-170">Um den Fehler zu beheben, legen Sie TLS auf <STRONG>erforderlich</STRONG> oder <STRONG>optional</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="91ee6-170">To resolve the error, set TLS to <STRONG>Required</STRONG> or <STRONG>Optional</STRONG>.</span></span> <span data-ttu-id="91ee6-171">Wenn die Verwendung von SASL optional ist und TLS-Aushandlungs Unterstützung nicht möglich ist, müssen Sie die SASL-Aushandlung auf <STRONG>nicht unterstützt</STRONG>setzen.</span><span class="sxs-lookup"><span data-stu-id="91ee6-171">If use of SASL is optional and TLS negotiation support is not possible, you must set SASL negotiation to <STRONG>Not Supported</STRONG>.</span></span> <span data-ttu-id="91ee6-172">Bestätigen Sie mit dem XMPP-Dienst, was die richtigen Aushandlungsdaten Ströme für TLS und SASL sein müssen, oder die Dienstunterbrechung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="91ee6-172">Confirm with the XMPP service what the proper negotiation streams must be for TLS and SASL or service interruption will occur.</span></span>

        
        </div>
        
          - <span></span>  
            <span data-ttu-id="91ee6-173">**Erforderlich**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-173">**Required**.</span></span> <span data-ttu-id="91ee6-174">Der XMPP-Dienst erfordert SASL-Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="91ee6-174">The XMPP service requires SASL negotiation.</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-175">**Optional**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-175">**Optional**.</span></span> <span data-ttu-id="91ee6-176">Der XMPP-Dienst gibt an, dass SASL obligatorisch-zu-Negotiate ist.</span><span class="sxs-lookup"><span data-stu-id="91ee6-176">The XMPP service indicates that SASL is mandatory-to-negotiate.</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-177">**Nicht unterstützt**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-177">**Not Supported**.</span></span> <span data-ttu-id="91ee6-178">SASL wird vom XMPP-Dienst nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91ee6-178">The XMPP service does not support SASL.</span></span>
    
      - <span data-ttu-id="91ee6-179">**Dialback-Aushandlung**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-179">**Dialback negotiation**.</span></span> <span data-ttu-id="91ee6-180">Dialback-Aushandlung wird vom XSF im Dokument **XEP-220: Server Dialback** definiert <http://xmpp.org/extensions/xep-0220.html> .</span><span class="sxs-lookup"><span data-stu-id="91ee6-180">Dialback negotiation is defined by the XSF in document **XEP-220 : Server Dialback** <http://xmpp.org/extensions/xep-0220.html>.</span></span> <span data-ttu-id="91ee6-181">Der Server Dialback-Prozess verwendet das Domain Name System (DNS) und einen autorisierenden Server, um zu überprüfen, ob die Anforderung von einem gültigen XMPP-Partner kam.</span><span class="sxs-lookup"><span data-stu-id="91ee6-181">The server dialback process uses the domain name system (DNS) and an authoritative server to verify that the request came from a valid XMPP partner.</span></span> <span data-ttu-id="91ee6-182">Zu diesem Zweck erstellt der ursprüngliche Server eine Nachricht eines bestimmten Typs mit einem generierten Dialback-Schlüssel und schlägt den empfangenden Server in DNS nach.</span><span class="sxs-lookup"><span data-stu-id="91ee6-182">To do this, the originating server creates a message of a specific type with a generated dialback key and looks up the receiving server in DNS.</span></span> <span data-ttu-id="91ee6-183">Der ursprüngliche Server sendet den Schlüssel in einem XML-Datenstrom an den resultierenden DNS-Lookup, vermutlich den empfangenden Server.</span><span class="sxs-lookup"><span data-stu-id="91ee6-183">The originating server sends the key in an XML stream to the resulting DNS lookup, presumably the receiving server.</span></span> <span data-ttu-id="91ee6-184">Nach Erhalt des Schlüssels über den XML-Datenstrom antwortet der empfangende Server nicht auf den ursprünglichen Server, sondern sendet den Schlüssel an einen bekannten autorisierenden Server.</span><span class="sxs-lookup"><span data-stu-id="91ee6-184">On receipt of the key over the XML stream, the receiving server does not respond to the originating server, but sends the key to a known authoritative server.</span></span> <span data-ttu-id="91ee6-185">Der autorisierende Server überprüft, ob der Schlüssel entweder gültig oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="91ee6-185">The authoritative server verifies that the key is either valid or not valid.</span></span> <span data-ttu-id="91ee6-186">Wenn dies nicht der Fall ist, antwortet der empfangende Server nicht auf den ursprünglichen Server.</span><span class="sxs-lookup"><span data-stu-id="91ee6-186">If not valid, the receiving server does not respond to the originating server.</span></span> <span data-ttu-id="91ee6-187">Wenn der Schlüssel gültig ist, informiert der empfangende Server den Ursprungsserver, dass Identität und Schlüssel gültig sind und die Konversation beginnen kann.</span><span class="sxs-lookup"><span data-stu-id="91ee6-187">If the key is valid, the receiving server informs the originating server that the identity and key is valid and the conversation can commence.</span></span>
        
        <span data-ttu-id="91ee6-188">Es gibt zwei gültige Zustände für **Dialback-Aushandlung**:</span><span class="sxs-lookup"><span data-stu-id="91ee6-188">There are two valid states for **Dialback negotiation**:</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-189">**True**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-189">**True**.</span></span> <span data-ttu-id="91ee6-190">Der XMPP-Server ist für die Verwendung von Dialback-Aushandlung konfiguriert, wenn eine Anforderung von einem Ursprungsserver empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="91ee6-190">The XMPP server is configured to use Dialback negotiation if a request should be received from an originating server</span></span>
        
          - <span></span>  
            <span data-ttu-id="91ee6-191">**False**.</span><span class="sxs-lookup"><span data-stu-id="91ee6-191">**False**.</span></span> <span data-ttu-id="91ee6-192">Der XMPP-Server ist nicht für die Verwendung von Dialback-Aushandlung konfiguriert, und wenn eine Anforderung von einem Ursprungsserver empfangen werden soll, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91ee6-192">The XMPP server is not configured to use Dialback negotiation and if a request should be received from an originating server, it will be ignored</span></span>

<span data-ttu-id="91ee6-193"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91ee6-193"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

