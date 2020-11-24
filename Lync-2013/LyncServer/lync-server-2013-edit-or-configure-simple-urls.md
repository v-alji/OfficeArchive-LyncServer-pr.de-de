---
title: 'Lync Server 2013: Bearbeiten oder Konfigurieren einfacher URLs'
description: 'Lync Server 2013: Bearbeiten oder konfigurieren einfacher URLs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edit or configure simple URLs
ms:assetid: 0008aeea-4ae9-4e36-83cd-ef7ff7b6e128
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398063(v=OCS.15)
ms:contentKeyID: 48183216
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9152a65083f71510f4cdb1189b3982afdd68b4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393783"
---
# <a name="edit-or-configure-simple-urls-in-lync-server-2013"></a>Bearbeiten oder Konfigurieren einfacher URLs in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-02-04_

Für dieses Verfahren ist keine Mitgliedschaft in einem lokalen Administrator oder einer privilegierten Domänengruppe erforderlich. Melden Sie sich als Standardbenutzer an einem Computer an.

Lync Server 2013 verwendet einfache URLs, um interne und externe Anrufe an Dienste auf dem Front-End-Server oder an den Director weiterzuleiten, falls einer bereitgestellt wurde. Weitere Informationen zu einfachen URLs finden Sie unter [Planen einfacher URLs in lync Server 2013](lync-server-2013-planning-for-simple-urls.md) in der Planungsdokumentation. Sie können das Format für ihre einfachen URLs aus verschiedenen Optionen auswählen. Ausführliche Informationen zu diesen Optionen finden Sie unter [DNS-Anforderungen für einfache URLs in lync Server 2013](lync-server-2013-dns-requirements-for-simple-urls.md) in der Planungsdokumentation.

Standardmäßig werden einfache URLs in Form von (beispielsweise der Einwahl einfachen URL) https://dialin konfiguriert:\<SIP Domain\>

<div>

## <a name="to-configure-simple-urls"></a>So konfigurieren Sie einfache URLs

1.  Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den **lync Server** -Knoten, und klicken Sie dann auf **Eigenschaften bearbeiten**.

2.  Wählen Sie im Bereich **Einfache URLs** entweder **Telefonzugriff-URLs:** (Dialin) oder **Besprechungs-URLs:** (Meet) aus und klicken Sie anschließend auf **URL bearbeiten**.

3.  Aktualisieren Sie die URL auf den gewünschten Wert, und klicken Sie dann auf **OK** , um die bearbeitete URL zu speichern. Das hier gezeigte Beispiel hat die Einwahl-URL in geändert https://pool01.contoso.net/dialin .

4.  Bearbeiten Sie ggf. auch die Besprechungs-URL, indem Sie dieselben Schritte ausführen.

</div>

<div>

## <a name="to-define-the-optional-admin-simple-url"></a>So definieren Sie die optionale einfache URL für den administrativen Zugriff

1.  Klicken Sie im Topologie-Generator mit der rechten Maustaste auf den **lync Server** -Knoten, und klicken Sie dann auf **Eigenschaften bearbeiten**.

2.  Geben Sie im Feld **Administratorzugriff-URL** die einfache URL ein, die Sie für den administrativen Zugriff auf die lync Server 2013-Systemsteuerung benötigen, und klicken Sie dann auf **OK**.
    
    <div>
    

    > [!TIP]  
    > Es wird empfohlen, die einfachstmögliche URL als Verwaltungs-URL zu verwenden. Die einfachste Option ist <STRONG> https://admin .</STRONG> &lt; Domäne aus &gt; .

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > Wenn Sie eine einfache URL nach der ersten Bereitstellung ändern, müssen Sie beachten, welche Änderungen sich auf Ihre DNS-Datensätze und -Zertifikate für einfache URLs auswirken. Wenn die Änderung Auswirkungen auf die Basis einer einfachen URL hat, müssen Sie auch die DNS-Einträge und Zertifikate ändern. Wenn Sie beispielsweise https://lync.contoso.com/Meet https://meet.contoso.com die Basis-URL von lync.contoso.com in Meet.contoso.com ändern, müssen Sie die DNS-Einträge und Zertifikate so ändern, dass Sie auf Meet.contoso.com verweisen. Wenn Sie die einfache URL von in geändert haben https://lync.contoso.com/Meet https://lync.contoso.com/Meetings , bleibt die Basis-URL von lync.contoso.com unverändert, sodass keine DNS-oder Zertifikat Änderungen erforderlich sind. Wenn Sie jedoch einen einfachen URL-Namen ändern, müssen Sie das Cmdlet <STRONG>enable-CsComputer</STRONG> auf jedem Director und Front-End-Server ausführen, um die Änderung zu registrieren.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Planung für einfache URLs in Lync Server 2013](lync-server-2013-planning-for-simple-urls.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

