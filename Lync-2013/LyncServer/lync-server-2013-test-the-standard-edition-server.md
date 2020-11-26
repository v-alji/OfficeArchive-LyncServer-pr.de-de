---
title: 'Lync Server 2013: Testen des Standard Edition-Servers'
description: 'Lync Server 2013: Testen Sie den Standard Edition-Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test the Standard Edition server
ms:assetid: b6ef67bb-9665-43e4-b8b3-eac8898eebf6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412890(v=OCS.15)
ms:contentKeyID: 48185220
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 35dc13fc01979cc8b293d0647a7886b7d65d7669
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441179"
---
# <a name="test-the-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="f4bba-103">Testen des Standard Edition-Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4bba-103">Test the Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f4bba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f4bba-104">

<span> </span></span></span>

<span data-ttu-id="f4bba-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="f4bba-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="f4bba-106">Im folgenden Verfahren wird beschrieben, wie Sie die Bereitstellungeines Standard Edition-Servers testen.</span><span class="sxs-lookup"><span data-stu-id="f4bba-106">The following procedure describes how to test the deployment of a Standard Edition server.</span></span>

<div>

## <a name="to-test-the-deployment-of-a-standard-edition-server"></a><span data-ttu-id="f4bba-107">So testen Sie die Bereitstellungeines Standard Edition-Servers</span><span class="sxs-lookup"><span data-stu-id="f4bba-107">To test the deployment of a Standard Edition Server</span></span>

1.  <span data-ttu-id="f4bba-108">Verwenden Sie Active Directory-Computer und-Benutzer, um das Active Directory-Benutzerobjekt der Administratorrolle für die lync Server 2013-Bereitstellung (auf der lync Server Control Panel installiert ist) zur **CSAdministrator** -Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f4bba-108">Use Active Directory Computers and Users to add the Active Directory user object of the administrator role for the Lync Server 2013 deployment (on which Lync Server Control Panel is installed) to the **CSAdministrator** group.</span></span>

2.  <span data-ttu-id="f4bba-109">Wenn das Benutzerobjekt derzeit angemeldet ist, melden Sie es ab und wieder an, um die neue Gruppenzuweisung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f4bba-109">If the user object is currently logged on, log off and then log on again to register the new group assignment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f4bba-110">Das Benutzerkonto kann nicht der lokale Administrator des Servers sein, auf dem lync Server 2013, Standard Edition, ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4bba-110">The user account cannot be the local administrator of the server running Lync Server 2013, Standard Edition.</span></span> <span data-ttu-id="f4bba-111">Wenn Sie die entsprechenden Benutzer und Gruppen nicht zur CsAdministors-Gruppe hinzufügen, erhalten Sie eine Fehlermeldung, wenn Sie die lync Server 2013-Systemsteuerung öffnen, in der angegeben ist, dass "nicht autorisiert: der Zugriff verweigert wird aufgrund eines Autorisierungs Fehlers bei der rollenbasierten Zugriffssteuerung (Role-Based Access Control, RBAC)".</span><span class="sxs-lookup"><span data-stu-id="f4bba-111">If you do not add the appropriate users and groups to the CsAdministors group, you will receive an error when opening Lync Server 2013 Control Panel, which states that “Unauthorized: Access is denied due to a role-based access control (RBAC) authorization failure.”</span></span>

    
    </div>

3.  <span data-ttu-id="f4bba-112">Verwenden Sie das Administratorkonto, um sich bei dem Computer anzumelden, auf dem die lync Server-Systemsteuerung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f4bba-112">Use the administrative account to log on to the computer where Lync Server Control Panel is installed.</span></span>

4.  <span data-ttu-id="f4bba-113">Starten Sie die lync Server-Systemsteuerung, und geben Sie bei Aufforderung Anmeldeinformationen ein.</span><span class="sxs-lookup"><span data-stu-id="f4bba-113">Start Lync Server Control Panel and provide credentials, if prompted.</span></span> <span data-ttu-id="f4bba-114">Die lync Server 2013-Systemsteuerung zeigt Bereitstellungsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="f4bba-114">Lync Server 2013 Control Panel displays deployment information.</span></span>

5.  <span data-ttu-id="f4bba-115">Klicken Sie in der linken Navigationsleiste auf **Topologie**, und stellen Sie dann sicher, dass es sich bei dem Dienststatus um ein Computersymbol mit einem grünen Pfeil und ein grünes Häkchen neben jeder lync Server-Serverrolle handelt, die bereitgestellt und online geschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="f4bba-115">In the left navigation bar, click **Topology**, and then confirm that the service status is a computer icon with a green arrow and there is a green check mark next to each Lync Server server role that has been deployed and brought online.</span></span>

6.  <span data-ttu-id="f4bba-116">Klicken Sie in der linken Navigationsleiste auf **Benutzer**, und aktivieren Sie dann die beiden Benutzer für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f4bba-116">In the left navigation bar, click **Users**, and then enable the two users for Lync Server 2013.</span></span>

7.  <span data-ttu-id="f4bba-117">Melden Sie einen Benutzer an einem Computer, der mit der Domäne verbunden ist, und dem anderen Benutzer auf einem anderen Computer in der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="f4bba-117">Log one user on to a computer that is joined to the domain, and the other user on to another computer in the domain.</span></span>

8.  <span data-ttu-id="f4bba-118">Installieren Sie lync Server 2013 auf jedem der beiden Clientcomputer, und stellen Sie dann sicher, dass sich beide Benutzer bei lync Server 2013 anmelden können und Sofortnachrichten senden können.</span><span class="sxs-lookup"><span data-stu-id="f4bba-118">Install Lync Server 2013 on each of the two client computers, and then verify that both users can sign in to Lync Server 2013 and can send instant messages to each other.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f4bba-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4bba-119">See Also</span></span>


[<span data-ttu-id="f4bba-120">Bereitstellen von Clients und Geräten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4bba-120">Deploying clients and devices in Lync Server 2013</span></span>](lync-server-2013-deploying-clients-and-devices.md)  
  

<span data-ttu-id="f4bba-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f4bba-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

