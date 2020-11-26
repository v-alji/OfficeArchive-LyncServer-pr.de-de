---
title: 'Lync Server 2013: Ändern des Standard-URL-Filters'
description: 'Lync Server 2013: Ändern Sie den Standard-URL-Filter.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default URL filter
ms:assetid: 80a472b3-054e-45a6-80fc-9ee2bda28ee6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182544(v=OCS.15)
ms:contentKeyID: 48184653
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 079fcc83cd9041f99f1d14663ad51e86f6c23619
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445708"
---
# <a name="modify-the-default-url-filter-in-lync-server-2013"></a><span data-ttu-id="1b833-103">Ändern des Standard-URL-Filters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b833-103">Modify the default URL filter in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1b833-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1b833-104">

<span> </span></span></span>

<span data-ttu-id="1b833-105">_**Letztes Änderungsdatum des Themas:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="1b833-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="1b833-106">Mithilfe des Instant Messaging-Filters (im) stellt lync Server 2013 einen globalen URL-Filter bereit, der bestimmte URLs blockiert, die in Chat Unterhaltungen zwischen Benutzern in ihrer lync Server 2013-Bereitstellung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1b833-106">By using the instant messaging (IM) filter, Lync Server 2013 provides a global URL filter that blocks specific URLs contained in IM conversations among users throughout your Lync Server 2013 deployment.</span></span> <span data-ttu-id="1b833-107">Mithilfe der lync Server-Systemsteuerung können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="1b833-107">By using Lync Server Control Panel, you can do the following:</span></span>

  - <span data-ttu-id="1b833-108">Blockieren Sie alle oder eine Teilmenge der URLs in Sofortnachrichtenunterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="1b833-108">Block all or a subset of URLs in instant message conversations.</span></span>

  - <span data-ttu-id="1b833-109">Alle URLs zulassen.</span><span class="sxs-lookup"><span data-stu-id="1b833-109">Allow all URLs.</span></span> <span data-ttu-id="1b833-110">Optional können Sie eine Benachrichtigung erstellen, die am Anfang jeder Chatnachricht eingefügt wird, die eine URL enthält.</span><span class="sxs-lookup"><span data-stu-id="1b833-110">As an option, you can create a notice that is inserted at the beginning of each instant message that contains a URL.</span></span>

  - <span data-ttu-id="1b833-111">Zulassen bestimmter URLs und einbeziehen einer Warnung in jede Sofortnachricht, die eine URL enthält.</span><span class="sxs-lookup"><span data-stu-id="1b833-111">Allow specific URLs and include a warning with each instant message that contains a URL.</span></span>

<span data-ttu-id="1b833-112">Darüber hinaus können Sie festlegen, dass URLs, die bestimmte Dateitypen enthalten, blockiert werden sollen, oder nur Internet-URLs blockieren, indem Sie URLs zulassen, die sich in der lokalen Intranetzone des Servers befinden – Intranet-URLs –, um den Server zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="1b833-112">In addition, you can choose to block URLs that contain specific file types, or block only Internet URLs by allowing URLs that are within the server’s local intranet zone — intranet URLs — to pass through the server.</span></span> <span data-ttu-id="1b833-113">Details zur URL-Filterung finden Sie unter [Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span><span class="sxs-lookup"><span data-stu-id="1b833-113">For details about URL filtering, see [Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="1b833-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b833-114">See Also</span></span>


[<span data-ttu-id="1b833-115">Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b833-115">Configuring file transfer and URL filtering for instant messaging (IM) in Lync Server 2013</span></span>](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[<span data-ttu-id="1b833-116">Erstellen eines neuen dateiübertragungsfilters in lync Server 2013 für eine bestimmte Website</span><span class="sxs-lookup"><span data-stu-id="1b833-116">Create a new file transfer filter in Lync Server 2013 for a specific site</span></span>](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[<span data-ttu-id="1b833-117">Erstellen eines neuen URL-Filters in lync Server 2013 zur Behandlung von Hyperlinks in Chat Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="1b833-117">Create a new URL filter in Lync Server 2013 to handle hyperlinks in IM conversations</span></span>](lync-server-2013-create-a-new-url-filter-to-handle-hyperlinks-in-im-conversations.md)  
[<span data-ttu-id="1b833-118">Ändern des standardmäßigen dateiübertragungsfilters in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b833-118">Modify the default file transfer filter in Lync Server 2013</span></span>](lync-server-2013-modify-the-default-file-transfer-filter.md)  
  

<span data-ttu-id="1b833-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1b833-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

