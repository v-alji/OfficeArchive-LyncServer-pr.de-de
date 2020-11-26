---
title: 'Lync Server 2013: Erstellen oder Ändern eines interaktiven Workflows'
description: 'Lync Server 2013: Erstellen oder Ändern eines interaktiven Workflows'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify an interactive workflow
ms:assetid: bc7bb1bc-bf6a-4636-ae93-c56fa22613fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205213(v=OCS.15)
ms:contentKeyID: 48185260
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 470a073322c48c351dbfdfb24ce376731b3e7512
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431694"
---
# <a name="create-or-modify-an-interactive-workflow-in-lync-server-2013"></a><span data-ttu-id="39355-103">Erstellen oder Ändern eines interaktiven Workflows in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39355-103">Create or modify an interactive workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39355-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39355-104">

<span> </span></span></span>

<span data-ttu-id="39355-105">_**Letztes Änderungsdatum des Themas:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="39355-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="39355-106">Führen Sie eines der folgenden Verfahren aus, um einen interaktiven Workflow zu erstellen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="39355-106">Use one of the following procedures to create or modify an interactive workflow.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="39355-107">Sie können die lync Server-Verwaltungsshell oder das Reaktionsgruppen-Konfigurations Tool verwenden, um interaktive Workflows zu erstellen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="39355-107">You can use Lync Server Management Shell or the Response Group Configuration Tool to create and modify interactive workflows.</span></span> <span data-ttu-id="39355-108">Sie können über die lync Server-Systemsteuerung auf das Tool für die Reaktionsgruppen Konfiguration zugreifen, oder indem Sie die Webseite direkt in einem Webbrowser öffnen, indem Sie die folgende URL eingeben: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39355-108">You can access the Response Group Configuration Tool from Lync Server Control Panel, or by opening the webpage directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>



</div>

<div>

## <a name="to-use-response-group-configuration-tool-to-create-or-modify-an-interactive-workflow"></a><span data-ttu-id="39355-109">So verwenden Sie das Reaktionsgruppen-Konfigurations Tool zum Erstellen oder Ändern eines interaktiven Workflows</span><span class="sxs-lookup"><span data-stu-id="39355-109">To use Response Group Configuration Tool to create or modify an Interactive workflow</span></span>

1.  <span data-ttu-id="39355-110">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39355-110">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="39355-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="39355-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="39355-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="39355-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="39355-113">Klicken Sie in der linken Navigationsleiste auf **Reaktionsgruppen** und dann auf **Workflow**.</span><span class="sxs-lookup"><span data-stu-id="39355-113">In the left navigation bar, click **Response Groups**, and then click **Workflow**.</span></span>

4.  <span data-ttu-id="39355-114">Klicken Sie auf der Seite **Workflow** auf **Workflow erstellen oder bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="39355-114">On the **Workflow** page, click **Create or edit a workflow**.</span></span>

5.  <span data-ttu-id="39355-115">Geben Sie im Suchfeld **Dienst auswählen** einen Teil oder den vollständigen Namen des **ApplicationServer**-Diensts ein, von dem der Workflow gehostet wird, den Sie erstellen oder ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="39355-115">In the **Select a Service** search field, type all or part of the name of the **ApplicationServer** service that hosts the workflow that you want to create or modify.</span></span> <span data-ttu-id="39355-116">Klicken Sie in der nun angezeigten Liste der Dienst auf den gewünschten Dienst und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="39355-116">In the resulting list of services, click the service that you want, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-117">Das Tool für die Reaktionsgruppen Konfiguration wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="39355-117">The Response Group Configuration Tool opens.</span></span> <span data-ttu-id="39355-118">Sie können das Tool für die Reaktionsgruppen Konfiguration auch direkt in einem Webbrowser öffnen, indem Sie die folgende URL eingeben: <STRONG>https://</STRONG> &lt; webPoolFqdn &gt; <STRONG>/RgsConfig</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39355-118">You can also open the Response Group Configuration Tool directly from a web browser by typing the following URL: <STRONG>https://</STRONG>&lt;webPoolFqdn&gt;<STRONG>/RgsConfig</STRONG>.</span></span>

    
    </div>

6.  <span data-ttu-id="39355-119">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="39355-119">Do one of the following:</span></span>
    
      - <span data-ttu-id="39355-120">Klicken Sie unterhalb von **Neuen Workflow erstellen** neben **Interaktiv** auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="39355-120">Under **Create a New Workflow**, next to **Interactive**, click **Create**.</span></span>
    
      - <span data-ttu-id="39355-121">Suchen Sie unter **Vorhandenen Workflow verwalten** nach dem Workflow, den Sie ändern möchten, und klicken Sie anschließend unter **Aktion** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="39355-121">Under **Manage an Existing Workflow**, locate the workflow you want to change, and then under **Action**, click **Edit**.</span></span>

7.  <span data-ttu-id="39355-122">Falls Benutzer den Workflow noch nicht aufrufen sollen, müssen Sie das Kontrollkästchen **Workflow aktivieren** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="39355-122">If you are not ready for users to start calling the workflow, clear the **Activate the workflow** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-p105">Wenn Sie einen verwalteten Workflow erstellen, müssen Sie <STRONG>Workflow aktivieren</STRONG> auswählen. Nachdem Sie den aktiven, verwalteten Workflow gespeichert haben, können Sie ihn ändern und deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="39355-p105">If you are to creating a managed workflow, you need to select <STRONG>Activate the workflow</STRONG>. After you save the active, managed workflow, you can then modify and deactivate it.</span></span>

    
    </div>

