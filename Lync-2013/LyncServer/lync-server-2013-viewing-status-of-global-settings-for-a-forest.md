---
title: 'Lync Server 2013: Anzeigen des Status globaler Einstellungen für eine Gesamtstruktur'
description: 'Lync Server 2013: Anzeige des Status globaler Einstellungen für eine Gesamtstruktur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View status of global settings for a forest
ms:assetid: 2ab0f2f1-9908-4e6f-aff3-d6b3cc474b6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn747889(v=OCS.15)
ms:contentKeyID: 63969590
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9f722ea66f6c54c816703bd1af1d3def57bbd84
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443909"
---
# <a name="view-status-of-global-settings-for-a-forest-in-lync-server-2013"></a><span data-ttu-id="d95fa-103">Anzeigen des Status globaler Einstellungen für eine Gesamtstruktur in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d95fa-103">View status of global settings for a forest in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d95fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d95fa-104">

<span> </span></span></span>

<span data-ttu-id="d95fa-105">_**Letztes Änderungsdatum des Themas:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="d95fa-105">_**Topic Last Modified:** 2014-05-20_</span></span>

<span data-ttu-id="d95fa-106">Administratoren sollten die globalen Einstellungen für eine lync Server 2013-Bereitstellung monatlich überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-106">Administrators should review the global settings for a Lync Server 2013 deployment monthly.</span></span> <span data-ttu-id="d95fa-107">Das Ziel besteht darin, die implementierten Einstellungen für eine Reihe bekannter Konfigurationen zu überprüfen – eine Baseline-Konfiguration, um sicherzustellen, dass die Einstellungen gültig sind, und um festzustellen, ob die Baseline-Dokumentation aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d95fa-107">The objective would be to review implemented settings against a set of known configurations—a baseline configuration to help guarantee that settings are valid and to determine whether the baseline documentation should be updated.</span></span> <span data-ttu-id="d95fa-108">Änderungen an der globalen Einstellung sollten über einen Änderungskontrollprozess implementiert werden, der die Dokumentation der neuen Einstellungen umfasst.</span><span class="sxs-lookup"><span data-stu-id="d95fa-108">Changes to global setting should be implemented through a Change Control process which should include documenting the new settings.</span></span>

<span data-ttu-id="d95fa-109">Die globalen Einstellungen, die überprüft werden sollten, werden in den folgenden Abschnitten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="d95fa-109">Global settings that should be reviewed are described in the following sections:</span></span>

<div>

## <a name="check-general-settings"></a><span data-ttu-id="d95fa-110">Allgemeine Einstellungen überprüfen</span><span class="sxs-lookup"><span data-stu-id="d95fa-110">Check general settings</span></span>

<span data-ttu-id="d95fa-111">Überprüfen Sie die allgemeinen Einstellungen, einschließlich der unterstützten SIP-Domänen (Session Initiation Protocol) für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d95fa-111">Check general settings, including the supported Session Initiation Protocol (SIP) domains for Lync Server 2013.</span></span>

<span data-ttu-id="d95fa-112">SIP-Domäneninformationen können mithilfe von Windows PowerShell und dem Cmdlet **Get-CsSipDomain** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-112">SIP domain information can be returned by using Windows PowerShell and the **Get-CsSipDomain** cmdlet.</span></span> <span data-ttu-id="d95fa-113">Wenn Sie diese Informationen zurückgeben möchten, führen Sie den `Get-CsSipDomain` Windows PowerShell-Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="d95fa-113">To return this information, run the `Get-CsSipDomain` Windows PowerShell command.</span></span>

<span data-ttu-id="d95fa-114">Get-CsSipDomain gibt ähnliche Informationen für alle autorisierten SIP-Domänen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-114">Get-CsSipDomain will return information similar to this for all the authorized SIP domains:</span></span>

<span data-ttu-id="d95fa-115">Identitäts Name IsDefault</span><span class="sxs-lookup"><span data-stu-id="d95fa-115">Identity Name IsDefault</span></span>

<span data-ttu-id="d95fa-116">\-------- ---- ---------</span><span class="sxs-lookup"><span data-stu-id="d95fa-116">\-------- ---- ---------</span></span>

<span data-ttu-id="d95fa-117">fabrikam.com fabrikam.com true</span><span class="sxs-lookup"><span data-stu-id="d95fa-117">fabrikam.com fabrikam.com True</span></span>

<span data-ttu-id="d95fa-118">na.fabrikam.com na.fabrikam.com false</span><span class="sxs-lookup"><span data-stu-id="d95fa-118">na.fabrikam.com na.fabrikam.com False</span></span>

<span data-ttu-id="d95fa-119">Wenn die IsDefault-Eigenschaft auf true festgelegt ist, ist die entsprechende Domäne Ihre standardmäßige SIP-Domäne.</span><span class="sxs-lookup"><span data-stu-id="d95fa-119">If the IsDefault property is set to True, the corresponding domain is your default SIP domain.</span></span> <span data-ttu-id="d95fa-120">Sie können das Set-CsSipDomain-Cmdlet verwenden, um die SIP-Standarddomäne für Ihre Organisation zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d95fa-120">You can use the Set-CsSipDomain cmdlet to change the default SIP domain for your organization.</span></span> <span data-ttu-id="d95fa-121">Sie können die standardmäßige SIP-Domäne jedoch nicht einfach löschen, da Sie ohne eine Standarddomäne verbleibt.</span><span class="sxs-lookup"><span data-stu-id="d95fa-121">However, you can't just delete the default SIP domain because that would leave you without a default domain.</span></span> <span data-ttu-id="d95fa-122">Wenn Sie die fabrikam.com-Domäne löschen möchten (wie im vorherigen Beispiel gezeigt), müssen Sie na.fabrikam.com zunächst so konfigurieren, dass es sich um Ihre Standarddomäne handelt.</span><span class="sxs-lookup"><span data-stu-id="d95fa-122">If you wanted to delete the fabrikam.com domain (as shown in the previous example), you would first have to configure na.fabrikam.com to be your default domain.</span></span>

</div>

<div>

## <a name="check-meeting-settings"></a><span data-ttu-id="d95fa-123">Überprüfen von Besprechungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-123">Check meeting settings</span></span>

<span data-ttu-id="d95fa-124">Zu den Besprechungseinstellungen gehören Richtlinien Definitionen für Besprechungen und die Unterstützung für die Teilnahme anonymer Benutzer an Besprechungen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-124">Meeting settings include meeting policy definitions and support for participation of anonymous users in meetings.</span></span>

