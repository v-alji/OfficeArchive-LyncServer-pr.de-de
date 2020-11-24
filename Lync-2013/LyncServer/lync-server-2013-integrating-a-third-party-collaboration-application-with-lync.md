---
title: Integrieren einer Drittanbieter-Zusammenarbeitsanwendung in lync
description: Integrieren einer Drittanbieter-Zusammenarbeitsanwendung in lync
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Integrating a third-party collaboration application with Lync
ms:assetid: 00b9312c-b0c8-4f79-8b76-05b2d820e197
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398068(v=OCS.15)
ms:contentKeyID: 48183224
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7adbe1abab83a569f581af034fc46abfef4cf819
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395094"
---
# <a name="integrating-a-third-party-collaboration-application-with-lync-server-2013"></a><span data-ttu-id="bf754-103">Integrieren einer Drittanbieter-Zusammenarbeitsanwendung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf754-103">Integrating a third-party collaboration application with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf754-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf754-104">

<span> </span></span></span>

<span data-ttu-id="bf754-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="bf754-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="bf754-106">Sie können lync 2013 in eine beliebige Anwendung für die Online Zusammenarbeit von Drittanbietern integrieren, indem Sie der Registrierung Informationen zur Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf754-106">You can integrate Lync 2013 with any third-party online collaboration application by adding information about the application to the registry.</span></span> <span data-ttu-id="bf754-107">Sie können lync 2013 verwenden, um Datenkonferenz Sitzungen zu starten, die auf einem internen Server, einem Internet basierten Dienst oder in beiden gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="bf754-107">You can use Lync 2013 to start data conferencing sessions hosted on an in-house server, an Internet-based service, or both.</span></span> <span data-ttu-id="bf754-108">Die Zusammenarbeits-oder Datenkonferenz Sitzung kann über die Kontaktliste oder über eine vorhandene Chat-, sprach-oder Videositzung gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="bf754-108">The collaboration or data conferencing session can be started from the Contacts list or from an existing instant messaging, voice, or video session.</span></span> <span data-ttu-id="bf754-109">Lync 2013 fungiert nur als Vehikel für das Starten der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bf754-109">Lync 2013 acts only as the vehicle for starting the application.</span></span> <span data-ttu-id="bf754-110">Alle vorhandenen lync 2013-Unterhaltungen bleiben nach Beginn der Online Zusammenarbeitssitzung aktiv.</span><span class="sxs-lookup"><span data-stu-id="bf754-110">Any existing Lync 2013 conversations remain active after the online collaboration session has begun.</span></span>

<span data-ttu-id="bf754-111">In den folgenden Abschnitten wird beschrieben, wie Sie lync 2013 mit Internet basierten und Server basierten Zusammenarbeitsanwendungen integrieren.</span><span class="sxs-lookup"><span data-stu-id="bf754-111">The following sections describe how to integrate Lync 2013 with Internet-based and server-based collaboration applications.</span></span>

<div>

## <a name="integrating-an-internet-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="bf754-112">Integrieren einer Internet-Based Zusammenarbeitsanwendung in lync 2013</span><span class="sxs-lookup"><span data-stu-id="bf754-112">Integrating an Internet-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="bf754-113">Im Allgemeinen sind die Schritte, die für die Integration einer Drittanbieter-Zusammenarbeitsanwendung erforderlich sind, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf754-113">Generally, the steps involved in integrating a third-party collaboration application are as follows:</span></span>

1.  <span data-ttu-id="bf754-114">Der Registrierung werden Informationen zur Anwendung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bf754-114">Information about the application is added to the registry.</span></span>

