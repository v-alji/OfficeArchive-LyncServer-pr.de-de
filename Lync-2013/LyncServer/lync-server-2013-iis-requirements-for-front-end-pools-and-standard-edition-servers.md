---
title: IIS-Anforderungen für Front-End-Pools und Standard Edition-Server
description: IIS-Anforderungen für Front-End-Pools und Standard Edition-Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IIS requirements for Front End pools and Standard Edition servers
ms:assetid: e8a6c7ac-b6d5-4c7e-abe9-d8ea5eedbc62
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399038(v=OCS.15)
ms:contentKeyID: 48185888
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f56452c7e47352333ac3ac5a51d649b0828a0ff9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427425"
---
# <a name="iis-requirements-for-front-end-pools-and-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="b87d1-103">IIS-Anforderungen für Front-End-Pools und Standard Edition-Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b87d1-103">IIS requirements for Front End pools and Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b87d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b87d1-104">

<span> </span></span></span>

<span data-ttu-id="b87d1-105">_**Letztes Änderungsdatum des Themas:** 2012-06-19_</span><span class="sxs-lookup"><span data-stu-id="b87d1-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="b87d1-106">Bei Standard Edition-Servern und-Front-End-Servern sowie Directors erstellt das lync Server 2013-Installationsprogramm virtuelle Verzeichnisse in Internet Informationsdienste (IIS) für die folgenden Zwecke:</span><span class="sxs-lookup"><span data-stu-id="b87d1-106">For Standard Edition servers and Front End Servers, and Directors, the Lync Server 2013 installer creates virtual directories in Internet Information Services (IIS) for the following purposes:</span></span>

  - <span data-ttu-id="b87d1-107">So aktivieren Sie Benutzer zum Herunterladen von Dateien aus dem Adressbuchdienst</span><span class="sxs-lookup"><span data-stu-id="b87d1-107">To enable users to download files from the Address Book Service</span></span>

  - <span data-ttu-id="b87d1-108">So aktivieren Sie Clients zum Abrufen von Updates</span><span class="sxs-lookup"><span data-stu-id="b87d1-108">To enable clients to obtain updates</span></span>

  - <span data-ttu-id="b87d1-109">So aktivieren Sie Konferenzen</span><span class="sxs-lookup"><span data-stu-id="b87d1-109">To enable conferencing</span></span>

  - <span data-ttu-id="b87d1-110">So aktivieren Sie Benutzer zum Herunterladen von Besprechungsinhalten</span><span class="sxs-lookup"><span data-stu-id="b87d1-110">To enable users to download meeting content</span></span>

  - <span data-ttu-id="b87d1-111">So aktivieren Sie Benutzer zum Erweitern von Verteilergruppen</span><span class="sxs-lookup"><span data-stu-id="b87d1-111">To enable users to expand distribution groups</span></span>

  - <span data-ttu-id="b87d1-112">So aktivieren Sie Telefonkonferenzen</span><span class="sxs-lookup"><span data-stu-id="b87d1-112">To enable phone conferencing</span></span>

  - <span data-ttu-id="b87d1-113">So aktivieren Sie die Features der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="b87d1-113">To enable response group features</span></span>

<span data-ttu-id="b87d1-114">Darüber hinaus erstellt das kumulative Update für lync Server 2010: November 2011-Installationsprogramm virtuelle Verzeichnisse in IIS für die folgenden Zwecke:</span><span class="sxs-lookup"><span data-stu-id="b87d1-114">In addition, the cumulative update for Lync Server 2010: November 2011 installer creates virtual directories in IIS for the following purposes:</span></span>

  - <span data-ttu-id="b87d1-115">Auf Front-End-Servern oder Standard Edition-Servern zur Unterstützung von Mobilitätsfunktionen wie Instant Messaging (im) und Anwesenheit auf mobilen Geräten</span><span class="sxs-lookup"><span data-stu-id="b87d1-115">On Front End Servers or Standard Edition servers to support mobility functionality, such as instant messaging (IM) and presence, on mobile devices</span></span>

  - <span data-ttu-id="b87d1-116">Auf Front-End-Servern oder Standard Edition-Servern und auf Directors, damit Mobile Geräte mobilitätsressourcen automatisch entdecken können</span><span class="sxs-lookup"><span data-stu-id="b87d1-116">On Front End Servers or Standard Edition servers and on Directors to enable mobile devices to automatically discover mobility resources</span></span>