<span data-ttu-id="d95fa-125">Die Einstellungen für die besprechungskonfiguration können mithilfe von Windows PowerShell und dem Cmdlet **Get-CsMeetingConfiguration** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-125">Meeting configuration settings can be retrieved by using Windows PowerShell and the **Get-CsMeetingConfiguration** cmdlet.</span></span> <span data-ttu-id="d95fa-126">Dieser Befehl gibt beispielsweise Informationen zu den Konfigurationseinstellungen für globale Besprechungen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-126">For example, this command returns information about the global meeting configuration settings:</span></span>

<span data-ttu-id="d95fa-127">Get-CsMeetingConfiguration – Identität "globale" Besprechungs Konfigurationseinstellungen können auch im Website Bereich konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-127">Get-CsMeetingConfiguration –Identity "Global"Meeting configuration settings can also be configured at the site scope.</span></span> <span data-ttu-id="d95fa-128">Aus diesem Grund sollten Sie den folgenden Befehl verwenden, der Informationen zu allen Besprechungs Konfigurationseinstellungen zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-128">Because of that, you might want to use the following command, which returns information about all the meeting configuration settings:</span></span>

`Get-CsMeetingConfiguration`

<span data-ttu-id="d95fa-129">Das Cmdlet " **Get-CsMeetingConfiguration** " gibt Informationen ähnlich der folgenden zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-129">The **Get-CsMeetingConfiguration** cmdlet returns information similar to the following:</span></span>

<span data-ttu-id="d95fa-130">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-130">Identity : Global</span></span>

<span data-ttu-id="d95fa-131">PstnCallersBypassLobby: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-131">PstnCallersBypassLobby : True</span></span>

<span data-ttu-id="d95fa-132">EnableAssignedConferenceType: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-132">EnableAssignedConferenceType : True</span></span>

<span data-ttu-id="d95fa-133">DesignateAsPresenter: Unternehmen</span><span class="sxs-lookup"><span data-stu-id="d95fa-133">DesignateAsPresenter : Company</span></span>

<span data-ttu-id="d95fa-134">AssignedConferenceTypeByDefault: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-134">AssignedConferenceTypeByDefault : True</span></span>

<span data-ttu-id="d95fa-135">AdmitAnonymousUsersByDefault: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-135">AdmitAnonymousUsersByDefault : True</span></span>

<span data-ttu-id="d95fa-136">Das letzte Element in der Liste, **AdmitAnonymousUsersByDefault**, aktiviert oder deaktiviert die Möglichkeit von anonymen Benutzern, an Besprechungen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-136">Again, the final item in the list, **AdmitAnonymousUsersByDefault**, enables or disables the ability of anonymous users to participate in meetings.</span></span>

<span data-ttu-id="d95fa-137">Wenn Sie die Einstellungen für die besprechungskonfiguration überprüfen, finden Sie es möglicherweise hilfreich, die aktuellen Einstellungen mit den Standard äquivalenten zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-137">When checking meeting configuration settings, you might find it useful to compare the current settings against the default equivalents.</span></span> <span data-ttu-id="d95fa-138">Sie können die Standardeinstellungen für die besprechungskonfiguration anzeigen, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-138">You can view the default meeting configuration settings by running the following command:</span></span>

