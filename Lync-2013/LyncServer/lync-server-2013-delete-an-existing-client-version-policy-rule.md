---
title: 'Lync Server 2013: Löschen einer vorhandenen clientversionsrichtlinien Regel'
description: 'Lync Server 2013: Löschen einer vorhandenen clientversionsrichtlinien Regel'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing client version policy rule
ms:assetid: 2fe351c4-d78b-47d5-af49-d47ee5e0fe42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923066(v=OCS.15)
ms:contentKeyID: 50675352
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 48cb2dc6458406c988bdc2626fc000c7a9bf5d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430609"
---
# <a name="delete-an-existing-client-version-policy-rule-in-lync-server-2013"></a><span data-ttu-id="6597a-103">Löschen einer vorhandenen clientversionsrichtlinien Regel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-103">Delete an existing client version policy rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6597a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6597a-104">

<span> </span></span></span>

<span data-ttu-id="6597a-105">_**Letztes Änderungsdatum des Themas:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="6597a-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="6597a-106">Eine clientversionsrichtlinie besteht aus einer Reihe von clientversionsrichtlinien Regeln.</span><span class="sxs-lookup"><span data-stu-id="6597a-106">A client version policy is made up of a set of client version policy rules.</span></span> <span data-ttu-id="6597a-107">Mit diesen Regeln werden die Aktionen definiert, die ausgeführt werden sollen, wenn Benutzer sich mit bestimmten Clients und Clientversionen anmelden möchten.</span><span class="sxs-lookup"><span data-stu-id="6597a-107">These rules define the actions that should be taken when users attempt to log on with specific clients and client versions.</span></span> <span data-ttu-id="6597a-108">Sie können einzelne Regeln aus einer clientversionsrichtlinie aus der lync Server 2013-Systemsteuerung löschen.</span><span class="sxs-lookup"><span data-stu-id="6597a-108">You can delete individual rules from a client version policy from Lync Server 2013 Control Panel.</span></span>

<div>

## <a name="to-delete-client-version-policy-rules-with-lync-server-control-panel"></a><span data-ttu-id="6597a-109">So löschen Sie clientversionsrichtlinien Regeln mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="6597a-109">To delete client version policy rules with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="6597a-110">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="6597a-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="6597a-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6597a-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="6597a-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="6597a-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="6597a-113">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Schaltfläche für die **Client Versionsrichtlinien** -Navigation.</span><span class="sxs-lookup"><span data-stu-id="6597a-113">In the left navigation bar, click **Clients**, and then click the **Client Version Policy** navigation button.</span></span>

4.  <span data-ttu-id="6597a-114">Doppelklicken Sie auf der Seite **clientversionsrichtlinie** auf die clientversionsrichtlinie für die Regel, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="6597a-114">On the **Client Version Policy** page, double-click the client version policy for the rule you want to delete.</span></span>

5.  <span data-ttu-id="6597a-115">Die Regeln werden auf der Seite **Richtlinie zum Bearbeiten der Client Version** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6597a-115">The rules appear on the **Edit Client Version Policy** page.</span></span> <span data-ttu-id="6597a-116">Wenn Sie eine Regel löschen möchten, wählen Sie die Regel aus, und klicken Sie dann auf **Entfernen**.</span><span class="sxs-lookup"><span data-stu-id="6597a-116">To delete a rule, select the rule, and then click **Remove**.</span></span>

<span data-ttu-id="6597a-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6597a-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

