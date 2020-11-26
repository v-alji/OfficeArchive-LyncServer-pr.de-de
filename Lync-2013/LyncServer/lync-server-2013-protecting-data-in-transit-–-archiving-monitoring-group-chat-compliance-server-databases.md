---
title: 'Lync Server 2013: Schützen von Daten während der Übertragung – Archivierungs-, Überwachungs- und Gruppenchat-Konformitätsserverdatenbanken'
description: 'Lync Server 2013: Schützen von Daten in Transit – Archivierung, Überwachung, Gruppen-Chat-Compliance Server-Datenbanken.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Protecting data in transit – archiving, monitoring, group chat compliance server databases in Lync Server 2013
ms:assetid: ea219705-1015-43a7-890b-e7e67b451e7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518336(v=OCS.15)
ms:contentKeyID: 62625494
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: d4d4127bb0404bca376da450d0b0c58cf3b76560
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436846"
---
# <a name="protecting-data-in-transit--archiving-monitoring-group-chat-compliance-server-databases-in-lync-server-2013"></a>Schützen von Daten während der Übertragung – Archivierungs-, Überwachungs- und Gruppenchat-Konformitätsserverdatenbanken in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-12-05_

Der Microsoft lync Server 2013-Archivierungsserver und der Überwachungsserver verwenden den Message Queuing-Dienst (auch als MSMQ-Dienst bezeichnet), um Daten Nachrichten vom Sammelpunkt zu den Repository-Servern zu sammeln und zuverlässig zu verschieben. Der Kompatibilitätsdienst sammelt Daten in Verbindung mit dem Gruppen-Chat Server, der auch Message Queuing verwendet.

In lync Server 2013 gibt es keinen internen Schutz für Daten auf dem Draht; Wenn es jedoch eine Anforderung zum Sichern dieses Datenverkehrs gibt, kann der Message Queuing-Dienst eine Verschlüsselung auf Nachrichtenebene in der sendenden Nachrichtenwarteschlange bereitstellen. Dies erfolgt mithilfe von Zertifikaten, die von den Active Directory-Domänendiensten verwaltet werden. Ausführliche Informationen finden Sie in Anhang D: Message Queuing und Internetkommunikation in Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?LinkId=145238](https://go.microsoft.com/fwlink/p/?linkid=145238) oder Anhang I: Message Queuing und Internetkommunikation in Windows Server 2008 R2 unter [https://go.microsoft.com/fwlink/p/?LinkId=211883](https://go.microsoft.com/fwlink/p/?linkid=211883) für Windows Server 2008 R2.

</div>

<span> </span>

</div>

</div>

</div>

