---
title: 'Lync Server 2013: Exportieren von Testfällen für das VoIP-Routing'
description: 'Lync Server 2013: Exportieren von Testfällen für das VoIP-Routing'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export voice routing test cases
ms:assetid: 489ac472-1a35-4755-b390-48f7cdf31e94
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425957(v=OCS.15)
ms:contentKeyID: 48184050
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 934bd183a17c46cf82fe5bc04faaa55a9bbe4731
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428349"
---
# <a name="export-voice-routing-test-cases-in-lync-server-2013"></a><span data-ttu-id="a0350-103">Exportieren von Testfällen für das VoIP-Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0350-103">Export voice routing test cases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0350-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0350-104">

<span> </span></span></span>

<span data-ttu-id="a0350-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a0350-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a0350-106">Testfälle bieten Ihnen die Möglichkeit, VoIP-Routen in Ihrer Organisation zu testen: Sie definieren solche Dinge wie die Nummer, die gewählt werden soll, und die Richtlinie für Wähleinstellungen und VoIP, die verwendet werden soll, und lync Server kann dann überprüfen, ob die angegebene Nummer unter diesen Bedingungen erfolgreich an das PSTN-Netzwerk weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0350-106">Test cases provide a way for you to test voice routes in your organization: you define such things as the number to be dialed and the dial plan and voice policy to be employed, and Lync Server can then verify that, given those conditions, the supplied number can successfully be routed to the PSTN network.</span></span>

<span data-ttu-id="a0350-107">Testfälle, die mithilfe der lync Server-Systemsteuerung erstellt werden können, werden in der Regel nur auf dem Server gespeichert, auf dem der Fall ursprünglich erstellt und ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0350-107">Test cases, which can be created by using Lync Server Control Panel, are typically saved only on the server where the case was originally created and run.</span></span> <span data-ttu-id="a0350-108">Diese Testfälle können jedoch als XML-Dateien (mit der Erweiterung. vtest) exportiert und dann auf anderen Servern importiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0350-108">However, these test cases can be exported as XML files (with the .vtest extension) and then imported on other servers.</span></span> <span data-ttu-id="a0350-109">Auf diese Weise können Sie dieselben Tests auf verschiedenen Computern ausführen, die sich an unterschiedlichen Stellen in Ihrer Topologie befinden.</span><span class="sxs-lookup"><span data-stu-id="a0350-109">This enables you to run the same tests on different computers located at different points in your topology.</span></span>

<div>

## <a name="to-export-a-voice-routing-test-case"></a><span data-ttu-id="a0350-110">So exportieren Sie einen Test Case für VoIP-Routing</span><span class="sxs-lookup"><span data-stu-id="a0350-110">To export a voice routing test case</span></span>

1.  <span data-ttu-id="a0350-111">Klicken Sie in der lync Server-Systemsteuerung auf **VoIP-Routing** , und klicken Sie dann auf **VoIP-Routing testen**.</span><span class="sxs-lookup"><span data-stu-id="a0350-111">In Lync Server Control Panel, click **Voice Routing** and then click **Test Voice Routing**.</span></span>

2.  <span data-ttu-id="a0350-112">Wählen Sie auf der Registerkarte **VoIP-Routing testen** den Testfall (oder Testfälle) aus, der exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0350-112">On the **Test Voice Routing** tab, select the test case (or test cases) to be exported.</span></span> <span data-ttu-id="a0350-113">Wenn Sie mehrere Testfälle auswählen möchten, klicken Sie auf den ersten zu exportierenden Fall, halten Sie dann die STRG-Taste gedrückt, und wählen Sie die zu exportierenden zusätzlichen Fälle aus.</span><span class="sxs-lookup"><span data-stu-id="a0350-113">To select multiple test cases, click the first case to be exported, then hold down the Ctrl key and select the additional cases to be exported.</span></span>

3.  <span data-ttu-id="a0350-114">Klicken Sie auf **Aktion** und dann auf **Test Cases exportieren**.</span><span class="sxs-lookup"><span data-stu-id="a0350-114">Click **Action**, then click **Export test cases**.</span></span>

4.  <span data-ttu-id="a0350-115">Wählen Sie im Dialogfeld **Speichern** unter einen Ordner zum Speichern der exportierten Testfälle aus, und geben Sie im Feld **Dateiname** einen Namen für die resultierende XML-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="a0350-115">In the **Save As** dialog box, select a folder to store the exported test cases and type a name for the resulting XML file in the **File name** box.</span></span> <span data-ttu-id="a0350-116">Beachten Sie, dass alle diese Testfälle in einer einzelnen XML-Datei gespeichert werden, wenn Sie mehrere Test Cases exportieren.</span><span class="sxs-lookup"><span data-stu-id="a0350-116">Note that if you are exporting multiple tests cases all of these test cases will be saved to a single XML file.</span></span>

5.  <span data-ttu-id="a0350-117">Klicken Sie auf **Speichern**, um die Test Cases zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a0350-117">To save the test cases, click **Save**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a0350-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0350-118">See Also</span></span>


[<span data-ttu-id="a0350-119">Importieren von Testfällen für das VoIP-Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0350-119">Import voice routing test cases in Lync Server 2013</span></span>](lync-server-2013-import-voice-routing-test-cases.md)  
  

<span data-ttu-id="a0350-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0350-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

