---
title: Erneutes Aktivieren eines Servers, nachdem der Sicherheitskonfigurations-Assistent Ports in IIS schließt
description: Server erneut aktivieren, nachdem der Sicherheitskonfigurations-Assistent die Ports in IIS geschlossen hat.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Re-activate server after Security Configuration Wizard closes ports in IIS
ms:assetid: cb8e17cf-f8c1-4099-b63b-c242d656c26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398851(v=OCS.15)
ms:contentKeyID: 48185644
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d824845a7f89c28087a7b5d180a6ed017cb47ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436720"
---
# <a name="re-activate-server-after-security-configuration-wizard-closes-ports-in-iis"></a>Erneutes Aktivieren eines Servers, nachdem der Sicherheitskonfigurations-Assistent Ports in IIS schließt

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-01_

Einige lync Server 2013-Rollen führen Webdienste im Internet Informationsdienste (IIS)-Port 4443 aus. Wenn Sie den lync Server-Bereitstellungs-Assistenten Bootstrapper.exe oder das Cmdlet **enable-CsComputer** verwenden, wird eine Ausnahme in der Firewall erstellt, und der Port wird geöffnet. Wenn Sie dann den Windows Server 2008 R2-Sicherheitskonfigurations-Assistenten (oder andere Härtungs Skripts) ausführen, wird Port 4443 blockiert, und externe Clients können keine Webdienste kontaktieren. Um den Port erneut zu öffnen, können Sie entweder die Firewall-Ausnahme direkt ändern oder den Server erneut aktivieren.

<div>

## <a name="to-re-activate-the-server-by-using-the-deployment-wizard"></a>So aktivieren Sie den Server mithilfe des Bereitstellungs-Assistenten erneut

1.  Klicken Sie auf der Seite lync Server-Bereitstellungs-Assistent neben **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten** auf **Ausführen** .

2.  Klicken Sie auf der Seite **Setup lync Server Components** auf **weiter**.

3.  Klicken Sie auf der Seite **Befehle ausführen** , wenn der Vorgangsstatus als erledigt angezeigt wird, auf **Fertig stellen**.
    
    <div>
    

    > [!NOTE]
    > Sie können auch bootstrapper.exe oder <STRONG>enable-CsComputer</STRONG> verwenden, um den Server wieder zu aktivieren.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

