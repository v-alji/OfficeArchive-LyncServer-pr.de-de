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
# <a name="configuring-the-various-policies"></a>Konfigurieren der verschiedenen Richtlinien

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-24_

<div>

Nachfolgend sind die verschiedenen Richtlinien aufgeführt, die Sie in ihrer lync Server 2013-Topologie konfigurieren können, bevor Sie das Stress-und Leistungs Tool lync Server 2013 ausführen.

<div>

## <a name="configuring-the-archiving-policy"></a>Konfigurieren der Archivierungsrichtlinie

Sehen Sie sich das Beispielskript ArchivingPolicy.ps1 an. Sie müssen dieses Skript nur verwenden, wenn ein Archivierungs Server in Ihrer Topologie bereitgestellt wird. Ausführliche Informationen finden Sie in der Dokumentation zu lync Server 2013 und in der Hilfe zu Cmdlets für das [Archivieren und Überwachen von Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415629\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-conferencing-policy"></a>Konfigurieren der konferenzrichtlinie

Sehen Sie sich das Beispielskript MeetingPolicy.ps1 an. Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Webkonferenz-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-contacts-policy"></a>Konfigurieren der Kontakt Richtlinie

Sehen Sie sich das Beispiel ContactsPolicy.ps1 an. Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Chat-und Anwesenheits-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg398611\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-federation-policy"></a>Konfigurieren der Verbund Richtlinie

Sehen Sie sich das Beispiel FederationPolicy.ps1 an. Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Edgeserver-Cmdlets in](https://technet.microsoft.com/library/gg415635\(v=ocs.15\)) lync Server 2013 sowie in den [Cmdlets für den Verbund und den externen Zugriff in lync Server 2013](https://technet.microsoft.com/library/gg415651\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-call-admission-control-policy"></a>Konfigurieren der Richtlinie für die Anrufsteuerung

Sehen Sie sich das Beispiel BandwidthPolicy.ps1 an. Ausführliche Informationen finden Sie in der Übersicht zur lync Server 2013-Dokumentation zur [Anrufsteuerung in lync Server 2013](https://technet.microsoft.com/library/gg398529\(v=ocs.15\)) und in der Hilfe zu Cmdlets für die [Anrufsteuerung in lync Server 2013](https://technet.microsoft.com/library/gg415676\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-the-voice-routing-rules"></a>Konfigurieren der VoIP-Weiterleitungsregeln

Sehen Sie sich das Beispiel RoutingRules.ps1 an. Wenn Sie die Regeln für das VoIP-Routing konfigurieren, notieren Sie sich den Telefonkontext (also/Location-Profil oder/SimpleName) sowie interne/externe Ortsvorwahl, damit Sie diese beim Erstellen von Benutzern und während der LyncPerfTool-Konfiguration angeben können (insbesondere für PSTN-UC und UC-PSTN). Beispielsweise sollte der Parameter SimpleName im Aufruf des Cmdlets **New-CsDialPlan** im RoutingRules.ps1 Beispiel für den LocationProfile-Wert in der folgenden Abbildung von UserProfileGenerator.exe verwendet werden.

![Beispiel für VoIP-Routingregel](images/JJ945610.9f34d971-4ed0-4a4c-b101-086a91c4578c(OCS.15).jpg "Beispiel für VoIP-Routingregel")

Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Enterprise-VoIP-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415658\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-conferencing-attendant-application"></a>Konfigurieren der Konferenz Aufsichts Anwendung

Sehen Sie sich das Beispiel ConferenceAutoAttendantConfiguration.ps1 an. Notieren Sie sich die ConferencingAutoAttendant-Telefonnummer (standardmäßig 1121111111), damit Sie Sie in das LyncPerf Tool-Konfigurationstool für die Konfigurations Generierung eingeben können.

![Konfigurieren der Conferencing Attendant-Anwendung](images/JJ945610.0618a22f-27a9-423a-9085-d2bf71e82db6(OCS.15).jpg "Konfigurieren der Conferencing Attendant-Anwendung")

Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und der Cmdlet-Hilfe für [Webkonferenz-Cmdlets in lync Server 2013](https://technet.microsoft.com/library/gg415675\(v=ocs.15\)) und [Cmdlets für Einwahlkonferenzen in lync Server 2013](https://technet.microsoft.com/library/gg415630\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-lync-server-call-park-service"></a>Konfigurieren des lync Server-Anruf Park Diensts

Der Anruf Park ist standardmäßig deaktiviert. Sehen Sie sich das Beispiel CallParkConfiguration.ps1 an. Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlet-Cmdlets für die [Anruf parken-Anwendung in lync Server 2013](https://technet.microsoft.com/library/gg415639\(v=ocs.15\)).

</div>

<div>

## <a name="configuring-emergency-calls"></a>Konfigurieren von Notrufen

Führen Sie die folgenden Schritte aus, um Belastungs-und Leistungstests für Notrufe zu konfigurieren.

1.  Einrichten einer VoIP-Route für Notrufe. Ein Beispiel für das Einrichten dieser VoIP-Route finden Sie im RoutingRules.ps1-Skript unter dem Kommentar "Route E911 to PSTN".
    
    <div>
    

    > [!WARNING]  
    > Der Beispielbefehl in RoutingRules.ps1 weist ein Zahlenmuster auf, das die Zahl 119 anstatt 911 enthält. Vermeiden Sie die Verwendung von 911 (oder ihrer tatsächlichen lokalen Notfallnummer), um versehentliche Anrufe an Ihre lokalen Notfall Operatoren während der Auslastungstests zu verhindern. Diese Konfiguration dient nur zu Simulationszwecken.

    
    </div>

2.  Konfigurieren Sie Adressen, indem Sie die Werte auf der Registerkarte " **LIS** " im UserProvisioningTool ausfüllen, wie in der folgenden Abbildung dargestellt.
    
    ![Konfigurieren des Standort Informationsdiensts](images/JJ945610.8ac1faa1-e9f9-40d0-b8b7-b159f4f459f7(OCS.15).jpg "Konfigurieren des Standort Informationsdiensts")  

3.  Klicken Sie auf **LIS-Konfigurationsdateien generieren**.

4.  CSV-Dateien für Ports, Subnetze, Switches und drahtlose Zugriffspunkte (WAPs) sowie eine XML-Datei für das Stress-und Leistungs Tool lync Server 2013 werden generiert. Die CSV-Dateien werden als Eingaben (im gleichen Ordner) verwendet, wenn der standortinformationsdienst (LIS) mit dem LisConfiguration.ps1-Skript konfiguriert wird. Verschieben Sie die generierte Locations0.xml Datei in denselben Ordner wie die lync Server 2013-Datei für Stress und Leistungs Tool (LyncPerfTool.exe), in der Standortprofil Szenarien (Wähl Plan) ausgeführt werden.

</div>

<div>

## <a name="creating-enabling-configuring-and-disabling-users"></a>Erstellen, aktivieren, konfigurieren und Deaktivieren von Benutzern

Bevor Sie die folgenden Skripts ausführen, sollten Sie alle Benutzer erstellen. Befolgen Sie die Anweisungen unter [Erstellen von Benutzern und Kontakten](create-users-and-contacts.md) zum Erstellen von Benutzern. Ausführliche Informationen finden Sie in der Dokumentation zum lync Server 2013-Cmdlet für die Cmdlets " [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\))", " [CsUser](https://technet.microsoft.com/library/gg398510\(v=ocs.15\))" und " [Disable-CsUser](https://technet.microsoft.com/library/gg398747\(v=ocs.15\)) ".

</div>

<div>

## <a name="configuring-response-group-application"></a>Konfigurieren der Antwortgruppen Anwendung

Sehen Sie sich das Beispiel ResponseGroupConfiguration.ps1 an. Ausführliche Informationen finden Sie in der lync Server 2013-Dokumentation und in der Hilfe zu Cmdlets für [Antwortgruppen Anwendungen in lync Server 2013](https://technet.microsoft.com/library/gg415654\(v=ocs.15\)). Informationen zum Überprüfen der Anwendungskonfiguration der Reaktionsgruppe finden Sie unter `https://<poolfqdn>/RgsConfig/` wie in der folgenden Abbildung dargestellt.

![Das Tool für die Reaktionsgruppen Konfiguration.](images/JJ945610.480a9440-2283-4533-98f8-86daaab4781c(OCS.15).jpg "Das Tool für die Reaktionsgruppen Konfiguration.")

</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

