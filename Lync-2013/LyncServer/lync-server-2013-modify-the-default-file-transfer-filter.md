---
title: 'Lync Server 2013: Ändern des standardmäßigen dateiübertragungsfilters'
description: 'Lync Server 2013: Ändern des standardmäßigen dateiübertragungsfilters'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default file transfer filter
ms:assetid: 791774a2-0bb6-4b5b-aeb0-ff69abb170f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521017(v=OCS.15)
ms:contentKeyID: 48184584
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8091dfebea87b793c56b9a670cfeeeab15ce6c44
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445722"
---
# <a name="modify-the-default-file-transfer-filter-in-lync-server-2013"></a><span data-ttu-id="42086-103">Ändern des standardmäßigen dateiübertragungsfilters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42086-103">Modify the default file transfer filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42086-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42086-104">

<span> </span></span></span>

<span data-ttu-id="42086-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="42086-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="42086-106">Lync Server 2013 bietet einen globalen Dateiübertragungsfilter, der bestimmte Dateitypen während der folgenden dateibezogenen Aktivitäten innerhalb ihrer lync Server 2013-Bereitstellung blockiert:</span><span class="sxs-lookup"><span data-stu-id="42086-106">Lync Server 2013 provides a global file transfer filter that blocks specific types of files during the following file-related activities within your Lync Server 2013 deployment:</span></span>

  - <span data-ttu-id="42086-107">Dateiübertragungsanforderungen während Chat Unterhaltungen (Sofortnachrichten)</span><span class="sxs-lookup"><span data-stu-id="42086-107">File transfer requests during instant messaging (IM) conversations</span></span>

  - <span data-ttu-id="42086-108">Hochladen und Herunterladen von Dateien beim Verwenden des Handzettel Features im Office Live Meeting 2007-Client</span><span class="sxs-lookup"><span data-stu-id="42086-108">File uploads and downloads while using the handout feature in the Office Live Meeting 2007 client</span></span>

  - <span data-ttu-id="42086-109">Multimedia-Wiedergabe während Konferenzen</span><span class="sxs-lookup"><span data-stu-id="42086-109">Multimedia playback during conferences</span></span>

<span data-ttu-id="42086-110">Je nach den Dateitypen, die Sie blockieren oder zulassen möchten, können Sie den globalen Filter mithilfe der lync Server-Systemsteuerung ändern.</span><span class="sxs-lookup"><span data-stu-id="42086-110">Depending on the types of files you want to block or allow, you can use Lync Server Control Panel to modify the global filter.</span></span> <span data-ttu-id="42086-111">Details zum Filtern von Dateiübertragungen finden Sie unter [Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="42086-111">For details about file transfer filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="to-modify-the-default-file-transfer-filter"></a><span data-ttu-id="42086-112">So ändern Sie den standardmäßigen Dateiübertragungsfilter</span><span class="sxs-lookup"><span data-stu-id="42086-112">To modify the default file transfer filter</span></span>

1.  <span data-ttu-id="42086-113">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="42086-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="42086-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="42086-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="42086-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="42086-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="42086-116">Klicken Sie in der linken Navigationsleiste auf **Chat und Anwesenheit** , und klicken Sie dann auf **Datei Filter**.</span><span class="sxs-lookup"><span data-stu-id="42086-116">In the left navigation bar, click **IM and Presence** and then click **File Filter**.</span></span>

4.  <span data-ttu-id="42086-117">Doppelklicken Sie auf der Seite **Dateifilter** auf den **globalen** Filter.</span><span class="sxs-lookup"><span data-stu-id="42086-117">On the **File Filter** page, double-click the **Global** filter.</span></span>

5.  <span data-ttu-id="42086-118">Aktivieren Sie unter **Dateifilter bearbeiten** das Kontrollkästchen **Dateifilter aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="42086-118">In **Edit File Filter**, select the **Enable file filter** check box.</span></span>

6.  <span data-ttu-id="42086-119">Klicken Sie im Dropdown-Listenfeld **Dateiübertragung** auf **Alle blockieren** oder **bestimmte Dateitypen blockieren**.</span><span class="sxs-lookup"><span data-stu-id="42086-119">In the **File transfer** drop-down list box, click **Block All** or **Block specific file types**.</span></span>

7.  <span data-ttu-id="42086-120">Wenn Sie auf **Alle blockieren** geklickt haben, fahren Sie mit Schritt 9 fort.</span><span class="sxs-lookup"><span data-stu-id="42086-120">If you clicked **Block All**, skip to step 9.</span></span>

8.  <span data-ttu-id="42086-121">Wenn Sie auf **bestimmte Dateitypen blockieren** geklickt haben, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="42086-121">If you clicked **Block specific file types**, do the following:</span></span>
    
    1.  <span data-ttu-id="42086-122">Klicken Sie auf **auswählen** , um die Standardliste der Dateitypen Erweiterungen zu ändern, die Sie blockieren möchten.</span><span class="sxs-lookup"><span data-stu-id="42086-122">Click **Select** to modify the default list of file type extensions that you want to block.</span></span>
    
    2.  <span data-ttu-id="42086-123">Wählen Sie unter **Dateityp** auswählen die Dateitypen aus, die Sie blockieren oder zulassen möchten, indem Sie deren Erweiterungen aus den Kategorien unter **Dateityperweiterungen** hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="42086-123">In **Select File Type**, select the file types that you want to block or allow by adding or removing their extensions from the categories under **File type extensions**.</span></span>
    
    3.  <span data-ttu-id="42086-124">Wenn die Erweiterung für einen Dateityp, den Sie blockieren möchten, nicht angezeigt wird, geben Sie die Erweiterung in das Textfeld unter **Hinzufügen von Dateityperweiterungen zur Liste** ein, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="42086-124">If you do not see the extension for a file type that you want to block, type the extension in the text box under **Add file type extensions to the list**, and then click **Add**.</span></span>
    
    4.  <span data-ttu-id="42086-125">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="42086-125">Click **OK**.</span></span>

9.  <span data-ttu-id="42086-126">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="42086-126">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="42086-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42086-127">See Also</span></span>


[<span data-ttu-id="42086-128">Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42086-128">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="42086-129">Erstellen eines neuen dateiübertragungsfilters in lync Server 2013 für eine bestimmte Website</span><span class="sxs-lookup"><span data-stu-id="42086-129">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="42086-130">Erstellen eines neuen URL-Filters in lync Server 2013 zur Behandlung von Hyperlinks in Chat Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="42086-130">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  


[<span data-ttu-id="42086-131">Ändern des Standard-URL-Filters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42086-131">Modify the default URL filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-url-filter.md)  
  

<span data-ttu-id="42086-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42086-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

