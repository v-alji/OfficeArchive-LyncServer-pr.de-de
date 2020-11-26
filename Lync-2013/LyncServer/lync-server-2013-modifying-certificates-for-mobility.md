---
title: 'Lync Server 2013: Ändern der Zertifikate für Mobilität'
description: 'Lync Server 2013: Ändern von Zertifikaten für Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modifying certificates for mobility
ms:assetid: 4e9107af-20f4-4c2a-8c98-ca35b39a4e2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690015(v=OCS.15)
ms:contentKeyID: 48184120
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 099122b1773c3f15d8ae0034ee5fa404225cdfd2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445694"
---
# <a name="modifying-certificates-for-mobility-in-lync-server-2013"></a><span data-ttu-id="932b2-103">Ändern der Zertifikate für Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="932b2-103">Modifying certificates for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="932b2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="932b2-104">

<span> </span></span></span>

<span data-ttu-id="932b2-105">_**Letztes Änderungsdatum des Themas:** 2014-06-20_</span><span class="sxs-lookup"><span data-stu-id="932b2-105">_**Topic Last Modified:** 2014-06-20_</span></span>

<span data-ttu-id="932b2-106">Um sichere Verbindungen zwischen Ihrer lync-Umgebung und ihren mobilen Clients zu unterstützen, müssen die Secure Socket Layer (SSL)-Zertifikate für Ihren Director-Pool, den Front-End-Pool und den Reverse-Proxy mit einigen zusätzlichen Einträgen für den alternativen Subject-Name (alternativer Name) aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="932b2-106">To support secure connections between your Lync environment and your mobile clients, the Secure Socket Layer (SSL) certificates for your Director pool, Front End pool, and reverse proxy are going to need to be updated with some additional subject alternative name (SAN) entries.</span></span> <span data-ttu-id="932b2-107">Wenn Sie weitere Details zu den Zertifikatanforderungen für Mobilität lesen müssen, lesen Sie den Abschnitt Zertifikatanforderungen unter [Technische Anforderungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), aber im Grunde müssen Sie neue Zertifikate von der Zertifizierungsstelle mit den zusätzlichen San-Einträgen abrufen und diese Zertifikate dann mithilfe der Schritte dieses Artikels hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="932b2-107">If you need to check out more details about the certificate requirements for mobility, see the Certificate Requirements section in [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md), but basically you’ll need to get new certificates from the Certificate Authority with the additional SAN entries included, and then add those certificates using this article’s steps.</span></span>

<span data-ttu-id="932b2-108">Bevor Sie beginnen, ist es in der Regel ratsam, zu wissen, welche alternativen Namen ihre Zertifikate bereits haben.</span><span class="sxs-lookup"><span data-stu-id="932b2-108">Of course before you begin, it’s usually a good idea to know what subject alternative names your certificates already have.</span></span> <span data-ttu-id="932b2-109">Wenn Sie sich nicht sicher sind, was bereits konfiguriert wurde, gibt es viele Möglichkeiten, dies herauszufinden. Während die Option zum Ausführen der Befehle " **Get-CsCertificate** " und "andere PowerShell" zum Anzeigen dieser Informationen (die wir weiter unten durchlaufen) standardmäßig die Daten abgeschnitten werden, werden möglicherweise nicht alle benötigten Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="932b2-109">If you’re not sure what’s already been configured, there are a lot of ways to find out. While the option’s there to run the **Get-CsCertificate** and other PowerShell commands to view this information, (which we walk through below) by default that data will be truncated, so you may not get to see all the properties you need.</span></span> <span data-ttu-id="932b2-110">Um sich das Zertifikat und alle seine Eigenschaften genauer anzusehen, können Sie zur Microsoft Management Console (MMC) wechseln und das Zertifikat-Snap-In laden (das wir auch weiter unten durchlaufen), oder Sie können einfach den lync Server-Bereitstellungs-Assistenten einchecken.</span><span class="sxs-lookup"><span data-stu-id="932b2-110">In order to get a good look at the certificate and all its properties, you can go to the Microsoft Management Console (MMC) and load the Certificates snap-in (which we also walk through below), or you can just check in the Lync Server Deployment Wizard.</span></span>

