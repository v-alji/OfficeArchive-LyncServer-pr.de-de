---
title: 'Lync Server 2013: Gewähren von Setupberechtigungen'
description: 'Lync Server 2013: Erteilen von Setup Berechtigungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Granting setup permissions
ms:assetid: 15982bfe-6844-44f6-815a-72dcaf0e4d21
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398225(v=OCS.15)
ms:contentKeyID: 48183491
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5523494219d07907caeefc1bd139c41856effa54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427900"
---
# <a name="granting-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="072d8-103">Gewähren von Setupberechtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="072d8-103">Granting setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="072d8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="072d8-104">

<span> </span></span></span>

<span data-ttu-id="072d8-105">_**Letztes Änderungsdatum des Themas:** 2012-08-27_</span><span class="sxs-lookup"><span data-stu-id="072d8-105">_**Topic Last Modified:** 2012-08-27_</span></span>

<span data-ttu-id="072d8-106">Sie können das Cmdlet **Grant-CsSetupPermission** verwenden, um der RTCUniversalServerAdmins-Gruppe für eine angegebene Active Directory-Organisationseinheit (OU) Lese-, Schreib-, ReadSPN-und WriteSPN-Berechtigungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="072d8-106">You can use the **Grant-CsSetupPermission** cmdlet to add Read, Write, ReadSPN, and WriteSPN permissions to the RTCUniversalServerAdmins group for a specified Active Directory organizational unit (OU).</span></span> <span data-ttu-id="072d8-107">Anschließend können Mitglieder der RTCUniversalServerAdmins-Gruppe in dieser OU Server mit lync Server 2013 in der angegebenen Domäne installieren, ohne Mitglieder der Gruppe der Domänenadministratoren zu sein.</span><span class="sxs-lookup"><span data-stu-id="072d8-107">Then members of the RTCUniversalServerAdmins group in that OU can install servers running Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="072d8-108">Verwenden Sie das Cmdlet **Test-CsSetupPermission** , um die Berechtigungen zu überprüfen, die Sie mithilfe des Cmdlets **Grant-CsSetupPermission** eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="072d8-108">Use the **Test-CsSetupPermission** cmdlet to verify the permissions you set up by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<span data-ttu-id="072d8-109">Sie können das Cmdlet **REVOKE-CsSetupPermission** verwenden, um Berechtigungen zu entfernen, die Sie mit dem Cmdlet **Grant-CsSetupPermission** erteilt haben.</span><span class="sxs-lookup"><span data-stu-id="072d8-109">You can use the **Revoke-CsSetupPermission** cmdlet to remove permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span>

<div>

## <a name="to-grant-setup-permissions"></a><span data-ttu-id="072d8-110">So erteilen Sie Setup Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="072d8-110">To grant setup permissions</span></span>

