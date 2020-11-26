---
title: Checkliste für die lync Server 2013-Bereitstellung für Webkonferenzen
description: Checkliste für die lync Server 2013-Bereitstellung für Webkonferenzen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for web conferencing
ms:assetid: 9908ebe0-e5d3-4920-b9b1-85021f7e69e9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205104(v=OCS.15)
ms:contentKeyID: 48184878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6194cb71af268a45dc5c142c1814d8c1ef15c09e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429706"
---
# <a name="deployment-checklist-for-web-conferencing-in-lync-server-2013"></a><span data-ttu-id="7b4ec-103">Bereitstellungscheckliste für Webkonferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b4ec-103">Deployment checklist for web conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b4ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b4ec-104">

<span> </span></span></span>

<span data-ttu-id="7b4ec-105">_**Letztes Änderungsdatum des Themas:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="7b4ec-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="7b4ec-106">Wie bei der Bereitstellung Ihrer anderen lync Server 2013-Komponenten erfordert die Bereitstellung von Webkonferenzen, dass Sie den Topologie-Generator verwenden, um eine Topologie zu erstellen und zu veröffentlichen, in der Konferenzen integriert sind.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-106">As with deployment of your other Lync Server 2013 components, deployment of web conferencing requires that you use Topology Builder to create and publish a topology that incorporates conferencing.</span></span>

<div>

## <a name="deployment-sequence"></a><span data-ttu-id="7b4ec-107">Bereitstellungssequenz</span><span class="sxs-lookup"><span data-stu-id="7b4ec-107">Deployment Sequence</span></span>

<span data-ttu-id="7b4ec-108">Sie können Konferenzen gleichzeitig bereitstellen, indem Sie Ihre anfängliche Topologie bereitstellen oder nachdem Sie mindestens einen Front-End-Pool oder Standard Edition-Server bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-108">You can deploy conferencing at the same time that you deploy your initial topology or after you have deployed at least one Front End pool or Standard Edition server.</span></span>

</div>

<div>

## <a name="conferencing-deployment-process"></a><span data-ttu-id="7b4ec-109">Konferenz Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="7b4ec-109">Conferencing Deployment Process</span></span>

<span data-ttu-id="7b4ec-110">Die folgende Tabelle enthält eine Übersicht über die erforderlichen Schritte zum Bereitstellen von Konferenzen in einer vorhandenen Topologie.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-110">The following table provides an overview of the steps required to deploy conferencing into an existing topology.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b4ec-111">Phase</span><span class="sxs-lookup"><span data-stu-id="7b4ec-111">Phase</span></span></th>
<th><span data-ttu-id="7b4ec-112">Schritte</span><span class="sxs-lookup"><span data-stu-id="7b4ec-112">Steps</span></span></th>
<th><span data-ttu-id="7b4ec-113">Rollen und Gruppenmitgliedschaften</span><span class="sxs-lookup"><span data-stu-id="7b4ec-113">Roles and group memberships</span></span></th>
<th><span data-ttu-id="7b4ec-114">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7b4ec-114">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b4ec-115"><strong>Installieren der erforderlichen Hardware und Software</strong></span><span class="sxs-lookup"><span data-stu-id="7b4ec-115"><strong>Install prerequisite hardware and software</strong></span></span></p></td>
<td><p><span data-ttu-id="7b4ec-116">Konferenzen werden auf Front-End-Servern in einem Front-End-Pool und auf Standard Edition-Servern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-116">Conferencing runs on Front End Servers in a Front End pool and Standard Edition servers.</span></span> <span data-ttu-id="7b4ec-117">Abgesehen von den herkömmlichen Anforderungen zur Installation dieser Server bestehen keine zusätzlichen Hardware- oder Softwareanforderungen.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-117">It has no additional hardware or software requirements beyond what is required to install those servers.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7b4ec-118">In lync Server 2013 werden Office Web Apps und der Office Web Apps-Server verwendet, um die Freigabe und das Rendern von PowerPoint-Präsentationen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-118">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="7b4ec-119">Informationen zum Installieren und Konfigurieren von Office Web Apps Server finden Sie unter <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Konfigurieren der Integration in Office Web Apps Server und lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-119">For information about installing and configuring the Office Web Apps Server, see <A href="lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md">Configuring integration with Office Web Apps Server and Lync Server 2013</A>.</span></span>