<span data-ttu-id="932b2-111">Wie bereits erwähnt, führen Sie die folgenden Schritte durch die Aktualisierung der Zertifikate mithilfe der lync Server-Verwaltungsshell und der MMC.</span><span class="sxs-lookup"><span data-stu-id="932b2-111">As noted above, the following steps will walk you through updating the certificates using the Lync Server Management Shell and the MMC.</span></span> <span data-ttu-id="932b2-112">Wenn Sie stattdessen den Zertifikat-Assistenten im lync Server-Bereitstellungs-Assistenten für diesen Zweck verwenden möchten, können Sie für den Director-oder Director-Pool die [Konfiguration von Zertifikaten für den Director in lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md) überprüfen, wenn Sie einen konfiguriert haben (Dies ist möglicherweise nicht der Fall).</span><span class="sxs-lookup"><span data-stu-id="932b2-112">If you’re interested in using the Certificate Wizard in the Lync Server Deployment Wizard for this instead, you can check [Configure certificates for the Director in Lync Server 2013](lync-server-2013-configure-certificates-for-the-director.md) out for the Director or Director pool, if you configured one (you may not have).</span></span> <span data-ttu-id="932b2-113">Für den Front-End-Server oder den Front-End-Pool empfiehlt es sich, [Zertifikate für Server in lync Server 2013 zu konfigurieren](lync-server-2013-configure-certificates-for-servers.md).</span><span class="sxs-lookup"><span data-stu-id="932b2-113">For the Front End Server or Front End pool, you’ll want to see [Configure certificates for servers in Lync Server 2013](lync-server-2013-configure-certificates-for-servers.md).</span></span>

<span data-ttu-id="932b2-114">Als letztes sollten Sie Bedenken, dass Sie möglicherweise über ein einzelnes Standardzertifikat in ihrer lync Server 2013-Umgebung verfügen, oder dass Sie möglicherweise getrennte Zertifikate für den Standardwert (alles andere als die Webdienste), WebServicesExternal und WebServicesInternal.</span><span class="sxs-lookup"><span data-stu-id="932b2-114">One last thing to keep in mind is that you may have a single Default certificate in your Lync Server 2013 environment, or you may have separate certificates for Default (which is everything but the web services), WebServicesExternal and WebServicesInternal.</span></span> <span data-ttu-id="932b2-115">Was auch immer Ihre Konfiguration ist, diese Schritte sollten Ihnen helfen.</span><span class="sxs-lookup"><span data-stu-id="932b2-115">Whatever your configuration, these steps should help you out.</span></span>

<div>

## <a name="to-update-certificates-with-new-subject-alternative-names-using-the-lync-server-management-shell"></a><span data-ttu-id="932b2-116">So aktualisieren Sie Zertifikate mit neuen alternativen Subjektnamen mithilfe der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="932b2-116">To update certificates with new subject alternative names using the Lync Server Management Shell</span></span>

1.  <span data-ttu-id="932b2-117">Sie müssen sich bei Ihrem lync Server 2013-Server mit einem Konto anmelden, das über lokale Administratorrechte und-Berechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="932b2-117">You need to log on to your Lync Server 2013 server using an account that has local administrator rights and permissions.</span></span> <span data-ttu-id="932b2-118">Wenn Sie die PowerShell **-Anforderungs-CsCertificate** in Schritten 12 und darüber hinaus ausführen, muss das Konto darüber hinaus über Rechte für die angegebene Zertifizierungsstelle (Certification Authority, ca) verfügen.</span><span class="sxs-lookup"><span data-stu-id="932b2-118">Additionally, if you’re running the PowerShell **Request-CsCertificate** in Steps 12 and beyond, the account needs to have rights to the specified Certificate Authority (CA).</span></span>

2.  <span data-ttu-id="932b2-119">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="932b2-119">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="932b2-120">Bevor Sie ein aktualisiertes Zertifikat zuweisen können, müssen Sie herausfinden, welche Zertifikate dem Server zugewiesen wurden und für welche Art von Verwendung.</span><span class="sxs-lookup"><span data-stu-id="932b2-120">Before you can assign an updated certificate, you’ll need to find out what certificates have been assigned to the server and for which type of use.</span></span> <span data-ttu-id="932b2-121">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-121">At the command line, type:</span></span>
    
        Get-CsCertificate