2.  <span data-ttu-id="bf754-115">Der Organisator meldet sich bei lync 2013 an und wählt Kontakte für die Datenfreigabe und Zusammenarbeit aus.</span><span class="sxs-lookup"><span data-stu-id="bf754-115">The organizer signs in to Lync 2013 and selects contacts for data sharing and collaboration.</span></span> <span data-ttu-id="bf754-116">Oder der Organisator befindet sich möglicherweise bereits in einer Unterhaltung und entscheidet sich, Datenkonferenzen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf754-116">Or, the organizer may already be in a conversation and decide to add data conferencing.</span></span>

3.  <span data-ttu-id="bf754-117">Lync 2013 liest die Registrierung, startet die Zusammenarbeitsanwendung und sendet dann eine benutzerdefinierte SIP-Nachricht – eine appINVITE – an die ausgewählten Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="bf754-117">Lync 2013 reads the registry, starts the collaboration application, and then sends a custom SIP message—an appINVITE—to the selected participants.</span></span>

4.  <span data-ttu-id="bf754-118">Die Teilnehmer akzeptieren die Einladung, und die Zusammenarbeitsanwendung wird auf dem Computer jeder Person gestartet.</span><span class="sxs-lookup"><span data-stu-id="bf754-118">Participants accept the invitation, and the collaboration application is started on each person’s computer.</span></span> <span data-ttu-id="bf754-119">Lync 2013 verwendet die Registrierung, um zu ermitteln, welche Zusammenarbeitsanwendung verwendet werden soll, und startet dann die Anwendung mithilfe der Parameter, die in der appINVITE-Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bf754-119">Lync 2013 uses the registry to determine which collaboration application to use, and then starts that application by using the parameters included in the appINVITE message.</span></span>

<span data-ttu-id="bf754-120">In der folgenden Tabelle werden die Registrierungseinträge beschrieben, die für die Integration einer Internet basierten Zusammenarbeitsanwendung in lync 2013 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bf754-120">The following table describes the registry entries required to integrate an Internet-based collaboration application with Lync 2013.</span></span> <span data-ttu-id="bf754-121">Diese Einträge werden in der Registrierung an folgendem Speicherort gespeichert:</span><span class="sxs-lookup"><span data-stu-id="bf754-121">These entries are placed in the registry in the following location:</span></span>

  - <span data-ttu-id="bf754-122">HKEY \_ - \_ Software für lokale Computer \\ \\ Microsoft \\ Office \\ 15,0 \\ lync \\ SessionManager-apps- \\ \\ Parameter</span><span class="sxs-lookup"><span data-stu-id="bf754-122">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="bf754-123">Registrierungseinträge für eine Internet basierte Zusammenarbeitsanwendung</span><span class="sxs-lookup"><span data-stu-id="bf754-123">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf754-124">Name</span><span class="sxs-lookup"><span data-stu-id="bf754-124">Name</span></span></th>
