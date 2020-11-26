---
title: Konfigurieren der verschiedenen Richtlinien
description: Konfigurieren der verschiedenen Richtlinien
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configuring the Various Policies
ms:assetid: e3b3cbda-7c17-470b-acb0-82fdcc473184
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945610(v=OCS.15)
ms:contentKeyID: 51541436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 746d299ac605c7dfe89a957246d47309dfbc0a5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440061"
---
# <a name="configuring-the-various-policies"></a><span data-ttu-id="d5c43-103">Konfigurieren der verschiedenen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d5c43-103">Configuring the Various Policies</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5c43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5c43-104">

<span> </span></span></span>

<span data-ttu-id="d5c43-105">_**Letztes Änderungsdatum des Themas:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="d5c43-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<div>

<span data-ttu-id="d5c43-106">Nachfolgend sind die verschiedenen Richtlinien aufgeführt, die Sie in ihrer lync Server 2013-Topologie konfigurieren können, bevor Sie das Stress-und Leistungs Tool lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5c43-106">Here are the various policies that you can configure in your Lync Server 2013 topology, prior to running the Lync Server 2013 Stress and Performance Tool.</span></span>

<div>

## <a name="configuring-the-archiving-policy"></a><span data-ttu-id="d5c43-107">Konfigurieren der Archivierungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d5c43-107">Configuring the Archiving Policy</span></span>