4.  <span data-ttu-id="932b2-122">Überprüfen Sie die Ausgabe des vorherigen Schritts, um festzustellen, ob ein einzelnes Zertifikat für mehrere Zwecke zugewiesen wurde oder ob für jede Verwendung ein anderes Zertifikat zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="932b2-122">Review the output from the previous step to see whether a single certificate has been assigned for multiple uses, or whether a different certificate is assigned for each use.</span></span> <span data-ttu-id="932b2-123">Schauen Sie sich den use-Parameter an, um zu erfahren, wie ein Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="932b2-123">Look in the Use parameter to find out how a certificate’s being used.</span></span> <span data-ttu-id="932b2-124">Vergleichen Sie den Parameter Fingerabdruck für die angezeigten Zertifikate, um festzustellen, ob dasselbe Zertifikat mehrere Verwendungszwecke aufweist.</span><span class="sxs-lookup"><span data-stu-id="932b2-124">Compare the Thumbprint parameter for the displayed certificates to see if the same certificate has multiple uses.</span></span> <span data-ttu-id="932b2-125">Behalten Sie den Parameter Fingerabdruck im Auge.</span><span class="sxs-lookup"><span data-stu-id="932b2-125">Keep your eye on the Thumbprint parameter.</span></span>

5.  <span data-ttu-id="932b2-126">Aktualisieren Sie das Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="932b2-126">Update the certificate.</span></span> <span data-ttu-id="932b2-127">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-127">At the command line, type:</span></span>
    
        Set-CsCertificate -Type <type of certificate as displayed in the Use parameter> -Thumbprint <unique identifier>
    
    <span data-ttu-id="932b2-128">Wenn beispielsweise das Cmdlet " **Get-CsCertificate** " ein Zertifikat mit der Verwendung von Default, einem anderen mit einer Verwendung von WebServicesInternal und einem anderen mit einer Verwendung von WebServicesExternal angezeigt hat und alle denselben Fingerabdruckwert hatten, sollten Sie in der Befehlszeile Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="932b2-128">For example, if the **Get-CsCertificate** cmdlet displayed a certificate with Use of Default, another with a Use of WebServicesInternal, and another with a Use of WebServicesExternal, and they all had the same Thumbprint value, at the command line, you should type:</span></span>
    
        Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
    
    <span data-ttu-id="932b2-129">**Wichtig:**</span><span class="sxs-lookup"><span data-stu-id="932b2-129">**Important:**</span></span>
    
    <span data-ttu-id="932b2-130">Wenn für jede Verwendung ein separates Zertifikat zugewiesen wird (damit der von Ihnen geprüfte Fingerabdruckwert für jedes Zertifikat anders ist), ist es wichtig, dass Sie das Cmdlet " **CsCertificate** " **nicht** mit mehreren Typen ausführen, wie im obigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="932b2-130">If a separate certificate is assigned for each use (so the Thumbprint value you checked above is different for each certificate), it’s vital that you **don’t** run the **Set-CsCertificate** cmdlet with multiple types, as in the example above.</span></span> <span data-ttu-id="932b2-131">Führen Sie in diesem Fall das Cmdlet " **Satz-CsCertificate** " für jede Verwendung separat aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-131">In this case, run the **Set-CsCertificate** cmdlet separately for each use.</span></span> <span data-ttu-id="932b2-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="932b2-132">For example:</span></span>
    
        Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
        Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>

6.  <span data-ttu-id="932b2-133">Klicken Sie zum Anzeigen des Zertifikats (oder der Zertifikate) auf **Start**, klicken Sie auf **ausführen.**...</span><span class="sxs-lookup"><span data-stu-id="932b2-133">To view the certificate (or certificates), click **Start**, click **Run…**.</span></span> <span data-ttu-id="932b2-134">Geben Sie MMC ein, um die Microsoft Management Console zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="932b2-134">Type MMC to open the Microsoft Management Console.</span></span>

7.  <span data-ttu-id="932b2-135">Wählen Sie im MMC-Menü **Datei** aus, wählen Sie **Snap-in hinzufügen/entfernen** aus, und wählen Sie Zertifikate aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-135">From the MMC menu, select **File**, select **Add/Remove snap-in…**, select Certificates.</span></span> <span data-ttu-id="932b2-136">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="932b2-136">Click **Add**.</span></span> <span data-ttu-id="932b2-137">Wenn Sie dazu aufgefordert werden, wählen Sie **Computer Konto** aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="932b2-137">When prompted, select **Computer account**, then click **Next**.</span></span>