<th><span data-ttu-id="bf754-125">Typ</span><span class="sxs-lookup"><span data-stu-id="bf754-125">Type</span></span></th>
<th><span data-ttu-id="bf754-126">Daten</span><span class="sxs-lookup"><span data-stu-id="bf754-126">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf754-127">Name</span><span class="sxs-lookup"><span data-stu-id="bf754-127">Name</span></span></p></td>
<td><p><span data-ttu-id="bf754-128">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-128">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-129">Der Anwendungsname für lync 2013-Menüs.</span><span class="sxs-lookup"><span data-stu-id="bf754-129">The application name for Lync 2013 menus.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-130">SmallIcon</span><span class="sxs-lookup"><span data-stu-id="bf754-130">SmallIcon</span></span></p></td>
<td><p><span data-ttu-id="bf754-131">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-131">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-132">Pfad zu 16 Pixel x 16-Pixel-Symbol, BMP oder PNG.</span><span class="sxs-lookup"><span data-stu-id="bf754-132">Path to 16-pixel x 16-pixel icon, BMP or PNG.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf754-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="bf754-133">Path</span></span></p></td>
<td><p><span data-ttu-id="bf754-134">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-134">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-135">Teilnehmerpfad zum Starten der Anwendung für die Online Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="bf754-135">Participant path for starting the online collaboration application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-136">OriginatorPath</span><span class="sxs-lookup"><span data-stu-id="bf754-136">OriginatorPath</span></span></p></td>
<td><p><span data-ttu-id="bf754-137">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-137">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-138">Organizer-Pfad zum Starten der Anwendung für die Online Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="bf754-138">Organizer path for starting the online collaboration application.</span></span> <span data-ttu-id="bf754-139">Dieser Pfad kann einen oder mehrere benutzerdefinierte Parameter enthalten, die im Unterschlüssel Parameters definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf754-139">This path can contain one or more custom parameters as defined in the Parameters subkey.</span></span> <span data-ttu-id="bf754-140">Zum Beispiel <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span><span class="sxs-lookup"><span data-stu-id="bf754-140">For example, <code>https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&amp;role=present&amp;pw=%param3%</code></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf754-141">SessionType</span><span class="sxs-lookup"><span data-stu-id="bf754-141">SessionType</span></span></p></td>
<td><p><span data-ttu-id="bf754-142">DWORD</span><span class="sxs-lookup"><span data-stu-id="bf754-142">DWORD</span></span></p></td>
<td><p><span data-ttu-id="bf754-143">0 = lokale Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bf754-143">0 = Local session.</span></span> <span data-ttu-id="bf754-144">Die Anwendung wird auf dem lokalen Computer gestartet.</span><span class="sxs-lookup"><span data-stu-id="bf754-144">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="bf754-145">1 = Sitzung mit zwei Teilnehmern (Standard).</span><span class="sxs-lookup"><span data-stu-id="bf754-145">1 = Two-party session (default).</span></span> <span data-ttu-id="bf754-146">Lync 2013 startet die Anwendung lokal und sendet dann eine Systembenachrichtigung an den anderen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bf754-146">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="bf754-147">Der andere Benutzer klickt auf die Benachrichtigung und startet die angegebene Anwendung auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="bf754-147">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="bf754-148">2 = mehrteilige Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bf754-148">2 = Multiparty session.</span></span> <span data-ttu-id="bf754-149">Lync 2013 startet die Anwendung lokal und sendet dann System Benachrichtigungen an die anderen Benutzer und fordert Sie auf, die angegebene Anwendung auf Ihrem eigenen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="bf754-149">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their own computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-150">ExensibleMenu</span><span class="sxs-lookup"><span data-stu-id="bf754-150">ExensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="bf754-151">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-151">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-152">Eine Liste der Menüs, in denen dieser Befehl angezeigt wird, getrennt durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="bf754-152">A list of the menus where this command will appear, separated by semi-colons.</span></span> <span data-ttu-id="bf754-153">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="bf754-153">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="bf754-154">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="bf754-154">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="bf754-155">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="bf754-155">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="bf754-156">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="bf754-156">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="bf754-157">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="bf754-157">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="bf754-158">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="bf754-158">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="bf754-159">Wenn ExtensibleMenu nicht definiert ist, werden die Standardwerte MainWindowRightClick und ConversationWindowActions verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf754-159">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf754-160">In der folgenden Tabelle werden die Registrierungseinträge für Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bf754-160">The following table describes the registry entries for parameters.</span></span> <span data-ttu-id="bf754-161">Diese Einträge finden Sie unter HKEY \_ aktuelle \_ Benutzer \\ Software \\ Microsoft \\ Office \\ 15,0 \\ lync \\ SessionManager \\ \\ -apps-Parameter.</span><span class="sxs-lookup"><span data-stu-id="bf754-161">These entries are place at HKEY\_CURRENT\_USER\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters.</span></span>