<span data-ttu-id="d5c43-108">Sehen Sie sich das Beispielskript ArchivingPolicy.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-108">See the example script ArchivingPolicy.ps1.</span></span> <span data-ttu-id="d5c43-109">Sie müssen dieses Skript nur verwenden, wenn ein Archivierungs Server in Ihrer Topologie bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d5c43-109">You need to use this script only if an Archiving Server is deployed in your topology.</span></span> <span data-ttu-id="d5c43-110">Ausführliche Informationen finden Sie in der Dokumentation zu lync Server 2013 und in der Hilfe zu Cmdlets für das [Archivieren und Überwachen von Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-110">For details, see the Lync Server 2013 documentation and cmdlet Help for [Archiving and Monitoring cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a><span data-ttu-id="d5c43-111">Konfigurieren der konferenzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="d5c43-111">Configuring the Conferencing Policy</span></span>

<span data-ttu-id="d5c43-112">Sehen Sie sich das Beispielskript MeetingPolicy.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-112">See the example script MeetingPolicy.ps1.</span></span> <span data-ttu-id="d5c43-113">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Webkonferenz-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-113">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-contacts-policy"></a><span data-ttu-id="d5c43-114">Konfigurieren der Kontakt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d5c43-114">Configuring the Contacts Policy</span></span>

<span data-ttu-id="d5c43-115">Sehen Sie sich das Beispiel ContactsPolicy.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-115">See the example ContactsPolicy.ps1.</span></span> <span data-ttu-id="d5c43-116">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Chat-und Anwesenheits-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-116">For details, see the Lync Server 2013 documentation and the cmdlet Help for [IM and presence cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-federation-policy"></a><span data-ttu-id="d5c43-117">Konfigurieren der Verbund Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d5c43-117">Configuring the Federation Policy</span></span>

<span data-ttu-id="d5c43-118">Sehen Sie sich das Beispiel FederationPolicy.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-118">See the example FederationPolicy.ps1.</span></span> <span data-ttu-id="d5c43-119">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Edgeserver-Cmdlets in](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) lync Server 2013 sowie in den [Cmdlets für den Verbund und den externen Zugriff in lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-119">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Edge Server cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) and [Federation and external access cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a><span data-ttu-id="d5c43-120">Konfigurieren der Richtlinie für die Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="d5c43-120">Configuring the Call Admission Control Policy</span></span>

<span data-ttu-id="d5c43-121">Sehen Sie sich das Beispiel BandwidthPolicy.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-121">See the example BandwidthPolicy.ps1.</span></span> <span data-ttu-id="d5c43-122">Ausführliche Informationen finden Sie in der Übersicht zur lync Server 2013-Dokumentation zur [Anrufsteuerung in lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) und in der Hilfe zu Cmdlets für die [Anrufsteuerung in lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-122">For details, see the Lync Server 2013 documentation [Overview of call admission control in Lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) and the cmdlet Help for [Call admission control cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a><span data-ttu-id="d5c43-123">Konfigurieren der VoIP-Weiterleitungsregeln</span><span class="sxs-lookup"><span data-stu-id="d5c43-123">Configuring the Voice Routing Rules</span></span>

<span data-ttu-id="d5c43-124">Sehen Sie sich das Beispiel RoutingRules.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-124">See the example RoutingRules.ps1.</span></span> <span data-ttu-id="d5c43-125">Wenn Sie die Regeln für das VoIP-Routing konfigurieren, notieren Sie sich den Telefonkontext (also/Location-Profil oder/SimpleName) sowie interne/externe Ortsvorwahl, damit Sie diese beim Erstellen von Benutzern und während der LyncPerfTool-Konfiguration angeben können (insbesondere für PSTN-UC und UC-PSTN).</span><span class="sxs-lookup"><span data-stu-id="d5c43-125">When you configure the voice routing rules, take note of the Phone Context (that is, /Location Profile or /SimpleName) and Internal/External Area Codes so that you can specify them when creating users and during LyncPerfTool configuration (specifically for PSTN-UC and UC-PSTN).</span></span> <span data-ttu-id="d5c43-126">Beispielsweise sollte der Parameter SimpleName im Aufruf des Cmdlets **New-CsDialPlan** im RoutingRules.ps1 Beispiel für den LocationProfile-Wert in der folgenden Abbildung von UserProfileGenerator.exe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5c43-126">For example, the SimpleName parameter in the call to the **New-CsDialPlan** cmdlet in the RoutingRules.ps1 example should be used for the LocationProfile value in the following figure of UserProfileGenerator.exe.</span></span>

<span data-ttu-id="d5c43-127">![Beispiel für VoIP-Routingregel](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Beispiel für VoIP-Routingregel")</span><span class="sxs-lookup"><span data-stu-id="d5c43-127">![Sample voice routing rule.](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Sample voice routing rule.")</span></span>

<span data-ttu-id="d5c43-128">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Enterprise-VoIP-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-128">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Enterprise Voice cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a><span data-ttu-id="d5c43-129">Konfigurieren der Konferenz Aufsichts Anwendung</span><span class="sxs-lookup"><span data-stu-id="d5c43-129">Configuring Conferencing Attendant application</span></span>

<span data-ttu-id="d5c43-130">Sehen Sie sich das Beispiel ConferenceAutoAttendantConfiguration.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-130">See the example ConferenceAutoAttendantConfiguration.ps1.</span></span> <span data-ttu-id="d5c43-131">Notieren Sie sich die ConferencingAutoAttendant-Telefonnummer (standardmäßig 1121111111), damit Sie Sie in das LyncPerf Tool-Konfigurationstool für die Konfigurations Generierung eingeben können.</span><span class="sxs-lookup"><span data-stu-id="d5c43-131">Take note of the ConferencingAutoAttendant phone number (1121111111, by default), so that you can type it into the LyncPerf Tool Configuration tool for configuration generation.</span></span>

<span data-ttu-id="d5c43-132">![Konfigurieren der Conferencing Attendant-Anwendung](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Konfigurieren der Conferencing Attendant-Anwendung")</span><span class="sxs-lookup"><span data-stu-id="d5c43-132">![Configuring the Conferencing Attendant application](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Configuring the Conferencing Attendant application")</span></span>

<span data-ttu-id="d5c43-133">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Webkonferenz-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) und [Cmdlets für Einwahlkonferenzen in lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-133">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Web conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) and [Dial-in conferencing cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a><span data-ttu-id="d5c43-134">Konfigurieren des lync Server-Anruf Park Diensts</span><span class="sxs-lookup"><span data-stu-id="d5c43-134">Configuring Lync Server Call Park Service</span></span>

<span data-ttu-id="d5c43-135">Der Anruf Park ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d5c43-135">Call Park is disabled by default.</span></span> <span data-ttu-id="d5c43-136">Sehen Sie sich das Beispiel CallParkConfiguration.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-136">See the example CallParkConfiguration.ps1.</span></span> <span data-ttu-id="d5c43-137">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlet-Cmdlets für die [Anruf parken-Anwendung in lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span><span class="sxs-lookup"><span data-stu-id="d5c43-137">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Call Park application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).</span></span>

</div>

<div>

## <a name="configuring-emergency-calls"></a><span data-ttu-id="d5c43-138">Konfigurieren von Notrufen</span><span class="sxs-lookup"><span data-stu-id="d5c43-138">Configuring Emergency Calls</span></span>

<span data-ttu-id="d5c43-139">Führen Sie die folgenden Schritte aus, um Belastungs-und Leistungstests für Notrufe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d5c43-139">Perform the following steps to configure stress and performance testing for emergency calls.</span></span>

1.  <span data-ttu-id="d5c43-140">Einrichten einer VoIP-Route für Notrufe.</span><span class="sxs-lookup"><span data-stu-id="d5c43-140">Set up a voice route for emergency calls.</span></span> <span data-ttu-id="d5c43-141">Ein Beispiel für das Einrichten dieser VoIP-Route finden Sie im RoutingRules.ps1-Skript unter dem Kommentar "Route E911 to PSTN".</span><span class="sxs-lookup"><span data-stu-id="d5c43-141">See the RoutingRules.ps1 script under the comment "Route E911 to PSTN" for an example of setting up this voice route.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="d5c43-142">Der Beispielbefehl in RoutingRules.ps1 weist ein Zahlenmuster auf, das die Zahl 119 anstatt 911 enthält.</span><span class="sxs-lookup"><span data-stu-id="d5c43-142">The example command in RoutingRules.ps1 has a number pattern that includes the number 119 rather than 911.</span></span> <span data-ttu-id="d5c43-143">Vermeiden Sie die Verwendung von 911 (oder ihrer tatsächlichen lokalen Notfallnummer), um versehentliche Anrufe an Ihre lokalen Notfall Operatoren während der Auslastungstests zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d5c43-143">You should avoid using 911 (or your actual local emergency number) to prevent accidental calls to your local emergency operators during load testing.</span></span> <span data-ttu-id="d5c43-144">Diese Konfiguration dient nur zu Simulationszwecken.</span><span class="sxs-lookup"><span data-stu-id="d5c43-144">This configuration is for simulation purposes only.</span></span>

    
    </div>

2.  <span data-ttu-id="d5c43-145">Konfigurieren Sie Adressen, indem Sie die Werte auf der Registerkarte " **LIS** " im UserProvisioningTool ausfüllen, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d5c43-145">Configure addresses by filling in the values on the **LIS** tab in the UserProvisioningTool, as shown in the following figure.</span></span>
    
    <span data-ttu-id="d5c43-146">![Konfigurieren des Standort Informationsdiensts](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Konfigurieren des Standort Informationsdiensts")</span><span class="sxs-lookup"><span data-stu-id="d5c43-146">![Configuring the Location Information Service.](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Configuring the Location Information Service.")</span></span>  

3.  <span data-ttu-id="d5c43-147">Klicken Sie auf **LIS-Konfigurationsdateien generieren**.</span><span class="sxs-lookup"><span data-stu-id="d5c43-147">Click **Generate LIS Config Files**.</span></span>

4.  <span data-ttu-id="d5c43-148">CSV-Dateien für Ports, Subnetze, Switches und drahtlose Zugriffspunkte (WAPs) sowie eine XML-Datei für das Stress-und Leistungs Tool lync Server 2013 werden generiert.</span><span class="sxs-lookup"><span data-stu-id="d5c43-148">CSV files for ports, subnets, switches, and wireless access points (WAPs), and an XML file for the Lync Server 2013 Stress and Performance Tool, are generated.</span></span> <span data-ttu-id="d5c43-149">Die CSV-Dateien werden als Eingaben (im gleichen Ordner) verwendet, wenn der standortinformationsdienst (LIS) mit dem LisConfiguration.ps1-Skript konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="d5c43-149">The CSV files are to be used as inputs (in the same folder) when configuring Location Information service (LIS) with the LisConfiguration.ps1 script.</span></span> <span data-ttu-id="d5c43-150">Verschieben Sie die generierte Locations0.xml Datei in denselben Ordner wie die lync Server 2013-Datei für Stress und Leistungs Tool (LyncPerfTool.exe), in der Standortprofil Szenarien (Wähl Plan) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5c43-150">Move the generated Locations0.xml file to the same folder as the Lync Server 2013 Stress and Performance Tool executable (LyncPerfTool.exe), which will run location profile (dial plan) scenarios.</span></span>

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a><span data-ttu-id="d5c43-151">Erstellen, aktivieren, konfigurieren und Deaktivieren von Benutzern</span><span class="sxs-lookup"><span data-stu-id="d5c43-151">Creating, Enabling, Configuring and Disabling Users</span></span>

<span data-ttu-id="d5c43-152">Bevor Sie die folgenden Skripts ausführen, sollten Sie alle Benutzer erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5c43-152">You should create all your users before running the following scripts.</span></span> <span data-ttu-id="d5c43-153">Befolgen Sie die Anweisungen unter [Erstellen von Benutzern und Kontakten](create-users-and-contacts.md) zum Erstellen von Benutzern.</span><span class="sxs-lookup"><span data-stu-id="d5c43-153">Follow the instructions in [Create Users and Contacts](create-users-and-contacts.md) to create users.</span></span> <span data-ttu-id="d5c43-154">Ausführliche Informationen finden Sie in der Dokumentation zum lync Server 2013-Cmdlet für die Cmdlets " [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\))", " [CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))" und " [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) ".</span><span class="sxs-lookup"><span data-stu-id="d5c43-154">For details, see the Lync Server 2013 cmdlet documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)), [Set-CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\)), and [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) cmdlets.</span></span>

</div>

<div>

## <a name="configuring-response-group-application"></a><span data-ttu-id="d5c43-155">Konfigurieren der Antwortgruppen Anwendung</span><span class="sxs-lookup"><span data-stu-id="d5c43-155">Configuring Response Group application</span></span>

<span data-ttu-id="d5c43-156">Sehen Sie sich das Beispiel ResponseGroupConfiguration.ps1 an.</span><span class="sxs-lookup"><span data-stu-id="d5c43-156">See the example ResponseGroupConfiguration.ps1.</span></span> <span data-ttu-id="d5c43-157">Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Antwortgruppen Anwendungen in lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)). Informationen zum Überprüfen der Anwendungskonfiguration der Reaktionsgruppe finden Sie unter `https://<poolfqdn>/RgsConfig/` wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d5c43-157">For details, see the Lync Server 2013 documentation and the cmdlet Help for [Response Group application cmdlets in Lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)).To review the Response Group application configuration, see `https://<poolfqdn>/RgsConfig/`, as shown in the following figure.</span></span>

<span data-ttu-id="d5c43-158">![Das Tool für die Reaktionsgruppen Konfiguration.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "Das Tool für die Reaktionsgruppen Konfiguration.")</span><span class="sxs-lookup"><span data-stu-id="d5c43-158">![The Response Group Configuration Tool.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "The Response Group Configuration Tool.")</span></span>

<span data-ttu-id="d5c43-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5c43-159"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

