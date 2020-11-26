---
title: 'Lync Server 2013: Installieren von lync für Windows Phone'
description: 'Lync Server 2013: Installieren von lync für Windows phone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Lync for Windows Phone
ms:assetid: bf502546-ff69-489f-a92e-a78b58803d53
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690996(v=OCS.15)
ms:contentKeyID: 51541513
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f5da90a5dc0babdc6944e4f9c426fe896d4f156
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427047"
---
# <a name="installing-lync-for-windows-phone-in-lync-server-2013"></a><span data-ttu-id="06a67-103">Installieren von lync für Windows phone in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="06a67-103">Installing Lync for Windows Phone in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="06a67-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="06a67-104">

<span> </span></span></span>

<span data-ttu-id="06a67-105">_**Letztes Änderungsdatum des Themas:** 2014-02-03_</span><span class="sxs-lookup"><span data-stu-id="06a67-105">_**Topic Last Modified:** 2014-02-03_</span></span>

<span data-ttu-id="06a67-106">Lync 2013 für Windows Phone ist eine vom Benutzer installierbare Anwendung, die auf dem Windows Phone Marketplace zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="06a67-106">Lync 2013 for Windows Phone is a user-installable application that is available in the Windows Phone Marketplace.</span></span>

<div>

## <a name="installing-lync-for-windows-mobile"></a><span data-ttu-id="06a67-107">Installieren von lync für Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="06a67-107">Installing Lync for Windows Mobile</span></span>

<span data-ttu-id="06a67-108">Sie können Ihre Benutzer anweisen, lync 2013 für Windows Phone auf Ihren Geräten zu installieren, indem Sie Sie an den Windows Phone Marketplace unterrichten <https://go.microsoft.com/fwlink/p/?linkid=231901> .</span><span class="sxs-lookup"><span data-stu-id="06a67-108">You can instruct your users to install Lync 2013 for Windows Phone on their devices by directing them to the Windows Phone Marketplace at <https://go.microsoft.com/fwlink/p/?linkid=231901>.</span></span>

</div>

<div>

## <a name="if-you-use-a-dns-srv-record-to-publish-exchange-web-services"></a><span data-ttu-id="06a67-109">Wenn Sie einen DNS-SRV-Eintrag zum Veröffentlichen von Exchange-Webdiensten verwenden</span><span class="sxs-lookup"><span data-stu-id="06a67-109">If You Use a DNS SRV Record to Publish Exchange Web Services</span></span>

