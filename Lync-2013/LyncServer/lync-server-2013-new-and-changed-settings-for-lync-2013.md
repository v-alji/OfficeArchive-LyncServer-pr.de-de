---
title: 'Lync Server 2013: neue und geänderte Einstellungen für lync 2013'
description: 'Lync Server 2013: neue und geänderte Einstellungen für lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New and changed settings for Lync 2013
ms:assetid: bb13789c-7eda-461c-a387-02ea8ca4dabe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205204(v=OCS.15)
ms:contentKeyID: 48185241
ms.date: 12/08/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf744e1bae774904733390ec624be523ad32bc1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445484"
---
# <a name="new-and-changed-settings-for-lync-2013"></a><span data-ttu-id="cb3c2-103">Neue und geänderte Einstellungen für lync 2013</span><span class="sxs-lookup"><span data-stu-id="cb3c2-103">New and changed settings for Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb3c2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb3c2-104">

<span> </span></span></span>

<span data-ttu-id="cb3c2-105">_**Letztes Änderungsdatum des Themas:** 2014-12-05_</span><span class="sxs-lookup"><span data-stu-id="cb3c2-105">_**Topic Last Modified:** 2014-12-05_</span></span>

<span data-ttu-id="cb3c2-106">In diesem Thema werden Änderungen an Cmdlets der lync Server-Verwaltungsshell erläutert, die sich direkt auf die Clientverwaltung beziehen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-106">This topic discusses changes to Lync Server Management Shell cmdlets that relate directly to client management.</span></span> <span data-ttu-id="cb3c2-107">Lync Server 2013 führt verschiedene neue Parameter ein und verwirft Parameter für Features, die auf andere Weise konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-107">Lync Server 2013 introduces several new parameters, and deprecates parameters for features that can be configured through other means.</span></span>

<div>

