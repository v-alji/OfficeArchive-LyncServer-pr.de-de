---
title: 'Lync Server 2013: Vorbereiten von Domänen'
description: 'Lync Server 2013: Vorbereiten von Domänen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing domains
ms:assetid: 8eea541c-5f9d-4afc-92a8-a31d6f742544
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398721(v=OCS.15)
ms:contentKeyID: 48184816
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7700bbdd10a96949f892858ae03da8de60d86a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424163"
---
# <a name="preparing-domains-for-lync-server-2013"></a><span data-ttu-id="f2789-103">Vorbereiten von Domänen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2789-103">Preparing domains for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2789-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2789-104">

<span> </span></span></span>

<span data-ttu-id="f2789-105">_**Letztes Änderungsdatum des Themas:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="f2789-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="f2789-106">Die Domänenvorbereitung ist der letzte Schritt beim Vorbereiten der Active Directory-Domänendienste für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2789-106">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span> <span data-ttu-id="f2789-107">Beim Schritt zur Domänenvorbereitung werden universellen Gruppen die erforderlichen ACEs (Access Control Entries, Zugriffssteuerungseinträge) hinzugefügt, über die Berechtigungen zum Hosten und Verwalten von Benutzern in der Domäne gewährt werden.</span><span class="sxs-lookup"><span data-stu-id="f2789-107">The domain preparation step adds the necessary access control entries (ACEs) to universal groups that grant permissions to host and manage users within the domain.</span></span> <span data-ttu-id="f2789-108">Bei der Domänenvorbereitung werden ACEs im Domänenstamm und in drei integrierten Containern erstellt: für Benutzer, Computer und Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="f2789-108">Domain preparation creates ACEs on the domain root and three built-in containers: User, Computers, and Domain Controllers.</span></span>

<span data-ttu-id="f2789-109">Sie können die Domänenvorbereitung auf jedem Computer in der Domäne ausführen, in der Sie lync Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f2789-109">You can run domain preparation on any computer in the domain where you are deploying Lync Server.</span></span> <span data-ttu-id="f2789-110">Sie müssen jede Domäne vorbereiten, die lync Server oder Benutzer hosten soll.</span><span class="sxs-lookup"><span data-stu-id="f2789-110">You must prepare every domain that will host Lync Server or users.</span></span>

<span data-ttu-id="f2789-111">Wenn die Vererbung von Berechtigungen deaktiviert ist oder die Berechtigungen für authentifizierte Benutzer in Ihrer Organisation deaktiviert sind, müssen Sie während der Domänenvorbereitung weitere Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2789-111">If permissions inheritance is disabled or authenticated user permissions are disabled in your organization, you must perform additional steps during domain preparation.</span></span> <span data-ttu-id="f2789-112">Ausführliche Informationen finden Sie unter [Vorbereiten einer gesperrten Active Directory-Domänendienste in lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="f2789-112">For details, see [Preparing a locked-down Active Directory Domain Services in Lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).</span></span>

<span data-ttu-id="f2789-113">Wenn Ihre Organisation Organisationseinheiten (OU) anstelle der drei integrierten Container (also Benutzer, Computer und Domänencontroller) verwendet, müssen Sie den Organisationseinheiten Lesezugriff für die Gruppe Authentifizierte Benutzer erteilen.</span><span class="sxs-lookup"><span data-stu-id="f2789-113">If your organization uses organizational units (OU) instead of the three built-in containers (that is, Users, Computers, and Domain Controllers), you must grant read access to the OUs for the Authenticated Users group.</span></span> <span data-ttu-id="f2789-114">Für die Domänenvorbereitung ist Lesezugriff auf die Container erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2789-114">Read access to the containers is required for domain preparation.</span></span> <span data-ttu-id="f2789-115">Wenn die Gruppe der authentifizierten Benutzer keinen Lesezugriff auf die Organisationseinheit hat, führen Sie das Cmdlet **Grant-CsOuPermission** aus, wie in den folgenden Codebeispielen veranschaulicht, um Leseberechtigungen für jede OU zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="f2789-115">If the Authenticated Users group does not have read access to the OU, run the **Grant-CsOuPermission** cmdlet as illustrated in the following code examples to grant read permissions for each OU.</span></span>

   ```PowerShell
    Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU > 
   ```

   ```PowerShell
    Grant-CsOuPermission -ObjectType "user","contact",inetOrgPerson" -OU "ou=Redmond,dc=contoso,dc=net"
   ```

<span data-ttu-id="f2789-116">Details zum Cmdlet **Grant-CsOuPermission** finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="f2789-116">For details about the **Grant-CsOuPermission** cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div class="">


> [!TIP]  
> <span data-ttu-id="f2789-117">Details zu den ACEs, die im Domänenstamm und in den Containern Benutzer, Computer und Domänencontroller erstellt wurden, finden Sie unter Änderungen, die <A href="lync-server-2013-changes-made-by-domain-preparation.md">von der Domänenvorbereitung in lync Server 2013 vorgenommen</A>wurden.</span><span class="sxs-lookup"><span data-stu-id="f2789-117">For details about the ACEs created on the domain root and in the Users, Computers, and Domain Controllers containers, see <A href="lync-server-2013-changes-made-by-domain-preparation.md">Changes made by domain preparation in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f2789-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f2789-118">In This Section</span></span>

  - [<span data-ttu-id="f2789-119">Ausführen der Domänenvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2789-119">Running domain preparation for Lync Server 2013</span></span>](lync-server-2013-running-domain-preparation.md)

  - [<span data-ttu-id="f2789-120">Verwenden von Cmdlets zum Rückgängigmachen der Domänenvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2789-120">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)

<span data-ttu-id="f2789-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2789-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

