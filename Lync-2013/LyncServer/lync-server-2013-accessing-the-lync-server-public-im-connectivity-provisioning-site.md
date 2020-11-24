---
title: Zugreifen auf die Lync Server-Bereitstellungswebsite für Verbindungen mit öffentlichen Chatdiensten
description: Zugreifen auf die Bereitstellungswebsite der lync Server-Bereitstellung für öffentliche Chats.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Accessing the Lync Server public IM connectivity provisioning site
ms:assetid: 77a08234-6bcf-4f59-b43b-ee5fc1926585
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440174(v=OCS.15)
ms:contentKeyID: 57793364
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e12916b12de1ef3a3f990c6bee54c312ba6c1992
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393894"
---
# <a name="accessing-the-lync-server-public-im-connectivity-provisioning-site-from-lync-server-2013"></a><span data-ttu-id="e11e3-103">Zugreifen auf die Lync Server-Bereitstellungswebsite für Verbindungen mit öffentlichen Chatdiensten von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e11e3-103">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e11e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e11e3-104">

<span> </span></span></span>

<span data-ttu-id="e11e3-105">_**Letztes Änderungsdatum des Themas:** 2019-03-22_</span><span class="sxs-lookup"><span data-stu-id="e11e3-105">_**Topic Last Modified:** 2019-03-22_</span></span>

<span data-ttu-id="e11e3-106">Der Bereitstellungsprozess für Lync-Skype Konnektivität hat sich im Vergleich zur vorherigen PIC-Bereitstellungsmethode geändert.</span><span class="sxs-lookup"><span data-stu-id="e11e3-106">The provisioning process for Lync-Skype connectivity has changed, as compared to previous PIC provisioning methods.</span></span> <span data-ttu-id="e11e3-107">Dieser Bereitstellungsprozess kann bis zu dreißig Tage dauern.</span><span class="sxs-lookup"><span data-stu-id="e11e3-107">This provisioning process can take up to thirty days to complete.</span></span> <span data-ttu-id="e11e3-108">Wir empfehlen, diesen Prozess zuerst zu starten und dann die verbleibenden Schritte in diesem Dokument auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-108">We recommend that you start this process first, prior to completing the remaining steps in this document.</span></span> <span data-ttu-id="e11e3-109">Nachdem der Lync-Skype Bereitstellungsprozess für Ihr Konto abgeschlossen ist, wird das Konto aktiviert, und ihre berechtigten Benutzer sind für öffentliche Chat Verbindungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e11e3-109">After the Lync-Skype provisioning process is completed for your account, the account is activated and your eligible users are enabled for public IM connectivity.</span></span>

### <a name="to-provision-lync-skype-connectivity-you-need-the-following-information"></a><span data-ttu-id="e11e3-110">Zur Bereitstellung Lync-Skype Konnektivität benötigen Sie die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="e11e3-110">To provision Lync-Skype connectivity, you need the following information:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="e11e3-111">Die Microsoft-Vertragsnummer</span><span class="sxs-lookup"><span data-stu-id="e11e3-111">Microsoft Agreement Number</span></span></p></li>
<li><p><span data-ttu-id="e11e3-112">Den vollqualifizierten Domänenname (Fully Qualified Domain Name, FQDN) des Zugriffs-Edgediensts</span><span class="sxs-lookup"><span data-stu-id="e11e3-112">Access Edge service fully qualified domain name (FQDN)</span></span></p></li>
<li><p><span data-ttu-id="e11e3-113">SIP-Domäne/n (Session Initiation Protocol)</span><span class="sxs-lookup"><span data-stu-id="e11e3-113">Session Initiation Protocol (SIP) domain(s)</span></span></p></li>
<li><p><span data-ttu-id="e11e3-114">FQDNs für alle zusätzlichen Zugriffs-Edgedienste</span><span class="sxs-lookup"><span data-stu-id="e11e3-114">Any additional Access Edge service FQDNs</span></span></p></li>
<li><p><span data-ttu-id="e11e3-115">Kontaktinformationen</span><span class="sxs-lookup"><span data-stu-id="e11e3-115">Contact information</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e11e3-116">Ab April 2019 werden wir die Erfassung und Speicherung von Kontaktinformationen für Kunden, die über die PIC.lync.com-Website für Skype Federation bereitgestellt werden, beenden.</span><span class="sxs-lookup"><span data-stu-id="e11e3-116">Beginning in April 2019, we will stop the collection and retention of contact information for customers who are provisioned for Skype Federation via the pic.lync.com website.</span></span> <span data-ttu-id="e11e3-117">Diese Änderung wird vorgenommen, um sicherzustellen, dass das PIC.lync.com-Bereitstellungssystem den Microsoft-Datenschutzrichtlinien entspricht.</span><span class="sxs-lookup"><span data-stu-id="e11e3-117">This change is being made to ensure that the pic.lync.com provisioning system adheres to Microsoft privacy policies.</span></span> 

