---
title: 'Lync Server 2013: Wiederherstellen von Überwachungs-oder Archivierungsdaten'
description: 'Lync Server 2013: Wiederherstellen von Überwachungs-oder Archivierungsdaten'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring monitoring or archiving data
ms:assetid: 60118526-13bb-4b03-803e-6ffae219d436
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202175(v=OCS.15)
ms:contentKeyID: 51541483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 169a5da2d606b97c7cd3f59d6cbae3d4c584e6e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442523"
---
# <a name="restoring-monitoring-or-archiving-data-in-lync-server-2013"></a>Wiederherstellen von Überwachungs-oder Archivierungsdaten in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-18_

Das Wiederherstellen von Überwachungs-und Archivierungsdaten ist nicht erforderlich, um den lync-Server nach einem Fehler in Betrieb zu nehmen. Wenn die Überwachung und Archivierung von Daten jedoch für Ihre Organisation von entscheidender Bedeutung ist, möchten Sie die Daten nach dem erneuten Erstellen der Datenbanken wiederherstellen.

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe von SQL Server Management Studio Archivierungs-oder Überwachungsdaten wiederherstellen.

<div>

## <a name="to-restore-monitoring-or-archiving-data-from-a-backup-file"></a>So stellen Sie die Überwachung oder Archivierung von Daten aus einer Sicherungsdatei wieder her

1.  Melden Sie sich bei dem Server an, den Sie als Mitglied der Gruppe Administratoren auf dem lokalen Computer oder einer Gruppe mit entsprechenden Benutzerrechten wiederherstellen.

2.  Öffnen Sie SQL Server Management Studio: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft SQL Server 2012** oder **Microsoft SQL Server 2008 R2**, und klicken Sie dann auf **SQL Server Management Studio**.

3.  Stellen Sie unter **Herstellen einer Verbindung** mit dem Server eine Verbindung mit der SQL Server-Instanz her, indem Sie mindestens den Namen des Servers und die Authentifizierungsinformationen angeben.

4.  Klicken Sie im **Objekt-Explorer** mit der rechten Maustaste auf **Datenbanken**, und klicken Sie dann auf **Datenbank wiederherstellen**.

5.  Klicken Sie unter **Seite auswählen** auf **Allgemein**, und wählen Sie dann in **zur Datenbank** den Datenbanknamen wie folgt aus:
    
      - Wählen Sie für eine Archivierungsdatenbank **LcsLog** aus.
    
      - Wählen Sie für eine CDR-Datenbank (Call Detail Recording) **LcsCDR** aus.
    
      - Wählen Sie für eine QoE-Datenbank (Quality of Experience) **Datenbank QoEMetrics werden** aus.

6.  Klicken Sie auf **vom Gerät**.

7.  Klicken Sie unter **Wählen Sie die wieder** herzustellenden Sicherungssätze auf die Sicherungsdatei, und klicken Sie dann auf **Wiederherstellen**.

8.  Klicken Sie unter **Seite auswählen** auf **Optionen**, stellen Sie sicher, dass sich der Datendateipfad und der Protokollpfad im richtigen Ordner befinden, und klicken Sie dann auf **OK**.

</div>

<div>

## <a name="to-make-sure-that-access-control-lists-acls-are-correct"></a>So stellen Sie sicher, dass Zugriffssteuerungslisten (ACLs) korrekt sind

1.  Erweitern Sie **Datenbanken**, erweitern Sie die Datenbank Archivierung oder Überwachung, erweitern Sie **Sicherheit**, und erweitern Sie dann **Benutzer**.

2.  Überprüfen Sie, ob die RTCComponentUniversalServices der Domänengruppe als Benutzer vorhanden ist.

3.  Wenn RTCComponentUniversalServices unter **Benutzer** nicht vorhanden ist, gehen Sie folgendermaßen vor:
    
    1.  Klicken Sie mit der rechten Maustaste auf **Benutzer**, und klicken Sie dann auf **neuer Benutzer**.
    
    2.  Geben Sie unter **Anmeldename** den fehlenden Gruppennamen RTCComponentUniversalServices ein.
    
    3.  Wählen Sie unter **Datenbankrollenmitgliedschaft** die Berechtigung **serverRole** aus, und klicken Sie dann auf **OK**.
    
    <div>
    

    > [!NOTE]  
    > Sie müssen den Archivierungs-oder Überwachungsdienst nicht erneut starten.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

