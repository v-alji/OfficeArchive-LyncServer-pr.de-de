---
title: 'Lync Server 2013: Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs'
description: 'Lync Server 2013: Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify an unassigned number range
ms:assetid: a102b226-0460-4d5c-82f9-79b8444fa958
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412748(v=OCS.15)
ms:contentKeyID: 48185013
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2998616b931e94c9c38fc44d569b84b3af37709d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431659"
---
# <a name="create-or-modify-an-unassigned-number-range-in-lync-server-2013"></a><span data-ttu-id="2f2c1-103">Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f2c1-103">Create or modify an unassigned number range in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2f2c1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2f2c1-104">

<span> </span></span></span>

<span data-ttu-id="2f2c1-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="2f2c1-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="2f2c1-106">Verwenden Sie eines der folgenden Verfahren, um nicht zugewiesene Nummernbereiche für die Ankündigungs Anwendung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-106">Use one of the following procedures to configure unassigned number ranges for the Announcement application.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="2f2c1-107">Bevor Sie die Tabelle nicht zugewiesene Nummern konfigurieren, müssen Sie bereits eine oder mehrere Ankündigungen definiert haben oder eine automatische UM-Telefonzentrale (Unified Messaging) von Exchange einrichten.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-107">Before you configure the unassigned number table, you must have already defined one or more announcements or set up an Exchange Unified Messaging (UM) Auto Attendant.</span></span>



</div>

<div>

## <a name="to-use-lync-server-control-panel-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="2f2c1-108">So verwenden Sie die lync Server-Systemsteuerung, um nicht zugewiesene Telefonnummern zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2f2c1-108">To use Lync Server Control Panel to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="2f2c1-109">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="2f2c1-110">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="2f2c1-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="2f2c1-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2f2c1-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="2f2c1-113">Klicken Sie in der linken Navigationsleiste auf **VoIP-Funktionen** und klicken Sie dann auf **Nicht zugewiesene Nummer**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-113">In the left navigation bar, click **Voice Features**, and then click **Unassigned Number**.</span></span>

4.  <span data-ttu-id="2f2c1-114">Führen Sie auf der Seite **Nicht zugewiesene Nummer** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-114">On the **Unassigned Number** page, do one of the following:</span></span>
    
      - <span data-ttu-id="2f2c1-p103">Wenn Sie einen neuen Nummernbereich erstellen möchten, klicken Sie auf **Neu**. Geben Sie unter **Name** den Namen für diesen Nummernbereich ein.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-p103">To create a new number range, click **New**. In **Name**, type an identifying name for this range of numbers.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="2f2c1-117">Nachdem Sie den neuen Bereich nicht zugewiesener Nummern per Commit in die Datenbank übernommen haben, können Sie diesen Namen nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-117">After you commit the new unassigned number range to the database, you cannot change this name.</span></span>

        
        </div>
    
      - <span data-ttu-id="2f2c1-p104">Wenn Sie einen vorhandenen Nummernbereich ändern möchten, geben Sie im Suchfeld den gesamten Namen oder einen Teil des Namens für den Nummernbereich ein. Klicken Sie in der Ergebnisliste der Nummernbereiche auf den gewünschten Namen, klicken Sie auf **Bearbeiten** und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-p104">To modify an existing number range, type all or part of the name of the number range in the search field. In the resulting list of number ranges, click the name you want, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="2f2c1-120">Geben Sie im ersten Feld **Nummernbereich** die Startnummer für den Bereich ein und geben Sie dann im zweiten Feld **Nummernbereich** die letzte Nummer für den Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-120">In the first **Number range** field, type the beginning number of the range, and in the second **Number range** field, type the ending number of the range.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="2f2c1-121">Die Startnummer für den Bereich muss kleiner oder gleich der Endnummer sein.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-121">The beginning number of the range must be less than or equal to the ending number of the range.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="2f2c1-122">Wenn die erste Nummer im Bereich oder die letzte Nummer im Bereich eine Durchwahl umfassen, müssen sowohl die erste als auch die letzte Nummer im Bereich einen Durchwahl aufweisen und die Durchwahlnummer muss für die erste und die letzte Nummer übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-122">If the beginning number of the range or the ending number of the range includes an extension number, both the beginning number and the ending number of the range must include an extension, and the extension number must be the same for both the beginning number and the ending number.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="2f2c1-123">Die Nummer muss mit dem regulären Ausdruck (Tel:)? überein \+ Stimmen? [1-9] \d {0,17} (; ext = [1-9] \d {0,9} )?</span><span class="sxs-lookup"><span data-stu-id="2f2c1-123">The number must match the regular expression (tel:)?(\+)?[1-9]\d{0,17}(;ext=[1-9]\d{0,9})?.</span></span> <span data-ttu-id="2f2c1-124">Demnach kann die Nummer mit der Zeichenfolge „tel:“ (wenn Sie diese Zeichenfolge nicht angeben, wird sie automatisch hinzugefügt) sowie einem Pluszeichen (+) und einer Zahl zwischen 1 und 9 beginnen.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-124">This means the number may begin with the string tel: (if you don’t specify that string, it will be automatically added for you), a plus sign (+), and a digit 1 through 9.</span></span> <span data-ttu-id="2f2c1-125">Die Telefonnummer kann bis zu 17 Zeichen umfassen, gefolgt von einer Durchwahl im Format „;ext=“ plus der Durchwahlnummer.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-125">The phone number can be up to 17 digits and may be followed by an extension in the format ;ext= followed by the extension number.</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="2f2c1-126">Führen Sie im Abschnitt **Ansagedienst** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-126">In **Announcement service**, do one of the following:</span></span>
    
      - <span data-ttu-id="2f2c1-127">Klicken Sie auf **Ansage**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-127">Click **Announcement**.</span></span>
    
      - <span data-ttu-id="2f2c1-128">Klicken Sie auf **Exchange UM**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-128">Click **Exchange UM**.</span></span>

