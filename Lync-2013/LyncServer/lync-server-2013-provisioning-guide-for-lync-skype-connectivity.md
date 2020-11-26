---
title: 'Lync Server 2013: Leitfaden für die Bereitstellung der Lync-Skype-Konnektivität'
description: 'Lync Server 2013: Bereitstellungshandbuch für Lync-Skype Konnektivität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Provisioning guide for Lync-Skype connectivity
ms:assetid: 69adda9b-5b72-4538-9be6-079b2f462e09
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440173(v=OCS.15)
ms:contentKeyID: 57793363
ms.date: 11/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9859a7a621ba4329fe0436fe50a0d9de1d0ae1ef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436741"
---
# <a name="provisioning-guide-for-lync-skype-connectivity-in-lync-server-2013"></a><span data-ttu-id="6e234-103">Leitfaden für die Bereitstellung der Lync-Skype-Konnektivität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e234-103">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e234-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e234-104">

<span> </span></span></span>

<span data-ttu-id="6e234-105">_**Letztes Änderungsdatum des Themas:** 2014-11-26_</span><span class="sxs-lookup"><span data-stu-id="6e234-105">_**Topic Last Modified:** 2014-11-26_</span></span>

<span data-ttu-id="6e234-106">Lync Server 2013 unterstützt die Konnektivität mit Skype.</span><span class="sxs-lookup"><span data-stu-id="6e234-106">Lync Server 2013 supports connectivity with Skype.</span></span> <span data-ttu-id="6e234-107">Mit dieser Konnektivität können Ihre lync 2013-Benutzer Skype-Kontakte mit dem Microsoft-Konto des Skype-Benutzers (MSA) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6e234-107">This connectivity enables your Lync 2013 users to add Skype contacts by using the Skype user’s Microsoft Account (MSA).</span></span> <span data-ttu-id="6e234-108">Skype-Clients können auch lync-Benutzer zu Ihrer Kontaktliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6e234-108">Skype clients can also add Lync users to their contact list.</span></span> <span data-ttu-id="6e234-109">Auf der Grundlage der in lync Server festgelegten Richtlinien können lync-und Skype-Benutzer über Chats kommunizieren, die Anwesenheit des jeweils anderen sehen und Audio-und Videoanrufe initiieren.</span><span class="sxs-lookup"><span data-stu-id="6e234-109">Based on policies administratively set in Lync Server, Lync and Skype users will be able to communicate using instant messaging, see each other’s presence, and initiate audio and video calls.</span></span> <span data-ttu-id="6e234-110">Lync-Skype Konnektivität ist auch eine Funktion von lync Online und kann für lync Online-Kunden über die lync-Verwaltungskonsole im Microsoft 365 Admin Center aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="6e234-110">Lync-Skype connectivity is also a feature of Lync Online, and can be enabled for Lync Online customers from the Lync Administration Center within the Microsoft 365 admin center.</span></span>

<div>

> [!IMPORTANT]  
> <span data-ttu-id="6e234-p102">Wenn Lync Server bereits für die Herstellung der Verbindung zu Windows Messenger über PIC (Public Instant Messaging Connectivity, Verbindung mit öffentlichen Instant Messaging-Diensten) konfiguriert ist, ist Ihre Umgebung bereits für die Lync-Skype-Konnektivität konfiguriert. Die einzige Änderung, die Sie ggf. vornehmen möchten, ist, den vorhandenen Messenger PIC-Eintrag in "Skype" umzubenennen. Einzelheiten hierzu finden Sie unter "Konfigurieren der Einstellung des Skype PIC-Anbieters für Lync" an späterer Stelle in diesem Leitfaden.</span><span class="sxs-lookup"><span data-stu-id="6e234-p102">If Lync Server is already configured to connect with Windows Messenger by using Public Instant Messaging Connectivity (PIC), your deployment is already configured for Lync-Skype connectivity. The only change you may want to consider is to rename your existing Messenger PIC entry as Skype. For details, see Configure the Skype PIC provider setting for Lync later in this guide.</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6e234-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6e234-114">In This Section</span></span>

  - [<span data-ttu-id="6e234-115">Hinweis zu Lync-Skype Konnektivität in lync Server 2013 für lync Online-Kunden</span><span class="sxs-lookup"><span data-stu-id="6e234-115">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>](lync-server-2013-note-about-lync-skype-connectivity-for-lync-on.md)

  - [<span data-ttu-id="6e234-116">Zugreifen auf die Lync Server-Bereitstellungswebsite für Verbindungen mit öffentlichen Chatdiensten von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e234-116">Accessing the Lync Server public IM connectivity provisioning site from Lync Server 2013</span></span>](lync-server-2013-accessing-the-lync-server-public-im-connectivity-provisioning-site.md)

  - [<span data-ttu-id="6e234-117">Aktivieren der Lync-Skype-Konnektivität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e234-117">Enabling Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-enabling-lync-skype-connectivity.md)

  - [<span data-ttu-id="6e234-118">Verwenden von Lync-Skype-Konnektivität als Endbenutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e234-118">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>](lync-server-2013-using-lync-skype-connectivity-as-an-end-user.md)

  - [<span data-ttu-id="6e234-119">Häufig gestellte Fragen: Bereitstellen der Skype-Konnektivität für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e234-119">Frequently Asked Questions: Provisioning Lync Server 2013 for Skype connectivity</span></span>](lync-server-2013-frequently-asked-questions-provisioning-lync-server-for-skype-connectivity.md)

<span data-ttu-id="6e234-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e234-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

