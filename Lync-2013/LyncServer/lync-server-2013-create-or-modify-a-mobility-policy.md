---
title: 'Lync Server 2013: Erstellen oder Ändern einer Mobilitätsrichtlinie'
description: 'Lync Server 2013: Erstellen oder Ändern einer Mobilitätsrichtlinie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a mobility policy
ms:assetid: fc2dfea0-2215-440d-9f4b-7c985da29211
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721946(v=OCS.15)
ms:contentKeyID: 49733884
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcf593c568a8ecf1bd6791641affc4076672b250
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431799"
---
# <a name="create-or-modify-a-mobility-policy-in-lync-server-2013"></a><span data-ttu-id="618e6-103">Erstellen oder Ändern einer Mobilitätsrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="618e6-103">Create or modify a mobility policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="618e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="618e6-104">

<span> </span></span></span>

<span data-ttu-id="618e6-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="618e6-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="618e6-106">Sie können mobilitätsrichtlinien erstellen oder ändern, um mobilen Benutzern die Verwendung unterstützter mobiler Geräte für lync-Funktionen wie Instant Messaging (im), Anwesenheitsinformationen und Kontakte zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="618e6-106">You can create or modify mobility policy to allow mobile users to use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span> <span data-ttu-id="618e6-107">Sie können mobilitätsrichtlinien in der lync Server 2013-Systemsteuerung oder in der lync Server 2013-Verwaltungsshell erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="618e6-107">You can create or modify mobility policies from Lync Server 2013 Control Panel or Lync Server 2013 Management Shell</span></span>

<div>

## <a name="to-create-a-mobility-policy-with-lync-server-control-panel"></a><span data-ttu-id="618e6-108">So erstellen Sie eine Mobilitätsrichtlinie mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="618e6-108">To create a mobility policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="618e6-109">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="618e6-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="618e6-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="618e6-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="618e6-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="618e6-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="618e6-112">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Mobilitätsrichtlinie** .</span><span class="sxs-lookup"><span data-stu-id="618e6-112">In the left navigation bar, click **Clients**, and then click the **Mobility Policy** navigation button.</span></span>

4.  <span data-ttu-id="618e6-113">Klicken Sie auf der Seite **Mobilitätsrichtlinie** auf **neu**, und führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="618e6-113">On the **Mobility Policy** page, click **New**, and do one of the following:</span></span>
    
    1.  <span data-ttu-id="618e6-114">Wenn Sie eine Website Mobilitätsrichtlinie erstellen möchten, klicken Sie auf **Website Richtlinie**, klicken Sie auf eine Website, klicken Sie auf **OK**, überprüfen Sie die Standardeinstellungen, und nehmen Sie bei Bedarf alle gewünschten Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="618e6-114">To create a site mobility policy, click **Site policy**, click a site, click **OK**, review the default settings, and, if you want to, make any changes.</span></span>
    
    2.  <span data-ttu-id="618e6-115">Wenn Sie eine Benutzer Mobilitätsrichtlinie erstellen möchten, klicken Sie auf **Benutzerrichtlinie**, geben Sie einen Namen ein, überprüfen Sie die Standardeinstellungen, und nehmen Sie bei Bedarf Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="618e6-115">To create a user mobility policy, click **User policy**, type a name, review the default settings, and if you want to, make any changes.</span></span>

5.  <span data-ttu-id="618e6-116">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="618e6-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-mobility-policy-with-lync-server-control-panel"></a><span data-ttu-id="618e6-117">So ändern Sie eine Mobilitätsrichtlinie mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="618e6-117">To modify a mobility policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="618e6-118">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="618e6-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="618e6-119">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="618e6-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="618e6-120">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="618e6-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="618e6-121">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Mobilitätsrichtlinie** .</span><span class="sxs-lookup"><span data-stu-id="618e6-121">In the left navigation bar, click **Clients**, and then click the **Mobility Policy** navigation button.</span></span>

4.  <span data-ttu-id="618e6-122">Klicken Sie auf der Seite **Mobilitätsrichtlinie** auf eine der vorhandenen mobilitätsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="618e6-122">On the **Mobility Policy** page, click one of the existing mobility policies.</span></span>

5.  <span data-ttu-id="618e6-123">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="618e6-123">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="618e6-124">Bearbeiten Sie alle Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="618e6-124">Edit any of the settings.</span></span>