7.  <span data-ttu-id="2f2c1-129">Wenn Sie im vorherigen Schritt auf **Ansage** geklickt haben, führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-129">If, in the previous step, you clicked **Announcement**, do the following:</span></span>
    
    1.  <span data-ttu-id="2f2c1-130">Klicken Sie unter **FQDN des Zielservers** auf **auswählen**, klicken Sie auf die Dienst-ID des Anwendungsdiensts, der die Ankündigungs Anwendung ausführt, die eingehende Anrufe an diesen Bereich nicht zugewiesener Nummern abwickeln soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-130">Under **FQDN of destination server**, click **Select**, click the service ID of the Application service that runs the Announcement application that will handle incoming calls to this range of unassigned numbers, and then click **OK**.</span></span>
    
    2.  <span data-ttu-id="2f2c1-131">Klicken Sie im Abschnitt **Ansage** auf die Ansage, die für diesen Bereich nicht zugewiesener Nummern wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-131">In **Announcement**, click the announcement to be played for this range of unassigned numbers.</span></span>

8.  <span data-ttu-id="2f2c1-132">Wenn Sie im vorherigen Schritt auf **Exchange UM** geklickt haben, klicken Sie unter **Nummer der automatischen Telefonzentrale** auf **Auswählen**, klicken Sie auf die für diesen Bereich nicht zugewiesener Nummern zu verwendende Telefonnummer und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-132">If, in the previous step, you clicked **Exchange UM**, under **Auto Attendant phone number**, click **Select**, click the phone number to be used for this range of unassigned numbers, and then click **OK**.</span></span>

9.  <span data-ttu-id="2f2c1-133">Klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-133">Click **OK**.</span></span>

10. <span data-ttu-id="2f2c1-p106">Stellen Sie sicher, dass die Bereiche nicht zugewiesener Nummern auf der Seite **Nicht zugewiesene Nummer** in der gewünschten Reihenfolge angezeigt werden. Wenn Sie die Position eines Bereichs in der Tabelle ändern möchten, klicken Sie auf einen oder mehrere aufeinanderfolgende Namen in der Liste der Bereiche und klicken Sie anschließend auf den Aufwärts- oder Abwärtspfeil.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-p106">On the **Unassigned Number** page, be sure that the unassigned number ranges are arranged in the order that you want. To change a range's position in the table, click one or more consecutive names in the list of ranges, and then click the up arrow or the down arrow.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="2f2c1-136">Lync Server durchsucht die Tabelle nicht zugewiesene Nummern von oben nach unten und verwendet den ersten Bereich, der der nicht zugewiesenen Zahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-136">Lync Server searches the unassigned number table from top to bottom and uses the first range that matches the unassigned number.</span></span> <span data-ttu-id="2f2c1-137">Wenn sich Bereiche überlappen und auf einen Bereich als letzte Aktion zurückgegriffen werden soll, stellen Sie sicher, dass sich dieser Bereich ganz unten in der Liste befindet.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-137">If you have overlapping ranges and one range specifies a last resort action, make sure that range is at the bottom of the list.</span></span>

    
    </div>

