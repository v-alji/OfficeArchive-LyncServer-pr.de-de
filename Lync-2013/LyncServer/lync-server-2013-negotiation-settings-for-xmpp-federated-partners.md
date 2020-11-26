---
title: 'Lync Server 2013: Aushandlungseinstellungen für XMPP-Verbundpartner'
description: 'Lync Server 2013: Aushandlungs Einstellungen für XMPP Federated-Partner.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Negotiation settings for XMPP federated partners
ms:assetid: ef773942-ef92-4f71-85a1-738dfebdfa00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552456(v=OCS.15)
ms:contentKeyID: 48679567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ac3d9c69d407dc750a1afb35f0a448869a88f09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445586"
---
# <a name="negotiation-settings-for-xmpp-federated-partners-in-lync-server-2013"></a><span data-ttu-id="d941f-103">Aushandlungseinstellungen für XMPP-Verbundpartner in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d941f-103">Negotiation settings for XMPP federated partners in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d941f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d941f-104">

<span> </span></span></span>

<span data-ttu-id="d941f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="d941f-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="d941f-106">Die Einstellungen für die Aushandlungs Typen in der Konfiguration eines XMPP-Partners haben eine Vielzahl möglicher Kombinationen.</span><span class="sxs-lookup"><span data-stu-id="d941f-106">The settings for the negotiation types in the configuration of an XMPP Partner have a wide variety of possible combinations.</span></span> <span data-ttu-id="d941f-107">Nicht alle diese Kombinationen sind gültig.</span><span class="sxs-lookup"><span data-stu-id="d941f-107">Not all of these combinations are valid.</span></span> <span data-ttu-id="d941f-108">In der in diesem Thema beschriebenen Tabelle werden die gültigen und ungültigen Einstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="d941f-108">The table detailed in this topic will define the valid and not valid settings.</span></span> <span data-ttu-id="d941f-109">Allgemeine Konfigurationen werden in der ersten Tabelle dargestellt, der zweiten Tabelle, in der alle möglichen Kombinationen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d941f-109">Common configurations are presented in the first table, the second table detailing all possible combinations.</span></span> <span data-ttu-id="d941f-110">Beachten Sie, dass Sie keine *einfache Authentifizierungs-und Sicherheitsschicht* (SASL) haben können, **es sei denn** , *Transport Layer Security* (TLS) steht ebenfalls zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d941f-110">Note that you cannot have *Simple Authentication and Security Layer* (SASL) **unless** *Transport Layer Security* (TLS) is also available.</span></span> <span data-ttu-id="d941f-111">SASL wird in einem unverschlüsselten (lesbaren) Format gesendet und sollte niemals übertragen werden, es sei denn, es wird durch ein anderes Mittel wie TLS geschützt.</span><span class="sxs-lookup"><span data-stu-id="d941f-111">SASL is sent in an unencrypted (readable) format and should never be transmitted unless protected by another means, such as TLS.</span></span>