8.  <span data-ttu-id="39355-125">Aktivieren Sie das Kontrollkästchen **Für Partnerverbund aktivieren**, um Partnerbenutzern Anrufe bei der Gruppe zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="39355-125">To allow federated users to call the group, select the **Enable for federation** check box.</span></span> <span data-ttu-id="39355-126">Außerdem müssen Sie über eine Richtlinie für den externen Zugriff verfügen, die für die für den Verbund konfigurierte reaktionsgruppenanwendung gilt.</span><span class="sxs-lookup"><span data-stu-id="39355-126">You must also have an external access policy that applies to the Response Group application configured for federation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-127">Die globale Richtlinie für den externen Zugriff gilt für die Antwortgruppen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="39355-127">The global external access policy applies to the Response Group application.</span></span> <span data-ttu-id="39355-128">Sie können die globale Richtlinie für die Antwortgruppen Föderation mithilfe der lync Server-Systemsteuerung oder mithilfe des Cmdlets "CsExternalAccessPolicy" konfigurieren, um den EnableOutsideAccess <STRONG>-</STRONG> Parameter auf "true" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="39355-128">You can configure the global policy for response group federation by using Lync Server Control Panel or by using the <STRONG>Set-CsExternalAccessPolicy</STRONG> cmdlet to set the EnableOutsideAccess parameter to True.</span></span> <span data-ttu-id="39355-129">Bedenken Sie, dass globale Richtlinieneinstellungen für alle Benutzer gelten, es sei denn, sie sind einer standort- oder benutzerspezifischen Richtlinie zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="39355-129">Keep in mind that global policy settings apply to all users unless they are assigned a site or user policy.</span></span> <span data-ttu-id="39355-130">Stellen Sie daher vor dem Ändern dieser Einstellung für Reaktionsgruppen sicher, dass die Partnerverbundeinstellung die Anforderungen Ihrer Organisation erfüllt.</span><span class="sxs-lookup"><span data-stu-id="39355-130">Therefore, before changing this setting for response groups, make sure that the federation setting meets the requirements of your organization.</span></span> <span data-ttu-id="39355-131">Details dazu, wie Richtlinien für Benutzer gelten, finden Sie unter <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Verwalten der Richtlinie für den externen Zugriff in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-131">For details about how policies apply to users, see <A href="lync-server-2013-manage-external-access-policy-for-your-organization.md">Manage external access policy in Lync Server 2013</A>.</span></span> <span data-ttu-id="39355-132">Details zur Föderations Einstellung finden Sie unter Dokumentation zu CsExternalAccessPolicy in der lync Server <STRONG>-</STRONG> Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="39355-132">For details about the federation setting, see <STRONG>Set-CsExternalAccessPolicy</STRONG> in Lync Server Management Shell documentation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-133">Benutzer, die in lync online gehostet werden, können keine Anrufe an Reaktionsgruppen tätigen, die in einer lokalen Bereitstellung gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="39355-133">Users who are hosted in Lync Online can’t place calls to response groups that are hosted in an on-premise deployment.</span></span> <span data-ttu-id="39355-134">Dies gilt sowohl in hybridbereitstellungen als auch in Fällen, in denen eine lokale Bereitstellung mit einer lync Online-Bereitstellung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="39355-134">This is true in both hybrid deployments and in cases where an on-premise deployment is federated with a Lync Online deployment.</span></span>

    
    </div>

9.  <span data-ttu-id="39355-135">Aktivieren Sie das Kontrollkästchen **Agentanonymität aktivieren**, um bei Anrufen die Identität der Agents zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="39355-135">To hide the identity of agents during calls, select the **Enable agent anonymity** check box.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-p109">Anonyme Anrufe können nicht mit Chats oder Video gestartet werden. Agent oder Anrufer können jedoch im Verlauf des Anrufs Chats und Video aktivieren. Ein anonymer Agent kann Anrufe halten, weiterleiten (sowohl blind als auch nach Rücksprache) sowie Anrufe parken und fortsetzen. Anonyme Anrufe bieten keine Unterstützung für Konferenzen, Anwendungs- und Desktopfreigabe, Dateiübertragung, Whiteboardverwendung und Datenzusammenarbeit sowie Anrufaufzeichnung. Agents, die das Lync VDI-Plugin verwenden, können eingehende Anrufe anonym empfangen, jedoch keine ausgehenden anonymen Anrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="39355-p109">Anonymous calls cannot start with instant messaging (IM) or video, although the agent or the caller can add IM and video after the call is established. An anonymous agent can also put calls on hold, transfer calls (both blind and consultative transfers), and park and retrieve calls. Anonymous calls do not support conferencing, application sharing and desktop sharing, file transfer, whiteboarding and data collaboration, and call recording. Agents using the Lync VDI Plugin can receive incoming calls anonymously, but they cannot make outgoing calls anonymously.</span></span>

    
    </div>

10. <span data-ttu-id="39355-140">Geben Sie im Feld **Adresse der Gruppe eingeben, die die Anrufe entgegennimmt** den primären SIP-URI (Uniform Resource Identifier) der Gruppe ein, die die Anrufe beim Workflow erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="39355-140">Under **Enter the address of the group that will receive the calls**, type the primary SIP uniform resource identifier (URI) address of the group that will answer calls to the workflow.</span></span>

11. <span data-ttu-id="39355-141">Geben Sie im Feld **Anzeigename** den Namen ein, der für den Workflow angezeigt werden soll (z. B. „Vertrieb-IVR-Reaktionsgruppe“).</span><span class="sxs-lookup"><span data-stu-id="39355-141">In **Display name**, type the name that you want to display for the workflow (for example, Sales IVR Response Group).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-142">Fügen Sie die Zeichen " &lt; " oder " &gt; " nicht in den Anzeigenamen ein.</span><span class="sxs-lookup"><span data-stu-id="39355-142">Do not include the "&lt;" or "&gt;" characters in the display name.</span></span> <span data-ttu-id="39355-143">Die folgenden Anzeigenamen sind reserviert und dürfen nicht verwendet werden: „RGS-Anwesenheitsmonitor“ oder „Ankündigungsdienst“.</span><span class="sxs-lookup"><span data-stu-id="39355-143">Do not use the following display names because they are reserved: RGS Presence Watcher or Announcement Service.</span></span>

    
    </div>

