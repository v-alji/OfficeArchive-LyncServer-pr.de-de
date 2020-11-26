---
title: 'Lync Server 2013: Lesen von Erfassungs Protokollen vom zentralen Protokollierungsdienst'
description: 'Lync Server 2013: Lesen von Erfassungs Protokollen vom zentralen Protokollierungsdienst'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reading capture logs from the Centralized Logging Service
ms:assetid: c86ccf61-d86f-4ebd-b8d1-984a1b73005d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721879(v=OCS.15)
ms:contentKeyID: 49733813
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcdd70c924b49098814e80a375ae34d2bf48dc41
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436774"
---
# <a name="reading-capture-logs-from-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="8d92d-103">Lesen von Aufnahme Protokollen vom zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d92d-103">Reading capture logs from the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d92d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d92d-104">

<span> </span></span></span>

<span data-ttu-id="8d92d-105">_**Letztes Änderungsdatum des Themas:** 2016-12-28_</span><span class="sxs-lookup"><span data-stu-id="8d92d-105">_**Topic Last Modified:** 2016-12-28_</span></span>

<span data-ttu-id="8d92d-106">Sie erkennen den wirklichen Vorteil des zentralen Protokollierungsdiensts, nachdem Sie die Suche ausgeführt haben, und Sie verfügen über eine Datei, mit der Sie ein gemeldetes Problem nachvollziehen können.</span><span class="sxs-lookup"><span data-stu-id="8d92d-106">You realize the real benefit of the Centralized Logging Service after you run the search and you have a file that you can use to track down a reported problem.</span></span> <span data-ttu-id="8d92d-107">Es gibt eine Reihe von Möglichkeiten, wie Sie die Datei lesen können.</span><span class="sxs-lookup"><span data-stu-id="8d92d-107">There are a number of ways that you can read the file.</span></span> <span data-ttu-id="8d92d-108">Die Ausgabedatei befindet sich in einem Standardtextformat und Sie können Notepad.exe oder alle anderen Programme verwenden, mit denen Sie eine Textdatei öffnen und lesen können.</span><span class="sxs-lookup"><span data-stu-id="8d92d-108">The output file is in a standard text format and you can use Notepad.exe or any other programs that will allow you to open and read a text file.</span></span> <span data-ttu-id="8d92d-109">Für größere Dateien und komplexere Probleme können Sie ein Tool wie Snooper.exe verwenden, das zum Lesen und Analysieren der Protokollierungsausgabe vom zentralen Protokollierungsdienst entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d92d-109">For larger files and more complex issues, you could use a tool like Snooper.exe that is designed to read and parse the logging output from the Centralized Logging Service.</span></span> <span data-ttu-id="8d92d-110">Snooper ist in den lync Server 2013-Debug-Tools enthalten, die als separater Download zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8d92d-110">Snooper is included with the Lync Server 2013 Debug Tools that are available as a separate download.</span></span> <span data-ttu-id="8d92d-111">Sie können die lync Server 2013-Debug-Tools hier herunterladen: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257) .</span><span class="sxs-lookup"><span data-stu-id="8d92d-111">You can download the Lync Server 2013 Debug Tools here: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257).</span></span> <span data-ttu-id="8d92d-112">Wenn Sie die lync Server 2013-Debug-Tools installieren, werden keine kurzen Schnitte und Menüelemente erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d92d-112">When you install the Lync Server 2013 Debug Tools, short cuts and menu items are not created.</span></span> <span data-ttu-id="8d92d-113">Nachdem Sie die lync Server 2013-Debug-Tools installiert haben, öffnen Sie den Windows-Explorer, ein Befehlszeilenfenster oder die lync Server-Verwaltungsshell, und wechseln Sie zu dem Verzeichnis (Standardspeicherort) C: \\ Programmdateien \\ Microsoft lync Server 2013 \\ Debug-Tools.</span><span class="sxs-lookup"><span data-stu-id="8d92d-113">After you install the Lync Server 2013 Debug Tools, open Windows Explorer, a command-line window, or Lync Server Management Shell and go to the directory (default location) C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="8d92d-114">Doppelklicken Sie auf Snooper.exe, oder geben Sie Snooper.exe ein, und drücken Sie dann die EINGABETASTE, wenn Sie die Befehlszeile oder die lync Server-Verwaltungsshell verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d92d-114">Double-click Snooper.exe or type Snooper.exe, and then press ENTER if you are using the command line or Lync Server Management Shell.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8d92d-115">In diesem Thema sollen keine Problembehandlungstechniken beschrieben und behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8d92d-115">The intent of this topic is not to detail and discuss troubleshooting techniques.</span></span> <span data-ttu-id="8d92d-116">Die Problembehandlung und die damit verbundenen Prozesse sind ein komplexes Thema.</span><span class="sxs-lookup"><span data-stu-id="8d92d-116">Troubleshooting and the processes around it is a complex subject.</span></span> <span data-ttu-id="8d92d-117">Details zu den Grundlagen der Problembehandlung und zur Problembehandlung bei bestimmten Arbeitslasten finden Sie im Microsoft lync Server 2010 Resource Kit-Handbuch unter <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A> .</span><span class="sxs-lookup"><span data-stu-id="8d92d-117">For details about troubleshooting basics and troubleshooting specific workloads, see the Microsoft Lync Server 2010 Resource Kit book at <A href="https://go.microsoft.com/fwlink/p/?linkid=211003">https://go.microsoft.com/fwlink/p/?linkId=211003</A>.</span></span> <span data-ttu-id="8d92d-118">Die Prozesse und Verfahren gelten weiterhin für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="8d92d-118">The processes and procedures still apply to Lync Server 2013.</span></span>