</div></td>
<td><p><span data-ttu-id="7b4ec-120">Domänenbenutzer, der Mitglied der lokalen Administratorgruppe ist</span><span class="sxs-lookup"><span data-stu-id="7b4ec-120">Domain user who is a member of the local Administrators group</span></span></p></td>
<td><p><span data-ttu-id="7b4ec-121"><a href="lync-server-2013-supported-hardware.md">Unterstützte Hardware für lync Server 2013</a> in der Dokumentation zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b4ec-121"><a href="lync-server-2013-supported-hardware.md">Supported hardware for Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="7b4ec-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Unterstützung für Server Software und-Infrastruktur in lync Server 2013</a> in der Dokumentation zur Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7b4ec-122"><a href="lync-server-2013-server-software-and-infrastructure-support.md">Server software and infrastructure support in Lync Server 2013</a> in the Supportability documentation</span></span></p>
<p><span data-ttu-id="7b4ec-123"><a href="lync-server-2013-determining-your-system-requirements.md">Ermitteln der Systemanforderungen für lync Server 2013</a> in der Planungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="7b4ec-123"><a href="lync-server-2013-determining-your-system-requirements.md">Determining your system requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p>
<p><span data-ttu-id="7b4ec-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technische Voraussetzungen für die Archivierung in lync Server 2013</a> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-124"><a href="lync-server-2013-technical-requirements-for-archiving.md">Technical requirements for Archiving in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b4ec-125"><strong>Erstellen der geeigneten internen Topologie zur Unterstützung von Konferenzen</strong></span><span class="sxs-lookup"><span data-stu-id="7b4ec-125"><strong>Create the appropriate internal topology to support conferencing</strong></span></span></p></td>
<td><p><span data-ttu-id="7b4ec-126">Führen Sie den Topologie-Generator aus, um der Topologie Konferenzen hinzuzufügen, und veröffentlichen Sie dann die Topologie.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-126">Run Topology Builder to add conferencing to the topology, and then publish the topology.</span></span></p></td>
<td><p><span data-ttu-id="7b4ec-127">Zum Definieren einer Topologie: Konto, das Mitglied der lokalen Benutzergruppe ist</span><span class="sxs-lookup"><span data-stu-id="7b4ec-127">To define a topology, an account that is a member of the local Users group</span></span></p>
<p><span data-ttu-id="7b4ec-128">So veröffentlichen Sie die Topologie: ein Konto, das ein Mitglied der Gruppe "Domänen-Admins" und der RTCUniversalServerAdmins-Gruppe ist und das Vollzugriffsberechtigungen (Lesen/Schreiben/ändern) für die Dateifreigabe hat, die für den lync Server 2013-Dateispeicher verwendet werden soll (damit der Topologie-Generator die erforderlichen DACLs konfigurieren kann)</span><span class="sxs-lookup"><span data-stu-id="7b4ec-128">To publish the topology, an account that is a member of the Domain Admins group and RTCUniversalServerAdmins group, and that has full control permissions (read/write/modify) on the file share to be used for the Lync Server 2013 file store (so that Topology Builder can configure the required DACLs)</span></span></p></td>
<td><p><span data-ttu-id="7b4ec-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Definieren und konfigurieren Sie eine Topologie im Topologie-Generator für lync Server 2013</a> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-129"><a href="lync-server-2013-define-and-configure-a-topology-in-topology-builder.md">Define and configure a topology in Topology Builder for Lync Server 2013</a> in the Deployment documentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b4ec-130"><strong>Konfigurieren von Konferenzrichtlinien und-Support</strong></span><span class="sxs-lookup"><span data-stu-id="7b4ec-130"><strong>Configure conferencing policies and support</strong></span></span></p></td>
<td><p><span data-ttu-id="7b4ec-131">Verwenden Sie die lync Server 2013-Systemsteuerung oder die lync Server-Verwaltungsshell, um Konferenzeinstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-131">Use the Lync Server 2013 Control Panel or Lync Server Management Shell to configure conferencing settings.</span></span></p></td>
<td><p><span data-ttu-id="7b4ec-132">RTCUniversalServerAdmins-Gruppe (nur Windows PowerShell) oder Zuweisen von Benutzern zur []-oder CSAdministrator-Rolle</span><span class="sxs-lookup"><span data-stu-id="7b4ec-132">RTCUniversalServerAdmins group ( Windows PowerShell only) or assign users to the [] or CSAdministrator role</span></span></p></td>
<td><p><span data-ttu-id="7b4ec-133"><a href="lync-server-2013-conferencing-policies.md">Konferenzrichtlinien in lync Server 2013</a> in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-133"><a href="lync-server-2013-conferencing-policies.md">Conferencing policies in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7b4ec-134">Lync Server 2013 enthält jetzt die **MaxUploadFileSizeMb** -Einstellung, die die Größe von Dateien begrenzt, die während einer Besprechung hochgeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-134">Lync Server 2013 now includes the **MaxUploadFileSizeMb** setting, which limits the size of files that can be uploaded during a meeting.</span></span> <span data-ttu-id="7b4ec-135">Der Standardwert für diese Einstellung ist 500 MB.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-135">The default value for this setting is 500 MB.</span></span> <span data-ttu-id="7b4ec-136">Sie können **MaxUploadFileSizeMb** mit dem Cmdlet " **Satz-CsConferencingConfiguration** " anpassen.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-136">You can adjust **MaxUploadFileSizeMb** using the **Set-CsConferencingConfiguration** cmdlet.</span></span>

