---
title: 'Lync Server 2013: Audio/Video (A/V)-Edgeserver'
description: 'Lync Server 2013: Audio/Video-Edgeserver (A/V).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Audio/Video (A/V) Edge Servers
ms:assetid: b0cc538b-77eb-47fb-be82-5ab0631c6219
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721852(v=OCS.15)
ms:contentKeyID: 49733785
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d5aefd4516540485b84ba0eb80f1a809d89eba0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438239"
---
# <a name="audiovideo-av-edge-servers-in-lync-server-2013"></a><span data-ttu-id="66e50-103">Audio/Video-Edgeserver (A/V) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66e50-103">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="66e50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="66e50-104">

<span> </span></span></span>

<span data-ttu-id="66e50-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="66e50-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="66e50-106">Der a/V-Edgedienst bietet internen Benutzern (Benutzern, die bei Ihrem Unternehmensnetzwerk angemeldet sind) die Möglichkeit, Audio und Video für externe Benutzer freizugeben (Benutzer, die nicht bei Ihrem Organisationsnetzwerk angemeldet sind).</span><span class="sxs-lookup"><span data-stu-id="66e50-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="66e50-107">Neben Audio und Video bietet der A/V-Edgedienst auch Unterstützung für die Desktopfreigabe und Dateiübertragung.</span><span class="sxs-lookup"><span data-stu-id="66e50-107">In addition to audio and video, the A/V Edge service also provides support for such things desktop sharing and file transfer.</span></span>

<span data-ttu-id="66e50-108">Der a/v-Edgedienst wird hauptsächlich mithilfe der a/v-Edge-Konfiguration verwaltet. Mithilfe dieser Einstellungen können Sie die maximale Bandbreite verwalten, die pro Port und pro Benutzer zugewiesen werden soll, und angeben, wie lange ein Authentifizierungstoken verwendet werden kann, bevor dieses Token erneuert werden muss.</span><span class="sxs-lookup"><span data-stu-id="66e50-108">The A/V Edge service is primarily managed by using A/V Edge configuration; these settings enable you to manage the maximum amount of bandwidth to be allocated per port and per user, and to specify the length of time that an authentication token can be used before that token must be renewed.</span></span> <span data-ttu-id="66e50-109">A/v-Edge-Konfigurationseinstellungen können auf Websites oder auf einzelne a/v-Edgeserver angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="66e50-109">A/V Edge configuration settings can be applied to sites or to individual A/V Edge servers.</span></span> <span data-ttu-id="66e50-110">Verwenden Sie die folgende Anleitung, um zu ermitteln, welche Sammlung von Einstellungen Vorrang hat:</span><span class="sxs-lookup"><span data-stu-id="66e50-110">When determining which collection of settings will take priority, use the following guide:</span></span>

  - <span data-ttu-id="66e50-111">Im Dienstbereich konfigurierte Einstellungen (also auf einem einzelnen Server) haben Vorrang vor allem.</span><span class="sxs-lookup"><span data-stu-id="66e50-111">Settings configured at the service scope (that is, on an individual server) take priority over everything.</span></span>

  - <span data-ttu-id="66e50-112">Die für den Website Bereich konfigurierten Einstellungen haben Vorrang vor den im globalen Bereich konfigurierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="66e50-112">Settings configured at the site scope take priority over settings configured at the global scope.</span></span> <span data-ttu-id="66e50-113">Dienstbereichs Einstellungen ersetzen jedoch auch die Einstellungen für den Website Bereich.</span><span class="sxs-lookup"><span data-stu-id="66e50-113">However, service scope settings will also supersede site-scope settings.</span></span>

  - <span data-ttu-id="66e50-114">Einstellungen im globalen Bereich werden nur verwendet, wenn auf dem einzelnen Server keine Diensteinstellungen konfiguriert sind und keine Websiteeinstellungen für die Website vorhanden sind, auf der sich der Server befindet.</span><span class="sxs-lookup"><span data-stu-id="66e50-114">Settings at the global scope will be used only if there are no service settings configured on the individual server and if there are no site settings for the site where that server is located.</span></span>

<span data-ttu-id="66e50-115">Der A/V-Edgedienst kann nur mithilfe der lync Server PowerShell und der CsAVEdgeConfiguration-Cmdlets verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="66e50-115">The A/V Edge service can only be managed by using Lync Server PowerShell and the CsAVEdgeConfiguration cmdlets.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="66e50-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="66e50-116">In This Section</span></span>

  - [<span data-ttu-id="66e50-117">Zurückgeben von A/V-Edgeserver-Konfigurationsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66e50-117">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)

  - [<span data-ttu-id="66e50-118">Erstellen oder Ändern einer Sammlung von a/V-Edgeserver-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66e50-118">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-a-v-edge-server-configuration-settings.md)

  - [<span data-ttu-id="66e50-119">Löschen einer vorhandenen Sammlung von A/V-Edgeserver-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="66e50-119">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)

<span data-ttu-id="66e50-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="66e50-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

