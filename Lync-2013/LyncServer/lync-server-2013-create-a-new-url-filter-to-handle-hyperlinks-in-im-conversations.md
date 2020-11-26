---
title: Erstellen eines neuen URL-Filters zur Behandlung von Links in Chat Unterhaltungen
description: Erstellen Sie einen neuen URL-Filter zur Behandlung von Links in Chat Unterhaltungen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new URL filter to handle hyperlinks in IM conversations
ms:assetid: d0ee01e5-f039-4a34-ac9d-659fe4e9e879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182590(v=OCS.15)
ms:contentKeyID: 48185426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e583b3e8cbd04279ab7f54b4138a349fa0d1e85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432121"
---
# <a name="create-a-new-url-filter-in-lync-server-2013-to-handle-hyperlinks-in-im-conversations"></a><span data-ttu-id="dd7ee-103">Erstellen eines neuen URL-Filters in lync Server 2013 zur Behandlung von Hyperlinks in Chat Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="dd7ee-103">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd7ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd7ee-104">

<span> </span></span></span>

<span data-ttu-id="dd7ee-105">_**Letztes Änderungsdatum des Themas:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="dd7ee-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="dd7ee-106">Zusätzlich zum Ändern des globalen URL-Filters können Sie benutzerdefinierte URL-Filter für einzelne Websites in ihrer lync Server 2013-Bereitstellung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-106">In addition to modifying the global URL filter, you can configure custom URL filters for individual sites within your Lync Server 2013 deployment.</span></span> <span data-ttu-id="dd7ee-107">Details zur URL-Filterung finden Sie unter [Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="dd7ee-107">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-create-a-new-url-filter"></a><span data-ttu-id="dd7ee-108">So erstellen Sie einen neuen URL-Filter</span><span class="sxs-lookup"><span data-stu-id="dd7ee-108">To create a new URL filter</span></span>

1.  <span data-ttu-id="dd7ee-109">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="dd7ee-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="dd7ee-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dd7ee-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="dd7ee-112">Klicken Sie in der linken Navigationsleiste auf **Chat und Anwesenheit**, und klicken Sie dann auf **URL-Filter**.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-112">In the left navigation bar, click **IM and Presence**, and then click **URL Filter**.</span></span>

4.  <span data-ttu-id="dd7ee-113">Klicken Sie auf der Seite **URL-Filter** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-113">On the **URL Filter** page, click **New**.</span></span>

5.  <span data-ttu-id="dd7ee-114">Klicken Sie unter **Website auswählen** auf die Website, für die Sie den URL-Filter erstellen möchten, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-114">In **Select a Site**, click the site for which you want to create the URL filter, and then click **OK**.</span></span>

6.  <span data-ttu-id="dd7ee-115">Aktivieren Sie im Dialogfeld **neuer URL-Filter** das Kontrollkästchen **URL-Filter aktivieren** , um die URL-Filterung für die Website zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-115">In the **New URL Filter** dialog box, select the **Enable URL Filter** check box to enable URL filtering for the site.</span></span>

7.  <span data-ttu-id="dd7ee-116">Aktivieren Sie das Kontrollkästchen **URLs mit Dateierweiterung blockieren** , um alle aktiven URLs zu blockieren, die eine Datei mit einer Erweiterung enthalten, die unter **Dateityperweiterungen zum Blockieren** in **Datei Filter bearbeiten** aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-116">To block any active URL that contains a file with an extension listed under **File type extensions to block** in **Edit File Filter**, select the **Block URLs with file extension** check box.</span></span>

8.  <span data-ttu-id="dd7ee-117">Klicken Sie im Dropdown-Listenfeld **Link-Präfix** auf die Option, die dem entspricht, wie URLs in Chat Unterhaltungen behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-117">In the **Hyperlink prefix** drop-down list box, click the option that corresponds to how you want to handle URLs in instant message conversations.</span></span>
    
    <span data-ttu-id="dd7ee-118">Im Dialogfeld " **zulassen** " können Sie beim Senden von Links, die gesendet werden dürfen, eine Warnmeldung an den Benutzer senden.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-118">The **Allow message** box enables a warning message to be sent to the user when sending hyperlinks that are allowed to be sent.</span></span>

9.  <span data-ttu-id="dd7ee-119">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="dd7ee-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dd7ee-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd7ee-120">See Also</span></span>


[<span data-ttu-id="dd7ee-121">Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd7ee-121">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="dd7ee-122">Erstellen eines neuen dateiübertragungsfilters in lync Server 2013 für eine bestimmte Website</span><span class="sxs-lookup"><span data-stu-id="dd7ee-122">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="dd7ee-123">Ändern des standardmäßigen dateiübertragungsfilters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd7ee-123">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[<span data-ttu-id="dd7ee-124">Ändern des Standard-URL-Filters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd7ee-124">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="dd7ee-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd7ee-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

