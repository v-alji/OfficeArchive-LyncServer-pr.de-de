---
title: 'Lync Server 2013: Konfigurieren von nicht zugewiesenen Telefonnummern'
description: 'Lync Server 2013: Konfigurieren Sie nicht zugewiesene Telefonnummern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure unassigned phone numbers
ms:assetid: a0650659-dce7-455f-8977-02454bbfa400
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182559(v=OCS.15)
ms:contentKeyID: 48185009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 702f297ea0a77d5e81be8b650a514ea4fa939d32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433584"
---
# <a name="configure-unassigned-phone-numbers-in-lync-server-2013"></a>Konfigurieren von nicht zugewiesenen Telefonnummern in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Mit lync Server können Sie konfigurieren, was mit eingehenden Anrufen an Telefonnummern geschieht, die für Ihre Organisation gültig sind, aber nicht einem Benutzer oder einem Telefon zugewiesen sind. Um die Behandlung solcher Anrufe zu konfigurieren, richten Sie eine nicht zugewiesene Nummern Tabelle ein. Sie können die Tabelle verwenden, um die Anrufe an eine Ankündigungs Anwendung oder an einen Exchange um-Server weiterzuleiten.

Wie Sie die Tabelle nicht zugewiesener Rufnummern konfigurieren, richtet sich danach, wie Sie diese verwenden möchten. Sie können die Tabelle mit allen gültigen Durchwahlnummern für Ihre Organisation konfigurieren, nur mit nicht zugewiesenen Durchwahlnummern oder als eine Kombination beider Nummerntypen. Die Tabelle nicht zugewiesener Rufnummern kann sowohl zugewiesene als auch nicht zugewiesene Rufnummern enthalten, wird jedoch nur ausgelöst, wenn ein Anrufer eine derzeit nicht zugewiesene Rufnummer wählt. Wenn Sie alle gültigen Durchwahlnummern in die Tabelle nicht zugewiesener Nummern aufnehmen, können Sie eine Aktion angeben, die bei Ausscheiden eines Mitarbeiters aus der Organisation ausgeführt werden soll. In diesem Fall ist eine Neukonfiguration der Tabelle nicht erforderlich. Wenn Sie nicht zugewiesene Durchwahlnummern in die Tabelle aufnehmen, können Sie die Aktion anpassen, die für bestimmte Nummern ausgeführt wird. Wenn Sie beispielsweise die Durchwahlnummer für Ihren Kundendienst ändern, können Sie die alte Rufnummer des Kundendiensts in die Tabelle aufnehmen und ihr eine Ansage zuweisen, in der die neue Rufnummer bereitgestellt wird.

<div>


> [!IMPORTANT]  
> Bevor Sie die Tabelle nicht zugewiesene Nummern konfigurieren, müssen Sie bereits eine oder mehrere Ankündigungen definiert oder eine automatische Exchange UM-Telefonzentrale eingerichtet haben. Details zum Erstellen von Ankündigungen finden Sie unter <A href="lync-server-2013-create-an-announcement.md">Erstellen einer Ankündigung in lync Server 2013</A>. Wenn Sie sehen möchten, ob Sie die Exchange um-Einstellungen konfiguriert haben, führen Sie das Cmdlet <STRONG>Get-CsExUmContact</STRONG> aus. Ausführliche Informationen finden Sie unter <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact">Get-CsExUmContact</A>.



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs in lync Server 2013](lync-server-2013-create-or-modify-an-unassigned-number-range.md)

  - [Löschen eines nicht zugewiesenen Nummernbereichs in lync Server 2013](lync-server-2013-delete-an-unassigned-number-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

