---
title: 'Lync Server 2013: Konfigurieren von Zertifikaten für die AutoErmittlung'
description: 'Lync Server 2013: Konfigurieren von Zertifikaten für die AutoErmittlung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring certificates for Autodiscover
ms:assetid: 1842191d-df9a-41e0-9286-08c25f9b5dca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945617(v=OCS.15)
ms:contentKeyID: 51541453
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98ab9eca92685eef8bccc500dc4a91efa891dec6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393830"
---
# <a name="configuring-certificates-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="42f81-103">Konfigurieren von Zertifikaten für die AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="42f81-103">Configuring certificates for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="42f81-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="42f81-104">

<span> </span></span></span>

<span data-ttu-id="42f81-105">_**Letztes Änderungsdatum des Themas:** 2012-12-12_</span><span class="sxs-lookup"><span data-stu-id="42f81-105">_**Topic Last Modified:** 2012-12-12_</span></span>

<span data-ttu-id="42f81-106">Die Zertifikate für den Director-Pool, den Front-End-Pool und den Reverse-Proxy erfordern zusätzliche Alternative Namenseinträge, um sichere Verbindungen mit lync-Clients zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="42f81-106">The certificates for your Director pool, Front End pool, and reverse proxy require additional subject alternative name entries to support secure connections with Lync clients.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="42f81-107">Sie können das Cmdlet <STRONG>Get-CsCertificate</STRONG> verwenden, um Informationen zu den aktuell zugewiesenen Zertifikaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="42f81-107">You can use the <STRONG>Get-CsCertificate</STRONG> cmdlet to view information about the currently assigned certificates.</span></span> <span data-ttu-id="42f81-108">Die Standardansicht schneidet jedoch die Eigenschaften des Zertifikats ab und zeigt nicht alle Werte in der SubjectAlternativeNames-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="42f81-108">However, the default view truncates the properties of the certificate and does not display all values in the SubjectAlternativeNames property.</span></span> <span data-ttu-id="42f81-109">Sie können die Cmdlets " <STRONG>Get-CsCertificate</STRONG> ", " <STRONG>Request-</STRONG>CsCertificate" und " <STRONG>Satz-CsCertificate</STRONG> " verwenden, um einige Informationen anzuzeigen und Zertifikate anzufordern und zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="42f81-109">You can use the <STRONG>Get-CsCertificate</STRONG> , <STRONG>Request-</STRONG>CsCertificate and the <STRONG>Set-CsCertificate</STRONG> cmdlets to view some information and to request and assign certificates.</span></span> <span data-ttu-id="42f81-110">Allerdings ist es nicht die beste Methode, wenn Sie sich nicht sicher sind, welche Eigenschaften das "Subject Alternative Names (San)" für das aktuelle Zertifikat hat.</span><span class="sxs-lookup"><span data-stu-id="42f81-110">However, it’s not the best method to use if you are unsure of the properties of the subject alternative names (SAN) on the current certificate.</span></span> <span data-ttu-id="42f81-111">Zum Anzeigen des Zertifikats und aller Eigenschafts Mitglieder wird empfohlen, das Zertifikat-Snap-in der <EM>Microsoft Management Console (MMC)</EM> zu verwenden oder den lync Server-Bereitstellungs-Assistenten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-111">To view the certificate and all property members, it is suggested to use the Certificates snap-in the <EM>Microsoft Management Console (MMC)</EM> or to use the Lync Server Deployment Wizard.</span></span> <span data-ttu-id="42f81-112">Im lync Server-Bereitstellungs-Assistenten können Sie den Zertifikat-Assistenten verwenden, um die Zertifikateigenschaften anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="42f81-112">In the Lync Server Deployment Wizard, you can use the Certificate Wizard to view the certificate properties.</span></span> <span data-ttu-id="42f81-113">Die Verfahren zum Anzeigen, anfordern und Zuweisen eines Zertifikats mithilfe der lync Server-Verwaltungsshell und der <EM>Microsoft Management Console (MMC)</EM> sind in den folgenden Verfahren detailliert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="42f81-113">The procedures for viewing, requesting and assigning a certificate using the Lync Server Management Shell and the <EM>Microsoft Management Console (MMC)</EM> are detailed in the following procedures.</span></span> <span data-ttu-id="42f81-114">Informationen zum Verwenden des lync Server-Bereitstellungs-Assistenten finden Sie hier, wenn Sie den optionalen Director-oder Director-Pool bereitgestellt haben: <A href="lync-server-2013-configure-certificates-for-the-director.md">Konfigurieren von Zertifikaten für den Director in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="42f81-114">To use the Lync Server Deployment Wizard, see details here if you have deployed the optional Director or Director pool: <A href="lync-server-2013-configure-certificates-for-the-director.md">Configure certificates for the Director in Lync Server 2013</A>.</span></span> <span data-ttu-id="42f81-115">Informationen zu Front-End-Servern oder Front-End-Pools finden Sie hier: <A href="lync-server-2013-configure-certificates-for-servers.md">Konfigurieren von Zertifikaten für Server in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="42f81-115">For the Front End Server or Front End pool, see the details here: <A href="lync-server-2013-configure-certificates-for-servers.md">Configure certificates for servers in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="42f81-116">Die ersten Schritte in diesem Verfahren sind Vorbereitungsschritte, mit denen Sie sich orientieren können, welche Rolle die aktuellen Zertifikate spielen.</span><span class="sxs-lookup"><span data-stu-id="42f81-116">The initial steps in this procedure are preparation steps, to orient you as to what role the current certificates play.</span></span> <span data-ttu-id="42f81-117">Standardmäßig haben die Zertifikate keinen lyncdiscover. &lt; sipdomain &gt; oder lyncdiscoverinternal. &lt; Interner Domänennamen &gt; Eintrag, es sei denn, Sie haben zuvor Mobilitätsdienste installiert oder Ihre Zertifikate im Voraus vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="42f81-117">By default, the certificates will not have a lyncdiscover.&lt;sipdomain&gt; or lyncdiscoverinternal.&lt;internal domain name&gt; entry unless you have previously installed Mobility Services or have prepared your certificates in advance.</span></span> <span data-ttu-id="42f81-118">Bei diesem Verfahren wird der SIP-Domänenname "contoso.com" und der Beispiel interne Domänenname "contoso.net" verwendet.</span><span class="sxs-lookup"><span data-stu-id="42f81-118">This procedure uses the example SIP domain name ‘contoso.com’ and the example internal domain name ‘contoso.net’.</span></span><BR><span data-ttu-id="42f81-119">Die Standardzertifikat Konfiguration für lync Server 2013 und lync Server 2010 besteht darin, ein einzelnes Zertifikat (mit dem Namen "Standard") mit dem Standard für die Zwecke zu verwenden (für alle Zwecke mit Ausnahme der Webdienste), WebServicesExternal und WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="42f81-119">The default certificate configuration for Lync Server 2013 and Lync Server 2010 is to use a single certificate (named ‘Default’) with the purposes Default (for all purposes except for the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="42f81-120">Eine optionale Konfiguration besteht darin, für jeden Zweck separate Zertifikate zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-120">An optional configuration is to use separate certificates for each purpose.</span></span> <span data-ttu-id="42f81-121">Zertifikate können mithilfe der lync Server-Verwaltungsshell und Windows PowerShell-Cmdlets oder mithilfe des Zertifikat-Assistenten im lync Server-Bereitstellungs-Assistenten verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="42f81-121">Certificates can be managed by using the Lync Server Management Shell and Windows PowerShell cmdlets, or by using the Certificate Wizard in the Lync Server Deployment Wizard.</span></span>



