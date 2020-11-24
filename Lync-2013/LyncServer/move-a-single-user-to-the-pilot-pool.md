---
title: Verschieben eines einzelnen Benutzers in den Pilot Pool
description: Verschieben eines einzelnen Benutzers in den Pilot Pool
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Move a single user to the pilot pool
ms:assetid: e9de81a8-40dd-4446-81e7-a2b810eaea50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205401(v=OCS.15)
ms:contentKeyID: 48185905
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f7396ed2d92c7015f01ff6cd6e90fd3998219d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394286"
---
# <a name="move-a-single-user-to-the-pilot-pool"></a><span data-ttu-id="bfda1-103">Verschieben eines einzelnen Benutzers in den Pilot Pool</span><span class="sxs-lookup"><span data-stu-id="bfda1-103">Move a single user to the pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfda1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfda1-104">

<span> </span></span></span>

<span data-ttu-id="bfda1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="bfda1-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="bfda1-106">Sie können einen Benutzer aus Ihrem lync Server 2010-Pool in ihren lync Server 2013-Pilot Pool mithilfe der lync Server 2013-Systemsteuerung oder der lync Server 2013-Verwaltungsshell verschieben.</span><span class="sxs-lookup"><span data-stu-id="bfda1-106">You can move a user from your Lync Server 2010 pool to your Lync Server 2013 pilot pool using Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="bfda1-107">Im folgenden Beispiel wird in der Spalte Registrierungspool **pool01.contoso.net** der lync Server 2010-Pool angezeigt, und alle sechs dieser Benutzer sind mit diesem Pool verbunden.</span><span class="sxs-lookup"><span data-stu-id="bfda1-107">In the example below, in the Registrar pool column, **pool01.contoso.net** is the Lync Server 2010 pool, and all six of these users are connected to this pool.</span></span> <span data-ttu-id="bfda1-108">Führen Sie die folgenden Verfahren aus, um einen Benutzer mithilfe der lync Server 2013-Systemsteuerung und der lync Server-Verwaltungsshell in ihren lync Server 2013-Pool zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="bfda1-108">Use the following procedures to move a user to your Lync Server 2013 pool using Lync Server 2013 Control Panel and Lync Server Management Shell.</span></span>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-control-panel"></a><span data-ttu-id="bfda1-109">So verschieben Sie einen Benutzer mithilfe der lync Server 2013-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="bfda1-109">To move a user by using the Lync Server 2013 Control Panel</span></span>

<span data-ttu-id="bfda1-110">**Liste der Benutzer in der lync Server 2013-Systemsteuerung**</span><span class="sxs-lookup"><span data-stu-id="bfda1-110">**List of users in the Lync Server 2013 Control Panel**</span></span>

