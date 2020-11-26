---
title: Verwalten von Add-Ins
description: Verwalten von Add-Ins.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage add-ins
ms:assetid: b84f868e-b36e-4ab4-b284-7db212d401c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205193(v=OCS.15)
ms:contentKeyID: 48185204
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2f381e73d8da33e1347ccc81e7b0d98270827d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446969"
---
# <a name="manage-add-ins"></a><span data-ttu-id="ee056-103">Verwalten von Add-Ins</span><span class="sxs-lookup"><span data-stu-id="ee056-103">Manage add-ins</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ee056-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ee056-104">

<span> </span></span></span>

<span data-ttu-id="ee056-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="ee056-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="ee056-106">So erstellen Sie ein neues Add-in für beständigen Chat Server</span><span class="sxs-lookup"><span data-stu-id="ee056-106">To create a new Persistent Chat Server Add-in</span></span>

    New-CsPersistentChatAddin -Name Contoso -PersistentChatPoolFqdn client.contoso.com -Url http://contoso.com 

<div>

## <a name="create-get-set-or-remove-an-add-in"></a><span data-ttu-id="ee056-107">Erstellen, abrufen, einrichten oder Entfernen eines Add-ins</span><span class="sxs-lookup"><span data-stu-id="ee056-107">Create, Get, Set, or Remove an Add-in</span></span>

<span data-ttu-id="ee056-108">So erstellen Sie ein neues Add-in</span><span class="sxs-lookup"><span data-stu-id="ee056-108">To create a new Add-in</span></span>

    New-CsPersistentChatAddin -PersistentChatPoolFqdn <String> -Name <String> -Url<String>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ee056-109">PersistentChatPoolFqdn &lt; -Zeichenfolge &gt; ist nur erforderlich, wenn mehr als ein beständiger Chat Server Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ee056-109">PersistentChatPoolFqdn &lt;String&gt; is required only if there is more than one Persistent Chat Server pool.</span></span>



</div>

<span data-ttu-id="ee056-110">So erhalten Sie ein Add-in</span><span class="sxs-lookup"><span data-stu-id="ee056-110">To get an Add-in</span></span>

    Get-CsPersistentChatAddin -Identity <String>]

<span data-ttu-id="ee056-111">oder</span><span class="sxs-lookup"><span data-stu-id="ee056-111">or</span></span>

    Get-CsPersistentChatAddin -PersistentChatPoolFqdn <String>

<span data-ttu-id="ee056-112">So setzen Sie ein Add-in</span><span class="sxs-lookup"><span data-stu-id="ee056-112">To set an Add-in</span></span>

    Set-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="ee056-113">oder</span><span class="sxs-lookup"><span data-stu-id="ee056-113">or</span></span>

    Set-CsPersistentChatAddIn -Identity <String> [-Name <String>] [-Url<String>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="ee056-114">So entfernen Sie ein Add-in</span><span class="sxs-lookup"><span data-stu-id="ee056-114">To remove an Add-in</span></span>

    Remove-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="ee056-115">oder</span><span class="sxs-lookup"><span data-stu-id="ee056-115">or</span></span>

    Remove-CsPersistentChatAddIn -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="ee056-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ee056-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