1.  <span data-ttu-id="072d8-111">Melden Sie sich bei einem Computer mit lync Server 2013 in der Domäne an, in der Sie Setup Berechtigungen erteilen möchten.</span><span class="sxs-lookup"><span data-stu-id="072d8-111">Log on to a computer running Lync Server 2013 in the domain where you want to grant setup permissions.</span></span> <span data-ttu-id="072d8-112">Verwenden Sie ein Konto, das ein Mitglied der Gruppe "Domänen-Admins" oder der Gruppe "Organisations-Admins" ist, wenn sich die Organisationseinheit in einer anderen untergeordneten Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="072d8-112">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="072d8-113">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="072d8-113">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="072d8-114">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="072d8-114">Run:</span></span>
    
        Grant-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="072d8-115">Sie können den ComputerOu-Parameter als relativ zum Standardnamenskontext der angegebenen Domäne (beispielsweise CN = Computers) angeben.</span><span class="sxs-lookup"><span data-stu-id="072d8-115">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="072d8-116">Sie können diesen Parameter auch als vollständigen Distinguished Name (DN) angeben (beispielsweise "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="072d8-116">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="072d8-117">In diesem Fall müssen Sie eine OU-DN angeben, die mit der von Ihnen angegebenen Domäne konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="072d8-117">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="072d8-118">Wenn Sie den Parameter Domain nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="072d8-118">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-verify-setup-permissions"></a><span data-ttu-id="072d8-119">So überprüfen Sie die Setup Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="072d8-119">To verify setup permissions</span></span>

1.  <span data-ttu-id="072d8-120">Melden Sie sich bei einem Computer mit lync Server 2013 in der Domäne an, in der Sie die mit dem Cmdlet **Grant-CsSetupPermission** gewährten Setup Berechtigungen überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="072d8-120">Log on to a computer running Lync Server 2013 in the domain where you want to verify setup permissions that you granted by using the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="072d8-121">Verwenden Sie ein Konto, das ein Mitglied der Gruppe "Domänen-Admins" oder der Gruppe "Organisations-Admins" ist, wenn sich die Organisationseinheit in einer anderen untergeordneten Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="072d8-121">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="072d8-122">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="072d8-122">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="072d8-123">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="072d8-123">Run:</span></span>
    
        Test-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside> [-Domain <Domain FQDN>]
    
    <span data-ttu-id="072d8-124">Sie können den ComputerOu-Parameter als relativ zum Standardnamenskontext der angegebenen Domäne (beispielsweise CN = Computers) angeben.</span><span class="sxs-lookup"><span data-stu-id="072d8-124">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="072d8-125">Sie können diesen Parameter auch als vollständigen Distinguished Name (DN) angeben (beispielsweise "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="072d8-125">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="072d8-126">In diesem Fall müssen Sie eine OU-DN angeben, die mit der von Ihnen angegebenen Domäne konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="072d8-126">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="072d8-127">Wenn Sie den Parameter Domain nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="072d8-127">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

</div>

<div>

## <a name="to-revoke-setup-permissions"></a><span data-ttu-id="072d8-128">So widerrufen Sie die Setup Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="072d8-128">To revoke setup permissions</span></span>

1.  <span data-ttu-id="072d8-129">Melden Sie sich bei einem Computer mit lync Server 2013 in der Domäne an, in der Sie die vom Cmdlet **Grant-CsSetupPermission** gewährten Setup Berechtigungen widerrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="072d8-129">Log on to a computer running Lync Server 2013 in the domain where you want to revoke setup permissions that were granted by the **Grant-CsSetupPermission** cmdlet.</span></span> <span data-ttu-id="072d8-130">Verwenden Sie ein Konto, das ein Mitglied der Gruppe "Domänen-Admins" oder der Gruppe "Organisations-Admins" ist, wenn sich die Organisationseinheit in einer anderen untergeordneten Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="072d8-130">Use an account that is a member of the Domain Admins group or the Enterprise Admins group if the OU is in a different child domain.</span></span>

2.  <span data-ttu-id="072d8-131">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="072d8-131">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="072d8-132">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="072d8-132">Run:</span></span>
    
        Revoke-CsSetupPermission -ComputerOu <DN of the OU or container where the computer objects that will run Lync Server reside > [-Domain <Domain FQDN>]
    
    <span data-ttu-id="072d8-133">Sie können den ComputerOu-Parameter als relativ zum Standardnamenskontext der angegebenen Domäne (beispielsweise CN = Computers) angeben.</span><span class="sxs-lookup"><span data-stu-id="072d8-133">You can specify the ComputerOu parameter as relative to the default naming context of the specified domain (for example, CN=computers).</span></span> <span data-ttu-id="072d8-134">Sie können diesen Parameter auch als vollständigen Distinguished Name (DN) angeben (beispielsweise "CN = Computers, DC = contoso, DC = com").</span><span class="sxs-lookup"><span data-stu-id="072d8-134">Alternatively, you can specify this parameter as the full OU distinguished name (DN) (for example, "CN=computers,DC=Contoso,DC=com").</span></span> <span data-ttu-id="072d8-135">In diesem Fall müssen Sie eine OU-DN angeben, die mit der von Ihnen angegebenen Domäne konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="072d8-135">In the latter case, you must specify an OU DN that is consistent with the domain you specify.</span></span>
    
    <span data-ttu-id="072d8-136">Wenn Sie den Parameter Domain nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="072d8-136">If you do not specify the Domain parameter, the default value is the local domain.</span></span>

<span data-ttu-id="072d8-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="072d8-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