### <a name="common-xmpp-federation-negotiation-methods"></a><span data-ttu-id="d941f-112">Allgemeine Methoden zur XMPP-Föderations Verhandlung</span><span class="sxs-lookup"><span data-stu-id="d941f-112">Common XMPP Federation Negotiation Methods</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d941f-113">Transport Layer Security (TLS)</span><span class="sxs-lookup"><span data-stu-id="d941f-113">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="d941f-114">Einfache Authentifizierungs-und Sicherheitsschicht (SASL)</span><span class="sxs-lookup"><span data-stu-id="d941f-114">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="d941f-115">Dialback-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d941f-115">Dialback Authentication</span></span></th>
<th><span data-ttu-id="d941f-116">Erwartete Authentifizierungsmethode (n)</span><span class="sxs-lookup"><span data-stu-id="d941f-116">Expected Authentication Method(s)</span></span></th>
<th><span data-ttu-id="d941f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d941f-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d941f-118"> Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-118">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-119">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-120">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-120">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-121">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-121">SASL over TLS</span></span></p></td>
<td><p><span data-ttu-id="d941f-122">TLS und SASL sind hilfreich, um sicherzustellen, dass der SASL-Nachrichtendatenstrom sicher ist.</span><span class="sxs-lookup"><span data-stu-id="d941f-122">TLS and SASL required helps to ensure that the SASL message stream is secure.</span></span> <span data-ttu-id="d941f-123">Dialback ist nicht verfügbar und kann nicht für eine Fallback-Methode verwendet werden, wenn der XMPP-Verbundpartner TLS nicht auf Required oder optional gesetzt hat.</span><span class="sxs-lookup"><span data-stu-id="d941f-123">Dialback is not available and cannot be used for a fallback method if the XMPP federated partner has not set TLS to required or optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-124">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-124">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-125">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-126">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-126">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-127">SASL über TLS, TLS-Dialback, TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-127">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-128">Wenn der XMPP-Föderationspartner SASL auf optional oder erforderlich SASL gesetzt hat, wird eine TLS-Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d941f-128">By requiring TLS, if the XMPP federated partner has set SASL to optional or required SASL is used.</span></span> <span data-ttu-id="d941f-129">Wenn SASL nicht zur Verfügung steht, wird Dialback über TLS verwendet.</span><span class="sxs-lookup"><span data-stu-id="d941f-129">If SASL is not available, Dialback over TLS will be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-130">Optional </span><span class="sxs-lookup"><span data-stu-id="d941f-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-131">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-132">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-132">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-133">SASL über TLS, TLS-Dialback, TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-133">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-134">Obwohl die angebotenen Verhandlungsmethoden sehr flexibel sind, basieren diese Einstellungen auf den Einstellungen des XMPP-Verbundpartners.</span><span class="sxs-lookup"><span data-stu-id="d941f-134">While very flexible in the negotiation methods offered, these settings rely on the XMPP federation partner’s settings.</span></span> <span data-ttu-id="d941f-135">Wenn der Partner TLS optional oder erforderlich hat, aber SASL nicht unterstützt wird, steht TLS-Dialback zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d941f-135">If the partner has TLS optional or required but SASL is not supported, TLS Dialback will be available.</span></span> <span data-ttu-id="d941f-136">Wenn der Partner TLS und SASL auf optional oder required eingestellt hat, wird die optimale Auswahl von TLS über SASL verwendet.</span><span class="sxs-lookup"><span data-stu-id="d941f-136">If the partner has TLS and SASL set to optional or required, the optimal selection of TLS over SASL is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-137">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-138">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-139">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-139">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-140">TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-140">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-141">In vielen Fällen ist TCP-Dialback die einzige mögliche Lösung.</span><span class="sxs-lookup"><span data-stu-id="d941f-141">In many cases, TCP Dialback is the only possible solution.</span></span> <span data-ttu-id="d941f-142">Weniger wünschenswert als andere Optionen, bietet dies ein gewisses Maß an Vertrauen.</span><span class="sxs-lookup"><span data-stu-id="d941f-142">Less desirable than other options, it does provide some level of trust.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="xmpp-federation-negotiation-methods-matrix---complete"></a><span data-ttu-id="d941f-143">XMPP-Verbund-Aushandlungs Methoden-Matrix – abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="d941f-143">XMPP Federation Negotiation Methods Matrix - Complete</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d941f-144">Transport Layer Security (TLS)</span><span class="sxs-lookup"><span data-stu-id="d941f-144">Transport Layer Security (TLS)</span></span></th>
<th><span data-ttu-id="d941f-145">Einfache Authentifizierungs-und Sicherheitsschicht (SASL)</span><span class="sxs-lookup"><span data-stu-id="d941f-145">Simple Authentication and Security Layer (SASL)</span></span></th>
<th><span data-ttu-id="d941f-146">Dialback-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d941f-146">Dialback Authentication</span></span></th>
<th><span data-ttu-id="d941f-147">Erwartete Authentifizierungsmethode</span><span class="sxs-lookup"><span data-stu-id="d941f-147">Expected Authentication Method</span></span></th>
<th><span data-ttu-id="d941f-148">Hinweise, Warnung oder Fehler für ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-148">Notes, Warning or Error for Not Valid Configuration</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d941f-149"> Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-149">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-150">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-150">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-151">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-151">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-152">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-152">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-153">Dialback wird nicht ausgeführt, wenn sowohl SASL als auch TLS erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d941f-153">Dialback will not operate if both SASL and TLS are required.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-154"> Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-154">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-155">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-155">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-156">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-156">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-157">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-157">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-158">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-158">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-159">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-159">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-160">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-160">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-161">SASL über TLS, TLS-Dialback, TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-161">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-162">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-162">SASL requires TLS.</span></span> <span data-ttu-id="d941f-163">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-163">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-164">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-164">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-165">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-165">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-166">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-166">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-167">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-167">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-168">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-168">SASL requires TLS.</span></span> <span data-ttu-id="d941f-169">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-169">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-170">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-171">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-171">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-172">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-172">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-173">TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-173">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-174">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-174">SASL requires TLS.</span></span> <span data-ttu-id="d941f-175">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-175">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-176">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-176">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-177">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-177">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-178">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-178">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-179">Ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-179">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-180">Da SASL TLS erfordert und TLS nicht zur Verfügung steht, kann SASL/TLS nicht erfolgreich sein.</span><span class="sxs-lookup"><span data-stu-id="d941f-180">Because SASL requires TLS, and TLS is not available, SASL/TLS cannot succeed.</span></span> <span data-ttu-id="d941f-181">TCP Dialback ist auf "false" festgelegt und kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d941f-181">TCP Dialback is set to false, and cannot be used.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-182">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-182">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-183">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-183">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-184">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-184">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-185">SASL über TLS, TLS-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-185">SASL over TLS, TLS Dialback</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-186">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-186">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-187">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-187">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-188">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-188">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-189">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-189">SASL over TLS</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-190">Optional </span><span class="sxs-lookup"><span data-stu-id="d941f-190">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-191">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-191">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-192">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-192">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-193">SASL über TLS, TLS-Dialback, TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-193">SASL over TLS, TLS Dialback, TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-194">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-194">SASL requires TLS.</span></span> <span data-ttu-id="d941f-195">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-195">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-196">Optional </span><span class="sxs-lookup"><span data-stu-id="d941f-196">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-197">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-197">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-198">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-198">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-199">SASL über TLS</span><span class="sxs-lookup"><span data-stu-id="d941f-199">SASL over TLS</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-200">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-200">SASL requires TLS.</span></span> <span data-ttu-id="d941f-201">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-201">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-202">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-202">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-203">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-203">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-204">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-204">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-205">TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-205">TCP Dialback</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-206">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-206">SASL requires TLS.</span></span> <span data-ttu-id="d941f-207">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-207">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-208">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-208">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-209">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-209">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-210">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-210">False</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-211">Ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-211">Not Valid Configuration</span></span>


