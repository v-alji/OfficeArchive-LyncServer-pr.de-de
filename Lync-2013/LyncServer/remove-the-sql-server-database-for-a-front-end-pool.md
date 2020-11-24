---
title: Entfernen der SQL Server-Datenbank für einen Front-End-Pool
description: Entfernen Sie die SQL Server-Datenbank für einen Front-End-Pool.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove the SQL Server database for a Front End pool
ms:assetid: 6bb932df-3ed7-49b6-ae17-61e4c6a5fe82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688084(v=OCS.15)
ms:contentKeyID: 49733681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c5d47e4c52197c5792fa3b7770da7bbd1b26cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395243"
---
# <a name="remove-the-sql-server-database-for-a-front-end-pool"></a><span data-ttu-id="c13bd-103">Entfernen der SQL Server-Datenbank für einen Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="c13bd-103">Remove the SQL Server database for a Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c13bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c13bd-104">

<span> </span></span></span>

<span data-ttu-id="c13bd-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="c13bd-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="c13bd-106">Nachdem Sie einen Microsoft lync Server 2010-Front-End-Pool entfernt oder den Pool neu konfiguriert haben, um eine andere Datenbank zu verwenden, können Sie die SQL Server-Datenbanken entfernen, die die Pooldaten gehostet haben.</span><span class="sxs-lookup"><span data-stu-id="c13bd-106">After you remove a Microsoft Lync Server 2010 Front End pool or reconfigure the pool to use a different database, you can remove the SQL Server databases that hosted the pool data.</span></span> <span data-ttu-id="c13bd-107">Gehen Sie wie folgt vor, um die Definitionen aus dem Topology Builder zu entfernen und dann die Datenbank-und Protokolldateien vom Datenbankserver zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="c13bd-107">Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.</span></span>

<div>

## <a name="to-remove-the-sql-server-database-using-topology-builder"></a><span data-ttu-id="c13bd-108">So entfernen Sie die SQL Server-Datenbank mithilfe des Topologie-Generators</span><span class="sxs-lookup"><span data-stu-id="c13bd-108">To remove the SQL Server database using Topology Builder</span></span>

1.  <span data-ttu-id="c13bd-109">Öffnen Sie im lync Server 2013-Front-End-Server den Topologie-Generator, und laden Sie die vorhandene Topologie herunter.</span><span class="sxs-lookup"><span data-stu-id="c13bd-109">From the Lync Server 2013 Front End Server, open Topology Builder and download the existing topology.</span></span>

2.  <span data-ttu-id="c13bd-110">Navigieren Sie im Topologie-Generator zu **freigegebenen Komponenten** und dann zu **SQL Server-speichern**, klicken Sie mit der rechten Maustaste auf die SQL Server-Instanz, die dem entfernten oder neu konfigurierten Front-End-Pool zugeordnet ist, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="c13bd-110">In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Front End pool, and then click **Delete**.</span></span>

3.  <span data-ttu-id="c13bd-111">Veröffentlichen Sie die Topologie, und überprüfen Sie dann den Replikationsstatus.</span><span class="sxs-lookup"><span data-stu-id="c13bd-111">Publish the topology, and then check the replication status.</span></span>

</div>

<div>

## <a name="to-remove-user-and-application-databases-from-the-sql-server"></a><span data-ttu-id="c13bd-112">So entfernen Sie Benutzer-und Anwendungsdatenbanken aus dem SQL Server</span><span class="sxs-lookup"><span data-stu-id="c13bd-112">To remove user and application databases from the SQL Server</span></span>

1.  <span data-ttu-id="c13bd-113">Um die Datenbanken auf dem SQL Server zu entfernen, müssen Sie ein Mitglied der Gruppe SQL Server Sysadmins für den SQL Server sein, auf dem Sie die Datenbankdateien entfernen.</span><span class="sxs-lookup"><span data-stu-id="c13bd-113">To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.</span></span>

2.  <span data-ttu-id="c13bd-114">Öffnen der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="c13bd-114">Open Lync Server Management Shell</span></span>

3.  <span data-ttu-id="c13bd-115">Wenn Sie die Datenbank für den Pool Benutzerspeicher entfernen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="c13bd-115">To remove the database for the pool user store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType User -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="c13bd-116">Dabei handelt es \<FQDN\> sich um den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Datenbankservers und \<instance\> um die benannte Datenbankinstanz (also, wenn eine Definition definiert wurde).</span><span class="sxs-lookup"><span data-stu-id="c13bd-116">Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

4.  <span data-ttu-id="c13bd-117">Wenn Sie die Datenbank für den Pool-Anwendungsspeicher entfernen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="c13bd-117">To remove the database for the pool application store, type:</span></span>
    
        Uninstall-CsDataBase -DatabaseType Application -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    <span data-ttu-id="c13bd-118">Dabei handelt es sich um \<FQDN\> den FQDN des Datenbankservers, und \<instance\> Es handelt sich um die benannte Datenbankinstanz (also, wenn eine definiert wurde).</span><span class="sxs-lookup"><span data-stu-id="c13bd-118">Where \<FQDN\> is the FQDN of the database server, and \<instance\> is the named database instance (that is, if one was defined).</span></span>

5.  <span data-ttu-id="c13bd-119">Wenn Sie vom Cmdlet " **deinstallieren-CsDataBase** " aufgefordert werden, Aktionen zu bestätigen, lesen Sie die Informationen, und drücken Sie dann **Y** (oder drücken Sie die EINGABETASTE), um fortzufahren, oder drücken Sie **N** , und geben Sie dann ein, wenn Sie das Cmdlet beenden möchten (d. h., falls Fehler auftreten).</span><span class="sxs-lookup"><span data-stu-id="c13bd-119">When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).</span></span>

<span data-ttu-id="c13bd-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c13bd-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