</div>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="42f81-122">So aktualisieren Sie Zertifikate mit neuen alternativen Subjektnamen mithilfe der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="42f81-122">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="42f81-123">Melden Sie sich bei dem Computer mit einem Konto an, das über lokale Administratorrechte und-Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="42f81-123">Log on to the computer using an account that has local administrator rights and permissions.</span></span>

2.  <span data-ttu-id="42f81-124">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="42f81-124">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="42f81-125">Finden Sie heraus, welche Zertifikate dem Server zugewiesen wurden und für welche Art von Verwendung.</span><span class="sxs-lookup"><span data-stu-id="42f81-125">Find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="42f81-126">Sie benötigen diese Informationen im nächsten Schritt, um das aktualisierte Zertifikat zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="42f81-126">You need this information in the next step to assign the updated certificate.</span></span> <span data-ttu-id="42f81-127">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-127">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="42f81-128">Sehen Sie in der Ausgabe des vorherigen Schritts nach, ob ein einzelnes Zertifikat für mehrere Verwendungen zugewiesen ist oder ob für jede Verwendung ein anderes Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-128">Look in the output from the previous step to see whether a single certificate is assigned for multiple uses or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="42f81-129">Schauen Sie sich den use-Parameter an, um zu erfahren, wie ein Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="42f81-129">Look in the Use parameter to find out how a certificate is used.</span></span> <span data-ttu-id="42f81-130">Vergleichen Sie den Parameter Fingerabdruck für die angezeigten Zertifikate, um festzustellen, ob dasselbe Zertifikat mehrere Verwendungszwecke aufweist.</span><span class="sxs-lookup"><span data-stu-id="42f81-130">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span>

