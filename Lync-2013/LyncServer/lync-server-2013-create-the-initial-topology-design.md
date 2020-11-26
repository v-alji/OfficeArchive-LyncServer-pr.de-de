---
title: 'Lync Server 2013: Erstellen des anfänglichen Topologie-Designs'
description: 'Lync Server 2013: Erstellen des anfänglichen Topologie-Designs.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create the initial design
ms:assetid: f3131153-de14-41be-b1e6-7d4bb0191af1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615047(v=OCS.15)
ms:contentKeyID: 51541530
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c91bfe68a1de4a1f9862948edd708b8efa6a5c6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431582"
---
# <a name="create-the-initial-topology-design-for-lync-server-2013"></a><span data-ttu-id="ae4ea-103">Erstellen des anfänglichen Topologie-Designs für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae4ea-103">Create the initial topology design for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae4ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae4ea-104">

<span> </span></span></span>

<span data-ttu-id="ae4ea-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ae4ea-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ae4ea-106">Nachdem Sie die Installation von lync Server 2013, Planungstool, abgeschlossen haben, können Sie das Planungstool starten und mit dem Entwerfen der vorgeschlagenen lync Server 2013-Infrastruktur beginnen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-106">After you have finished installing the Lync Server 2013, Planning Tool, you are ready to start the Planning Tool and begin designing the proposed Lync Server 2013 infrastructure.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ae4ea-107">Das Planungstool ist ein Assistenten gesteuertes Tool mit detaillierten Leitfäden, mit deren Hilfe Sie Ihre Entscheidungsfindung beim Entwerfen Ihrer Websites und Topologie unterrichten können.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-107">The Planning Tool is a wizard-driven tool with detailed guides to inform your decision-making process in designing your sites and topology.</span></span> <span data-ttu-id="ae4ea-108">Dieses Thema ist nicht als umfassender Leitfaden zu verstehen, sondern dient lediglich dazu, Ihnen bei der Verwendung des Planungstools in ihren Entwurfs Sitzungen zu helfen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-108">This topic is intended not as an exhaustive guide, but simply to help get you started using the Planning Tool in your design sessions.</span></span>



</div>

<div>

## <a name="to-get-started-using-the-planning-tool-and-create-the-initial-design"></a><span data-ttu-id="ae4ea-109">So beginnen Sie mit der Verwendung des Planungstools und Erstellen des anfänglichen Entwurfs</span><span class="sxs-lookup"><span data-stu-id="ae4ea-109">To get started using the Planning Tool and create the initial design</span></span>

1.  <span data-ttu-id="ae4ea-110">Starten Sie lync Server 2013, Planungstool: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **Planungstool**.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-110">Start the Lync Server 2013, Planning Tool: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Planning Tool**.</span></span>

