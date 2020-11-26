---
title: 'Lync Server 2013: Importieren einer VoIP-Routenkonfigurationsdatei'
description: 'Lync Server 2013: Importieren einer sprach Routen-Konfigurationsdatei'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Import a voice route configuration file
ms:assetid: 4bac05e5-ed8b-4f10-96b0-b8a65ff356ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398301(v=OCS.15)
ms:contentKeyID: 48184049
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 994095598b39548f00447edd4b0d322a7ec5545e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427334"
---
# <a name="import-a-voice-route-configuration-file-in-lync-server-2013"></a><span data-ttu-id="5aa61-103">Importieren einer VoIP-Routenkonfigurationsdatei in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa61-103">Import a voice route configuration file in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5aa61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5aa61-104">

<span> </span></span></span>

<span data-ttu-id="5aa61-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="5aa61-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="5aa61-106">Wenn Sie Ihre sprach Routingkonfiguration speichern möchten, ohne Sie zu veröffentlichen, führen Sie die folgenden Schritte aus, um die Konfigurations Export-und-Importbefehle in lync Server Control Panel zu verwenden, um eine Momentaufnahme Ihrer VoIP-Routingkonfiguration zu speichern und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5aa61-106">If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration.</span></span> <span data-ttu-id="5aa61-107">Wenn Sie eine sprach Routing-Konfigurationsdatei (. vcfg) importieren, aber Änderungen an der sprach Routingkonfiguration auf dem Server in der Zwischenzeit vorgenommen wurden, zeigen die Seiten in der Gruppe **VoIP-Routing** in der lync Server-Systemsteuerung an, dass nicht festgeschriebene Änderungen an der sprach Weiterleitung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="5aa61-107">When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing.</span></span> <span data-ttu-id="5aa61-108">Diese noch nicht übernommenen Änderungen stellen die Unterschiede zwischen den zwei Konfigurationen dar, die einer Zusammenführung bedürfen.</span><span class="sxs-lookup"><span data-stu-id="5aa61-108">Those uncommitted changes are the differences between the two configurations that require reconciliation.</span></span>

<span data-ttu-id="5aa61-109">Wenn Sie Änderungen an den Einstellungen auf einer beliebigen Seite innerhalb der Gruppe vorgenommen haben, werden die Änderungen in der exportierten sprach Konfigurationsdatei (vcfg) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5aa61-109">If you have made any uncommitted changes to the settings on any page within the group, the changes are saved in the exported voice configuration file (.vcfg).</span></span> <span data-ttu-id="5aa61-110">So können Sie während mehrerer Sitzungen Änderungen an der sprach Routingkonfiguration vornehmen, bevor Sie die Änderungen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5aa61-110">This enables you to make voice routing configuration changes during multiple sessions before you publish the changes.</span></span>

<div>

## <a name="to-import-a-voice-routing-configuration"></a><span data-ttu-id="5aa61-111">So importieren Sie eine VoIP-Routingkonfiguration</span><span class="sxs-lookup"><span data-stu-id="5aa61-111">To import a voice routing configuration</span></span>

1.  <span data-ttu-id="5aa61-112">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="5aa61-112">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="5aa61-113">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="5aa61-113">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="5aa61-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5aa61-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5aa61-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5aa61-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5aa61-116">Klicken Sie in der linken Navigationsleiste auf **VoIP-Routing**.</span><span class="sxs-lookup"><span data-stu-id="5aa61-116">In the left navigation bar, click **Voice Routing**.</span></span>

4.  <span data-ttu-id="5aa61-117">Klicken Sie im Menü **Aktionen** auf **Konfiguration importieren**.</span><span class="sxs-lookup"><span data-stu-id="5aa61-117">On the **Actions** menu, click **Import configuration**.</span></span>

5.  <span data-ttu-id="5aa61-118">Suchen Sie nach der Konfigurationsdatei, die Sie importieren möchten, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="5aa61-118">Find the configuration file you want to import and then click **Open**.</span></span>

6.  <span data-ttu-id="5aa61-119">Klicken Sie auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5aa61-119">Click **Commit**, and then click **Commit all**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5aa61-120">Jedes Mal, wenn Sie eine VoIP-Konfigurationsdatei importieren, müssen Sie den Befehl <STRONG>Commit für alle Elemente ausführen</STRONG> ausführen, um die Konfigurationsänderung zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5aa61-120">Whenever you import a voice configuration file, you must run the <STRONG>Commit all</STRONG> command to publish the configuration change.</span></span> <span data-ttu-id="5aa61-121">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">veröffentlichen ausstehender Änderungen an der VoIP-Routingkonfiguration in lync Server 2013</A> in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5aa61-121">For details, see <A href="lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md">Publish pending changes to the voice routing configuration in Lync Server 2013</A> in the Operations documentation.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5aa61-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aa61-122">See Also</span></span>


[<span data-ttu-id="5aa61-123">Exportieren einer sprach Routen-Konfigurationsdatei in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa61-123">Export a voice route configuration file in Lync Server 2013</span></span>](lync-server-2013-export-a-voice-route-configuration-file.md)  
[<span data-ttu-id="5aa61-124">Veröffentlichen ausstehender Änderungen an der VoIP-Routingkonfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5aa61-124">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)  
  

<span data-ttu-id="5aa61-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5aa61-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

