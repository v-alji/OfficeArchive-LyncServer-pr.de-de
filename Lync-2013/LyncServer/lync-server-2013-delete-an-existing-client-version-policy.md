---
title: 'Lync Server 2013: Löschen einer vorhandenen clientversionsrichtlinie'
description: 'Lync Server 2013: Löschen einer vorhandenen clientversionsrichtlinie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing client version policy
ms:assetid: b88aaa25-97ff-4eb6-bd34-b97332cd6890
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ923064(v=OCS.15)
ms:contentKeyID: 50675349
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1328d54790b2a7856fa2776bb59feeb515bab1cf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430602"
---
# <a name="delete-an-existing-client-version-policy-in-lync-server-2013"></a><span data-ttu-id="b5770-103">Löschen einer vorhandenen clientversionsrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5770-103">Delete an existing client version policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5770-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5770-104">

<span> </span></span></span>

<span data-ttu-id="b5770-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="b5770-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="b5770-106">Wenn Sie eine zuvor konfigurierte clientversionsrichtlinie löschen möchten, können Sie Sie aus der lync Server 2013-Systemsteuerung oder der lync Server 2013-Verwaltungsshell löschen.</span><span class="sxs-lookup"><span data-stu-id="b5770-106">If you want to delete a client version policy that was previously configured, you can delete it from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-delete-client-version-policies-by-using-lync-server-control-panel"></a><span data-ttu-id="b5770-107">So löschen Sie clientversionsrichtlinien mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="b5770-107">To delete client version policies by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="b5770-108">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b5770-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b5770-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b5770-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b5770-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b5770-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b5770-111">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Schaltfläche für die **Client Versionsrichtlinien** -Navigation.</span><span class="sxs-lookup"><span data-stu-id="b5770-111">In the left navigation bar, click **Clients**, and then click the **Client Version Policy** navigation button.</span></span>

4.  <span data-ttu-id="b5770-112">Wählen Sie auf der Seite **clientversionsrichtlinie** die clientversionsrichtlinie oder Richtlinien aus, die Sie löschen möchten, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="b5770-112">On the **Client Version Policy** page, select the client version policy or policies you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="deleting-client-version-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="b5770-113">Löschen von Client Versionsrichtlinien mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b5770-113">Deleting Client Version Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="b5770-114">Sie können clientversionsrichtlinien mithilfe des Cmdlets **Remove-CsClientVersionPolicy** löschen.</span><span class="sxs-lookup"><span data-stu-id="b5770-114">You can delete client version policies by using the **Remove-CsClientVersionPolicy** cmdlet.</span></span> <span data-ttu-id="b5770-115">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b5770-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b5770-116">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b5770-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specific-client-version-policy"></a><span data-ttu-id="b5770-117">So entfernen Sie eine bestimmte clientversionsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b5770-117">To remove a specific client version policy</span></span>

  - <span data-ttu-id="b5770-118">Mit diesem Befehl wird die auf die Redmond-Website angewendete clientversionsrichtlinie gelöscht:</span><span class="sxs-lookup"><span data-stu-id="b5770-118">This command deletes the client version policy applied to the Redmond site:</span></span>
    
        Remove-CsClientVersionPolicy -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-client-version-policies-applied-to-the-site-scope"></a><span data-ttu-id="b5770-119">So entfernen Sie alle auf den Website Bereich angewendeten clientversionsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="b5770-119">To remove all the client version policies applied to the site scope</span></span>

  - <span data-ttu-id="b5770-120">Mit diesem Befehl werden alle auf dem Website Bereich konfigurierten clientversionsrichtlinien entfernt:</span><span class="sxs-lookup"><span data-stu-id="b5770-120">This command removes all the client version policies configured at the site scope:</span></span>
    
        Get-CsClientVersionPolicy -Fiter "site:*" | Remove-CsClientVersionPolicy

</div>

<div>

## <a name="to-remove-client-version-policies-that-do-not-include-a-specific-user-agent"></a><span data-ttu-id="b5770-121">So entfernen Sie clientversionsrichtlinien, die keinen bestimmten Benutzer-Agent enthalten</span><span class="sxs-lookup"><span data-stu-id="b5770-121">To remove client version policies that do not include a specific user agent</span></span>

  - <span data-ttu-id="b5770-122">Und mit diesem Befehl werden alle clientversionsrichtlinien entfernt, die keine Regel für den Windows Phone lync (WPLync)-Benutzer-Agent enthalten:</span><span class="sxs-lookup"><span data-stu-id="b5770-122">And this command removes any client version policies that do not include a rule for the Windows Phone Lync (WPLync) user agent:</span></span>
    
        Get-CsClientVersionPolicy | Where-Object {$_.Rules -notmatch "UserAgent=WPLync" | Remove-CsClientVersionPolicy

</div>

<span data-ttu-id="b5770-123">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) .</span><span class="sxs-lookup"><span data-stu-id="b5770-123">For details, see the Help topic for the [Remove-CsClientVersionPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsClientVersionPolicy) cmdlet.</span></span>

<span data-ttu-id="b5770-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5770-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

