---
title: 'Lync Server 2013: Zuweisen einer VoIP-Richtlinie für einzelne Benutzer'
description: 'Lync Server 2013: Zuweisen einer VoIP-Richtlinie für einzelne Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user voice policy
ms:assetid: 9ee47ee7-1030-43b8-a4dc-bf685ea24659
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688155(v=OCS.15)
ms:contentKeyID: 49733758
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7ea0b171e10302b4c466187c54324cc2548e821
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443162"
---
# <a name="assign-a-per-user-voice-policy-in-lync-server-2013"></a>Zuweisen einer VoIP-Richtlinie für einzelne Benutzer in lync Server 2013

 


VoIP-Richtlinien auf globaler und Websiteebene werden automatisch allen lync Server 2013-Benutzerkonten zugewiesen, die für Enterprise-VoIP aktiviert sind. Sie können bestimmten Benutzern auch Sprachrichtlinien zuweisen, indem Sie entweder die lync Server 2013-Systemsteuerung oder die lync Server 2013-Verwaltungsshell verwenden. Verwenden Sie die in diesem Thema beschriebenen Verfahren, um lync Server-Benutzern explizit Richtlinien für einzelne Benutzer zuzuweisen.

## <a name="to-assign-a-user-specific-voice-policy-using-the-lync-server-control-panel"></a>So weisen Sie mithilfe der lync Server-Systemsteuerung eine benutzerspezifische VoIP-Richtlinie zu

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie in der linken Navigationsleiste auf **Benutzer** und suchen Sie anschließend nach dem Benutzerkonto, das Sie konfigurieren möchten.

4.  Klicken Sie in der Tabelle mit den Suchergebnissen auf das Benutzerkonto, klicken Sie auf **Bearbeiten** und dann auf **Details anzeigen**.

5.  Wählen Sie in **lync Server-Benutzer bearbeiten** unter **VoIP-Richtlinie** die Benutzerrichtlinie aus, die Sie anwenden möchten.
    

    > [!NOTE]  
    > Die <STRONG> &lt; automatischen &gt; </STRONG> Einstellungen gelten für den Standardserver oder die globalen Richtlinieneinstellungen.



## <a name="assign-per-user-voice-policies"></a>Zuweisen von VoIP-Richtlinien für einzelne Benutzer

Sie können VoIP-Richtlinien für einzelne Benutzer mithilfe von Windows PowerShell und dem Cmdlet **Grant-CsVoicePolicy** zuweisen. Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen. Informationen zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie in diesem lync Server Windows PowerShell-Blogbeitrag: [schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell](https://go.microsoft.com/fwlink/p/?linkId=255876).

### <a name="assign-a-per-user-voice-policy-to-a-single-user"></a>Zuweisen einer pro-Benutzer-VoIP-Richtlinie zu einem einzelnen Benutzer

  - Mit dem folgenden Befehl wird dem Benutzer Ken Myers die Richtlinie für die benutzerspezifische VoIP-RedmondVoicePolicy zugewiesen.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName "RedmondVoicePolicy"

## <a name="assign-a-per-user-voice-policy-to-multiple-users"></a>Zuweisen einer pro-Benutzer-VoIP-Richtlinie zu mehreren Benutzern

  - Dieser Befehl weist allen Benutzern, die über Konten in der Organisationseinheit Finanzen in Active Directory verfügen, die VoIP-Richtlinien für einzelne Benutzer zu FinanceVoicePolicy. Weitere Informationen zu dem in diesem Befehl verwendeten ou-Parameter finden Sie in der Dokumentation für das Cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .
    
        Get-CsUser -OU "ou=Finance,ou=North America,dc=litwareinc,dc=com" | Grant-CsVoicePolicy -PolicyName "FinanceVoicePolicy"

## <a name="unassign-a-per-user-voice-policy"></a>Aufheben der Zuweisung einer VoIP-Richtlinie für einzelne Benutzer

  - Mit dem folgenden Befehl wird die Zuweisung einer einzelnen Benutzer-VoIP-Richtlinie, die Ken Myers zuvor zugewiesen wurde, aufheben. Anschließend wird Ken Myer automatisch mithilfe der globalen Richtlinie oder, soweit vorhanden, mit seiner lokalen Standortrichtlinie verwaltet. Eine Standortrichtlinie hat Vorrang vor der globalen Richtlinie.
    
        Grant-CsVoicePolicy -Identity "Ken Myer" -PolicyName $Null

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Grant-CsVoicePolicy](https://technet.microsoft.com/library/gg398828\(v=ocs.15\)) .

## <a name="see-also"></a>Siehe auch


[Deaktivieren eines Benutzers für Enterprise-VoIP in lync Server 2013](lync-server-2013-disable-a-user-for-enterprise-voice.md)  


[Verwaltungsshell für Lync Server 2013](lync-server-2013-lync-server-management-shell.md)

