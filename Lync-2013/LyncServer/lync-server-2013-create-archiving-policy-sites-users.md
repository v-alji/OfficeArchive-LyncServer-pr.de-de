---
title: 'Lync Server 2013: Erstellen einer Archivierungsrichtlinie zum Aktivieren oder Deaktivieren der Archivierung interner oder externer Kommunikation für bestimmte Websites oder Benutzer'
description: 'Lync Server 2013: Erstellen einer Archivierungsrichtlinie, um die Archivierung interner oder externer Kommunikation für bestimmte Websites oder Benutzer zu aktivieren oder zu deaktivieren.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating an Archiving policy to enable or disable Archiving of internal or external communications for specific sites or users
ms:assetid: 5864793a-ba72-470c-bb5b-9fb41e968896
ms:mtpsurl: https://technet.microsoft.com/library/Gg398385(v=OCS.15)
ms:contentKeyID: 48184193
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a23f952229df9fe950f2666914263a7cf46595f4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431988"
---
# <a name="creating-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-specific-sites-or-users"></a>Erstellen einer Archivierungsrichtlinie in lync Server 2013 zum Aktivieren oder Deaktivieren der Archivierung interner oder externer Kommunikation für bestimmte Websites oder Benutzer

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-23_

In lync Server 2013 verwenden Sie Richtlinien, um die Archivierung für die interne Kommunikation und die externe Kommunikation für Benutzer zu aktivieren und zu deaktivieren, die in lync Server 2013 gehostet werden. Dies umfasst die folgenden Archivierungsrichtlinien:

  - Eine globale Richtlinie, die standardmäßig beim Bereitstellen von lync Server 2013 erstellt wird.

  - Optionale Richtlinien auf Websiteebene und auf Benutzerebene, die Sie erstellen und verwenden können, um anzugeben, wie die Archivierung für bestimmte Websites oder Benutzer implementiert wird.

Sie haben zunächst Archivierungsrichtlinien eingerichtet, wenn Sie die Archivierung bereitstellen, Sie können aber nach der Bereitstellung Richtlinien ändern, hinzufügen und löschen. In der lync Server 2013-Systemsteuerung können Sie die Seite **Archivierungsrichtlinie** der Gruppe **Archivierung und Überwachung** verwenden, um Richtlinien auf globaler Ebene, auf Websiteebene und auf Benutzerebene zu verwalten. Wenn Sie Ihren lync-Server Speicher in Exchange 2013-Speicher integrieren, haben die Exchange-Benutzerrichtlinien Vorrang vor den Archivierungsrichtlinien für lync Server 2013.

Einzelheiten zur Implementierung von Richtlinien, einschließlich der Hierarchie der Richtlinien, finden Sie unter [Funktionsweise der Archivierung in lync Server 2013](lync-server-2013-how-archiving-works.md) in der Planungsdokumentation, Bereitstellungsdokumentation oder in der Betriebsdokumentation.

<div>


> [!NOTE]
> Um die Implementierung der Archivierung zu steuern, müssen Sie Optionen in Archivierungs Konfigurationen angeben, beispielsweise ob Sie Chatnachrichten oder Konferenzen archivieren, die Verwendung des kritischen Modus und Bereinigungsoptionen verwenden möchten. Standardmäßig sind keine Optionen in der globalen Archivierungskonfiguration oder einer Standort-oder Pool Archivierungskonfiguration aktiviert. Sie sollten alle geeigneten Optionen in den Archivierungs Konfigurationen angeben, bevor Sie die Archivierung für die interne oder externe Kommunikation in den Archivierungsrichtlinien aktivieren. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Verwalten von Archivierungs Konfigurationsoptionen in lync Server 2013 für Ihre Organisation, Websites und Pools</A> in der Betriebsdokumentation.<BR>Wenn Sie die Microsoft Exchange-Integration für Ihre Bereitstellung aktiviert haben, Steuern Exchange-Richtlinien, ob die Archivierung für die Benutzer aktiviert ist, die sich in Exchange 2013 befinden, und dass ihre Postfächer In-Place halten. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</A> in der Bereitstellungsdokumentation.



</div>

<div>

## <a name="to-create-an-archiving-policy-for-a-site-or-users"></a>So erstellen Sie eine Archivierungsrichtlinie für eine Website oder für Benutzer

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsArchivingAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie auf der linken Navigationsleiste auf **Überwachung und Archivierung** und anschließend auf **Archivierungsrichtlinie**.

