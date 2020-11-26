---
title: 'Lync Server 2013: Löschen einer Sammlung von Konfigurationseinstellungen für Geräte Updates'
description: 'Lync Server 2013: Löschen einer Sammlung von Konfigurationseinstellungen für Geräte Updates.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a collection of Device Update configuration settings
ms:assetid: 1a649136-34a9-42a7-a5b3-a78bbfe93f36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994019(v=OCS.15)
ms:contentKeyID: 51803928
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b3a03227869f68a52a30ea94db33bfb954b7e122
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430714"
---
# <a name="delete-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a>Löschen einer Sammlung von Konfigurationseinstellungen für Geräte Updates in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-20_

Die Konfigurationseinstellungen für Geräte Updates können auch mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsdeviceUpdateConfiguration** gelöscht werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden. Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>


<div>

## <a name="to-remove-a-specific-collection-of-device-update-configuration-settings"></a>So entfernen Sie eine bestimmte Sammlung von Konfigurationseinstellungen für Geräte Updates

  - Mit diesem Befehl werden die Konfigurationseinstellungen für das Geräteupdate gelöscht, die auf die Redmond-Website angewendet wurden:
    
        Remove-CsDeviceUpdateConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-device-update-configuration-settings-applied-to-the-site-scope"></a>So entfernen Sie alle auf den Website Bereich angewendeten Konfigurationseinstellungen für Geräte Updates

  - Dieser Befehl löscht alle Konfigurationseinstellungen für Geräte Updates, die auf den Website Bereich angewendet werden:
    
        Get-CsDeviceUpdateConfiguration -Filter "site:*" | Remove-CsDeviceUpdateConfiguration

</div>

<div>

## <a name="to-remove-device-update-configuration-settings-based-on-the-value-of-the-logcleanupinterval-property"></a>So entfernen Sie die Konfigurationseinstellungen für Geräte Updates basierend auf dem Wert der LogCleanUpInterval-Eigenschaft

  - Mit dem folgenden Befehl werden alle Konfigurationseinstellungen für Geräte Updates gelöscht, bei denen das Protokoll Bereinigungsintervall größer als 10 Tage ist (10.00:00:00):
    
        Get-CsDeviceUpdateConfiguration | Where-Object {$_.LogCleanUpInterval -gt "10.00:00:00" | Remove-CsDeviceUpdateConfiguration

</div>

Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsDeviceUpdateConfiguration) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