## <a name="new-client-management-parameters"></a><span data-ttu-id="cb3c2-108">Neue Client Verwaltungsparameter</span><span class="sxs-lookup"><span data-stu-id="cb3c2-108">New Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb3c2-109">Neu</span><span class="sxs-lookup"><span data-stu-id="cb3c2-109">New</span></span></th>
<th><span data-ttu-id="cb3c2-110">Cmdlet "lync Server-Verwaltungsshell"</span><span class="sxs-lookup"><span data-stu-id="cb3c2-110">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="cb3c2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb3c2-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-112">TracingLevel</span><span class="sxs-lookup"><span data-stu-id="cb3c2-112">TracingLevel</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-113">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-113">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-114">Wenn Sie auf "true" festgelegt ist, wird die Software Ablaufverfolgung in lync aktiviert. Wenn Sie auf false festgelegt ist, wird die Software Ablaufverfolgung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-114">When set to True, software tracing will be enabled in Lync; when set to False, software tracing will be disabled.</span></span> <span data-ttu-id="cb3c2-115">Bei der Software Ablaufverfolgung wird eine detaillierte Aufzeichnung aller Elemente des Programms (einschließlich nach Verfolgungs-API-aufrufen) unterhalten.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-115">Software tracing involves keeping a detailed record of everything that a program does (including tracking API calls).</span></span> <span data-ttu-id="cb3c2-116">Die Ablaufverfolgung ist für Entwickler und das Supportpersonal der Anwendung hauptsächlich hilfreich. Diese Einstellung entspricht der Gruppenrichtlinieneinstellung Communications Server 2007 R2 aktivieren der &quot; Ablaufverfolgung für Communicator. &quot; Die Einstellungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cb3c2-116">Tracing is mostly useful to developers and to application support personnel.This setting is equivalent to the Communications Server 2007 R2 Group Policy setting &quot;Turn on tracing for Communicator.&quot; The settings are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="cb3c2-117">Off = Ablaufverfolgung ist deaktiviert, und der Benutzer kann diese Einstellung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-117">Off = Tracing is disabled and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="cb3c2-118">Light = minimale Nachverfolgung wird ausgeführt, und der Benutzer kann diese Einstellung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-118">Light = Minimal tracing is performed, and the user cannot change this setting.</span></span></p></li>
<li><p><span data-ttu-id="cb3c2-119">On = Verbose-Ablaufverfolgung wird ausgeführt, und der Benutzer kann diese Einstellung nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-119">On = Verbose tracing is performed, and the user cannot change this setting.</span></span></p></li>
</ul>
<p><span data-ttu-id="cb3c2-120">Standardmäßig ist TracingLevel auf einen NULL-Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-120">By default TracingLevel is set to a null value.</span></span> <span data-ttu-id="cb3c2-121">Das bedeutet, dass die minimale Ablaufverfolgung ausgeführt wird, aber der Benutzer kann diese minimale Ablaufverfolgung aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-121">That means that minimal tracing is performed, but the user can enable or disable this minimal tracing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-122">EnableMediaRedirection</span><span class="sxs-lookup"><span data-stu-id="cb3c2-122">EnableMediaRedirection</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-123">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-123">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-124">Wenn der Wert auf true ($true) festgelegt ist, können Audio-und Videodatenströme vom anderen Netzwerkdatenverkehr getrennt werden, was wiederum Clientgeräten ermöglicht, Audio-und Videodaten lokal zu codieren und zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-124">When set to True ($True) allows audio and video streams to be separated from other network traffic, In turn, this allows client devices to do encoding and decoding of audio and video locally.</span></span> <span data-ttu-id="cb3c2-125">Die Medien Umleitung führt in der Regel zu einer niedrigeren Bandbreitennutzung, höherer Serverskalierbarkeit und einer optimierten Benutzererfahrung im Vergleich zu ähnlichen Techniken wie Geräte-Remoting oder Codec-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-125">Media redirection typically results in lower bandwidth usage, higher server scalability, and a more-optimal user experience compared to similar techniques such as device remoting or codec compression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-126">AllowLargeMeetings</span><span class="sxs-lookup"><span data-stu-id="cb3c2-126">AllowLargeMeetings</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-127">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="cb3c2-127">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-128">Wenn Sie auf "true" festgelegt ist, werden alle lync-Besprechungen als &quot; große Besprechungen behandelt. &quot; Bei einer großen Besprechung werden Einschränkungen für die Anzahl der Benachrichtigungen, die an die Teilnehmer gesendet werden, sowie die Größe des standardmäßig übermittelten Besprechungs Arbeitsplans festgestellt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-128">When set to True, all Lync Meetings are treated as &quot;large meetings.&quot; With a large meeting, restrictions are placed on the number of notifications that are sent to participants, in addition to the size of the meeting roster that is transmitted by default.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-129">DisablePowerPointAnnotations</span><span class="sxs-lookup"><span data-stu-id="cb3c2-129">DisablePowerPointAnnotations</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-130">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="cb3c2-130">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-131">Bei Festlegung auf true ($true) können Benutzer keine Anmerkungen zu PowerPoint-Folien hinzufügen, die in einer Konferenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-131">When set to True ($True) users won’t be able to add annotations to PowerPoint slides used in a conference.</span></span> <span data-ttu-id="cb3c2-132">Je nach dem Wert der AllowAnnotations-Eigenschaft können die Benutzer jedoch weiterhin auf andere Whiteboard-Features zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-132">However (depending on the value of the AllowAnnotations property), users will still have access to other whiteboarding features.</span></span> <span data-ttu-id="cb3c2-133">Der Standardwert ist "falsch", was bedeutet, dass PowerPoint-Anmerkungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-133">The default value is False, meaning that PowerPoint annotations are allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-134">AllowSharedNotes</span><span class="sxs-lookup"><span data-stu-id="cb3c2-134">AllowSharedNotes</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-135">CsConferencing</span><span class="sxs-lookup"><span data-stu-id="cb3c2-135">CsConferencing</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-136">Wenn auf "true" (der Standardwert) festgelegt ist, werden alle geöffneten OneNote-Notizbücher, die mit der Konferenz verknüpft sind, automatisch mit Informationen wie Konferenzteilnehmern und Details zu den während der Konferenz freigegebenen Inhalten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-136">When set to True (the default value) any open OneNote notebooks linked to the conference will automatically be updated with information such as conference participants and details about content shared during the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-137">EnableInviteCustomization</span><span class="sxs-lookup"><span data-stu-id="cb3c2-137">EnableInviteCustomization</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-138">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb3c2-138">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-139">Wird zusammen mit den anderen neuen CsMeetingConfiguration-Parametern verwendet, um die vom Online Besprechungs-Add-in für lync 2013 generierten Besprechungseinladungen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-139">Used along with the other new CsMeetingConfiguration parameters to customize the meeting invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-140">LogoURL</span><span class="sxs-lookup"><span data-stu-id="cb3c2-140">LogoURL</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-141">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb3c2-141">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-142">Fügt dem Logo Ihrer Organisation alle Einladungen hinzu, die vom Online Besprechungs-Add-in für lync 2013 generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-142">Adds your organization’s logo to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="cb3c2-143">Sie geben die URL eines GIF-oder JPG-Bilds an.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-143">You specify the URL of a GIF or JPG image.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-144">HelpUrl</span><span class="sxs-lookup"><span data-stu-id="cb3c2-144">HelpURL</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-145">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb3c2-145">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-146">Fügt die Hilfe-oder Support-URL Ihrer Organisation zu allen Einladungen hinzu, die vom Online Besprechungs-Add-in für lync 2013 generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-146">Adds your organization’s help or support URL to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-147">LegalURL</span><span class="sxs-lookup"><span data-stu-id="cb3c2-147">LegalURL</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-148">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb3c2-148">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-149">Fügt allen Einladungen, die vom Online Besprechungs-Add-in für lync 2013 generiert wurden, juristischen Text oder Verzichts Text hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-149">Adds legal text or disclaimer text to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="cb3c2-150">Sie geben die URL für den Speicherort des Texts an.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-150">You specify the URL for the location of the text.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-151">CustomFooterText</span><span class="sxs-lookup"><span data-stu-id="cb3c2-151">CustomFooterText</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-152">CsMeetingConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb3c2-152">CsMeetingConfiguration</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-153">Fügt allen Einladungen, die vom Online Besprechungs-Add-in für lync 2013 generiert wurden, eine benutzerdefinierte Fußzeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-153">Adds a custom footer to all invitations generated by the Online Meeting Add-in for Lync 2013.</span></span> <span data-ttu-id="cb3c2-154">Sie geben die URL für den Speicherort des benutzerdefinierten Fußzeilentexts an.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-154">You specify the URL for the location of the custom footer text.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="deprecated-client-management-parameters"></a><span data-ttu-id="cb3c2-155">Veraltete Client Verwaltungsparameter</span><span class="sxs-lookup"><span data-stu-id="cb3c2-155">Deprecated Client Management Parameters</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb3c2-156">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb3c2-156">Parameter</span></span></th>
<th><span data-ttu-id="cb3c2-157">Cmdlet "lync Server-Verwaltungsshell"</span><span class="sxs-lookup"><span data-stu-id="cb3c2-157">Lync Server Management Shell Cmdlet</span></span></th>
<th><span data-ttu-id="cb3c2-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb3c2-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-159">CustomizedHelpUrl</span><span class="sxs-lookup"><span data-stu-id="cb3c2-159">CustomizedHelpUrl</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-160">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-160">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-161">Dieser Parameter wurde für die Verwendung mit lync Server 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-161">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="cb3c2-162">Bei Verwendung in Verbindung mit EnableEnterpriseCustomizedHelp ermöglicht dieser Parameter einer Organisation, eine URL anzugeben, damit Benutzer, die auf das Menü "Hilfe" in lync geklickt haben, eine angepasste Hilfe anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-162">When used in conjunction with EnableEnterpriseCustomizedHelp, this parameter enabled an organization to specify a URL so that when users clicked the Help menu in Lync, customized help would display.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-163">EnableEnterpriseCustomizedHelp</span><span class="sxs-lookup"><span data-stu-id="cb3c2-163">EnableEnterpriseCustomizedHelp</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-164">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-164">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-165">Dieser Parameter wurde für die Verwendung mit lync Server 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-165">This parameter has been deprecated for use with Lync Server 2013.</span></span> <span data-ttu-id="cb3c2-166">Wenn dieser Parameter in Verbindung mit CustomizedHelpUrl verwendet wird, konnten Organisationen angepasste Hilfe anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-166">When used in conjunction with CustomizedHelpUrl, this parameter enabled organizations to display customized help.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-167">EnableSQMData</span><span class="sxs-lookup"><span data-stu-id="cb3c2-167">EnableSQMData</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-168">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-168">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-169">Der EnableSQMData-Parameter des Set-CSClientPolicy-Cmdlets wurde in lync Server 2013 entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-169">The EnableSQMData parameter of the Set-CSClientPolicy cmdlet has been removed in Lync Server 2013.</span></span> <span data-ttu-id="cb3c2-170">Stattdessen können Sie die freigegebene Gruppenrichtlinieneinstellung für Software Quality Management (qm)-Daten verwenden, um die Benutzeroberfläche für die Option zur Verbesserung der Benutzerfreundlichkeit auf der Seite lync-Client-allgemeine Optionen zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="cb3c2-170">Instead, you can use the shared Group Policy setting for Software Quality Management (SQM) data to determine the user interface for the Customer Experience Improvement option in the Lync client General options page:</span></span></p>
<p><span data-ttu-id="cb3c2-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span><span class="sxs-lookup"><span data-stu-id="cb3c2-171">HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Common\QMEnable</span></span></p>
<p><span data-ttu-id="cb3c2-172">Werte</span><span class="sxs-lookup"><span data-stu-id="cb3c2-172">Values:</span></span></p>
<p><span data-ttu-id="cb3c2-173">1 = Anzeige und Aktivieren des Kontrollkästchens (der Benutzer kann das Kontrollkästchen deaktivieren)</span><span class="sxs-lookup"><span data-stu-id="cb3c2-173">1 = Display and select the check box (the user can clear the check box)</span></span></p>
<p><span data-ttu-id="cb3c2-174">0 = deaktivieren und Deaktivieren des Kontrollkästchens (Benutzer können nicht überschreiben)</span><span class="sxs-lookup"><span data-stu-id="cb3c2-174">0 = Turn off and disable the check box (user can't override)</span></span></p>
<p><span data-ttu-id="cb3c2-175">NULL = der Wert wird durch das Office-Setup festgelegt, und das Kontrollkästchen wird angezeigt, damit die Benutzer Ihre Auswahl treffen können.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-175">Null = The value is determined by Office setup, and the check box is displayed for users to set as they choose</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-176">AllowExchangeContactStore</span><span class="sxs-lookup"><span data-stu-id="cb3c2-176">AllowExchangeContactStore</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-177">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-177">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-178">Dieser Parameter wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-178">This parameter has been removed.</span></span> <span data-ttu-id="cb3c2-179">Wenn Sie stattdessen lync Server 2013 bereitstellen und die Topologie veröffentlichen, ist der Unified Contact Store standardmäßig für alle Benutzer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-179">Instead, when you deploy Lync Server 2013 and publish the topology, unified contact store is enabled for all users by default.</span></span> <span data-ttu-id="cb3c2-180">Dies bedeutet, dass alle Kontakte eines Benutzers in Exchange aufbewahrt werden und in lync, Outlook und Outlook Web Access zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-180">This means that all a user’s contacts are kept in Exchange and are available in Lync, Outlook, and Outlook Web Access.</span></span> <span data-ttu-id="cb3c2-181">Sie können das Set-CsUserServicesPolicy-Cmdlet verwenden, um die verfügbaren Unified Contact Store-Benutzer anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-181">You can use the Set-CsUserServicesPolicy cmdlet to customize which users have unified contact store available.</span></span> <span data-ttu-id="cb3c2-182">Sie können Benutzer Global, nach Website, nach Mandanten oder nach Einzelpersonen oder Gruppen von Personen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-182">You can enable users globally, by site, by tenant, or by individuals or groups of individuals.</span></span> <span data-ttu-id="cb3c2-183">Ausführliche Informationen finden Sie unter <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Aktivieren von Benutzern für den Unified Contact Store in lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-183">For details, see <a href="lync-server-2013-enable-users-for-unified-contact-store.md">Enable users for unified contact store in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3c2-184">MAPIPollInterval</span><span class="sxs-lookup"><span data-stu-id="cb3c2-184">MAPIPollInterval</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-185">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-185">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-186">Dieser Parameter wird von lync 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-186">This parameter is not used by Lync 2013.</span></span> <span data-ttu-id="cb3c2-187">In früheren Versionen hat dieser Parameter angegeben, wie oft der Client MAPI-Daten aus öffentlichen Exchange-Ordnern abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-187">In previous releases, this parameter specified how often the client retrieved MAPI data from Exchange public folders</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3c2-188">DisableICE</span><span class="sxs-lookup"><span data-stu-id="cb3c2-188">DisableICE</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-189">CsClientPolicy</span><span class="sxs-lookup"><span data-stu-id="cb3c2-189">CsClientPolicy</span></span></p></td>
<td><p><span data-ttu-id="cb3c2-190">Dieser Parameter war in lync 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-190">This parameter was deprecated in Lync 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cb3c2-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb3c2-191">


</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

