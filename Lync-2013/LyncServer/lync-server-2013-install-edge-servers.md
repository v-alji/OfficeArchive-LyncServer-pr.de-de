---
title: 'Lync Server 2013: Installieren von Edgeservern'
description: 'Lync Server 2013: Installieren von Edgeserver.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Edge Servers
ms:assetid: 1655ab69-3899-4ee4-a1cc-8243bc1bfa0f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398230(v=OCS.15)
ms:contentKeyID: 48183503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e699a7f41b0ee554bc85fb2d9a72a2d9a42870cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427208"
---
# <a name="install-edge-servers-for-lync-server-2013"></a><span data-ttu-id="8bae0-103">Installieren von Edgeservern für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8bae0-103">Install Edge Servers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bae0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bae0-104">

<span> </span></span></span>

<span data-ttu-id="8bae0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="8bae0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="8bae0-106">Sie installieren lync Server 2013 auf Edge-Servern mithilfe des lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="8bae0-106">You install Lync Server 2013 on Edge Servers by using Lync Server Deployment Wizard.</span></span> <span data-ttu-id="8bae0-107">Wenn Sie den Bereitstellungs-Assistenten auf jedem Edgeserver ausführen, können Sie die meisten Aufgaben ausführen, die zum Einrichten des Edge-Servers erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8bae0-107">By running the Deployment Wizard on each Edge Server, you can complete most of the tasks required to set up the Edge Server.</span></span> <span data-ttu-id="8bae0-108">Damit Sie lync Server 2013 auf einem Edgeserver bereitstellen können, müssen Sie den Topologie-Generator bereits ausgeführt haben, um die Edgeserver-Topologie zu definieren und zu veröffentlichen und Sie auf Medien zu exportieren, die vom Edgeserver zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8bae0-108">In order to deploy Lync Server 2013 on an Edge Server, you must have already run Topology Builder to define and publish your Edge Server topology, and exported it to media that is available from the Edge Server.</span></span> <span data-ttu-id="8bae0-109">Ausführliche Informationen finden Sie unter [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) , [Exportieren Ihrer lync Server 2013-Topologie und Kopieren dieser in externe Medien für die Edge-Installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span><span class="sxs-lookup"><span data-stu-id="8bae0-109">For details, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<span data-ttu-id="8bae0-110">Nachdem Sie den Bereitstellungs-Assistenten verwendet haben, um jeden Edgeserver zu installieren, die erforderlichen Zertifikate zu installieren und zuzuweisen und die erforderlichen Dienste zu starten, können Sie die Einrichtung mithilfe der Informationen unter [Konfigurieren der Unterstützung für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-configuring-support-for-external-user-access.md) zum Aktivieren und Konfigurieren des Zugriffs auf externe Benutzer sowie der Informationen unter [Überprüfen der Edge-Bereitstellung in lync Server 2013 zum über](lync-server-2013-verifying-your-edge-deployment.md)</span><span class="sxs-lookup"><span data-stu-id="8bae0-110">After using the Deployment Wizard to install each Edge Server, install and assign the required certificates, and start the required services, you can complete the setup by using the information in [Configuring support for external user access in Lync Server 2013](lync-server-2013-configuring-support-for-external-user-access.md) to enable and configure external user access and the information in [Verifying your edge deployment in Lync Server 2013](lync-server-2013-verifying-your-edge-deployment.md) to validate the setup, including server and client connectivity.</span></span>

<div>

## <a name="to-install-an-edge-server"></a><span data-ttu-id="8bae0-111">So installieren Sie einen Edgeserver</span><span class="sxs-lookup"><span data-stu-id="8bae0-111">To install an Edge Server</span></span>

1.  <span data-ttu-id="8bae0-112">Melden Sie sich bei dem Computer an, auf dem Sie Ihren Edge-Server als Mitglied der lokalen Gruppe Administratoren installieren möchten, oder ein Konto mit entsprechenden Benutzerrechten und Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="8bae0-112">Log on to the computer on which you want to install your Edge Server as a member of the local Administrators group or an account with equivalent user rights and permissions.</span></span>

2.  <span data-ttu-id="8bae0-113">Stellen Sie sicher, dass die Topologie-Konfigurationsdatei, die Sie mit dem Topologie-Generator erstellt und dann auf externe Medien exportiert und kopiert haben, auf dem Edgeserver verfügbar ist (beispielsweise Zugriff auf das USB-Laufwerk, auf dem Sie die Topologie-Konfigurationsdatei kopiert haben, oder überprüfen Sie den Zugriff auf die Netzwerkfreigabe, in die Sie die Datei kopiert haben).</span><span class="sxs-lookup"><span data-stu-id="8bae0-113">Ensure that the topology configuration file you created using Topology Builder, and then exported and copied to external media, is available on the Edge Server (for example, access to the USB drive onto which you copied the topology configuration file, or verify access to the network share where you copied the file).</span></span>

3.  <span data-ttu-id="8bae0-114">Starten Sie den Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="8bae0-114">Start the Deployment Wizard.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8bae0-115">Wenn Sie eine Meldung erhalten, die besagt, dass Sie Microsoft Visual C++ Redistributable installieren müssen, klicken Sie auf <STRONG>Ja</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8bae0-115">If you get a message saying that you need to install Microsoft Visual C++ Redistributable, click <STRONG>Yes</STRONG>.</span></span> <span data-ttu-id="8bae0-116">Im nächsten Dialogfeld können Sie den Standard <STRONG>Installationsspeicherort</STRONG> übernehmen oder auf die <STRONG>Schaltfläche Durchsuchen</STRONG> klicken, um einen anderen Speicherort auszuwählen, und dann auf <STRONG>Installieren</STRONG>klicken.</span><span class="sxs-lookup"><span data-stu-id="8bae0-116">In the next dialog box, you can accept the default <STRONG>Installation Location</STRONG> or click the <STRONG>Browse</STRONG> to select an alternate location, and then click <STRONG>Install</STRONG>.</span></span> <span data-ttu-id="8bae0-117">Aktivieren Sie im nächsten Dialogfeld das Kontrollkästchen <STRONG>Ich akzeptiere die Bedingungen im Lizenzvertrag</STRONG> , und klicken Sie dann auf <STRONG>OK</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="8bae0-117">In the next dialog box, select the <STRONG>I accept the terms in the license agreement</STRONG> check box, and then click <STRONG>OK</STRONG>.</span></span>

    
    </div>

4.  <span data-ttu-id="8bae0-118">Klicken Sie im Bereitstellungs-Assistenten auf **lync Server System installieren oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-118">In the Deployment Wizard, click **Install or Update Lync Server System**.</span></span>

5.  <span data-ttu-id="8bae0-119">Nachdem der Assistent den Bereitstellungsstatus für Schritt 1 festgelegt hat **. Installieren Sie den lokalen Konfigurationsspeicher**, klicken Sie auf **Ausführen** , und gehen Sie dann folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="8bae0-119">After the wizard determines the deployment state, for **Step 1. Install Local Configuration Store**, click **Run** and then do the following:</span></span>
    
      - <span data-ttu-id="8bae0-120">Klicken Sie im Dialogfeld **lokales Replikat des zentralen Verwaltungsspeichers konfigurieren** auf **aus einer Datei importieren (empfohlen für Edgeserver)**, wechseln Sie zum Speicherort der exportierten Topologie-Konfigurationsdatei, wählen Sie die ZIP-Datei aus, klicken Sie auf **Öffnen**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-120">In the **Configure Local Replica of Central Management Store** dialog box, click **Import from a file (Recommended for Edge Servers)**, go to the location of the exported topology configuration file, select the .zip file, click **Open**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="8bae0-121">Der Bereitstellungs-Assistent liest die Konfigurationsinformationen aus der Konfigurationsdatei und schreibt die XML-Konfigurationsdatei auf den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="8bae0-121">The Deployment Wizard reads the configuration information from the configuration file and writes the XML configuration file to the local computer.</span></span>
    
      - <span data-ttu-id="8bae0-122">Nachdem der Prozess **Befehle werden ausgeführt** abgeschlossen wurde, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="8bae0-122">After the **Executing Commands** process is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="8bae0-123">Klicken Sie im Bereitstellungs-Assistenten auf **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten** , um die in der XML-Konfigurationsdatei angegebenen Edge-Komponenten von lync Server 2013 zu installieren, die auf dem lokalen Computer gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="8bae0-123">In the Deployment Wizard, click **Step 2: SetUp or Remove Lync Server Components** to install the Lync Server 2013 edge components specified in the XML configuration file that is stored on the local computer.</span></span>

7.  <span data-ttu-id="8bae0-124">Nachdem Sie die Installation abgeschlossen haben, verwenden Sie die Informationen unter [Einrichten von Edge-Zertifikaten für lync Server 2013](lync-server-2013-set-up-edge-certificates.md) , um die erforderlichen Zertifikate zu installieren und zuzuweisen, bevor Sie Dienste starten.</span><span class="sxs-lookup"><span data-stu-id="8bae0-124">After completing the installation, use the information in [Set up Edge certificates for Lync Server 2013](lync-server-2013-set-up-edge-certificates.md) to install and assign the required certificates before you start services.</span></span>

<span data-ttu-id="8bae0-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bae0-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

