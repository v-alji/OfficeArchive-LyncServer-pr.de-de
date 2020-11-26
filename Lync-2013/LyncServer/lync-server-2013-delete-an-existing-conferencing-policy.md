---
title: 'Lync Server 2013: Löschen einer vorhandenen konferenzrichtlinie'
description: 'Lync Server 2013: Löschen einer vorhandenen konferenzrichtlinie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing conferencing policy
ms:assetid: 709ed771-790f-4bf1-a4de-b37ca5168688
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688089(v=OCS.15)
ms:contentKeyID: 49733688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b64e51acc6e6dc91b938244da28057b01957069
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430504"
---
# <a name="delete-an-existing-conferencing-policy-in-lync-server-2013"></a><span data-ttu-id="98b85-103">Löschen einer vorhandenen konferenzrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98b85-103">Delete an existing conferencing policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98b85-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98b85-104">

<span> </span></span></span>

<span data-ttu-id="98b85-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="98b85-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="98b85-106">Führen Sie die folgenden Schritte aus, um eine konferenzrichtlinie auf Benutzerebene oder auf Websiteebene zu löschen.</span><span class="sxs-lookup"><span data-stu-id="98b85-106">Follow these steps to delete a user-level or a site-level conferencing policy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="98b85-107">Sie können die globale konferenzrichtlinie nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="98b85-107">You cannot delete the global conferencing policy.</span></span>



</div>

<div>

## <a name="to-delete-a-site-or-user-conferencing-policy"></a><span data-ttu-id="98b85-108">So löschen Sie eine Website-oder Benutzer konferenzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="98b85-108">To delete a site or user conferencing policy</span></span>

1.  <span data-ttu-id="98b85-109">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="98b85-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="98b85-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="98b85-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="98b85-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="98b85-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="98b85-112">Klicken Sie in der linken Navigationsleiste auf **Konferenzen** , und klicken Sie dann auf **konferenzrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="98b85-112">In the left navigation bar, click **Conferencing** and then click **Conferencing Policy**.</span></span>

4.  <span data-ttu-id="98b85-113">Klicken Sie in der Liste der Konferenzrichtlinien auf die zu löschende Benutzer- oder Standortrichtlinie, klicken Sie auf **Bearbeiten** und dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="98b85-113">In the list of conferencing policies, click the site or user policy that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-conferencing-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="98b85-114">Entfernen von Konferenzrichtlinien mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98b85-114">Removing Conferencing Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="98b85-115">Sie können Konferenzrichtlinien mithilfe der lync Server-Verwaltungsshell und des Cmdlets **Remove-CsConferencingPolicy** löschen.</span><span class="sxs-lookup"><span data-stu-id="98b85-115">You can delete conferencing policies by using Lync Server Management Shell and the **Remove-CsConferencingPolicy** cmdlet.</span></span> <span data-ttu-id="98b85-116">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="98b85-116">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="98b85-117">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="98b85-117">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-conferencing-policy"></a><span data-ttu-id="98b85-118">So entfernen Sie eine bestimmte konferenzrichtlinie</span><span class="sxs-lookup"><span data-stu-id="98b85-118">To remove a specified conferencing policy</span></span>

  - <span data-ttu-id="98b85-119">Mit dem folgenden Befehl wird die Konferenzrichtlinie mit dem Identitätswert "RedmondConferencingPolicy" entfernt:</span><span class="sxs-lookup"><span data-stu-id="98b85-119">The following command removes the conferencing policy with the Identity RedmondConferencingPolicy:</span></span>
    
        Remove-CsConferencingPolicy -Identity "RedmondConferencingPolicy"

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-policies-applied-to-the-per-user-scope"></a><span data-ttu-id="98b85-120">So entfernen Sie alle auf den Benutzerbereich angewendeten Konferenzrichtlinien</span><span class="sxs-lookup"><span data-stu-id="98b85-120">To remove all of the conferencing policies applied to the per-user scope</span></span>

  - <span data-ttu-id="98b85-121">Mit dem folgenden Befehl werden alle im Benutzerbereich konfigurierten Konferenzrichtlinien entfernt:</span><span class="sxs-lookup"><span data-stu-id="98b85-121">The following command removes all the conferencing policies configured at the per-user scope:</span></span>
    
        Get-CsConferencingPolicy -Filter "tag:*" | Remove-CsConferencingPolicy

</div>

<div>

## <a name="to-remove-all-of-the-conferencing-polices-that-allow-recording-by-external-users"></a><span data-ttu-id="98b85-122">So entfernen Sie alle Konferenzrichtlinien, die die Aufzeichnung durch externe Benutzer zulassen</span><span class="sxs-lookup"><span data-stu-id="98b85-122">To remove all of the conferencing polices that allow recording by external users</span></span>

  - <span data-ttu-id="98b85-123">Mit dem folgenden Befehl werden alle Konferenzrichtlinien gelöscht, mit denen externe Benutzer die Konferenz aufzeichnen können:</span><span class="sxs-lookup"><span data-stu-id="98b85-123">The following command deletes any conferencing policies that allow external users to record the conference:</span></span>
    
        Get-CsConferencingPolicy | Where-Object {$_.AllowExternalUsersToRecordMeetings -eq $True} | Remove-CsConferencingPolicy

</div>

<span data-ttu-id="98b85-124">Ausführliche Informationen finden Sie unter [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span><span class="sxs-lookup"><span data-stu-id="98b85-124">For details, see [Remove-CsConferencingPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsConferencingPolicy).</span></span>

<span data-ttu-id="98b85-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98b85-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

