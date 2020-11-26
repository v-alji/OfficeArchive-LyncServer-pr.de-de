---
title: Beispiel für eine XMPP-Konfiguration – XMPP-Partnerverbund mit Google Talk
description: Beispiel für die XMPP-Konfiguration – XMPP Federation mit Google Talk.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
manager: serdars
audience: admin
f1.keywords:
- NOCSH
TOCTitle: Example XMPP configuration – XMPP federation with Google Talk
ms:assetid: 360a2f7b-015b-4e93-ac67-0f609c21f1a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204807(v=OCS.15)
ms:contentKeyID: 48183848
ms.date: 07/23/2014
mtps_version: v=OCS.15
ms.openlocfilehash: e6ea920fad0344e784aac104ab5528d89b90f47b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428450"
---
# <a name="example-xmpp-configuration-in-lync-server-2013--xmpp-federation-with-google-talk"></a>Beispiel für eine XMPP-Konfiguration in Lync Server 2013 – XMPP-Partnerverbund mit Google Talk

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-04-22_

Eine Beispielkonfiguration für die Bereitstellung des XMPP-Proxys definiert einen Verbund mit Google Talk.

<div>

## <a name="example-xmpp-configuration--xmpp-federation-with-google-talk"></a>Beispiel für eine XMPP-Konfiguration – XMPP-Partnerverbund mit Google Talk

1.  Öffnen Sie auf dem Front-End-Server den lync Server-Bereitstellungs-Assistenten. Klicken Sie auf **lync Server System** **Installieren** oder aktualisieren und dann auf **lync Server-Komponenten** **Einrichten** oder entfernen. Klicken Sie **erneut auf Ausführen**.

2.  Klicken Sie bei der **Installation von lync Server-Komponenten** auf **weiter**. Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt. Klicken Sie nach Abschluss der Bereitstellung auf **Protokoll anzeigen** , um die verfügbaren Protokolldateien anzuzeigen. Klicken Sie auf **Fertig stellen** , um die Bereitstellung abzuschließen.

3.  Öffnen Sie auf dem Edgeserver den lync Server-Bereitstellungs-Assistenten. Klicken Sie auf **lync Server System** **Installieren** oder aktualisieren und dann auf **lync Server-Komponenten** **Einrichten** oder entfernen. Klicken Sie **erneut auf Ausführen**.