<span data-ttu-id="bfda1-111">![Lync Server-Systemsteuerung, Dialogfeld ' Benutzer verschieben '](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server-Systemsteuerung, Dialogfeld ' Benutzer verschieben '")</span><span class="sxs-lookup"><span data-stu-id="bfda1-111">![Lync Server Control Panel, Move User dialog](images/JJ721870.a2bce284-0392-4db3-9bb2-9f12699738e7(OCS.15).jpg "Lync Server Control Panel, Move User dialog")</span></span>

1.  <span data-ttu-id="bfda1-112">Melden Sie sich über ein Konto, das Mitglied der Gruppe „RTCUniversalServerAdmins“ oder der Administratorrolle „CsAdministrator“ oder „CsUserAdministrator“ ist, am Front-End-Server an.</span><span class="sxs-lookup"><span data-stu-id="bfda1-112">Log on to the Front End Server with an account that is a member of the RTCUniversalServerAdmins group or a member of the CsAdministrator or CsUserAdministrator administrative role.</span></span>

2.  <span data-ttu-id="bfda1-113">Öffnen Sie die **Lync Server-Systemsteuerung**.</span><span class="sxs-lookup"><span data-stu-id="bfda1-113">Open **Lync Server Control Panel**.</span></span>

3.  <span data-ttu-id="bfda1-114">Klicken Sie auf **Benutzer** und anschließend auf **Suchen**.</span><span class="sxs-lookup"><span data-stu-id="bfda1-114">Click **Users**, click Search, and then click **Find**.</span></span>

4.  <span data-ttu-id="bfda1-115">Wählen Sie einen Benutzer aus, den Sie in den lync Server 2013-Pool verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="bfda1-115">Select a user that you want to move to the Lync Server 2013 pool.</span></span> <span data-ttu-id="bfda1-116">In diesem Beispiel verschieben wir den Benutzer Sara Davis.</span><span class="sxs-lookup"><span data-stu-id="bfda1-116">In this example, we will move user Sara Davis.</span></span>

5.  <span data-ttu-id="bfda1-117">Wählen Sie im Menü **Aktion** die Option **Ausgewählte Benutzer in Pool verschieben** aus.</span><span class="sxs-lookup"><span data-stu-id="bfda1-117">On the **Action** menu, select **Move selected users to pool**.</span></span>

6.  <span data-ttu-id="bfda1-118">Wählen Sie in der Dropdownliste den lync Server 2013-Pool aus.</span><span class="sxs-lookup"><span data-stu-id="bfda1-118">From the drop-down list, select the Lync Server 2013 pool.</span></span>

7.  <span data-ttu-id="bfda1-119">Klicken Sie auf **Aktion** und dann auf **Ausgewählte Benutzer in Pool verschieben**.</span><span class="sxs-lookup"><span data-stu-id="bfda1-119">Click **Action** and then click **Move selected users to pool**.</span></span> <span data-ttu-id="bfda1-120">Klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bfda1-120">Click **OK**.</span></span>
    
    <span data-ttu-id="bfda1-121">![Dialogfeld ' Benutzer verschieben, Ziel Registrierungspool '](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Dialogfeld ' Benutzer verschieben, Ziel Registrierungspool '")</span><span class="sxs-lookup"><span data-stu-id="bfda1-121">![Move Users, destination registrar pool dialog box](images/JJ205401.8a375003-dc00-4541-b578-4d88f2010601(OCS.15).png "Move Users, destination registrar pool dialog box")</span></span>  

8.  <span data-ttu-id="bfda1-122">Überprüfen Sie, ob die Spalte des **registrierungspools** für den Benutzer jetzt den lync Server 2013-Pool enthält, der angibt, dass der Benutzer erfolgreich verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="bfda1-122">Verify that the **Registrar pool** column for the user now contains the Lync Server 2013 pool, which indicates that the user has been successfully moved.</span></span>

</div>

<div>

## <a name="to-move-a-user-by-using-the-lync-server-2013-management-shell"></a><span data-ttu-id="bfda1-123">So verschieben Sie einen Benutzer mithilfe der lync Server 2013-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="bfda1-123">To move a user by using the Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="bfda1-124">Öffnen Sie die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="bfda1-124">Open the Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="bfda1-125">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bfda1-125">At the command line, type the following:</span></span>
    
        Move-CsUser -Identity "David Pelton" -Target "pool02.contoso.net"

3.  <span data-ttu-id="bfda1-126">Geben Sie als nächstes in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bfda1-126">Next, at the command line, type the following:</span></span>
    
        Get-CsUser -Identity "David Pelton"

4.  <span data-ttu-id="bfda1-127">Die **RegistrarPool** -Identität verweist nun auf den lync Server 2013-Pool.</span><span class="sxs-lookup"><span data-stu-id="bfda1-127">The **RegistrarPool** identity now points to the Lync Server 2013 pool.</span></span> <span data-ttu-id="bfda1-128">Das vorhanden sein dieser Identität bestätigt, dass der Benutzer erfolgreich verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="bfda1-128">The presence of this identity confirms that the user has been successfully moved.</span></span>
    
    <span data-ttu-id="bfda1-129">![Ausgabe von Get-CsUser-Cmdlet mit Identitäts Filter](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Ausgabe von Get-CsUser-Cmdlet mit Identitäts Filter")</span><span class="sxs-lookup"><span data-stu-id="bfda1-129">![Output from Get-CsUser cmdlet with Identity filter](images/JJ205401.bc5d4672-8068-4475-b882-dbd305c801a9(OCS.15).jpg "Output from Get-CsUser cmdlet with Identity filter")</span></span>  
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bfda1-130">Details zum Cmdlet " <STRONG>Get-CsUser</STRONG> " finden Sie unter <STRONG>Get-Help Get-CsUser – detailliert</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="bfda1-130">For details about the <STRONG>Get-CsUser</STRONG> cmdlet, run: <STRONG>Get-Help Get-CsUser –Detailed</STRONG></span></span>

    
    <span data-ttu-id="bfda1-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfda1-131"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