</div>

<span data-ttu-id="8d92d-119">Lync Server 2013 führt eine aktualisierte Version von Snooper mit einigen neuen Features ein.</span><span class="sxs-lookup"><span data-stu-id="8d92d-119">Lync Server 2013 introduces an updated version of Snooper that includes some new features.</span></span> <span data-ttu-id="8d92d-120">Der folgende Screenshot zeigt die Version von Snooper von Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="8d92d-120">The following screen shot shows the version of Snooper from Office Communications Server 2007.</span></span>

<span data-ttu-id="8d92d-121">![Office Communications 2007-Version von Snooper.](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Office Communications 2007-Version von Snooper.")</span><span class="sxs-lookup"><span data-stu-id="8d92d-121">![Office Communications 2007 version of Snooper.](images/JJ721879.129503a8-8edd-4bb0-a68f-c43f9a548b93(OCS.15).jpg "Office Communications 2007 version of Snooper.")</span></span>

<span data-ttu-id="8d92d-122">Der folgende Screenshot zeigt die neue Version von Snooper, die in den lync Server 2013-Debug-Tools enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8d92d-122">The following screen shot shows the new version of Snooper included in the Lync Server 2013 Debug Tools.</span></span>

<span data-ttu-id="8d92d-123">![Lync Server 2013-Version von Snooper.](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Lync Server 2013-Version von Snooper.")</span><span class="sxs-lookup"><span data-stu-id="8d92d-123">![Lync Server 2013 version of Snooper.](images/JJ721879.131495dd-8220-4ae4-af37-0ac5c318fd45(OCS.15).jpg "Lync Server 2013 version of Snooper.")</span></span>

<span data-ttu-id="8d92d-124">Der folgende Screenshot zeigt die Symbolleiste mit häufig verwendeten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8d92d-124">The following screen shot shows the toolbar with frequently used functions.</span></span>

<span data-ttu-id="8d92d-125">![Snooper 2013-Symbolleiste.](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Snooper 2013-Symbolleiste.")</span><span class="sxs-lookup"><span data-stu-id="8d92d-125">![Snooper 2013 toolbar.](images/JJ721879.989249c5-a33e-4251-b8b4-411019cc12b2(OCS.15).jpg "Snooper 2013 toolbar.")</span></span>

<span data-ttu-id="8d92d-126">Und das neueste Feature, das einen Wert hinzufügt, ist die Diagrammansicht Flussdiagramm (Anruffluss).</span><span class="sxs-lookup"><span data-stu-id="8d92d-126">And, the newest feature that adds value is the Flow Chart (call flow) diagram view.</span></span> <span data-ttu-id="8d92d-127">Sie wählen einen Nachrichtenfluss auf dem Reiter **Nachricht** und klicken Sie auf die Schaltfläche **Anruffluss** .</span><span class="sxs-lookup"><span data-stu-id="8d92d-127">You select a message flow in the **Message** tab and click the **Call Flow** button.</span></span> <span data-ttu-id="8d92d-128">Während Sie die Nachrichten durchlaufen, wird das Anruffluss Diagramm mit neuen Daten aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8d92d-128">As you proceed through the messages, the call flow diagram updates with new data.</span></span>

<span data-ttu-id="8d92d-129">![Snooper 2013-Anruffluss Diagramm](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Snooper 2013-Anruffluss Diagramm")</span><span class="sxs-lookup"><span data-stu-id="8d92d-129">![Snooper 2013 call flow diagram.](images/JJ721879.bb8be45d-a842-48fe-86f8-380207d70bab(OCS.15).jpg "Snooper 2013 call flow diagram.")</span></span>

<span data-ttu-id="8d92d-130">Sie können mit der Maus auf die Diagrammansicht zeigen und Details zu den Nachrichten und dem Inhalt der Flüsse und Nachrichten sowie zu den Serverelementen abrufen.</span><span class="sxs-lookup"><span data-stu-id="8d92d-130">You can hover over the diagram view and get details about the messages and content of the flows and messages as well as the server elements.</span></span> <span data-ttu-id="8d92d-131">Klicken Sie auf einen beliebigen Anruffluss Pfeil, um in der Ansicht Nachrichten zu der Nachricht zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="8d92d-131">Click on any call flow arrow to go to the message in the Messages view.</span></span>

<span data-ttu-id="8d92d-132">![Nachrichtendetails des Anruffluss Diagramms.](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "Nachrichtendetails des Anruffluss Diagramms.")</span><span class="sxs-lookup"><span data-stu-id="8d92d-132">![Call flow diagram message details.](images/JJ721879.1147d720-38a9-4bda-8361-78f27ecde3d1(OCS.15).jpg "Call flow diagram message details.")</span></span>

<div>

## <a name="to-open-a-log-file-in-snooper"></a><span data-ttu-id="8d92d-133">So öffnen Sie eine Protokolldatei in Snooper</span><span class="sxs-lookup"><span data-stu-id="8d92d-133">To open a log file in Snooper</span></span>

1.  <span data-ttu-id="8d92d-p106">Zum Öffnen von Protokolldateien mithilfe von Snooper benötigen Sie Lesezugriff für die Protokolldateien. Für den Zugriff auf die Protokolldateien mithilfe von Snooper müssen Sie ein Mitglied der rollenbasierten Zugriffssteuerungs-Sicherheitsgruppe „CsAdministrator“ oder „CsServerAdministrator“ oder einer benutzerdefinierten rollenbasierten Zugriffssteuerungsrolle sein, die eine dieser beiden Gruppen enthält.</span><span class="sxs-lookup"><span data-stu-id="8d92d-p106">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files you must be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="8d92d-136">Wechseln Sie nach der Installation der lync Server-Debugging-Tools (LyncDebugTools.msi) in Windows-Explorer oder über die Befehlszeile in den Speicherort von Snooper.exe.</span><span class="sxs-lookup"><span data-stu-id="8d92d-136">After the installation of the Lync Server Debugging Tools (LyncDebugTools.msi), change directory to the location of Snooper.exe using Windows Explorer or from the command line.</span></span> <span data-ttu-id="8d92d-137">Standardmäßig befinden sich die Debug-Tools unter C: \\ Programmdateien \\ Microsoft lync Server 2013 \\ -Debugging-Tools.</span><span class="sxs-lookup"><span data-stu-id="8d92d-137">By default, the debugging tools are located in C:\\Program Files\\Microsoft Lync Server 2013\\Debugging Tools.</span></span> <span data-ttu-id="8d92d-138">Führen Sie „Snooper.exe“ mittels Doppelklick aus.</span><span class="sxs-lookup"><span data-stu-id="8d92d-138">Double-click or run Snooper.exe.</span></span>

3.  <span data-ttu-id="8d92d-139">Nachdem Snooper geöffnet wurde, klicken Sie mit der rechten Maustaste auf **File** (Datei), klicken Sie auf **OpenFile** (Datei öffnen), suchen Sie nach Ihren Protokolldateien, wählen Sie eine Datei im Dialogfeld **Open** (Öffnen) aus und klicken Sie dann auf **Open** (Öffnen).</span><span class="sxs-lookup"><span data-stu-id="8d92d-139">After Snooper is open, right-click **File**, click **OpenFile**, find your log files, select a file in the **Open** dialog box, and then click **Open**.</span></span>

4.  <span data-ttu-id="8d92d-140">Die Ablaufverfolgungsmeldungen werden auf der Registerkarte **Trace** (Ablaufverfolgung) angezeigt. Klicken Sie auf die Registerkarte **Messages** (Nachrichten), um die Nachrichteninhalte der erfassten Ablaufverfolgungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d92d-140">The log file’s **Trace** messages are displayed on the **Trace** tab. Click the **Messages** tab to view the message contents of the collected traces.</span></span>

</div>

<div>

## <a name="to-display-a-call-flow-diagram"></a><span data-ttu-id="8d92d-141">So zeigen Sie ein Anrufflussdiagramm an</span><span class="sxs-lookup"><span data-stu-id="8d92d-141">To display a call flow diagram</span></span>

1.  <span data-ttu-id="8d92d-p108">Zum Öffnen von Protokolldateien mithilfe von Snooper benötigen Sie Lesezugriff für die Protokolldateien. Für den Zugriff auf die Protokolldateien mithilfe von Snooper müssen Sie ein Mitglied der rollenbasierten Zugriffssteuerungs-Sicherheitsgruppe „CsAdministrator“ oder „CsServerAdministrator“ oder einer benutzerdefinierten rollenbasierten Zugriffssteuerungsrolle sein, die eine dieser beiden Gruppen enthält.</span><span class="sxs-lookup"><span data-stu-id="8d92d-p108">To use Snooper and open log files, you need read access to the log files. To use Snooper and access the log files, you need to be a member of the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span>

2.  <span data-ttu-id="8d92d-144">Öffnen Sie eine Protokolldatei und klicken Sie auf die Registerkarte **Messages** (Nachrichten), wählen Sie eine Unterhaltung in der Nachrichtenansicht aus oder wählen Sie eine Ablaufverfolgungskomponente auf der Registerkarte **Trace** (Ablaufverfolgung) aus.</span><span class="sxs-lookup"><span data-stu-id="8d92d-144">Open a log file and click the **Messages** tab, select a conversation in the messages view or select a trace component on the **Trace** tab.</span></span>

3.  <span data-ttu-id="8d92d-145">Klicken Sie auf **Call Flow** (Anruffluss).</span><span class="sxs-lookup"><span data-stu-id="8d92d-145">Click **Call Flow**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8d92d-p109">Wenn Sie auf eine Nachricht oder Ablaufverfolgung klicken, die nicht Bestandteil eines Anrufflusses ist, wird das Diagramm nicht angezeigt. Außerdem wird unten in Snooper die Statusmeldung angezeigt, dass diese Nachricht nicht für den Anruffluss in Frage kommt. Wählen Sie eine andere Nachricht oder Ablaufverfolgung aus. Der Anruffluss wird angezeigt, falls die Nachricht oder Ablaufverfolgung Bestandteil eines Anrufflusses ist.</span><span class="sxs-lookup"><span data-stu-id="8d92d-p109">If you click on a message or trace that is not part of a call flow, the diagram will not appear and a status message appears at the bottom of Snooper stating “This message is not eligible for callfow”. Choose another message or trace and the call flow will appear if the message or trace is part of a call flow.</span></span>

    
    </div>

4.  <span data-ttu-id="8d92d-148">Navigieren Sie in den Nachrichten oder Ablaufverfolgungszeilen und überprüfen Sie, ob das Anrufflussdiagramm aktualisiert oder geändert und ein neues Diagramm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8d92d-148">Move through the Messages or the Trace lines and note whether the call flow diagram updates or changes to display a new diagram.</span></span>

5.  <span data-ttu-id="8d92d-149">Zeigen Sie auf Elemente, um Informationen zu Anrufnachrichten, Endpunkten und sonstigen Komponenten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8d92d-149">Hover over elements to get information about call messages, endpoints, and other components.</span></span>

<span data-ttu-id="8d92d-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d92d-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

