---
title: 'Lync Server 2013: Konfigurieren der Orbittabelle für das Parken von Anrufen'
description: 'Lync Server 2013: Konfigurieren der Umlaufbahn Tabelle des Anruf Parks'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Call Park orbit table
ms:assetid: e5cc0c19-7b2c-48e7-a21d-cfb23c842f0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399020(v=OCS.15)
ms:contentKeyID: 48185666
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce9fb35c2958a426888d83d075064c88ddae4bfa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433633"
---
# <a name="configure-the-call-park-orbit-table-in-lync-server-2013"></a>Konfigurieren der Orbittabelle für das Parken von Anrufen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-10_

Call Park verwendet Umlaufbahnen für Park Anrufe. Bevor Benutzer Anrufe parken und abrufen können, müssen Sie die Umlaufbahn Tabelle des Anruf Parks konfigurieren. Sie müssen die Bereiche der Durchwahlnummern (Orbits) angeben, die Ihre Organisation für Park Anrufe reserviert, und den Arbeitsplan für diese Bereiche definieren, indem Sie angeben, welcher Anruf Park Pool für jeden Bereich zuständig ist. Wenn Sie Umlaufbahn Bereiche definieren, besteht das Ziel darin, genügend Umlaufbahnen zu haben, damit eine Umlaufbahn nicht zu schnell wieder verwendet wird, aber nicht so viele Umlaufbahnen, dass Sie die Anzahl der für Benutzer oder andere Dienste verfügbaren Erweiterungen einschränken. Sie können für jeden lync Server-Pool, in dem die Park-Anwendung bereitgestellt wird, mehrere orbitbereiche für den Anruf Bereich erstellen. Jeder Orbit-Bereich für das Parken von Anrufen muss einen global eindeutigen Namen und einen eindeutigen Satz von Erweiterungen aufweisen.

<div>


> [!IMPORTANT]  
> Ein Orbitbereich umfasst normalerweise 100 oder weniger Orbits. Jeder Bereich kann deutlich größer sein, solange der Höchstwert von 10.000 Orbits pro Bereich nicht überschritten wird und Sie über weniger als 50.000 Orbits pro Pool verfügen. Ist ein Bereich zu klein, werden die Orbits zu schnell wiederverwendet.



</div>

Verwenden Sie für Ihre Orbitbereiche Blöcke virtueller Durchwahlnummern (Durchwahlnummern, denen kein Benutzer oder Telefon zugewiesen ist).

<div>


> [!NOTE]  
> Das Zuweisen von Direktwahlnummern (DID) als Orbit-Nummern in der Orbit-Tabelle des Anruf Parks wird nicht unterstützt.



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

[Erstellen oder Ändern eines orbitbereichs für einen Anruf Bereich in lync Server 2013](lync-server-2013-create-or-modify-a-call-park-orbit-range.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

