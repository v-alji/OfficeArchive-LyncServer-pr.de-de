---
title: 'Lync Server 2013: Einrichten von Kennwörtern für ein Kerberos-Authentifizierungskonto'
description: 'Lync Server 2013: Einrichten von Kennwörtern für Kerberos-Authentifizierungs Konten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Kerberos authentication account passwords
ms:assetid: b435f88e-4a77-4be7-b7e5-c17484303b74
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412870(v=OCS.15)
ms:contentKeyID: 48185167
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614b1411f9454c39843f4e69cabbfc3b02986e51
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423971"
---
# <a name="setting-up-kerberos-authentication-account-passwords-in-lync-server-2013"></a>Einrichten von Kennwörtern für ein Kerberos-Authentifizierungskonto in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2010-11-03_

Nachdem Sie das Computerobjekt für das Kerberos-Authentifizierungs Konto erstellt haben, können Sie das Kennwort für das Konto einrichten. Sie führen das Windows PowerShell-Cmdlet aus, um das Kerberos-Kontokennwort auf einem Server festzulegen. Sie können das Kennwort für das für die Kerberos-Authentifizierung erstellte Objekt festlegen. Das Kennwort kann auf einen bekannten Wert eingestellt werden, ist aber standardmäßig ein zufälliges Kennwort. Das Kennwort steht für alle Kerberos-Authentifizierungsquellen, die das Konto verwenden, zur Verfügung. Sie verwenden Windows PowerShell-Cmdlets zum Einrichten und Verwalten von Kennwörtern für Kerberos-Konten.

<div>


> [!NOTE]  
> Das Kerberos-Kontoobjekt ist ein Computerobjekt, verwendet aber den Benutzerkonto-Parameter für Vorgänge in den Windows PowerShell-Cmdlets, auf die verwiesen wird. Beachten Sie, dass es sich nicht um einen Fehler handelt, sondern um das beabsichtigte Verhalten des Cmdlets, wenn es mit dem Erstellen und Verwalten von Kerberos-Konten verwendet wird.



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Festlegen eines Kennworts für das Kerberos-Authentifizierungskonto auf einem Server in Lync Server 2013](lync-server-2013-set-a-kerberos-authentication-account-password-on-a-server.md)

  - [Synchronisieren eines Kennworts für das Kerberos-Authentifizierungskonto mit IIS in Lync Server 2013](lync-server-2013-synchronize-a-kerberos-authentication-account-password-to-iis.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

