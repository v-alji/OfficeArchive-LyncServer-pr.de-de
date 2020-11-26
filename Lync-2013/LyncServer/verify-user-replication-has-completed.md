---
title: Überprüfen, ob die Benutzerreplikation abgeschlossen wurde
description: Überprüfen Sie, ob die Benutzerreplikation abgeschlossen ist.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify user replication has completed
ms:assetid: 119e9896-45e5-4f8b-af43-7b09360ada0b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204680(v=OCS.15)
ms:contentKeyID: 48183441
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 60bca44fcce811c29b1633bd4d3a39f832851885
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446072"
---
# <a name="verify-user-replication-has-completed"></a><span data-ttu-id="19117-103">Überprüfen, ob die Benutzerreplikation abgeschlossen wurde</span><span class="sxs-lookup"><span data-stu-id="19117-103">Verify user replication has completed</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="19117-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="19117-104">

<span> </span></span></span>

<span data-ttu-id="19117-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="19117-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="19117-106">Bei der Ausführung des Cmdlets **Move-CsUser** tritt möglicherweise ein Fehler auf, da die Benutzerinformationen zwischen den Active Directory-Domänendiensten (AD DS) und den lync Server 2013-Datenbanken nicht synchronisiert sind, weil die anfängliche Replikation unvollständig ist.</span><span class="sxs-lookup"><span data-stu-id="19117-106">When running the **Move-CsUser** cmdlet, you may experience a failure because user information between Active Directory Domain Services (AD DS) and the Lync Server 2013 databases are out of sync because the initial replication is incomplete.</span></span> <span data-ttu-id="19117-107">Die Zeit, die für den erfolgreichen Abschluss der ersten Synchronisierung des lync Server 2013-Benutzerreplikationsdiensts benötigt wird, hängt von der Anzahl der Domänencontroller ab, die in der Active Directory-Gesamtstruktur gehostet werden, die den lync Server 2013-Pool hostet.</span><span class="sxs-lookup"><span data-stu-id="19117-107">The time it takes for the successful completion of the Lync Server 2013 User Replicator service's initial synchronization depends on the number of domain controllers that are hosted in the Active Directory forest that hosts the Lync Server 2013 pool.</span></span> <span data-ttu-id="19117-108">Der erst Synchronisierungsvorgang des lync Server 2013-Benutzerreplikationsdiensts erfolgt, wenn der lync Server 2013-Front-End-Server zum ersten Mal gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="19117-108">The Lync Server 2013 User Replicator service initial synchronization process occurs when the Lync Server 2013 Front End Server is started for the first time.</span></span> <span data-ttu-id="19117-109">Danach basiert die Synchronisierung auf dem Intervall des Benutzerreplikationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="19117-109">After that, the synchronization is then based on the User Replicator interval.</span></span> <span data-ttu-id="19117-110">Führen Sie die folgenden Schritte aus, um zu überprüfen, ob die Benutzerreplikation abgeschlossen ist, bevor Sie das Cmdlet **Move-CsUser** ausführen.</span><span class="sxs-lookup"><span data-stu-id="19117-110">Complete the following steps to verify user replication has completed before running the **Move-CsUser** cmdlet.</span></span>

<div>

## <a name="to-verify-user-replication-has-completed"></a><span data-ttu-id="19117-111">So überprüfen Sie, ob die Benutzerreplikation abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="19117-111">To verify user replication has completed</span></span>

1.  <span data-ttu-id="19117-112">Melden Sie sich auf dem Computer, auf dem der Topologie-Generator installiert ist, als Mitglied der Gruppe "Domänen-Admins" oder "RTCUniversalServerAdmins" an.</span><span class="sxs-lookup"><span data-stu-id="19117-112">Log on to the computer where Topology Builder is installed as a member of the Domain Admins group and the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="19117-113">Klicken Sie auf das **Startmenü** , und klicken Sie dann auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="19117-113">Click the **Start** menu, and then click **Run**.</span></span>

3.  <span data-ttu-id="19117-114">Geben Sie **eventvwr.exe** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="19117-114">Enter **eventvwr.exe** and then click **OK**.</span></span>

4.  <span data-ttu-id="19117-115">Klicken Sie in der Ereignisanzeige auf **Anwendungen und Dienstprotokolle** , um Sie zu erweitern, und wählen Sie dann lync Server aus.</span><span class="sxs-lookup"><span data-stu-id="19117-115">In Event Viewer, click **Applications and Services logs** to expand it, and then select Lync Server.</span></span>

5.  <span data-ttu-id="19117-116">Klicken Sie im Bereich **Aktionen** auf **Aktuelles Protokoll filtern**.</span><span class="sxs-lookup"><span data-stu-id="19117-116">In the **Actions** pane click **Filter Current Log**.</span></span>

6.  <span data-ttu-id="19117-117">Klicken Sie in der Liste **Ereignisquellen** auf **ls-Benutzer Replikations** Dienst.</span><span class="sxs-lookup"><span data-stu-id="19117-117">From the **Event sources** list, click **LS User Replicator**.</span></span>

7.  <span data-ttu-id="19117-118">**\<All Event IDs\>** Geben Sie **30024** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="19117-118">In **\<All Event IDs\>** enter **30024** and then click **OK**.</span></span>

8.  <span data-ttu-id="19117-119">Suchen Sie in der Liste Gefilterte Ereignisse auf der Registerkarte **Allgemein** nach einem Eintrag, der besagt, dass die Benutzerreplikation erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="19117-119">In the filtered events list, on the **General** tab, look for an entry that states user replication has completed successfully.</span></span>

<span data-ttu-id="19117-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="19117-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

