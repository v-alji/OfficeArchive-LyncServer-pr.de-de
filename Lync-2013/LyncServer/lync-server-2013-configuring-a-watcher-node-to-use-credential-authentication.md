---
title: 'Lync Server 2013: Konfigurieren eines Watcher-Knotens zur Verwendung der Authentifizierung von Anmeldeinformationen'
description: 'Lync Server 2013: Konfigurieren eines Watcher-Knotens zur Verwendung der Anmelde Informations Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to use credential authentication
ms:assetid: 032e33f3-9483-42e6-a33c-347eb6779597
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204632(v=OCS.15)
ms:contentKeyID: 48183255
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b65d4e3f90b27aac69b8569472ac9896766e093e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433444"
---
# <a name="configuring-a-watcher-node-to-use-credential-authentication-in-lync-server-2013"></a><span data-ttu-id="c4a35-103">Konfigurieren eines Watcher-Knotens zur Verwendung der Authentifizierung von Anmeldeinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4a35-103">Configuring a watcher node to use credential authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4a35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4a35-104">

<span> </span></span></span>

<span data-ttu-id="c4a35-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="c4a35-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="c4a35-106">Wenn sich Ihr Watcher-Knoten Computer außerhalb des Umkreisnetzwerks befindet, müssen Sie ein etwas anderes Verfahren ausführen, um diesen Watcher-Knoten so zu konfigurieren, dass synthetische Transaktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c4a35-106">If your watcher node computer lies outside the perimeter network, then you must follow a slightly different procedure in order to configure that watcher node to run synthetic transactions.</span></span> <span data-ttu-id="c4a35-107">Insbesondere sollten Sie keinen vertrauenswürdigen Anwendungspool und eine vertrauenswürdige Anwendung erstellen, und Sie müssen ein Zertifikat installieren, mit dem der Watcher-Knoten Benachrichtigungen an einen Computer im Umkreisnetzwerk senden kann.</span><span class="sxs-lookup"><span data-stu-id="c4a35-107">Specifically, you should not create a trusted application pool and a trusted application, and you must install a certificate that enables the watcher node to send alerts to a computer inside the perimeter network.</span></span> <span data-ttu-id="c4a35-108">Das bedeutet, dass Sie zwei getrennte Aufgaben ausführen müssen:</span><span class="sxs-lookup"><span data-stu-id="c4a35-108">This means that you will need to complete two separate tasks:</span></span>

  - <span data-ttu-id="c4a35-109">Aktualisieren der Mitgliedschaft in der RTC Local-Gruppe "nur-Lese-Administratoren" des Computers</span><span class="sxs-lookup"><span data-stu-id="c4a35-109">Update the membership in the computer's RTC Local Read-only Administrators Group</span></span>

  - <span data-ttu-id="c4a35-110">Installieren der Watcher-Knoten-Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="c4a35-110">Install the watcher node configuration files</span></span>

<div>

## <a name="updating-membership-in-the-rtc-local-read-only-administrators-group"></a><span data-ttu-id="c4a35-111">Aktualisieren der Mitgliedschaft in der Gruppe RTC Local Read-Only Administratoren</span><span class="sxs-lookup"><span data-stu-id="c4a35-111">Updating Membership in the RTC Local Read-Only Administrators Group</span></span>

<span data-ttu-id="c4a35-112">Wenn sich der Watcher-Knoten außerhalb des Umkreisnetzwerks befindet, müssen Sie das Netzwerkdienstkonto der Gruppe "RTC Local Read-only" auf dem Watcher-Knoten Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c4a35-112">If your watcher node lies outside the perimeter network, you must add the Network Service account to the RTC Local Read-only Administrators group on the watcher node computer.</span></span> <span data-ttu-id="c4a35-113">Führen Sie dazu das folgende Verfahren auf dem Watcher-Knoten aus:</span><span class="sxs-lookup"><span data-stu-id="c4a35-113">To do this, complete the following procedure on the watcher node:</span></span>

1.  <span data-ttu-id="c4a35-114">Klicken Sie auf **Start**, klicken Sie mit der rechten Maustaste auf **Computer**, und klicken Sie dann auf **Verwalten**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-114">Click **Start**, right-click **Computer**, and then click **Manage**.</span></span>

2.  <span data-ttu-id="c4a35-115">Erweitern Sie im Server-Manager **Konfiguration**, erweitern Sie **lokale Benutzer und Gruppen**, und klicken Sie dann auf **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-115">In Server Manager, expand **Configuration**, expand **Local Users and Groups**, and then click **Groups**.</span></span>

3.  <span data-ttu-id="c4a35-116">Doppelklicken Sie im Bereich Gruppen auf **RTC Local Read-Only-Administratoren**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-116">In the Groups pane, double-click **RTC Local Read-only Administrators**.</span></span>