5.  <span data-ttu-id="42f81-131">Aktualisieren Sie das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="42f81-131">Update the certificate.</span></span> <span data-ttu-id="42f81-132">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-132">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="42f81-133">Wenn beispielsweise das Cmdlet " **Get-CsCertificate** " ein Zertifikat mit der Verwendung von Default, einem anderen mit einer Verwendung von WebServicesInternal und einem anderen mit einer Verwendung von WebServicesExternal und alle denselben Fingerabdruckwert aufweisen, geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-133">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="42f81-134">**Wichtig:**</span><span class="sxs-lookup"><span data-stu-id="42f81-134">**Important:**</span></span>
    
    <span data-ttu-id="42f81-135">Wenn für jede Verwendung ein separates Zertifikat zugewiesen wird (der Fingerabdruckwert ist für jedes Zertifikat anders), ist es wichtig, dass Sie das Cmdlet " **festgelegt-CsCertificate** " nicht mit mehreren Typen ausführen.</span><span class="sxs-lookup"><span data-stu-id="42f81-135">If a separate certificate is assigned for each use (the Thumbprint value is different for each certificate), it is important that you do not run the **Set-CsCertificate** cmdlet with multiple types.</span></span> <span data-ttu-id="42f81-136">Führen Sie in diesem Fall das Cmdlet " **Satz-CsCertificate** " für jede Verwendung separat aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-136">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="42f81-137">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42f81-137">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="42f81-138">Klicken Sie zum Anzeigen des Zertifikats auf **Start**, klicken Sie auf **ausführen.**...</span><span class="sxs-lookup"><span data-stu-id="42f81-138">To view the certificate, click **Start**, click **Run…**.</span></span> <span data-ttu-id="42f81-139">Geben Sie MMC ein, um die Microsoft Management Console zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="42f81-139">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="42f81-140">Wählen Sie im MMC-Menü **Datei** aus, wählen Sie **Snap-in hinzufügen/entfernen** aus, und wählen Sie Zertifikate aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-140">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="42f81-141">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="42f81-141">Click **Add**.</span></span> <span data-ttu-id="42f81-142">Wenn Sie dazu aufgefordert werden, wählen Sie **Computer Konto** aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="42f81-142">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="42f81-143">Wenn sich das Zertifikat auf diesem Computer befindet, wählen Sie **lokaler Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-143">If the certificate is located on this computer, select **Local computer**.</span></span> <span data-ttu-id="42f81-144">Wenn sich das Zertifikat auf einem anderen Computer befindet, wählen Sie **einen anderen Computer** aus, geben Sie den vollqualifizierten Domänennamen des Computers ein, oder klicken Sie auf **Durchsuchen** **Geben Sie den zu wählenden Objektnamen** ein, und geben Sie den Namen des Computers ein.</span><span class="sxs-lookup"><span data-stu-id="42f81-144">If the certificate is located on another computer, select **Another computer**, type in the fully qualified domain name of the computer or click **Browse** In **Enter the object name to select**, type the name of the computer.</span></span> <span data-ttu-id="42f81-145">Klicken Sie auf **Namen überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="42f81-145">Click **Check Names**.</span></span> <span data-ttu-id="42f81-146">Wenn der Name des Computers aufgelöst wird, wird er unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="42f81-146">When the name of the computer is resolved, it will be underlined.</span></span> <span data-ttu-id="42f81-147">Klicken Sie auf **OK** und dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="42f81-147">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="42f81-148">Klicken Sie auf **OK** , um die Auswahl zu bestätigen, und schließen Sie das Dialogfeld **Snap-Ins hinzufügen oder entfernen** .</span><span class="sxs-lookup"><span data-stu-id="42f81-148">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="42f81-149">Wenn das Zertifikat nicht in der Konsole angezeigt wird, stellen Sie sicher, dass Sie keinen Benutzer oder Dienst ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="42f81-149">If the certificate does not show up in the console, ensure that you have not selected User or Service.</span></span> <span data-ttu-id="42f81-150">Sie müssen Computer auswählen, oder Sie können das probper-Zertifikat nicht finden.</span><span class="sxs-lookup"><span data-stu-id="42f81-150">You must select Computer, or you will not be able to locate the probper certificate.</span></span>

    
    </div>