2.  <span data-ttu-id="ae4ea-111">Nachdem das Planungstool gestartet wurde, wird die Seite **Willkommen bei Planning Tool für Microsoft lync Server 2013** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-111">After the Planning Tool has started, the **Welcome to the Planning Tool for Microsoft Lync Server 2013** page appears.</span></span> <span data-ttu-id="ae4ea-112">Wählen Sie eine der folgenden Optionen, um zu beginnen:</span><span class="sxs-lookup"><span data-stu-id="ae4ea-112">Choose one of the following options to begin your design:</span></span>
    
      - <span data-ttu-id="ae4ea-113">**Option 1: Erste Schritte**   Durch Klicken auf " **Erste Schritte" erhalten Sie** eine bestimmte Reihe von Interview Fragen mit relevanten Auswahlmöglichkeiten, um die Kriterien zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-113">**Option 1: Get Started**   Clicking **Get Started** provides a specific series of interview questions with relevant selections to define the criteria.</span></span> <span data-ttu-id="ae4ea-114">Fahren Sie nach Beantwortung der anfänglichen Fragen in **Erste Schritte** mit dem Abschnitt **Standorte entwerfen** fort, um die Architektur Ihres Standorts zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-114">After you have finished the initial **Get Started** interview section, you proceed into **Design Sites** to define your site architecture.</span></span> <span data-ttu-id="ae4ea-115">Fahren Sie mit Schritt 3 fort, um diese Option abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-115">To complete this option, proceed to step 3.</span></span>
    
      - <span data-ttu-id="ae4ea-116">**Option 2: Entwerfen von Websites**   Wenn Sie auf der Willkommensseite auf " **Websites entwerfen** " klicken, werden die im Abschnitt " **Erste Schritte** " vorgestellten Fragen im Interview umgangen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-116">**Option 2: Design Sites**   Clicking **Design Sites** at the Welcome page bypasses the interview questions presented in the **Get Started** section.</span></span> <span data-ttu-id="ae4ea-117">Die Informationen, die anhand der Fragen im Abschnitt **Erste Schritte** erfasst worden wären, werden bei Auswahl dieser Option auf Standardwerte gesetzt.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-117">The information that would have been gathered by responding to the interview questions in **Get Started** section is set to default values with this option.</span></span> <span data-ttu-id="ae4ea-118">Durch Klicken auf **Standorte entwerfen** können erfahrene Nutzer, die für den Entwurf verantwortlich sind, die anfänglichen Fragen umgehen und die Standardwerte nach Bedarf auf der Startseite für den Abschnitt **Zentrale Standorte** ändern.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-118">By clicking **Design Sites**, the experienced designer can bypass the initial interview and change the default values, as needed, on the **Central Sites** start page.</span></span> <span data-ttu-id="ae4ea-119">Überspringen Sie die Schritte 3–5, und beginnen Sie mit Schritt 6, um diese Option abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-119">To complete this option, skip over steps 3-5 and start at step 6.</span></span>
    
      - <span data-ttu-id="ae4ea-120">**Option 3: Anzeigen der gespeicherten Topologie**   Wenn Sie bereits eine Topologie durch die vorherige Verwendung des Planungstools abgeschlossen und gespeichert haben, können Sie die meisten dieser Schritte überspringen und beginnen, indem Sie die Topologie öffnen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-120">**Option 3: Display Your Saved Topology**   If you have already completed and saved a topology through previous use of the Planning Tool, you can skip over most of these steps and start by opening and displaying the topology.</span></span> <span data-ttu-id="ae4ea-121">Sie können die Topologie ändern, aktualisieren, erneut speichern und anschließend nach Microsoft Excel oder Microsoft Visio exportieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-121">You can also make changes and updates to the topology, resave it, and then export it to Microsoft Excel or Microsoft Visio.</span></span> <span data-ttu-id="ae4ea-122">Überspringen Sie die Schritte 3–12 und beginnen Sie mit Schritt 13, um diese Option abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-122">To complete this option, skip over steps 3-12 and start at step 13.</span></span>

3.  <span data-ttu-id="ae4ea-123">Klicken Sie auf **Erste Schritte** , um mit dem Entwerfen Ihrer lync Server 2013-Topologie zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-123">Click **Get Started** to begin designing your Lync Server 2013 topology.</span></span>

