---
title: 'Lync Server 2013: Delegieren der administrativen Steuerung von Lync Server'
description: 'Lync Server 2013: Delegieren der administrativen Steuerung von lync Server'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegating administrative control of Lync Server 2013
ms:assetid: 0f378eff-8ef4-4c60-9fd2-67d7ee259ef8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520951(v=OCS.15)
ms:contentKeyID: 48183418
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8d3710af2d194a5aa4ebdd7291be2ee58176507
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430763"
---
# <a name="delegating-administrative-control-of-lync-server-2013"></a><span data-ttu-id="ce767-103">Delegieren der administrativen Steuerung von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ce767-103">Delegating administrative control of Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ce767-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ce767-104">

<span> </span></span></span>

<span data-ttu-id="ce767-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="ce767-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="ce767-106">In lync Server 2013 werden administrative Aufgaben mithilfe des neuen Features rollenbasierte Zugriffssteuerung (Role-Based Access Control, RBAC) an Benutzer delegiert.</span><span class="sxs-lookup"><span data-stu-id="ce767-106">In Lync Server 2013, administrative tasks are delegated to users by using the new role-based access control (RBAC) feature.</span></span> <span data-ttu-id="ce767-107">Wenn Sie lync Server installieren, werden eine Reihe von RBAC-Rollen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce767-107">When you install Lync Server, a number of RBAC roles are created for you.</span></span> <span data-ttu-id="ce767-108">Diese Rollen entsprechen den allgemeinen Sicherheitsgruppen in den Active Directory-Domänendiensten.</span><span class="sxs-lookup"><span data-stu-id="ce767-108">These roles correspond to universal security groups in Active Directory Domain Services.</span></span> <span data-ttu-id="ce767-109">Beispielsweise entspricht die RBAC-Rolle CsHelpDesk der CsHelpDesk-Gruppe, die im Container Benutzer in den Active Directory-Domänendiensten gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="ce767-109">For example, the RBAC role CsHelpDesk corresponds to the CsHelpDesk group found in the Users container in Active Directory Domain Services.</span></span> <span data-ttu-id="ce767-110">Darüber hinaus ist jede RBAC-Rolle einer Gruppe von lync Server-Windows PowerShell-Cmdlets zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ce767-110">In addition, each RBAC role is associated with a set of Lync Server Windows PowerShell cmdlets.</span></span> <span data-ttu-id="ce767-111">Diese Cmdlets stellen die Aufgaben dar, die von Benutzern ausgeführt werden können, denen die angegebene RBAC-Rolle zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce767-111">These cmdlets represent the tasks that can be carried out by users who have been assigned the given RBAC role.</span></span> <span data-ttu-id="ce767-112">Beispielsweise wurden der CsHelpDesk-Rolle die Lock-CsClientPin-und UnlockCsClientPin-Cmdlets zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ce767-112">For example, the CsHelpDesk role has been assigned the Lock-CsClientPin and UnlockCsClientPin cmdlets.</span></span> <span data-ttu-id="ce767-113">Das bedeutet, dass Benutzer, denen die CsHelpDesk-Rolle zugewiesen wurde, Benutzer-PIN-Nummern Sperren und entsperren können.</span><span class="sxs-lookup"><span data-stu-id="ce767-113">That means users who have been assigned the CsHelpDesk role can lock and unlock user PIN numbers.</span></span> <span data-ttu-id="ce767-114">Der CsHelpDesk-Rolle wurde jedoch nicht das New-CsVoicePolicy-Cmdlet zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ce767-114">However, the CsHelpDesk role has not been assigned the New-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="ce767-115">Das bedeutet, dass Benutzer, denen die CsHelpDesk-Rolle zugewiesen wurde, keine neuen VoIP-Richtlinien erstellen können.</span><span class="sxs-lookup"><span data-stu-id="ce767-115">That means that users who have been assigned the CsHelpDesk role cannot create new voice policies.</span></span>

<div>

## <a name="viewing-information-about-rbac-roles"></a><span data-ttu-id="ce767-116">Anzeigen von Informationen zu RBAC-Rollen</span><span class="sxs-lookup"><span data-stu-id="ce767-116">Viewing Information about RBAC Roles</span></span>

<span data-ttu-id="ce767-117">Sie können grundlegende Informationen zu ihren RBAC-Rollen abrufen, indem Sie den folgenden Befehl in der lync Server-Verwaltungsshell ausführen:</span><span class="sxs-lookup"><span data-stu-id="ce767-117">You can retrieve basic information about your RBAC roles by running the following command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRole

<span data-ttu-id="ce767-118">Beachten Sie, dass die Identität der RBAC-Rolle (beispielsweise CsVoiceAdministrator) eine direkte Zuordnung zu einer Sicherheitsgruppe hat, die sich im Container Benutzer in den Active Directory-Domänendiensten befindet.</span><span class="sxs-lookup"><span data-stu-id="ce767-118">Keep in mind that the Identity of the RBAC role (for example, CsVoiceAdministrator) has a direct mapping to a security group found in the Users container in Active Directory Domain Services.</span></span>