`New-CsMeetingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d95fa-139">Der vorherige Befehl erstellt eine speicherresidente Instanz der globalen Besprechungs Konfigurationseinstellungen, eine Instanz, die den Standardwert für jede Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="d95fa-139">The previous command creates an in-memory-only instance of the global meeting configuration settings, an instance that uses the default value for each property.</span></span> <span data-ttu-id="d95fa-140">Wenn Sie den Befehl ausführen, werden keine tatsächlichen Besprechungs Konfigurationseinstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d95fa-140">No actual meeting configuration settings are created when you run the command.</span></span> <span data-ttu-id="d95fa-141">Alle standardmäßigen Eigenschaftswerte werden jedoch auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d95fa-141">However, all the default property values will be displayed on-screen.</span></span>

</div>

<div>

## <a name="check-edge-servers-and-their-settings"></a><span data-ttu-id="d95fa-142">Überprüfen von Edgeserver und deren Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-142">Check Edge Servers and their settings</span></span>

<span data-ttu-id="d95fa-143">Edge-Server Informationen können mithilfe von Windows PowerShell abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-143">Edge Server information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="d95fa-144">Dieser Befehl gibt Informationen zu allen Edge-Servern zurück, die für die Verwendung in Ihrer Organisation konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="d95fa-144">This command returns information about all the Edge Servers configured for use in your organization:</span></span>

`Get-CsService -EdgeServer`

<span data-ttu-id="d95fa-145">Die zurückgegebenen Informationen enthalten alle FQDN-und Porteinstellungen für jeden Edgeserver:</span><span class="sxs-lookup"><span data-stu-id="d95fa-145">The returned information includes all of the FQDN and port settings for each Edge Server:</span></span>

<span data-ttu-id="d95fa-146">Identity: EdgeServer: DC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-146">Identity : EdgeServer: dc.fabrikam.com</span></span>

<span data-ttu-id="d95fa-147">Kanzler: Kanzler: LYNC-SE.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-147">Registrar : Registrar: LYNC-SE.fabrikam.com</span></span>

<span data-ttu-id="d95fa-148">AccessEdgeInternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="d95fa-148">AccessEdgeInternalSipPort : 5061</span></span>

<span data-ttu-id="d95fa-149">AccessEdgeExternalSipPort: 5061</span><span class="sxs-lookup"><span data-stu-id="d95fa-149">AccessEdgeExternalSipPort : 5061</span></span>

<span data-ttu-id="d95fa-150">AccessEdgeClientPort: 443</span><span class="sxs-lookup"><span data-stu-id="d95fa-150">AccessEdgeClientPort : 443</span></span>

<span data-ttu-id="d95fa-151">DataPsomServerPort: 8057</span><span class="sxs-lookup"><span data-stu-id="d95fa-151">DataPsomServerPort : 8057</span></span>

<span data-ttu-id="d95fa-152">DataPsomClientPort: 444</span><span class="sxs-lookup"><span data-stu-id="d95fa-152">DataPsomClientPort : 444</span></span>

<span data-ttu-id="d95fa-153">MediaRelayAuthEdgePort: 5062</span><span class="sxs-lookup"><span data-stu-id="d95fa-153">MediaRelayAuthEdgePort : 5062</span></span>

<span data-ttu-id="d95fa-154">MediaRelayAuthInternalTurnTcpPort: 443</span><span class="sxs-lookup"><span data-stu-id="d95fa-154">MediaRelayAuthInternalTurnTcpPort : 443</span></span>

<span data-ttu-id="d95fa-155">MediaRelayAuthExternalTurnTcpPort: 445</span><span class="sxs-lookup"><span data-stu-id="d95fa-155">MediaRelayAuthExternalTurnTcpPort : 445</span></span>

<span data-ttu-id="d95fa-156">MediaRelayAuthInternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="d95fa-156">MediaRelayAuthInternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="d95fa-157">MediaRelayAuthExternalTurnUdpPort: 3478</span><span class="sxs-lookup"><span data-stu-id="d95fa-157">MediaRelayAuthExternalTurnUdpPort : 3478</span></span>

<span data-ttu-id="d95fa-158">MediaCommunicationPortStart: 50000</span><span class="sxs-lookup"><span data-stu-id="d95fa-158">MediaCommunicationPortStart : 50000</span></span>

<span data-ttu-id="d95fa-159">MediaComunicationPortCount: 10000</span><span class="sxs-lookup"><span data-stu-id="d95fa-159">MediaComunicationPortCount : 10000</span></span>

<span data-ttu-id="d95fa-160">AccessEdgeExternalFqdn: DC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-160">AccessEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d95fa-161">DataEdgeExternalFqdn: DC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-161">DataEdgeExternalFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d95fa-162">AVEdgeExternalFqdn :</span><span class="sxs-lookup"><span data-stu-id="d95fa-162">AVEdgeExternalFqdn :</span></span>

<span data-ttu-id="d95fa-163">InternalInterfaceFqdn :</span><span class="sxs-lookup"><span data-stu-id="d95fa-163">InternalInterfaceFqdn :</span></span>

<span data-ttu-id="d95fa-164">ExternalMrasFqdn: DC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-164">ExternalMrasFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d95fa-165">DependentServiceList: {Registrar: LYNC-SE.fabrikam.com,</span><span class="sxs-lookup"><span data-stu-id="d95fa-165">DependentServiceList : {Registrar:LYNC-SE.fabrikam.com,</span></span>

<span data-ttu-id="d95fa-166">ConferencingServer: LYNC-SE. fabrikam</span><span class="sxs-lookup"><span data-stu-id="d95fa-166">ConferencingServer:LYNC-SE.fabrikam</span></span>

<span data-ttu-id="d95fa-167">com, MediationServer: LYNC-SE.</span><span class="sxs-lookup"><span data-stu-id="d95fa-167">com, MediationServer:LYNC-SE.</span></span>

<span data-ttu-id="d95fa-168">fabrikam.com}</span><span class="sxs-lookup"><span data-stu-id="d95fa-168">fabrikam.com}</span></span>

<span data-ttu-id="d95fa-169">Dienst-Nr: fabrikam.com-EdgeServer-2</span><span class="sxs-lookup"><span data-stu-id="d95fa-169">ServiceId : fabrikam.com-EdgeServer-2</span></span>

<span data-ttu-id="d95fa-170">Website-Nr: Website:fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="d95fa-170">SiteId : site:fabrikam.com</span></span>

<span data-ttu-id="d95fa-171">PoolFqdn: DC.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="d95fa-171">PoolFqdn : dc.fabrikam.com</span></span>

<span data-ttu-id="d95fa-172">Version: 5</span><span class="sxs-lookup"><span data-stu-id="d95fa-172">Version : 5</span></span>

<span data-ttu-id="d95fa-173">Rolle: EdgeServer</span><span class="sxs-lookup"><span data-stu-id="d95fa-173">Role : EdgeServer</span></span>

<div>

## <a name="check-federation-settings"></a><span data-ttu-id="d95fa-174">Überprüfen der Verbund Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-174">Check federation settings</span></span>

<span data-ttu-id="d95fa-175">Überprüfen Sie die Verbund Einstellungen, beispielsweise ob Sie konfiguriert ist und, wenn die Antwort "Ja" lautet, den FQDN und den Port.</span><span class="sxs-lookup"><span data-stu-id="d95fa-175">Check Federation settings, such as whether it is configured and, if the answer is "yes,", the FQDN and port.</span></span> <span data-ttu-id="d95fa-176">Der Verbund wird mithilfe der globalen Sammlung von Access Edge-Konfigurationseinstellungen aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d95fa-176">Federation is enabled and disabled by using the global collection of Access Edge configuration settings.</span></span> <span data-ttu-id="d95fa-177">Unter anderem bedeutet dies, dass der Verbund auf der Grundlage einer vollständigen oder gar nichts-Basis konfiguriert ist: entweder ist der Verbund für die gesamte Organisation aktiviert, oder der Verbund ist für die gesamte Organisation deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d95fa-177">Among other things, these mean that federation is configured on an all-or-nothing basis: either federation is enabled for the whole organization or federation is disabled for the whole organization</span></span>

<span data-ttu-id="d95fa-178">Ihre Access Edge-Konfigurationseinstellungen können mithilfe von Windows PowerShell zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-178">Your Access Edge configuration settings can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="d95fa-179">Führen Sie dazu den folgenden Windows PowerShell-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d95fa-179">To do that, run the following Windows PowerShell command:</span></span>

`Get-CsAccessEdgeConfiguration`

<span data-ttu-id="d95fa-180">Dieser Befehl gibt wiederum Daten zurück, die wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-180">In turn, that command will return data similar to this:</span></span>

<span data-ttu-id="d95fa-181">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-181">Identity : Global</span></span>

<span data-ttu-id="d95fa-182">AllowAnonymousUsers: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-182">AllowAnonymousUsers : False</span></span>

<span data-ttu-id="d95fa-183">AllowFederatedUsers: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-183">AllowFederatedUsers : False</span></span>

<span data-ttu-id="d95fa-184">AllowOutsideUsers: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-184">AllowOutsideUsers : False</span></span>

<span data-ttu-id="d95fa-185">Beclearing: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-185">BeClearingHouse : False</span></span>

<span data-ttu-id="d95fa-186">EnablePartnerDiscovery: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-186">EnablePartnerDiscovery : False</span></span>

<span data-ttu-id="d95fa-187">EnableArchivingDisclaimer: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-187">EnableArchivingDisclaimer : False</span></span>

<span data-ttu-id="d95fa-188">KeepCrlsUpToDateForPeers: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-188">KeepCrlsUpToDateForPeers : True</span></span>

<span data-ttu-id="d95fa-189">MarkSourceVerifiableOnOutgoingMessages: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-189">MarkSourceVerifiableOnOutgoingMessages : True</span></span>

<span data-ttu-id="d95fa-190">OutgoingTlsCountForFederatedPartners: 4</span><span class="sxs-lookup"><span data-stu-id="d95fa-190">OutgoingTlsCountForFederatedPartners : 4</span></span>

<span data-ttu-id="d95fa-191">RoutingMethod : UseDnsSrvRouting</span><span class="sxs-lookup"><span data-stu-id="d95fa-191">RoutingMethod : UseDnsSrvRouting</span></span>

<span data-ttu-id="d95fa-192">Wenn die **AllowFederatedUsers** -Eigenschaft auf "true" festgelegt ist, bedeutet dies, dass der Verbund für Ihre Organisation aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d95fa-192">If the **AllowFederatedUsers** property is set to True, that means that federation is enabled for your organization.</span></span> <span data-ttu-id="d95fa-193">(Wenn Sie **AllowFederatedUsers** auf "true" festlegen, bedeutet dies auch, dass Ihre lokalen Benutzer in einem geteilten Domänen Szenario nahtlos mit ihren in-the-Cloud-Benutzern kommunizieren können.)</span><span class="sxs-lookup"><span data-stu-id="d95fa-193">(Setting **AllowFederatedUsers** to True also means that, in a split domain scenario, your on-premises users will be able to communicate seamlessly with your in-the-cloud users.)</span></span>

<span data-ttu-id="d95fa-194">Informationen zum Abrufen der FQDN-und Porteinstellungen für Ihren Edgeserver finden Sie in der vorherigen Aufgabe (Edgeserver und deren Einstellungen).</span><span class="sxs-lookup"><span data-stu-id="d95fa-194">To retrieve the FQDN and port settings for your Edge Server, see the previous task (Edge Servers and their settings).</span></span>

<span data-ttu-id="d95fa-195">Das Aktivieren des Föderations Bereichs im globalen Bereich bedeutet nur, dass Benutzer potenziell mit Verbundbenutzern kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="d95fa-195">Enabling federation at the global scope only means that users can potentially communicate with federated users.</span></span> <span data-ttu-id="d95fa-196">Wenn Sie feststellen möchten, ob einzelne Benutzer tatsächlich mit Verbundbenutzern kommunizieren können, müssen Sie die Richtlinie für den externen Benutzer Zugriff untersuchen, die diesem Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d95fa-196">To determine whether any individual users can actually communicate with federated users requires you to examine the external user access policy assigned to that user.</span></span>

<span data-ttu-id="d95fa-197">Zugriffsinformationen für externe Benutzer können mithilfe von Windows PowerShell zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-197">External user access information can be returned by using Windows PowerShell.</span></span> <span data-ttu-id="d95fa-198">Dieser Befehl gibt beispielsweise Informationen für die globale Richtlinie für den externen Benutzer Zugriff zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-198">For example, this command returns information for the global external user access policy:</span></span>

`Get-CsExternalAccessPolicy -Identity "Global"`

<span data-ttu-id="d95fa-199">Und dieser Befehl gibt Informationen für alle Richtlinien für den externen Benutzer Zugriff zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-199">And this command returns information for all the external user access policies:</span></span>

`Get-CsExternalAccessPolicy`

<span data-ttu-id="d95fa-200">Die zurückgegebenen Informationen werden wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-200">The returned information will resemble this:</span></span>

<span data-ttu-id="d95fa-201">Identität: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-201">Identity : False</span></span>

<span data-ttu-id="d95fa-202">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95fa-202">Description :</span></span>

<span data-ttu-id="d95fa-203">EnableFederationAccess: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-203">EnableFederationAccess : False</span></span>

<span data-ttu-id="d95fa-204">EnablePublicCloudAccess: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-204">EnablePublicCloudAccess : False</span></span>

<span data-ttu-id="d95fa-205">EnablePublicCloudAccessAudioVideoAccess: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-205">EnablePublicCloudAccessAudioVideoAccess : False</span></span>

<span data-ttu-id="d95fa-206">EnableOutsideAccess: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-206">EnableOutsideAccess : False</span></span>

<span data-ttu-id="d95fa-207">Wenn **EnableFederationAccess** auf "true" festgelegt ist, können Benutzer, die von der angegebenen Richtlinie verwaltet werden, mit Verbundbenutzern kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d95fa-207">If **EnableFederationAccess** is set to True, then users managed by the given policy can communicate with federated users.</span></span>

</div>

</div>

<div>

## <a name="check-archiving-settings"></a><span data-ttu-id="d95fa-208">Überprüfen der Archivierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-208">Check archiving settings</span></span>

<span data-ttu-id="d95fa-209">Überprüfen Sie die Archivierungseinstellungen für die interne und die Verbundkommunikation. Bevor Sie die Einstellungen für die interne und externe Archivierung überprüfen, sollten Sie sicherstellen, dass die Archivierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d95fa-209">Check archiving settings for internal and federated communications.Before verifying the settings for internal and external archiving, you should verify that archiving is enabled.</span></span>

<span data-ttu-id="d95fa-210">Die Archivierungs Konfigurationseinstellungen können mithilfe von Windows PowerShell und dem Get-CsArchivingConfiguration-Cmdlet überprüft werden:</span><span class="sxs-lookup"><span data-stu-id="d95fa-210">Archiving configuration settings can be verified by using Windows PowerShell and the Get-CsArchivingConfiguration cmdlet:</span></span>

`Get-CsArchivingConfiguration -Identity "Global"`

<span data-ttu-id="d95fa-211">Beachten Sie, dass Archivierungseinstellungen auch im Website Bereich konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="d95fa-211">Note that archiving settings can also be configured at the site scope.</span></span> <span data-ttu-id="d95fa-212">Wenn Sie Informationen zu allen Archivierungseinstellungen zurückgeben möchten, verwenden Sie den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="d95fa-212">To return information about all the archiving settings, use this command:</span></span>

`Get-CsArchivingConfiguration`

<span data-ttu-id="d95fa-213">Das Get-CsArchivingConfiguration-Cmdlet gibt Daten ähnlich wie folgt zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-213">The Get-CsArchivingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="d95fa-214">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-214">Identity : Global</span></span>

<span data-ttu-id="d95fa-215">EnableArchiving: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-215">EnableArchiving : False</span></span>

<span data-ttu-id="d95fa-216">EnablePurging: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-216">EnablePurging : False</span></span>

<span data-ttu-id="d95fa-217">PurgeExportedArchivesOnly: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-217">PurgeExportedArchivesOnly : False</span></span>

<span data-ttu-id="d95fa-218">BlockOnArchiveFailure: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-218">BlockOnArchiveFailure : False</span></span>

<span data-ttu-id="d95fa-219">"Keeparchivingdatafordays": 14</span><span class="sxs-lookup"><span data-stu-id="d95fa-219">KeepArchivingDataForDays : 14</span></span>

<span data-ttu-id="d95fa-220">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="d95fa-220">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="d95fa-221">ArchiveDuplicateMessages: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-221">ArchiveDuplicateMessages : True</span></span>

<span data-ttu-id="d95fa-222">CachePurgingInterval: 24</span><span class="sxs-lookup"><span data-stu-id="d95fa-222">CachePurgingInterval : 24</span></span>

<span data-ttu-id="d95fa-223">Wenn die EnableArchiving-Eigenschaft auf false festgelegt ist, bedeutet dies, dass keine Kommunikationssitzungen archiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-223">If the EnableArchiving property is set to False, that means that no communication sessions will be archived.</span></span> <span data-ttu-id="d95fa-224">Wenn Sie nur Instant Messaging-Sitzungen archivieren möchten, verwenden Sie einen Befehl wie den folgenden, um die Archivierung von Chatsitzungen zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="d95fa-224">If you want to archive instant messaging sessions only, use a command such as the following to enable the archiving of IM sessions:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="d95fa-225">Verwenden Sie den folgenden Befehl, um Konferenzsitzungen und Chatsitzungen zu archivieren:</span><span class="sxs-lookup"><span data-stu-id="d95fa-225">To archive conferencing sessions and instant messaging sessions, use this command:</span></span>

`Set-CsArchivingConfiguration -Identity "Global" -EnableArchiving "IMOnly"`

<span data-ttu-id="d95fa-226">Wenn Sie Ihre aktuellen Archivierungseinstellungen mit den Standardeinstellungen vergleichen möchten, führen Sie den folgenden Windows PowerShell-Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d95fa-226">If you’d like to compare your current archiving settings with the default settings, run the following Windows PowerShell command:</span></span>

`New-CsArchivingConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d95fa-227">Dieser Befehl erstellt eine speicherresidente Instanz der globalen Archivierungs Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-227">That command creates an in-memory-only instance of the global archiving configuration settings.</span></span> <span data-ttu-id="d95fa-228">Hierbei handelt es sich nicht um eine echte Sammlung von Einstellungen, die von lync Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-228">This is not a real collection of settings that is used by Lync Server.</span></span> <span data-ttu-id="d95fa-229">Es werden jedoch die Standardwerte für alle Archivierungs Konfigurationseigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d95fa-229">However, it does display the default values for all the archiving configuration properties.</span></span>