7.  <span data-ttu-id="618e6-125">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="618e6-125">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-external-access-policies-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="618e6-126">Erstellen von Richtlinien für den externen Zugriff mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="618e6-126">Creating External Access Policies by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="618e6-127">Mit Windows PowerShell und dem Cmdlet **New-CsMobilityPolicy** können Sie mobilitätsrichtlinien (im Bereich "Website" oder "pro Benutzer") erstellen.</span><span class="sxs-lookup"><span data-stu-id="618e6-127">You can create mobility policies (at the site scope or the per-user scope) by using Windows PowerShell and the **New-CsMobilityPolicy** cmdlet.</span></span> <span data-ttu-id="618e6-128">Darüber hinaus können Sie das Cmdlet " **Satz-CsMobilityPolicy** " verwenden, um Ihre vorhandenen Richtlinien einschließlich der globalen Richtlinie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="618e6-128">Additionally, you can use the **Set-CsMobilityPolicy** cmdlet to modify any of your existing policies, including the global policy.</span></span> <span data-ttu-id="618e6-129">Diese Cmdlets können entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="618e6-129">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="618e6-130">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="618e6-130">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-a-mobility-policy-at-the-site-scope"></a><span data-ttu-id="618e6-131">So erstellen Sie eine Mobilitätsrichtlinie im Website Bereich</span><span class="sxs-lookup"><span data-stu-id="618e6-131">To create a mobility policy at the site scope</span></span>

  - <span data-ttu-id="618e6-132">Mit diesem Befehl wird eine neue Mobilitätsrichtlinie für die Website "Redmond" erstellt:</span><span class="sxs-lookup"><span data-stu-id="618e6-132">This command creates a new mobility policy for the Redmond site:</span></span>
    
        New-CsMobilityPolicy -Identity "site:Redmond"
    
    <span data-ttu-id="618e6-133">Da im vorhergehenden Befehl keine Parameter (mit Ausnahme des Parameters zur obligatorischen Identität) angegeben wurden, verwenden die Richtlinien die Standardwerte für alle zugehörigen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="618e6-133">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the policies will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-create-a-mobility-policy-at-the-per-user-scope"></a><span data-ttu-id="618e6-134">So erstellen Sie eine Mobilitätsrichtlinie für einzelne Benutzer</span><span class="sxs-lookup"><span data-stu-id="618e6-134">To create a mobility policy at the per-user scope</span></span>

  - <span data-ttu-id="618e6-135">Wenn Sie eine Mobilitätsrichtlinie für den Benutzerbereich erstellen möchten, geben Sie eine eindeutige Identität für die Richtlinie an:</span><span class="sxs-lookup"><span data-stu-id="618e6-135">To create a mobility policy at the per-user scope, specify a unique Identity for the policy:</span></span>
    
        New-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-a-mobility-policy"></a><span data-ttu-id="618e6-136">So ändern Sie einen einzelnen Eigenschaftswert beim Erstellen einer Mobilitätsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="618e6-136">To change a single property value when creating a mobility policy</span></span>

  - <span data-ttu-id="618e6-137">Zum Erstellen von Richtlinien, die unterschiedliche Eigenschaftswerte verwenden, schließen Sie den entsprechenden Parameter-und Parameterwert ein.</span><span class="sxs-lookup"><span data-stu-id="618e6-137">To create policies that use different property values, include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="618e6-138">Mit diesem Befehl wird beispielsweise eine Mobilitätsrichtlinie erstellt, die den Anruf über die Arbeit deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="618e6-138">For example, this command creates mobility policy that disables Call via Work:</span></span>
    
        New-CsMobilityPolicy -Identity "site:Redmond" -EnableOutsideVoice $False

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-a-mobility-policy"></a><span data-ttu-id="618e6-139">So ändern Sie beim Erstellen einer Mobilitätsrichtlinie mehrere Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="618e6-139">To change multiple property values when creating a mobility policy</span></span>

  - <span data-ttu-id="618e6-140">Mehrere Eigenschaftswerte können geändert werden, indem Sie mehrere Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="618e6-140">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="618e6-141">Mit diesem Befehl wird beispielsweise eine Richtlinie erstellt, die sowohl Mobilität als auch Anruf über die Arbeit deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="618e6-141">For example, this command creates a policy that disables both mobility and Call via Work:</span></span>
    
        New-CsMobilityPolicy "site:Redmond" -EnableMobility $False -EnableOutsideVoice $False

</div>

<span data-ttu-id="618e6-142">Ausführliche Informationen finden Sie im Hilfethema zu den Cmdlets [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy) und [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy) .</span><span class="sxs-lookup"><span data-stu-id="618e6-142">For details, see the Help topic for the [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy) and the [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy) cmdlets.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="618e6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="618e6-143">See Also</span></span>


[<span data-ttu-id="618e6-144">Konfigurieren der Mobilitätsrichtlinie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="618e6-144">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)  
  

<span data-ttu-id="618e6-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="618e6-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

