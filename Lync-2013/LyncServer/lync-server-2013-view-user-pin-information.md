---
title: 'Lync Server 2013: Benutzer-PIN-Informationen anzeigen'
description: 'Lync Server 2013: Benutzer-PIN-Informationen anzeigen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View user PIN information
ms:assetid: 59e38117-8112-4851-82ac-a746ffa0f89d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688067(v=OCS.15)
ms:contentKeyID: 49733661
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 56f0808e645a2589841ff70d4923fa2de2c020ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444021"
---
# <a name="view-user-pin-information-in-lync-server-2013"></a><span data-ttu-id="40e72-103">Anzeigen von Benutzer-PIN-Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40e72-103">View user PIN information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40e72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40e72-104">

<span> </span></span></span>

<span data-ttu-id="40e72-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="40e72-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="40e72-106">Um an einer Einwahlkonferenz als authentifizierter Benutzer teilzunehmen, erfordert ein lync Server 2013-Benutzer mit den Active Directory-Domänendiensten (AD DS) eine persönliche Identifikationsnummer (PIN).</span><span class="sxs-lookup"><span data-stu-id="40e72-106">To join a dial-in conference as an authenticated user, a Lync Server 2013 user with Active Directory Domain Services (AD DS) credentials requires a personal identification number (PIN).</span></span> <span data-ttu-id="40e72-107">Sie können die PIN-Informationen eines Benutzers in der lync Server 2013-Systemsteuerung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="40e72-107">You can view a user’s PIN information from Lync Server 2013 Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="40e72-108">Sie können Informationen zum Pin-Status anzeigen, beispielsweise, ob die PIN festgesetzt wurde oder wann die PIN zuletzt geändert wurde, aber Sie können die aktuelle PIN nicht sehen, indem Sie den PIN-Status betrachten.</span><span class="sxs-lookup"><span data-stu-id="40e72-108">You can view PIN status information such as whether the PIN has been set or when the PIN was last changed, but you cannot see the current PIN by looking at the PIN status.</span></span> <span data-ttu-id="40e72-109">Wenn ein Benutzer seine PIN verloren hat, können Sie ihn zurücksetzen, indem Sie die Schritte unter <A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">Festlegen der PIN für Einwahlkonferenzen eines Benutzers in lync Server 2013</A></span><span class="sxs-lookup"><span data-stu-id="40e72-109">If a user has lost their PIN, you can reset it by following the procedures in <A href="lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md">Set a user's dial-in conferencing PIN in Lync Server 2013</A></span></span>



</div>

<div>