4.  Klicken Sie auf **Neu** und führen Sie eine der folgenden Aktionen aus:
    
      - Wenn Sie eine Archivierungsrichtlinie auf Websiteebene erstellen möchten, klicken Sie auf **Website Richtlinie** , und klicken Sie dann unter **Website auswählen** auf die Website, auf die die Richtlinie angewendet werden soll.
    
      - Um eine Archivierungsrichtlinie auf Benutzerebene zu erstellen, klicken Sie auf **Benutzerrichtlinie**.

5.  Führen Sie unter **Neue Archivierungsrichtlinie** die folgenden Aktionen aus:
    
      - Geben Sie unter **Name** einen Namen für die neue Richtlinie an (z. B. „externalContoso“).
    
      - Geben Sie unter **Beschreibung** Einzelheiten über den Zweck der Richtlinie an (z. B. Archivierungsrichtlinie für externe Benutzer von Contoso).
    
      - Aktivieren oder deaktivieren Sie das Kontrollkästchen **Interne Kommunikation archivieren**, um die Archivierung der Kommunikation mit internen Benutzern zu aktivieren oder zu deaktivieren.
    
      - Aktivieren oder deaktivieren Sie das Kontrollkästchen **Externe Kommunikation archivieren**, um die Archivierung der externen Kommunikation zu aktivieren oder zu deaktivieren.

6.  Klicken Sie auf **Commit ausführen**.
    
    <div>
    

    > [!IMPORTANT]
    > Die Einstellungen einer Benutzerrichtlinie gelten nur für bestimmte Benutzer und Benutzergruppen, auf die Sie die Richtlinie anwenden. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Anwenden einer Archivierungsrichtlinie auf Benutzer in lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="creating-an-archiving-policy-by-using-windows-powershell-cmdlets"></a>Erstellen einer Archivierungsrichtlinie mithilfe von Windows PowerShell-Cmdlets

Archivierungsrichtlinien können mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsArchivingPolicy** erstellt werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden. Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-create-a-new-archiving-policy-at-the-site-scope"></a>So erstellen Sie eine neue Archivierungsrichtlinie im Website Bereich

  - Mit diesem Befehl wird eine neue Archivierungsrichtlinie für den Standort „Redmond“ erstellt:
    
        New-CsArchivingPolicy -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-at-the-per-user-scope"></a>So erstellen Sie eine neue Archivierungsrichtlinie im Bereich "pro Benutzer"

  - Wenn Sie eine neue Archivierungsrichtlinie auf Benutzerebene erstellen möchten, geben Sie beim Erstellen der Richtlinie einfach eine eindeutige Identität an:
    
        New-CsArchivingPolicy -Identity "RedmondArchivingPolicy"

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-internal-communication-sessions"></a>So erstellen Sie eine neue Archivierungsrichtlinie zum Aktivieren der Archivierung interner Kommunikationssitzungen

  - Da in den vorhergehenden Befehlen keine Parameter (mit Ausnahme des Parameters zur obligatorischen Identität) angegeben wurden, verwenden die neuen Richtlinien die Standardwerte für alle ihre Eigenschaften. Zum Erstellen von Richtlinien, die unterschiedliche Eigenschaftswerte verwenden, fügen Sie einfach den entsprechenden Parameter-und Parameterwert hinzu. Wenn Sie beispielsweise eine Archivierungsrichtlinie erstellen möchten, die das Archivieren interner Chat-Sitzungen ermöglicht, verwenden Sie einen Befehl wie den folgenden:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True

</div>

<div>

## <a name="to-create-a-new-archiving-policy-that-enables-archiving-of-both-internal-and-external-communication-sessions"></a>So erstellen Sie eine neue Archivierungsrichtlinie zur Archivierung interner und externer Kommunikationssitzungen

  - Mehrere Eigenschaftenwerte können durch Einschließen mehrerer Parameter geändert werden. Mit diesem Befehl wird beispielsweise die neue Richtlinie für die Archivierung interner und externer Chat-Sitzungen konfiguriert:
    
        New-CsArchivingPolicy -Identity "site:Redmond" -ArchiveInternal $True -ArchiveExternal $True

</div>

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [New-CsArchivingPolicy](https://technet.microsoft.com/library/Gg399032(v=OCS.15)) .

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Verwalten der Archivierung interner und externer Kommunikation in lync Server 2013](lync-server-2013-managing-the-archiving-of-internal-and-external-communications.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