<span data-ttu-id="d95fa-230">Sie können diesen Befehl auch verwenden, um den FQDN ihrer Archivierungsserver zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="d95fa-230">You can also use this command to return the FQDN of your Archiving servers:</span></span>

`Get-CsService -ArchivingServer`

<span data-ttu-id="d95fa-231">Nachdem Sie überprüft haben, dass die Archivierung aktiviert ist, können Sie Ihre Archivierungsrichtlinien anzeigen, um festzustellen, ob interne und externe Kommunikationssitzungen archiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-231">After you have verified that archiving is enabled, you can then view your archiving policies to determine whether internal and external communication sessions are being archived.</span></span>

<span data-ttu-id="d95fa-232">Informationen zur Archivierungsrichtlinie können mithilfe des Get-CsArchivingPolicy-Cmdlets abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-232">Archiving policy information can be retrieved by using the Get-CsArchivingPolicy cmdlet.</span></span> <span data-ttu-id="d95fa-233">Dieser Befehl gibt beispielsweise Informationen zur globalen Archivierungsrichtlinie zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-233">For example, this command returns information about the global archiving policy:</span></span>

`Get-CsArchivingPolicy -Identity "Global"`

<span data-ttu-id="d95fa-234">Da Archivierungsrichtlinien auch auf der Website und im Benutzerbereich konfiguriert werden können, möchten Sie möglicherweise auch diesen Befehl verwenden, der Informationen zu allen Archivierungsrichtlinien zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-234">Because archiving policies can also be configured at the site and the per-user scope, you might also want to use this command, which returns information about all the archiving policies:</span></span>