4.  <span data-ttu-id="ae4ea-p106">Beantworten Sie die Fragen in jedem Abschnitt, indem Sie die geeigneten Kriterien für Ihren Entwurf auswählen, und klicken Sie anschließend auf **Weiter**, um mit der nächsten Seite des Assistenten fortzufahren. Klicken Sie auf **Zurück**, um Änderungen auf vorherigen Seiten vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-p106">Answer each section by selecting the appropriate criteria for your design, and then click **Next** to proceed to the next Wizard page. Click **Back** to make changes on previous pages.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="ae4ea-126">Jede Seite bietet eine Beschreibung der Auswahlkriterien sowie Empfehlungen basierend auf bevorzugten Vorgehensweisen und der Kapazitätsplanung.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-126">Each page has a description of the selection criteria, and recommendations based on preferred practices and capacity planning.</span></span> <span data-ttu-id="ae4ea-127">Wenn Sie weitere Informationen benötigen <STRONG>, klicken Sie auf Weitere Informationen</STRONG> , um detaillierte Informationen aus der lync Server 2013-Planungsdokumentation auf der Microsoft TechNet-Website zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-127">If you require additional details, click <STRONG>Learn more</STRONG> to read detailed information from the Lync Server 2013 Planning documentation on the Microsoft TechNet website.</span></span> <span data-ttu-id="ae4ea-128">Für den Zugriff auf die Microsoft TechNet-Website ist eine Internetverbindung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-128">You must have Internet connectivity to access the Microsoft TechNet website.</span></span>

    
    </div>

5.  <span data-ttu-id="ae4ea-129">Wählen Sie die geeigneten Optionen für Ihren Entwurf.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-129">Select the appropriate options for your design.</span></span> <span data-ttu-id="ae4ea-130">Nach der Definition der anfänglichen Kriterien werden Sie darüber informiert, dass die Funktionsübersicht vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-130">After the initial criteria are defined, a page will confirm that your Features Overview is complete.</span></span>

6.  <span data-ttu-id="ae4ea-131">Klicken Sie auf **Websites entwerfen** , um Ihre zentrale Website zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-131">Click **Design Sites** to define your central site.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ae4ea-132">Jede lync Server 2013-Topologie verfügt über mindestens einen zentralen Standort.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-132">Each Lync Server 2013 topology will have at least one central site.</span></span> <span data-ttu-id="ae4ea-133">Ihr Entwurf kann eine einzige zentrale Website, einen zentralen Standort mit einer Reihe von Zweigstellen, eine Reihe von zentralen Standorten oder eine Reihe zentraler Standorte mit Verzweigungs Websites aufweisen, die jedem zentralen Standort zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-133">Your design may have a single central site, a central site with a number of branch sites, a number of central sites, or a number of central sites with branch sites associated with each central site.</span></span>

    
    </div>

7.  <span data-ttu-id="ae4ea-134">Geben Sie unter **Websitename** den Namen ein, der diese zentrale Website kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-134">In **Site Name**, type the name that will identify this central site.</span></span>

8.  <span data-ttu-id="ae4ea-135">Geben Sie in "Website-vernetzte **Benutzer**" die erwartete Anzahl von lokalen gleichzeitigen Benutzern ein, die an diesem zentralen Standort verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-135">In **Site Homed Users**, type the expected number of on-premises concurrent users who will be homed in this central site.</span></span>

9.  <span data-ttu-id="ae4ea-136">Geben Sie in Cloud-vernetzten **Benutzern** die erwartete Anzahl von gleichzeitigen Online Benutzern ein, die in diesem zentralen Standort verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-136">In **Cloud Homed Users**, type the expected number of online concurrent users who will be homed in this central site.</span></span>

10. <span data-ttu-id="ae4ea-137">Ändern Sie nach Bedarf die Auswahl für Onlinezusammenarbeit, Benutzer, VoIP, zusätzliche Bereitstellungsoptionen oder Serveranwendungen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-137">Modify the selections for Online Collaboration, Users, Voice, Additional Deployment Options, or Server Applications, as needed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="ae4ea-138">Zu diesem Entwurfszeitpunkt können Sie Optionen für Ihre Bereitstellung nur auswählen oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-138">At this point in the design, you can only select or clear options for your deployment.</span></span> <span data-ttu-id="ae4ea-139">Sie können jedoch in einer späteren Phase des Planungstools weitere Optionen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-139">However, you can configure more options in a later phase of the Planning Tool.</span></span> <span data-ttu-id="ae4ea-140">Einige Optionen sind nicht verfügbar und können nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-140">There are also options that are unavailable and cannot be cleared.</span></span> <span data-ttu-id="ae4ea-141">Darüber hinaus müssen Sie möglicherweise eine Option deaktivieren, um eine andere deaktivieren zu können.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-141">In addition, you may have to clear one option in order to clear another.</span></span> <span data-ttu-id="ae4ea-142">Wenn Sie zum Beispiel unter „VoIP“ die Option <STRONG>Enterprise-VoIP</STRONG> deaktivieren, sind unter „Serveranwendungen“ die Optionen <STRONG>Reaktionsgruppe</STRONG>, <STRONG>Ankündigung</STRONG> und <STRONG>Anruf parken</STRONG> deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-142">For example, if you clear the <STRONG>Enterprise Voice</STRONG> option under Voice, then the <STRONG>Response Group</STRONG>, <STRONG>Announcement</STRONG>, and <STRONG>Call Park</STRONG> options under Server Applications (all of which are features of Enterprise Voice) are also cleared.</span></span>

    
    </div>

