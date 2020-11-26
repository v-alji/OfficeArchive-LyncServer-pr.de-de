---
title: 'Lync Server 2013: Konfigurieren des Reverseproxys für Mobilität'
description: 'Lync Server 2013: Konfigurieren des Reverse-Proxys für Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the reverse proxy for mobility
ms:assetid: 3f4a9e33-77e4-4c18-a73f-24d4bec8ea9c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690011(v=OCS.15)
ms:contentKeyID: 48183946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4e1a71f97bc1737299d54cc0f4c56f0f5981bef
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432485"
---
# <a name="configuring-the-reverse-proxy-for-mobility-in-lync-server-2013"></a><span data-ttu-id="a8671-103">Konfigurieren des Reverseproxys für Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8671-103">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8671-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8671-104">

<span> </span></span></span>

<span data-ttu-id="a8671-105">_**Letztes Änderungsdatum des Themas:** 2014-03-20_</span><span class="sxs-lookup"><span data-stu-id="a8671-105">_**Topic Last Modified:** 2014-03-20_</span></span>

<span data-ttu-id="a8671-106">Wenn Sie die automatische Ermittlung für Clients für mobile Geräte verwenden möchten, müssen Sie eine vorhandene oder eine neue Webveröffentlichungsregel für den Reverseproxy ändern, unabhängig davon, ob Sie die Listen Betreff alternativer Name auf den Reverse-Proxy Zertifikaten aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8671-106">If you want to use automatic discovery for mobile device clients, you need to modify an existing or create a new web publishing rule for the reverse proxy whether or not you update the subject alternative name lists on the reverse proxy certificates.</span></span>

<span data-ttu-id="a8671-107">Wenn Sie sich entschließen, HTTPS für anfängliche lync Server 2013-Erkennungsdienst Anforderungen zu verwenden und die Listen Betreff Alternative Namen auf den Reverse-Proxy Zertifikaten zu aktualisieren, müssen Sie das aktualisierte öffentliche Zertifikat dem Secure Sockets Layer (SSL)-Listener auf dem Reverse-Proxy zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a8671-107">If you decide to use HTTPS for initial Lync Server 2013 Autodiscover Service requests and update the subject alternative names lists on the reverse proxy certificates, you need to assign the updated public certificate to the Secure Sockets Layer (SSL) Listener on your reverse proxy.</span></span> <span data-ttu-id="a8671-108">Details zu den erforderlichen Einträgen für Alternativen Betreff finden Sie unter [Technische Voraussetzungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="a8671-108">For details about the required subject alternative name entries, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="a8671-109">Anschließend müssen Sie den vorhandenen Listener für die externen Webdienste ändern oder eine neue Webveröffentlichungsregel für die externe AutoErmittlungsdienst-URL erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8671-109">You then need to modify the existing listener for the external web services or create a new web publishing rule for the external Autodiscover Service URL.</span></span> <span data-ttu-id="a8671-110">Wenn Sie noch keine Webveröffentlichungsregel für die externe lync Server 2013-Webdienste-URL für Ihren Front-End-Pool besitzen, müssen Sie auch eine Regel dafür veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="a8671-110">If you do not already have a web publishing rule for the external Lync Server 2013 Web Services URL for your Front End pool, you also need to publish a rule for that.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a8671-111">Die Reverse Proxy-Veröffentlichungsregel und der Listener können sowohl die externen Webdienste als auch den AutoErmittlungsdienst bedienen, solange das dem Listener zugewiesene Zertifikat den erforderlichen Namen und die alternativen Subjektnamen für beide enthält.</span><span class="sxs-lookup"><span data-stu-id="a8671-111">The reverse proxy publishing rule and listener can service both the external web services and the Autodiscover Service, as long as the certificate assigned to the listener contains the necessary subject name and subject alternative names for both.</span></span> <span data-ttu-id="a8671-112">Details zur Standardkonfiguration der Weblistener-und Veröffentlichungsregel finden Sie unter <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Einrichten von Reverse-Proxyservern für lync Server 2013</A> für weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="a8671-112">For details on the default configuration of the web listener and publishing rule, see <A href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</A> for more details.</span></span>