`Get-CsArchivingPolicy`

<span data-ttu-id="d95fa-235">Die Informationen, die Sie von Get-CsArchivingPolicy erhalten, ähneln Ihnen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-235">The information that you receive from Get-CsArchivingPolicy will resemble this:</span></span>

<span data-ttu-id="d95fa-236">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-236">Identity : Global</span></span>

<span data-ttu-id="d95fa-237">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95fa-237">Description :</span></span>

<span data-ttu-id="d95fa-238">ArchiveInternal: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-238">ArchiveInternal : False</span></span>

<span data-ttu-id="d95fa-239">ArchiveExternal: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-239">ArchiveExternal : False</span></span>

<span data-ttu-id="d95fa-240">Beachten Sie, dass die interne und externe Archivierung standardmäßig in einer Archivierungsrichtlinie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d95fa-240">Note that, by default, both internal and external archiving are disabled in an archiving policy.</span></span>

</div>

<div>

## <a name="check-cdr-settings"></a><span data-ttu-id="d95fa-241">Überprüfen der CDR-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="d95fa-241">Check CDR settings</span></span>

<span data-ttu-id="d95fa-242">Überprüfen Sie die Einstellungen für den Anruf Detailsatz (CDR) für Peer-to-Peer-, Konferenz-und Sprachanruf Detail Aufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="d95fa-242">Check Call Detail Record (CDR) settings for peer-to-peer, conferencing, and Voice call detail recording.</span></span> <span data-ttu-id="d95fa-243">Detaillierte Informationen zu Ihren CDR-Einstellungen können mit dem Cmdlet **Get-CsCdrConfiguration** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-243">Detailed information about your CDR settings can be returned by using the **Get-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="d95fa-244">Dieser Befehl gibt beispielsweise Informationen zur globalen Sammlung von CDR-Konfigurationseinstellungen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-244">For example, this command returns information about the global collection of CDR configuration settings:</span></span>

