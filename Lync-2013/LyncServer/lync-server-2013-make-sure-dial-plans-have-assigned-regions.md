---
title: 'Lync Server 2013: Sicherstellen, dass Wählplänen Regionen zugewiesen wurden'
description: 'Lync Server 2013: Stellen Sie sicher, dass die Wählpläne Regionen zugewiesen haben.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Make sure dial plans have assigned regions
ms:assetid: 3da3a907-0dbf-4440-b12f-370f94dd4c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425903(v=OCS.15)
ms:contentKeyID: 48183937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c055eda221bc03de449631ba38483165a8621773
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426151"
---
# <a name="make-sure-dial-plans-lync-server-2013-have-assigned-regions"></a><span data-ttu-id="a2cac-103">Sicherstellen, dass die Wähleinstellungen lync Server 2013 Regionen zugewiesen haben</span><span class="sxs-lookup"><span data-stu-id="a2cac-103">Make sure dial plans Lync Server 2013 have assigned regions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2cac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2cac-104">

<span> </span></span></span>

<span data-ttu-id="a2cac-105">_**Letztes Änderungsdatum des Themas:** 2010-11-02_</span><span class="sxs-lookup"><span data-stu-id="a2cac-105">_**Topic Last Modified:** 2010-11-02_</span></span>

<span data-ttu-id="a2cac-106">Für Wählpläne, die für Einwahlkonferenzen verwendet werden, muss ein **Bereich für Einwahlkonferenzen** angegeben werden, um Zugriffsnummern für Einwahlkonferenzen mit den entsprechenden Wähleinstellungen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a2cac-106">Dial plans that are used for dial-in conferencing need to have a **Dial-in conferencing region** specified to associate dial-in conferencing access numbers with the appropriate dial plan.</span></span> <span data-ttu-id="a2cac-107">Wenn Sie einen Satz mit Wähleinstellungen einrichten, geben Sie die Region für Einwahlkonferenzen an, die für diese Wähleinstellungen gilt.</span><span class="sxs-lookup"><span data-stu-id="a2cac-107">When you set up a dial plan, you specify the dial-in conferencing region that applies to that dial plan.</span></span> <span data-ttu-id="a2cac-108">Wenn Sie die Einwahl Zugriffsnummer erstellen, wählen Sie dann die Regionen aus, die die Zugriffsnummer den entsprechenden Wählplänen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a2cac-108">Then, when you create the dial-in access number, you select the regions that associate the access number with the appropriate dial plans.</span></span>

<span data-ttu-id="a2cac-109">Da es wichtig ist, einen Bereich für alle Wählpläne anzugeben, empfehlen wir, dass Sie diese Vorgehensweise verwenden, um zu überprüfen, ob alle Wählpläne Regionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a2cac-109">Because it important to specify a region for all dial plans, we recommend that you use this procedure to verify that all dial plans have regions.</span></span> <span data-ttu-id="a2cac-110">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="a2cac-110">This step is optional.</span></span>

<span data-ttu-id="a2cac-111">Verwenden Sie das Cmdlet **Get-CsDialPlan** , um zu überprüfen, ob der Bereich für alle Wählpläne für Einwahlkonferenzen festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="a2cac-111">Use the **Get-CsDialPlan** cmdlet to verify whether the region is set for all dial-in conferencing dial plans.</span></span> <span data-ttu-id="a2cac-112">Wenn die Region in bestimmten Wählplänen nicht vorhanden ist, können Sie die Region über das Cmdlet **Set-CsDialPlan** festlegen.</span><span class="sxs-lookup"><span data-stu-id="a2cac-112">If the region is missing from dial plans, you can use the **Set-CsDialPlan** cmdlet to set the region.</span></span> <span data-ttu-id="a2cac-113">Sie können auch die lync Server-Systemsteuerung verwenden, um den Bereich in vorhandenen Wählplänen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a2cac-113">You can also use Lync Server Control Panel to update the region in existing dial plans.</span></span> <span data-ttu-id="a2cac-114">Ausführliche Informationen zur Verwendung der lync Server-Systemsteuerung finden Sie unter [Ändern von Wähleinstellungen in lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="a2cac-114">For details about using Lync Server Control Panel, see [Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md).</span></span>

