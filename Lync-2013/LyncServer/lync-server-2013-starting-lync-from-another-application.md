---
title: 'Lync Server 2013: Starten von lync aus einer anderen Anwendung'
description: 'Lync Server 2013: Starten von lync aus einer anderen Anwendung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Starting Lync from another application
ms:assetid: 573b30b1-6590-4b24-8e96-a41be57cb0ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398376(v=OCS.15)
ms:contentKeyID: 48184184
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd64b8b9f335638b54a0bf6473b5d159c97a0e7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393947"
---
# <a name="starting-lync-from-another-application"></a><span data-ttu-id="d34cf-103">Starten von lync aus einer anderen Anwendung</span><span class="sxs-lookup"><span data-stu-id="d34cf-103">Starting Lync from another application</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d34cf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d34cf-104">

<span> </span></span></span>

<span data-ttu-id="d34cf-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="d34cf-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="d34cf-106">Sie können Befehlszeilenparameter verwenden, um lync 2013 schnell zu starten.</span><span class="sxs-lookup"><span data-stu-id="d34cf-106">You can use command-line parameters to quick-start Lync 2013.</span></span> <span data-ttu-id="d34cf-107">Wenn ein Benutzer beispielsweise in einer anderen Anwendung auf eine Telefonnummer klickt, kann die Anwendung eine Instanz von lync 2013 starten und einen Anruf an diese Nummer initiieren.</span><span class="sxs-lookup"><span data-stu-id="d34cf-107">For example, if a user clicks a phone number in another application, the application can start an instance of Lync 2013 and initiate a call to that number.</span></span>

<span data-ttu-id="d34cf-108">Lync 2013 kann auch eine durch Semikolons getrennte Liste der Kontaktnamen für mehrteilige Konferenzen erkennen.</span><span class="sxs-lookup"><span data-stu-id="d34cf-108">Lync 2013 can also recognize a semicolon-delimited list of contact names for multiparty conferencing.</span></span>

<span data-ttu-id="d34cf-109">Wenn lync 2013 so konfiguriert ist, dass die Anmeldung beim Start automatisch erfolgt, wird beim Starten von lync 2013 mit Befehlszeilenparametern das lync-Hauptfenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d34cf-109">If Lync 2013 is configured to automatically sign in when started, then starting Lync 2013 with command-line parameters will open the Lync main window.</span></span> <span data-ttu-id="d34cf-110">Wenn lync nicht so konfiguriert ist, dass sich beim Start automatisch anmelden, wird das Anmeldefenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d34cf-110">If Lync is not configured to automatically sign in when started, the sign-in window opens.</span></span>

<span data-ttu-id="d34cf-111">In der folgenden Tabelle sind die verfügbaren Parameter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d34cf-111">The following table shows the available parameters.</span></span>

