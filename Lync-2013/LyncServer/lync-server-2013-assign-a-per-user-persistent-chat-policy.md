---
title: 'Lync Server 2013: Zuweisen einer beständigen Chat Richtlinie für einzelne Benutzer'
description: 'Lync Server 2013: weisen Sie eine Richtlinie für beständigen Chat pro Benutzer zu.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a per-user Persistent Chat policy
ms:assetid: e22168f2-fde1-4f0a-b194-1fc881436822
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721908(v=OCS.15)
ms:contentKeyID: 49733842
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 637f1947fff7f4e919e5f9c252c047b2d0e60392
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443195"
---
# <a name="assign-a-per-user-persistent-chat-policy-in-lync-server-2013"></a><span data-ttu-id="fa2c5-103">Zuweisen einer beständigen Chat Richtlinie für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa2c5-103">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>

 


<span data-ttu-id="fa2c5-104">Sie können der lync Server 2013-Systemsteuerung oder der lync Server 2013-Verwaltungsshell eine Richtlinie für beständigen Chat pro Benutzer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-104">You can assign a per-user persistent chat policy with either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="fa2c5-105">Details zum Erstellen von Benutzerrichtlinien für beständigen Chat Server finden Sie unter [Erstellen einer Benutzerrichtlinie für beständigen Chat in lync Server 2013](lync-server-2013-create-a-user-policy-for-persistent-chat.md).</span><span class="sxs-lookup"><span data-stu-id="fa2c5-105">For details on creating user policies for Persistent Chat Server, see [Create a user policy for Persistent Chat in Lync Server 2013](lync-server-2013-create-a-user-policy-for-persistent-chat.md).</span></span>

## <a name="to-assign-a-per-user-persistent-chat-policy-with-lync-server-control-panel"></a><span data-ttu-id="fa2c5-106">So weisen Sie eine Richtlinie für beständigen Chat für einzelne Benutzer mit der lync Server-Systemsteuerung zu</span><span class="sxs-lookup"><span data-stu-id="fa2c5-106">To assign a per-user persistent chat policy with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="fa2c5-107">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-107">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fa2c5-108">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-108">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="fa2c5-109">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="fa2c5-109">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="fa2c5-110">Klicken Sie in der linken Navigationsleiste auf **Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-110">In the left navigation bar, click **Users**.</span></span>

4.  <span data-ttu-id="fa2c5-111">Verwenden Sie eine der folgenden Methoden, um nach einem Benutzer zu suchen:</span><span class="sxs-lookup"><span data-stu-id="fa2c5-111">Use one of the following methods to locate a user:</span></span>
    
      - <span data-ttu-id="fa2c5-112">Geben Sie im Feld **Benutzer suchen** den vollständigen oder teilweisen Anzeigenamen, Vornamen, Nachnamen, SAM-Kontonamen (Security Accounts Manager), die SIP-Adresse oder den Anschluss-URI (Uniform Resource Identifier) des Benutzerkontos ein und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-112">In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account, and then click **Find**.</span></span>
    
      - <span data-ttu-id="fa2c5-113">Wenn Sie über eine gespeicherte Abfrage verfügen, klicken Sie auf das Symbol **Abfrage öffnen**, verwenden Sie das Dialogfeld **Öffnen**, um die Abfrage abzurufen (eine USF-Datei), und klicken Sie dann auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-113">If you have a saved query, click the **Open query** icon, use the **Open** dialog box to retrieve the query (a .usf file), and then click **Find**.</span></span>

5.  <span data-ttu-id="fa2c5-114">(Optional) Geben Sie zusätzliche Suchkriterien ein, um die Ergebnisse einzuschränken:</span><span class="sxs-lookup"><span data-stu-id="fa2c5-114">(Optional) Specify additional search criteria to narrow the results:</span></span>
    
    1.  <span data-ttu-id="fa2c5-115">Klicken Sie auf **Filter hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-115">Click **Add Filter**.</span></span>
    
    2.  <span data-ttu-id="fa2c5-116">Geben Sie die Benutzereigenschaft ein, indem Sie sie über die Tastatur eintippen oder auf den Pfeil in der Dropdownliste klicken, um die Eigenschaft auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-116">Enter the user property by typing it or by clicking the arrow in the drop-down list to select the property.</span></span>
    
    3.  <span data-ttu-id="fa2c5-117">Klicken Sie in der Dropdownliste **Gleich** auf den Operator (beispielsweise **Gleich** oder **Ungleich**).</span><span class="sxs-lookup"><span data-stu-id="fa2c5-117">In the **Equal to** drop-down list, click the operator (for example, **Equal to** or **Not equal to**).</span></span>
    
    4.  <span data-ttu-id="fa2c5-118">Geben Sie je nach gewählter Benutzereigenschaft entweder das Kriterium für die Filterung der Suchergebnisse ein oder klicken Sie auf den Pfeil in der Dropdownliste.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-118">Depending on the user property you selected, enter the criteria you want to use to filter the search results by typing it or by clicking the arrow in the drop-down list.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="fa2c5-119">Klicken Sie auf <STRONG>Filter hinzufügen</STRONG>, um zusätzliche Suchklauseln einzugeben.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-119">To add additional search clauses to your query, click <STRONG>Add Filter</STRONG>.</span></span>

    
    5.  <span data-ttu-id="fa2c5-120">Klicken Sie auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-120">Click **Find**.</span></span>