> [!NOTE]
> <span data-ttu-id="b87d1-117">Wenn Sie Mobilität bereitstellen, empfehlen wir, IIS 7,5 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b87d1-117">If you are deploying mobility, we recommend that you use IIS 7.5.</span></span> <span data-ttu-id="b87d1-118">Das lync Server Mobility Service-Installationsprogramm legt einige ASP.net-Flags fest, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="b87d1-118">The Lync Server Mobility Service installer sets some ASP.NET flags to improve performance.</span></span> <span data-ttu-id="b87d1-119">IIS 7,5 wird standardmäßig unter Windows Server 2008 R2 installiert, und das Mobilitätsdienst-Installationsprogramm ändert automatisch die ASP.NET-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b87d1-119">IIS 7.5 is installed by default on Windows Server 2008 R2, and the Mobility Service installer automatically changes the ASP.NET settings.</span></span> <span data-ttu-id="b87d1-120">Wenn Sie IIS 7,0 unter Windows Server 2008 verwenden, müssen Sie diese Einstellungen manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="b87d1-120">If you use IIS 7.0 on Windows Server 2008, you need to manually change these settings.</span></span>



<span data-ttu-id="b87d1-121">Für lync Server müssen die folgenden IIS-Module installiert werden:</span><span class="sxs-lookup"><span data-stu-id="b87d1-121">Lync Server requires the following IIS modules to be installed:</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b87d1-122">Wenn Ihre Organisation erfordert, dass Sie IIS und alle Webdienste auf einem anderen Laufwerk als dem Systemlaufwerk finden, können Sie den Pfad für den Installationspfad für die lync Server-Dateien im Dialogfeld einrichten ändern.</span><span class="sxs-lookup"><span data-stu-id="b87d1-122">If your organization requires that you locate IIS and all Web Services on a drive other than the system drive, you can change the installation location path for the Lync Server files in the Setup dialog box.</span></span> <span data-ttu-id="b87d1-123">Wenn Sie die Setup Dateien in diesem Pfad installieren, einschließlich OCSCore.msi, werden die restlichen lync Server-Dateien ebenfalls auf diesem Laufwerk bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b87d1-123">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server files will be deployed to this drive as well.</span></span> <span data-ttu-id="b87d1-124">Ausführliche Informationen dazu, wie Sie die INETPUB, die vom Windows Server-Manager bereitgestellt werden, bei der Installation von IIS verschieben, finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A> .</span><span class="sxs-lookup"><span data-stu-id="b87d1-124">For details about how to relocate the INETPUB deployed by Windows Server Manager when installing IIS, see <A href="https://go.microsoft.com/fwlink/p/?linkid=216888">https://go.microsoft.com/fwlink/p/?linkId=216888</A>.</span></span>


  - <span data-ttu-id="b87d1-125">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="b87d1-125">Static Content</span></span>

  - <span data-ttu-id="b87d1-126">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="b87d1-126">Default Document</span></span>

  - <span data-ttu-id="b87d1-127">HTTP-Fehler</span><span class="sxs-lookup"><span data-stu-id="b87d1-127">HTTP Errors</span></span>

  - <span data-ttu-id="b87d1-128">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="b87d1-128">ASP.NET</span></span>

  - <span data-ttu-id="b87d1-129">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="b87d1-129">.NET Extensibility</span></span>

  - <span data-ttu-id="b87d1-130">ISAPI-Erweiterungen (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="b87d1-130">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="b87d1-131">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="b87d1-131">ISAPI Filters</span></span>

  - <span data-ttu-id="b87d1-132">HTTP-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="b87d1-132">HTTP Logging</span></span>

  - <span data-ttu-id="b87d1-133">Protokollierungstools</span><span class="sxs-lookup"><span data-stu-id="b87d1-133">Logging Tools</span></span>

  - <span data-ttu-id="b87d1-134">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="b87d1-134">Tracing</span></span>

  - <span data-ttu-id="b87d1-135">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b87d1-135">Windows Authentication</span></span>

  - <span data-ttu-id="b87d1-136">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="b87d1-136">Request Filtering</span></span>

  - <span data-ttu-id="b87d1-137">Komprimierung statischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="b87d1-137">Static Content Compression</span></span>

  - <span data-ttu-id="b87d1-138">Komprimierung dynamischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="b87d1-138">Dynamic Content Compression</span></span>

  - <span data-ttu-id="b87d1-139">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="b87d1-139">IIS Management Console</span></span>

  - <span data-ttu-id="b87d1-140">IIS-Verwaltungsskripts und -tools</span><span class="sxs-lookup"><span data-stu-id="b87d1-140">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="b87d1-141">Anonyme Authentifizierung (standardmäßig installiert, wenn IIS installiert ist)</span><span class="sxs-lookup"><span data-stu-id="b87d1-141">Anonymous Authentication (installed by default when IIS is installed)</span></span>

  - <span data-ttu-id="b87d1-142">Clientzertifikatzuordnungs-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="b87d1-142">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="b87d1-143">In der folgenden Tabelle sind die URIs für die virtuellen Verzeichnisse für den internen Zugriff und die Dateisystemressourcen aufgelistet, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="b87d1-143">The following table lists the URIs for the virtual directories for internal access and the file system resources to which they refer.</span></span>

### <a name="virtual-directories-for-internal-access"></a><span data-ttu-id="b87d1-144">Virtuelle Verzeichnisse für den internen Zugriff</span><span class="sxs-lookup"><span data-stu-id="b87d1-144">Virtual Directories for Internal Access</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b87d1-145">Feature</span><span class="sxs-lookup"><span data-stu-id="b87d1-145">Feature</span></span></th>
<th><span data-ttu-id="b87d1-146">URI für virtuelles Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="b87d1-146">Virtual directory URI</span></span></th>
<th><span data-ttu-id="b87d1-147">Bezieht sich auf</span><span class="sxs-lookup"><span data-stu-id="b87d1-147">Refers to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-148">Adressbuchserver</span><span class="sxs-lookup"><span data-stu-id="b87d1-148">Address Book Server</span></span></p></td>
<td><p><span data-ttu-id="b87d1-149"> https:// &lt; Interner FQDN- &gt; /ABS/int/Handler</span><span class="sxs-lookup"><span data-stu-id="b87d1-149">https://&lt;Internal FQDN&gt;/ABS/int/Handler</span></span></p></td>
<td><p><span data-ttu-id="b87d1-150">Speicherort der Adressbuch Server-Downloaddateien für interne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b87d1-150">Location of Address Book Server download files for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b87d1-151">AutoErmittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b87d1-151">Autodiscover Service</span></span></p></td>
<td><p><span data-ttu-id="b87d1-152"> https:// &lt; Interner FQDN- &gt; /autodiscover</span><span class="sxs-lookup"><span data-stu-id="b87d1-152">https://&lt;Internal FQDN&gt;/Autodiscover</span></span></p></td>
<td><p><span data-ttu-id="b87d1-153">Der Speicherort des lync Server-AutoErmittlungsdiensts, der mobilitätsressourcen für interne Benutzer von mobilen Geräten findet.</span><span class="sxs-lookup"><span data-stu-id="b87d1-153">Location of the Lync Server Autodiscover Service that locates mobility resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-154">Clientupdates</span><span class="sxs-lookup"><span data-stu-id="b87d1-154">Client updates</span></span></p></td>
<td><p><span data-ttu-id="b87d1-155"> http:// &lt; Interner FQDN- &gt; /AutoUpdate/int</span><span class="sxs-lookup"><span data-stu-id="b87d1-155">http://&lt;Internal FQDN&gt;/AutoUpdate/Int</span></span></p></td>
<td><p><span data-ttu-id="b87d1-156">Speicherort der Updatedateien für interne computerbasierte Clients.</span><span class="sxs-lookup"><span data-stu-id="b87d1-156">Location of update files for internal computer-based clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b87d1-157">Conf</span><span class="sxs-lookup"><span data-stu-id="b87d1-157">Conf</span></span></p></td>
<td><p><span data-ttu-id="b87d1-158"> http:// &lt; Interner FQDN- &gt; /conf/int</span><span class="sxs-lookup"><span data-stu-id="b87d1-158">http://&lt;Internal FQDN&gt;/Conf/Int</span></span></p></td>
<td><p><span data-ttu-id="b87d1-159">Der Speicherort der Konferenzressourcen für interne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b87d1-159">Location of conferencing resources for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-160">Geräte Updates</span><span class="sxs-lookup"><span data-stu-id="b87d1-160">Device updates</span></span></p></td>
<td><p><span data-ttu-id="b87d1-161"> http:// &lt; Interner FQDN &gt; /DeviceUpdateFiles_Int</span><span class="sxs-lookup"><span data-stu-id="b87d1-161">http://&lt;Internal FQDN&gt;/DeviceUpdateFiles_Int</span></span></p></td>
<td><p><span data-ttu-id="b87d1-162">Speicherort der Unified Communications (UC)-Geräteaktualisierungsdateien für interne UC-Geräte.</span><span class="sxs-lookup"><span data-stu-id="b87d1-162">Location of unified communications (UC) device update files for internal UC devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b87d1-163">Besprechung</span><span class="sxs-lookup"><span data-stu-id="b87d1-163">Meeting</span></span></p></td>
<td><p><span data-ttu-id="b87d1-164"> http:// &lt; Interner FQDN- &gt; /etc/Place/NULL</span><span class="sxs-lookup"><span data-stu-id="b87d1-164">http://&lt;Internal FQDN&gt;/etc/place/null</span></span></p></td>
<td><p><span data-ttu-id="b87d1-165">Ort des Besprechungsinhalts für interne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b87d1-165">Location of meeting content for internal users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-166">Mobilitätsdienst</span><span class="sxs-lookup"><span data-stu-id="b87d1-166">Mobility Service</span></span></p></td>
<td><p><span data-ttu-id="b87d1-167"> https:// &lt; Interner FQDN- &gt; /MCX</span><span class="sxs-lookup"><span data-stu-id="b87d1-167">https://&lt;Internal FQDN&gt;/Mcx</span></span></p></td>
<td><p><span data-ttu-id="b87d1-168">Speicherort der Mobilitätsdienst Ressourcen für Benutzer interner mobiler Geräte.</span><span class="sxs-lookup"><span data-stu-id="b87d1-168">Location of Mobility Service resources for internal mobile device users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b87d1-169">Gruppenerweiterung und Adressbuch-Webabfrage Dienst</span><span class="sxs-lookup"><span data-stu-id="b87d1-169">Group Expansion and Address Book Web Query service</span></span></p></td>
<td><p><span data-ttu-id="b87d1-170"> http:// &lt; Interner FQDN- &gt; /GroupExpansion/int/Service.asmx</span><span class="sxs-lookup"><span data-stu-id="b87d1-170">http://&lt;Internal FQDN&gt;/GroupExpansion/int/service.asmx</span></span></p></td>
<td><p><span data-ttu-id="b87d1-171">Der Speicherort des Webdiensts, der die Gruppenerweiterung für interne Benutzer ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b87d1-171">Location of the Web service that enables group expansion for internal users.</span></span> <span data-ttu-id="b87d1-172">Außerdem wird der Speicherort des Adressbuch-Webabfrage Diensts bereitgestellt, der den internen lync Mobile Microsoft lync 2010 Mobile-Clients globale Adresslisteninformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b87d1-172">Also, the location of the Address Book Web Query service that provides global address list information to internal Lync Mobile Microsoft Lync 2010 Mobile clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-173">Telefonkonferenzen</span><span class="sxs-lookup"><span data-stu-id="b87d1-173">Phone Conferencing</span></span></p></td>
<td><p><span data-ttu-id="b87d1-174"> http:// &lt; Interner FQDN- &gt; /PhoneConferencing/int</span><span class="sxs-lookup"><span data-stu-id="b87d1-174">http://&lt;Internal FQDN&gt;/PhoneConferencing/Int</span></span></p></td>
<td><p><span data-ttu-id="b87d1-175">Standort von Telefonkonferenz Daten für interne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b87d1-175">Location of phone conferencing data for internal users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b87d1-176">Geräte Updates</span><span class="sxs-lookup"><span data-stu-id="b87d1-176">Device updates</span></span></p></td>
<td><p><span data-ttu-id="b87d1-177"> http:// &lt; Interner FQDN- &gt; /RequestHandler</span><span class="sxs-lookup"><span data-stu-id="b87d1-177">http://&lt;Internal FQDN&gt;/RequestHandler</span></span></p></td>
<td><p><span data-ttu-id="b87d1-178">Der Speicherort des Webdienst Anforderungshandlers für den Geräteaktualisierungsdienst, der es internen UC-Geräten ermöglicht, Protokolle hochzuladen und auf Updates zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b87d1-178">Location of the Device Update Web service Request Handler that enables internal UC devices to upload logs and check for updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b87d1-179">Reaktionsgruppenanwendung</span><span class="sxs-lookup"><span data-stu-id="b87d1-179">Response Group application</span></span></p></td>
<td><p><span data-ttu-id="b87d1-180"> http:// &lt; Interner FQDN- &gt; /RgsConfig</span><span class="sxs-lookup"><span data-stu-id="b87d1-180">http://&lt;Internal FQDN&gt;/RgsConfig</span></span></p>
<p><span data-ttu-id="b87d1-181"> http:// &lt; Interner FQDN- &gt; /RgsClients</span><span class="sxs-lookup"><span data-stu-id="b87d1-181">http://&lt;Internal FQDN&gt;/RgsClients</span></span></p></td>
<td><p><span data-ttu-id="b87d1-182">Speicherort des Reaktionsgruppen-Konfigurationstools</span><span class="sxs-lookup"><span data-stu-id="b87d1-182">Location of Response Group Configuration Tool.</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="b87d1-183">Für Front-End-Pools in einer konsolidierten Konfiguration müssen Sie IIS bereitstellen, bevor Sie dem Pool Server hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b87d1-183">For Front End pools in a consolidated configuration, you must deploy IIS before you can add servers to the pool.</span></span>


<table>
<thead>
<tr class="header">
<th><img src="images/Gg398321.security(OCS.15).gif" title="Sicherheits" alt="security" /><span data-ttu-id="b87d1-185">Sicherheitshinweis:</span><span class="sxs-lookup"><span data-stu-id="b87d1-185">Security Note:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b87d1-186">Sie müssen das IIS-Verwaltungs-Snap-in verwenden, um das vom IIS-Webkomponentenserver verwendete Zertifikat zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b87d1-186">You must use the IIS administrative snap-in to assign the certificate used by the IIS web component server.</span></span></td>
</tr>
</tbody>
</table><span data-ttu-id="b87d1-187">



</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b87d1-187">



</div>

<span> </span>

</div>

</div>

</span></span></div>

