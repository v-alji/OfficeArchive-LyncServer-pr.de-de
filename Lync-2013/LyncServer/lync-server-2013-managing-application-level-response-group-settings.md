---
title: 'Lync Server 2013: Verwalten von Einstellungen für die Reaktionsgruppe auf Anwendungsebene'
description: 'Lync Server 2013: Verwalten von Einstellungen für die Reaktionsgruppe auf Anwendungsebene.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing application-level Response Group settings
ms:assetid: aab749a1-fa2d-4ce8-a6c6-ebcfa37ce02a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721843(v=OCS.15)
ms:contentKeyID: 49733776
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd362cbe8ce738a16639b89edd79439b564444ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425997"
---
# <a name="managing-application-level-response-group-settings-in-lync-server-2013"></a><span data-ttu-id="c70be-103">Verwalten von Reaktionsgruppeneinstellungen auf Anwendungsebene in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c70be-103">Managing application-level Response Group settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c70be-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c70be-104">

<span> </span></span></span>

<span data-ttu-id="c70be-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="c70be-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="c70be-106">Zu den Einstellungen auf Anwendungsebene für die Anwendung der Reaktionsgruppe gehören die standardmäßige Musik-in-situ-Konfiguration, die standardmäßige Musik-in-halten-Audiodatei, die Kulanzzeit für den Agent-Rückruf und die Konfiguration des Anruf Kontexts.</span><span class="sxs-lookup"><span data-stu-id="c70be-106">Application-level settings for Response Group application include the default music-on-hold configuration, the default music-on-hold audio file, the agent ringback grace period, and the call context configuration.</span></span> <span data-ttu-id="c70be-107">Pro Pool können Sie nur eine Gruppe von Einstellungen auf Anwendungsebene definieren.</span><span class="sxs-lookup"><span data-stu-id="c70be-107">You can define only one set of application-level settings per pool.</span></span> <span data-ttu-id="c70be-108">Verwenden Sie zum Anzeigen der Einstellungen auf Anwendungsebene das Cmdlet **Get-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c70be-108">To view application-level settings, use the **Get-CsRgsConfiguration** cmdlet.</span></span> <span data-ttu-id="c70be-109">Wenn Sie die Einstellungen auf Anwendungsebene ändern möchten, verwenden Sie das Cmdlet **Set-CsRgsConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c70be-109">To modify the application-level settings, use the **Set-CsRgsConfiguration** cmdlet.</span></span>

<span data-ttu-id="c70be-p102">Die Standard-Wartemusik wird wiedergegeben, wenn ein Anruf in der Warteschleife platziert wird, und auch nur dann, wenn keine benutzerdefinierte Wartemusik definiert wurde. Der Anrufkontext ist nur für Warteschleifen verfügbar, die interaktiven Workflows zugeordnet sind. Wenn der Anrufkontext aktiviert ist, kann ein Agent Informationen wie die Wartezeit des Anrufers oder Fragen und Antworten zu einem Workflow anzeigen, wenn der Anruf empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="c70be-p102">The default music on hold is played when a call is placed on hold only if no custom music on hold is defined. Call context is available only for queues assigned to interactive workflows. If call context is enabled, an agent can see information such as caller wait time or workflow questions and answers when the call is received.</span></span>

<div>

## <a name="to-modify-response-group-application-level-settings"></a><span data-ttu-id="c70be-113">So ändern Sie die Einstellungen der Reaktionsgruppe auf Anwendungsebene</span><span class="sxs-lookup"><span data-stu-id="c70be-113">To modify Response Group application-level settings</span></span>

1.  <span data-ttu-id="c70be-114">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c70be-114">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="c70be-115">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="c70be-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="c70be-116">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="c70be-116">At the command line, run:</span></span>
    
        Set-CsRgsConfiguration -Identity <name of service hosting Response Group> [-AgentRingbackGracePeriod <# seconds until call returns to agent after declined>] [-DefaultMusicOnHoldFile <audio file>] [-DisableCallContext <$true | $false>]
    
    <span data-ttu-id="c70be-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c70be-117">For example:</span></span>
    
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -AgentRingbackGracePeriod 30 -DisableCallContext $false
    
    <span data-ttu-id="c70be-p103">Wenn Sie eine Audiodatei angeben möchten, die als Standard-Wartemusik verwendet werden soll, müssen Sie zunächst die Audiodatei importieren. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c70be-p103">To specify an audio file to use as the default music on hold, you need to import the audio file first. For example:</span></span>
    
        $x = Import-CsRgsAudioFile -Identity "service:ApplicationServer:redmond.contoso.com" -FileName "MusicWhileYouWait.wav" -Content (Get-Content C:\Media\ MusicWhileYouWait.wav -Encoding byte -ReadCount 0)
        Set-CsRgsConfiguration -Identity "service:ApplicationServer:redmond.contoso.com" -DefaultMusicOnHoldFile <$x>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c70be-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c70be-120">See Also</span></span>


[<span data-ttu-id="c70be-121">Get-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="c70be-121">Get-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsRgsConfiguration)  
[<span data-ttu-id="c70be-122">Satz-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="c70be-122">Set-CsRgsConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsRgsConfiguration)  
[<span data-ttu-id="c70be-123">Importieren-CsRgsAudioFile</span><span class="sxs-lookup"><span data-stu-id="c70be-123">Import-CsRgsAudioFile</span></span>](https://docs.microsoft.com/powershell/module/skype/Import-CsRgsAudioFile)  
  

<span data-ttu-id="c70be-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c70be-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

