---
title: 'Lync Server 2013: Konferenzrichtlinien'
description: 'Lync Server 2013: Konferenzrichtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing policies
ms:assetid: 8f92eb7c-ee66-4df6-a726-4bff93b122cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688133(v=OCS.15)
ms:contentKeyID: 49733732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6f117cfb077fc24c3e728e208d8bef78cd3284ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434312"
---
# <a name="conferencing-policies-in-lync-server-2013"></a><span data-ttu-id="055e5-103">Konferenzrichtlinien in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="055e5-103">Conferencing policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="055e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="055e5-104">

<span> </span></span></span>

<span data-ttu-id="055e5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="055e5-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="055e5-106">Konferenzrichtlinie definiert die Features und Funktionen, die Benutzer während einer Konferenz (auch als Besprechung bezeichnet) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="055e5-106">Conferencing policy defines the features and capabilities that users have available during a conference (also known as a meeting).</span></span> <span data-ttu-id="055e5-107">Konferenzrichtlinieneinstellungen umfassen eine breite Auswahl an Planungs- und Teilnahmeoptionen, von der Verwendung von IP-Audio und -Video in einer Besprechung bis hin zur Höchstzahl der möglichen Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="055e5-107">Conferencing policy settings encompass a wide variety of scheduling and participation options, ranging from whether a meeting can include IP audio and video to the maximum number of people who can attend.</span></span> <span data-ttu-id="055e5-108">Administratoren können Konferenzrichtlinien verwenden, um Sicherheit, Bandbreite und rechtliche Aspekte von Besprechungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="055e5-108">Administrators can use conferencing policy to manage security, bandwidth, and legal aspects of meetings.</span></span>

<span data-ttu-id="055e5-109">Die Konferenzrichtlinie kann auf drei Ebenen definiert werden: auf globaler, auf Standort- und auf Benutzerebene.</span><span class="sxs-lookup"><span data-stu-id="055e5-109">You can define conferencing policy on three levels: global scope, site scope, and user scope.</span></span> <span data-ttu-id="055e5-110">Die Einstellungen gelten für einen bestimmten Benutzer vom engsten bis hin zum weitesten Bereich.</span><span class="sxs-lookup"><span data-stu-id="055e5-110">Settings apply to a specific user from the narrowest scope to the widest scope.</span></span> <span data-ttu-id="055e5-111">Wenn Sie einem Benutzer eine Benutzerrichtlinie zuweisen, haben diese Einstellungen Vorrang.</span><span class="sxs-lookup"><span data-stu-id="055e5-111">If you assign a user policy to a user, those settings take precedence.</span></span> <span data-ttu-id="055e5-112">Wenn Sie keine Benutzerrichtlinie zuweisen, gelten die Standorteinstellungen.</span><span class="sxs-lookup"><span data-stu-id="055e5-112">If you do not assign a user policy, site settings apply.</span></span> <span data-ttu-id="055e5-113">Gelten weder Benutzer- noch Standortrichtlinien, stellt die globale Richtlinie die Standardeinstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="055e5-113">If no user or site policies apply, global policy provides the default settings.</span></span>

<span data-ttu-id="055e5-114">Eine globale Richtlinie ist standardmäßig vorhanden, sodass Sie keine neue globale Richtlinie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="055e5-114">A global policy exists by default, so you cannot create a new global policy.</span></span> <span data-ttu-id="055e5-115">Sie können auch die vorhandene globale Richtlinie nicht löschen, aber Sie können die vorhandene globale Richtlinie so ändern, dass die Standardeinstellungen angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="055e5-115">You also cannot delete the existing global policy, but you can change the existing global policy to customize your default settings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="055e5-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="055e5-116">In This Section</span></span>

  - [<span data-ttu-id="055e5-117">Anzeigen von Konferenzrichtlinien Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="055e5-117">View conferencing policy information in Lync Server 2013</span></span>](lync-server-2013-view-conferencing-policy-information.md)

  - [<span data-ttu-id="055e5-118">Erstellen oder Ändern einer konferenzrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="055e5-118">Create or modify a conferencing policy in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-conferencing-policy.md)

  - [<span data-ttu-id="055e5-119">Löschen einer vorhandenen konferenzrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="055e5-119">Delete an existing conferencing policy in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-conferencing-policy.md)

  - [<span data-ttu-id="055e5-120">Referenz für konferenzrichtlinieneinstellungen für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="055e5-120">Conferencing policy settings reference for Lync Server 2013</span></span>](lync-server-2013-conferencing-policy-settings-reference.md)

<span data-ttu-id="055e5-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="055e5-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

