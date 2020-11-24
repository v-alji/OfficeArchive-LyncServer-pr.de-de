---
title: 'Lync Server 2013: Technische Anforderungen für das Parken von Anrufen'
description: 'Lync Server 2013: Technische Voraussetzungen für den Parken von anrufen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Call Park
ms:assetid: 38bcf302-2b72-4492-9266-f6dc31b566e1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204818(v=OCS.15)
ms:contentKeyID: 48183897
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ddc17b40f78c42c090d1a87b4580ebdad0a07f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394682"
---
# <a name="technical-requirements-for-call-park-in-lync-server-2013"></a>Technische Anforderungen für das Parken von Anrufen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-11-07_

In diesem Abschnitt werden die folgenden technischen Voraussetzungen für den Parken von Anrufen beschrieben:

  - Hardwareanforderungen

  - Softwareanforderungen

  - Portanforderungen

  - Audiodatei-Anforderungen

<div>

## <a name="hardware-requirements"></a>Hardware Anforderungen

Die Anwendung für den Anruf Park hat die gleichen Hardwareanforderungen wie Front-End-Server. Details zu den Hardwareanforderungen finden Sie unter [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md) in der Dokumentation zur Unterstützung.

</div>

<div>

## <a name="software-requirements"></a>Software Anforderungen

Die Anwendung für den Anruf Park hat die gleichen Betriebssystemanforderungen und Softwarevoraussetzungen wie Front-End-Server. Ausführliche Informationen zu den Softwareanforderungen finden Sie unter unter [Stützung von Server-und Tools-Betriebssystemen in lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in der Dokumentation zur Unterstützung.

Auf allen Front-End-Servern und Standard Edition-Servern, auf denen die Anwendung für das Parken von Anrufen bereitgestellt wird, muss die Windows Media-Format Laufzeit für Server mit Windows Server 2008 R2 oder Microsoft Media Foundation für Server mit Windows Server 2012 oder Windows Server 2012 R2 installiert sein. Für Windows Server 2008 R2 wird die Windows Media-Format Laufzeit als Teil der Windows-Desktop Oberfläche installiert. Windows Media Format Runtime oder Microsoft Media Foundation ist für Windows Media Audio-Dateien (WMA) erforderlich, in denen Park Wiedergaben für Musik im Wartebereich aufgerufen werden.

</div>

<div>

## <a name="port-requirements"></a>Portanforderungen

Die Anwendung für den Anruf Park verwendet den folgenden Port:

  - **Port 5075** Wird für SIP-Überwachungsanforderungen verwendet.

<div>


> [!NOTE]  
> Dieser Port ist die Standardeinstellung, die Sie mit dem Cmdlet <STRONG>Set-CsApplicationServer</STRONG> ändern können. Details zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.



</div>

</div>

<div>

## <a name="audio-file-requirements"></a>Anforderungen für Audiodateien

Die Anwendung "Parken" unterstützt nur WMA-Dateien (Windows Media Audio) für Musik in Wartestellung. Sie können den Microsoft Expression Encoder 4 verwenden, um Dateien für Musik in Wartestellung anzupassen. Informationen zum Herunterladen von Expression Encoder 4 finden Sie unter "Expression Encoder 4" unter [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) . Verwenden Sie das Tool, um die Datei in ein WMA-Format umzuwandeln. Das empfohlene Format für Music-on-halten-Dateien im Parken von anrufen ist Media Audio 9, 44 kHz, 16 Bits, Mono, CBR, 32 Kbit/s.

<div>


> [!NOTE]  
> Die konvertierte Datei wird über das Telefon nur mit 16 kHz abgespielt, auch wenn sie mit 44 kHz aufgezeichnet wurde.



</div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

