---
title: 'Lync Server 2013: Installieren des lokalen Konfigurationsspeichers'
description: 'Lync Server 2013: Installieren des lokalen Konfigurationsspeichers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install the Local Configuration store
ms:assetid: b563030d-d338-411f-9611-28d5eb4b3238
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412874(v=OCS.15)
ms:contentKeyID: 48185180
ms.date: 06/28/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bbf603704a8e1bdfbe71e0a9b064013d57bceda7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427138"
---
# <a name="install-the-local-configuration-store-in-lync-server-2013"></a><span data-ttu-id="a5270-103">Installieren des lokalen Konfigurationsspeichers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5270-103">Install the Local Configuration store in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5270-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5270-104">

<span> </span></span></span>

<span data-ttu-id="a5270-105">_**Letztes Änderungsdatum des Themas:** 2014-06-27_</span><span class="sxs-lookup"><span data-stu-id="a5270-105">_**Topic Last Modified:** 2014-06-27_</span></span>

<span data-ttu-id="a5270-106">Bevor Sie diese Schritte ausführen, stellen Sie sicher, dass Sie mit einem Domänenbenutzerkonto am Server angemeldet sind, das sowohl ein lokaler Administrator als auch ein Mitglied der RTCUniversalReadOnlyAdmin-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="a5270-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmin group.</span></span>

<span data-ttu-id="a5270-107">Damit Sie mit dem lync Server-Bereitstellungs-Assistenten etwas tun können, muss der lokale Konfigurationsspeicher auf einem Server vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a5270-107">To be able to do anything with the Lync Server Deployment Wizard, we need the Local Configuration store to exist on a server.</span></span> <span data-ttu-id="a5270-108">Der lokale Konfigurationsspeicher ist eine schreibgeschützte Kopie des zentralen Verwaltungsspeichers, der nach der lokalen Installation von SQL Server Express erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5270-108">The Local Configuration store is a read-only copy of the Central Management store, which gets created after the local installation of SQL Server Express.</span></span> <span data-ttu-id="a5270-109">Der zentrale Verwaltungsspeicher selbst wird der vorhandenen SQL Server-Datenbank hinzugefügt, die auf dem Standard Edition-Server oder auf der SQL Server Express-basierten Datenbank installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a5270-109">The Central Management store itself is added to the existing SQL Server database installed on the Standard Edition server or SQL Server Express-based database.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a5270-110">Wenn Sie das lync Server 2013-Setup noch nicht auf diesem Server ausgeführt haben, werden Sie zur Eingabe eines Laufwerks und Pfads aufgefordert, auf dem lync Server 2013 installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5270-110">If you haven’t run Lync Server 2013 setup on this server before, you’ll be prompted for a drive and path to install Lync Server 2013 to.</span></span> <span data-ttu-id="a5270-111">Auf diese Weise können Sie die Installation auf einem anderen Laufwerk als dem Systemlaufwerk durchführen, wenn es in Ihrer Organisation erforderlich ist, oder wenn Sie Platz Bedenken haben.</span><span class="sxs-lookup"><span data-stu-id="a5270-111">This will let you install to a drive other than the system drive, if your organization requires it, or if you have space concerns.</span></span> <span data-ttu-id="a5270-112">Sie können einfach den Pfad für den Installationspfad für die lync Server-Dateien im Dialogfeld einrichten auf ein neues, verfügbares Laufwerk ändern.</span><span class="sxs-lookup"><span data-stu-id="a5270-112">You can just change the installation location path for the Lync Server files in the Setup dialog box to a new, available drive.</span></span> <span data-ttu-id="a5270-113">Wenn Sie die Setup Dateien in diesem Pfad, einschließlich OCSCore.msi, installieren, werden die restlichen lync Server 2013-Dateien ebenfalls bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a5270-113">If you install the Setup files to this path, including OCSCore.msi, the rest of the Lync Server 2013 files will deploy there as well.</span></span>



</div>

<div>

## <a name="to-install-the-local-configuration-store"></a><span data-ttu-id="a5270-114">So installieren Sie den lokalen Konfigurationsspeicher</span><span class="sxs-lookup"><span data-stu-id="a5270-114">To install the Local Configuration store</span></span>

1.  <span data-ttu-id="a5270-115">Navigieren Sie auf Ihrem Installationsmedium zu \\ Setup \\ amd64 \\Setup.exe, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5270-115">From your installation media, browse to \\setup\\amd64\\Setup.exe, and then click **OK**.</span></span>

2.  <span data-ttu-id="a5270-116">Wenn Sie aufgefordert werden, die Microsoft Visual C++ 2012-verteilbare Installation zu installieren, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a5270-116">If you’re prompted to install the Microsoft Visual C++ 2012 Redistributable, click **Yes**.</span></span>

3.  <span data-ttu-id="a5270-117">Klicken Sie auf der Seite **lync Server 2013-Installationsspeicherort** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5270-117">On the **Lync Server 2013 Installation Location** page, click **OK**.</span></span>

4.  <span data-ttu-id="a5270-118">Überprüfen Sie auf der Seite **Endbenutzer-Lizenzvertrag** die Lizenzbedingungen, und wählen Sie **Ich akzeptiere die Bedingungen im Lizenzvertrag** aus, und klicken Sie dann auf **OK** , um den Vorgang fortsetzen zu können.</span><span class="sxs-lookup"><span data-stu-id="a5270-118">On the **End User License Agreement** page, review the license terms, you’ll need to select **I accept the terms in the license agreement**, and then click **OK** to be able to continue.</span></span>

5.  <span data-ttu-id="a5270-119">Klicken Sie auf der Seite Deployment-Assistent auf **lync Server System installieren oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="a5270-119">On the Deployment Wizard page, click **Install or Update Lync Server System**.</span></span>

6.  <span data-ttu-id="a5270-120">Klicken Sie auf der Seite **lync Server 2013** neben Schritt 1 **: lokalen Konfigurationsspeicher installieren** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="a5270-120">On the **Lync Server 2013** page, next to **Step1: Install Local Configuration Store**, click **Run**.</span></span>

7.  <span data-ttu-id="a5270-121">Vergewissern Sie sich auf der Seite **Lokalen Konfigurationsspeicher installieren**, dass die Option **Direkt vom zentralen Verwaltungsspeicher abrufen** ausgewählt ist, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="a5270-121">On the **Install Local Configuration Store** page, make sure that the **Retrieve directly from the Central Management store** option is selected, and then click **Next**.</span></span>

8.  <span data-ttu-id="a5270-122">Wenn die Installation der lokalen Serverkonfiguration abgeschlossen ist, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="a5270-122">When the local server configuration installation is complete, you should click **Finish**.</span></span>

<span data-ttu-id="a5270-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5270-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