`Get-CsCdrConfiguration -Identity "Global"`

<span data-ttu-id="d95fa-245">Da CdR auch im Website Bereich konfiguriert werden kann, möchten Sie möglicherweise auch diesen Befehl ausführen, der Informationen zu allen CdR-Konfigurationseinstellungen zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-245">Because CDR can also be configured at the site scope, you might also want to run this command, which returns information about all the CDR configuration settings:</span></span>

`Get-CsCdrConfiguration`

<span data-ttu-id="d95fa-246">Das Get-CsCdrConfiguration-Cmdlet gibt für jede Sammlung von CDR-Konfigurationseinstellungen ähnliche Informationen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-246">The Get-CsCdrConfiguration cmdlet returns information similar to this for each collection of CDR configuration settings:</span></span>

<span data-ttu-id="d95fa-247">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-247">Identity : Global</span></span>

<span data-ttu-id="d95fa-248">EnableCDR: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-248">EnableCDR : True</span></span>

<span data-ttu-id="d95fa-249">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-249">EnablePurging : True</span></span>

<span data-ttu-id="d95fa-250">KeepCallDetailForDays: 60</span><span class="sxs-lookup"><span data-stu-id="d95fa-250">KeepCallDetailForDays : 60</span></span>

<span data-ttu-id="d95fa-251">KeepErrorReportForDays: 60</span><span class="sxs-lookup"><span data-stu-id="d95fa-251">KeepErrorReportForDays : 60</span></span>

<span data-ttu-id="d95fa-252">PurgeHourOfDay: 2</span><span class="sxs-lookup"><span data-stu-id="d95fa-252">PurgeHourOfDay : 2</span></span>

<span data-ttu-id="d95fa-253">Ähnliche Informationen können für die QoE-Überwachung mithilfe des Get-CsQoEConfiguration-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-253">Similar information can be returned for QoE monitoring by using the Get-CsQoEConfiguration cmdlet.</span></span> <span data-ttu-id="d95fa-254">Dieser Befehl gibt beispielsweise Informationen zur globalen Sammlung der QoE-Konfigurationseinstellungen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-254">For example, this command returns information about the global collection of QoE configuration settings:</span></span>

`Get-QoEConfiguration -Identity "Global"`

<span data-ttu-id="d95fa-255">Diese Informationen werden wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-255">That information will resemble this:</span></span>

<span data-ttu-id="d95fa-256">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-256">Identity : Global</span></span>

<span data-ttu-id="d95fa-257">ExternalConsumerIssuedCertId :</span><span class="sxs-lookup"><span data-stu-id="d95fa-257">ExternalConsumerIssuedCertId :</span></span>

<span data-ttu-id="d95fa-258">EnablePurging: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-258">EnablePurging : True</span></span>

<span data-ttu-id="d95fa-259">KeepQoEDataForDays: 60</span><span class="sxs-lookup"><span data-stu-id="d95fa-259">KeepQoEDataForDays : 60</span></span>

<span data-ttu-id="d95fa-260">PurgeHourOfDay: 1</span><span class="sxs-lookup"><span data-stu-id="d95fa-260">PurgeHourOfDay : 1</span></span>

<span data-ttu-id="d95fa-261">EnableExternalConsumer: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-261">EnableExternalConsumer : False</span></span>

<span data-ttu-id="d95fa-262">ExternalConsumerName :</span><span class="sxs-lookup"><span data-stu-id="d95fa-262">ExternalConsumerName :</span></span>

<span data-ttu-id="d95fa-263">ExternalConsumerURL :</span><span class="sxs-lookup"><span data-stu-id="d95fa-263">ExternalConsumerURL :</span></span>

<span data-ttu-id="d95fa-264">EnableQoE: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-264">EnableQoE : True</span></span>

<span data-ttu-id="d95fa-265">Wenn Sie Ihre aktuellen CdR-Einstellungen mit den standardmäßigen CdR-Einstellungen vergleichen möchten, können Sie die Standardwerte überprüfen, indem Sie folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-265">If you want to compare your current CDR settings with the default CDR settings, the default values can be reviewed by running this command:</span></span>

`New-CsCdrConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d95fa-266">Ebenso können die Standardwerte für die QoE-Überwachung mithilfe dieses Befehls abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="d95fa-266">Likewise, the default values for QoE monitoring can be retrieved by using this command:</span></span>

`New-CsQoEConfiguration -Identity "Global" -InMemory`

<span data-ttu-id="d95fa-267">Sie können auch den FQDN ihrer Überwachungsserver zurückgeben, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-267">You can also return the FQDN of your Monitoring servers by running this command:</span></span>

`Get-CsService -MonitoringServer`

</div>

<div>

## <a name="check-voice-settings"></a><span data-ttu-id="d95fa-268">Spracheinstellungen überprüfen</span><span class="sxs-lookup"><span data-stu-id="d95fa-268">Check voice settings</span></span>

<span data-ttu-id="d95fa-269">Die in der Regel für Administratoren wichtigen Spracheinstellungen sind in VoIP-Richtlinien und VoIP-Routen enthalten: VoIP-Richtlinien enthalten die Einstellungen, die die für einzelne Benutzer verfügbar gemachten Funktionen (wie die Möglichkeit zum Weiterleiten oder übertragen von Anrufen) bestimmen, während VoIP-Routen bestimmen, wie (und wenn) Anrufe über das PSTN weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-269">The voice settings typically important to administrators are contained in voice policies and voice routes: voice policies contain the settings that determine the capabilities exposed to individual users (such as the ability to forward or transfer calls), while voice routes determine how (and if) calls are routed across the PSTN.</span></span>

<span data-ttu-id="d95fa-270">VoIP-Richtlinieninformationen können mithilfe von Windows PowerShell abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-270">Voice policy information can be retrieved by using Windows PowerShell.</span></span> <span data-ttu-id="d95fa-271">Dieser Befehl gibt beispielsweise Informationen zur globalen VoIP-Richtlinie zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-271">For example, this command returns information about the global voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global"`