6.  <span data-ttu-id="fa2c5-121">Klicken Sie in den Suchergebnissen auf einen Benutzer, klicken Sie auf **Aktion** und anschließend auf **Richtlinien zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-121">Click a user in the search results, click **Action**, and then click **Assign policies**.</span></span>
    

    > [!TIP]  
    > <span data-ttu-id="fa2c5-122">Wenn Sie möchten, dass die gleiche Richtlinie für Benutzer mit beständigem Chat für mehrere Benutzer gilt, wählen Sie in den Suchergebnissen mehrere Benutzer aus, klicken Sie dann auf <STRONG>Aktionen</STRONG>, und klicken Sie dann auf <STRONG>Richtlinien zuweisen</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-122">If you want the same per-user persistent Chat policy to apply to multiple users, select multiple users in the search results, then click <STRONG>Actions</STRONG>, and then click <STRONG>Assign policies</STRONG>.</span></span>



7.  <span data-ttu-id="fa2c5-123">Führen Sie in Richt **Linien zuweisen** unter Richtlinien für **beständigen Chat** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="fa2c5-123">In **Assign Policies**, under **Persistent Chat policy**, do one of the following:</span></span>
    

    > [!NOTE]  
    > <span data-ttu-id="fa2c5-124">Da es mehrere Richtlinien gibt, die Sie mithilfe des Dialogfelds <STRONG>Richtlinien zuweisen</STRONG> konfigurieren können, ist für jede Richtlinie im Dialogfeld standardmäßig <STRONG> &lt; &gt; beibehalten</STRONG> aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-124">Because there are multiple policies that you can configure by using the <STRONG>Assign Policies</STRONG> dialog box, <STRONG>&lt;Keep as is&gt;</STRONG> is selected by default for every policy in the dialog box.</span></span> <span data-ttu-id="fa2c5-125">Wenn Sie an dieser Einstellung keine Änderung vornehmen, wird eine zuvor zugewiesene Richtlinie weiterhin auf den Benutzer angewendet.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-125">Continue using the policy previously assigned to the user by making no changes to this setting.</span></span>

    
      - <span data-ttu-id="fa2c5-126">Wählen Sie aus **\<Automatic\>** , um zu ermöglichen, dass lync Server 2013 automatisch entweder die Richtlinie auf globaler Ebene oder, falls definiert, die Richtlinie auf Websiteebene wählt.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-126">Select **\<Automatic\>** to allow Lync Server 2013 to automatically choose either the global-level policy or, if defined, the site-level policy.</span></span>
    
      - <span data-ttu-id="fa2c5-127">Klicken Sie auf den Namen einer auf der Seite für **beständigen Chats** festgelegten beständigen Chat Richtlinie für einzelne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-127">Click the name of a per-user Persistent Chat policy you previously defined on the **Persistent Chat Policy** page.</span></span>
        

        > [!TIP]  
        > <span data-ttu-id="fa2c5-128">Um besser entscheiden zu können, welche Richtlinie zugewiesen werden soll, klicken Sie auf einen Richtliniennamen und anschließend auf <STRONG>Anzeigen</STRONG>, um die in der Richtlinie definierten Benutzerrechte und -berechtigungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-128">To help you decide the policy you want to assign, after you click a policy name, click <STRONG>View</STRONG> to view the user rights and permissions defined in the policy.</span></span>



8.  <span data-ttu-id="fa2c5-129">Nachdem Sie die Eingabe beendet haben, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-129">When you are finished, click **OK**.</span></span>

