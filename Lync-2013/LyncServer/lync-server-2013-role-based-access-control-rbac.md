---
title: 'Lync Server 2013: rollenbasierte Zugriffssteuerung (RBAC)'
description: 'Lync Server 2013: rollenbasierte Zugriffssteuerung (RBAC).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Role-based access control (RBAC) for Lync Server 2013
ms:assetid: d01fba36-eb7e-4de9-9bba-5102ae157820
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn481134(v=OCS.15)
ms:contentKeyID: 59893872
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6586517083ff6cd2c4e20d83e9b8f861edf800c0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442345"
---
# <a name="role-based-access-control-rbac-for-lync-server-2013"></a><span data-ttu-id="b092f-103">Rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC) für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b092f-103">Role-based access control (RBAC) for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b092f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b092f-104">

<span> </span></span></span>

<span data-ttu-id="b092f-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="b092f-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="b092f-106">Microsoft lync Server 2013 enthält Role-Based Zugriffssteuerungsgruppen, mit denen Sie Verwaltungsaufgaben delegieren und gleichzeitig hohe Sicherheitsstandards gewährleisten können.</span><span class="sxs-lookup"><span data-stu-id="b092f-106">Microsoft Lync Server 2013 includes Role-Based Access Control (RBAC) groups to enable you to delegate administrative tasks while maintaining high standards for security.</span></span> <span data-ttu-id="b092f-107">Diese Gruppen werden während der Gesamtstrukturvorbereitung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b092f-107">These groups are created during forest preparation.</span></span> <span data-ttu-id="b092f-108">Details zur Vorbereitung der Gesamtstruktur finden Sie unter [Active Directory-Domänendienste für lync Server 2013](lync-server-2013-active-directory-domain-services-for-lync-server.md).</span><span class="sxs-lookup"><span data-stu-id="b092f-108">For details about forest preparation, see [Active Directory Domain Services for Lync Server 2013](lync-server-2013-active-directory-domain-services-for-lync-server.md).</span></span> <span data-ttu-id="b092f-109">Details zu den von der Gesamtstrukturvorbereitung erstellten Gruppen finden Sie unter Änderungen, die [von der Gesamtstrukturvorbereitung in lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md) in der Bereitstellungsdokumentation vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="b092f-109">For details about the specific groups created by forest preparation, see [Changes made by forest preparation in Lync Server 2013](lync-server-2013-changes-made-by-forest-preparation.md) in the Deployment documentation.</span></span>

<span data-ttu-id="b092f-110">Mit RBAC wird das administrative Recht gewährt, indem Nutzer vordefinierten administrativen Rollen zugewiesen werden, einschließlich der elf vordefinierten Rollen, die viele häufig verwendete administrative Aufgaben abdecken.</span><span class="sxs-lookup"><span data-stu-id="b092f-110">With RBAC, administrative privilege is granted by assigning users to pre-defined administrative roles, including the 11 predefined roles that cover many common administrative tasks.</span></span> <span data-ttu-id="b092f-111">Jede Rolle ist einer bestimmten Liste der lync Server-Verwaltungsshell-Cmdlets zugeordnet, die Benutzer in dieser Rolle ausführen dürfen.</span><span class="sxs-lookup"><span data-stu-id="b092f-111">Each role is associated with a specific list of Lync Server Management Shell cmdlets that users in that role are allowed to run.</span></span> <span data-ttu-id="b092f-112">Mit der rollenbasierten Zugriffssteuerung können Sie dem Prinzip der geringsten Rechte folgen, bei dem Nutzer nur die administrativen Funktionen erhalten, die sie für ihre Arbeit benötigen.</span><span class="sxs-lookup"><span data-stu-id="b092f-112">You can use RBAC to follow the principle of "least privilege," in which users are given only the administrative abilities that their jobs require.</span></span> <span data-ttu-id="b092f-113">Ausführliche Informationen finden Sie unter [Planen der rollenbasierten Zugriffssteuerung in lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b092f-113">For details, see [Planning for role-based access control in Lync Server 2013](lync-server-2013-planning-for-role-based-access-control.md) in the Planning documentation.</span></span>

<span data-ttu-id="b092f-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b092f-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

