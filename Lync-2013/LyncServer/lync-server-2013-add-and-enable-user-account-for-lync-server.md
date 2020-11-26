---
title: 'Lync Server 2013: Hinzufügen und Aktivieren des Benutzerkontos für lync Server'
description: 'Lync Server 2013: Hinzufügen und Aktivieren des Benutzerkontos für lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439373"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a>Hinzufügen und Aktivieren des Benutzerkontos für lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-02_

Nachdem Sie ein Benutzerkonto in Active Directory-Benutzer und-Computer aktiviert haben, können Sie die lync Server-Systemsteuerung verwenden, um neue lync Server 2013-Benutzerkonten zu erstellen und zu aktivieren, indem Sie einen Active Directory-Benutzer zu lync Server hinzufügen.

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a>So fügen Sie einen neuen lync Server-Benutzer hinzu und aktivieren ihn

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie in der linken Navigationsleiste auf **Benutzer**.

4.  Klicken Sie auf **Benutzer aktivieren**.

5.  Klicken Sie im Dialogfeld **neuer lync Server-Benutzer** auf **Hinzufügen**.

6.  Geben Sie im Feld Benutzer suchen den gesamten oder den ersten Teil des Namens, den Anzeigenamen, den Vornamen, den **Nachnamen** , den Kontonamen, die e-Mail-Adresse, den Benutzerprinzipalnamen (User Principal Name, UPN) oder die Telefonnummer des gewünschten Active Directory-Benutzerkontos ein, und klicken Sie dann auf **Suchen**.

7.  Wählen Sie in der Tabelle das Konto aus, das Sie zu lync Server hinzufügen möchten, und klicken Sie dann auf **OK**.

8.  Weisen Sie den Benutzer einem Pool zu, geben Sie zusätzliche Details an, und weisen Sie die Richtlinien dem gewünschten Benutzer zu, und klicken Sie dann auf **aktivieren**.

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Deaktivieren oder erneutes Aktivieren des Benutzerkontos für lync Server 2013](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[Entfernen eines Benutzerkontos aus lync Server 2013](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[Aktivieren und Deaktivieren von Benutzern für lync Server 2013](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

