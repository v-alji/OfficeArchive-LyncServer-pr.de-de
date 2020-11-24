---
title: 'Lync Server 2013: Cmdlets für Benutzerrechte und Berechtigungen'
description: 'Lync Server 2013: Cmdlets für Benutzerrechte und Berechtigungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User rights and permissions cmdlets
ms:assetid: b53aae4c-651f-4cbc-a762-ba818d63897e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415672(v=OCS.15)
ms:contentKeyID: 48185178
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec14442e6cdd5c398da9e9291109d8ba128dbd9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394298"
---
# <a name="user-rights-and-permissions-cmdlets-in-lync-server-2013"></a><span data-ttu-id="78462-103">Cmdlets für Benutzerrechte und Berechtigungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78462-103">User rights and permissions cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78462-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78462-104">

<span> </span></span></span>

<span data-ttu-id="78462-105">_**Letztes Änderungsdatum des Themas:** 2012-06-26_</span><span class="sxs-lookup"><span data-stu-id="78462-105">_**Topic Last Modified:** 2012-06-26_</span></span>

<span data-ttu-id="78462-106">Die Cmdlets für Benutzerberechtigungen werden in erster Linie zum Verwalten der rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC), der neuen Technologie zum Delegieren der administrativen Steuerung von Microsoft lync Server 2013, verwendet.</span><span class="sxs-lookup"><span data-stu-id="78462-106">The user permission cmdlets are primarily used to manage role-based access control (RBAC), the new technology for delegating administrative control of Microsoft Lync Server 2013.</span></span>

<div>

## <a name="user-permission-cmdlets"></a><span data-ttu-id="78462-107">Cmdlets für Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="78462-107">User Permission Cmdlets</span></span>

<span data-ttu-id="78462-108">Die folgende Liste enthält Cmdlets, die sich direkt auf die Verwaltung von Benutzerberechtigungen beziehen:</span><span class="sxs-lookup"><span data-stu-id="78462-108">The following is a list of cmdlets that relate directly to managing user permissions:</span></span>

<span data-ttu-id="78462-109">**Benutzerberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="78462-109">**User Permissions**</span></span>

  - <span></span>  
    <span data-ttu-id="78462-110">[Get-CsAdminRole](https://technet.microsoft.com/library/Gg399050(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-110">[Get-CsAdminRole](https://technet.microsoft.com/library/Gg399050(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-111">[Neu – CsAdminRole](https://technet.microsoft.com/library/Gg398271(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-111">[New-CsAdminRole](https://technet.microsoft.com/library/Gg398271(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-112">[Remove-CsAdminRole](https://technet.microsoft.com/library/Gg413036(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-112">[Remove-CsAdminRole](https://technet.microsoft.com/library/Gg413036(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-113">[Satz-CsAdminRole](https://technet.microsoft.com/library/Gg399066(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-113">[Set-CsAdminRole](https://technet.microsoft.com/library/Gg399066(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-114">[Update-CsAdminRole](https://technet.microsoft.com/library/JJ204851(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-114">[Update-CsAdminRole](https://technet.microsoft.com/library/JJ204851(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="78462-115">[Get-CsAdminRoleAssignment](https://technet.microsoft.com/library/Gg398434(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-115">[Get-CsAdminRoleAssignment](https://technet.microsoft.com/library/Gg398434(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="78462-116">[Grant-CsOUPermission](https://technet.microsoft.com/library/Gg425739(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-116">[Grant-CsOUPermission](https://technet.microsoft.com/library/Gg425739(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-117">[REVOKE-CsOUPermission](https://technet.microsoft.com/library/Gg398977(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-117">[Revoke-CsOUPermission](https://technet.microsoft.com/library/Gg398977(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-118">[Test-CsOUPermission](https://technet.microsoft.com/library/Gg398787(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-118">[Test-CsOUPermission](https://technet.microsoft.com/library/Gg398787(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="78462-119">[Grant-CsSetupPermission](https://technet.microsoft.com/library/Gg398569(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-119">[Grant-CsSetupPermission](https://technet.microsoft.com/library/Gg398569(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-120">[REVOKE-CsSetupPermission](https://technet.microsoft.com/library/Gg425834(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-120">[Revoke-CsSetupPermission](https://technet.microsoft.com/library/Gg425834(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="78462-121">[Test-CsSetupPermission](https://technet.microsoft.com/library/Gg398428(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="78462-121">[Test-CsSetupPermission](https://technet.microsoft.com/library/Gg398428(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="78462-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78462-122">See Also</span></span>


[<span data-ttu-id="78462-123">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="78462-123">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="78462-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78462-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

