---
title: 'Lync Server 2013: Erstellen von Standortrichtlinien'
description: 'Lync Server 2013: Erstellen von Standortrichtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create location policies
ms:assetid: f1878194-c756-4794-8fa1-15dd2118b4b3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413006(v=OCS.15)
ms:contentKeyID: 48185794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 464ea9893890ab6185f180434e2dad13818123d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431932"
---
# <a name="create-location-policies-in-lync-server-2013"></a><span data-ttu-id="ffdd5-103">Erstellen von Standortrichtlinien in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ffdd5-103">Create location policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffdd5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffdd5-104">

<span> </span></span></span>

<span data-ttu-id="ffdd5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="ffdd5-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="ffdd5-106">Lync Server verwendet eine ortungsrichtlinie, um lync-Clients für E9-1-1 während der Clientregistrierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-106">Lync Server uses a location policy to enable Lync clients for E9-1-1 during client registration.</span></span> <span data-ttu-id="ffdd5-107">Eine Standortrichtlinie enthält die Einstellungen für die Definition der Notrufdienstimplementierung.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-107">A location policy contains the settings that define how E9-1-1 will be implemented.</span></span>

<span data-ttu-id="ffdd5-p102">Sie können die globale Standortrichtlinie bearbeiten und bereichsspezifische Standortrichtlinien erstellen. Ein Client, der sich nicht in einem Subnetz mit zugeordneter Standortrichtlinie befindet oder dem nicht direkt eine Standortrichtlinie zugeordnet wurde, ruft eine globale Richtlinie ab. Bereichsspezifische Standortrichtlinien werden Subnetzen oder Benutzern zugewiesen.  </span><span class="sxs-lookup"><span data-stu-id="ffdd5-p102">You can edit the global location policy and create new tagged location policies. A client obtains a global policy when it is not located within a subnet with an associated location policy, or when the client has not been directly assigned a location policy. Tagged policies are assigned to subnets or users.</span></span>

<span data-ttu-id="ffdd5-111">Zum Erstellen einer Standortrichtlinie müssen Sie ein Konto verwenden, das Mitglied der Gruppe „RTCUniversalServerAdmins“ oder der Administratorrolle „CsVoiceAdministrator“ ist oder entsprechende Administratorrechte und -berechtigungen besitzt.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-111">To create a location policy, you must use an account that is a member of the RTCUniversalServerAdmins group, or is a member of the CsVoiceAdministrator administrative role, or has equivalent administrator rights and permissions.</span></span>

