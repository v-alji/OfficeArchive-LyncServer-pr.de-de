---
title: Entfernen der SQL Server-Datenbank für einen Monitoring Server
description: Entfernen Sie die SQL Server-Datenbank für einen Überwachungs Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Monitoring server
ms:assetid: aed5e394-d63e-4ad4-af40-f12d3a044344
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721848(v=OCS.15)
ms:contentKeyID: 49733781
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 99bf734f0a9978fe14055fb36b01ce37f77e14a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440255"
---
# <a name="remove-the-sql-server-database-for-a-monitoring-server"></a><span data-ttu-id="aea5e-103">Entfernen der SQL Server-Datenbank für einen Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="aea5e-103">Remove the SQL Server database for a Monitoring server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aea5e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aea5e-104">

<span> </span></span></span>

<span data-ttu-id="aea5e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="aea5e-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="aea5e-106">Nachdem Sie einen Microsoft lync Server 2010-Überwachungs Server entfernt haben, können Sie die SQL Server-Datenbanken entfernen, die die Server Daten gehostet haben.</span><span class="sxs-lookup"><span data-stu-id="aea5e-106">After you remove a Microsoft Lync Server 2010 Monitoring Server, you can remove the SQL Server databases that hosted the server data.</span></span> <span data-ttu-id="aea5e-107">Gehen Sie wie folgt vor, um die Definitionen aus dem Topology Builder zu entfernen und dann die Datenbank-und Protokolldateien vom Datenbankserver zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="aea5e-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="aea5e-108">So entfernen Sie die SQL Server-Datenbank mithilfe des Topologie-Generators</span><span class="sxs-lookup"><span data-stu-id="aea5e-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="aea5e-109">Öffnen Sie auf dem lync Server 2013-Front-End-Server den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="aea5e-109">On the Lync Server 2013 Front End Server, open Topology Builder.</span></span>

2.  <span data-ttu-id="aea5e-110">Navigieren Sie im Topologie-Generator zu **freigegebenen Komponenten** und dann zu **SQL Server-speichern**, klicken Sie mit der rechten Maustaste auf die SQL Server-Instanz, die dem entfernten oder neu konfigurierten Überwachungs Server zugeordnet ist, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="aea5e-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Monitoring Server, and then click **Delete**.</span></span>

3.  <span data-ttu-id="aea5e-111">Veröffentlichen Sie die Topologie, und überprüfen Sie dann den Replikationsstatus.</span><span class="sxs-lookup"><span data-stu-id="aea5e-111">Publish the topology, and then check replication status.</span></span>

</div>

<div>

## <a name="to-remove-the-database-files-from-the-sql-server"></a><span data-ttu-id="aea5e-112">So entfernen Sie die Datenbankdateien aus dem SQL Server</span><span class="sxs-lookup"><span data-stu-id="aea5e-112">To remove the database files from the SQL Server</span></span>

1.  <span data-ttu-id="aea5e-113">Um die Datenbanken auf dem SQL Server-basierten Server zu entfernen, müssen Sie ein Mitglied der Gruppe SQL Server-Sysadmins für den SQL Server-Server sein, auf dem Sie die Datenbankdateien entfernen.</span><span class="sxs-lookup"><span data-stu-id="aea5e-113">To remove the databases on the SQL Server-based server, you must be a member of the SQL Server sysadmins group for the SQL Server server where you are removing the database files.</span></span>

2.  <span data-ttu-id="aea5e-114">Öffnen Sie die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="aea5e-114">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="aea5e-115">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="aea5e-115">At the command line, type the following:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Monitoring -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="aea5e-116">Dabei handelt es sich um \<FQDN\> den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Datenbankservers und \<instance\> um die optionale benannte Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="aea5e-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the optional named database instance.</span></span>

4.  <span data-ttu-id="aea5e-117">Wenn Sie vom Cmdlet " **deinstallieren-CsDataBase** " aufgefordert werden, Aktionen zu bestätigen, lesen Sie die Informationen, und drücken Sie dann **Y** (oder drücken Sie die EINGABETASTE), um fortzufahren, oder drücken Sie **N** , und geben Sie dann ein, wenn Sie das Cmdlet beenden möchten (d. h., falls Fehler auftreten).</span><span class="sxs-lookup"><span data-stu-id="aea5e-117">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="aea5e-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aea5e-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

