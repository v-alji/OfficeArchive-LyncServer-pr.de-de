---
title: Erstellen oder Ändern einer Sammlung von Konfigurationseinstellungen für Clientversionen
description: Erstellen oder ändern Sie eine Sammlung von Konfigurationseinstellungen für Clientversionen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of client version configuration settings
ms:assetid: 4e6faffd-a36f-40f1-8734-78d84b7df921
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ898477(v=OCS.15)
ms:contentKeyID: 50873757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0082b618b8417c9d0da44599f1606cd238dfd7e8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394758"
---
# <a name="create-or-modify-a-collection-of-client-version-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d8317-103">Erstellen oder Ändern einer Sammlung von Konfigurationseinstellungen für Clientversionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d8317-103">Create or modify a collection of client version configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8317-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8317-104">

<span> </span></span></span>

<span data-ttu-id="d8317-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="d8317-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="d8317-106">Client Version-Konfigurationseinstellungen werden verwendet, um die Client Versionskontrolle zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d8317-106">Client version configuration settings are used to turn client version control on or off.</span></span> <span data-ttu-id="d8317-107">Die Konfiguration der globalen Client Version wird mit lync Server installiert und verwendet, um die Client Versionskontrolle für die gesamte Server Bereitstellung zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d8317-107">The global client version configuration installs with Lync Server and is used to enable or disable client version control for the entire server deployment.</span></span> <span data-ttu-id="d8317-108">Sie können auch Konfigurationseinstellungen für Clientversionen für einzelne Websites konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d8317-108">You can also configure client version configuration settings for individual sites.</span></span> <span data-ttu-id="d8317-109">Sie können die Konfigurationseinstellungen für Clientversionen in der lync Server 2013-Systemsteuerung oder in der lync Server 2013-Verwaltungsshell erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="d8317-109">You can create or modify client version configuration settings from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="d8317-110">Da anonyme Benutzer keinem Benutzer, Standort oder Dienst zugeordnet sind, unterliegen anonyme Benutzer ausschließlich globalen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d8317-110">Because anonymous users are not associated with a user, site, or service, anonymous users are affected by global-level policies only.</span></span>



</div>

<div>

## <a name="to-create-or-modify-client-version-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="d8317-111">So erstellen oder ändern Sie die Konfigurationseinstellungen für Clientversionen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="d8317-111">To create or modify client version configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="d8317-112">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="d8317-112">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="d8317-113">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8317-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d8317-114">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d8317-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d8317-115">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Client Versions Konfiguration** .</span><span class="sxs-lookup"><span data-stu-id="d8317-115">In the left navigation bar, click **Clients**, and then click the **Client Version Configuration** navigation button.</span></span>

4.  <span data-ttu-id="d8317-116">Führen Sie auf der Seite **Client Versions Konfiguration** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="d8317-116">On the **Client Version Configuration** page, do the following:</span></span>
    
      - <span data-ttu-id="d8317-117">Wenn Sie eine neue Konfiguration erstellen möchten, klicken Sie auf **neu**, wählen Sie eine Website aus, klicken Sie auf **OK** Name, und aktualisieren Sie die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="d8317-117">To create a new configuration, click **New**, select a site, click **OK** name, and update the settings.</span></span>
    
      - <span data-ttu-id="d8317-118">Wenn Sie eine Konfiguration ändern möchten, wählen Sie die Konfiguration aus, klicken Sie auf **Bearbeiten**, klicken Sie auf **Details anzeigen**, und nehmen Sie die gewünschten Änderungen an den Einstellungen vor.</span><span class="sxs-lookup"><span data-stu-id="d8317-118">To modify a configuration, select the configuration, click **Edit**, click **Show details**, and make changes to the settings.</span></span>

</div>

<div>

## <a name="creating-or-modifying-client-version-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="d8317-119">Erstellen oder Ändern von Client Versions Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d8317-119">Creating or Modifying Client Version Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="d8317-120">Sie können Konfigurationseinstellungen für Clientversionen mithilfe des Cmdlets **New-CsClientVersionConfiguration** erstellen und mithilfe des Cmdlets " **Satz-CsClientVersionConfiguration** " ändern.</span><span class="sxs-lookup"><span data-stu-id="d8317-120">You can create client version configuration settings by using the **New-CsClientVersionConfiguration** cmdlet, and modify them by using the **Set-CsClientVersionConfiguration** cmdlet.</span></span> <span data-ttu-id="d8317-121">Diese Cmdlets können entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8317-121">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="d8317-122">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="d8317-122">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-new-collection-of-client-version-configuration-settings"></a><span data-ttu-id="d8317-123">So erstellen Sie eine neue Sammlung von Konfigurationseinstellungen für Clientversionen</span><span class="sxs-lookup"><span data-stu-id="d8317-123">To create a new collection of client version configuration settings</span></span>

  - <span data-ttu-id="d8317-124">Mit dem folgenden Befehl wird eine neue Sammlung von Client Versions-Konfigurationseinstellungen erstellt, die auf die Redmond-Website angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="d8317-124">The following command creates a new collection of client version configuration settings applied to the Redmond site.</span></span> <span data-ttu-id="d8317-125">In diesem Beispiel ist die Client Versionsverwaltung für die Redmond-Website deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8317-125">In this example, client versioning is disabled for the Redmond site.</span></span>
    
        New-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $False

</div>

<div>

## <a name="to-enable-client-versioning-for-a-site"></a><span data-ttu-id="d8317-126">So aktivieren Sie die Client Versionsverwaltung für eine Website</span><span class="sxs-lookup"><span data-stu-id="d8317-126">To enable client versioning for a site</span></span>

  - <span data-ttu-id="d8317-127">Mit diesem Befehl wird die Client Versionsverwaltung für die Redmond-Website aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8317-127">This command enables client versioning for the Redmond site.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -Enabled $True

</div>

<div>

## <a name="to-disable-client-versioning-throughout-the-organization"></a><span data-ttu-id="d8317-128">So deaktivieren Sie die Client Versionsverwaltung in der gesamten Organisation</span><span class="sxs-lookup"><span data-stu-id="d8317-128">To disable client versioning throughout the organization</span></span>

  - <span data-ttu-id="d8317-129">In diesem Beispiel ist die Client Versionsverwaltung für alle Konfigurationseinstellungen der Client Version deaktiviert, die in der Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8317-129">In this example, client versioning is disabled for all the client version configuration settings in use in the organization.</span></span>
    
        Get-CsClientVersionConfiguration | Set-CsClientVersionConfiguration  -Enabled $False

</div>

<span data-ttu-id="d8317-130">Ausführliche Informationen finden Sie im Hilfethema zu den Cmdlets [New-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg399029(v=OCS.15)) und [CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg398623(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="d8317-130">For details, see the Help topic for the [New-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg399029(v=OCS.15)) and [Set-CsClientVersionConfiguration](https://technet.microsoft.com/library/Gg398623(v=OCS.15)) cmdlets.</span></span>

<span data-ttu-id="d8317-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8317-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

