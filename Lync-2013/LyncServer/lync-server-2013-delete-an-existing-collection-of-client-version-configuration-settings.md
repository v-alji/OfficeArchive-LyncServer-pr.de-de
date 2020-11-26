---
title: Löschen einer vorhandenen Sammlung von Konfigurationseinstellungen für Clientversionen
description: Löschen Sie eine vorhandene Sammlung von Konfigurationseinstellungen für Clientversionen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of client version configuration settings
ms:assetid: 70bf1216-d0d2-45ce-881f-b8edadf3cec7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898480(v=OCS.15)
ms:contentKeyID: 50873760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25a7d384bdfd84a1a6e04041988c16788a116626
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430567"
---
# <a name="delete-an-existing-collection-of-client-version-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="5a53d-103">Löschen einer vorhandenen Sammlung von Konfigurationseinstellungen für Clientversionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5a53d-103">Delete an existing collection of client version configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5a53d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5a53d-104">

<span> </span></span></span>

<span data-ttu-id="5a53d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="5a53d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="5a53d-106">Wenn Sie die Clientkonfigurationseinstellungen entfernen möchten, die zuvor für eine Website konfiguriert wurden, können Sie die Einstellungen aus der lync Server 2013-Systemsteuerung oder der lync Server 2013-Verwaltungsshell entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a53d-106">If you want to remove the client configuration settings that have been previously configured for a site, you can remove the settings from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-remove-client-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="5a53d-107">So entfernen Sie Clientkonfigurationseinstellungen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="5a53d-107">To remove client configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="5a53d-108">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="5a53d-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5a53d-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5a53d-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5a53d-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5a53d-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5a53d-111">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Client Versions Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="5a53d-111">In the left navigation bar, click **Clients**, and then click the **Client Version Configuration** navigation button.</span></span>

4.  <span data-ttu-id="5a53d-112">Wählen Sie die Website aus, klicken Sie auf **Bearbeiten**, klicken Sie auf **Löschen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a53d-112">Select the site, click **Edit**, click **Delete**, and then click **OK**.</span></span>

</div>

<div>

## <a name="removing-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="5a53d-113">Entfernen von Client Versions Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5a53d-113">Removing Client Version Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="5a53d-114">Mithilfe des Cmdlets **Remove-CsClientVersionConfiguration** können Sie Konfigurationseinstellungen für Clientversionen löschen.</span><span class="sxs-lookup"><span data-stu-id="5a53d-114">You can delete client version configuration settings by using the **Remove-CsClientVersionConfiguration** cmdlet.</span></span> <span data-ttu-id="5a53d-115">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a53d-115">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="5a53d-116">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="5a53d-116">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-client-version-configuration-settings"></a><span data-ttu-id="5a53d-117">So entfernen Sie eine angegebene Sammlung von Konfigurationseinstellungen für Clientversionen</span><span class="sxs-lookup"><span data-stu-id="5a53d-117">To remove a specified collection of client version configuration settings</span></span>

  - <span data-ttu-id="5a53d-118">Mit dem folgenden Befehl werden die auf die Redmond-Website angewendeten Konfigurationseinstellungen für Clientversionen entfernt:</span><span class="sxs-lookup"><span data-stu-id="5a53d-118">The following command removes the client version configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsClientVersionConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-client-version-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="5a53d-119">So entfernen Sie alle auf den Website Bereich angewendeten Konfigurationseinstellungen für Clientversionen</span><span class="sxs-lookup"><span data-stu-id="5a53d-119">To remove all the client version configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="5a53d-120">Mit diesem Befehl werden alle Konfigurationseinstellungen für Clientversionen entfernt, die für den Website Bereich konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="5a53d-120">This command removes all the client version configuration settings configured at the site scope:</span></span>
    
        Get-CsClientVersionConfiguration -Filter site:* | Remove-CsClientVersionConfiguration

</div>

<div>

## <a name="to-remove-all-the-client-version-configuration-settings-based-on-the-value-of-the-defaultaction-property"></a><span data-ttu-id="5a53d-121">So entfernen Sie alle Konfigurationseinstellungen für Clientversionen basierend auf dem Wert der standardmäßigen Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5a53d-121">To remove all the client version configuration settings based on the value of the DefaultAction property</span></span>

  - <span data-ttu-id="5a53d-122">Und dieser Befehl entfernt alle Konfigurationseinstellungen für Clientversionen, bei denen die Standardaktion auf "blockieren" gesetzt wurde:</span><span class="sxs-lookup"><span data-stu-id="5a53d-122">And this command removes all the client version configuration settings where the default action has been set to "Block":</span></span>
    
        Get-CsClientVersionConfiguration | Where-Object {$_.DefaultAction -eq "Block" | Remove-CsClientVersionConfiguration

</div>

<span data-ttu-id="5a53d-123">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg425925(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="5a53d-123">For details, see the Help topic for the [Remove-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg425925(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="5a53d-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5a53d-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