12. <span data-ttu-id="39355-144">Geben Sie unter **Telefonnummer** den Anschluss-URI für die Reaktionsgruppe ein (z. B. +14255550165).</span><span class="sxs-lookup"><span data-stu-id="39355-144">In **Telephone number**, type the line URI for the response group (for example, +14255550165).</span></span>

13. <span data-ttu-id="39355-145">Geben Sie im Feld **Anzeigenummer** die Nummer ein, wie sie für die Reaktionsgruppe angezeigt werden soll (z. B. +1 (425) 555-0165).</span><span class="sxs-lookup"><span data-stu-id="39355-145">In **Display number**, type the number as you want it to appear for the response group (for example, +1 (425) 555-0165).</span></span>

14. <span data-ttu-id="39355-146">Optional Geben Sie in **Beschreibung** eine Beschreibung für den Workflow ein, der auf der Visitenkarte im lync-Client angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39355-146">(Optional) In **Description**, type a description for the workflow that you want to appear on the contact card in the Lync client.</span></span>

15. <span data-ttu-id="39355-147">Wählen Sie unter **Workflowtyp** die Option **Verwaltet** aus, wenn dieser Workflow von einem Reaktionsgruppenmanager verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="39355-147">In **Workflow Type**, select **Managed** if this workflow will be managed by a Response Group Manager.</span></span> <span data-ttu-id="39355-148">Gehen Sie wie folgt vor, um dem Workflow Antwortgruppen-Manager zuzuweisen:</span><span class="sxs-lookup"><span data-stu-id="39355-148">Do the following to assign Response Group Managers to the workflow:</span></span>
    
    1.  <span data-ttu-id="39355-149">Geben Sie den SIP-URI eines Managers für diesen Workflow ein und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39355-149">Type the SIP URI of a manager for this workflow, and click **Add**..</span></span>
    
    2.  <span data-ttu-id="39355-150">Geben Sie den SIP-URI zusätzlicher Manager für den Workflow ein und klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="39355-150">Type the SIP URI of additional managers to add to the workflow, and click **Add**..</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="39355-p112">Jedem Benutzer, der als Manager einer Reaktionsgruppe bestimmt wurde, muss die Rolle „CsResponseGroupManager“ zugewiesen sein. Falls Benutzern diese Rolle nicht zugewiesen ist, können sie keine Reaktionsgruppen verwalten.</span><span class="sxs-lookup"><span data-stu-id="39355-p112">Every user who is designated as a manager of a response group must be assigned the CsResponseGroupManager role. If users are not assigned this role, they cannot manage response groups.</span></span>

    
    </div>

16. <span data-ttu-id="39355-153">Klicken Sie unter **Schritt 2: Sprache auswählen** auf die Sprache, die für die Spracherkennung und die Text-zu-Sprache-Funktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="39355-153">Under **Step 2 Select a Language**, click the language to use for speech recognition and text-to-speech.</span></span>

17. <span data-ttu-id="39355-154">Aktivieren Sie zum Konfigurieren einer Willkommensnachricht unter **Schritt 3: Willkommensnachricht konfigurieren** das Kontrollkästchen **Willkommensnachricht wiedergeben** und führen Sie eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="39355-154">If you want to configure a welcome message, under **Step 3 Configure a Welcome Message**, select the **Play a welcome message** check box, and then do one of the following:</span></span>
    
      - <span data-ttu-id="39355-155">Um die Willkommensnachricht als Text einzugeben, die für Anrufer in Sprache umgewandelt wird, klicken Sie auf **Text-zu-Sprache verwenden** und geben Sie die Willkommensnachricht in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="39355-155">To enter the welcome message as text that is converted to speech for callers, click **Use text-to-speech**, and then type the welcome message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-p113">Verwenden Sie im eingegebenen Text keine HTML-Tags. Andernfalls wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39355-p113">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="39355-p114">Um eine aufgezeichnete WAV- oder WMA-Datei für die Willkommensnachricht zu verwenden, klicken Sie auf **Aufzeichnung auswählen**. Klicken Sie auf den Link **Aufzeichnung**, um eine neue Audiodatei hochzuladen. Klicken Sie im neuen Browserfenster auf **Durchsuchen**, markieren Sie die gewünschte Audiodatei und klicken Sie dann auf **Öffnen**. Klicken Sie auf **Hochladen**, um die Datei zu laden.</span><span class="sxs-lookup"><span data-stu-id="39355-p114">To use a Wave or Windows Media Audio file recording for the welcome message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the audio file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-162">Alle von Benutzern bereitgestellten Audiodateien müssen bestimmte Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="39355-162">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="39355-163">Ausführliche Informationen zu unterstützten Dateiformaten finden Sie unter <A href="lync-server-2013-technical-requirements-for-response-group.md">Technische Anforderungen für die Reaktionsgruppe in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-163">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

18. <span data-ttu-id="39355-164">Klicken Sie unter **Schritt 4: Geschäftszeiten angeben** im Feld **Ihre Zeitzone** auf die Zeitzone des Workflows.</span><span class="sxs-lookup"><span data-stu-id="39355-164">Under **Step 4 Specify Your Business Hours**, in the **Your time zone** box, click the time zone of the workflow.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-p116">Dies ist die Zeitzone, in der sich die Anrufer und Agents des Workflows befinden. Die Angabe wird verwendet, um die Öffnungszeiten zu berechnen. Wenn der Workflow z. B. für die mitteleuropäische Zeit konfiguriert wurde und der Workflow um 7:00 Uhr öffnen und um 11:00 Uhr schließen soll, werden die Zeiten 7:00 Uhr MEZ und 23:00 Uhr MEZ verwendet. (Die Zeiten müssen im 24-Stunden-Format eingegeben werden.)</span><span class="sxs-lookup"><span data-stu-id="39355-p116">The time zone is the time zone where the callers and agents of the workflow reside. It is used to calculate the open and close hours. For example, if the workflow is configured to use the North American Eastern Time zone and the workflow is scheduled to open at 7:00 A.M. and close at 11:00 P.M., the open and close times are assumed to be 7:00 Eastern Time and 11:00 Eastern Time respectively. (You must enter the times in 24-hour time notation.)</span></span>

    
    </div>