<span data-ttu-id="e11e3-118">Sobald diese Änderung in Echtzeit erfolgt, können wir keine e-Mail-Updates mehr für ausstehende Bereitstellungsänderungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-118">Once this change goes live, we will no longer be able to provide email updates on pending provisioning changes.</span></span> <span data-ttu-id="e11e3-119">PIC-Bereitstellungsänderungen werden in der Regel innerhalb von 24-48 Stunden nach der Eingabe abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-119">PIC provisioning changes typically complete within 24-48 hours after being entered.</span></span> <span data-ttu-id="e11e3-120">Wenn Sie nach dem Einreichen einer Bereitstellungsanfrage nach wie vor Skype Federation Issues (48) erleben, wenden Sie sich bitte an den technischen Support von Microsoft, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e11e3-120">If you are still experiencing Skype Federation issues 48 hours after submitting a provisioning request, please engage Microsoft Technical Support to investigate further.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e11e3-121">Im Rahmen dieser Änderung werden alle zuvor eingegebenen Kontaktinformationen bis Ende April 2019 aus unserem System gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e11e3-121">As part of this change, all previously entered contact information will be purged from our system by the end of April, 2019.</span></span>

### <a name="to-initiate-the-provisioning-process-for-lync-skype-connectivity"></a><span data-ttu-id="e11e3-122">So initiieren Sie den Bereitstellungsprozess für Lync-Skype Konnektivität:</span><span class="sxs-lookup"><span data-stu-id="e11e3-122">To initiate the provisioning process for Lync-Skype connectivity:</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><ol>
<li><p><span data-ttu-id="e11e3-123">Registrieren Sie sich mit <strong>https://pic.lync.com</strong> Ihrer Microsoft Windows Live ID bei der Website.</span><span class="sxs-lookup"><span data-stu-id="e11e3-123">Sign in to the website, <strong>https://pic.lync.com</strong>, using your Microsoft Windows Live ID.</span></span></p></li>
<li><p><span data-ttu-id="e11e3-124">Wählen Sie den Typ Ihres Microsoft-Lizenzvertrags aus.</span><span class="sxs-lookup"><span data-stu-id="e11e3-124">Select the Microsoft licensing agreement type.</span></span></p></li>
<li><p><span data-ttu-id="e11e3-125">Aktivieren Sie das Kontrollkästchen, um sicherzustellen, dass Sie die Produkt Nutzungsrechte für lync Server gelesen und akzeptiert haben.</span><span class="sxs-lookup"><span data-stu-id="e11e3-125">Select the check box, verifying that you have read and accept the Product Use Rights for Lync Server.</span></span></p></li>
<li><p><span data-ttu-id="e11e3-126">Klicken Sie auf der Seite <strong>Bereitstellungsanforderung initiieren</strong> auf den entsprechenden Link, um eine Bereitstellungsanforderung zu initiieren:</span><span class="sxs-lookup"><span data-stu-id="e11e3-126">On the <strong>Initiate a Provisioning Request</strong> page, click the appropriate link to initiate a provisioning request:</span></span></p></li>
<li><p><span data-ttu-id="e11e3-127">Geben Sie auf der Seite <strong>Bereitstellungsinformationen angeben</strong> den <strong>FQDN des Access-Edgedienst</strong>ein.</span><span class="sxs-lookup"><span data-stu-id="e11e3-127">On the <strong>Specify Provisioning Information</strong> page, enter the <strong>Access Edge service FQDN</strong>.</span></span> <span data-ttu-id="e11e3-128">Beispiel: <strong>SIP.contoso.com</strong>.</span><span class="sxs-lookup"><span data-stu-id="e11e3-128">For example, <strong>sip.contoso.com</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="e11e3-129">Nach dem 1. Juli 2017 Microsoft zusätzlich für Kunden den Verbund-DNS-SRV-Eintrag bereitgestellt, der für die Verbindung mit öffentlichen Chat Diensten bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e11e3-129">After July 1st, 2017 Microsoft will additionally require customers have the Federation DNS SRV record deployed for Public IM connectivity to continue to work.</span></span>