## <a name="assigning-a-per-user-persistent-chat-policy-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="fa2c5-130">Zuweisen einer Per-User beständigen Chat Richtlinie mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fa2c5-130">Assigning a Per-User Persistent Chat Policy by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="fa2c5-131">Mithilfe des Cmdlets **Grant-CsPersistentChatPolicy** können Sie auch beständige Chat-Richtlinien für einzelne Benutzer zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-131">You can also assign per-user persistent chat policies by using the **Grant-CsPersistentChatPolicy** cmdlet.</span></span> <span data-ttu-id="fa2c5-132">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="fa2c5-133">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="fa2c5-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

## <a name="to-assign-a-per-user-persistent-chat-policy-to-a-single-user"></a><span data-ttu-id="fa2c5-134">So weisen Sie einem einzelnen Benutzer eine Richtlinie für beständigen Chat pro Benutzer zu</span><span class="sxs-lookup"><span data-stu-id="fa2c5-134">To assign a per-user persistent chat policy to a single user</span></span>

  - <span data-ttu-id="fa2c5-135">Mit dem folgenden Befehl wird dem Benutzer Ken Myers die Richtlinie für den beständigen Chat für einzelne Benutzer zugewiesen RedmondPersistentChatPolicy.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-135">The following command assigns the per-user Persistent Chat policy RedmondPersistentChatPolicy to the user Ken Myer.</span></span>
    
        Grant-CsPersistentChatPolicy -Identity "Ken Myer" -PolicyName "RedmondPersistentChatPolicy"

## <a name="to-assign-a-per-user-persistent-chat-policy-to-multiple-users"></a><span data-ttu-id="fa2c5-136">So weisen Sie mehreren Benutzern eine Richtlinie für beständigen Chat pro Benutzer zu</span><span class="sxs-lookup"><span data-stu-id="fa2c5-136">To assign a per-user persistent chat policy to multiple users</span></span>

  - <span data-ttu-id="fa2c5-137">Dieser Befehl weist allen Benutzern, die für die IT-Abteilung arbeiten, die Richtlinien für die beständigen Chat-RedmondUsersPersistentChatPolicy zu.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-137">This command assigns the per-user Persistent Chat policy RedmondUsersPersistentChatPolicy to all the users who work for the IT department.</span></span> <span data-ttu-id="fa2c5-138">Weitere Informationen zu dem in diesem Befehl verwendeten LdapFilter-Parameter finden Sie in der Dokumentation für das Cmdlet [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="fa2c5-138">For more information on the LdapFilter parameter used in this command, see the documentation for the [Get-CsUser](https://technet.microsoft.com/library/gg398125\(v=ocs.15\)) cmdlet.</span></span>
    
        Get-CsUser -LdapFilter "Department=IT" | Grant-CsPersistentChatPolicy -PolicyName "RedmondUsersPersistentChatPolicy"

## <a name="to-unassign-a-per-user-persistent-chat-policy"></a><span data-ttu-id="fa2c5-139">So heben Sie die Zuweisung einer beständigen Chat Richtlinie für einzelne Benutzer auf</span><span class="sxs-lookup"><span data-stu-id="fa2c5-139">To unassign a per-user persistent chat policy</span></span>

  - <span data-ttu-id="fa2c5-140">Mit dem folgenden Befehl wird die Zuweisung einer beständigen Chat Richtlinie für einzelne Benutzer aufheben, die Ken Myers zuvor zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-140">The following command unassigns any per-user Persistent Chat policy previously assigned to Ken Myer.</span></span> <span data-ttu-id="fa2c5-141">Anschließend wird Ken Myer automatisch mithilfe der globalen Richtlinie oder, soweit vorhanden, mit seiner lokalen Standortrichtlinie verwaltet.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-141">After the per-user policy is unassigned, Ken Myer will automatically be managed by using the global policy or, if one exists, his local site policy.</span></span> <span data-ttu-id="fa2c5-142">Eine Standortrichtlinie hat Vorrang vor der globalen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fa2c5-142">A site policy takes precedence over the global policy.</span></span>
    
        Grant-CsPersistentChatPolicy -Identity "Ken Myer" -PolicyName $Null

<span data-ttu-id="fa2c5-143">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/jj204907\(v=ocs.15\)) .</span><span class="sxs-lookup"><span data-stu-id="fa2c5-143">For more information, see the help topic for the [Grant-CsPersistentChatPolicy](https://technet.microsoft.com/library/jj204907\(v=ocs.15\)) cmdlet.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa2c5-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa2c5-144">See Also</span></span>


[<span data-ttu-id="fa2c5-145">Erstellen einer Benutzerrichtlinie für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fa2c5-145">Create a user policy for Persistent Chat in Lync Server 2013</span></span>](lync-server-2013-create-a-user-policy-for-persistent-chat.md)

