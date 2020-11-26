---
title: 'Lync Server 2013: Unterstützung für Exchange und SharePoint-Integration'
description: 'Lync Server 2013: Exchange-und SharePoint-Integrationsunterstützung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange and SharePoint integration support
ms:assetid: 72bf8aa5-55b1-4851-8a59-c96bf85d215a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205005(v=OCS.15)
ms:contentKeyID: 48184504
ms.date: 01/20/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7416ffa23de9a0820c3087d18254810d58444ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428405"
---
# <a name="exchange-and-sharepoint-integration-support-in-lync-server-2013"></a><span data-ttu-id="0077d-103">Unterstützung für Exchange-und SharePoint-Integration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0077d-103">Exchange and SharePoint integration support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0077d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0077d-104">

<span> </span></span></span>

<span data-ttu-id="0077d-105">_**Letztes Änderungsdatum des Themas:** 2017-01-18_</span><span class="sxs-lookup"><span data-stu-id="0077d-105">_**Topic Last Modified:** 2017-01-18_</span></span>

<span data-ttu-id="0077d-106">Lync Server 2013 und lync 2013 können sicher und nahtlos mit anderen Anwendungen und Server Produkten kommunizieren, einschließlich Office 2013, Exchange Server 2013, Exchange Server 2016 und SharePoint, wenn Sie diese Produkte integrieren.</span><span class="sxs-lookup"><span data-stu-id="0077d-106">Lync Server 2013 and Lync 2013 can securely and seamlessly communicate with other applications and server products, including Office 2013, Exchange Server 2013, Exchange Server 2016, and SharePoint, if you integrate these products.</span></span> <span data-ttu-id="0077d-107">Durch die Integration von lync Server 2013 und Office erhalten Benutzer einen kontextbezogenen Zugriff auf Instant Messaging (im), erweiterte Anwesenheits-, Telefonie-und Konferenzfunktionen von lync.</span><span class="sxs-lookup"><span data-stu-id="0077d-107">Integrating Lync Server 2013 and Office provides users with in-context access to the instant messaging (IM), enhanced presence, telephony, and conferencing capabilities of Lync.</span></span> <span data-ttu-id="0077d-108">Office-Benutzer können im Outlook 2013-Messaging-und-Zusammenarbeitsclient sowie in anderen Office-Programmen oder auf einer SharePoint-Seite auf lync-Features zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0077d-108">Office users can access Lync features from within the Outlook 2013 messaging and collaboration client and other Office programs or from a SharePoint page.</span></span> <span data-ttu-id="0077d-109">Benutzer können auch einen Datensatz mit lync-Unterhaltungen im Outlook-Ordner "Konversations Verlauf" anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0077d-109">Users can also view a record of Lync conversations in the Outlook Conversation History folder.</span></span> <span data-ttu-id="0077d-110">Wenn Sie in Exchange 2013, Exchange 2016 oder Exchange Online integriert sind, unterstützt lync Server 2013 auch die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="0077d-110">When integrated with Exchange 2013, Exchange 2016, or Exchange Online, Lync Server 2013 also supports the following:</span></span>

  - <span data-ttu-id="0077d-111">Einheitlicher Kontaktspeicher, mit dem Benutzer alle Kontaktinformationen in Exchange oder Exchange Online speichern können, damit die Informationen Global über lync 2013, Exchange, Outlook und Outlook Web App zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="0077d-111">Unified contact store, which enables users to store all contact information in Exchange or Exchange Online so that the information is available globally across Lync 2013, Exchange, Outlook, and Outlook Web App.</span></span>

  - <span data-ttu-id="0077d-112">Konversations Verlauf und Webkonferenz Verlauf, der in Exchange-Benutzerordnern gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0077d-112">Conversation history and Web conferencing history, which is stored in Exchange user folders.</span></span>

  - <span data-ttu-id="0077d-113">Archivierte Inhalte aus lync, wie Chat-und Besprechungsinhalte, können im Exchange-Speicher gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0077d-113">Archived content from Lync, such as IM and meeting content, can be stored in Exchange storage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0077d-114">Lync Server 2013 unterstützt die Integration in frühere Versionen von Microsoft Exchange Server und SharePoint Server, aber nicht alle Funktionen werden mit diesen vorherigen Versionen unterstützt, beispielsweise die Integration von Archivierungsspeicher mit Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="0077d-114">Lync Server 2013 supports integration with previous versions of Microsoft Exchange Server and SharePoint Server, but not all functionality is supported with these previous versions, such as integration of Archiving storage with Microsoft Exchange.</span></span><BR><span data-ttu-id="0077d-115">Wenn Sie Ihre Benutzer zu Exchange 2013 oder Exchange 2016 migrieren, können Sie Exchange-Speicher und lync Server-Speicher auf Interimsbasis verwenden, während Sie die Migration abschließen.</span><span class="sxs-lookup"><span data-stu-id="0077d-115">If you are migrating your users to Exchange 2013 or Exchange 2016, you can use both Exchange storage and Lync Server storage on an interim basis, while you complete the migration.</span></span> <span data-ttu-id="0077d-116">Die permanente Verwendung von Exchange und lync Server-Speicher wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0077d-116">Permanent use of both Exchange and Lync Server storage is not supported.</span></span>



