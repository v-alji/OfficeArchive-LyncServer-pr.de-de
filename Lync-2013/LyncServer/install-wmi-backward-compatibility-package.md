---
title: Installieren des WMI-abwärts Kompatibilitätspakets
description: Installieren Sie das WMI-abwärts Kompatibilitätspaket.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Install WMI Backward Compatibility package
ms:assetid: 38797fbd-06a0-4008-b099-158e7b5d7703
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204816(v=OCS.15)
ms:contentKeyID: 48183893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9062e209981fd180b8772801960bd94d2256513a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439579"
---
# <a name="install-wmi-backward-compatibility-package"></a>Installieren des WMI-abwärts Kompatibilitätspakets

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-02_

Wenn Sie versuchen, den Zusammenführungs-Assistenten des Topologie-Generators auszuführen, ohne das WMI-abwärts Kompatibilitätspaket zu installieren, wird der folgende Fehler angezeigt:

![WMI-Fehlermeldung](images/JJ204816.a007d2f2-fc85-430c-91eb-382b032469af(OCS.15).jpg "WMI-Fehlermeldung")

Wenn Sie versuchen, das **Merge-CsLegacytopology-** Cmdlet auszuführen, ohne das WMI-abwärts Kompatibilitätspaket zu installieren, wird der folgende Fehler angezeigt:

![Windows PowerShell-WMI-Anbieterfehler](images/JJ204816.c510824e-1807-4c7e-bb28-c6cfea2eac1d(OCS.15).jpg "Windows PowerShell-WMI-Anbieterfehler")

So installieren Sie das WMI-abwärts Kompatibilitätspaket

1.  Navigieren Sie auf Ihrem Installationsmedium zu \\ Setup \\ amd64- \\ Setup \\OCSWMIBC.MSI.

2.  Installieren Sie OCSWMIBC.MSI.
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi müssen auf dem Computer installiert sein, auf dem der Zusammenführungs-Assistent für Topologie-Builder ausgeführt wird. Es wird jedoch empfohlen, OCSWMIBC.msi auf allen Front-End-Servern in Ihrer Topologie zu installieren.

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > OCSWMIBC.msi kann auf jedem Computer in der Domäne installiert werden, auf dem die lync Server 2013-Core-Komponenten und die lync Server 2013-Verwaltungsshell installiert sind, und Sie können auf die Office Communications Server 2007 R2-Topologie (WMI-Anbieter für Active Directory-Domänendienste (AD DS) und SQL Server) zugreifen.

    
    </div>

</div>

<span> </span>

</div>

</div>

</div>

