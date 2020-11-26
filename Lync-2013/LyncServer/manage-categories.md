---
title: Verwalten von Kategorien
description: Verwalten von Kategorien
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Manage categories
ms:assetid: 1b118d91-b4c4-4b2f-b842-b451417ec2c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204719(v=OCS.15)
ms:contentKeyID: 48183543
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf335b96c455647ebeb665364944e15d2e463fbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446962"
---
# <a name="manage-categories"></a><span data-ttu-id="3815c-103">Manage categories</span><span class="sxs-lookup"><span data-stu-id="3815c-103">Manage categories</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3815c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3815c-104">

<span> </span></span></span>

<span data-ttu-id="3815c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="3815c-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="3815c-106">So erstellen Sie eine neue Kategorie für beständigen Chat Server</span><span class="sxs-lookup"><span data-stu-id="3815c-106">To create a new Persistent Chat Server Category</span></span>

    New-CsPersistentChatCategory -Name Foo -PersistentChatPoolFqdn client.contoso1b118d91-b4c4-4b2f-b842-b451417ec2c6.com [other parameters]

<div>


> [!IMPORTANT]  
> <span data-ttu-id="3815c-107">PersistentChatPoolFqdn ist nur erforderlich, wenn mehr als ein beständiger Chat Server Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3815c-107">PersistentChatPoolFqdn is needed only if there is more than one Persistent Chat Server pool.</span></span>



</div>

<span data-ttu-id="3815c-108">So nehmen Sie Änderungen an der vorhandenen beständigen Chat Server Kategorie vor</span><span class="sxs-lookup"><span data-stu-id="3815c-108">To make changes to existing Persistent Chat Server Category</span></span>

    Set-CsPersistentChatCategory -Identity testCat -AllowedMembers @{Add="sip:user1@contoso.com", "CN=container,DC=contoso,DC=com"}  -DeniedMembers @{Add="sip:user2@contoso.com"}
    Set-CsPersistentChatCategory -Identity testCat -Creators @{Add="sip:user1@contoso.com"}

<span data-ttu-id="3815c-109">Windows PowerShell: AllowedMembers, DeniedMembers und Creators können gleichzeitig eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3815c-109">Windows PowerShell: AllowedMembers, DeniedMembers, and Creators can be set simultaneously.</span></span> <span data-ttu-id="3815c-110">Ersteller sollten die Teilmenge von AllowedMembers minus DeniedMembers sein.</span><span class="sxs-lookup"><span data-stu-id="3815c-110">Creators should be the subset of AllowedMembers minus DeniedMembers.</span></span> <span data-ttu-id="3815c-111">Sie können auch die Eigenschaften einer Kategorie zur gleichen Zeit wie die Mitglieder und Ersteller einstellen.</span><span class="sxs-lookup"><span data-stu-id="3815c-111">You can also set the properties of a category at the same time as the members and creators.</span></span>

<div>

## <a name="create-get-set-or-remove-a-category"></a><span data-ttu-id="3815c-112">Erstellen, abrufen, einrichten oder Entfernen einer Kategorie</span><span class="sxs-lookup"><span data-stu-id="3815c-112">Create, Get, Set, or Remove a Category</span></span>

<span data-ttu-id="3815c-113">So erstellen Sie eine neue Kategorie</span><span class="sxs-lookup"><span data-stu-id="3815c-113">To create a new Category</span></span>

    New-CsPersistentChatCategory -Name <String> [-PersistentChatPoolFqdn <String>] [-Description <String>] [-EnableInvitations<Switch Parameter>] [-EnableFileUpload <Switch Parameter>] [-RemoveChatHistory <Switch Parameter>] [-MaxContentSize <Integer>]

<span data-ttu-id="3815c-114">So erhalten Sie eine Kategorie</span><span class="sxs-lookup"><span data-stu-id="3815c-114">To get a Category</span></span>

    Get-CsPersistentChatCategory -Identity <String>

<span data-ttu-id="3815c-115">oder</span><span class="sxs-lookup"><span data-stu-id="3815c-115">or</span></span>

    Get-CsPersistentChatCategory -PersistentChatPoolFqdn <String>

<span data-ttu-id="3815c-116">So setzen Sie eine Kategorie</span><span class="sxs-lookup"><span data-stu-id="3815c-116">To set a Category</span></span>

    Set-CsPersistentChatCategory -Instance <CategoryObject> [-WhatIf] [-Confirm] [<CommonParameters>]

<span data-ttu-id="3815c-117">oder</span><span class="sxs-lookup"><span data-stu-id="3815c-117">or</span></span>

    Set-CsPersistentChatCategory [-Identity] <string> [-Name <string>] [-Description <string>] [-Invitations <bool>] [-FileUpload <bool>] [-ChatHistory <bool>] [-AllowedMembers <PSListModifier[string]>] [-DeniedMembers <PSListModifier[string]>] [-Creators <PSListModifier[string]>] [-WhatIf] [-Confirm]  [<CommonParameters>]

<span data-ttu-id="3815c-118">So entfernen Sie eine Kategorie</span><span class="sxs-lookup"><span data-stu-id="3815c-118">To remove a Category</span></span>

    Remove-CsPersistentChatCategory -Instance <CategoryObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="3815c-119">oder</span><span class="sxs-lookup"><span data-stu-id="3815c-119">or</span></span>

    Remove-CsPersistentChatCategory -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

<span data-ttu-id="3815c-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3815c-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