</div>

<span data-ttu-id="0077d-117">Die Integration von lync Server 2013 mit Exchange Server und SharePoint Server erfordert eine Server-zu-Server-Authentifizierung zwischen Servern mit lync Server 2013, Exchange Server und SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="0077d-117">Integration of Lync Server 2013 with Exchange Server and SharePoint Server requires server-to-server authentication between servers running Lync Server 2013, Exchange Server, and SharePoint Server.</span></span> <span data-ttu-id="0077d-118">Lync Server 2013 unterstützt das OAuth (Open Authorization)-Protokoll für die Server-zu-Server-Authentifizierung und-Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="0077d-118">Lync Server 2013 supports OAuth (Open Authorization) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="0077d-119">Für die lokale Server-zu-Server-Authentifizierung zwischen zwei Microsoft-Servern muss kein tokenserver eines Drittanbieters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0077d-119">For on-premises server-to-server authentication between two Microsoft servers, there is no need to use a third-party token server.</span></span> <span data-ttu-id="0077d-120">Lync Server 2013, Exchange Server und SharePoint Server verfügen über einen integrierten tokenserver, der für Authentifizierungszwecke untereinander verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0077d-120">Lync Server 2013, Exchange Server, and SharePoint Server have a built-in token server that can be used for authentication purposes with each other.</span></span> <span data-ttu-id="0077d-121">Lync Server 2013 kann beispielsweise ein Sicherheitstoken selbst ausgeben und Signieren und dieses Token bei der Kommunikation mit Exchange verwenden.</span><span class="sxs-lookup"><span data-stu-id="0077d-121">For example, Lync Server 2013 can issue and sign a security token by itself, and use that token when communicating with Exchange.</span></span> <span data-ttu-id="0077d-122">In diesem Fall ist es nicht erforderlich, einen Token Server eines Drittanbieters zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0077d-122">In this case, there is no need to use a third-party token server.</span></span>

<span data-ttu-id="0077d-123">Lync Server 2013 unterstützt die beiden Server-zu-Server-Authentifizierungsszenarien.</span><span class="sxs-lookup"><span data-stu-id="0077d-123">Lync Server 2013 supports the two server-to-server authentication scenarios.</span></span> <span data-ttu-id="0077d-124">Dazu gehören die Konfiguration der Server-zu-Server-Authentifizierung zwischen den folgenden:</span><span class="sxs-lookup"><span data-stu-id="0077d-124">These include configuration of server-to-server authentication between the following:</span></span>

  - <span data-ttu-id="0077d-125">Eine lokale Installation von lync Server 2013 und eine lokale Installation von Exchange Server 2013, Exchange Server 2016 und/oder SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="0077d-125">An on-premise installation of Lync Server 2013 and an on-premises installation of Exchange Server 2013, Exchange Server 2016, and/or SharePoint Server.</span></span>

  - <span data-ttu-id="0077d-126">Ein paar von Office-Komponenten (beispielsweise zwischen Microsoft Exchange 365 und Microsoft lync Server 365 oder zwischen Microsoft lync Server 365 und Microsoft SharePoint 365).</span><span class="sxs-lookup"><span data-stu-id="0077d-126">A pair of Office components (for example, between Microsoft Exchange 365 and Microsoft Lync Server 365, or between Microsoft Lync Server 365 and Microsoft SharePoint 365).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0077d-127">Die Server-zu-Server-Authentifizierung zwischen einem lokalen Server und einer Microsoft 365-oder Office 365-Komponente wird in dieser Version von lync Server 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0077d-127">Server-to-server authentication between an on-premises server and a Microsoft 365 or Office 365 component is not supported in this Lync Server 2013 release.</span></span> <span data-ttu-id="0077d-128">Dies bedeutet unter anderem, dass Sie keine Server-zu-Server-Authentifizierung zwischen einer lokalen Installation von lync Server 2013 und Microsoft Exchange 365 einrichten können.</span><span class="sxs-lookup"><span data-stu-id="0077d-128">Among other things, this means that you cannot set up server-to-server authentication between an on-premises installation of Lync Server 2013 and Microsoft Exchange 365.</span></span>



</div>

<span data-ttu-id="0077d-129">Ausführliche Informationen zur Server-zu-Server-Authentifizierung finden Sie unter [Verwalten von Server-zu-Server-Authentifizierung (OAuth) und Partneranwendungen in lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in der Bereitstellungsdokumentation oder in der Dokumentation zur Betriebsanleitung.</span><span class="sxs-lookup"><span data-stu-id="0077d-129">For details about server-to-server authentication, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or Operations documentation.</span></span>

<span data-ttu-id="0077d-130"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0077d-130"></div>

<span> </span>

</div>

</div>

</span></span></div>