<span data-ttu-id="ffdd5-112">Eine vollständige Beschreibung der Standortrichtlinien finden Sie unter [Definieren der Standortrichtlinie für lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="ffdd5-112">For a complete description of Location policies, see [Defining the location policy for Lync Server 2013](lync-server-2013-defining-the-location-policy.md).</span></span> <span data-ttu-id="ffdd5-113">Cmdlets in diesem Verfahren verwenden eine Standortrichtlinie, die mit den folgenden Werten definiert ist:</span><span class="sxs-lookup"><span data-stu-id="ffdd5-113">Cmdlets in this procedure use a location policy defined using the following values:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffdd5-114">Element</span><span class="sxs-lookup"><span data-stu-id="ffdd5-114">Element</span></span></th>
<th><span data-ttu-id="ffdd5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ffdd5-115">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-116">EnhancedEmergencyServicesEnabled</span><span class="sxs-lookup"><span data-stu-id="ffdd5-116">EnhancedEmergencyServicesEnabled</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-117"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-117"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffdd5-118">LocationRequired</span><span class="sxs-lookup"><span data-stu-id="ffdd5-118">LocationRequired</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-119"><strong>Haftungsausschluss</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-119"><strong>Disclaimer</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-120">EnhancedEmergencyServiceDisclaimer</span><span class="sxs-lookup"><span data-stu-id="ffdd5-120">EnhancedEmergencyServiceDisclaimer</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-p104">Die Unternehmensrichtlinie erfordert, dass Sie einen Standort festlegen. Wenn Sie keinen Standort festlegen, können Sie im Ernstfall nicht von Notfalldiensten lokalisiert werden. Bitte legen Sie einen Standort fest.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-p104">Your company policy requires you to set a location. If you do not set a location, emergency services will not be able to locate you in an emergency. Please set a location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffdd5-124">UseLocationForE911Only</span><span class="sxs-lookup"><span data-stu-id="ffdd5-124">UseLocationForE911Only</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-125"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-125"><strong>False</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-126">PstnUsage</span><span class="sxs-lookup"><span data-stu-id="ffdd5-126">PstnUsage</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-127"><strong>EmergencyUsage</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-127"><strong>EmergencyUsage</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffdd5-128">EmergencyDialString</span><span class="sxs-lookup"><span data-stu-id="ffdd5-128">EmergencyDialString</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-129"><strong>911</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-129"><strong>911</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-130">EmergencyDialMask</span><span class="sxs-lookup"><span data-stu-id="ffdd5-130">EmergencyDialMask</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-131"><strong>112</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-131"><strong>112</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffdd5-132">NotificationUri</span><span class="sxs-lookup"><span data-stu-id="ffdd5-132">NotificationUri</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-133"><strong>sip:security@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-133"><strong>sip:security@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-134">ConferenceUri</span><span class="sxs-lookup"><span data-stu-id="ffdd5-134">ConferenceUri</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-135"><strong>sip:+14255550123@litwareinc.com</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-135"><strong>sip:+14255550123@litwareinc.com</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffdd5-136">ConferenceMode</span><span class="sxs-lookup"><span data-stu-id="ffdd5-136">ConferenceMode</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-137"><strong>twoway</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-137"><strong>twoway</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffdd5-138">LocationRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="ffdd5-138">LocationRefreshInterval</span></span></p></td>
<td><p><span data-ttu-id="ffdd5-139"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="ffdd5-139"><strong>2</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ffdd5-140">Details zum Arbeiten mit Standortrichtlinien finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="ffdd5-140">For details about working with location policies, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="ffdd5-141">New-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ffdd5-141">New-CsLocationPolicy</span></span>

  - <span data-ttu-id="ffdd5-142">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ffdd5-142">Get-CsLocationPolicy</span></span>

  - <span data-ttu-id="ffdd5-143">Set-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ffdd5-143">Set-CsLocationPolicy</span></span>

  - <span data-ttu-id="ffdd5-144">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ffdd5-144">Remove-CsLocationPolicy</span></span>

  - <span data-ttu-id="ffdd5-145">Grant-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ffdd5-145">Grant-CsLocationPolicy</span></span>

<div>

## <a name="to-create-location-policies"></a><span data-ttu-id="ffdd5-146">So erstellen Sie Standortrichtlinien</span><span class="sxs-lookup"><span data-stu-id="ffdd5-146">To create location policies</span></span>

1.  <span data-ttu-id="ffdd5-147">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ffdd5-148">Bei Ausführung von „CsLocationPolicy“ tritt ein Fehler auf, wenn sich die Einstellung für <STRONG>PstnUsage</STRONG> nicht bereits in der globalen Liste „PstnUsages“ befindet.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-148">CsLocationPolicy will fail if the setting for <STRONG>PstnUsage</STRONG> is not already in the Global list of PstnUsages.</span></span>

    
    </div>

2.  <span data-ttu-id="ffdd5-149">Optional können Sie auch das folgende Cmdlet ausführen, um die globale Standortrichtlinie zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="ffdd5-149">Optionally, run the following cmdlet to edit the global Location Policy:</span></span>
    
        Set-CsLocationPolicy -Identity Global -EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -PstnUsage "emergencyUsage" -EmergencyDialString "911" -ConferenceMode "twoway" -ConferenceUri "sip:+14255550123@litwareinc.com" -EmergencyDialMask "112" NotificationUri "sip:security@litwareinc.com" -UseLocationForE911Only $true -LocationRefreshInterval 2

3.  <span data-ttu-id="ffdd5-150">Führen Sie folgendes Cmdlet aus, um eine bereichsspezifische Standortrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-150">Run the following to create a tagged Location Policy.</span></span>
    
        New-CsLocationPolicy -Identity Tag:Redmond - EnhancedEmergencyServicesEnabled $true -LocationRequired "disclaimer" -EnhancedEmergencyServiceDisclaimer "Your company policy requires you to set a location. If you do not set a location emergency services will not be able to locate you in an emergency. Please set a location." -UseLocationForE911Only $false -PstnUsage "EmergencyUsage" -EmergencyDialString "911" -EmergencyDialMask "112" -NotificationUri "sip:security@litwareinc.com" -ConferenceUri "sip:+14255550123@litwareinc.com" -ConferenceMode "twoway" -LocationRefreshInterval 2

4.  <span data-ttu-id="ffdd5-151">Führen Sie das folgende Cmdlet aus, um die in Schritt 3 erstellte bereichsspezifische Standortrichtlinie auf eine Benutzerrichtlinie anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="ffdd5-151">Run the following cmdlet to apply the tagged Location Policy created in step 3 to a user policy.</span></span>
    
        (Get-CsUser | where { $_.Name -match "UserName" }) | Grant-CsLocationPolicy -PolicyName Redmond

<span data-ttu-id="ffdd5-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffdd5-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