19. <span data-ttu-id="39355-170">Sie haben folgende Möglichkeiten, um die gewünschten Geschäftszeiten anzugeben:</span><span class="sxs-lookup"><span data-stu-id="39355-170">Select the type of business hours schedule you want to use by doing one of the following:</span></span>
    
      - <span data-ttu-id="39355-171">Wenn Sie einen vordefinierten Zeitplan für die Geschäftszeiten verwenden möchten, klicken Sie auf **Vordefinierten Zeitplan verwenden** und wählen Sie den gewünschten Zeitplan in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="39355-171">To use a predefined schedule of business hours, click **Use a preset schedule**, and then select the schedule you want to use from the drop-down list.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-172">Sie müssen mindestens einen vordefinierten Zeitplan erstellt haben, um diese Option auswählen zu können.</span><span class="sxs-lookup"><span data-stu-id="39355-172">You must have defined at least one preset schedule previously to be able to select this option.</span></span> <span data-ttu-id="39355-173">Sie erstellen vordefinierte Zeitpläne mit dem <STRONG>New-CSRgsHoursOfBusiness</STRONG>-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39355-173">You define preset schedules by using the <STRONG>New-CSRgsHoursOfBusiness</STRONG> cmdlet.</span></span> <span data-ttu-id="39355-174">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-optional-define-response-group-business-hours.md">(optional) definieren von Reaktionsgruppen-Geschäftszeiten in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-174">For details, see <A href="lync-server-2013-optional-define-response-group-business-hours.md">(Optional) Define Response Group business hours in Lync Server 2013</A>.</span></span> <span data-ttu-id="39355-175">Wenn Sie einen vordefinierten Zeitplan verwenden, werden die Werte für <STRONG>Tag</STRONG>, <STRONG>Öffnen</STRONG> und <STRONG>Schließen</STRONG>, automatisch mit den Tagen und Stunden ausgefüllt, an denen die Reaktionsgruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="39355-175">When you select a preset schedule, <STRONG>Day</STRONG>, <STRONG>Open</STRONG>, and <STRONG>Close</STRONG> are automatically filled with the days and hours that the response group is available.</span></span>

        
        </div>
    
      - <span data-ttu-id="39355-176">Klicken Sie auf **Benutzerdefinierten Zeitplan verwenden**, um einen benutzerdefinierten Zeitplan zu erstellen, der nur für diesen Workflow gilt.</span><span class="sxs-lookup"><span data-stu-id="39355-176">To use a custom schedule that applies only to this workflow, click **Use a custom schedule**.</span></span>

20. <span data-ttu-id="39355-177">Wenn Sie einen benutzerdefinierten Zeitplan für diesen Workflow erstellen, aktivieren Sie die Kontrollkästchen für die Wochentage, an denen die Reaktionsgruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="39355-177">If you are creating a custom schedule for this workflow, click the check boxes for the days of the week that the response group is available.</span></span>

21. <span data-ttu-id="39355-178">Beim Erstellen eines benutzerdefinierten Zeitplans geben Sie über die Werte für **Öffnen** und **Schließen** den Zeitraum ein, in dem die Reaktionsgruppe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="39355-178">If you are creating a custom schedule, type the **Open** and **Close** hours when the response group available.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-p118">Die Werte für <STRONG>Öffnen</STRONG> und <STRONG>Schließen</STRONG> müssen im 24-Stunden-Format angegeben werden. Wenn Ihr Büro z. B. von 9 Uhr bis 17 Uhr geöffnet und mittags geschlossen ist, können Sie die Geschäftszeiten als <STRONG>Öffnen</STRONG> 9:00, <STRONG>Schließen</STRONG> 12:00, <STRONG>Öffnen</STRONG> 13:00 und <STRONG>Schließen</STRONG> 17:00 angeben.</span><span class="sxs-lookup"><span data-stu-id="39355-p118">The <STRONG>Open</STRONG> and <STRONG>Close</STRONG> hours must be in 24-hour time notation. For example, if your office works a 9-to-5 work day and closes at noon for lunch, the business hours are specified as <STRONG>Open</STRONG> 9:00, <STRONG>Close</STRONG> 12:00, <STRONG>Open</STRONG> 13:00, and <STRONG>Close</STRONG> 17:00.</span></span>

    
    </div>

22. <span data-ttu-id="39355-181">Wenn Sie eine Nachricht wiedergeben möchten, wenn das Büro geschlossen ist, aktivieren Sie das Kontrollkästchen **Nachricht wiedergeben, wenn die Reaktionsgruppe nicht geöffnet ist** und geben Sie die Nachricht ein, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="39355-181">If you want to play a message when the office is not open, select the **Play a message when the response group is outside of business hours** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="39355-182">Um die Nachricht als Text einzugeben, die für Anrufer in Sprache umgewandelt wird, klicken Sie auf **Text-zu-Sprache verwenden** und geben Sie die Nachricht in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="39355-182">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-p119">Verwenden Sie im eingegebenen Text keine HTML-Tags. Andernfalls wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39355-p119">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="39355-p120">Um eine aufgezeichnete Audiodatei als Nachricht zu verwenden, klicken Sie auf **Aufzeichnung auswählen**. Klicken Sie auf den Link **Aufzeichnung**, um eine neue Audiodatei hochzuladen. Klicken Sie im neuen Browserfenster auf **Durchsuchen**, markieren Sie die gewünschte Datei und klicken Sie auf **Öffnen**. Klicken Sie auf **Hochladen**, um die Datei zu laden.</span><span class="sxs-lookup"><span data-stu-id="39355-p120">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-189">Alle von Benutzern bereitgestellten Audiodateien müssen bestimmte Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="39355-189">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="39355-190">Ausführliche Informationen zu unterstützten Dateiformaten finden Sie unter <A href="lync-server-2013-technical-requirements-for-response-group.md">Technische Anforderungen für die Reaktionsgruppe in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-190">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

