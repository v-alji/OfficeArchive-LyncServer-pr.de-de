---
title: Importieren von Richtlinien und Einstellungen
description: Importieren von Richtlinien und Einstellungen
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e014b7e8f0498742104118eec9eb313394ae6a94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439604"
---
# <a name="import-policies-and-settings"></a><span data-ttu-id="88668-103">Importieren von Richtlinien und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="88668-103">Import policies and settings</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88668-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88668-104">

<span> </span></span></span>

<span data-ttu-id="88668-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="88668-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="88668-106">Nachdem Sie Ihre Office Communications Server 2007 R2-Topologieinformationen mit Ihrem lync Server 2013-Pilot Pool zusammengeführt haben, müssen Sie ein lync Server 2013-Verwaltungsshell-Cmdlet ausführen, um Ihre Office Communications Server 2007 R2-Richtlinien und-Konfigurationseinstellungen zu Ihrem lync Server 2013-Pilot Pool zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="88668-106">After you merge your Office Communications Server 2007 R2 topology information with your Lync Server 2013 pilot pool, you need to run a Lync Server 2013 Management Shell cmdlet to migrate your Office Communications Server 2007 R2 policies and configuration settings to your Lync Server 2013 pilot pool.</span></span>

<span data-ttu-id="88668-107">Mit dem Cmdlet " **Import-CsLegacyConfiguration** " werden Richtlinien, VoIP-Routen, Wählpläne, Communicator Web Access-URLs und Einwahl Zugriffsnummern in lync Server 2013 importiert.</span><span class="sxs-lookup"><span data-stu-id="88668-107">The **Import-CsLegacyConfiguration** cmdlet imports policies, voice routes, dial plans, Communicator Web Access URLs, and dial-in access numbers to Lync Server 2013.</span></span>

<div>

## <a name="to-migrate-policies-and-settings"></a><span data-ttu-id="88668-108">So migrieren Sie Richtlinien und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="88668-108">To migrate policies and settings</span></span>

1.  <span data-ttu-id="88668-109">Starten Sie auf dem lync Server 2013-Front-End-Server die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="88668-109">On the Lync Server 2013 Front End server, start the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="88668-110">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="88668-110">At the command line, type the following:</span></span>
    
        Import-CsLegacyConfiguration
    
    <span data-ttu-id="88668-111">Nachdem die Richtlinien importiert wurden, führen Sie die folgenden Schritte aus, um die importierten Richtlinien in der lync Server-Systemsteuerung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="88668-111">After the policies are imported, use the procedure that follows to see the imported policies in the Lync Server Control Panel .</span></span>

</div>

<div>

## <a name="to-view-imported-policies"></a><span data-ttu-id="88668-112">So zeigen Sie importierte Richtlinien an</span><span class="sxs-lookup"><span data-stu-id="88668-112">To view imported policies</span></span>

1.  <span data-ttu-id="88668-113">Öffnen Sie die lync Server 2013-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="88668-113">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="88668-114">Klicken Sie auf **sprach Routing** , und zeigen Sie die importierten Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="88668-114">Click **Voice Routing** and view the imported policies.</span></span>

3.  <span data-ttu-id="88668-115">Klicken Sie auf **Konferenzen** , und zeigen Sie die importierten Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="88668-115">Click **Conferencing** and view the imported policies.</span></span>

4.  <span data-ttu-id="88668-116">Klicken Sie auf **Föderation und externer Zugriff** , und zeigen Sie die importierten Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="88668-116">Click **Federation and External Access** and view the imported policies.</span></span>

5.  <span data-ttu-id="88668-117">Klicken Sie auf **Überwachung und Archivierung** , und zeigen Sie die importierten Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="88668-117">Click **Monitoring and Archiving** and view the imported policies.</span></span>

<span data-ttu-id="88668-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88668-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