8.  <span data-ttu-id="932b2-138">Wenn es sich um den Server handelt, auf dem sich das Zertifikat befindet, wählen Sie **lokaler Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-138">If this is the server where the certificate’s located, select **Local computer**.</span></span> <span data-ttu-id="932b2-139">Wenn sich das Zertifikat auf einem anderen Computer befindet, sollten Sie **einen anderen Computer** auswählen, und dann können Sie entweder den vollqualifizierten Domänennamen des Computers eingeben, oder Sie klicken auf **Durchsuchen** **Geben Sie den zu wählenden Objektnamen** ein, und geben Sie den Namen des Computers ein.</span><span class="sxs-lookup"><span data-stu-id="932b2-139">If the certificate’s located on another computer, you should select **Another computer**, and then you can either type in the fully qualified domain name of the computer, or click **Browse** in **Enter the object name to select**, and type the name of the computer.</span></span> <span data-ttu-id="932b2-140">Klicken Sie auf **Namen überprüfen**.</span><span class="sxs-lookup"><span data-stu-id="932b2-140">Click **Check Names**.</span></span> <span data-ttu-id="932b2-141">Wenn der Name des Computers aufgelöst wird, wird er unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="932b2-141">When the name of the computer resolves, it’ll be underlined.</span></span> <span data-ttu-id="932b2-142">Klicken Sie auf **OK** und dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="932b2-142">Click **OK**, then click **Finish**.</span></span> <span data-ttu-id="932b2-143">Klicken Sie auf **OK** , um die Auswahl zu bestätigen, und schließen Sie das Dialogfeld **Snap-Ins hinzufügen oder entfernen** .</span><span class="sxs-lookup"><span data-stu-id="932b2-143">Click **OK** to commit the selection and close the **Add or Remove Snap-ins** dialog.</span></span>

9.  <span data-ttu-id="932b2-144">Wenn Sie die Eigenschaften des Zertifikats anzeigen möchten, erweitern Sie **Zertifikate**, erweitern Sie **Personal**, und wählen Sie **Zertifikate** aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-144">To view the properties of the certificate, expand **Certificates**, expand **Personal**, and select **Certificates**.</span></span> <span data-ttu-id="932b2-145">Wählen Sie das Zertifikat aus, das Sie anzeigen möchten, klicken Sie mit der rechten Maustaste auf das Zertifikat, und wählen Sie **Öffnen** aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-145">Select the certificate to view, right-click on the certificate and select **Open**.</span></span>

10. <span data-ttu-id="932b2-146">Wählen Sie in der **Zertifikat** Ansicht **Details** aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-146">In the **Certificate** view, select **Details**.</span></span> <span data-ttu-id="932b2-147">Hier können Sie den Namen des Zertifikat Antragstellers auswählen, indem Sie **Betreff** auswählen und der zugewiesene Antragstellername und die zugehörigen Eigenschaften angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="932b2-147">From here, you can select the certificate subject name by selecting **Subject** and the assigned subject name and associated properties are displayed.</span></span>

