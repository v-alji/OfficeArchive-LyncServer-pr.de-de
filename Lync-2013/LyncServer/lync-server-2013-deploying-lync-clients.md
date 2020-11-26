---
title: 'Lync Server 2013: Bereitstellen von lync-Clients'
description: 'Lync Server 2013: Bereitstellen von lync-Clients.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync clients
ms:assetid: 3d10abf2-d484-4fa0-8f10-4a5f9dfba4f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204827(v=OCS.15)
ms:contentKeyID: 48183925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 09b501fc721ac880c5cf7da0293e3aa9c6443722
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429986"
---
# <a name="deploying-lync-clients-in-lync-server-2013"></a>Bereitstellen von lync-Clients in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-03_

Lync 2013 führt einen anderen Ansatz für die Clientbereitstellung ein. In einer Abweichung von vorherigen Versionen verfügt lync 2013 nicht mehr über ein eigenes Installationsprogramm. Stattdessen ist lync im Office 2013-Setupprogramm enthalten. Wenn Sie lync 2013 für Ihre Benutzer bereitstellen möchten, können Sie die Office 2013-Installationsmethoden und Anpassungstools verwenden.

  - **Office 2013 Windows Installer** ist ein Windows Installer-basiertes Installationspaket, das aus mehreren MSI-Dateien besteht. Ein MSI-Paket mit sprachneutralem Kern wird mit einem oder mehreren sprachenspezifischen Paketen zu einem vollständigen Produkt kombiniert. Setup fügt die einzelnen Pakete zusammen und führt während und nach der Installation von Office auf den Computern der Benutzer Anpassungs- und Wartungsaufgaben aus. In den Themen in diesem Abschnitt wird beschrieben, wie Sie das Office 2013 Windows Installer zum Bereitstellen von lync 2013 verwenden und anpassen.

  - **Office 2013 Klick-und-Los** ist ein Installationsprogramm, das die Office-Setupdateien aus dem Microsoft 365 Admin Center an den Benutzer streamt. Administratoren können die Installation mithilfe des Office-Bereitstellungstools für Klick-und-Los maßschneidern. Da Office 2013 Klick-und-Los in erster Linie in der Microsoft 365-Umgebung verwendet wird, wird diese Installationsmethode nicht ausführlich in diesem Abschnitt beschrieben. Detaillierte Informationen zur Verwendung und Anpassung der Klick-und-Los-Installation finden Sie in der Dokumentation zum Office 2013 Resource Kit. Administratoren können auch das Office 2013-Klick-und-Los-Programm und die sprach Quelldateien in einen lokalen Speicherort herunterladen, was nützlich ist, wenn Sie die Netzwerk Nachfrage minimieren oder verhindern möchten, dass Benutzer Software aus dem Internet installieren, weil Sie die Sicherheitsanforderungen der Unternehmen erfüllen.

Die Themen in diesem Abschnitt konzentrieren sich auf die Bereitstellung von Clients mithilfe des MSI-basierten Installationsprogramms von Office 2013. Ihr primärer Bezug sollte die Office 2013 Resource Kit-Dokumentation sein, in der ausführlich beschrieben wird, wie Sie Ihre Infrastruktur vorbereiten, Setup anpassen und Office 2013 bereitstellen. Sie sollten die Office-Dokumentation jedoch in Verbindung mit den Themen in diesem Abschnitt verwenden, die auf Bereitstellungsüberlegungen verweisen, die für lync 2013 spezifisch sind.

<div>


> [!NOTE]  
> <UL>
> <LI>
> <P>Das Online Besprechungs-Add-in für lync 2013, das die Besprechungsverwaltung innerhalb des Outlook-Messaging-und Zusammenarbeits Clients unterstützt, wird automatisch mit lync 2013 installiert.</P>
> <LI>
> <P>Das Office 2013-Setupprogramm deinstalliert keine früheren Versionen von lync oder Office Communicator. Der lync 2013-Client wird nebeneinander mit anderen lync-oder Office Communicator-Clients installiert</P></LI></UL>



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Anpassen der Clientinstallation in lync Server 2013](lync-server-2013-customizing-client-installation.md)

  - [Anpassen des lync-Verhaltens und der Benutzeroberfläche in lync Server 2013](lync-server-2013-customizing-lync-behavior-and-the-user-interface.md)

  - [Anpassen des Online Besprechungs-Add-Ins in lync Server 2013](lync-server-2013-customizing-the-online-meeting-add-in.md)

  - [Konfigurieren der Seite für den Besprechungsbeitritt in Lync Server 2013](lync-server-2013-configuring-the-meeting-join-page.md)

  - [Konfigurieren von unterstützten Clientversionen in lync Server 2013](lync-server-2013-configuring-supported-client-versions.md)

  - [Konfigurieren des erweiterten Anwesenheitsdaten Schutzmodus in lync Server 2013](lync-server-2013-configuring-enhanced-presence-privacy-mode.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