</div>

<span data-ttu-id="a8671-113">Wenn Sie sich entschließen, http für anfängliche AutoErmittlungsdienst Anforderungen zu verwenden, damit Sie keine alternativen Antragstellernamen für den Reverse-Proxy aktualisieren müssen, müssen Sie eine Webveröffentlichungsregel für Port 80 erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="a8671-113">If you decide to use HTTP for initial Autodiscover Service requests so that you do not need to update subject alternative names for the reverse proxy, you need to create or modify a web publishing rule for port 80.</span></span>

<span data-ttu-id="a8671-114">Die Verfahren in diesem Abschnitt beschreiben, wie Sie die Webveröffentlichungsregeln in Microsoft Forefront Threat Management Gateway 2010 für die automatische Ermittlung erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="a8671-114">The procedures in this section describe how to create or modify the web publishing rules in Microsoft Forefront Threat Management Gateway 2010 for automatic discovery.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a8671-115">Bei diesen Verfahren wird davon ausgegangen, dass Sie die Standard Edition von Forefront Threat Management Gateway (TMG) 2010 installiert haben.</span><span class="sxs-lookup"><span data-stu-id="a8671-115">These procedures assume that you have installed the Standard Edition of Forefront Threat Management Gateway (TMG) 2010.</span></span> <span data-ttu-id="a8671-116">Wenn Sie einen anderen Reverseproxy verwenden, sind die Verfahren ähnlich, müssen aber der Dokumentation des Drittanbieterprodukts zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="a8671-116">If you are using another reverse proxy, the procedures are similar, but will need to be mapped to the documentation for the third-party product.</span></span>



</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-the-external-autodiscover-url"></a><span data-ttu-id="a8671-117">So erstellen Sie eine Webveröffentlichungsregel für die externe Auto Ermittlungs-URL</span><span class="sxs-lookup"><span data-stu-id="a8671-117">To create a web publishing rule for the external Autodiscover URL</span></span>

1.  <span data-ttu-id="a8671-118">Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft Forefront TMG**, und klicken Sie dann auf **Forefront TMG-Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="a8671-118">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="a8671-119">Erweitern Sie im linken Bereich **Servername**, klicken Sie mit der rechten Maustaste auf **Firewall-Richtlinie**, zeigen Sie auf **neu**, und klicken Sie dann auf **Website Veröffentlichungsregel**.</span><span class="sxs-lookup"><span data-stu-id="a8671-119">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="a8671-120">Geben Sie auf der Seite **Willkommen bei der neuen Webveröffentlichungsregel** einen Anzeigenamen für die neue Veröffentlichungsregel ein (beispielsweise LyncDiscoveryURL).</span><span class="sxs-lookup"><span data-stu-id="a8671-120">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, LyncDiscoveryURL).</span></span>

4.  <span data-ttu-id="a8671-121">Wählen Sie auf der Seite **Regelaktion auswählen** die Option **zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-121">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="a8671-122">Wählen Sie auf der Seite **Veröffentlichungs** **eine einzelne Website oder ein Lastenausgleichsmodul veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-122">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="a8671-123">Wählen Sie auf der Seite **Server Verbindungssicherheit** die Option **SSL verwenden aus, um eine Verbindung mit dem veröffentlichten Webserver oder der Serverfarm herzustellen**.</span><span class="sxs-lookup"><span data-stu-id="a8671-123">On the **Server Connection Security** page, select **Use SSL to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="a8671-124">Geben Sie auf der Seite **interne Veröffentlichungs Details** unter **interner Websitename** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) Ihres Director-Pools ein (beispielsweise "lyncdir01. contoso. local").</span><span class="sxs-lookup"><span data-stu-id="a8671-124">On the **Internal Publishing Details** page, in **Internal Site name**, type the fully qualified domain name (FQDN) of your Director pool (for example, lyncdir01.contoso.local).</span></span> <span data-ttu-id="a8671-125">Wenn Sie eine Regel für die externe Webdienste-URL im Front-End-Pool erstellen, geben Sie die VIP-Adresse des Hardware Load Balancer (HLB) vor dem Front-End-Pool ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-125">If you are creating a rule for the external Web Services URL on the Front End pool, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="a8671-126">Geben Sie auf der Seite **interne Veröffentlichungs Details** in **Path (optional)** **/ \* *_ als Pfad des zu veröffentlichenden Ordners ein, und wählen Sie dann _* forward the Originalhost Header** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-126">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header\*\*.</span></span>