</div></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-212">SASL erfordert TLS.</span><span class="sxs-lookup"><span data-stu-id="d941f-212">SASL requires TLS.</span></span> <span data-ttu-id="d941f-213">Wenn Sie zulassen, dass TLS optional ist, kann dies zu fehlgeschlagenen Sitzungs Verhandlungen führen.</span><span class="sxs-lookup"><span data-stu-id="d941f-213">Allowing TLS to be optional may result in failed session negotiations.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-214">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-214">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-215">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-215">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-216">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-216">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-217">TLS-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-217">TLS Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-218">Die Konfiguration ermöglicht TLS-Dialback.</span><span class="sxs-lookup"><span data-stu-id="d941f-218">Configuration allows for TLS Dialback.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-219">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d941f-219">Required</span></span></p></td>
<td><p><span data-ttu-id="d941f-220">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-220">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-221">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-221">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-222">Ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-222">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-223">SASL oder Dialback muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d941f-223">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-224">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-224">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-225">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-225">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-226">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-226">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-227">TLS-Dialback, TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-227">TLS Dialback, TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-228">Basierend auf den Aushandlungs Optionen des anderen Endpunkts werden TCP-oder TLS-Dialback akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d941f-228">Based on negotiation choices of the other end point, TCP or TLS Dialback will be accepted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-229">Optional</span><span class="sxs-lookup"><span data-stu-id="d941f-229">Optional</span></span></p></td>
<td><p><span data-ttu-id="d941f-230">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-230">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-231">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-231">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-232">Ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-232">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-233">SASL oder Dialback muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d941f-233">SASL or Dialback must be enabled.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d941f-234">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-234">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-235">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-235">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-236">Wahr</span><span class="sxs-lookup"><span data-stu-id="d941f-236">True</span></span></p></td>
<td><p><span data-ttu-id="d941f-237">TCP-Dialback</span><span class="sxs-lookup"><span data-stu-id="d941f-237">TCP Dialback</span></span></p></td>
<td><p><span data-ttu-id="d941f-238">TCP-Dialback ist die einzige verfügbare Aushandlungsmethode.</span><span class="sxs-lookup"><span data-stu-id="d941f-238">TCP Dialback is the only negotiation method available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d941f-239">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-239">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-240">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d941f-240">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="d941f-241">Falsch</span><span class="sxs-lookup"><span data-stu-id="d941f-241">False</span></span></p></td>
<td><p><span data-ttu-id="d941f-242">Ungültige Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d941f-242">Not Valid Configuration</span></span></p></td>
<td><div>

> [!WARNING]  
> <span data-ttu-id="d941f-243">SASL oder Dialback muss aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="d941f-243">SASL or Dialback must be enabled.</span></span>


<span data-ttu-id="d941f-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d941f-244"></div></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

