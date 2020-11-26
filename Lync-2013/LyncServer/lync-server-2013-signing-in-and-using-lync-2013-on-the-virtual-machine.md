---
title: 'Lync Server 2013: Anmelden bei und Verwenden von Lync 2013 auf dem virtuellen Computer'
description: 'Lync Server 2013: anmelden und Verwenden von lync 2013 auf dem virtuellen Computer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Signing in and using Lync 2013 on the virtual machine
ms:assetid: 6140fc19-5bef-4b58-9b0f-19112b5ecd00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204948(v=OCS.15)
ms:contentKeyID: 48184318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad9a92d450fb9d60aed70617089d95280528892f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444703"
---
# <a name="signing-in-and-using-lync-2013-on-the-virtual-machine"></a><span data-ttu-id="b91e1-103">Anmelden bei und Verwenden von Lync 2013 auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b91e1-103">Signing in and using Lync 2013 on the virtual machine</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b91e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b91e1-104">

<span> </span></span></span>

<span data-ttu-id="b91e1-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="b91e1-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="b91e1-106">Nachdem das VDI-Plug-in aktiviert wurde, treten die folgenden Schritte auf, wenn sich der Benutzer bei lync 2013 anmeldet.</span><span class="sxs-lookup"><span data-stu-id="b91e1-106">After the VDI plug-in is enabled, the following steps occur when the user signs in to Lync 2013.</span></span>

1.  <span data-ttu-id="b91e1-107">Der Benutzer gibt seine Anmeldeinformationen in den lync 2013-Client ein, der auf dem virtuellen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b91e1-107">The user types his or her credentials in to the Lync 2013 client running on the virtual machine.</span></span>

2.  <span data-ttu-id="b91e1-108">Nachdem lync die Verfügbarkeit des VDI-Plug-ins erkannt hat, fordert lync den Benutzer auf, seine Anmeldeinformationen erneut einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b91e1-108">After Lync detects the availability of the VDI plug-in, Lync prompts the user to re-enter his or her credentials.</span></span> <span data-ttu-id="b91e1-109">In diesem Dialogfeld sollten die Benutzer das Kontrollkästchen **Kennwort speichern** aktivieren, damit sie die Anmeldeinformationen bei folgenden Anmeldevorgängen nicht erneut eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="b91e1-109">In this dialog box, we recommend that the user select the **Save my password** check box so that he or she will not be required to enter credentials during subsequent sign in.</span></span>

3.  <span data-ttu-id="b91e1-110">Lync beginnt die Kopplung mit dem VDI-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="b91e1-110">Lync begins pairing with the VDI plug-in.</span></span> <span data-ttu-id="b91e1-111">Bevor die Kopplung abgeschlossen ist, zeigt der Client zwei Symbole in der lync-Statusleiste an.</span><span class="sxs-lookup"><span data-stu-id="b91e1-111">Before pairing is complete, the client displays two icons in the Lync status bar.</span></span> <span data-ttu-id="b91e1-112">Das Symbol in der unteren linken Ecke zeigt an, dass keine Audiogeräte verfügbar sind, und das blinkende Symbol in der unteren rechten Ecke zeigt an, dass die VDI-Kopplung in Bearbeitung ist (siehe Abbildung).</span><span class="sxs-lookup"><span data-stu-id="b91e1-112">The icon in the lower left indicates that no audio devices are available, and the blinking icon in the lower right indicates that the VDI pairing is in progress, as shown:</span></span>
    
    <span data-ttu-id="b91e1-113">![Lync-VDI-Symbol mit erfolgreicher Kopplung](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync-VDI-Symbol mit erfolgreicher Kopplung")</span><span class="sxs-lookup"><span data-stu-id="b91e1-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>  

4.  <span data-ttu-id="b91e1-114">Nach einer erfolgreichen VDI-Kopplung ändern sich die Symbole und zeigen nun das für Anrufe verwendete Audiogerät bzw. den Erfolg der VDI-Kopplung an:</span><span class="sxs-lookup"><span data-stu-id="b91e1-114">After VDI pairing is successful, the icons change to indicate the audio device that will be used for calls and the VDI pairing success:</span></span>
    
    <span data-ttu-id="b91e1-115">![Lync-VDI-Kopplungs Symbol mit Erfolg](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync-VDI-Kopplungs Symbol mit Erfolg")</span><span class="sxs-lookup"><span data-stu-id="b91e1-115">![Lync VDI pairing icon showing success](images/JJ204948.57be3387-a3e5-4949-831e-f5ff9fcc5598(OCS.15).png "Lync VDI pairing icon showing success")</span></span>  

5.  <span data-ttu-id="b91e1-116">Nach lync-Paaren mit dem VDI-Plug-in kann der Benutzer seine Anwesenheit auf lync-kompatiblen Geräten sehen, die mit dem lokalen Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="b91e1-116">After Lync pairs with the VDI plug-in, the user can see his or her presence on Lync compatible devices that are connected to the local computer.</span></span> <span data-ttu-id="b91e1-117">Der Benutzer kann nun wie gewohnt Anrufe tätigen und annehmen.</span><span class="sxs-lookup"><span data-stu-id="b91e1-117">The user can now place and answer calls as usual.</span></span>

<span data-ttu-id="b91e1-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b91e1-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