11. <span data-ttu-id="ae4ea-143">Klicken Sie nach dem Definieren von Standortname und Nutzeranzahl auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-143">After defining a site name and number of users, click **Next**.</span></span>

12. <span data-ttu-id="ae4ea-144">Auf den folgenden Seiten werden Informationen zu SIP-Domänen, Konferenzeinstellungen, Spracheinstellungen und-Infrastruktur, Exchange um-, externer Benutzer Zugriff, Einstellungen für beständigen Chat, Clienteinstellungen, Zusammenstellungsoptionen und Verzweigungs Websites verlangt.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-144">The following pages ask for information about SIP domains, conference settings, voice settings and infrastructure, Exchange UM, external user access, Persistent Chat settings, client settings, collocation options, and branch sites.</span></span> <span data-ttu-id="ae4ea-145">Geben Sie die entsprechenden Informationen an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-145">Answer these questions as appropriate.</span></span>

13. <span data-ttu-id="ae4ea-146">In der letzten Frage wird gefragt, ob Sie eine weitere zentrale Website erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-146">The final question asks if you want to create another central site.</span></span> <span data-ttu-id="ae4ea-147">Wenn Sie **Ja** auswählen, kehrt das Planungs Tool zur Seite "zentrale Websites" zurück.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-147">If you select **Yes**, then the Planning Tool returns to the Central Sites page.</span></span> <span data-ttu-id="ae4ea-148">Wenn Sie **Nein** auswählen, klicken Sie auf **Weiter** und anschließend auf **Zeichnen**, um die allgemeine Übersicht über die globale Technologie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-148">If you select **No**, click **Next**, and then click **Draw** to display the high-level Global Topology view.</span></span>

14. <span data-ttu-id="ae4ea-149">Klicken Sie zum Anzeigen einer vorhandenen Topologie auf **Anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-149">To view an existing topology, click **Display**.</span></span>

15. <span data-ttu-id="ae4ea-150">Klicken Sie auf die XML-Datei, welche die zuvor gespeicherte Topologie enthält, und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-150">Click the .xml file that represents the previously saved topology, and then click **Open**.</span></span>

16. <span data-ttu-id="ae4ea-151">Das Planungs Tool zeigt die Seite globale Topologie an.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-151">The Planning Tool displays the Global Topology page.</span></span> <span data-ttu-id="ae4ea-152">Mit den im Planungs Tool verfügbaren Tools können Sie nun mit dem Bearbeiten, aktualisieren oder Ändern der Topologie beginnen.</span><span class="sxs-lookup"><span data-stu-id="ae4ea-152">You can now begin editing, updating, or changing the topology by using the tools available in the Planning Tool.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ae4ea-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae4ea-153">See Also</span></span>


[<span data-ttu-id="ae4ea-154">Bearbeiten des Entwurfs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae4ea-154">Editing the design in Lync Server 2013</span></span>](lync-server-2013-editing-the-design.md)  
  

<span data-ttu-id="ae4ea-155"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae4ea-155"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