23. <span data-ttu-id="39355-191">Geben Sie an, wie nach Wiedergabe der Nachricht verfahren werden soll (sofern eine Nachricht konfiguriert wurde):</span><span class="sxs-lookup"><span data-stu-id="39355-191">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="39355-192">Klicken Sie auf **Verbindung trennen**, um die Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="39355-192">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="39355-193">Um den Anruf an ein Voicemailsystem weiterzuleiten, klicken Sie auf **An Voicemail weiterleiten** und geben Sie die Voicemailadresse ein.</span><span class="sxs-lookup"><span data-stu-id="39355-193">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="39355-194">Das Format für die Voicemail-Adresse lautet \<username\> @ \<domainname\> (beispielsweise Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="39355-194">The format for the voice mail address is \<username\>@\<domainname\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="39355-195">Um den Anruf an einen anderen Benutzer weiterzuleiten, klicken Sie auf **An SIP-URI weiterleiten** und geben Sie die Adresse eines Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="39355-195">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="39355-196">Das Format für die Benutzeradresse lautet \<username\> @ \<domainname\> .</span><span class="sxs-lookup"><span data-stu-id="39355-196">The format for the user address is \<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="39355-197">Um den Anruf an eine andere Telefonnummer weiterzuleiten, klicken Sie auf **An Telefonnummer weiterleiten** und geben Sie die Telefonnummer ein.</span><span class="sxs-lookup"><span data-stu-id="39355-197">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="39355-198">Das Format für die Telefonnummer lautet \<number\> @ \<domainname\> (beispielsweise + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="39355-198">The format for the telephone number is \<number\>@\<domainname\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="39355-199">Der Domänenname wird verwendet, um den Anrufer an das richtige Ziel weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="39355-199">The domain name is used to route the caller to the correct destination.</span></span>

24. <span data-ttu-id="39355-200">Aktivieren Sie unter **Schritt 5: Feiertage angeben** die Kontrollkästchen für einen oder mehrere Feiertagssätze, mit denen die Tage definiert werden, an denen die Reaktionsgruppe aufgrund eines Feiertags nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="39355-200">Under **Step 5 Specify Your Holidays**, click the check boxes for one or more sets of holidays that define the days when the response group is closed for business.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-201">Sie müssen Feiertage und Feiertagssätze definieren, bevor Sie den Workflow konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="39355-201">You need to define holidays and holiday sets before you configure the workflow.</span></span> <span data-ttu-id="39355-202">Verwenden Sie zum Definieren von Feiertagen und Feiertagssätzen die Cmdlets <STRONG>New-CsRgsHoliday</STRONG> und <STRONG>New-CsRgsHolidaySet</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="39355-202">Use the <STRONG>New-CsRgsHoliday</STRONG> and <STRONG>New-CsRgsHolidaySet</STRONG> cmdlets to define holidays and holiday sets.</span></span> <span data-ttu-id="39355-203">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(optional) definieren von Reaktionsgruppen Feiertagssätzen in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-203">For details, see <A href="lync-server-2013-optional-define-response-group-holiday-sets.md">(Optional) Define Response Group holiday sets in Lync Server 2013</A>.</span></span>

    
    </div>

25. <span data-ttu-id="39355-204">Wenn Sie an Feiertagen eine Nachricht wiedergeben möchten, aktivieren Sie das Kontrollkästchen **An Feiertagen eine Nachricht wiedergegeben** und geben Sie die Nachricht ein, indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="39355-204">If you want to play a message on holidays, select the **Play a message during holidays** check box, and then specify the message to play by doing one of the following:</span></span>
    
      - <span data-ttu-id="39355-205">Um die Nachricht als Text einzugeben, die für Anrufer in Sprache umgewandelt wird, klicken Sie auf **Text-zu-Sprache verwenden** und geben Sie die Nachricht in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="39355-205">To enter the message as text that is converted to speech for the caller, click **Use text-to-speech**, and then type the message in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-p126">Verwenden Sie im eingegebenen Text keine HTML-Tags. Andernfalls wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39355-p126">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
    
      - <span data-ttu-id="39355-p127">Um eine aufgezeichnete Audiodatei als Nachricht zu verwenden, klicken Sie auf **Aufzeichnung auswählen**. Klicken Sie auf den Link **Aufzeichnung**, um eine neue Audiodatei hochzuladen. Klicken Sie im neuen Browserfenster auf **Durchsuchen**, markieren Sie die gewünschte Datei und klicken Sie auf **Öffnen**. Klicken Sie auf **Hochladen**, um die Datei zu laden.</span><span class="sxs-lookup"><span data-stu-id="39355-p127">To use an audio file recording for the message, click **Select a recording**. If you want to upload a new audio file, click the **a recording** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-212">Alle von Benutzern bereitgestellten Audiodateien müssen bestimmte Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="39355-212">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="39355-213">Ausführliche Informationen zu unterstützten audiodateidateien finden Sie unter <A href="lync-server-2013-technical-requirements-for-response-group.md">Technische Anforderungen für die Reaktionsgruppe in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-213">For details about supported audio file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

26. <span data-ttu-id="39355-214">Geben Sie an, wie nach Wiedergabe der Nachricht verfahren werden soll (sofern eine Nachricht konfiguriert wurde):</span><span class="sxs-lookup"><span data-stu-id="39355-214">Specify how to handle calls after the message is played (if a message is configured):</span></span>
    
      - <span data-ttu-id="39355-215">Klicken Sie auf **Verbindung trennen**, um die Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="39355-215">To disconnect the call, click **Disconnect Call**.</span></span>
    
      - <span data-ttu-id="39355-216">Um den Anruf an ein Voicemailsystem weiterzuleiten, klicken Sie auf **An Voicemail weiterleiten** und geben Sie die Voicemailadresse ein.</span><span class="sxs-lookup"><span data-stu-id="39355-216">To forward the call to voice mail, click **Forward to voice mail**, and then type the voice mail address.</span></span> <span data-ttu-id="39355-217">Das Format für die Voicemail-Adresse lautet \<username\> @ \<domainname\> (beispielsweise Bob@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="39355-217">The format for the voice mail address is \<username\>@\<domainname\> (for example, bob@contoso.com).</span></span>
    
      - <span data-ttu-id="39355-218">Um den Anruf an einen anderen Benutzer weiterzuleiten, klicken Sie auf **An SIP-URI weiterleiten** und geben Sie die Adresse eines Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="39355-218">To forward the call to another user, click **Forward to SIP URI**, and then type a user address.</span></span> <span data-ttu-id="39355-219">Das Format für die Benutzeradresse lautet \<username\> @ \<domainname\> .</span><span class="sxs-lookup"><span data-stu-id="39355-219">The format for the user address is \<username\>@\<domainname\>.</span></span>
    
      - <span data-ttu-id="39355-220">Um den Anruf an eine andere Telefonnummer weiterzuleiten, klicken Sie auf **An Telefonnummer weiterleiten** und geben Sie die Telefonnummer ein.</span><span class="sxs-lookup"><span data-stu-id="39355-220">To forward the call to another telephone number, click **Forward to telephone number**, and then type the telephone number.</span></span> <span data-ttu-id="39355-221">Das Format für die Telefonnummer lautet \<number\> @ \<domainname\> (beispielsweise + 14255550121@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="39355-221">The format for the telephone number is \<number\>@\<domainname\> (for example, +14255550121@contoso.com).</span></span> <span data-ttu-id="39355-222">Der Domänenname wird verwendet, um den Anrufer an das richtige Ziel weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="39355-222">The domain name is used to route the caller to the correct destination.</span></span>

27. <span data-ttu-id="39355-223">Wählen Sie unter **Schritt 6: Wartemusik konfigurieren** aus, was Anrufer beim Warten auf einen Agent hören sollen, indem Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="39355-223">Under **Step 6 Configure Music on Hold**, choose what you want callers to listen to while waiting for an agent by doing one of the following:</span></span>
    
      - <span data-ttu-id="39355-224">Klicken Sie auf **Standard verwenden**, um die Standardwartemusik zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="39355-224">To use the default music on-hold recording, click **Use default**.</span></span>
    
      - <span data-ttu-id="39355-p132">Klicken Sie auf **Musikdatei auswählen**, um eine aufgezeichnete Audiodatei als Wartemusik zu verwenden. Klicken Sie auf den Link **Musikdatei**, um eine neue Audiodatei hochzuladen. Klicken Sie im neuen Browserfenster auf **Durchsuchen**, markieren Sie die gewünschte Datei und klicken Sie auf **Öffnen**. Klicken Sie auf **Hochladen**, um die Datei zu laden.</span><span class="sxs-lookup"><span data-stu-id="39355-p132">To use an audio file recording for the on-hold music, click **Select a music file**. If you want to upload a new audio file, click the **a music file** link. In the new browser window, click **Browse**, select the file that you want to use, and then click **Open**. Click **Upload** to load the audio file.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-229">Alle von Benutzern bereitgestellten Audiodateien müssen bestimmte Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="39355-229">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="39355-230">Ausführliche Informationen zu unterstützten Dateiformaten finden Sie unter <A href="lync-server-2013-technical-requirements-for-response-group.md">Technische Anforderungen für die Reaktionsgruppe in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-230">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

28. <span data-ttu-id="39355-231">Geben Sie in **Schritt 7: Interaktive Sprachantwort (IVR) konfigurieren** unter **Der Benutzer hört den folgenden Text bzw. die folgende aufgezeichnete Nachricht** die Frage ein, die dem Anrufer gestellt wird. Führen Sie hierzu die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="39355-231">Under **Step 7 Configure Interactive Voice Response**, under the **The user will hear the following text or recorded message** heading, specify the question to ask callers as follows:</span></span>
    
      - <span data-ttu-id="39355-232">Um die Frage im Textformat einzugeben, klicken Sie auf **Text-zu-Sprache verwenden** und geben Sie die Frage in das Textfeld ein.</span><span class="sxs-lookup"><span data-stu-id="39355-232">To enter the question in text format, click **Use text-to-speech**, and type the question in the text box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-p134">Verwenden Sie im eingegebenen Text keine HTML-Tags. Andernfalls wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39355-p134">Do not include HTML tags in the text you enter. If you include HTML tags, you will receive an error message.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-235">Das Symbol „#“ wird vom Text-zu-Sprache-Modul als das Wort „Nummer“ übersetzt.</span><span class="sxs-lookup"><span data-stu-id="39355-235">The "#" symbol is translated by the text-to-speech engine as the word "number".</span></span> <span data-ttu-id="39355-236">Wenn Sie auf die Taste # verweisen möchten, sollten Sie bei der Eingabe anstelle des Symbols den Tastennamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="39355-236">If you need to refer to the # key, you should use the key name, rather than the symbol, in your prompt.</span></span> <span data-ttu-id="39355-237">Beispiel: „Wenn Sie mit unserem Vertrieb verbunden werden möchten, drücken Sie die Rautetaste.“</span><span class="sxs-lookup"><span data-stu-id="39355-237">For example, "To talk to sales, press the pound key."</span></span>

        
        </div>
    
      - <span data-ttu-id="39355-p136">Um eine aufgezeichnete Audiodatei mit der Frage zu verwenden, klicken Sie auf **Aufzeichnung auswählen** und dann auf den Link **Aufzeichnung**, um die Datei hochzuladen. Klicken Sie im neuen Browserfenster auf **Durchsuchen**, markieren Sie die gewünschte Audiodatei und klicken Sie auf **Öffnen**. Klicken Sie auf **Hochladen**, um die Datei zu laden und geben Sie dann optional die Frage in das Textfeld ein (auf diese Weise kann die Frage und die Antwort des Anrufers an den zuständigen Agent weitergeleitet werden).</span><span class="sxs-lookup"><span data-stu-id="39355-p136">To use a prerecorded audio file that contains the question, click **Select a recording**, and then click the **a recording** link to upload the file. In the new browser window, click **Browse**, select the audio file, and then click **Open**. Click **Upload** to load the file, and then optionally you can type the question in the text box (this enables the question, and the caller’s response, to be forwarded to the responding agent).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="39355-241">Alle von Benutzern bereitgestellten Audiodateien müssen bestimmte Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="39355-241">All user-provided audio files must meet certain requirements.</span></span> <span data-ttu-id="39355-242">Ausführliche Informationen zu unterstützten Dateiformaten finden Sie unter <A href="lync-server-2013-technical-requirements-for-response-group.md">Technische Anforderungen für die Reaktionsgruppe in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="39355-242">For details about supported file formats, see <A href="lync-server-2013-technical-requirements-for-response-group.md">Technical requirements for Response Group in Lync Server 2013</A>.</span></span>

        
        </div>

29. <span data-ttu-id="39355-243">Geben Sie unter **Antwort 1** wie folgt die erste mögliche Antwort auf die Frage ein:</span><span class="sxs-lookup"><span data-stu-id="39355-243">Under **Response 1**, specify the first possible answer to the question by doing the following:</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="39355-p138">Verwenden Sie in Sprachantworten keine Anführungszeichen („“). Bei Verwendung von Anführungszeichen funktioniert die interaktive Sprachantwort nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="39355-p138">Do not use quotation marks (") in any voice responses. Quotation marks cause the IVR to fail.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-246">Sie können auswählen, ob Anrufer per Sprache, Tasteneingabe oder beidem antworten können.</span><span class="sxs-lookup"><span data-stu-id="39355-246">You can choose to allow callers to answer using speech, alphanumeric keypad input, or both.</span></span>

    
    </div>
    
      - <span data-ttu-id="39355-247">Wenn Sie zulassen möchten, dass Anrufer per Sprache antworten, geben Sie die Antwort in das Feld **Sprachantwort eingeben** ein.</span><span class="sxs-lookup"><span data-stu-id="39355-247">If you want to allow the caller to respond using speech, enter the answer in **Enter a voice response**.</span></span>
    
      - <span data-ttu-id="39355-248">Wenn Sie zulassen möchten, dass Anrufer per Tasteneingabe antworten, klicken Sie im Feld **Ziffer** auf die entsprechende Ziffer.</span><span class="sxs-lookup"><span data-stu-id="39355-248">If you want to allow the caller to respond by pressing a key on the keypad, in **Digit**, click the keypad digit.</span></span>

30. <span data-ttu-id="39355-249">Geben Sie wie folgt an, ob der Anrufer an eine Warteschleife weitergeleitet wird oder ob eine weitere Frage gestellt werden soll:</span><span class="sxs-lookup"><span data-stu-id="39355-249">Specify whether to route the caller to a queue, or to ask another question as follows:</span></span>
    
      - <span data-ttu-id="39355-250">Um den Anrufer an eine Warteschleife weiterzuleiten, klicken Sie auf **An eine Warteschleife senden** und klicken Sie unter **Warteschleife auswählen** auf die Warteschleife, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="39355-250">To route the caller to a queue, click **Send to a queue**, and in **Select a queue**, click the queue that you want to use.</span></span>
    
      - <span data-ttu-id="39355-p139">Wenn eine weitere Frage gestellt werden soll, klicken Sie auf **Eine weitere Frage stellen**, klicken Sie dann auf **Text-zu-Sprache verwenden** und geben Sie die Frage ein oder klicken Sie auf **Aufzeichnung auswählen**. Verwenden Sie die Einstellungen in diesem Abschnitt, um bis zu vier mögliche Antworten auf die zusätzliche Frage sowie die Warteschleife für jede Antwort anzugeben. Um eine dritte oder vierte mögliche Antwort anzugeben, aktivieren Sie das Kontrollkästchen **Antwort 3** oder das Kontrollkästchen **Antwort 4**.</span><span class="sxs-lookup"><span data-stu-id="39355-p139">To ask another question, click **Ask another question**, and then click **Use text-to-speech** and type the question, or click **Select a recording**. Use the response groupings in this section to specify up to four possible responses to the additional question and the queue to use for each response. To specify a third or fourth possible response, click the **Response 3** check box or the **Response 4** check box.</span></span>

31. <span data-ttu-id="39355-p140">Geben Sie bis zu drei weitere mögliche Antworten auf die ursprüngliche Frage ein, indem Sie die Schritte 28 und 29 wiederholen, um mögliche Antworten und die Aktion für jede Antwort anzugeben. Um eine dritte oder vierte mögliche Antwort anzugeben, aktivieren Sie das Kontrollkästchen **Antwort 3** oder das Kontrollkästchen **Antwort 4**.</span><span class="sxs-lookup"><span data-stu-id="39355-p140">Specify up to three more possible answers to the original question by repeating steps 28 and 29 to specify the possible responses and the action to take for each response. To specify a third or fourth possible answer, click the **Response 3** check box or the **Response 4** check box.</span></span>

32. <span data-ttu-id="39355-256">Klicken Sie auf **Bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="39355-256">Click **Deploy**.</span></span>

</div>

<div>

## <a name="to-use-windows-powershell-to-create-or-modify-an-interactive-workflow"></a><span data-ttu-id="39355-257">So verwenden Sie Windows PowerShell zum Erstellen oder Ändern eines interaktiven Workflows</span><span class="sxs-lookup"><span data-stu-id="39355-257">To use Windows PowerShell to create or modify an Interactive workflow</span></span>

1.  <span data-ttu-id="39355-258">Melden Sie sich als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Mitglied einer der vordefinierten Administratorrollen an, die Reaktionsgruppen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39355-258">Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.</span></span>

2.  <span data-ttu-id="39355-259">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="39355-259">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="39355-p141">Rufen Sie den Dienstnamen für den Reaktionsgruppendienst ab und weisen Sie ihn einer Variablen zu. Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p141">Retrieve the service name for the Response Group service and assign it to a variable. At the command line, run:</span></span>
    
        $serviceId="service:"+(Get-CSService | ?{$_.Applications -like "*RGS*"}).ServiceId;

4.  <span data-ttu-id="39355-p142">Ein interaktiver Workflow erfordert mindestens zwei Warteschlangen und mindestens zwei Agentgruppen. Erstellen Sie zunächst die Agentgruppen. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p142">An interactive workflow requires two or more queues and two or more agent groups. First, create the agent groups. Run:</span></span>
    
        $AGSupport = New-CsRgsAgentGroup -Parent $serviceId -Name "Technical Support" [-AgentAlertTime "20"] [-ParticipationPolicy "Informal"] [-RoutingMethod LongestIdle] [-AgentsByUri("sip:agent1@contoso.com", "sip:agent2@contoso.com")]
        $AGSales = New-CsRgsAgentGroup -Parent $serviceId -Name "Sales Team" [-AgentAlertTime "20"] [-ParticipationPolicy "Informal"] [-RoutingMethod LongestIdle] [-AgentsByUri("sip:bob@contoso.com", "sip:alice@contoso.com")]

5.  <span data-ttu-id="39355-p143">Erstellen Sie die Warteschlangen. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p143">Create the queues. Run:</span></span>
    
        $QSupport = New-CsRgsQueue -Parent $ServiceId -Name "Contoso Support" -AgentGroupIDList($AG-Support.Identity)
        $QSales = New-CsRgsQueue -Parent $ServiceId -Name "Contoso Sales" -AgentGroupIDList($AG-Sales.Identity)

6.  <span data-ttu-id="39355-p144">Erstellen Sie die erste Reaktionsgruppen-Eingabeaufforderung. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p144">Create the first response group prompt. Run:</span></span>
    
        $SupportPrompt = New-CsRgsPrompt -TextToSpeechPrompt "Please be patient while we connect you with Contoso Technical Support."

7.  <span data-ttu-id="39355-p145">Erstellen Sie anschließend die Aktion, die nach der Eingabeaufforderung ausgeführt werden soll. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p145">Then create the action to be performed after the prompt. Run:</span></span>
    
        $SupportAction = New-CsRgsCallAction -Prompt $SupportPrompt -Action TransferToQueue -QueueID $QSupport.Identity

8.  <span data-ttu-id="39355-p146">Erstellen Sie die erste Reaktionsgruppenantwort. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p146">Create the first response group answer. Run:</span></span>
    
        $SupportAnswer = New-CsRgsAnswer -Action $SupportAction [-DtmfResponse 1]

9.  <span data-ttu-id="39355-p147">Erstellen Sie nun die zweite Eingabeaufforderung, die zweite Anrufaktion und die zweite Antwort. Erstellen Sie zunächst die Eingabeaufforderung. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p147">Now create the second prompt, call action, and answer. First create the prompt. Run:</span></span>
    
        $SalesPrompt = New-CsRgsPrompt -TextToSpeechPrompt "Please hold while we connect you with Contoso Sales."

10. <span data-ttu-id="39355-p148">Erstellen Sie die zweite Anrufaktion. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p148">Create the second call action. Run:</span></span>
    
        $SalesAction = New-CsRgsCallAction -Prompt $SalesPrompt -Action TransferToQueue -QueueID $QSales.Identity

11. <span data-ttu-id="39355-p149">Erstellen Sie die zweite Reaktionsgruppenantwort. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p149">Create the second response group answer. Run:</span></span>
    
        $SalesAnswer = New-CsRgsAnswer -Action $SalesAction [-DtmfResponse 2]

12. <span data-ttu-id="39355-p150">Erstellen Sie die Eingabeaufforderung der obersten Ebene. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p150">Create the top-level prompt. Run:</span></span>
    
        $TopLevelPrompt = New-CsRgsPrompt -TextToSpeechPrompt "Thank you for calling Contoso. For Technical Support, press 1. For a Sales Representative, press 2."

13. <span data-ttu-id="39355-p151">Erstellen Sie die Frage der obersten Ebene. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p151">Create the top-level question. Run:</span></span>
    
        $TopLevelQuestion = New-CsRgsQuestion -Prompt $TopLevelPrompt [-AnswerList ($SupportAnswer, $SalesAnswer)]

14. <span data-ttu-id="39355-p152">Erstellen Sie nun den Workflow. Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39355-p152">Now create the workflow. Run:</span></span>
    
        $IVRAction = New-CsRgsCallAction -Action TransferToQuestion [-Question $Question]
        $IVRWorkflow = New-CsRgsWorkflow -Parent $ServiceId -Name "Contoso Helpdesk" [-Description "The Contoso Helpdesk line."] -PrimaryUri "sip:helpdesk@contoso.com" [-LineUri tel:+14255554321] [-DisplayNumber "+1 (425) 555-4321"] [-Active $true] [-Anonymous $true] [-DefaultAction $IVRAction] [-Managed $true] [-ManagersByURI ("sip:mindy@contoso.com", "sip:bob@contoso.com")]
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39355-p153">Allen Benutzern, die als Manager einer Reaktionsgruppe bestimmt wurden, muss die Rolle „CsResponseGroupManager“ zugewiesen sein. Falls Benutzern diese Rolle nicht zugewiesen ist, können sie keine Reaktionsgruppen verwalten.</span><span class="sxs-lookup"><span data-stu-id="39355-p153">All users who have been designated as manager of a response group must be assigned th CsResponseGroupManager role. If users are not assigned this role, they cannot manage response groups.</span></span>

    
    <span data-ttu-id="39355-288"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39355-288"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

