---
title: 'Lync Server 2013: Unterstützung für Exchange Unified Messaging (UM)'
description: 'Lync Server 2013: Exchange Unified Messaging (um)-Unterstützung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Exchange Unified Messaging (UM) support
ms:assetid: 0da62b8d-7416-4fb8-a405-381ca805c53a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398179(v=OCS.15)
ms:contentKeyID: 48183405
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 563517bb72167bbab0b08eba3b1359ae3ab52836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395018"
---
# <a name="exchange-unified-messaging-um-support-in-lync-server-2013"></a><span data-ttu-id="64bb1-103">Unterstützung für Exchange Unified Messaging (UM) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64bb1-103">Exchange Unified Messaging (UM) support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64bb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64bb1-104">

<span> </span></span></span>

<span data-ttu-id="64bb1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="64bb1-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="64bb1-106">Lync Server 2013 unterstützt die Integration in Exchange Unified Messaging (um) zum Kombinieren von Voicemail und e-Mail-Messaging in einer einzelnen Messaginginfrastruktur.</span><span class="sxs-lookup"><span data-stu-id="64bb1-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="64bb1-107">In Exchange 2013 besteht Exchange um aus dem Exchange um-Dienst, der auf dem Postfachserver installiert ist und ausgeführt wird, und dem um-Anruf Router, der auf dem Client Zugriffsserver installiert ist und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64bb1-107">In Exchange 2013, Exchange UM consists of the Exchange UM service, which is installed and runs on the Mailbox server, and the UM Call Router, which is installed and runs on the Client Access server.</span></span> <span data-ttu-id="64bb1-108">Bei lync Server 2013 Enterprise-VoIP-Bereitstellungen kombiniert Exchange um Sprachnachrichten und e-Mail-Nachrichten in einem einzigen Speicher, auf den von einem Telefon (also Outlook Voice Access) oder einem Computer aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="64bb1-108">For Lync Server 2013 Enterprise Voice deployments, Exchange UM combines voice messaging and email messaging into a single store that is accessible from a telephone (that is, Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="64bb1-109">Exchange um-und lync Server 2013 arbeiten zusammen, um Benutzern von Enterprise-VoIP die Anrufannahme, Outlook Voice Access und automatische Telefonzentralendienste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="64bb1-109">Exchange UM and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="64bb1-110">Neben der Unterstützung für die Integration in lokale Bereitstellungen von Exchange um unterstützt lync Server 2013 die Integration in gehostete Exchange um.</span><span class="sxs-lookup"><span data-stu-id="64bb1-110">In addition to the support for integration with on-premises deployments of Exchange UM, Lync Server 2013 supports integration with hosted Exchange UM.</span></span> <span data-ttu-id="64bb1-111">Auf diese Weise können Sie Ihren Benutzern Sprachnachrichten senden, wenn Sie einige oder alle von Ihnen zu einem gehosteten Exchange-Dienstanbieter wie Microsoft Exchange Online migrieren.</span><span class="sxs-lookup"><span data-stu-id="64bb1-111">This enables you to provide voice messaging to your users if you migrate some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="64bb1-112">Lync Server 2013 unterstützt die folgenden Versionen:</span><span class="sxs-lookup"><span data-stu-id="64bb1-112">Lync Server 2013 supports the following versions:</span></span>

  - <span data-ttu-id="64bb1-113">Microsoft Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="64bb1-113">Microsoft Exchange 2013</span></span>

  - <span data-ttu-id="64bb1-114">Microsoft Exchange Server 2010 (erforderlich) oder mit dem neuesten Service Pack (empfohlen)</span><span class="sxs-lookup"><span data-stu-id="64bb1-114">Microsoft Exchange Server 2010 (required) or with latest service pack (recommended)</span></span>

  - <span data-ttu-id="64bb1-115">Microsoft Exchange Server 2007 mit Service Pack 1 (SP1) (erforderlich) oder neuestes Service Pack (empfohlen)</span><span class="sxs-lookup"><span data-stu-id="64bb1-115">Microsoft Exchange Server 2007 with Service Pack 1 (SP1) (required) or latest service pack (recommended)</span></span>

<span data-ttu-id="64bb1-116">Sie können Exchange um nicht mit lync Server 2013 oder einer lync Server 2013-Datenbank collocate.</span><span class="sxs-lookup"><span data-stu-id="64bb1-116">You cannot collocate Exchange UM with Lync Server 2013 or a Lync Server 2013 database.</span></span> <span data-ttu-id="64bb1-117">Sie können Exchange um-und lync Server 2013 in getrennten Gesamtstrukturen installieren.</span><span class="sxs-lookup"><span data-stu-id="64bb1-117">You can install Exchange UM and Lync Server 2013 in separate forests.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="64bb1-118">Exchange um ist möglicherweise für Enterprise-VoIP-Bereitstellungen, für die eine Telefonanlage bereitgestellt wurde, nicht erforderlich, da die Telefonanlage weiterhin Voicemail und verwandte Dienste für alle Benutzer bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="64bb1-118">Exchange UM may not be required for Enterprise Voice deployments that have a PBX deployed, because the PBX can continue to provide voice mail and related services to all users.</span></span> <span data-ttu-id="64bb1-119">Wenn Sie die Telefonanlage schließlich zurückziehen (wenn Sie beispielsweise SIP-Trunking für PSTN-Konnektivität (Public Switched Telephone Network) bereitstellen), müssen Sie Exchange um für die Bereitstellung von Voicemail für Benutzer neu konfigurieren, die zuvor das Telefonanlagen-Voicemailsystem verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="64bb1-119">If you eventually retire the PBX (for example, if you deploy SIP trunking for public switched telephone network (PSTN) connectivity), you must reconfigure Exchange UM to provide voice mail to users who previously used the PBX voice mail system.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="64bb1-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="64bb1-120">In This Section</span></span>

  - [<span data-ttu-id="64bb1-121">Komponenten und Topologien für lokales Unified Messaging in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64bb1-121">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="64bb1-122">Unterstützung für die Integration gehosteter Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64bb1-122">Support for hosted Exchange UM integration in Lync Server 2013</span></span>](lync-server-2013-support-for-hosted-exchange-um-integration.md)

<span data-ttu-id="64bb1-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64bb1-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