<span data-ttu-id="06a67-110">Um die Exchange-Integration für lync-Clients zu aktivieren, veröffentlichen einige Organisationen die Exchange-Webdienste-URL mithilfe eines DNS-SRV-Eintrags.</span><span class="sxs-lookup"><span data-stu-id="06a67-110">To enable Exchange integration for Lync clients, some organizations publish the Exchange Web Services URL by using a DNS SRV record.</span></span> <span data-ttu-id="06a67-111">Das Dokument "Understanding and Troubleshooting Exchange Integration", das im Microsoft Download Center verfügbar ist [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095) , beschreibt Szenarien, in denen dies erforderlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="06a67-111">The document "Understanding and Troubleshooting Exchange Integration," available in the Microsoft Download Center at [https://go.microsoft.com/fwlink/?LinkID=391095](https://go.microsoft.com/fwlink/?linkid=391095), describes scenarios in which this might be necessary.</span></span> <span data-ttu-id="06a67-112">Die Exchange-Integration für Windows Phone-Benutzer funktioniert in diesem Szenario jedoch nicht, da die Windows Phone-Plattform keine SRV-Lookups unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06a67-112">However, Exchange integration for Windows Phone users will not work in this scenario, because the Windows Phone platform does not support SRV lookups.</span></span> <span data-ttu-id="06a67-113">Sie müssen Windows Phone-Benutzer anweisen, die Exchange-Webdienste-URL anzugeben, anstatt dem Smartphone den automatischen Erkennen des Servers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="06a67-113">You will need to instruct Windows Phone users to specify the Exchange Web Services URL instead of allowing the phone to automatically detect the server.</span></span>

<span data-ttu-id="06a67-114">Weisen Sie die Benutzer an, die lync-Einstellungen auf Ihren Windows-Smartphones wie folgt zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="06a67-114">Instruct your users to configure the Lync settings on their Windows Phones as follows:</span></span>

1.  <span data-ttu-id="06a67-115">Wählen Sie in Windows phone in den lync-Einstellungen den Bildschirm **Exchange** aus.</span><span class="sxs-lookup"><span data-stu-id="06a67-115">In Windows Phone, in the Lync settings, select the **Exchange** screen.</span></span>

2.  <span data-ttu-id="06a67-116">Verschieben Sie den **Server automatisch erkennen** auf **aus**.</span><span class="sxs-lookup"><span data-stu-id="06a67-116">Move **Auto-Detect Server** to **Off**.</span></span>

3.  <span data-ttu-id="06a67-117">Tippen Sie auf das leere Feld, und geben Sie den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder die URL für Exchange Web Services ein.</span><span class="sxs-lookup"><span data-stu-id="06a67-117">Tap the empty field and enter the fully qualified domain name (FQDN) or URL for Exchange Web Services.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="06a67-118">Sie können entweder den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder die vollständige URL Ihres Exchange-Webdienste-Servers angeben.</span><span class="sxs-lookup"><span data-stu-id="06a67-118">You can specify either the fully qualified domain name (FQDN) or the full URL of your Exchange Web Services server.</span></span> <span data-ttu-id="06a67-119">Wenn Sie den FQDN angeben, werden das Protokoll (https://) und der Exchange-Webdienste Pfad (/EWS/Exchange.asmx) automatisch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="06a67-119">If you specify the FQDN, the protocol (https://) and the Exchange Web Services path (/ews/exchange.asmx) are added automatically.</span></span> <span data-ttu-id="06a67-120">Wenn ihr Pfad für Exchange-Webdienste anders ist, können Sie die vollständige URL angeben.</span><span class="sxs-lookup"><span data-stu-id="06a67-120">If your Exchange Web Services path is different, you can specify the full URL.</span></span>

    
    </div>

4.  <span data-ttu-id="06a67-121">Schließen Sie den Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="06a67-121">Close the screen.</span></span>

</div>

<div>

## <a name="verifying-mobile-client-installation"></a><span data-ttu-id="06a67-122">Überprüfen der Installation des mobilen Clients</span><span class="sxs-lookup"><span data-stu-id="06a67-122">Verifying Mobile Client Installation</span></span>

<span data-ttu-id="06a67-123">Nachdem Sie den Client konfiguriert und sich erfolgreich angemeldet haben, verwenden Sie die folgenden Tests, um zu überprüfen, ob Ihre Installation von lync 2013 auf Ihrem mobilen Gerät ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="06a67-123">After you configure the client and sign in successfully, use the following tests to verify that your installation of Lync 2013 is working correctly on your mobile device.</span></span>

<span data-ttu-id="06a67-124">**Suchen nach einem Kontakt im Unternehmensverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="06a67-124">**Search for a contact in the corporate directory**</span></span>

1.  <span data-ttu-id="06a67-125">Tippen Sie in der Kontaktliste unten auf **Suchen** .</span><span class="sxs-lookup"><span data-stu-id="06a67-125">In the Contacts list, tap **Search** at the bottom.</span></span>

2.  <span data-ttu-id="06a67-126">Suchen Sie einen Kontakt, der nur in der globalen Adressliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="06a67-126">Search for a contact that exists only in the global address list.</span></span>

3.  <span data-ttu-id="06a67-127">Stellen Sie sicher, dass der Kontaktname in den Suchergebnissen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06a67-127">Verify that the contact name appears in the search results.</span></span>

<span data-ttu-id="06a67-128">**Testen der Chat- und Anwesenheitsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="06a67-128">**Test instant messaging and presence**</span></span>

1.  <span data-ttu-id="06a67-129">Tippen Sie in der Kontaktliste auf einen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="06a67-129">In the Contacts list, tap a contact.</span></span>

2.  <span data-ttu-id="06a67-130">Tippen Sie auf der Visitenkarte auf das Symbol **Chat** .</span><span class="sxs-lookup"><span data-stu-id="06a67-130">In the contact card, tap the **IM** icon.</span></span>

3.  <span data-ttu-id="06a67-131">Stellen Sie sicher, dass ein Chatfenster zum Eingeben und Senden einer Sofortnachricht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="06a67-131">Verify that an instant messaging (IM) window appears and that you can type and send an IM.</span></span>

<span data-ttu-id="06a67-132">**Testen der Auswahlkonferenz**</span><span class="sxs-lookup"><span data-stu-id="06a67-132">**Test dial-out conferencing**</span></span>

1.  <span data-ttu-id="06a67-133">Planen Sie in Outlook eine lync-Besprechung.</span><span class="sxs-lookup"><span data-stu-id="06a67-133">In Outlook, schedule a Lync meeting.</span></span>

2.  <span data-ttu-id="06a67-134">Öffnen Sie auf dem mobilen Gerät die Besprechungseinladung.</span><span class="sxs-lookup"><span data-stu-id="06a67-134">On the mobile device, open the meeting invitation.</span></span>

3.  <span data-ttu-id="06a67-135">Klicken Sie in der Besprechung auf den Link, um an der Besprechung teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="06a67-135">Click the link in the meeting to join.</span></span>

4.  <span data-ttu-id="06a67-136">Nehmen Sie den Anruf vom Konferenzdienst entgegen und stellen Sie sicher, dass Sie mit dem Besprechungsaudio verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="06a67-136">Answer the call from the conference service and verify that you are connected to meeting audio.</span></span>

<span data-ttu-id="06a67-137">**Testen von Pushbenachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="06a67-137">**Test push notifications**</span></span>

1.  <span data-ttu-id="06a67-138">Registrieren Sie sich auf dem mobilen Gerät von Benutzer a bei lync mit dem Konto von Benutzer a.</span><span class="sxs-lookup"><span data-stu-id="06a67-138">On user A’s mobile device, sign in to Lync with user A’s account.</span></span>

2.  <span data-ttu-id="06a67-139">Öffnen Sie eine andere Anwendung auf dem mobilen Gerät.</span><span class="sxs-lookup"><span data-stu-id="06a67-139">Open another application on the mobile device.</span></span>

3.  <span data-ttu-id="06a67-140">Bei einem anderen Client können Sie sich mit dem Konto von Benutzer B bei lync anmelden.</span><span class="sxs-lookup"><span data-stu-id="06a67-140">On a different client, sign in to Lync with user B’s account.</span></span>

4.  <span data-ttu-id="06a67-141">Senden Sie eine Sofortnachricht von Benutzer B an Benutzer A.</span><span class="sxs-lookup"><span data-stu-id="06a67-141">Send an IM from user B to user A.</span></span>

5.  <span data-ttu-id="06a67-142">Stellen Sie sicher, dass die Sofortnachricht auf dem mobilen Gerät von Benutzer A erscheint.</span><span class="sxs-lookup"><span data-stu-id="06a67-142">Verify that the IM notification appears on user A’s mobile device.</span></span>

<span data-ttu-id="06a67-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="06a67-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