## <a name="to-view-a-users-pin-in-lync-server-control-panel"></a><span data-ttu-id="40e72-110">So zeigen Sie die PIN eines Benutzers in der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="40e72-110">To view a user’s PIN in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="40e72-111">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="40e72-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="40e72-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="40e72-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="40e72-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="40e72-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="40e72-114">Klicken Sie in der linken Navigationsleiste auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="40e72-114">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="40e72-115">Verwenden Sie eine der folgenden Methoden, um nach einem Benutzer zu suchen:</span><span class="sxs-lookup"><span data-stu-id="40e72-115">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="40e72-116">Geben Sie im Feld **Benutzer suchen** den vollständigen oder teilweisen Anzeigenamen, Vornamen, Nachnamen, SAM-Kontonamen (Security Accounts Manager), die SIP-Adresse oder den Anschluss-URI (Uniform Resource Identifier) des Benutzerkontos ein und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="40e72-116">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="40e72-117">Wenn Sie über eine gespeicherte Abfrage verfügen, klicken Sie auf das Symbol **Abfrage öffnen**, verwenden Sie das Dialogfeld **Öffnen**, um die Abfrage abzurufen (eine USF-Datei), und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="40e72-117">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="40e72-118">(Optional) Geben Sie zusätzliche Suchkriterien ein, um die Ergebnisse einzuschränken:</span><span class="sxs-lookup"><span data-stu-id="40e72-118">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="40e72-119">Klicken Sie auf **Filter hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="40e72-119">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="40e72-120">Geben Sie die Benutzereigenschaft ein, indem Sie sie über die Tastatur eintippen oder auf den Pfeil in der Dropdownliste klicken, um die Eigenschaft auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="40e72-120">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="40e72-121">Klicken Sie in der Dropdownliste **Gleich** auf den Operator (beispielsweise **Gleich** oder **Ungleich**).</span><span class="sxs-lookup"><span data-stu-id="40e72-121">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="40e72-122">Je nachdem, welche Benutzereigenschaft Sie ausgewählt haben, geben Sie nun die Kriterien ein, mit denen Sie die Suchergebnisse filtern möchten, oder treffen eine entsprechende Auswahl in der Dropdownliste.</span><span class="sxs-lookup"><span data-stu-id="40e72-122">Depending on the user property you selected, enter the criteria that you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="40e72-123">Klicken Sie auf <STRONG>Filter hinzufügen</STRONG>, um zusätzliche Suchklauseln einzugeben.</span><span class="sxs-lookup"><span data-stu-id="40e72-123">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

        
        </div>
    
    5.  <span data-ttu-id="40e72-124">Klicken Sie auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="40e72-124">Click **Find**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="40e72-p104">Ist die PIN gesperrt, müssen Sie die Sperre zunächst aufheben, bevor Sie die PIN festlegen können. Klicken Sie zum Aufheben der Sperre auf den Benutzer, dann auf <STRONG>Aktion</STRONG> und auf <STRONG>PIN entsperren</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="40e72-p104">If the PIN is locked, you must unlock the PIN before you can set it. To unlock the PIN, click the user, click <STRONG>Action</STRONG>, and then click <STRONG>Unlock PIN</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="40e72-127">Klicken Sie auf einen Benutzer in den Suchergebnissen und dann auf **Aktion** und auf **PIN-Status anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="40e72-127">Click a user in the search results, click **Action**, and then click **View PIN status**.</span></span>

</div>

<div>

## <a name="viewing-user-pin-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="40e72-128">Anzeigen von Benutzer-PIN-Informationen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="40e72-128">Viewing User PIN Information by Using Windows PowerShell cmdlets</span></span>

<span data-ttu-id="40e72-129">Sie können die PIN-Informationen für Benutzer mit dem Cmdlet „Get-CsClientPinInfo“ anzeigen.</span><span class="sxs-lookup"><span data-stu-id="40e72-129">You can view user PIN information by using the Get-CsClientPinInfo cmdlet.</span></span> <span data-ttu-id="40e72-130">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="40e72-130">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="40e72-131">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="40e72-131">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-user-pin-information"></a><span data-ttu-id="40e72-132">So zeigen Sie die PIN-Informationen von Benutzern an</span><span class="sxs-lookup"><span data-stu-id="40e72-132">To view user PIN information</span></span>

  - <span data-ttu-id="40e72-133">Wenn Sie die PIN-Informationen für einen Benutzer anzeigen möchten, geben Sie in der lync Server-Verwaltungsshell einen Befehl ähnlich der folgenden ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="40e72-133">To view PIN information for a user, type a command similar to the following in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsClientPinInfo -Identity "Ken Myer"
    
    <span data-ttu-id="40e72-134">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="40e72-134">That will return information similar to this:</span></span>
    
        Identity          : sip:kenmyer@litwareinc.com
        IsPinSet          : False
        IsLockedOut       : False
        LastPinChangeTime : 9/25/2012 1:35:03 PM
        PinExpirationTime :

</div>

<span data-ttu-id="40e72-135">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) .</span><span class="sxs-lookup"><span data-stu-id="40e72-135">For more information, see the help topic for the [Get-CsConferenceDisclaimer](https://docs.microsoft.com/powershell/module/skype/Get-CsConferenceDisclaimer) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="40e72-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40e72-136">See Also</span></span>


[<span data-ttu-id="40e72-137">Einrichten der PIN für Einwahlkonferenzen eines Benutzers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40e72-137">Set a user's dial-in conferencing PIN in Lync Server 2013</span></span>](lync-server-2013-set-a-user-s-dial-in-conferencing-pin.md)  
[<span data-ttu-id="40e72-138">Sperren oder Entsperren einer Benutzer-PIN in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40e72-138">Lock or unlock a user PIN in Lync Server 2013</span></span>](lync-server-2013-lock-or-unlock-a-user-pin.md)  
  

<span data-ttu-id="40e72-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40e72-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