### <a name="registry-entries-for-an-internet-based-collaboration-application"></a><span data-ttu-id="bf754-162">Registrierungseinträge für eine Internet basierte Zusammenarbeitsanwendung</span><span class="sxs-lookup"><span data-stu-id="bf754-162">Registry Entries for an Internet-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf754-163">Name</span><span class="sxs-lookup"><span data-stu-id="bf754-163">Name</span></span></th>
<th><span data-ttu-id="bf754-164">Typ</span><span class="sxs-lookup"><span data-stu-id="bf754-164">Type</span></span></th>
<th><span data-ttu-id="bf754-165">Daten</span><span class="sxs-lookup"><span data-stu-id="bf754-165">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf754-166">Parameter1</span><span class="sxs-lookup"><span data-stu-id="bf754-166">Param1</span></span></p></td>
<td><p><span data-ttu-id="bf754-167">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-167">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-168">Wird in tokenformat ( <code>%Parm1%</code> ) verwendet, um dem Registrierungsschlüssel OriginatorPath benutzerspezifische Werte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bf754-168">Used in tokenized format (<code>%Parm1%</code>) to add user-specific values to the OriginatorPath registry key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-169">Parameter2</span><span class="sxs-lookup"><span data-stu-id="bf754-169">Param2</span></span></p></td>
<td><p><span data-ttu-id="bf754-170">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-170">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-171">Siehe parameter1.</span><span class="sxs-lookup"><span data-stu-id="bf754-171">See Param1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf754-172">Param3</span><span class="sxs-lookup"><span data-stu-id="bf754-172">Param3</span></span></p></td>
<td><p><span data-ttu-id="bf754-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-174">Siehe parameter1.</span><span class="sxs-lookup"><span data-stu-id="bf754-174">See Param1.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf754-175">Die folgenden Beispiel Registrierungseinstellungen integrieren den Adatum-Zusammenarbeits Client in lync 2013:</span><span class="sxs-lookup"><span data-stu-id="bf754-175">The following example registry settings integrate ADatum Collaboration Client with Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Path"="https://meetingservice.adatum.com/cc/%param1%/meet/%param2%"
    "OriginatorPath"="https://meetserv.adatum.com/cc/%param1%/join?id=%param2%&role=present&pw=%param3%"
    "SessionType"=dword:00000002
    "ApplicationType"=dword:00000001
    "LiveServerIntegration"=dword:00000000
    "Name"="ADatum Online Collaboration Service"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"
    
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters]
    [HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\Lync\SessionManager\Apps\Parameters\{C3F6E17A-855F-44a0-B90D-C0B92D38E5F1}]
    "Param1"="meetserv"
    "Param2"="admin"
    "Param3"="abcdefg123"

</div>

<div>

## <a name="integrating-a-server-based-collaboration-application-with-lync-2013"></a><span data-ttu-id="bf754-176">Integrieren einer Server-Based Zusammenarbeitsanwendung in lync 2013</span><span class="sxs-lookup"><span data-stu-id="bf754-176">Integrating a Server-Based Collaboration Application with Lync 2013</span></span>

<span data-ttu-id="bf754-177">Die Einstellungen zum Hinzufügen von Befehlen zum Starten einer Server basierten Zusammenarbeitsanwendung innerhalb von lync 2013 ähneln den im vorherigen Abschnitt beschriebenen Funktionen zum Integrieren einer Internet-Based Zusammenarbeitsanwendung in lync 2013.</span><span class="sxs-lookup"><span data-stu-id="bf754-177">The settings to add commands for starting a server-based collaboration application from within Lync 2013 are similar to those described in the previous section, Integrating an Internet-Based Collaboration Application with Lync 2013.</span></span> <span data-ttu-id="bf754-178">Die OriginatorPath ist jedoch nicht erforderlich, und einige Werte werden geändert.</span><span class="sxs-lookup"><span data-stu-id="bf754-178">However, the OriginatorPath is not required, and some values are changed.</span></span> <span data-ttu-id="bf754-179">Registrierungseinträge werden an folgendem Speicherort gespeichert:</span><span class="sxs-lookup"><span data-stu-id="bf754-179">Registry entries are placed in the following location:</span></span>

  - <span data-ttu-id="bf754-180">HKEY \_ - \_ Software für lokale Computer \\ \\ Microsoft \\ Office \\ 15,0 \\ lync \\ SessionManager-apps- \\ \\ Parameter</span><span class="sxs-lookup"><span data-stu-id="bf754-180">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Office\\15.0\\Lync\\SessionManager\\Apps\\Parameters</span></span>