<div>

## <a name="to-verify-whether-dial-plans-have-the-region-property-set"></a><span data-ttu-id="a2cac-115">So überprüfen Sie, ob für Wähleinstellungen die Region festgelegt wurde</span><span class="sxs-lookup"><span data-stu-id="a2cac-115">To verify whether dial plans have the region property set</span></span>

1.  <span data-ttu-id="a2cac-116">Melden Sie sich beim Computer als Mitglied der Gruppe „RTCUniversalServerAdmins“ oder als Benutzer mit der Rolle **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** oder **CsAdministrator** an.</span><span class="sxs-lookup"><span data-stu-id="a2cac-116">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="a2cac-117">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="a2cac-117">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="a2cac-118">Führen Sie den folgenden Befehl an der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="a2cac-118">Run the following at the command prompt:</span></span>
    
        Get-CsDialPlan [-Identity <Identifier of the dial plans to be retrieved>]
    
    <span data-ttu-id="a2cac-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a2cac-119">For example:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="a2cac-120">In diesem Beispiel werden alle für Ihre Organisation konfigurierten Wähleinstellungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a2cac-120">In this example, all the dial plans configured for your organization are returned.</span></span>

4.  <span data-ttu-id="a2cac-121">Überprüfen Sie die zurückgegebenen Wähleinstellungen, um fehlende Regionen für Einwahlkonferenzen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a2cac-121">Review the returned dial plans to identify any that are missing the dial-in conferencing region.</span></span> <span data-ttu-id="a2cac-122">Ausführliche Informationen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="a2cac-122">For details, see the Lync Server Management Shell documentation.</span></span>

</div>

<div>

## <a name="to-set-the-region-property-for-a-dial-plan"></a><span data-ttu-id="a2cac-123">So legen Sie die Region für einen Satz mit Wähleinstellungen fest</span><span class="sxs-lookup"><span data-stu-id="a2cac-123">To set the region property for a dial plan</span></span>

1.  <span data-ttu-id="a2cac-124">Melden Sie sich beim Computer als Mitglied der Gruppe „RTCUniversalServerAdmins“ oder als Benutzer mit der Rolle **Cs-VoiceAdministrator**, **Cs-ServerAdministrator** oder **CsAdministrator** an.</span><span class="sxs-lookup"><span data-stu-id="a2cac-124">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the **Cs-VoiceAdministrator**, **Cs-ServerAdministrator**, or **CsAdministrator** role.</span></span>

2.  <span data-ttu-id="a2cac-125">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="a2cac-125">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="a2cac-126">Führen Sie für alle Wähleinstellungen, in denen die Region für Einwahlkonferenzen fehlt, den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="a2cac-126">For any dial plans that are missing the dial-in conferencing region, run:</span></span>
    
        Set-CsDialPlan [-Identity <Identity of the dial plan to be modified>] -DialinConferencingRegion "<new region>"
    
    <span data-ttu-id="a2cac-127">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a2cac-127">For example:</span></span>
    
        Set-CsDialPlan -Identity Redmond -DialinConferencingRegion "US West Coast"
    
    <span data-ttu-id="a2cac-128">In diesem Beispiel wird die Eigenschaft "DialinConferencingRegion" in den Wähleinstellungen mit der Identität "Redmond" in den Wert "US West Coast" geändert.</span><span class="sxs-lookup"><span data-stu-id="a2cac-128">In this example, the dial plan with the Identity of Redmond is modified to set the DialinConferencingRegion property to "US West Coast".</span></span> <span data-ttu-id="a2cac-129">Ausführliche Informationen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="a2cac-129">For details, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="a2cac-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2cac-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