<span data-ttu-id="ce767-119">Wenn Sie eine Liste der Cmdlets anzeigen möchten, die einer Rolle zugewiesen wurden, verwenden Sie einen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="ce767-119">To view a list of the cmdlets that have been assigned to a role, use a command similar to this:</span></span>

    Get-CsAdminRole -Identity "CsHelpDesk" | Select-Object -ExpandProperty Cmdlets

</div>

<div>

## <a name="assigning-an-rbac-role-to-a-user"></a><span data-ttu-id="ce767-120">Zuweisen einer RBAC-Rolle zu einem Benutzer</span><span class="sxs-lookup"><span data-stu-id="ce767-120">Assigning an RBAC Role to a User</span></span>

<span data-ttu-id="ce767-121">Wenn Sie einem Benutzer eine RBAC-Rolle zuweisen möchten, müssen Sie diesen Benutzer der entsprechenden Active Directory-Sicherheitsgruppe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce767-121">To assign an RBAC role to a user, you must add that user to the appropriate Active Directory security group.</span></span> <span data-ttu-id="ce767-122">Um beispielsweise die CsLocationAdministrator-Rolle einem Benutzer zuzuweisen, müssen Sie diesen Benutzer der Gruppe CsLocationAdministrator hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce767-122">For example, to assign the CsLocationAdministrator role to a user, you must add that user to the CsLocationAdministrator group.</span></span> <span data-ttu-id="ce767-123">Dies kann durchführen des folgenden Verfahrens erfolgen:</span><span class="sxs-lookup"><span data-stu-id="ce767-123">That can be done by carrying out the following procedure:</span></span>

<span data-ttu-id="ce767-124">**So weisen Sie einen Benutzer einer Sicherheitsgruppe zu**</span><span class="sxs-lookup"><span data-stu-id="ce767-124">**To assign a user to a security group**</span></span>

1.  <span data-ttu-id="ce767-125">Melden Sie sich bei einem Computer, auf dem Active Directory-Benutzer und-Computer installiert wurden, mit einem Konto an, das über die Berechtigung zum Ändern der Mitgliedschaft einer Active Directory-Gruppe verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce767-125">Using an account that has permission to modify the membership of an Active Directory group, log on to a computer where Active Directory Users and Computers has been installed.</span></span>

2.  <span data-ttu-id="ce767-126">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Active Directory-Benutzer und-Computer**.</span><span class="sxs-lookup"><span data-stu-id="ce767-126">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

3.  <span data-ttu-id="ce767-127">Erweitern Sie in Active Directory-Benutzer und-Computer den Namen Ihrer Domäne, und klicken Sie auf den Container **Benutzer** .</span><span class="sxs-lookup"><span data-stu-id="ce767-127">In Active Directory Users and Computers, expand the name of your domain and click the **Users** container.</span></span>

4.  <span data-ttu-id="ce767-128">Klicken Sie mit der rechten Maustaste auf die Sicherheitsgruppe **CsLocationAdministrator**, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="ce767-128">Right-click the security group **CsLocationAdministrator**, and then click **Properties**.</span></span>

5.  <span data-ttu-id="ce767-129">Klicken Sie im Dialogfeld **Eigenschaften** auf der Registerkarte **Mitglieder** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ce767-129">In the **Properties** dialog box, on the **Members** tab, click **Add**.</span></span>

6.  <span data-ttu-id="ce767-130">Geben Sie im Dialogfeld **Benutzer, Computer, Kontakte oder Gruppen auswählen** den Benutzernamen oder den Anzeigenamen des Benutzers ein, der der Gruppe hinzugefügt werden soll (beispielsweise **Ken Myers**), und klicken Sie dann im Feld **Geben Sie die zu verwendenden Objektnamen ein** , und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce767-130">In the **Select Users, Computers, Contacts, or Groups** dialog box, type the user name or display name of the user to be added to the group (for example, **Ken Myer**) in the **Enter the object names to select** box and then click **OK**.</span></span>

7.  <span data-ttu-id="ce767-131">Klicken Sie im Dialogfeld **Eigenschaften** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce767-131">In the **Properties** dialog box, click **OK**.</span></span>

<span data-ttu-id="ce767-132">Um zu überprüfen, ob die RBAC-Rolle zugewiesen wurde, verwenden Sie das Cmdlet [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) , und übergeben Sie dem Cmdlet den sAMAccountName (Active Directory-Anmeldename) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ce767-132">To verify that the RBAC role has been assigned, use the [Get-CsAdminRoleAssignment](https://docs.microsoft.com/powershell/module/skype/Get-CsAdminRoleAssignment) cmdlet, passing the cmdlet the SamAccountName (Active Directory logon name) of the user.</span></span> <span data-ttu-id="ce767-133">Führen Sie diesen Befehl beispielsweise in der lync Server-Verwaltungsshell aus:</span><span class="sxs-lookup"><span data-stu-id="ce767-133">For example, run this command from within the Lync Server Management Shell:</span></span>

    Get-CsAdminRoleAssignment  -Identity "kenmyer"

<span data-ttu-id="ce767-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ce767-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