11. <span data-ttu-id="932b2-148">Wenn Sie die alternativen Namen des zugewiesenen betreffs anzeigen möchten, wählen Sie **alternativer Betreffname** aus.</span><span class="sxs-lookup"><span data-stu-id="932b2-148">To view the assigned subject alternative names, select **Subject Alternative Name**.</span></span> <span data-ttu-id="932b2-149">Hier werden alle zugewiesenen Subjekt alternativen Namen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="932b2-149">All assigned subject alternative names are displayed here.</span></span> <span data-ttu-id="932b2-150">Die hier gefundenen Alternativen Betreff-Namen sind standardmäßig vom Typ **DNS-Name** .</span><span class="sxs-lookup"><span data-stu-id="932b2-150">The subject alternative names found here are of type **DNS Name** by default.</span></span> <span data-ttu-id="932b2-151">Die folgenden Member sollten angezeigt werden (alle sollten vollqualifizierte Domänennamen sein, die in DNS-Hosteinträgen (A oder, wenn IPv6 AAAA) dargestellt werden:</span><span class="sxs-lookup"><span data-stu-id="932b2-151">You should see the following members (all of which should be fully qualified domain names as represented in DNS host (A or, if IPv6 AAAA) records:</span></span>
    
      - <span data-ttu-id="932b2-152">Poolname für diesen Pool oder der Name des einzelnen Servers, wenn es sich nicht um einen Pool handelt</span><span class="sxs-lookup"><span data-stu-id="932b2-152">Pool name for this pool, or the single server name if this isn’t a pool</span></span>
    
      - <span data-ttu-id="932b2-153">Server Name, dem das Zertifikat zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="932b2-153">Server name that the certificate is assigned to</span></span>
    
      - <span data-ttu-id="932b2-154">Einfache URL-Einträge, in der Regel treffen und einwählen</span><span class="sxs-lookup"><span data-stu-id="932b2-154">Simple URL records, typically meet and dialin</span></span>
    
      - <span data-ttu-id="932b2-155">Webdienste interne und Webdienste externe Namen (beispielsweise webpool01.contoso.net, webpool01.contoso.com), basierend auf den Optionen, die im Topologie-Generator und über berittenen Webdiensten ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="932b2-155">Web services internal and Web services external names (for example, webpool01.contoso.net, webpool01.contoso.com), based on choices made in Topology Builder and over-ridden web services selections.</span></span>
    
      - <span data-ttu-id="932b2-156">Wenn Sie bereits zugewiesen ist, wird die lyncdiscover.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="932b2-156">If already assigned, the lyncdiscover.\<sipdomain\></span></span> <span data-ttu-id="932b2-157">und lyncdiscoverinternal.\<sipdomain\></span><span class="sxs-lookup"><span data-stu-id="932b2-157">and lyncdiscoverinternal.\<sipdomain\></span></span> <span data-ttu-id="932b2-158">Einträge.</span><span class="sxs-lookup"><span data-stu-id="932b2-158">records.</span></span>
    
    <span data-ttu-id="932b2-159">Das letzte Element ist das, was Sie am meisten interessieren – wenn ein lyncdiscover-und lyncdiscoverinternal-San-Eintrag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="932b2-159">The last item is what you’re most interested in – if there’s a lyncdiscover and lyncdiscoverinternal SAN entry.</span></span>
    
    <span data-ttu-id="932b2-160">Wiederholen Sie diese Schritte, wenn Sie über mehrere zu überprüfende Zertifikate verfügen.</span><span class="sxs-lookup"><span data-stu-id="932b2-160">Repeat these steps if you have multiple certificates to check.</span></span> <span data-ttu-id="932b2-161">Sobald Sie über diese Informationen verfügen, können Sie die Zertifikat Ansicht und die MMC schließen.</span><span class="sxs-lookup"><span data-stu-id="932b2-161">Once you have this information, you can close the certificate view and the MMC.</span></span>

12. <span data-ttu-id="932b2-162">Gehen Sie wie folgt vor, wenn der Alternative Name des AutoErmittlungsdiensts nicht vorhanden ist und Sie ein einzelnes Standardzertifikat für die Typen Standard, WebServicesInternal und WebServiceExternal verwenden:</span><span class="sxs-lookup"><span data-stu-id="932b2-162">If an Autodiscover Service subject alternative name is missing, and you are using a single Default certificate for the Default, WebServicesInternal and WebServiceExternal types, do the following:</span></span>
    
      - <span data-ttu-id="932b2-163">Geben Sie an der Eingabeaufforderung der Befehlszeile der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-163">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="932b2-164">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-164">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="932b2-165">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-165">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="932b2-166">Wenn Sie den Parameter Domain Name verwenden, müssen Sie den FQDN für die lyncdiscoverinternal-und lyncdiscover-Datensätze definieren.</span><span class="sxs-lookup"><span data-stu-id="932b2-166">When you use the DomainName parameter, you’ve got to define the FQDN for the lyncdiscoverinternal and lyncdiscover records.</span></span> <span data-ttu-id="932b2-167">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="932b2-167">For example:</span></span>
        
            Request-CsCertificate -New -Type Default,WebServicesInternal,WebServicesExternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="932b2-168">Um das Zertifikat zuzuweisen, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-168">To assign the certificate, type the following:</span></span>
        
            Set-CsCertificate -Type Default,WebServicesInternal,WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="932b2-169">Wobei "Daumenabdruck" der für das neu ausgestellte Zertifikat angezeigte Fingerabdruck ist.</span><span class="sxs-lookup"><span data-stu-id="932b2-169">Where “Thumbprint” is the thumbprint displayed for the newly issued certificate.</span></span>

13. <span data-ttu-id="932b2-170">Gehen Sie bei einem fehlenden internen autodiscover-San bei Verwendung separater Zertifikate für Standard, WebServicesInternal und WebServicesExternal wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="932b2-170">For a missing internal Autodiscover SAN when using separate certificates for Default, WebServicesInternal, and WebServicesExternal, do the following:</span></span>
    
      - <span data-ttu-id="932b2-171">Geben Sie an der Eingabeaufforderung der Befehlszeile der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-171">At the Lync Server Management Shell command line prompt, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="932b2-172">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-172">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="932b2-173">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-173">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="932b2-174">Wenn Sie den Parameter Domain Name verwenden, müssen Sie ein entsprechendes Präfix für den FQDN der SIP-Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-174">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="932b2-175">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="932b2-175">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesInternal -Ca dc\myca -DomainName "LyncdiscoverInternal.contoso.com, LyncdiscoverInternal.contoso.net" -verbose
    
      - <span data-ttu-id="932b2-176">Geben Sie für einen fehlenden externen Auto Ermittlungs Betreff-alternativen Namen in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-176">For a missing external Autodiscover subject alternative name, at the command line, type:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -AllSipDomain -verbose
        
        <span data-ttu-id="932b2-177">Wenn Sie über viele SIP-Domänen verfügen, können Sie den neuen AllSipDomain-Parameter nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-177">If you have many SIP domains, you can’t use the new AllSipDomain parameter.</span></span> <span data-ttu-id="932b2-178">Stattdessen müssen Sie den Domain Name-Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-178">Instead, you need to use the DomainName parameter.</span></span> <span data-ttu-id="932b2-179">Wenn Sie den Parameter Domain Name verwenden, müssen Sie ein entsprechendes Präfix für den FQDN der SIP-Domäne verwenden.</span><span class="sxs-lookup"><span data-stu-id="932b2-179">When you use the DomainName parameter, you’ve got to use an appropriate prefix for the SIP domain FQDN.</span></span> <span data-ttu-id="932b2-180">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="932b2-180">For example:</span></span>
        
            Request-CsCertificate -New -Type WebServicesExternal -Ca dc\myca -DomainName "Lyncdiscover.contoso.com, Lyncdiscover.contoso.net" -verbose
    
      - <span data-ttu-id="932b2-181">Wenn Sie die einzelnen Zertifikattypen zuweisen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="932b2-181">To assign the individual certificate types, type the following:</span></span>
        
            Set-CsCertificate -Type Default -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesInternal -Thumbprint <Certificate Thumbprint>
            Set-CsCertificate -Type WebServicesExternal -Thumbprint <Certificate Thumbprint>
        
        <span data-ttu-id="932b2-182">Wobei "Daumenabdruck" der für die neu ausgestellten einzelnen Zertifikate angezeigte Fingerabdruck ist.</span><span class="sxs-lookup"><span data-stu-id="932b2-182">Where “Thumbprint” is the thumbprint displayed for the newly issued individual certificates.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="932b2-183">Einfach zu beachten: die Schritte 12 und 13 sollten nur ausgeführt werden, wenn das Konto, auf dem Sie ausgeführt wird, Zugriff auf die Zertifizierungsstelle mit den entsprechenden Berechtigungen hat.</span><span class="sxs-lookup"><span data-stu-id="932b2-183">Just to note, Steps 12 and 13 should be run only if the account running them has access to the Certificate Authority with appropriate permissions.</span></span> <span data-ttu-id="932b2-184">Wenn Sie sich nicht mit einem Konto anmelden können, das diese Berechtigungen hat, oder wenn Sie eine öffentliche oder Remote-Zertifizierungsstelle für Ihre Zertifikate verwenden, müssen Sie diese über den lync Server-Bereitstellungs-Assistenten anfordern, der am Anfang des Artikels berührt wurde.</span><span class="sxs-lookup"><span data-stu-id="932b2-184">If you are unable to log in with an account that’s got those permissions, or if you’re using a public or remote Certificate Authority for your certificates, you would need to request them through the Lync Server Deployment Wizard, which was touched on at the top of the article.</span></span>

    
    <span data-ttu-id="932b2-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="932b2-185"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