<span data-ttu-id="7b4ec-137">**MaxUploadFileSizeMb** schränkt die Einstellung für den Dateiupload für lync Web App nicht ein.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-137">**MaxUploadFileSizeMb** does not limit the file upload setting for Lync Web App.</span></span> <span data-ttu-id="7b4ec-138">Die maximale Upload-Grenze für die Dateigröße für lync Web App ist auf ungefähr 30 MB festgesetzt und wird durch die IIS web.config-Datei gesteuert:/DataCollabWeb/int \[ Ext \] /Handler/web.config. Zum Konfigurieren des Upload-Grenzwerts für die Dateigröße für lync Web App aktualisieren Sie `maxRequestLength` und `maxAllowedContentLength` in der web.config-Datei wie unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-138">The file size upload limit for Lync Web App is set to approximately 30MB and is controlled by the IIS web.config file: /DataCollabWeb/Int\[Ext\]/Handler/web.config. To configure the file size upload limit for Lync Web App, update `maxRequestLength` and `maxAllowedContentLength` in the web.config file as shown below.</span></span>

    <system.web>
        <!-- 
            Since this handler is used to upload files to DMCU the request size (in kilobytes) 
            has to fit max allowed file size uploaded by LWA client.
            The timeout has to reflect the min client bandwidth. Timeout of 600 secs 
            and 512 Kbits of *client* bandwidth would result into aproximately 30 Mbytes 
            for LWA upload size limit.
        -->
          <httpRuntime maxRequestLength="500000" executionTimeout="600" />
    
    
    
                    <security>
                    <requestFiltering>
                               <requestLimits maxAllowedContentLength="524288000" />
                    </requestFiltering>
                    </security>

<span data-ttu-id="7b4ec-139">Sie müssen die web.config-Datei für jeden Front-End-Server aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7b4ec-139">You must update the web.config file for each Front End Server.</span></span>

<span data-ttu-id="7b4ec-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b4ec-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