### <a name="registry-entries-for-a-server-based-collaboration-application"></a><span data-ttu-id="bf754-181">Registrierungseinträge für eine Server basierte Zusammenarbeitsanwendung</span><span class="sxs-lookup"><span data-stu-id="bf754-181">Registry Entries for a Server-based Collaboration Application</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf754-182">Name</span><span class="sxs-lookup"><span data-stu-id="bf754-182">Name</span></span></th>
<th><span data-ttu-id="bf754-183">Typ</span><span class="sxs-lookup"><span data-stu-id="bf754-183">Type</span></span></th>
<th><span data-ttu-id="bf754-184">Daten</span><span class="sxs-lookup"><span data-stu-id="bf754-184">Data</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf754-185">Name</span><span class="sxs-lookup"><span data-stu-id="bf754-185">Name</span></span></p></td>
<td><p><span data-ttu-id="bf754-186">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-186">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-187">Der Name der Anwendung, wie er im Menü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bf754-187">Name of the application as it appears on the menu.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-188">Applicationtype</span><span class="sxs-lookup"><span data-stu-id="bf754-188">ApplicationType</span></span></p></td>
<td><p><span data-ttu-id="bf754-189">DWORD</span><span class="sxs-lookup"><span data-stu-id="bf754-189">DWORD</span></span></p></td>
<td><p><span data-ttu-id="bf754-190">Wert = 1.</span><span class="sxs-lookup"><span data-stu-id="bf754-190">Value = 1.</span></span> <span data-ttu-id="bf754-191">Legt den Anwendungstyp auf Protocol fest.</span><span class="sxs-lookup"><span data-stu-id="bf754-191">Sets the application type to protocol.</span></span> <span data-ttu-id="bf754-192">In diesem Fall gelten die anderen möglichen Werte nicht.</span><span class="sxs-lookup"><span data-stu-id="bf754-192">The other possible values do not apply in this case.</span></span> <span data-ttu-id="bf754-193">Wenn es nicht vorhanden ist, wird applicationtype auf 0 (ausführbare Datei) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="bf754-193">If not present, ApplicationType is set to 0 (executable).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf754-194">Pfad</span><span class="sxs-lookup"><span data-stu-id="bf754-194">Path</span></span></p></td>
<td><p><span data-ttu-id="bf754-195">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-195">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-196">Das Protokoll, das zum Starten der Zusammenarbeitsanwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf754-196">Protocol used to start the collaboration application.</span></span> <span data-ttu-id="bf754-197">Für Live Meeting 2007 ist der Wert von Path auf gesetzt <code>meet:%conf-uri%</code> .</span><span class="sxs-lookup"><span data-stu-id="bf754-197">For Live Meeting 2007, the value of Path is set to <code>meet:%conf-uri%</code>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-198">SessionType</span><span class="sxs-lookup"><span data-stu-id="bf754-198">SessionType</span></span></p></td>
<td><p><span data-ttu-id="bf754-199">DWORD</span><span class="sxs-lookup"><span data-stu-id="bf754-199">DWORD</span></span></p></td>
<td><p><span data-ttu-id="bf754-200">0 = lokale Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bf754-200">0 = Local session.</span></span> <span data-ttu-id="bf754-201">Die Anwendung wird auf dem lokalen Computer gestartet.</span><span class="sxs-lookup"><span data-stu-id="bf754-201">The application is started on the local computer.</span></span></p>
<p><span data-ttu-id="bf754-202">1 = Sitzung mit zwei Teilnehmern (Standard).</span><span class="sxs-lookup"><span data-stu-id="bf754-202">1 = Two-party session (default).</span></span> <span data-ttu-id="bf754-203">Lync 2013 startet die Anwendung lokal und sendet dann eine Systembenachrichtigung an den anderen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bf754-203">Lync 2013 starts the application locally, and then sends a system notification to the other user.</span></span> <span data-ttu-id="bf754-204">Der andere Benutzer klickt auf die Benachrichtigung und startet die angegebene Anwendung auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="bf754-204">The other user clicks the notification and starts the specified application on their computer.</span></span></p>
<p><span data-ttu-id="bf754-205">2 = mehrteilige Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bf754-205">2 = Multiparty session.</span></span> <span data-ttu-id="bf754-206">Lync 2013 startet die Anwendung lokal und sendet dann System Benachrichtigungen an die anderen Benutzer und fordert Sie auf, die angegebene Anwendung auf Ihrem Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="bf754-206">Lync 2013 starts the application locally, and then sends system notifications to the other users, prompting them to start the specified application on their computer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf754-207">MCUType</span><span class="sxs-lookup"><span data-stu-id="bf754-207">MCUType</span></span></p></td>
<td><p><span data-ttu-id="bf754-208">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-208">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-209">Data = der Servertyp.</span><span class="sxs-lookup"><span data-stu-id="bf754-209">DATA = The type of server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf754-210">ExtensibleMenu</span><span class="sxs-lookup"><span data-stu-id="bf754-210">ExtensibleMenu</span></span></p></td>
<td><p><span data-ttu-id="bf754-211">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bf754-211">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bf754-212">Eine Liste der Menüs, in denen dieser Befehl angezeigt wird, getrennt durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="bf754-212">A list of the menus where this command will appear, separated by semicolons.</span></span> <span data-ttu-id="bf754-213">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="bf754-213">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="bf754-214">MainWindowActions</span><span class="sxs-lookup"><span data-stu-id="bf754-214">MainWindowActions</span></span></p></li>
<li><p><span data-ttu-id="bf754-215">MainWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="bf754-215">MainWindowRightClick</span></span></p></li>
<li><p><span data-ttu-id="bf754-216">ConversationWindowActions</span><span class="sxs-lookup"><span data-stu-id="bf754-216">ConversationWindowActions</span></span></p></li>
<li><p><span data-ttu-id="bf754-217">ConversationWindowButton</span><span class="sxs-lookup"><span data-stu-id="bf754-217">ConversationWindowButton</span></span></p></li>
<li><p><span data-ttu-id="bf754-218">ConversationWindowRightClick</span><span class="sxs-lookup"><span data-stu-id="bf754-218">ConversationWindowRightClick</span></span></p></li>
</ul>
<p><span data-ttu-id="bf754-219">Wenn ExtensibleMenu nicht definiert ist, werden die Standardwerte MainWindowRightClick und ConversationWindowActions verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf754-219">If ExtensibleMenu is not defined, the default values of MainWindowRightClick and ConversationWindowActions are used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf754-220">Im folgenden Beispiel werden Befehle zum Starten des Adatum-Zusammenarbeits Clients in lync 2013 hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bf754-220">The following example adds commands to start ADatum Collaboration Client from within Lync 2013:</span></span>

    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps]
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Lync\SessionManager\Apps\{27877e66-615c-4582-ab88-0cb2ca05d951}]
    "Path"="meet:%conf-uri%"
    "SessionType"=dword:00000002
    "LiveServerIntegration"=dword:00000001
    "ApplicationType"=dword:00000001
    "Name"="ADatum Collaboration Client"
    "MCUType"="Data"
    "Extensiblemenu"="MainWindowActions;MainWindowRightClick;ConversationWindowActions;ConversationWindowRightClick"

<span data-ttu-id="bf754-221"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf754-221"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

