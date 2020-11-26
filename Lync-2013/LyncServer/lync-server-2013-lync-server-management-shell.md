---
title: 'Lync Server 2013: lync Server-Verwaltungsshell'
description: 'Lync Server 2013: lync Server-Verwaltungsshell.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync Server Management Shell
ms:assetid: 674b523b-c0b7-4ed6-9e67-afa6e8ac7e12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398474(v=OCS.15)
ms:contentKeyID: 48184386
ms.date: 09/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45727c42899defcf20ce36e2a27a9268a52ecd71
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426265"
---
# <a name="lync-server-2013-management-shell"></a>Verwaltungsshell für Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2017-09-20_

<div>


> [!NOTE]  
> Die Skype for Business-Cmdlet-Referenz wurde in docs.Microsoft.com verschoben. Wenn Sie auf die Links unten klicken, gelangen Sie zur neuen docs.Microsoft.com-Seite. Der Inhalt wird nun über GitHub freigegeben und steht für Community-Beiträge zur Verfügung. Möchten Sie einen Beitrag leisten? Schauen Sie sich die Readme-Datei im Repo hier an: <A href="https://github.com/microsoftdocs/office-docs-powershell">https://github.com/MicrosoftDocs/office-docs-powershell</A>



</div>

Microsoft lync Server 2010 hat einen umfangreichen Satz neuer und verbesserter Features im Vergleich zu den in Microsoft Office Communications Server 2007 R2 verfügbaren Funktionen eingeführt. Eine Verbesserung ist die Art und Weise, in der Sie Ihre Implementierung verwalten. So gibt es beispielsweise eine neue Benutzeroberfläche, die so genannte lync Server-Systemsteuerung, die eine große Schicht von dem entspricht, was die meisten Personen mit der Microsoft Management Console gewohnt sind. Eine weitere wesentliche Verbesserung der Verwaltbarkeit ist die Einbeziehung von Windows PowerShell.

Mit Windows PowerShell können Sie Microsoft-Anwendungen über die Befehlszeile verwalten. Enthalten sind eine Befehlszeilenumgebung, produktspezifische Befehle und eine vollständige Skriptsprache. Windows PowerShell wurde erst spät in 2006 als herunterladbare Version für das Windows-Betriebssystem eingeführt und als Befehlszeilenschnittstelle für die Verwaltbarkeit von Microsoft Exchange Server 2007 integriert. Von diesem Zeitpunkt an wurde es weiter ausgebaut, und es wurde in die meisten Microsoft-Serverprodukte integriert, wobei es sich um die neueste Microsoft lync Server 2013 handelt. Lync Server 2010 hat nahezu 550 produktspezifische Cmdlets eingeführt, mit denen Sie alle Aspekte Ihrer Bereitstellung verwalten können.

Die folgenden Abschnitte enthalten eine Liste der Cmdlets sowie Beschreibungen der Cmdlets. Diese Informationen stehen auch direkt über die Befehlszeile zur Verfügung. Geben Sie einfach Folgendes an der Eingabeaufforderung der lync Server-Verwaltungsshell ein:

    Get-Help <cmdlet name> -Full

Wenn Sie beispielsweise Hilfeinformationen zum Cmdlet **New-CsVoicePolicy** von der Befehlszeile aus abrufen möchten, geben Sie folgenden Befehl ein:

    Get-Help New-CsVoicePolicy -Full

Wissenswertes zu Windows PowerShell in lync Server 2013:

  - Zum Ausführen der lync Server-Cmdlets öffnen Sie die lync Server-Verwaltungsshell.
    
    <div>
    

    > [!WARNING]  
    > Wenn Sie ein Windows PowerShell-Fenster anstelle der lync Server-Verwaltungsshell öffnen, können Sie die lync Server-Cmdlets standardmäßig nicht ausführen. Wenn Sie die lync Server-Cmdlets in Windows PowerShell ausführen möchten, geben Sie zuerst Folgendes an der Windows PowerShell-Eingabeaufforderung ein:<BR>Import-Module lync

    
    </div>

  - Die lync Server-Verwaltungsshell wird automatisch auf jedem lync Server Enterprise Edition-Front-End-Server oder Standard Edition-Server installiert.

  - Neue und aktualisierte Informationen, Beispielskripts und Hilfe für erste Schritte und weitere Informationen zu Windows PowerShell-und Microsoft lync Server 2013-Cmdlets finden Sie im lync Server Windows PowerShell-Blog [https://go.microsoft.com/fwlink/p/?linkId=203150](https://go.microsoft.com/fwlink/p/?linkid=203150) .

</div>

<span> </span>

</div>

</div>

</div>

