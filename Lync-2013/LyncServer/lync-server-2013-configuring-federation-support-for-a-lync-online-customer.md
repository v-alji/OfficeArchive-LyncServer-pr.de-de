---
title: 'Lync Server 2013: Konfigurieren der Verbundunterstützung für einen lync Online-Kunden'
description: 'Lync Server 2013: Konfigurieren der Föderations Unterstützung für einen lync Online-Kunden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring federation support for a Lync Online customer
ms:assetid: e5f7f38d-ede5-4af3-88c2-026e8a78df12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202193(v=OCS.15)
ms:contentKeyID: 48185669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b5e7995e686a9492b3a4be98a92b848716cacf9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433115"
---
# <a name="configuring-federation-support-for-a-lync-online-customer-in-lync-server-2013"></a><span data-ttu-id="cd9fc-103">Konfigurieren der Verbundunterstützung für einen lync Online-Kunden in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd9fc-103">Configuring federation support for a Lync Online customer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd9fc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd9fc-104">

<span> </span></span></span>

<span data-ttu-id="cd9fc-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="cd9fc-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="cd9fc-106">Sie können den Benutzern in Ihrer Organisation auf eine der folgenden Arten Kommunikationsdienste bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="cd9fc-106">You can provide communications services to users in your organization in any of the following ways:</span></span>

  - <span data-ttu-id="cd9fc-107">Bereitstellen von lync Server 2013 in Ihrer Organisation (als *Lokale Dienste* bezeichnet) und Einrichten von lync 2013-Benutzerkonten in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="cd9fc-107">Deploying Lync Server 2013 in your organization (known as *on-premises services*) and setting up Lync 2013 user accounts in your organization.</span></span>

  - <span data-ttu-id="cd9fc-108">Einrichten eines Microsoft lync Online 2010-Kundenkontos bei einem Hostinganbieter und Einrichten von Benutzerkonten beim Hostinganbieter (so genannte *Online Dienste*).</span><span class="sxs-lookup"><span data-stu-id="cd9fc-108">Setting up a Microsoft Lync Online 2010 customer account with a Hosting Provider and setting up user accounts with the Hosting Provider (known as *online services*).</span></span>

<span data-ttu-id="cd9fc-109">Wenn Sie lync 2013 in Ihrer Organisation bereitstellen, können Sie sich mit den Domänen eines oder mehrerer Microsoft lync Online 2010-Kunden vereinigen.</span><span class="sxs-lookup"><span data-stu-id="cd9fc-109">If you deploy Lync 2013 in your organization, you can federate with the domains of one or more Microsoft Lync Online 2010 customers.</span></span> <span data-ttu-id="cd9fc-110">Um die Föderation zwischen Benutzern Ihrer lokalen lync 2013-Bereitstellung und Benutzern eines lync Online 2010-Kunden zu aktivieren, müssen Sie die Unterstützung für die Domäne und die Benutzer des lync Online-Kunden konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cd9fc-110">To enable federation between users of your on-premises Lync 2013 deployment and users of a Lync Online 2010 customer, you must configure support for the domain and users of the Lync Online customer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cd9fc-111">In dieser Dokumentation werden nur die Verfahren zum Konfigurieren Ihrer Organisation zur Unterstützung der Föderation mit einem lync Online 2010-Kunden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd9fc-111">This documentation describes only the procedures for configuring your organization to support federation with an Lync Online 2010 customer.</span></span> <span data-ttu-id="cd9fc-112">In dieser Dokumentation werden die Verfahren zum Konfigurieren des lync Online 2010-Kunden zur Unterstützung von Föderationen nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd9fc-112">This documentation does not describe the procedures for configuring the Lync Online 2010 customer to support federation.</span></span> <span data-ttu-id="cd9fc-113">Details zu lync Online Services finden Sie unter lync online unter <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A> .</span><span class="sxs-lookup"><span data-stu-id="cd9fc-113">For details about Lync Online services, see Lync Online at <A href="https://go.microsoft.com/fwlink/p/?linkid=218941">https://go.microsoft.com/fwlink/p/?linkId=218941</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cd9fc-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cd9fc-114">In This Section</span></span>

  - [<span data-ttu-id="cd9fc-115">Voraussetzungen für die Föderation mit einem lync Online-Kunden in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd9fc-115">Prerequisites for federating with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md)

  - [<span data-ttu-id="cd9fc-116">Konfigurieren der Verbundunterstützung für eine lync Online-Domäne in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd9fc-116">Configure federation support for a Lync Online domain in Lync Server 2013</span></span>](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md)

  - [<span data-ttu-id="cd9fc-117">Konfigurieren des Benutzerzugriffs für den Verbund mit einem lync Online-Kunden in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd9fc-117">Configure user access for federation with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md)

  - [<span data-ttu-id="cd9fc-118">Überprüfen der Kommunikation mit einem lync Online-Kunden in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd9fc-118">Verify communications with a Lync Online customer in Lync Server 2013</span></span>](lync-server-2013-verify-communications-with-a-lync-online-customer.md)

<span data-ttu-id="cd9fc-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd9fc-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

