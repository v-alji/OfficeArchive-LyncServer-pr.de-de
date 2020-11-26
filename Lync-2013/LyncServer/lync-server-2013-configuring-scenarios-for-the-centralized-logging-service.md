---
title: 'Lync Server 2013: Konfigurieren von Szenarien für den zentralisierten Protokollierungsdienst'
description: 'Lync Server 2013: Konfigurieren von Szenarien für den zentralisierten Protokollierungsdienst'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring scenarios for the Centralized Logging Service
ms:assetid: 6c3bf826-e7fd-4002-95dc-01020641ef01
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688085(v=OCS.15)
ms:contentKeyID: 49733682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1bf3f569ae8d2596f735851ae3d5d6c55f022b09
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432674"
---
# <a name="configuring-scenarios-for-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="1632f-103">Konfigurieren von Szenarien für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1632f-103">Configuring scenarios for the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1632f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1632f-104">

<span> </span></span></span>

<span data-ttu-id="1632f-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="1632f-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="1632f-106">Szenarien definieren den Bereich (Global, Site, Pool oder Computer) und welche Anbieter im zentralisierten Protokollierungsdienst zu verwenden sind.</span><span class="sxs-lookup"><span data-stu-id="1632f-106">Scenarios define the scope (that is, global, site, pool, or computer) and what providers to use in the Centralized Logging Service.</span></span> <span data-ttu-id="1632f-107">Mithilfe von Szenarien können Sie die Ablaufverfolgung für Dienstanbieter aktivieren oder deaktivieren (z. B. bezüglich S4, SIPStack, IM und Anwesenheit).</span><span class="sxs-lookup"><span data-stu-id="1632f-107">By using scenarios, you enable or disable tracing on providers (for example, S4, SIPStack, IM, and Presence).</span></span> <span data-ttu-id="1632f-108">Durch das Konfigurieren eines Szenarios können Sie alle Dienstanbieter für eine bestimmte logische Sammlung gruppieren, die sich mit einem bestimmten Problemzustand befassen.</span><span class="sxs-lookup"><span data-stu-id="1632f-108">By configuring a scenario, you can group all of the providers for a given logical collection that address a specific problem condition.</span></span> <span data-ttu-id="1632f-109">Wenn Sie feststellen, dass ein Szenario geändert werden muss, um die Anforderungen zur Problembehandlung und Protokollierung zu erfüllen, bietet Ihnen die lync Server 2013-Debug-Tools ein Windows PowerShell-Modul mit dem Namen *ClsController. psm1* , das eine Funktion mit dem Namen *Edit-CsClsScenario* enthält.</span><span class="sxs-lookup"><span data-stu-id="1632f-109">If you find that a scenario needs to be modified to meet your troubleshooting and logging needs, the Lync Server 2013 Debug Tools provides you a Windows PowerShell module named *ClsController.psm1* that contains a function named *Edit-CsClsScenario*.</span></span> <span data-ttu-id="1632f-110">Dieses Modul soll dazu dienen, die Eigenschaften des betreffenden Szenarios zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="1632f-110">The purpose of the module is to edit the properties of the named scenario.</span></span> <span data-ttu-id="1632f-111">Beispiele für die Funktionsweise des Moduls erhalten Sie in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="1632f-111">Examples of how this module works are provided in this topic.</span></span> <span data-ttu-id="1632f-112">Die lync Server 2013-Debug-Tools werden über den folgenden Link heruntergeladen: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257)</span><span class="sxs-lookup"><span data-stu-id="1632f-112">The Lync Server 2013 Debug Tools are downloaded from the following link: [https://go.microsoft.com/fwlink/?LinkId=285257](https://go.microsoft.com/fwlink/?linkid=285257)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1632f-113">Für einen bestimmten Bereich – Website, Global, Pool oder Computer – können Sie maximal zwei Szenarien zu einem bestimmten Zeitpunkt ausführen.</span><span class="sxs-lookup"><span data-stu-id="1632f-113">For any given scope—site, global, pool or computer—you can run a maximum of two scenarios at any given time.</span></span> <span data-ttu-id="1632f-114">Um zu ermitteln, welche Szenarien zurzeit ausgeführt werden, verwenden Sie Windows PowerShell und <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsClsScenario">Get-CsClsScenario</A>.</span><span class="sxs-lookup"><span data-stu-id="1632f-114">To determine which scenarios are currently running, use Windows PowerShell and <A href="https://docs.microsoft.com/powershell/module/skype/Get-CsClsScenario">Get-CsClsScenario</A>.</span></span> <span data-ttu-id="1632f-115">Mithilfe von Windows PowerShell und der <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClsScenario">CsClsScenario</A>können Sie dynamisch ändern, welche Szenarien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1632f-115">By using Windows PowerShell and <A href="https://docs.microsoft.com/powershell/module/skype/Set-CsClsScenario">Set-CsClsScenario</A>, you can dynamically change which scenarios are running.</span></span> <span data-ttu-id="1632f-116">Sie können ändern, welche Szenarien während einer Protokollierungssitzung ausgeführt werden, um die Daten, die Sie sammeln, und von welchen Anbietern anzupassen oder zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="1632f-116">You can modify which scenarios are running during a logging session to adjust or refine the data you are collecting and from which providers.</span></span>



</div>

<span data-ttu-id="1632f-117">Wenn Sie die Funktionen für den zentralisierten Protokollierungsdienst mithilfe der lync Server-Verwaltungsshell ausführen möchten, müssen Sie ein Mitglied der CsAdministrator-oder CsServerAdministrator-Sicherheitsgruppe (Role-Based Access Control, RBAC) oder eine benutzerdefinierte RBAC-Rolle sein, die eine dieser beiden Gruppen enthält.</span><span class="sxs-lookup"><span data-stu-id="1632f-117">To run the Centralized Logging Service functions by using the Lync Server Management Shell, you must be a member of either the CsAdministrator or the CsServerAdministrator role-based access control (RBAC) security groups, or a custom RBAC role that contains either of these two groups.</span></span> <span data-ttu-id="1632f-118">Führen Sie den folgenden Befehl in der lync Server-Verwaltungsshell oder in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde, einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="1632f-118">To return a list of all the RBAC roles this cmdlet has been assigned to, including any custom RBAC roles you have created yourself, run the following command from the Lync Server Management Shell or the Windows PowerShell prompt:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Lync Server 2013 cmdlet"}

<span data-ttu-id="1632f-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1632f-119">For example:</span></span>

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsClsConfiguration"}

<span data-ttu-id="1632f-120">Nachfolgend wird beschrieben, wie Sie ein Szenario definieren, ein Szenario ändern, wie Sie abrufen, welche Szenarien ausgeführt werden, wie Sie ein Szenario entfernen und wie Sie die Inhalte eines Szenarios auf eine optimale Problembehandlung abstimmen können.</span><span class="sxs-lookup"><span data-stu-id="1632f-120">The remainder of this topic focuses on how to define a scenario, modify a scenario, retrieve what scenarios are running, remove a scenario, and specify what a scenario contains to optimize your troubleshooting.</span></span> <span data-ttu-id="1632f-121">Es gibt zwei Möglichkeiten zum Ausgeben von Befehlen für zentralisierte Protokollierungsdienste.</span><span class="sxs-lookup"><span data-stu-id="1632f-121">There are two ways to issue Centralized Logging Service commands.</span></span> <span data-ttu-id="1632f-122">Sie können die CLSController.exe verwenden, die sich standardmäßig im Verzeichnis C: \\ Programmdateien \\ Allgemeine Dateien \\ Microsoft lync Server 2013 \\ CLSAgent befindet.</span><span class="sxs-lookup"><span data-stu-id="1632f-122">You can use the CLSController.exe that is located, by default, in the directory C:\\Program Files\\Common Files\\Microsoft Lync Server 2013\\CLSAgent.</span></span> <span data-ttu-id="1632f-123">Oder Sie können die lync Server-Verwaltungsshell zum Ausgeben von Windows PowerShell-Befehlen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1632f-123">Or, you can use the Lync Server Management Shell to issue Windows PowerShell commands.</span></span> <span data-ttu-id="1632f-124">Der wichtige Unterschied besteht darin, dass bei der Verwendung von CLSController.exe in der Befehlszeile eine begrenzte Auswahl von Szenarien zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="1632f-124">The important distinction is that when you use CLSController.exe at the command line there is a finite selection of scenarios available.</span></span> <span data-ttu-id="1632f-125">Wenn Sie Windows PowerShell verwenden, können Sie neue Szenarien für die Verwendung in ihren Protokollierungssitzungen definieren.</span><span class="sxs-lookup"><span data-stu-id="1632f-125">When you use Windows PowerShell, you can define new scenarios for use in your logging sessions.</span></span>

<span data-ttu-id="1632f-126">Wie in der [Übersicht über den zentralisierten Protokollierungsdienst in lync Server 2013](lync-server-2013-overview-of-the-centralized-logging-service.md)eingeführt, sind die Elemente eines Szenarios:</span><span class="sxs-lookup"><span data-stu-id="1632f-126">As introduced in [Overview of the Centralized Logging Service in Lync Server 2013](lync-server-2013-overview-of-the-centralized-logging-service.md), the elements of a scenario are:</span></span>

  - <span data-ttu-id="1632f-127">**Anbieter**   Wenn Sie mit OCSLogger vertraut sind, sind Anbieter die Komponenten, die Sie angeben, um OCSLogger zu informieren, von welchem das Ablaufverfolgungsmodul Protokolle sammeln soll.</span><span class="sxs-lookup"><span data-stu-id="1632f-127">**Providers**   If you are familiar with OCSLogger, providers are the components that you choose to tell OCSLogger what the tracing engine should collect logs from.</span></span> <span data-ttu-id="1632f-128">Die Anbieter sind die gleichen Komponenten und haben in vielen Fällen denselben Namen wie die Komponenten in OCSLogger.</span><span class="sxs-lookup"><span data-stu-id="1632f-128">The providers are the same components, and in many cases have the same name as the components in OCSLogger.</span></span> <span data-ttu-id="1632f-129">Wenn Sie mit OCSLogger nicht vertraut sind, sind Anbieterserver rollenspezifische Komponenten, von denen der zentralisierte Protokollierungsdienst Protokolle sammeln kann.</span><span class="sxs-lookup"><span data-stu-id="1632f-129">If you are not familiar with OCSLogger, providers are server role specific components that the Centralized Logging Service can collect logs from.</span></span> <span data-ttu-id="1632f-130">Details zur Konfiguration von Anbietern finden Sie unter [Konfigurieren von Anbietern für den zentralisierten Protokollierungsdienst in lync Server 2013](lync-server-2013-configuring-providers-for-centralized-logging-service.md).</span><span class="sxs-lookup"><span data-stu-id="1632f-130">For details about the configuration of providers, see [Configuring providers for Centralized Logging Service in Lync Server 2013](lync-server-2013-configuring-providers-for-centralized-logging-service.md).</span></span>

  - <span data-ttu-id="1632f-131">**Identität**   Der Parameter – Identity legt den Bereich und den Namen des Szenarios fest.</span><span class="sxs-lookup"><span data-stu-id="1632f-131">**Identity**   The parameter –Identity sets the scope and name of the scenario.</span></span> <span data-ttu-id="1632f-132">So können Sie beispielsweise einen Bereich von "Global" festlegen und das Szenario mit "LyssServiceScenario" identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1632f-132">For example, you could set a scope of “global” and identify the scenario with “LyssServiceScenario”.</span></span> <span data-ttu-id="1632f-133">Wenn Sie die beiden kombinieren, definieren Sie die Identität (beispielsweise "Global/LyssServiceScenario").</span><span class="sxs-lookup"><span data-stu-id="1632f-133">When you combine the two, you define the Identity (for example, “global/LyssServiceScenario”).</span></span>
    
    <span data-ttu-id="1632f-p107">Optional können Sie auch die Parameter „–Name“ und „–Parent“ verwenden. Sie definieren den Parameter „Name“, um das Szenario eindeutig zu identifizieren. Wenn Sie „Name“ verwenden, müssen Sie auch „Parent“ verwenden, um das Szenario entweder einem globalen oder einem standortweiten Geltungsbereich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1632f-p107">Optionally, you can use the –Name and –Parent parameters. You define the Name parameter to uniquely identify the scenario. If you use Name, you must also use Parent to add the scenario to either global or site.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1632f-137">Falls Sie die Parameter „Name“ und „Parent“ verwenden, können Sie den Parameter <STRONG>–Identity</STRONG> nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="1632f-137">If you use the Name and Parent parameters, you cannot use the <STRONG>–Identity</STRONG> parameter.</span></span>

    
    </div>

<div>

## <a name="to-create-a-new-scenario-with-the-new-csclsscenario-cmdlet"></a><span data-ttu-id="1632f-138">So erstellen Sie ein neues Szenario mit dem Cmdlet „New-CsClsScenario“</span><span class="sxs-lookup"><span data-stu-id="1632f-138">To create a new scenario with the New-CsClsScenario cmdlet</span></span>

1.  <span data-ttu-id="1632f-139">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-139">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-p108">Verwenden Sie für die Erstellung eines neuen Szenarios für eine Protokollierungssitzung [New-CsClsProvider](https://docs.microsoft.com/powershell/module/skype/New-CsClsProvider) und definieren Sie den Namen für das Szenario (d. h. dessen eindeutige Identifikation). Wählen Sie als Typ für das Protokollierungsformat entweder WPP (Windows-Präprozessorformat für die Softwareablaufverfolgung, Standard), EventLog (Windows-Ereignisprotokoll-Format) oder IISLog (Datei im ASCII-Format basierend auf dem IIS-Protokolldatei-Format). Definieren Sie anschließend den Protokolliergrad (gemäß der Definition im entsprechenden Abschnitt in diesem Thema) und die Flags (gemäß der Definition im entsprechenden Abschnitt in diesem Thema).</span><span class="sxs-lookup"><span data-stu-id="1632f-p108">To create a new scenario for a logging session, use [New-CsClsProvider](https://docs.microsoft.com/powershell/module/skype/New-CsClsProvider) and define the name of the scenario (that is, how it will be uniquely identified). Choose a type of logging format from WPP (that is, Windows software tracing preprocessor and is the default), EventLog (that is, Windows event log format), or IISLog (that is, ASCII format file based on the IIS log file format). Next, define Level (as the defined under Logging Levels in this topic), and Flags (as defined under Flags in this topic).</span></span>
    
    <span data-ttu-id="1632f-143">Für dieses Beispielszenario verwenden wir LyssProvider als Beispiel für die Anbietervariable.</span><span class="sxs-lookup"><span data-stu-id="1632f-143">For this example scenario, we use LyssProvider as the example provider variable.</span></span>
    
    <span data-ttu-id="1632f-144">Geben Sie zum Erstellen eines Szenarios mit den definierten Optionen Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1632f-144">To create a scenario using the options defined, type:</span></span>
    
        New-CsClsScenario -Identity <scope>/<unique scenario name> -Provider <provider variable>
    
    <span data-ttu-id="1632f-145">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1632f-145">For example:</span></span>
    
        New-CsClsScenario -Identity "site:Redmond/LyssServiceScenario" -Provider $LyssProvider
    
    <span data-ttu-id="1632f-146">Alternatives Format unter Verwendung von „–Name“ und „–Parent“:</span><span class="sxs-lookup"><span data-stu-id="1632f-146">The alternate format using –Name and –Parent:</span></span>
    
        New-CsClsScenario -Name "LyssServiceScenario" -Parent "site:Redmond" -Provider $LyssProvider

</div>

<div>

## <a name="to-create-a-new-scenario-with-multiple-providers-with-the-new-csclsscenario-cmdlet"></a><span data-ttu-id="1632f-147">So erstellen Sie ein neues Szenario mit mehreren Anbietern mithilfe des Cmdlets „New-CsClsScenario“</span><span class="sxs-lookup"><span data-stu-id="1632f-147">To create a new scenario with multiple providers with the New-CsClsScenario cmdlet</span></span>

1.  <span data-ttu-id="1632f-148">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-148">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-149">Für jeweils einen Geltungsbereich können Sie nur zwei Szenarien erstellen.</span><span class="sxs-lookup"><span data-stu-id="1632f-149">You are limited to two scenarios per scope.</span></span> <span data-ttu-id="1632f-150">Sie sind jedoch nicht auf eine feste Anzahl von Anbietern beschränkt.</span><span class="sxs-lookup"><span data-stu-id="1632f-150">However, you are not limited to a set number of providers.</span></span> <span data-ttu-id="1632f-151">In diesem Beispiel wird davon ausgegangen, dass drei Anbieter erstellt wurden, die Sie allesamt dem Szenario zuweisen möchten, das Sie soeben erstellen.</span><span class="sxs-lookup"><span data-stu-id="1632f-151">In this example, assume that we have created three providers, and you want to assign all three to the scenario you are defining.</span></span> <span data-ttu-id="1632f-152">Die Variablennamen der Anbieter lauten „LyssProvider“, „ABServerProvider“ und „SIPStackProvider“.</span><span class="sxs-lookup"><span data-stu-id="1632f-152">The provider variable names are LyssProvider, ABServerProvider, and SIPStackProvider.</span></span> <span data-ttu-id="1632f-153">Wenn Sie einem Szenario mehrere Anbieter definieren und zuweisen möchten, geben Sie Folgendes an einer lync Server-Verwaltungsshell oder Windows PowerShell-Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="1632f-153">To define and assign multiple providers to a scenario, type the following at a Lync Server Management Shell or Windows PowerShell command prompt:</span></span>
    
        New-CsClsScenario -Identity "site:Redmond/CollectDataScenario" -Provider @{Add=$LyssProvider, $ABServerProvider,  $SIPStackProvider}
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1632f-154">Wie es in Windows PowerShell bekannt ist, wird die Konvention zum Erstellen einer Hashtabelle mit Werten unter dem Namen <CODE>@{&lt;variable&gt;=&lt;value1&gt;, &lt;value2&gt;, &lt;value&gt;...}</CODE> <EM>splatting</EM>.</span><span class="sxs-lookup"><span data-stu-id="1632f-154">As it is known in Windows PowerShell, the convention for creating a hash table of values using <CODE>@{&lt;variable&gt;=&lt;value1&gt;, &lt;value2&gt;, &lt;value&gt;...}</CODE> is known as <EM>splatting</EM>.</span></span> <span data-ttu-id="1632f-155">Ausführliche Informationen zu splatting in Windows PowerShell finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=267760">https://go.microsoft.com/fwlink/p/?LinkId=267760</A> .</span><span class="sxs-lookup"><span data-stu-id="1632f-155">For details about splatting in Windows PowerShell, see <A href="https://go.microsoft.com/fwlink/p/?linkid=267760">https://go.microsoft.com/fwlink/p/?LinkId=267760</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="to-modify-an-existing-scenario-with-the-set-csclsscenario-cmdlet"></a><span data-ttu-id="1632f-156">So ändern Sie ein vorhandenes Szenario mithilfe des Cmdlets „Set-CsClsScenario“</span><span class="sxs-lookup"><span data-stu-id="1632f-156">To modify an existing scenario with the Set-CsClsScenario cmdlet</span></span>

1.  <span data-ttu-id="1632f-157">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-157">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-p111">Es gilt eine Beschränkung auf zwei Szenarien pro Geltungsbereich. Sie können jederzeit ändern, welche Szenarien ausgeführt werden, auch wenn gerade eine Protokollerfassungssitzung läuft. Falls Sie die ausgeführten Szenarien neu definieren, verwendet die aktuelle Protokollierungssitzung ab diesem Zeitpunkt nicht mehr das entfernte Szenario, sondern stattdessen das neue Szenario. Die Protokollinformationen, die im Rahmen des entfernten Szenarios erfasst wurden, verbleiben jedoch in den erfassten Protokollen. Gehen Sie wie folgt vor, um ein neues Szenarios zu definieren (hierbei wird angenommen, dass ein bereits definierter Anbieter namens „S4Provider“ hinzugefügt wurde):</span><span class="sxs-lookup"><span data-stu-id="1632f-p111">You are limited to two scenarios per scope. You can change which scenarios are running at any time, even when a logging capture session is in process. If you redefine the running scenarios, the current logging session will stop using the scenario that was removed and then begin using the new scenario. However, the logging information that was captured with the removed scenario remains in the captured logs. To define a new scenario, do the following (that is, assuming the addition of an already defined provider named “S4Provider”):</span></span>
    
        Set-CsClsScenario -Identity <name of scope and scenario defined by New-CsClsScenario> -Provider @{Add=<new provider to add>}
    
    <span data-ttu-id="1632f-163">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1632f-163">For example:</span></span>
    
        Set-CsClsScenario -Identity "site:Redmond/LyssServiceScenario" -Provider @{Add=$S4Provider}
    
    <span data-ttu-id="1632f-p112">Falls Sie Anbieter ersetzen möchten, definieren Sie einen einzelnen Anbieter oder eine kommagetrennte Liste mit Anbietern, um die aktuelle Gruppe zu ersetzen. Für den Fall, dass Sie nur einen von vielen Anbietern ersetzen möchten, fügen Sie die aktuellen Anbieter zu den neuen Anbietern hinzu, um eine neue Gruppe von Anbietern zu erstellen, die sowohl die neuen als auch die zuvor vorhandenen Anbieter enthält. Geben Sie Folgendes ein, um sämtliche Anbieter durch eine neue Gruppe zu ersetzen:</span><span class="sxs-lookup"><span data-stu-id="1632f-p112">If you want to replace providers, define a single provider or a comma separated list of providers to replace the current set. If you only want to replace one of many providers, add the current providers with the new providers to create a new set of providers that contains both new providers and existing providers. To replace all providers with a new set, type the following:</span></span>
    
        Set-CsClsScenario -Identity <name of scope and scenario defined by New-CsClsScenario> -Provider @{Replace=<providers to replace existing provider set>}
    
    <span data-ttu-id="1632f-167">Beispiel, bei dem die aktuelle aus „$LyssProvider“, „$ABServerProvider“ und „$SIPStackProvider“ bestehende Gruppe durch „$LyssServiceProvider“ ersetzt wird:</span><span class="sxs-lookup"><span data-stu-id="1632f-167">For example, to replace the current set of $LyssProvider, $ABServerProvider, and $SIPStackProvider with $LyssServiceProvider:</span></span>
    
        Set-CsClsScenario -Identity "site:Redmond/LyssServiceScenario" -Provider @{Replace=$LyssServiceProvider}
    
    <span data-ttu-id="1632f-168">Geben Sie Folgendes ein, um lediglich den Anbieter „$LyssProvider“ aus der aktuellen Gruppe mit „$LyssProvider“, „$ABServerProvider“ und „$SIPStackProvider“ durch den Anbieter „$LyssServiceProvider“ zu ersetzen:</span><span class="sxs-lookup"><span data-stu-id="1632f-168">To replace just the $LyssProvider provider from the current set of $LyssProvider, $ABServerProvider, and $SIPStackProvider with $LyssServiceProvider, type the following:</span></span>
    
        Set-CsClsScenario -Identity "site:Redmond/LyssServiceScenario" -Provider @{Replace=$LyssServiceProvider, $ABServerProvider, $SIPStackProvider}

</div>

<div>

## <a name="to-remove-an-existing-scenario-with-the-remove-csclsscenario-cmdlet"></a><span data-ttu-id="1632f-169">So entfernen Sie ein vorhandenes Szenario mithilfe des Cmdlets „Remove-CsClsScenario“</span><span class="sxs-lookup"><span data-stu-id="1632f-169">To remove an existing scenario with the Remove-CsClsScenario cmdlet</span></span>

1.  <span data-ttu-id="1632f-170">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-170">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-171">Wenn Sie ein Szenario entfernen möchten, das zuvor definiert wurde, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1632f-171">If you want to remove a scenario that has been previously defined, type the following:</span></span>
    
        Remove-CsClsScenario -Identity <name of scope and scenario>
    
    <span data-ttu-id="1632f-172">Beispiel für das Entfernen des Szenarios „site:Redmond/LyssServiceScenario“:</span><span class="sxs-lookup"><span data-stu-id="1632f-172">For example, to remove the defined scenario site:Redmond/LyssServiceScenario:</span></span>
    
        Remove-CsClsScenario -Identity "site:Redmond/LyssServiceScenario"

<span data-ttu-id="1632f-173">Das Cmdlet **Remove-CsClsScenario** entfernt das angegebene Szenario. Die bereits erfassten Ablaufverfolgungen sind jedoch nach wie vor in den Protokollen verfügbar und können gesucht werden.</span><span class="sxs-lookup"><span data-stu-id="1632f-173">The **Remove-CsClsScenario** cmdlet removes the specified scenario, but the traces that have been captured are still available in the logs for you to search on.</span></span>

</div>

<div>

## <a name="to-load-and-unload-the-edit-csclsscenario-cmdlet-using-the-clscontrollerpsm1-module"></a><span data-ttu-id="1632f-174">So laden und Entladen Sie das Edit-CsClsScenario-Cmdlet mithilfe des ClsController. psm1-Moduls</span><span class="sxs-lookup"><span data-stu-id="1632f-174">To load and unload the Edit-CsClsScenario cmdlet using the ClsController.psm1 module</span></span>

1.  <span data-ttu-id="1632f-175">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-175">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="1632f-176">Das ClsController. psm1-Modul wird als separater Webdownload bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1632f-176">The ClsController.psm1 module is provided as a separate Web download.</span></span> <span data-ttu-id="1632f-177">Das Modul gehört zu den lync Server 2013-Debugging-Tools.</span><span class="sxs-lookup"><span data-stu-id="1632f-177">The module is part of the Lync Server 2013 Debugging tools.</span></span> <span data-ttu-id="1632f-178">Standardmäßig werden die Debug-Tools im Verzeichnis C:\Program Files\Lync Server 2013 \ Debugging Tools installiert.</span><span class="sxs-lookup"><span data-stu-id="1632f-178">By default, the debugging tools are installed in the directory C:\Program Files\Lync Server 2013\Debugging Tools.</span></span>

    
    </div>

2.  <span data-ttu-id="1632f-179">Geben Sie in der Windows PowerShell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1632f-179">From the Windows PowerShell, type:</span></span>
    
        Import-Module "C:\Program Files\Lync Server 2013\Debugging Tools\ClsController.psm1"
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="1632f-180">Durch erfolgreiches Laden des Moduls kehren Sie zur Windows PowerShell-Eingabeaufforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="1632f-180">Successful loading of the module returns you to the Windows PowerShell command prompt.</span></span> <span data-ttu-id="1632f-181">Um zu bestätigen, dass das Modul geladen wird und Edit-CsClsScenario verfügbar ist, geben Sie <CODE>Get-Help Edit-CsClsScenario</CODE> .</span><span class="sxs-lookup"><span data-stu-id="1632f-181">To confirm that the module is loaded and that Edit-CsClsScenario is available, type <CODE>Get-Help Edit-CsClsScenario</CODE>.</span></span> <span data-ttu-id="1632f-182">Daraufhin sollte die grundlegende Kurzfassung der Syntax für „EditCsClsScenario“ angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1632f-182">You should see the basic synopsis of the syntax for EditCsClsScenario.</span></span>

    
    </div>

3.  <span data-ttu-id="1632f-183">Geben Sie zum Entladen des Moduls Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="1632f-183">To unload the modules, type:</span></span>
    
        Remove-Module ClsController
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="1632f-184">Durch erfolgreiches Entladen des Moduls kehren Sie zur Windows PowerShell-Eingabeaufforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="1632f-184">Successful unloading of the module returns you to the Windows PowerShell command prompt.</span></span> <span data-ttu-id="1632f-185">Um zu bestätigen, dass das Modul entladen wird, geben Sie <CODE>Get-Help Edit-CsClsScenario</CODE> .</span><span class="sxs-lookup"><span data-stu-id="1632f-185">To confirm that the module is unloaded, type <CODE>Get-Help Edit-CsClsScenario</CODE>.</span></span> <span data-ttu-id="1632f-186">Windows PowerShell versucht, die Hilfe für das Cmdlet zu finden, und es wird ein Fehler ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1632f-186">Windows PowerShell will attempt to locate the help for the cmdlet and fail.</span></span>

    
    </div>

</div>

<div>

## <a name="to-remove-an-existing-provider-from-a-scenario-with-the-edit-clscontroller-module"></a><span data-ttu-id="1632f-187">So entfernen Sie einen vorhandenen Anbieter mithilfe des Edit-ClsController-Moduls aus einem Szenario</span><span class="sxs-lookup"><span data-stu-id="1632f-187">To remove an existing provider from a scenario with the Edit-ClsController module</span></span>

1.  <span data-ttu-id="1632f-188">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-188">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-189">Geben Sie Folgendes ein, um einen Anbieter aus dem Szenario „AlwaysOn“ zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="1632f-189">To remove a provider from the AlwaysOn scenario, type:</span></span>
    
        Edit-CsClsScenario -ScenarioName <string of the scenario to edit> -ProviderName <string of the provider to remove> -Remove
    
    <span data-ttu-id="1632f-190">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1632f-190">For Example:</span></span>
    
        Edit-CsClsScenario -ScenarioName AlwaysOn -ProviderName ChatServer -Remove
    
    <span data-ttu-id="1632f-p116">Bei den Parametern „ScenarioName“ und „ProviderName“ handelt es sich um Positionsparameter (d. h., dass sie in der erwarteten Position in der Eingabeaufforderung definiert werden müssen). Der Parametername muss nicht explizit definiert werden, sofern der Szenarioname an zweiter Position und der Anbieter an dritter Position steht (in Bezug auf den Namen des Cmdlets, der an erster Position steht):</span><span class="sxs-lookup"><span data-stu-id="1632f-p116">The parameters ScenarioName and ProviderName are positional (that is, they must be defined in the expected position in the command line) parameters. The parameter name does not have to be explicitly defined if the scenario name is in position two and the provider is in position three, relative to the name of the cmdlet as position one. Using this information, the previous command would be typed as:</span></span>
    
        Edit-CsClsScenario AlwaysOn ChatServer -Remove
    
    <span data-ttu-id="1632f-p117">Die Platzierung der Parameterwerte an einer bestimmten Position gilt nur für  „–Scenario“ und „–Provider“. Alle anderen Parameter müssen explizit definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1632f-p117">The positional placing of the parameter values applies only to –Scenario and –Provider. All other parameters must be explicitly defined.</span></span>

</div>

<div>

## <a name="to-add-a-provider-to-a-scenario-with-the-edit-clscontroller-module"></a><span data-ttu-id="1632f-196">So fügen Sie ein Szenario mit dem Modul „Edit-ClsController“ hinzu</span><span class="sxs-lookup"><span data-stu-id="1632f-196">To add a provider to a scenario with the Edit-ClsController module</span></span>

1.  <span data-ttu-id="1632f-197">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="1632f-197">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="1632f-198">Geben Sie Folgendes ein, um einen Anbieter zum Szenario „AlwaysOn“ hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="1632f-198">To add a provider to the AlwaysOn scenario, type:</span></span>
    
        Edit-CsClsScenario -ScenarioName <string of the scenario to edit> -ProviderName <string of the provider to add> -Level <string of type level> -Flags <string of type flags>
    
    <span data-ttu-id="1632f-199">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1632f-199">For Example:</span></span>
    
        Edit-CsClsScenario -ScenarioName AlwaysOn -ProviderName ChatServer -Level Info -Flags TF_COMPONENT
    
    <span data-ttu-id="1632f-200">\-LogLevel kann vom Typ fatal, Error, Warning, Info, Verbose, Debug oder all sein.</span><span class="sxs-lookup"><span data-stu-id="1632f-200">\-Loglevel can be of the type Fatal, Error, Warning, Info, Verbose, Debug, or All.</span></span> <span data-ttu-id="1632f-201">– Flags können beliebige der vom Anbieter unterstützten Flags sein, wie TF \_ -Komponente, TF \_ diag.</span><span class="sxs-lookup"><span data-stu-id="1632f-201">–Flags can be any of the flags that the provider supports, such as TF\_COMPONENT, TF\_DIAG.</span></span> <span data-ttu-id="1632f-202">Der Wert ALL ist für „–Flags“ ebenfalls möglich.</span><span class="sxs-lookup"><span data-stu-id="1632f-202">–Flags can also be of value ALL</span></span>
    
    <span data-ttu-id="1632f-p119">Das vorherige Beispiel kann auch mithilfe der Positionsfunktion des Cmdlets eingegeben werden. So würden Sie beispielsweise Folgendes eingeben, um „ChatServer“ zum Szenario „AlwaysOn“ hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="1632f-p119">The previous example can also be typed using the positional feature of the cmdlet. For example, to add the provider ChatServer to the AlwaysOn scenario, type:</span></span>
    
        Edit-CsClsScenario AlwaysOn ChatServer -Level Info -Flags ALL

<span data-ttu-id="1632f-205"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1632f-205"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