<span data-ttu-id="d95fa-272">Und dieser Befehl gibt Informationen zu allen VoIP-Richtlinien zurück, die für die Verwendung in der Organisation konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="d95fa-272">And this command returns information about all the voice policies configured for use in the organization:</span></span>

`Get-CsVoicePolicy`

<span data-ttu-id="d95fa-273">Die vom Get-CsVoicePolicy-Cmdlet zurückgegebenen Informationen ähneln wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-273">The information returned by the Get-CsVoicePolicy cmdlet resembles the following:</span></span>

<span data-ttu-id="d95fa-274">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-274">Identity : Global</span></span>

<span data-ttu-id="d95fa-275">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="d95fa-275">PstnUsages : {}</span></span>

<span data-ttu-id="d95fa-276">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95fa-276">Description :</span></span>

<span data-ttu-id="d95fa-277">AllowSimulRing: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-277">AllowSimulRing : True</span></span>

<span data-ttu-id="d95fa-278">AllowCallForwarding: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-278">AllowCallForwarding : True</span></span>

<span data-ttu-id="d95fa-279">AllowPSTNReRouting: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-279">AllowPSTNReRouting : True</span></span>

<span data-ttu-id="d95fa-280">Name: DefaultPolicy</span><span class="sxs-lookup"><span data-stu-id="d95fa-280">Name : DefaultPolicy</span></span>

<span data-ttu-id="d95fa-281">EnableDelegation: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-281">EnableDelegation : True</span></span>

<span data-ttu-id="d95fa-282">EnableTeamCall: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-282">EnableTeamCall : True</span></span>

<span data-ttu-id="d95fa-283">EnableCallTransfer: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-283">EnableCallTransfer : True</span></span>

<span data-ttu-id="d95fa-284">EnableCallPark: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-284">EnableCallPark : False</span></span>

<span data-ttu-id="d95fa-285">EnableMaliciousCallTracing: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-285">EnableMaliciousCallTracing : False</span></span>

<span data-ttu-id="d95fa-286">EnableBWPolicyOverride: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-286">EnableBWPolicyOverride : False</span></span>

<span data-ttu-id="d95fa-287">PreventPSTNTollBypass: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-287">PreventPSTNTollBypass : False</span></span>

<span data-ttu-id="d95fa-288">Sie können auch Abfragen erstellen, die eine Teilmenge ihrer VoIP-Richtlinien zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="d95fa-288">You can also create queries that returned a subset of your voice policies.</span></span> <span data-ttu-id="d95fa-289">Dieser Befehl gibt beispielsweise alle VoIP-Richtlinien zurück, die die Anrufweiterleitung zulassen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-289">For example, this command returns all the voice policies that allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $True}`

<span data-ttu-id="d95fa-290">Und dieser Befehl gibt alle VoIP-Richtlinien zurück, die keine Anrufweiterleitung zulassen:</span><span class="sxs-lookup"><span data-stu-id="d95fa-290">And this command returns all the voice policies that don’t allow call forwarding:</span></span>

`Get-CsVoicePolicy | Where-Object {$_.AllowCallForwarding -eq $False}`

<span data-ttu-id="d95fa-291">Verwenden Sie in Windows PowerShell das Get-CsVoiceRouting-Cmdlet, um Informationen zu Ihren VoIP-Routen zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="d95fa-291">In Windows PowerShell, use the Get-CsVoiceRouting cmdlet to return information about your voice routes:</span></span>

`Get-CsVoiceRoute`

<span data-ttu-id="d95fa-292">Dieser Befehl gibt Informationen wie diesen für alle VoIP-Routen zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-292">That command returns information such as this for all the voice routes:</span></span>

<span data-ttu-id="d95fa-293">Identität: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="d95fa-293">Identity : LocalRoute</span></span>

<span data-ttu-id="d95fa-294">Priorität: 0</span><span class="sxs-lookup"><span data-stu-id="d95fa-294">Priority : 0</span></span>

<span data-ttu-id="d95fa-295">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95fa-295">Description :</span></span>

<span data-ttu-id="d95fa-296">NumberPattern: ^ ( \\ + 1 \[ 0-9 \] {10} ) $</span><span class="sxs-lookup"><span data-stu-id="d95fa-296">NumberPattern : ^(\\+1\[0-9\]{10})$</span></span>

<span data-ttu-id="d95fa-297">PstnUsages : {}</span><span class="sxs-lookup"><span data-stu-id="d95fa-297">PstnUsages : {}</span></span>

<span data-ttu-id="d95fa-298">PstnGatewayList : {}</span><span class="sxs-lookup"><span data-stu-id="d95fa-298">PstnGatewayList : {}</span></span>

<span data-ttu-id="d95fa-299">Name: LocalRoute</span><span class="sxs-lookup"><span data-stu-id="d95fa-299">Name : LocalRoute</span></span>

<span data-ttu-id="d95fa-300">SuppressCallerId :</span><span class="sxs-lookup"><span data-stu-id="d95fa-300">SuppressCallerId :</span></span>

<span data-ttu-id="d95fa-301">AlternateCallerId :</span><span class="sxs-lookup"><span data-stu-id="d95fa-301">AlternateCallerId :</span></span>

<span data-ttu-id="d95fa-302">Mit lync Server können Sie VoIP-Routen erstellen, die keine PSTN-Nutzung aufweisen, und kein PSTN-Gateway angeben.</span><span class="sxs-lookup"><span data-stu-id="d95fa-302">Lync Server allows you to create voice routes that do not have a PSTN usage and do not specify a PSTN gateway.</span></span> <span data-ttu-id="d95fa-303">Sie können jedoch keine Anrufe über eine VoIP-Route weiterleiten, für die diese beiden Eigenschaftswerte nicht konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="d95fa-303">However, you can't actually route calls over a voice route that does not have these two property values configured.</span></span> <span data-ttu-id="d95fa-304">Aus diesem Grund ist es möglicherweise hilfreich, diesen Befehl in regelmäßigen Abständen auszuführen, wodurch die Identität einer VoIP-Route zurückgegeben wird, die keine PSTN-Nutzung aufweist:</span><span class="sxs-lookup"><span data-stu-id="d95fa-304">Because of that, you might find it useful to periodically run this command, which returns the identity of any voice route that does not have a PSTN usage:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnUsages -eq $Null} | Select-Object Identity`