11. <span data-ttu-id="2f2c1-138">Wenn Sie die Bereiche nicht zugewiesener Nummern in der gewünschten Reihenfolge angeordnet haben, klicken Sie auf **Commit für alle**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-138">When you have the unassigned number ranges in the order that you want, click **Commit all**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-configure-unassigned-phone-numbers"></a><span data-ttu-id="2f2c1-139">So verwenden Sie Windows PowerShell zum Konfigurieren von nicht zugewiesenen Telefonnummern</span><span class="sxs-lookup"><span data-stu-id="2f2c1-139">To use Windows PowerShell to configure unassigned phone numbers</span></span>

1.  <span data-ttu-id="2f2c1-140">Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe oder mit den erforderlichen Benutzerrechten installiert ist, wie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-140">Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="2f2c1-141">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-141">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="2f2c1-142">Verwenden Sie **New-CsUnassignedNumber** zum Erstellen eines neuen Bereichs nicht zugewiesener Nummern.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-142">Use **New-CsUnassignedNumber** to create a new unassigned number range.</span></span> <span data-ttu-id="2f2c1-143">Verwenden Sie **Set-CsUnassignedNumber** zum Ändern eines vorhandenen Bereichs nicht zugewiesener Nummern.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-143">Use **Set-CsUnassignedNumber** to modify an existing unassigned number range.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="2f2c1-p109">Wenn sich Bereiche überlappen und die Bereiche in einer bestimmten Reihenfolge angewendet werden sollen, fügen Sie den Parameter „Priority“ ein. Daraufhin wird der Bereich mit der höchsten Priorität für den Anruf angewendet.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-p109">If you have overlapping ranges and want the ranges to be applied in a specific order, include the Priority parameter. The range with the highest priority will be applied to the call.</span></span>

    
    </div>
    
    <span data-ttu-id="2f2c1-146">Führen Sie in der Befehlszeile eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-146">At the command line, do one of the following:</span></span>
    
      - <span data-ttu-id="2f2c1-147">Führen Sie zum Erstellen eines Nummernbereichs für einen Ankündigungsdienst Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-147">To create a number range for an Announcement service, run:</span></span>
        
            New-CsUnassignedNumber -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range> -AnnouncementName <announcement name> -AnnouncementService <FQDN or service ID of the Announcement service>
    
      - <span data-ttu-id="2f2c1-148">Oder führen Sie zum Erstellen eines Nummernbereichs für die automatische Exchange UM-Telefonzentrale Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-148">Or, to create a number range for Exchange UM Auto Attendant, run:</span></span>
        
            New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber <phone number> -Identity <unique identifier for unassigned number range> -NumberRangeStart <first number in range> -NumberRangeEnd <last number in range>
    
    <span data-ttu-id="2f2c1-149">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-149">For example:</span></span>
    
        New-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100" -AnnouncementName "Welcome Announcement" -AnnouncementService ApplicationServer:Redmond.contoso.com
    
    <span data-ttu-id="2f2c1-150">Oder</span><span class="sxs-lookup"><span data-stu-id="2f2c1-150">Or</span></span>
    
        New-CsUnassignedNumber -ExUmAutoAttendantPhoneNumber "+12065551234" -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551100"
    
    <span data-ttu-id="2f2c1-151">Im folgenden Beispiel wird veranschaulicht, wie Sie die Nummern in einem vorhandenen Bereich nicht zugewiesener Nummern ändern:</span><span class="sxs-lookup"><span data-stu-id="2f2c1-151">The following example shows how to modify the numbers in an existing unassigned number range:</span></span>
    
        Set-CsUnassignedNumber -Identity "Unassigned range 1" -NumberRangeStart "+14255551000" -NumberRangeEnd "+14255551900"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2f2c1-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f2c1-152">See Also</span></span>


[<span data-ttu-id="2f2c1-153">Löschen eines nicht zugewiesenen Nummernbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f2c1-153">Delete an unassigned number range in Lync Server 2013</span></span>](lync-server-2013-delete-an-unassigned-number-range.md)  


[<span data-ttu-id="2f2c1-154">New-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="2f2c1-154">New-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUnassignedNumber)  
[<span data-ttu-id="2f2c1-155">Set-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="2f2c1-155">Set-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUnassignedNumber)  
[<span data-ttu-id="2f2c1-156">Get-CsUnassignedNumber</span><span class="sxs-lookup"><span data-stu-id="2f2c1-156">Get-CsUnassignedNumber</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUnassignedNumber)  
  

<span data-ttu-id="2f2c1-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2f2c1-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

