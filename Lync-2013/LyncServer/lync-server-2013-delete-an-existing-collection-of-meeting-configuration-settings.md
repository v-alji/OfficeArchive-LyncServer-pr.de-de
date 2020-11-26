---
title: Löschen einer vorhandenen Sammlung von Konfigurationseinstellungen für Besprechungen
description: Löschen Sie eine vorhandene Sammlung von Einstellungen für die besprechungskonfiguration.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430532"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a>Löschen einer vorhandenen Sammlung von Besprechungs Konfigurationseinstellungen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-23_

Sie können eine Website-oder Benutzerkonfiguration löschen. Die globale Konfiguration kann nicht entfernt werden. Wenn Sie die globale Konfiguration löschen, wird sie automatisch auf die Standardwerte zurückgesetzt.

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a>So löschen Sie eine Website-oder Benutzer besprechungskonfiguration

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie in der linken Navigationsleiste auf **Konferenzen** , und klicken Sie dann auf **besprechungskonfiguration**.

4.  Klicken Sie in der Liste der Besprechungskonfigurationen auf die Standort- oder Poolkonfiguration, die Sie löschen möchten, klicken Sie dann auf **Bearbeiten** und anschließend auf **Löschen**.

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a>Entfernen von Besprechungs Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets

Besprechungseinstellungen können mithilfe von Windows PowerShell und dem Cmdlet Remove-CsMeetingConfiguration gelöscht werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden. Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a>So entfernen Sie eine bestimmte Sammlung von Besprechungs Konfigurationseinstellungen

  - Mit diesem Befehl werden die auf die Redmond-Website angewendeten Besprechungs Konfigurationseinstellungen entfernt:
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a>So entfernen Sie alle auf den Website Bereich angewendeten Besprechungs Konfigurationseinstellungen

  - Mit diesem Befehl werden alle auf den Website Bereich angewendeten Besprechungs Konfigurationseinstellungen entfernt:
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a>So entfernen Sie alle Einstellungen für die besprechungskonfiguration, die standardmäßig anonyme Benutzer zulassen

  - Und dieser entfernt alle Einstellungen, mit denen anonyme Benutzer standardmäßig zugelassen werden können:
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