<span data-ttu-id="d95fa-305">Ebenso gibt dieser Befehl die Identität einer VoIP-Route zurück, die nicht für ein PSTN-Gateway konfiguriert wurde:</span><span class="sxs-lookup"><span data-stu-id="d95fa-305">Similarly, this command returns the identity of any voice route that has not been configured to have a PSTN gateway:</span></span>

`Get-CsVoiceRoute | Where-Object {$_.PstnGatewayList -eq $Null}} | Select-Object Identity`

</div>

<div>

## <a name="check-conferencing-attendant-settings"></a><span data-ttu-id="d95fa-306">Überprüfen der Einstellungen der Konferenzzentrale</span><span class="sxs-lookup"><span data-stu-id="d95fa-306">Check Conferencing Attendant settings</span></span>

<span data-ttu-id="d95fa-307">Überprüfen Sie die Einstellungen der Konferenzzentrale für PSTN-Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="d95fa-307">Check conferencing Attendant settings for PSTN dial-in conferencing.</span></span> <span data-ttu-id="d95fa-308">Einstellungen der Konferenzzentrale können nur mit dem Cmdlet **Get-CsDialInConferencingConfiguration** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d95fa-308">Conferencing Attendant settings can only be retrieved by using the **Get-CsDialInConferencingConfiguration** cmdlet.</span></span> <span data-ttu-id="d95fa-309">Diese Einstellungen stehen in der lync Server-Systemsteuerung nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d95fa-309">These settings are not available in the Lync Server Control Panel.</span></span> <span data-ttu-id="d95fa-310">Verwenden Sie zum Anzeigen der Einstellungen der Konferenzzentrale einen Windows PowerShell-Befehl ähnlich der folgenden, der die globale Sammlung der Konferenz Aufsichts Einstellungen zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="d95fa-310">To view your Conferencing Attendant settings, use a Windows PowerShell command similar to the following, which returns the global collection of Conferencing Attendant settings:</span></span>

`Get-CsDialInConferencingConfiguration -Identity "Global"`

<span data-ttu-id="d95fa-311">Beachten Sie, dass die Einstellungen der Konferenzzentrale auch im Website Bereich konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="d95fa-311">Note that Conferencing Attendant settings can also be configured at the site scope.</span></span> <span data-ttu-id="d95fa-312">Wenn Sie Informationen zu allen Einstellungen der Konferenzzentrale zurückgeben möchten, verwenden Sie stattdessen folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="d95fa-312">To return information about all the Conferencing Attendant settings, use this command instead:</span></span>

`Get-CsDialInConferencingConfiguration`

<span data-ttu-id="d95fa-313">Das Get-CsDialInConferencingConfiguration-Cmdlet gibt Daten ähnlich wie folgt zurück:</span><span class="sxs-lookup"><span data-stu-id="d95fa-313">The Get-CsDialInConferencingConfiguration cmdlet returns data similar to this:</span></span>

<span data-ttu-id="d95fa-314">Identität: Global</span><span class="sxs-lookup"><span data-stu-id="d95fa-314">Identity : Global</span></span>

<span data-ttu-id="d95fa-315">EntryExitAnnouncementsType : UseNames</span><span class="sxs-lookup"><span data-stu-id="d95fa-315">EntryExitAnnouncementsType : UseNames</span></span>

<span data-ttu-id="d95fa-316">EnableNameRecording: true</span><span class="sxs-lookup"><span data-stu-id="d95fa-316">EnableNameRecording : True</span></span>

<span data-ttu-id="d95fa-317">EntryExitAnnouncementsEnabledByDefault: falsch</span><span class="sxs-lookup"><span data-stu-id="d95fa-317">EntryExitAnnouncementsEnabledByDefault : False</span></span>

<span data-ttu-id="d95fa-318">Wenn EntryExitAnnouncementsEnabledByDefault auf "false" festgelegt ist, bedeutet dies, dass die Konferenz Ankündigungen deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d95fa-318">If EntryExitAnnouncementsEnabledByDefault is set to False, that means the conferencing announcements are disabled.</span></span> <span data-ttu-id="d95fa-319">Führen Sie zum Aktivieren von Eingabe-und Beendigungs Ankündigungen einen Windows PowerShell-Befehl wie den folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="d95fa-319">To enable entry and exit announcements, run a Windows PowerShell command similar to this:</span></span>

`Set-CsDialInConferencingConfiguration -Identity "Global" -EntryExitAnnouncementsEnabledByDefault $True`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d95fa-320">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d95fa-320">See Also</span></span>


[<span data-ttu-id="d95fa-321">Get-CsSipDomain</span><span class="sxs-lookup"><span data-stu-id="d95fa-321">Get-CsSipDomain</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsSipDomain)  
[<span data-ttu-id="d95fa-322">Get-CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95fa-322">Get-CsMeetingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsMeetingConfiguration)  
[<span data-ttu-id="d95fa-323">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="d95fa-323">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="d95fa-324">Get-csaccessedgeconfiguration nicht angeben</span><span class="sxs-lookup"><span data-stu-id="d95fa-324">Get-CsAccessEdgeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAccessEdgeConfiguration)  
[<span data-ttu-id="d95fa-325">Get-CsExternalAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d95fa-325">Get-CsExternalAccessPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsExternalAccessPolicy)  
[<span data-ttu-id="d95fa-326">Get-CsArchivingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95fa-326">Get-CsArchivingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsArchivingConfiguration)  
[<span data-ttu-id="d95fa-327">Get-CsCdrConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95fa-327">Get-CsCdrConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration)  
[<span data-ttu-id="d95fa-328">Get-CsQoEConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95fa-328">Get-CsQoEConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsQoEConfiguration)  
[<span data-ttu-id="d95fa-329">Get-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="d95fa-329">Get-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoicePolicy)  
[<span data-ttu-id="d95fa-330">Get-CsVoiceRoute</span><span class="sxs-lookup"><span data-stu-id="d95fa-330">Get-CsVoiceRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsVoiceRoute)  
[<span data-ttu-id="d95fa-331">Get-CsDialInConferencingConfiguration</span><span class="sxs-lookup"><span data-stu-id="d95fa-331">Get-CsDialInConferencingConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingConfiguration)  
  

<span data-ttu-id="d95fa-332"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d95fa-332"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