</li>
<li><p><span data-ttu-id="e11e3-130">Geben Sie mindestens einen SIP-Domänennamen ein, und klicken Sie dann auf <strong>Hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="e11e3-130">Enter at least one or more SIP domain names, and then click <strong>Add</strong>.</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="e11e3-131">Mindestens ein Access Edge-Server und eine SIP-Domäne sind erforderlich, um den Bereitstellungsprozess abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-131">At least one Access Edge server and one SIP domain are required to complete the provisioning process.</span></span> <span data-ttu-id="e11e3-132">SIP-Domäne und Zugriffs-Edge-Server müssen aktiv, betriebsbereit und im Netzwerk erreichbar sein.</span><span class="sxs-lookup"><span data-stu-id="e11e3-132">The SIP domain and the Access Edge server must be active, functioning, and reachable on the network.</span></span>

</li>
<li><p><span data-ttu-id="e11e3-133">Wählen Sie in der Liste der <strong>öffentlichen Chatdienst Anbieter</strong> <strong>Skype aus,</strong> und klicken Sie auf <strong>weiter</strong> , um Kontaktinformationen hinzuzufügen, und übermitteln Sie die Bereitstellungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="e11e3-133">In the list of <strong>Public IM Service providers</strong>, select <strong>Skype,</strong> and click <strong>Next</strong> to add contact information, and submit the provisioning request.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e11e3-134">Nachdem die Bereitstellungsanforderung übermittelt wurde, kann es bis zu 30 Tage dauern, bis das Konto aktiviert ist und die Benutzer für die öffentliche Chat Verbindung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e11e3-134">After the provisioning request has been submitted, it can take up to 30 days for the account to activate and for users to be enabled for public IM connectivity.</span></span>

<div>

## <a name="enabling-federation-and-public-im-connectivity-pic"></a><span data-ttu-id="e11e3-135">Aktivieren von Partnerverbünden und Verbindungen mit öffentlichen Chatdiensten (PIC)</span><span class="sxs-lookup"><span data-stu-id="e11e3-135">Enabling Federation and Public IM Connectivity (PIC)</span></span>

