---
title: 'Lync Server 2013: Genehmigen einer geräteaktualisierungsregel'
description: 'Lync Server 2013: Genehmigen einer geräteaktualisierungsregel'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Approve a Device Update rule
ms:assetid: 9dbb1c9a-be0f-4e13-9234-05501ab43ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994053(v=OCS.15)
ms:contentKeyID: 51803964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 127d16dad6329e952b9033db07ac2f4a4fe9112c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440563"
---
# <a name="approve-a-device-update-rule-in-lync-server-2013"></a>Genehmigen einer geräteaktualisierungsregel in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-23_

Nachdem Sie eine geräteaktualisierungsregel importiert haben, ist Sie auf Ihren Testgeräten installiert. Wenn die Tests erfolgreich sind und Sie das Update für Ihre Organisation bereitzustellen möchten, genehmigen Sie es entweder mithilfe der lync Server-Systemsteuerung oder Windows PowerShell.

<div>

## <a name="to-approve-a-device-update-rule-by-using-lync-server-control-panel"></a>So genehmigen Sie eine geräteaktualisierungsregel mithilfe der lync Server-Systemsteuerung

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Führen Sie auf der Seite **Device Update** eine der folgenden Aktionen aus:
    
      - Wenn Sie eine Regel genehmigen möchten, wählen Sie diese Regel aus.
    
      - Um alle Regeln zu genehmigen, klicken Sie auf **Bearbeiten** und dann auf **Alle auswählen**.

4.  Klicken Sie auf **Aktion** und dann auf **genehmigen**.

</div>

<div>

## <a name="approving-a-device-update-rule-by-using-windows-powershell-cmdlets"></a>Genehmigen einer geräteaktualisierungsregel mithilfe von Windows PowerShell-Cmdlets

Geräteaktualisierungsregeln können auch mithilfe von Windows PowerShell und dem Cmdlet " **genehmigen-CsDeviceUpdateRule** " genehmigt werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.

<div>


> [!NOTE]  
> Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>

## <a name="to-approve-a-single-device-update-rule"></a>So genehmigen Sie eine einzelne geräteaktualisierungsregel

  - Der folgende Befehl genehmigt die geräteaktualisierungsregel d5ce3c10-2588-420A-82ac-dc2d9b1222ff9, die auf dem Webserver ATL-CS-001.litwareinc.com gefunden wurde:
    
        Approve-CsDeviceUpdateRule -Identity service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9

</div>

<div>

## <a name="to-approve-multiple-device-update-rules"></a>So genehmigen Sie mehrere geräteaktualisierungsregeln

  - Dieser Befehl genehmigt alle geräteaktualisierungsregeln für Geräte mit Microsoft-Branding:
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Approve-CsDeviceUpdateRule

</div>

Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet " [genehmigen-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) ".

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Importieren von geräteaktualisierungsregeln in lync Server 2013](lync-server-2013-import-device-update-rules.md)  
[Wiederherstellen einer geräteaktualisierungsregel in lync Server 2013](lync-server-2013-restore-a-device-update-rule.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