9.  <span data-ttu-id="42f81-151">Wenn Sie die Eigenschaften des Zertifikats anzeigen möchten, erweitern Sie **Zertifikate**, erweitern Sie **Personal**, und wählen Sie **Zertifikate** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-151">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="42f81-152">Wählen Sie das Zertifikat aus, das Sie anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Zertifikat, und wählen Sie **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-152">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="42f81-153">Wählen Sie in der **Zertifikat** Ansicht **Details** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-153">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="42f81-154">Hier können Sie den Namen des Zertifikat Antragstellers auswählen, indem Sie **Betreff** auswählen und der zugewiesene Antragstellername und die zugehörigen Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="42f81-154">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="42f81-155">Wenn Sie die alternativen Namen des zugewiesenen betreffs anzeigen möchten, wählen Sie **alternativer Betreffname** aus.</span><span class="sxs-lookup"><span data-stu-id="42f81-155">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="42f81-156">Alle zugewiesenen Subjekt alternativen Namen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42f81-156">All assigned subject alternative names are displayed.</span></span> <span data-ttu-id="42f81-157">Die in der Eigenschaft gefundenen Alternativen Betreff-Namen sind standardmäßig vom Typ **DNS-Name** .</span><span class="sxs-lookup"><span data-stu-id="42f81-157">The subject alternative names that are found in the property are of type **DNS Name** by default.</span></span> <span data-ttu-id="42f81-158">Die folgenden Member sollten angezeigt werden (alle sollten vollqualifizierte Domänennamen sein, die in DNS-Hosteinträgen (A oder, wenn IPv6 AAAA) dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="42f81-158">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="42f81-159">Poolname für diesen Pool oder der Name des einzelnen Servers, wenn es sich nicht um einen Pool handelt</span><span class="sxs-lookup"><span data-stu-id="42f81-159">Pool name for this pool, or the single server name if this is not a pool</span></span>
    
      - <span data-ttu-id="42f81-160">Server Name, dem das Zertifikat zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="42f81-160">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="42f81-161">Einfache URL-Einträge, in der Regel treffen und einwählen</span><span class="sxs-lookup"><span data-stu-id="42f81-161">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="42f81-162">Webdienste interne und Webdienste externe Namen (beispielsweise webpool01.contoso.net, webpool01.contoso.com), basierend auf den Optionen, die im Topologie-Generator und über berittenen Webdiensten ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="42f81-162">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="42f81-163">Wenn Sie bereits zugewiesen ist, wird die lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="42f81-163">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="42f81-164">und lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="42f81-164">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="42f81-165">Einträge.</span><span class="sxs-lookup"><span data-stu-id="42f81-165">records.</span></span>
    
    <span data-ttu-id="42f81-166">Das letzte Element ist das, was Sie am meisten interessieren, wenn es einen lyncdiscover-und lyncdiscoverinternal-San-Eintrag gibt.</span><span class="sxs-lookup"><span data-stu-id="42f81-166">The last item is what you are most interested in – if there is a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="42f81-167">Sobald Sie über diese Informationen verfügen, können Sie die Zertifikat Ansicht und die MMC schließen.</span><span class="sxs-lookup"><span data-stu-id="42f81-167">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="42f81-168">Wenn ein AutoErmittlungsdienst, also das lyncdiscover. \> Domänenname \> und lyncdiscoverinternal.\<domain name\></span><span class="sxs-lookup"><span data-stu-id="42f81-168">If an Autodiscover Service, meaning the lyncdiscover.\>domain name\> and lyncdiscoverinternal.\<domain name\></span></span> <span data-ttu-id="42f81-169">(auf der Grundlage, wenn es sich um ein externes oder internes Zertifikat handelt) der Betreff alternativer Name fehlt, und Sie verwenden ein einzelnes Standardzertifikat für die Typen Standard, WebServicesInternal und WebServiceExternal, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="42f81-169">(based on if this is an external or internal certificate) subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="42f81-170">Geben Sie an der Eingabeaufforderung der Befehlszeile der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-170">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="42f81-171">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-171">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="42f81-172">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-172">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="42f81-173">Wenn Sie den Parameter Domain Name verwenden, müssen Sie den FQDN für die lyncdiscoverinternal-und lyncdiscover-Datensätze definieren.</span><span class="sxs-lookup"><span data-stu-id="42f81-173">When you use the DomainName parameter, you must define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="42f81-174">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42f81-174">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="42f81-175">Um das Zertifikat zuzuweisen, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-175">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="42f81-176">Wobei "Daumenabdruck" der für das neu ausgestellte Zertifikat angezeigte Fingerabdruck ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-176">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="42f81-177">Gehen Sie wie folgt vor, wenn Sie bei Verwendung separater Zertifikate für Standard, WebServicesInternal und WebServicesExternal für einen fehlenden internen Auto Ermittlungs Betreff Alternative Namen verwenden:</span><span class="sxs-lookup"><span data-stu-id="42f81-177">For a missing internal Autodiscover subject alternative names when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="42f81-178">Geben Sie an der Eingabeaufforderung der Befehlszeile der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-178">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="42f81-179">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-179">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="42f81-180">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-180">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="42f81-181">Wenn Sie den Parameter Domain Name verwenden, müssen Sie ein entsprechendes Präfix für den FQDN der SIP-Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-181">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="42f81-182">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42f81-182">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="42f81-183">Geben Sie für einen fehlenden externen Auto Ermittlungs Betreff-alternativen Namen in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-183">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="42f81-184">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-184">If you have many SIP domains, you cannot use the new AllSipDomain parameter.</span></span> <span data-ttu-id="42f81-185">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-185">Instead, you must use DomainName parameter.</span></span> <span data-ttu-id="42f81-186">Wenn Sie den Parameter Domain Name verwenden, müssen Sie ein entsprechendes Präfix für den FQDN der SIP-Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="42f81-186">When you use the DomainName parameter, you must use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="42f81-187">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42f81-187">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="42f81-188">Wenn Sie die einzelnen Zertifikattypen zuweisen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="42f81-188">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="42f81-189">Wobei "Daumenabdruck" der für die neu ausgestellten einzelnen Zertifikate angezeigte Fingerabdruck ist.</span><span class="sxs-lookup"><span data-stu-id="42f81-189">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>

<span data-ttu-id="42f81-190"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="42f81-190"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

