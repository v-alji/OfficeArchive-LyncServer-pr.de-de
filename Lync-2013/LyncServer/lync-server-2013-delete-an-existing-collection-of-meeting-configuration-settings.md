---
title: Löschen einer vorhandenen Sammlung von Konfigurationseinstellungen für Besprechungen
description: Löschen Sie eine vorhandene Sammlung von Einstellungen für die besprechungskonfiguration.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of meeting configuration settings
ms:assetid: 92ff8a91-05c5-4047-a533-5dff12f22299
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688136(v=OCS.15)
ms:contentKeyID: 49733736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc0985023a1459130c7d589327535436145a0ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430532"
---
# <a name="delete-an-existing-collection-of-meeting-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="fc933-103">Löschen einer vorhandenen Sammlung von Besprechungs Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc933-103">Delete an existing collection of meeting configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc933-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc933-104">

<span> </span></span></span>

<span data-ttu-id="fc933-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="fc933-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="fc933-106">Sie können eine Website-oder Benutzerkonfiguration löschen.</span><span class="sxs-lookup"><span data-stu-id="fc933-106">You can delete a site or user configuration.</span></span> <span data-ttu-id="fc933-107">Die globale Konfiguration kann nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="fc933-107">The global configuration cannot be removed.</span></span> <span data-ttu-id="fc933-108">Wenn Sie die globale Konfiguration löschen, wird sie automatisch auf die Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fc933-108">If you delete the global configuration, it is automatically reset to the default values.</span></span>

<div>

## <a name="to-delete-a-site-or-user-meeting-configuration"></a><span data-ttu-id="fc933-109">So löschen Sie eine Website-oder Benutzer besprechungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="fc933-109">To delete a site or user meeting configuration</span></span>

1.  <span data-ttu-id="fc933-110">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fc933-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fc933-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc933-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fc933-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fc933-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fc933-113">Klicken Sie in der linken Navigationsleiste auf **Konferenzen** , und klicken Sie dann auf **besprechungskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="fc933-113">In the left navigation bar, click **Conferencing** and then click **Meeting Configuration**.</span></span>

4.  <span data-ttu-id="fc933-114">Klicken Sie in der Liste der Besprechungskonfigurationen auf die Standort- oder Poolkonfiguration, die Sie löschen möchten, klicken Sie dann auf **Bearbeiten** und anschließend auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="fc933-114">In the list of meeting configurations, click the site or pool configuration that you want to delete, click **Edit**, and then click **Delete**.</span></span>

</div>

<div>

## <a name="removing-meeting-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fc933-115">Entfernen von Besprechungs Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc933-115">Removing Meeting Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fc933-116">Besprechungseinstellungen können mithilfe von Windows PowerShell und dem Cmdlet Remove-CsMeetingConfiguration gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fc933-116">Meeting settings can be deleted by using Windows PowerShell and the Remove-CsMeetingConfiguration cmdlet.</span></span> <span data-ttu-id="fc933-117">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fc933-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fc933-118">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fc933-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-meeting-configuration-settings"></a><span data-ttu-id="fc933-119">So entfernen Sie eine bestimmte Sammlung von Besprechungs Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fc933-119">To remove a specified collection of meeting configuration settings</span></span>

  - <span data-ttu-id="fc933-120">Mit diesem Befehl werden die auf die Redmond-Website angewendeten Besprechungs Konfigurationseinstellungen entfernt:</span><span class="sxs-lookup"><span data-stu-id="fc933-120">This command removes the meeting configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsMeetingConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="fc933-121">So entfernen Sie alle auf den Website Bereich angewendeten Besprechungs Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fc933-121">To remove all the meeting configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="fc933-122">Mit diesem Befehl werden alle auf den Website Bereich angewendeten Besprechungs Konfigurationseinstellungen entfernt:</span><span class="sxs-lookup"><span data-stu-id="fc933-122">This command removes all the meeting configuration settings applied to the site scope:</span></span>
    
        Get-CsMeetingConfiguration -Filter "site:*" | Remove-CsMeetingConfiguration

</div>

<div>

## <a name="to-remove-all-the-meeting-configuration-settings-that-admit-anonymous-users-by-default"></a><span data-ttu-id="fc933-123">So entfernen Sie alle Einstellungen für die besprechungskonfiguration, die standardmäßig anonyme Benutzer zulassen</span><span class="sxs-lookup"><span data-stu-id="fc933-123">To remove all the meeting configuration settings that admit anonymous users by default</span></span>

  - <span data-ttu-id="fc933-124">Und dieser entfernt alle Einstellungen, mit denen anonyme Benutzer standardmäßig zugelassen werden können:</span><span class="sxs-lookup"><span data-stu-id="fc933-124">And this one removes all the settings that allow anonymous users to be admitted by default:</span></span>
    
        Get-CsMeetingConfiguration | Where-Object {$_.AdmitAnonymousUsersByDefault -eq $True} | Remove-CsMeetingConfiguration

</div>

<span data-ttu-id="fc933-125">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="fc933-125">For more information, see the help topic for the [Remove-CsMeetingConfiguration](https://technet.microsoft.com/library/Gg412775(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="fc933-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc933-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

