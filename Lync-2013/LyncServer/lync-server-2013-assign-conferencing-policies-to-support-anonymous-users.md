---
title: 'Lync Server 2013: Zuweisen von Konferenzrichtlinien zur Unterstützung anonymer Benutzer'
description: 'Lync Server 2013: Zuweisen von Konferenzrichtlinien zur Unterstützung anonymer Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign conferencing policies to support anonymous users
ms:assetid: 662de022-1111-40f7-bad4-f2b686f30973
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521007(v=OCS.15)
ms:contentKeyID: 48184333
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07e94c3097e3e21f854e91fdee1ad0b33c3b9f53
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443211"
---
# <a name="assign-conferencing-policies-to-support-anonymous-users-in-lync-server-2013"></a><span data-ttu-id="5028b-103">Zuweisen von Konferenzrichtlinien zur Unterstützung anonymer Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5028b-103">Assign conferencing policies to support anonymous users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5028b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5028b-104">

<span> </span></span></span>

<span data-ttu-id="5028b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="5028b-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="5028b-106">Standardmäßig werden alle Benutzer daran gehindert, anonyme Benutzer zur Teilnahme an einer Besprechung einzuladen.</span><span class="sxs-lookup"><span data-stu-id="5028b-106">By default, all users are prevented from inviting anonymous users to participate in a meeting.</span></span> <span data-ttu-id="5028b-107">Sie steuern, wer anonyme Benutzer einladen kann, indem Sie eine konferenzrichtlinie für die Unterstützung anonymer Benutzer konfigurieren und diese konferenzrichtlinie auf bestimmte Benutzer anwenden.</span><span class="sxs-lookup"><span data-stu-id="5028b-107">You control who can invite anonymous users by configuring a conferencing policy to support anonymous users, and applying that conferencing policy to specific users.</span></span> <span data-ttu-id="5028b-108">Details zum Konfigurieren von Konferenzrichtlinien zur Unterstützung anonymer Benutzer finden Sie unter [erstellen oder Ändern einer konferenzrichtlinie in lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) und [Verwalten des Föderations-und des externen Zugriffs auf lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="5028b-108">For details about how to configure a conferencing policies to support anonymous users, see [Create or modify a conferencing policy in Lync Server 2013](lync-server-2013-create-or-modify-a-conferencing-policy.md) and [Managing federation and external access to Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md).</span></span>

<span data-ttu-id="5028b-109">Verwenden Sie das Verfahren in diesem Abschnitt, um eine konferenzrichtlinie anzuwenden, die Sie bereits für einen oder mehrere Benutzer oder Benutzergruppen erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5028b-109">Use the procedure in this section to apply a conferencing policy that you have already created to one or more users or user groups.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5028b-110">Neben der Konfiguration und Anwendung einer Richtlinie, mit der Benutzer anonyme Benutzer einladen können, müssen Sie auch die Unterstützung für anonyme Benutzer für Ihre Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5028b-110">In addition to configuring and applying a policy to enable users to invite anonymous users, you must also enable support for anonymous users for your organization.</span></span> <span data-ttu-id="5028b-111">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">Konfigurieren von Richtlinien zum Steuern des Zugriffs öffentlicher Benutzer in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="5028b-111">For details, see <A href="lync-server-2013-configure-policies-to-control-public-user-access.md">Configure policies to control public user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-configure-a-user-policy-for-anonymous-participation-in-meetings"></a><span data-ttu-id="5028b-112">So konfigurieren Sie eine Benutzerrichtlinie für die anonyme Teilnahme an Besprechungen</span><span class="sxs-lookup"><span data-stu-id="5028b-112">To configure a user policy for anonymous participation in meetings</span></span>

1.  <span data-ttu-id="5028b-113">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="5028b-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5028b-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5028b-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5028b-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5028b-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5028b-116">Klicken Sie in der linken Navigationsleiste auf **Konferenzen**, und führen Sie dann eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="5028b-116">In the left navigation bar, click **Conferencing**, and then do one of the following:</span></span>
    
    1.  <span data-ttu-id="5028b-117">Klicken Sie zum Erstellen einer neuen Benutzerrichtlinie auf **neu**, und klicken Sie dann auf **Benutzerrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="5028b-117">To create a new user policy, click **New**, and then click **User policy**.</span></span> <span data-ttu-id="5028b-118">Erstellen Sie im Feld **Name** einen eindeutigen Namen, der angibt, was die Benutzerrichtlinie umfasst (beispielsweise **EnableAnonymous** für eine Benutzerrichtlinie, die die Kommunikation mit anonymen Benutzern ermöglicht).</span><span class="sxs-lookup"><span data-stu-id="5028b-118">Create a unique name in the **Name** field that indicates what the user policy covers (for example, **EnableAnonymous** for a user policy that enables communications with anonymous users).</span></span>
    
    2.  <span data-ttu-id="5028b-119">Wenn Sie eine vorhandene Benutzerrichtlinie konfigurieren möchten, klicken Sie auf die entsprechende Richtlinie, die in der Tabelle aufgeführt ist, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="5028b-119">To configure an existing user policy, click the appropriate policy listed in the table, click **Edit**, and then click **Show details**.</span></span>

4.  <span data-ttu-id="5028b-120">Aktivieren Sie im Dialogfeld **Konferenzrichtlinien** das Kontrollkästchen **Teilnehmern die Möglichkeit geben, anonyme Benutzer einzuladen** .</span><span class="sxs-lookup"><span data-stu-id="5028b-120">In the **Conferencing Policies** dialog box, select the **Allow participants to invite anonymous users** check box.</span></span>

5.  <span data-ttu-id="5028b-121">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5028b-121">Click **Commit**.</span></span>

6.  <span data-ttu-id="5028b-122">Klicken Sie in der linken Navigationsleiste auf **Benutzer**, suchen Sie nach dem Benutzerkonto, das Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5028b-122">In the left navigation bar, click **Users**, search on the user account that you want to configure.</span></span>

7.  <span data-ttu-id="5028b-123">Klicken Sie in der Tabelle mit den Suchergebnissen auf das Benutzerkonto, klicken Sie auf **Bearbeiten** und dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="5028b-123">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

8.  <span data-ttu-id="5028b-124">Wählen Sie in **lync Server-Benutzer bearbeiten** unter **konferenzrichtlinie** die Benutzerrichtlinie mit der Konfiguration für den anonymen Benutzer Zugriff aus, die Sie auf diesen Benutzer anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5028b-124">In **Edit Lync Server User** under **Conferencing policy**, select the user policy with the anonymous user access configuration that you want to apply to this user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5028b-125">Die <STRONG> &lt; automatischen &gt; </STRONG> Einstellungen wenden die Standardeinstellungen für Server Installationen an und werden automatisch vom Server angewendet.</span><span class="sxs-lookup"><span data-stu-id="5028b-125">The <STRONG>&lt;Automatic&gt;</STRONG> settings apply the default server installation settings and are applied automatically by the server.</span></span>

    
    </div>

<span data-ttu-id="5028b-126">Damit Benutzer anonyme Benutzer zu Konferenzen einladen können, müssen Sie auch die Unterstützung für anonyme Benutzer in Ihrer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5028b-126">To enable users to invite anonymous users to conferences, you must also enable support for anonymous users in your organization.</span></span> <span data-ttu-id="5028b-127">Ausführliche Informationen finden Sie unter [Konfigurieren von Richtlinien zum Steuern des Zugriffs öffentlicher Benutzer in lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) in der Bereitstellungsdokumentation oder in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5028b-127">For details, see [Configure policies to control public user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-public-user-access.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="5028b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5028b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

