---
title: 'Lync Server 2013: Konfigurieren von Standardbild Optionen'
description: 'Lync Server 2013: Konfigurieren von Standardbild Optionen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring default picture options
ms:assetid: b1c986f0-6400-447a-9e36-78c1c3a4f793
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn205074(v=OCS.15)
ms:contentKeyID: 56280893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6261aca82b4c71eb8e0573e8d2adbfc008e743fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433213"
---
# <a name="configuring-default-picture-options-in-lync-server-2013"></a><span data-ttu-id="8683a-103">Konfigurieren von Standardbild Optionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8683a-103">Configuring default picture options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8683a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8683a-104">

<span> </span></span></span>

<span data-ttu-id="8683a-105">_**Letztes Änderungsdatum des Themas:** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="8683a-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="8683a-106">Standardmäßig werden die Bilder der Benutzer automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8683a-106">By default, users’ pictures are automatically displayed.</span></span> <span data-ttu-id="8683a-107">Wenn Benutzer Ihre Bilder ausblenden möchten, können Sie die Option " **mein Bild ausblenden** " im lync-Client auswählen.</span><span class="sxs-lookup"><span data-stu-id="8683a-107">If users want to hide their pictures, they can select the **Hide my picture** option in the Lync client.</span></span> <span data-ttu-id="8683a-108">Diese Einstellung wird jedoch von einigen anderen Office-Anwendungen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8683a-108">However, this setting is ignored by some other Office applications.</span></span>

<span data-ttu-id="8683a-109">Wenn die Möglichkeit zum Anzeigen von Bildern, auch wenn Sie vom Benutzer deaktiviert werden, problematisch ist, können Sie die Einstellungen für die lync-Bildanzeige Global oder für eine Website oder einen Dienst ändern, damit die Bilder der Benutzer nicht standardmäßig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8683a-109">If the possibility of displaying pictures even when turned off by the user is a concern, you can change Lync picture display settings globally or for a site or service so that users’ pictures are not shown by default.</span></span> <span data-ttu-id="8683a-110">Verwenden Sie das folgende Cmdlet der lync Server-Verwaltungsshell, damit die Bilder des Benutzers nur angezeigt werden, wenn Sie die Option " **mein Bild anzeigen** " im Client explizit auswählen:</span><span class="sxs-lookup"><span data-stu-id="8683a-110">Use the following Lync Server Management Shell cmdlet so that user’s pictures will not be shown unless they explicitly select the **Show my picture** option in the client:</span></span>

    Set-CsPrivacyConfiguration -DisplayPublishedPhotoDefault $False

<span data-ttu-id="8683a-111">Weitere Informationen zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell unter [CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="8683a-111">For more information about this cmdlet, see the [Set-CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="8683a-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8683a-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

