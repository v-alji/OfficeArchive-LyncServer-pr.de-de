---
title: 'Lync Server 2013: Löschen einer Standort- oder Benutzerrichtlinie für den externen Benutzerzugriff'
description: 'Lync Server 2013: Löschen einer Website oder Benutzerrichtlinie für den Zugriff durch externe Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete a site or user policy for external user access
ms:assetid: 6d907507-825b-4354-9c03-337a459f72de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521013(v=OCS.15)
ms:contentKeyID: 48184455
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6aac81e7b50603e5eb80cde8877cdc06f138d872
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430672"
---
# <a name="delete-a-site-or-user-policy-for-external-user-access-in-lync-server-2013"></a>Löschen einer Standort- oder Benutzerrichtlinie für den externen Benutzerzugriff in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-22_

Sie können jede Website oder Benutzerrichtlinie löschen, die in der lync Server-Systemsteuerung auf der Seite " **externe Zugriffsrichtlinie** " aufgeführt ist. Wenn Sie die globale Richtlinie löschen, wird Sie nicht tatsächlich gelöscht, sondern nur auf die Standardeinstellungen zurückgesetzt, die keine Unterstützung für die Zugriffsoptionen für externe Benutzer beinhalten. Details zum Zurücksetzen der globalen Richtlinie finden Sie unter [Zurücksetzen der globalen Richtlinie für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-reset-the-global-policy-for-external-user-access.md).

<div>

## <a name="to-delete-a-site-or-user-policy-for-external-user-access"></a>So löschen Sie eine Website-oder Benutzerrichtlinie für den Zugriff durch externe Benutzer

1.  Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie auf **externer Benutzer Zugriff**, und klicken Sie auf **Richtlinie für den externen Zugriff**.

4.  Klicken Sie auf der Registerkarte **Richtlinie für den externen Zugriff** auf die Website oder Benutzerrichtlinie, die Sie löschen möchten, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **Löschen**.

5.  Wenn Sie aufgefordert werden, den Löschvorgang zu bestätigen, klicken Sie auf **OK**.

</div>

<div>

## <a name="removing-pin-policies-by-using-windows-powershell-cmdlets"></a>Entfernen von PIN-Richtlinien mithilfe von Windows PowerShell-Cmdlets

Richtlinien für den externen Zugriff können mithilfe von Windows PowerShell und dem Cmdlet Remove-CsExternalAccessPolicy gelöscht werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden. Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-remove-a-specific-external-access-policy"></a>So entfernen Sie eine bestimmte Richtlinie für den externen Zugriff

  - Mit diesem Befehl wird die auf die Redmond-Website angewendete Richtlinie für den externen Zugriff entfernt:
    
        Remove-CsExternalAccessPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-external-access-policies-applied-to-the-per-user-scope"></a>So entfernen Sie alle auf den Benutzerbereich angewendeten Richtlinien für den externen Zugriff

  - Mit diesem Befehl werden alle im Benutzerbereich konfigurierten externen Zugriffsrichtlinien entfernt:
    
        Get-CsExternalAccessPolicy -Filter "tag:*" | Remove-CsExternalAccessPolicy

</div>

<div>

## <a name="to-remove-all-the-external-access-policies-where-outside-user-access-is-disabled"></a>So entfernen Sie alle externen Zugriffsrichtlinien, bei denen der Zugriff außerhalb des Benutzers deaktiviert ist

  - Dieser Befehl löscht alle externen Zugriffsrichtlinien, bei denen der Zugriff außerhalb des Benutzers deaktiviert wurde:
    
        Get-CsExternalAccessPolicy | Where-Object {$_.EnableOutsideAccess -eq $False} | Remove-CsExternalAccessPolicy

</div>

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsExternalAccessPolicy) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