9.  <span data-ttu-id="a8671-127">Führen Sie auf der Seite " **Details zum öffentlichen Namen** " die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a8671-127">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="a8671-128">Wählen Sie unter **Anforderungen annehmen für** **den folgenden Domänennamen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-128">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="a8671-129">Geben Sie in **Öffentlicher Name** **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="a8671-129">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="a8671-130">(die URL des externen AutoErmittlungsdiensts).</span><span class="sxs-lookup"><span data-stu-id="a8671-130">(the external Autodiscover Service URL).</span></span> <span data-ttu-id="a8671-131">Wenn Sie eine Regel für die externe Webdienste-URL im Front-End-Pool erstellen, geben Sie den FQDN für die externen Webdienste in Ihrem Front-End-Pool ein (beispielsweise lyncwebextpool01.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a8671-131">If you are creating a rule for the external Web Services URL on the Front End pool, type the FQDN for the external Web Services on your Front End pool (for example, lyncwebextpool01.contoso.com).</span></span>
    
      - <span data-ttu-id="a8671-132">Geben Sie in **path**\* */\** _ ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-132">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="a8671-133">Wählen Sie auf _ *Weblistener*\* Seite auswählen im **Weblistener** Ihren vorhandenen SSL-Listener mit dem aktualisierten öffentlichen Zertifikat aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-133">On _ *Select Web Listener*\* page, in **Web Listener**, select your existing SSL Listener with the updated public certificate.</span></span>

11. <span data-ttu-id="a8671-134">Wählen Sie auf der Seite **Authentifizierungsdelegierung** **keine Delegierung aus, aber der Client kann sich direkt authentifizieren**.</span><span class="sxs-lookup"><span data-stu-id="a8671-134">On the **Authentication Delegation** page, select **No delegation, but client may authenticate directly**.</span></span>

12. <span data-ttu-id="a8671-135">Wählen Sie auf der Seite **Benutzer festlegen** **alle Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-135">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="a8671-136">Überprüfen Sie auf der Seite zum **Abschließen der neuen Webveröffentlichungsregel** , ob die Einstellungen für die Webveröffentlichungsregel richtig sind, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="a8671-136">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="a8671-137">Doppelklicken Sie in der Liste der Forefront TMG-Webveröffentlichungsregeln auf die neue Regel, die Sie soeben hinzugefügt haben, um **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8671-137">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="a8671-138">Führen Sie auf der Registerkarte **an** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a8671-138">On the **To** tab, do the following:</span></span>
    
      - <span data-ttu-id="a8671-139">Wählen Sie **den ursprünglichen Hostheader anstelle des tatsächlichen weiterleiten** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-139">Select **Forward the original host header instead of the actual one**.</span></span>
    
      - <span data-ttu-id="a8671-140">Select- **Anforderungen scheinen vom Forefront TMG-Computer zu stammen**.</span><span class="sxs-lookup"><span data-stu-id="a8671-140">Select **Requests appear to come from the Forefront TMG computer**.</span></span>

16. <span data-ttu-id="a8671-141">Konfigurieren Sie auf der Registerkarte **Bridging** Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a8671-141">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="a8671-142">Wählen Sie **Webserver** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-142">Select **Web server**.</span></span>
    
      - <span data-ttu-id="a8671-143">Wählen Sie **Anforderungen an http-Port umleiten** aus, und geben Sie **8080** für die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-143">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="a8671-144">Wählen Sie **Anforderungen an SSL-Port umleiten** aus, und geben Sie **4443** für die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-144">Select **Redirect requests to SSL port**, and type **4443** for the port number.</span></span>

17. <span data-ttu-id="a8671-145">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8671-145">Click **OK**.</span></span>

18. <span data-ttu-id="a8671-146">Klicken Sie im Detailbereich auf über **nehmen** , um die Änderungen zu speichern und die Konfiguration zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8671-146">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

19. <span data-ttu-id="a8671-147">Klicken Sie auf **Regel testen** , um zu überprüfen, ob Ihre neue Regel ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a8671-147">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-modify-an-existing-web-publishing-rule-to-add-the-external-autodiscover-san-and-url"></a><span data-ttu-id="a8671-148">So ändern Sie eine vorhandene Webveröffentlichungsregel, um den externen Auto Ermittlungs-San und die URL hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="a8671-148">To modify an existing web publishing rule to add the external Autodiscover SAN and URL</span></span>

1.  <span data-ttu-id="a8671-149">Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft Forefront TMG**, und klicken Sie dann auf **Forefront TMG-Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="a8671-149">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a8671-150">Sie werden die Änderung für jede Veröffentlichungsregel und jeden Listener wiederholen, die Sie haben.</span><span class="sxs-lookup"><span data-stu-id="a8671-150">You will repeat the modification for each publishing rule and listener that you have.</span></span> <span data-ttu-id="a8671-151">In der Regel handelt es sich um eine Regel und einen Listener für die Front-End-Pools und einen für die optionalen Directors-oder Director-Pools, wenn Sie diese bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="a8671-151">Typically, this will be one rule and listener for the Front End pools and one for the optional Directors or Director pools, if you have deployed them.</span></span>

    
    </div>

2.  <span data-ttu-id="a8671-152">Erweitern Sie im linken Bereich **Servername**, klicken Sie mit der rechten Maustaste auf **Firewall-Richtlinie**, und klicken Sie auf die entsprechende Regel.</span><span class="sxs-lookup"><span data-stu-id="a8671-152">In the left pane, expand **ServerName**, right-click **Firewall Policy**, click the applicable rule.</span></span> <span data-ttu-id="a8671-153">Klicken Sie auf der Registerkarte **Aufgaben** auf **ausgewählte Regel bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="a8671-153">On the **Tasks** tab, click **Edit Selected rule**.</span></span>

3.  <span data-ttu-id="a8671-154">Wählen Sie auf der Registerkarte **Öffentlicher Name** in **dieser Regel gilt** für **die Option Anforderungen für die folgenden Websites** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-154">On the **Public Name** tab, in **This rule applies to**, select **Requests for the following Web sites**.</span></span>

4.  <span data-ttu-id="a8671-155">Klicken Sie auf **Hinzufügen**, geben Sie den Namen der neuen Auto Ermittlungs Website ein (beispielsweise "lyncdiscover.contoso.com"), und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8671-155">Click **Add**, type the name of the new Autodiscover site (for example, “lyncdiscover.contoso.com”), and then click **OK**.</span></span>

5.  <span data-ttu-id="a8671-156">Klicken Sie auf der Registerkarte **Listener** auf **Zertifikat auswählen** , und weisen Sie dem hinzugefügten San-Eintrag für die AutoErmittlung das neue Zertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="a8671-156">On the **Listener** tab, click **Select Certificate** and assign the new certificate with the added Autodiscover SAN entries.</span></span> <span data-ttu-id="a8671-157">Schließen Sie die Listener-und Webveröffentlichungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a8671-157">Close the Listener and Web Publishing properties.</span></span>

6.  <span data-ttu-id="a8671-158">Klicken Sie im Detailbereich auf über **nehmen** , um die Änderungen zu speichern und die Konfiguration zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8671-158">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

7.  <span data-ttu-id="a8671-159">Klicken Sie auf **Regel testen** , um zu überprüfen, ob Ihre neue Regel ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a8671-159">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

</div>

<div>

## <a name="to-create-a-web-publishing-rule-for-port-80"></a><span data-ttu-id="a8671-160">So erstellen Sie eine Webveröffentlichungsregel für Port 80</span><span class="sxs-lookup"><span data-stu-id="a8671-160">To create a web publishing rule for port 80</span></span>

1.  <span data-ttu-id="a8671-161">Klicken Sie auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Microsoft Forefront TMG**, und klicken Sie dann auf **Forefront TMG-Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="a8671-161">Click **Start**, point to **Programs**, point to **Microsoft Forefront TMG**, and then click **Forefront TMG Management**.</span></span>

2.  <span data-ttu-id="a8671-162">Erweitern Sie im linken Bereich **Servername**, klicken Sie mit der rechten Maustaste auf **Firewall-Richtlinie**, zeigen Sie auf **neu**, und klicken Sie dann auf **Website Veröffentlichungsregel**.</span><span class="sxs-lookup"><span data-stu-id="a8671-162">In the left pane, expand **ServerName**, right-click **Firewall Policy**, point to **New**, and then click **Web Site Publishing Rule**.</span></span>

3.  <span data-ttu-id="a8671-163">Geben Sie auf der Seite **Willkommen bei der neuen Webveröffentlichungsregel** einen Anzeigenamen für die neue Veröffentlichungsregel ein (beispielsweise lync AutoErmittlung (http)).</span><span class="sxs-lookup"><span data-stu-id="a8671-163">On the **Welcome to the New Web Publishing Rule** page, type a display name for the new publishing rule (for example, Lync Autodiscover (HTTP)).</span></span>

4.  <span data-ttu-id="a8671-164">Wählen Sie auf der Seite **Regelaktion auswählen** die Option **zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-164">On the **Select Rule Action** page, select **Allow**.</span></span>

5.  <span data-ttu-id="a8671-165">Wählen Sie auf der Seite **Veröffentlichungs** **eine einzelne Website oder ein Lastenausgleichsmodul veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-165">On the **Publishing Type** page, select **Publish a single Web site or load balancer**.</span></span>

6.  <span data-ttu-id="a8671-166">Wählen Sie auf der Seite **Server Verbindungssicherheit** die Option **nicht gesicherte Verbindungen verwenden aus, um eine Verbindung mit dem veröffentlichten Webserver oder der Serverfarm herzustellen**.</span><span class="sxs-lookup"><span data-stu-id="a8671-166">On the **Server Connection Security** page, select **Use non-secured connections to connect to the published Web server or server farm**.</span></span>

7.  <span data-ttu-id="a8671-167">Geben Sie auf der Seite **interne Veröffentlichungs Details** unter **interner Websitename** die VIP-Adresse des Hardware Lastenausgleichs (Hardware Load Balancer, HLB) vor dem Front-End-Pool ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-167">On the **Internal Publishing Details** page, in **Internal Site name**, type the VIP address of the Hardware Load Balancer (HLB) in front of the Front End pool.</span></span>

8.  <span data-ttu-id="a8671-168">Geben Sie auf der Seite **interne Veröffentlichungs Details** in **Path (optional)** **/ \* *_ als Pfad des zu veröffentlichenden Ordners ein, und wählen Sie dann _* forward the Originalhost Header anstelle der im Feld Interner Websitename angegebenen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-168">On the **Internal Publishing Details** page, in **Path (optional)**, type \**/\**_ as the path of the folder to be published, and then select _\* Forward the original host header instead of the one specified in the Internal site name field\*\*.</span></span>

9.  <span data-ttu-id="a8671-169">Führen Sie auf der Seite " **Details zum öffentlichen Namen** " die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a8671-169">On the **Public Name Details** page, do the following:</span></span>
    
      - <span data-ttu-id="a8671-170">Wählen Sie unter **Anforderungen annehmen für** **den folgenden Domänennamen** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-170">Under **Accept Requests for**, select **This domain name**.</span></span>
    
      - <span data-ttu-id="a8671-171">Geben Sie in **Öffentlicher Name** **lyncdiscover.**\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="a8671-171">In **Public Name**, type **lyncdiscover.**\<sipdomain\></span></span> <span data-ttu-id="a8671-172">(die URL des externen AutoErmittlungsdiensts).</span><span class="sxs-lookup"><span data-stu-id="a8671-172">(the external Autodiscover Service URL).</span></span>
    
      - <span data-ttu-id="a8671-173">Geben Sie in **path**\* */\** _ ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-173">In **Path**, type \**/\** _.</span></span>

10. <span data-ttu-id="a8671-174">Wählen Sie auf _ *Weblistener*\* Seite auswählen im **Weblistener** einen Weblistener aus, oder verwenden Sie den Assistenten für neue Weblistener-Definition, um eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8671-174">On _ *Select Web Listener*\* page, in **Web Listener**, select a Web Listener or use the New Web Listener Definition Wizard to create a new one.</span></span>

11. <span data-ttu-id="a8671-175">Wählen Sie auf der Seite **Authentifizierungsdelegierung** **keine Delegierung aus, und der Client kann sich nicht direkt authentifizieren**.</span><span class="sxs-lookup"><span data-stu-id="a8671-175">On the **Authentication Delegation** page, select **No delegation, and client cannot authenticate directly**.</span></span>

12. <span data-ttu-id="a8671-176">Wählen Sie auf der Seite **Benutzer festlegen** **alle Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-176">On the **User Set** page, select **All Users**.</span></span>

13. <span data-ttu-id="a8671-177">Überprüfen Sie auf der Seite zum **Abschließen der neuen Webveröffentlichungsregel** , ob die Einstellungen für die Webveröffentlichungsregel richtig sind, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="a8671-177">On the **Completing the New Web Publishing Rule Wizard** page, verify that the web publishing rule settings are correct, and then click **Finish**.</span></span>

14. <span data-ttu-id="a8671-178">Doppelklicken Sie in der Liste der Forefront TMG-Webveröffentlichungsregeln auf die neue Regel, die Sie soeben hinzugefügt haben, um **Eigenschaften** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8671-178">In the Forefront TMG list of web publishing rules, double-click the new rule you just added to open **Properties**.</span></span>

15. <span data-ttu-id="a8671-179">Konfigurieren Sie auf der Registerkarte **Bridging** Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a8671-179">On the **Bridging** tab, configure the following:</span></span>
    
      - <span data-ttu-id="a8671-180">Wählen Sie **Webserver** aus.</span><span class="sxs-lookup"><span data-stu-id="a8671-180">Select **Web server**.</span></span>
    
      - <span data-ttu-id="a8671-181">Wählen Sie **Anforderungen an http-Port umleiten** aus, und geben Sie **8080** für die Portnummer ein.</span><span class="sxs-lookup"><span data-stu-id="a8671-181">Select **Redirect requests to HTTP port**, and type **8080** for the port number.</span></span>
    
      - <span data-ttu-id="a8671-182">Vergewissern Sie sich, dass " **Anforderungen an SSL-Port umleiten** " nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8671-182">Verify that **Redirect requests to SSL port** is not selected.</span></span>

16. <span data-ttu-id="a8671-183">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8671-183">Click **OK**.</span></span>

17. <span data-ttu-id="a8671-184">Klicken Sie im Detailbereich auf über **nehmen** , um die Änderungen zu speichern und die Konfiguration zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a8671-184">Click **Apply** in the details pane to save the changes and update the configuration.</span></span>

18. <span data-ttu-id="a8671-185">Klicken Sie auf **Regel testen** , um zu überprüfen, ob Ihre neue Regel ordnungsgemäß eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a8671-185">Click **Test Rule** to verify that your new rule is set up correctly.</span></span>

19. <span data-ttu-id="a8671-186">Überprüfen Sie, ob die URL des externen AutoErmittlungsdiensts in einer anderen Webveröffentlichungsregel nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a8671-186">Verify that the external Autodiscover Service URL is not defined on any other web publishing rule.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a8671-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8671-187">See Also</span></span>


[<span data-ttu-id="a8671-188">Einrichten von Reverseproxyservern für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8671-188">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)  
[<span data-ttu-id="a8671-189">Technische Anforderungen für die Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8671-189">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  
  

<span data-ttu-id="a8671-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8671-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