<span data-ttu-id="e11e3-136">Nachdem Sie die Bereitstellungsanforderung übermittelt haben, können Sie sich auf die lync Server-Umgebung und die administrativen Aufgaben konzentrieren, die zum Konfigurieren der Lync-Skype Konnektivität erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e11e3-136">After you have submitted the provisioning request, you can focus on the Lync Server environment and administrative tasks required to configure Lync-Skype connectivity.</span></span> <span data-ttu-id="e11e3-137">In diesem Abschnitt wird davon ausgegangen, dass der lync Server-Administrator lync Server bereitgestellt und den externen Zugriff konfiguriert hat.</span><span class="sxs-lookup"><span data-stu-id="e11e3-137">In this section, we assume that the Lync Server administrator has deployed Lync Server and configured external access.</span></span> <span data-ttu-id="e11e3-138">Weitere Informationen zum Konfigurieren von externem Zugriff für lync Server finden Sie unter "Planen des Zugriffs für externe Benutzer" unter [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) und "Bereitstellen des Zugriffs auf externe Benutzer" unter [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378) .</span><span class="sxs-lookup"><span data-stu-id="e11e3-138">For additional information on configuring external access for Lync Server, see "Planning for External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=273772](https://go.microsoft.com/fwlink/p/?linkid=273772) and "Deploying External User Access" at [https://go.microsoft.com/fwlink/p/?LinkID=27378](https://go.microsoft.com/fwlink/p/?linkid=27378).</span></span>

<span data-ttu-id="e11e3-139">Um die lync Server-Umgebung für Lync-Skype Konnektivität vorzubereiten, muss der lync Server-Administrator die folgenden drei Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="e11e3-139">To prepare the Lync Server environment for Lync-Skype connectivity, the Lync Server administrator must complete the following three tasks:</span></span>

<div>

## <a name="1-configure-federation-and-pic"></a><span data-ttu-id="e11e3-140">1 \.</span><span class="sxs-lookup"><span data-stu-id="e11e3-140">1\.</span></span> <span data-ttu-id="e11e3-141">Konfigurieren des Partnerverbunds und der PIC</span><span class="sxs-lookup"><span data-stu-id="e11e3-141">Configure Federation and PIC</span></span>

<span data-ttu-id="e11e3-142">Föderation ist erforderlich, um Skype-Benutzern die Kommunikation mit lync-Benutzern in Ihrer Organisation zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-142">Federation is required to enable Skype users to communicate with Lync users in your organization.</span></span> <span data-ttu-id="e11e3-143">PIC (Public Instant Messaging Connectivity) ist eine Klasse des Verbandes und muss so konfiguriert sein, dass Ihre lync-Nutzer mit Skype-Nutzern kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="e11e3-143">Public Instant Messaging Connectivity (PIC) is a class of federation, and it must be configured to enable your Lync users to communicate with Skype users.</span></span> <span data-ttu-id="e11e3-144">Föderation und PIC werden mithilfe der lync Server-Systemsteuerung konfiguriert (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="e11e3-144">Federation and PIC are configured by using the Lync Server Control Panel, shown below.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="e11e3-145">Der PIC-Partnerverbund wird von Live Communication Server 2005 SP1 oder Office Communications Server 2007 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e11e3-145">PIC federation is no longer supported by Live Communication Server 2005 SP1 or by Office Communications Server 2007.</span></span> <span data-ttu-id="e11e3-146">Zu den unterstützten Plattformen für die PIC-Föderation gehören lync Server 2013, lync Server 2010 und Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="e11e3-146">The supported platforms for PIC federation include Lync Server 2013, Lync Server 2010, and Office Communications Server 2007 R2.</span></span>



</div>

</div>

<div>

## <a name="2-configure-at-least-one-policy-to-support-federated-user-access"></a><span data-ttu-id="e11e3-147">2 \.</span><span class="sxs-lookup"><span data-stu-id="e11e3-147">2\.</span></span> <span data-ttu-id="e11e3-148">Konfigurieren von mindestens einer Richtlinie zur Unterstützung des Benutzerzugriffs im Partnerverbund</span><span class="sxs-lookup"><span data-stu-id="e11e3-148">Configure at least one policy to support federated user access</span></span>

<span data-ttu-id="e11e3-149">Mithilfe der lync Server-Systemsteuerung muss ein Administrator mindestens eine Richtlinie für den externen Benutzer Zugriff konfigurieren, um zu steuern, ob Skype-Benutzer mit internen lync Server-Benutzern zusammenarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="e11e3-149">Using the Lync Server Control Panel, an administrator must configure one or more external user access policies to control whether Skype users can collaborate with internal Lync Server users.</span></span>

</div>

<div>

## <a name="3-configure-the-skype-pic-provider-setting-for-lync"></a><span data-ttu-id="e11e3-150">3 \.</span><span class="sxs-lookup"><span data-stu-id="e11e3-150">3\.</span></span> <span data-ttu-id="e11e3-151">Konfigurieren der Skype PIC-Anbieter Einstellung für lync</span><span class="sxs-lookup"><span data-stu-id="e11e3-151">Configure the Skype PIC provider setting for Lync</span></span>

<span data-ttu-id="e11e3-152">Mithilfe der lync Server-Verwaltungsshell muss ein Administrator die lync-Clientrichtlinie so konfigurieren, dass Skype als zusätzlicher PIC-Anbieter angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e11e3-152">Using the Lync Server Management Shell, an administrator must configure the Lync client policy to display Skype as an additional PIC provider.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="e11e3-153">Benutzer von PIC-Dienstanbietern können erst dann an Chatunterhaltungen oder Konferenzen in Ihrer Organisation teilnehmen, wenn Sie zudem mindestens eine Richtlinie (Schritt 2 an früherer Stelle in diesem Verfahren) zur Unterstützung der Verbindung mit öffentlichen Chatanbietern konfiguriert haben. </span><span class="sxs-lookup"><span data-stu-id="e11e3-153">Users of the Public Instant Messaging Connectivity (PIC) service providers can’t participate in IM or conferences in your organization until you also configure at least one policy (step 2, earlier in this procedure) to support public IM connectivity.</span></span><BR><span data-ttu-id="e11e3-154">Informationen zum Konfigurieren von Verbund und PIC finden Sie unter "aktivieren oder Deaktivieren von Verbund-und öffentlichen Chat Verbindungen" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A> .</span><span class="sxs-lookup"><span data-stu-id="e11e3-154">To configure federation and PIC, see "Enable or Disable Federation and Public IM Connectivity" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306063">https://go.microsoft.com/fwlink/p/?LinkId=306063</A>.</span></span><BR><span data-ttu-id="e11e3-155">Informationen zum Konfigurieren von mindestens einer Richtlinie zur Unterstützung des Zugriffs von Verbundbenutzern finden Sie unter "Konfigurieren von Richtlinien zum Steuern des Zugriffs öffentlicher Benutzer" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A> .</span><span class="sxs-lookup"><span data-stu-id="e11e3-155">To configure at least one policy to support federated user access, see "Configure Policies to Control Public User Access" at <A href="https://go.microsoft.com/fwlink/p/?linkid=306064">https://go.microsoft.com/fwlink/p/?LinkId=306064</A>.</span></span>



</div>

1.  <span data-ttu-id="e11e3-156">Öffnen Sie auf einem lync Server-Front-End-Server die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="e11e3-156">From a Lync Server Front End Server, open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="e11e3-157">Führen Sie die folgenden beiden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="e11e3-157">Run the following two commands:</span></span>
    
      - `Remove-CsPublicProvider -Identity <identity-name>`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="e11e3-158">Wenn Sie nicht bereits über einen PIC-Anbieter in Ihrer Umgebung verfügen und einen neuen PIC-Anbieter erstellen, müssen Sie das Cmdlet <STRONG>Remove-CsPublicProvider</STRONG> nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-158">If you do not already have a PIC provider in your environment and are creating a new PIC provider then you do not need to run the <STRONG>Remove-CsPublicProvider</STRONG> cmdlet.</span></span>

        
        </div>
    
      - `New-CsPublicProvider -ProxyFqdn federation.messenger.msn.com -Enabled 1 -Identity Skype  -VerificationLevel 2 -NameDecorationRoutingDomain msn.com -NameDecorationExcludedDomainList "msn.com,outlook.com,live.com,hotmail.com" -IconUrl "https://images.edge.messenger.live.com/Messenger_16x16.png"`
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="e11e3-159">In lync Server 2013 CU5 &amp; lync-Desktop Client in Office 2013 SP1 wurde die Situation verbessert, in der lync-Benutzer Skype-Kontakte hinzufügen, um nicht-Microsoft-Domänen zu "schmücken", um Sie zu identifizieren und an Skype weiterzuleiten (das Format von: User (contoso. com) @MSN. com).</span><span class="sxs-lookup"><span data-stu-id="e11e3-159">Added in Lync Server 2013 CU5 &amp; Lync desktop client in Office 2013 SP1, the NameDecorationRoutingDomain and NameDecorationExcludedDomainList improve the situation where Lync users adding Skype contacts needed to “decorate” non-Microsoft domains to identify and route them to Skype (the format of: user(contoso.com)@msn.com).</span></span> <span data-ttu-id="e11e3-160">Diese neuen Einstellungen ermöglichen die automatische Formatierung der im Dialogfeld „Skype-Kontakt hinzufügen“ eingegebenen Benutzeradresse mit dem Parameter „NameDecorationRoutingDomain“ (der auf „msn.com“ festgelegt sein sollte), wenn die Domänen nicht im Parameter „NameDecorationExcludedDomainList“ enthalten sind (zurzeit werden „msn.com“, „live.com“, „Hotmail.com“ und „outlook.com“ unterstützt).</span><span class="sxs-lookup"><span data-stu-id="e11e3-160">These new settings will allow automatic formatting of the address user’s enter in the “Add Skype contact” dialog box with the NameDecorationRoutingDomain (which should be set to msn.com) if it does not contain the domains in the NameDecorationExcludedDomainList (we currently can support msn.com, live.com, Hotmail.com, outlook.com).</span></span>

        
        </div>

3.  <span data-ttu-id="e11e3-161">Von einem lync-Client aus können Sie nun Skype als PIC-Anbieter auswählen und einen Skype-Client hinzufügen, indem Sie sein Microsoft-Konto angeben.</span><span class="sxs-lookup"><span data-stu-id="e11e3-161">From a Lync client, you can now select Skype as the PIC provider, and add a Skype client by specifying their Microsoft account.</span></span> <span data-ttu-id="e11e3-162">Darüber hinaus kann ein Skype-Nutzer, der sich mit seinem Microsoft-Konto zusammengeführt und angemeldet hat, Kontaktanfragen an lync-Nutzer senden.</span><span class="sxs-lookup"><span data-stu-id="e11e3-162">In addition, a Skype user who has merged and logged in with their Microsoft account can send contact request to Lync users.</span></span> <span data-ttu-id="e11e3-163">Weitere Informationen zu Microsoft-Konten finden Sie unter [Was ist ein Microsoft-Konto?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span><span class="sxs-lookup"><span data-stu-id="e11e3-163">For more information about Microsoft accounts, see [What is a Microsoft account?](https://support.skype.com/en/faq/fa12059/what-is-a-microsoft-account).</span></span> <span data-ttu-id="e11e3-164">Weitere Informationen zum Hinzufügen von Clients zu lync finden Sie unter [Verwenden von Lync-Skype Konnektivität in lync Server 2013 als Endbenutzer](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span><span class="sxs-lookup"><span data-stu-id="e11e3-164">For additional information on adding clients to Lync, see [Using Lync-Skype connectivity in Lync Server 2013 as an end user](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md).</span></span>

4.  <span data-ttu-id="e11e3-165">Detaillierte Informationen zum Ändern von gehosteten Anbietern finden Sie unter "erstellen oder Bearbeiten von gehosteten SIP-Verbund Anbietern" unter [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065) .</span><span class="sxs-lookup"><span data-stu-id="e11e3-165">For detailed information on modifying hosted providers, see "Create or Edit Hosted SIP Federated Providers" at [https://go.microsoft.com/fwlink/p/?LinkId=306065](https://go.microsoft.com/fwlink/p/?linkid=306065).</span></span>

<span data-ttu-id="e11e3-166">Damit sind die Verwaltungsaufgaben abgeschlossen, die auf dem Server durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e11e3-166">This completes the administrative tasks that must be performed on the server.</span></span> <span data-ttu-id="e11e3-167">Sie sind jetzt für Lync-Skype Konnektivität eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e11e3-167">You are now set up for Lync-Skype connectivity.</span></span>

</div>

</div>

<div>

## <a name="additional-resources"></a><span data-ttu-id="e11e3-168">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e11e3-168">Additional Resources</span></span>

[<span data-ttu-id="e11e3-169">Verwenden von Lync-Skype-Konnektivität als Endbenutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e11e3-169">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

[<span data-ttu-id="e11e3-170">Leitfaden für die Bereitstellung der Lync-Skype-Konnektivität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e11e3-170">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

<span data-ttu-id="e11e3-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e11e3-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