### <a name="lync-2013-command-line-parameters"></a><span data-ttu-id="d34cf-112">Lync 2013 Command-Line-Parameter</span><span class="sxs-lookup"><span data-stu-id="d34cf-112">Lync 2013 Command-Line Parameters</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d34cf-113">Erweiterung</span><span class="sxs-lookup"><span data-stu-id="d34cf-113">Extension</span></span></th>
<th><span data-ttu-id="d34cf-114">Format der Daten</span><span class="sxs-lookup"><span data-stu-id="d34cf-114">Format of Data</span></span></th>
<th><span data-ttu-id="d34cf-115">Aktion</span><span class="sxs-lookup"><span data-stu-id="d34cf-115">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-116">Tel</span><span class="sxs-lookup"><span data-stu-id="d34cf-116">tel:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-117">Tel-URI</span><span class="sxs-lookup"><span data-stu-id="d34cf-117">tel URI</span></span></p></td>
<td><p><span data-ttu-id="d34cf-118">Öffnet das Unterhaltungsfenster für einen Audioanruf, wählt aber nicht die angegebene Nummer.</span><span class="sxs-lookup"><span data-stu-id="d34cf-118">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d34cf-119">callto</span><span class="sxs-lookup"><span data-stu-id="d34cf-119">callto:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-120">Tel:, SIP: oder Typ Tel-URI</span><span class="sxs-lookup"><span data-stu-id="d34cf-120">tel:, sip:, or typeable tel URI</span></span></p></td>
<td><p><span data-ttu-id="d34cf-121">Öffnet das Unterhaltungsfenster für einen Audioanruf, wählt aber nicht die angegebene Nummer.</span><span class="sxs-lookup"><span data-stu-id="d34cf-121">Opens the Conversation window for an audio call but does not dial the specified number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-122">SIP</span><span class="sxs-lookup"><span data-stu-id="d34cf-122">sip:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-123">SIP-URI</span><span class="sxs-lookup"><span data-stu-id="d34cf-123">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="d34cf-124">Öffnet das Unterhaltungsfenster mit dem angegebenen SIP-URI (Uniform Resource Identifier) in der Teilnehmerliste.</span><span class="sxs-lookup"><span data-stu-id="d34cf-124">Opens the Conversation window with the specified SIP Uniform Resource Identifier (URI) in the participant list.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d34cf-125">SIPs</span><span class="sxs-lookup"><span data-stu-id="d34cf-125">Sips:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-126">SIP-URI</span><span class="sxs-lookup"><span data-stu-id="d34cf-126">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="d34cf-127">Wenn lync 2013 für die Verwendung des TLS-Protokolls (Transport Layer Security) konfiguriert ist, funktioniert genau wie SIP:.</span><span class="sxs-lookup"><span data-stu-id="d34cf-127">If Lync 2013 is configured to use the Transport Layer Security (TLS) protocol, functions exactly like sip:.</span></span> <span data-ttu-id="d34cf-128">Wenn TLS nicht verwendet wird, wird ein Dialogfeld angezeigt, in dem der Benutzer informiert wird, dass eine höhere Sicherheitsstufe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d34cf-128">If TLS is not being used, displays a dialog box informing the user that a higher level of security is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-129">conf</span><span class="sxs-lookup"><span data-stu-id="d34cf-129">conf:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-130">SIP-URI der Konferenz, an der Sie teilnehmen möchten</span><span class="sxs-lookup"><span data-stu-id="d34cf-130">SIP URI of conference to join</span></span></p></td>
<td><p><span data-ttu-id="d34cf-131">Wenn URI selbst ist, wird der Fokus instanziiert, und es wird eine Liste mit nur einer Rost geschützten Ansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d34cf-131">If URI is self, instantiates the focus and brings up roster-only view.</span></span> <span data-ttu-id="d34cf-132">Andernfalls wird die Liste der Teilnehmer angezeigt, aber die Einladung wird nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="d34cf-132">Otherwise, brings up roster view but does not send INVITE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d34cf-133">Chat</span><span class="sxs-lookup"><span data-stu-id="d34cf-133">im:</span></span></p></td>
<td><p><span data-ttu-id="d34cf-134">SIP-URI</span><span class="sxs-lookup"><span data-stu-id="d34cf-134">SIP URI</span></span></p></td>
<td><p><span data-ttu-id="d34cf-135">Zeigt ein Chat-Fenster mit dem SIP-URI an.</span><span class="sxs-lookup"><span data-stu-id="d34cf-135">Displays an instant messaging (IM)-only Conversation window with the SIP URI.</span></span> <span data-ttu-id="d34cf-136">Akzeptiert mehrere SIP-URIs, die in Spitze Klammern ( &lt; &gt; ) ohne Trennzeichen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d34cf-136">Accepts multiple SIP URIs specified inside angle brackets (&lt;&gt;) without any separator.</span></span></p>
<pre><code>im:&lt;sip:user1@host&gt;&lt;sip:user2@host&gt;</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d34cf-137">Die folgende Tabelle enthält Beispiele für diese Befehlszeilenparameter.</span><span class="sxs-lookup"><span data-stu-id="d34cf-137">The following table provides examples of these command-line parameters.</span></span>

### <a name="command-line-parameter-examples"></a><span data-ttu-id="d34cf-138">Beispiele für Command-Line Parameter</span><span class="sxs-lookup"><span data-stu-id="d34cf-138">Command-Line Parameter Examples</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d34cf-139">Instanz</span><span class="sxs-lookup"><span data-stu-id="d34cf-139">Instance</span></span></th>
<th><span data-ttu-id="d34cf-140">Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="d34cf-140">Results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-141">Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="d34cf-141">Tel:+14255550101</span></span></p></td>
<td><p><span data-ttu-id="d34cf-142">Öffnet eine nur-Telefon-Ansicht mit + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="d34cf-142">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d34cf-143">Callto: Tel: + 14255550101</span><span class="sxs-lookup"><span data-stu-id="d34cf-143">Callto:tel:+ 14255550101</span></span></p></td>
<td><p><span data-ttu-id="d34cf-144">Öffnet eine nur-Telefon-Ansicht mit + 14255550101.</span><span class="sxs-lookup"><span data-stu-id="d34cf-144">Opens a phone-only view with +14255550101.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-145">Callto:sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d34cf-145">Callto:sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="d34cf-146">Öffnet eine nur-Telefon-Ansicht mit Kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="d34cf-146">Opens a phone-only view with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d34cf-147">sip:kazuto@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="d34cf-147">sip:kazuto@litwareinc.com</span></span></p></td>
<td><p><span data-ttu-id="d34cf-148">Öffnet ein Unterhaltungsfenster mit Kazuto@litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="d34cf-148">Opens a Conversation window with kazuto@litwareinc.com.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d34cf-149">conf: SIP:https://meet.contoso.com/kazuto/7322994</span><span class="sxs-lookup"><span data-stu-id="d34cf-149">conf:sip:https://meet.contoso.com/kazuto/7322994</span></span></p></td>
<td><p><span data-ttu-id="d34cf-150">Öffnet ein Unterhaltungsfenster und zeigt die Optionen für die Teilnahme an einer Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="d34cf-150">Opens a Conversation window and displays meeting audio join options.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d34cf-151">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d34cf-151">


</div>

<span> </span>

</div>

</div>

</span></span></div>

