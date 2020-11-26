---
title: 'Lync Server 2013: Ändern einer Archivierungsrichtlinie zum Aktivieren oder Deaktivieren der Archivierung interner oder externer Kommunikation für Ihre Organisation, Websites oder Benutzer'
description: 'Lync Server 2013: Ändern einer Archivierungsrichtlinie, um die Archivierung interner oder externer Kommunikation für Ihre Organisation, ihre Websites oder Ihre Benutzer zu aktivieren oder zu deaktivieren.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing an Archiving policy to enable or disable Archiving of internal or external communications for your organization, sites, or users
ms:assetid: b85dc3fb-8ebd-4e3c-ac90-fc79270ac867
ms:mtpsurl: https://technet.microsoft.com/library/Gg182576(v=OCS.15)
ms:contentKeyID: 48185234
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee24f3d72e447a778d434994dff1795baa04d420
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435180"
---
# <a name="changing-an-archiving-policy-in-lync-server-2013-to-enable-or-disable-archiving-of-internal-or-external-communications-for-your-organization-sites-or-users"></a>Ändern einer Archivierungsrichtlinie in lync Server 2013, um die Archivierung interner oder externer Kommunikation für Ihre Organisation, ihre Websites oder Ihre Benutzer zu aktivieren oder zu deaktivieren

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
> Wenn Sie die Microsoft Exchange-Integration für Ihre Bereitstellung aktiviert haben, Steuern Exchange-Richtlinien, ob die Archivierung für die Benutzer aktiviert ist, die sich in Exchange 2013 befinden, und dass ihre Postfächer In-Place halten. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</A> in der Bereitstellungsdokumentation.<BR>Sie sollten alle geeigneten Optionen in den Archivierungs Konfigurationen angeben, bevor Sie die Archivierung aktivieren. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-managing-archiving-configuration-options-for-your-organization-sites-and-pools.md">Verwalten von Archivierungs Konfigurationsoptionen in lync Server 2013 für Ihre Organisation, Websites und Pools</A> in der Betriebsdokumentation.



</div>

<div>

## <a name="to-change-an-archiving-policy"></a>So ändern Sie eine Archivierungsrichtlinie

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsArchivingAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie auf der linken Navigationsleiste auf **Überwachung und Archivierung** und anschließend auf **Archivierungsrichtlinie**.

4.  Führen Sie in der Liste der Richtlinie einen der folgenden Schritte aus:
    
      - Um die Richtlinie für Ihre gesamte Bereitstellung zu ändern, klicken Sie in der Liste der Richtlinien auf **Global**, klicken Sie auf **Bearbeiten** und anschließend auf **Details anzeigen**.
    
      - Um die Richtlinie für einen einzelnen Standort zu ändern, klicken Sie in der Liste der Richtlinien auf den Standortnamen, klicken Sie auf **Bearbeiten** und klicken Sie dann auf **Details anzeigen**.
    
      - Um die Richtlinie für einen einzelnen Benutzer oder eine Benutzergruppe zu ändern, klicken Sie in der Liste der Richtlinien auf den Benutzer- oder Gruppennamen, klicken Sie auf **Bearbeiten** und klicken Sie dann auf **Details anzeigen**.

5.  Führen Sie auf der Seite **Bearbeiten der Archivierungsrichtlinien** die folgenden Aktionen aus:
    
      - Markieren Sie das Kontrollkästchen **Interne Kommunikation archivieren** oder entfernen Sie die Markierung, um die interne Archivierung für die Richtlinie zu aktivieren oder zu deaktivieren.
    
      - Markieren Sie das Kontrollkästchen **Externe Kommunikation archivieren** oder entfernen Sie die Markierung, um die externe Archivierung für die Richtlinie zu aktivieren oder zu deaktivieren.

6.  Klicken Sie auf **Commit ausführen**.
    
    <div>
    

    > [!IMPORTANT]  
    > Die Einstellungen einer Benutzerrichtlinie gelten nur für bestimmte Benutzer und Benutzergruppen, auf die Sie die Richtlinie anwenden. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-applying-an-archiving-policy-to-users.md">Anwenden einer Archivierungsrichtlinie auf Benutzer in lync Server 2013</A>

    
    </div>

</div>

<div>

## <a name="enabling-and-disabling-archiving-by-using-windows-powershell-cmdlets"></a>Aktivieren und Deaktivieren der Archivierung mithilfe von Windows PowerShell-Cmdlets

Die Archivierung kann mithilfe des Cmdlets " **Satz-CsArchivingPolicy** " (für interne und externe Kommunikationssitzungen) aktiviert und deaktiviert werden. Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden. Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .

<div>

## <a name="to-enable-the-archiving-of-internal-communication-sessions"></a>So aktivieren Sie die Archivierung interner Kommunikationssitzungen

  - Um die Archivierung interner Kommunikationssitzungen zu aktivieren, setzen Sie den Wert der **ArchiveInternal** -Eigenschaft auf true ($true). Beispiel:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-external-communication-sessions"></a>So aktivieren Sie die Archivierung externer Kommunikationssitzungen

  - Um die Archivierung externer Kommunikationssitzungen zu aktivieren, setzen Sie den Wert der **ArchiveExternal** -Eigenschaft auf true ($true). Beispiel:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveExternal $True

</div>

<div>

## <a name="to-enable-the-archiving-of-both-internal-and-external-communication-sessions"></a>So aktivieren Sie die Archivierung interner und externer Kommunikationssitzungen

  - Um die Archivierung sowohl interner als auch externer Kommunikationssitzungen zu aktivieren, müssen Sie die **ArchiveInternal** -Eigenschaft und die **ArchiveExternal** -Eigenschaft auf "true" festlegen:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $True -ArchiveExternal $True

</div>

<div>

## <a name="to-disable-archiving"></a>So deaktivieren Sie die Archivierung

  - Um die Archivierung insgesamt zu deaktivieren, setzen Sie die Eigenschaften **ArchiveInternal** und **ArchiveExternal** auf false ($false). Beispiel:
    
        Set-CsArchivingPolicy -Identity "global" -ArchiveInternal $False -ArchiveExternal $False

</div>

Weitere Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsArchivingPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsArchivingPolicy) ".

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

