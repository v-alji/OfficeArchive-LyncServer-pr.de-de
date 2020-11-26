---
title: 'Lync Server 2013: Hinzufügen und Aktivieren des Benutzerkontos für lync Server'
description: 'Lync Server 2013: Hinzufügen und Aktivieren des Benutzerkontos für lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add and enable user account for Lync Server
ms:assetid: 1edd1c1c-307d-450b-abea-33aaf56bdf13
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520961(v=OCS.15)
ms:contentKeyID: 48183578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f70ae2da122a0db3986a75677c1d29234fbe0e3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439373"
---
# <a name="add-and-enable-user-account-for-lync-server-2013"></a><span data-ttu-id="26501-103">Hinzufügen und Aktivieren des Benutzerkontos für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26501-103">Add and enable user account for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26501-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26501-104">

<span> </span></span></span>

<span data-ttu-id="26501-105">_**Letztes Änderungsdatum des Themas:** 2012-11-02_</span><span class="sxs-lookup"><span data-stu-id="26501-105">_**Topic Last Modified:** 2012-11-02_</span></span>

<span data-ttu-id="26501-106">Nachdem Sie ein Benutzerkonto in Active Directory-Benutzer und-Computer aktiviert haben, können Sie die lync Server-Systemsteuerung verwenden, um neue lync Server 2013-Benutzerkonten zu erstellen und zu aktivieren, indem Sie einen Active Directory-Benutzer zu lync Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="26501-106">After enabling a user account in Active Directory Users and Computers, you can use Lync Server Control Panel to create and enable new Lync Server 2013 user accounts by adding an Active Directory user to Lync Server.</span></span>

<div>

## <a name="to-add-and-enable-a-new-lync-server-user"></a><span data-ttu-id="26501-107">So fügen Sie einen neuen lync Server-Benutzer hinzu und aktivieren ihn</span><span class="sxs-lookup"><span data-stu-id="26501-107">To add and enable a new Lync Server user</span></span>

1.  <span data-ttu-id="26501-108">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="26501-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="26501-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="26501-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="26501-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="26501-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="26501-111">Klicken Sie in der linken Navigationsleiste auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="26501-111">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="26501-112">Klicken Sie auf **Benutzer aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="26501-112">Click **Enable users**.</span></span>

5.  <span data-ttu-id="26501-113">Klicken Sie im Dialogfeld **neuer lync Server-Benutzer** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="26501-113">On the **New Lync Server User** dialog, click **Add**.</span></span>

6.  <span data-ttu-id="26501-114">Geben Sie im Feld Benutzer suchen den gesamten oder den ersten Teil des Namens, den Anzeigenamen, den Vornamen, den **Nachnamen** , den Kontonamen, die e-Mail-Adresse, den Benutzerprinzipalnamen (User Principal Name, UPN) oder die Telefonnummer des gewünschten Active Directory-Benutzerkontos ein, und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="26501-114">In the **Search users** box, type all or the first portion of the name, display name, first name, last name, Security Accounts Manager (SAM) account name, email address, User Principal Name (UPN), or phone number of the Active Directory user account that you want, and then click **Find**.</span></span>

7.  <span data-ttu-id="26501-115">Wählen Sie in der Tabelle das Konto aus, das Sie zu lync Server hinzufügen möchten, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="26501-115">In the table, select the account you want to add to Lync Server, and then click **OK**.</span></span>

8.  <span data-ttu-id="26501-116">Weisen Sie den Benutzer einem Pool zu, geben Sie zusätzliche Details an, und weisen Sie die Richtlinien dem gewünschten Benutzer zu, und klicken Sie dann auf **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="26501-116">Assign the user to a pool, specify any additional details, and assign the policies to the user you want, and then click **Enable**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="26501-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26501-117">See Also</span></span>


[<span data-ttu-id="26501-118">Deaktivieren oder erneutes Aktivieren des Benutzerkontos für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26501-118">Disable or re-enable user account for Lync Server 2013</span></span>](lync-server-2013-disable-or-re-enable-user-account-for-lync-server.md)  
[<span data-ttu-id="26501-119">Entfernen eines Benutzerkontos aus lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26501-119">Remove a user account from Lync Server 2013</span></span>](lync-server-2013-remove-a-user-account-from-lync-server.md)  


[<span data-ttu-id="26501-120">Aktivieren und Deaktivieren von Benutzern für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26501-120">Enabling and disabling users for Lync Server 2013</span></span>](lync-server-2013-enabling-and-disabling-users-for-lync-server.md)  
  

<span data-ttu-id="26501-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26501-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

