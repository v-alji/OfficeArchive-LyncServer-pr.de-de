---
title: Entfernen von BackCompatSite
description: Entfernen Sie BackCompatSite.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove BackCompatSite
ms:assetid: 039650e3-541b-45c2-a682-c4fa08423118
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204637(v=OCS.15)
ms:contentKeyID: 48183265
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 809324320ec1869ac0c9d324b8fc270a3cf8f174
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440307"
---
# <a name="remove-backcompatsite"></a>Entfernen von BackCompatSite

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-28_

Nachdem alle Pools deaktiviert und alle Edgeserver deinstalliert wurden, führen Sie den Assistenten zum Zusammenführen des Topologie-Generators aus, um den **BackCompatSite** zu entfernen.

<div>

## <a name="to-remove-backcompat-site-from-topology-builder"></a>So entfernen Sie die backcompat-Website aus dem Topologie-Generator

1.  Öffnen Sie eine vorhandene Bereitstellung vom Topologie-Generator.

2.  Klicken Sie im Menü **Aktion** auf **2007 R2-Topologie zusammenführen**.

3.  Klicken Sie auf **Weiter**, um fortzufahren.

4.  Stellen Sie auf der Seite **Legacy Edge angeben** sicher, dass die Liste der Edgeserver leer ist. Wenn die Liste nicht leer ist, verwenden Sie die Schaltfläche **Entfernen** , um alle Legacy-Edgeserver zu entfernen, und klicken Sie dann auf **weiter**.
    
    ![Assistenten für die Zusammenführungs Topologie, Seite "Edge-Setup" angeben](images/JJ204637.fb35a59a-711e-4259-b177-7311df1fed3c(OCS.15).jpg "Assistenten für die Zusammenführungs Topologie, Seite "Edge-Setup" angeben")  

5.  Klicken Sie auf der Seite **interne SIP-Porteinstellung angeben** auf **weiter**.

6.  Klicken Sie auf der Seite **Zusammenfassung** auf **weiter** , um mit dem Zusammenführen der Topologien zu beginnen, um die Legacy Website zu entfernen.

7.  Überprüfen Sie in der Spalte **Status** , ob der Wert **erfolgreich** ist, und klicken Sie dann auf **Fertig stellen** , um den Assistenten zu schließen.

8.  Erweitern Sie im linken Bereich des Topologie-Generators die BackCompatSite, und stellen Sie sicher, dass keine Server aufgelistet sind.

9.  Klicken Sie mit der rechten Maustaste auf das **BackCompatSite**, und klicken Sie dann auf **Löschen**.

10. Wählen Sie im **Topologie-Generator** den **lync-Server** mit dem höchsten Knoten aus.

11. Wählen Sie im Menü **Aktion** die Option **Topologie veröffentlichen** aus, und klicken Sie dann auf **weiter**.

12. Klicken Sie nach Abschluss des **Veröffentlichungs-Assistenten** auf **Fertig stellen** , um den Assistenten zu schließen.

</div>

</div>

<span> </span>

</div>

</div>

</div>

