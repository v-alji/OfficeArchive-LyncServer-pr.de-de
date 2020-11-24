---
title: 'Lync Server 2013: Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte'
description: 'Lync Server 2013: Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394378"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a>Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-10-02_

Zum Erstellen eines Konferenzraum Objekts erstellen Sie zunächst ein Active Directory-Benutzerkonto, um das Gerät darzustellen. Verwenden Sie dann das Cmdlet **enable-CsMeetingRoom** , damit dieses Konto als Konferenzgerät funktioniert. Wenn Sie die Eigenschaften eines vorhandenen Konferenz Geräts ändern müssen, verwenden Sie das Cmdlet " **Satz-CsMeetingRoom** ".

Diese Cmdlets können entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.

<div>


> [!NOTE]  
> Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a>Erstellen eines Konferenz Geräts

  - Nachdem Sie das Active Directory-Benutzerkonto erstellt haben, das das neue Konferenzgerät darstellt, aktivieren Sie es mithilfe des Cmdlets **enable-CsMeetingRoom** . Stellen Sie sicher, dass Sie a) die Konferenzgeräte Identität, b) den Registrar-Pool, in dem das Raumkonto verwaltet wird, und c) die SIP-Adresse einbeziehen, die diesem Konto zugewiesen werden soll. Beispiel:
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a>Ändern eines Konferenz Geräts

  - Verwenden Sie das Cmdlet " **CsMeetingRoom** ", um die Eigenschaftswerte eines vorhandenen Konferenz Geräts zu ändern. Mit dem folgenden Befehl wird beispielsweise die Telefonnummer (LineUri) aktualisiert, die einem Konferenzgerät zugeordnet ist:
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

Ausführliche Informationen finden Sie in den Hilfethemen zum Cmdlet [enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) und dem Cmdlet " [Satz-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) ".

</div>

</div>

<span> </span>

</div>

</div>

</div>