4.  Als XMPP-Partner können Sie Google Talk hinzufügen. Google Talk unterstützt derzeit nur unverschlüsselte TCP-Verbindungen für Server-zu-Server-XMPP-Föderationen und unterstützt nur Server-Dialback zur Identitätsüberprüfung. (Siehe <http://xmpp.org/extensions/xep-0220.html> ).
    
        New-CsXmppAllowedPartner gmail.com -TlsNegotiation NotSupported -SaslNegotiation NotSupported -EnableKeepAlive $false -SupportDialbackNegotiation $true

5.  Um Edge Federation zu aktivieren, geben Sie Folgendes ein:
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $true

6.  Klicken Sie bei der **Installation von lync Server-Komponenten** auf **weiter**. Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt. Nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf **Protokoll anzeigen** , um die verfügbaren Protokolldateien anzuzeigen. Klicken Sie auf **Fertig stellen** , um die Bereitstellung abzuschließen.

7.  Klicken Sie auf dem Edgeserver im lync Server-Bereitstellungs-Assistenten neben **Schritt 3: anfordern, installieren oder Zuweisen von Zertifikaten** auf **erneut ausführen**.
    
    <div>
    

    > [!TIP]
    > Wenn Sie den Edgeserver zum ersten Mal bereitstellen, wird Run anstelle von Run erneut angezeigt.

    
    </div>

8.  Klicken Sie auf der Seite **Verfügbare Zertifikataufgaben** auf **Neue Zertifikatsanforderung erstellen**.

9.  Klicken Sie auf der Seite **Zertifikatanforderung** auf **externes Zertifikat**.

10. Aktivieren Sie auf der Seite **verzögerte oder sofortige Anforderung** das Kontrollkästchen **Anforderung jetzt vorbereiten, aber später senden** .

11. Geben Sie auf der Seite **Zertifikatanforderungsdatei** den vollständigen Pfad und den Dateinamen der Datei ein, in der die Anforderung gespeichert werden soll (beispielsweise c: CERT, " \\ \_ \_ Edge. cer").

12. Aktivieren Sie auf der Seite **Alternative Zertifikatvorlage angeben** für das Kontrollkästchen **Alternative Zertifikatvorlage für die ausgewählte Zertifizierungsstelle verwenden** , um eine andere Vorlage als die standardmäßige Webservervorlage zu verwenden.

13. Gehen Sie auf der Seite **Name und Sicherheitseinstellungen** wie folgt vor:
    
    1.  Geben Sie unter **Anzeigename einen** Anzeigenamen für das Zertifikat ein.
    
    2.  Geben Sie in **Bit length** die Bit-Länge an (in der Regel der Standardwert von **2048**).
    
    3.  Überprüfen, ob das Kontrollkästchen " **Zertifikat privater Schlüssel als exportierbar kennzeichnen** " aktiviert ist

14. Geben Sie auf der Seite **Organisationsinformationen** den Namen für die Organisation und die Organisationseinheit ein (beispielsweise eine Abteilung oder Abteilung).

15. Geben Sie auf der Seite **geographische Informationen** die Standortinformationen an.

16. Auf der Seite **Betreffname/Subject Alternative** Names werden die Informationen angezeigt, die automatisch vom Assistenten ausgefüllt werden sollen. Wenn zusätzliche Alternative Namen für Subjekte benötigt werden, geben Sie diese in den nächsten beiden Schritten an.

17. Aktivieren Sie in der **SIP-Domäneneinstellung auf der Seite Subject Alternate Names (SANs)** das Kontrollkästchen Domäne, um einen SIP hinzuzufügen. \<sipdomain\> Eintrag in die Liste der alternativen Subjektnamen.

18. Geben Sie auf der Seite **configure additional Subject Alternative Names** alle zusätzlichen alternativen Subjektnamen an, die erforderlich sind.
    
    <div>
    

    > [!TIP]
    > Wenn der XMPP-Proxy installiert ist, wird standardmäßig der Domänenname (wie contoso.com) in den San-Einträgen ausgefüllt. Wenn Sie weitere Einträge benötigen, fügen Sie Sie in diesem Schritt hinzu.

    
    </div>

19. Überprüfen Sie auf der Seite **Anforderungszusammenfassung** die Zertifikatinformationen, die zum Generieren der Anforderung verwendet werden sollen.

20. Nachdem die Befehle ausgeführt wurden, können Sie das **Protokoll anzeigen** oder auf **weiter** klicken, um fortzufahren.

21. Auf der Seite **Zertifikatanforderungsdatei** können Sie die generierte CSR-Datei (Certificate Signing Request) anzeigen, indem Sie auf **Fertig stellen** **klicken oder den** Zertifikat-Assistenten verlassen.

22. Kopieren Sie die Anforderungsdatei, und senden Sie Sie an Ihre öffentliche Zertifizierungsstelle.

23. Nachdem Sie das öffentliche Zertifikat empfangen, importiert und zugewiesen haben, müssen Sie die Edgeserver-Dienste beenden und neu starten. Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**. Geben Sie in der lync Server-Verwaltungsshell Folgendes ein:
    ```
        Stop-CsWindowsService
    ```
    
    ```
        Start-CsWindowsService
    ```
    
24. Zum Konfigurieren von DNS für die XMPP-Föderation fügen Sie den folgenden SRV-Eintrag zu externem DNS hinzu: \_ XMPP-Server. \_ TCP.\<domain name\> Der SRV-Eintrag wird in den Access-Edge-FQDN des Edge-Servers aufgelöst, wobei der Portwert 5269

25. Konfigurieren Sie eine neue Richtlinie für den externen Zugriff, um alle Benutzer zu aktivieren, indem Sie die lync Server-Verwaltungsshell auf einem Front-End-Server öffnen und Folgendes eingeben:
    
        New-CsExternalAccessPolicy -Identity FedPic -EnableFederationAccess $true -EnablePublicCloudAccess $true
        Get-CsUser | Grant-CsExternalAccessPolicy -PolicyName FedPic

</div>

</div>

<span> </span>

</div>

</div>

</div>