4.  <span data-ttu-id="c4a35-117">Klicken Sie im Dialogfeld **Eigenschaften von RTC Local nur-Lese-Administratoren** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-117">In the **RTC Local Read-only Administrators Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="c4a35-118">Klicken Sie im Dialogfeld **Benutzer, Computer, Dienstkonten oder Gruppen auswählen** auf **Speicherorte**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-118">In the **Select Users, Computers, Service Accounts, or Groups** dialog box, click **Locations**.</span></span>

6.  <span data-ttu-id="c4a35-119">Wählen Sie im Dialogfeld **Speicherorte** den Namen des Watcher-Knoten Computers aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-119">In the **Locations** dialog box, select the name of the watcher node computer, and then click **OK**.</span></span>

7.  <span data-ttu-id="c4a35-120">Geben Sie im Feld Geben Sie die **zu wählenden Objektnamen ein den Namen** **Netzwerkdienst** ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-120">In the **Enter object names to select** box, type **Network Service**, and then click **OK**.</span></span>

8.  <span data-ttu-id="c4a35-121">Klicken Sie im Dialogfeld **Eigenschaften von RTC-schreibgeschützten Administratoren** auf **OK**, und schließen Sie dann **Server-Manager**.</span><span class="sxs-lookup"><span data-stu-id="c4a35-121">In the **RTC Local Read-only Administrators Properties** dialog box, click **OK**, and then close **Server Manager**.</span></span>

<span data-ttu-id="c4a35-122">Starten Sie den Monitorknotencomputer neu.</span><span class="sxs-lookup"><span data-stu-id="c4a35-122">Restart the watcher node computer.</span></span>

</div>

<div>

## <a name="installing-the-watcher-node-configuration-files"></a><span data-ttu-id="c4a35-123">Installieren der Watcher-Knoten-Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="c4a35-123">Installing the Watcher Node Configuration Files</span></span>

<span data-ttu-id="c4a35-124">Nachdem der Watcher-Knoten Computer neu gestartet wurde, besteht der nächste Schritt darin, die Datei Watchernode.msi auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c4a35-124">After the watcher node computer has restarted, your next step is to run the file Watchernode.msi.</span></span> <span data-ttu-id="c4a35-125">Um diese Datei auszuführen, öffnen Sie die lync Server 2013-Verwaltungsshell, indem Sie auf **Start** klicken, auf **Alle Programme** klicken, auf **lync Server 2013** und dann auf **lync Server-Verwaltungsshell** klicken.</span><span class="sxs-lookup"><span data-stu-id="c4a35-125">To run this file, open the Lync Server 2013 Management Shell by clicking **Start**, clicking **All Programs**, clicking **Lync Server 2013**, and then clicking **Lync Server Management Shell**.</span></span> <span data-ttu-id="c4a35-126">Geben Sie in der lync Server-Verwaltungsshell den folgenden Befehl ein, und drücken Sie dann die EINGABETASTE (stellen Sie sicher, dass Sie den tatsächlichen Pfad zu Ihrer Kopie von Watchernode.msi angeben):</span><span class="sxs-lookup"><span data-stu-id="c4a35-126">In the Lync Server Management Shell, type the following command and then press ENTER (be sure and specify the actual path to your copy of Watchernode.msi):</span></span>

    C:\Tools\Watchernode.msi Authentication=Negotiate

<div>


> [!NOTE]  
> <span data-ttu-id="c4a35-127">Wie bereits erwähnt, können Watchernode.msi auch über ein Befehlsfenster ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c4a35-127">As noted previously, Watchernode.msi can also be run from a command window.</span></span> <span data-ttu-id="c4a35-128">Klicken Sie zum Öffnen eines Befehlsfensters auf <STRONG>Start</STRONG>, klicken Sie mit der rechten Maustaste auf <STRONG>Eingabeaufforderung</STRONG> und klicken Sie dann auf <STRONG>Als Administrator ausführen</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="c4a35-128">To open a command window, click <STRONG>Start</STRONG>, right-click <STRONG>Command Prompt</STRONG>, and then click <STRONG>Run as administrator</STRONG>.</span></span> <span data-ttu-id="c4a35-129">Wenn das Befehlsfenster geöffnet wird, geben Sie den gleichen Befehl wie zuvor gezeigt ein.</span><span class="sxs-lookup"><span data-stu-id="c4a35-129">When the command window opens, type the same command as shown earlier.</span></span>



</div>

<span data-ttu-id="c4a35-p105">Der Aushandlungsmodus wird verwendet, wenn der Monitorknoten nicht als Pool mit vertrauenswürdigen Anwendungen eingerichtet werden kann. In diesem Modus müssen Administratoren Testbenutzerkennwörter für den Monitorknoten verwalten.</span><span class="sxs-lookup"><span data-stu-id="c4a35-p105">The Negotiate mode is used any time the watcher node cannot be set up as a trusted application pool. In this mode, administrators will need to manage test user passwords on the watcher node.</span></span>

<span data-ttu-id="c4a35-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4a35-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

