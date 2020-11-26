---
title: 'Lync Server 2013: Konfigurieren des persönlichen Kontaktspeichers auf Clientcomputern'
description: 'Lync Server 2013: Konfigurieren des persönlichen Kontaktspeichers auf Clientcomputern'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the personal contacts store on client computers
ms:assetid: ec69a6cb-07f2-4057-9544-55035f83eeae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721922(v=OCS.15)
ms:contentKeyID: 49733857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1040b3eb9aa38e3e0c537d690b9292ab8f1ead2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432520"
---
# <a name="configuring-the-personal-contacts-store-on-client-computers-for-lync-server-2013"></a>Konfigurieren des Speichers für persönliche Kontakte auf Clientcomputern für lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-02-05_

Wenn Sie Microsoft lync Server 2013 und Microsoft Exchange Server 2013 integrieren, wird empfohlen, den persönlichen Kontaktspeicher auf allen Clientcomputern zu konfigurieren, auf denen Microsoft lync 2010 ausgeführt wird. Insbesondere sollten Sie lync so konfigurieren, dass Exchange als persönlicher Kontaktspeicher verwendet wird, und gleichzeitig sicherstellen, dass Benutzer diese Entscheidung nicht außer Kraft setzen können. Dies ist nur dann möglich, wenn Sie auf jedem Clientcomputer einen Registrierungswert erstellen und konfigurieren.

Beachten Sie, dass dies auf Computern, auf denen lync 2013 ausgeführt wird, nicht erforderlich ist.

Zum Konfigurieren dieses Werts auf einem einzelnen Computer führen Sie die folgenden Schritte aus:

1.  Klicken Sie auf dem Clientcomputer im Menü **Start** auf **Ausführen**.

2.  Geben Sie im Dialogfeld **Ausführen** den Befehl regedit ein und drücken Sie dann die EINGABETASTE.

3.  Erweitern Sie im Registrierungs-Editor **HKEY \_ lokaler \_ Computer**, erweitern Sie **Software**, erweitern Sie **Richtlinien**, erweitern Sie **Microsoft**, und erweitern Sie dann **Communicator**.

4.  Klicken Sie mit der rechten Maustaste auf **Communicator**, zeigen Sie auf **Neu** und klicken Sie auf **DWORD-Wert (32-Bit)**.

5.  Geben Sie nach dem Erstellen des neuen Werts **PersonalContactStoreOverride** ein und drücken Sie die EINGABETASTE, um den Wert umzubenennen.

6.  Stellen Sie sicher, dass der Wert von PersonalContactStoreOverride 0 ist, und schließen Sie dann den Registrierungs-Editor.

Wenn Sie die gleiche Änderung auf mehreren Computern durchführen müssen, können Sie dazu ein benutzerdefiniertes Gruppenrichtlinienobjekt erstellen. Ausführliche Informationen finden Sie in der Gruppenrichtlinien-Dokumentation unter [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543) .

</div>

<span> </span>

</div>

</div>

</div>

