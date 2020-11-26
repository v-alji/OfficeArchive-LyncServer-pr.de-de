---
title: 'Lync Server 2013: Installieren von Lync Server-Serverkomponenten'
description: 'Lync Server 2013: Installieren der lync Server-Server Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server server components
ms:assetid: 186aed6e-7adf-4a92-9f2e-f9a4de5ff202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398239(v=OCS.15)
ms:contentKeyID: 48183528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1930926f3a46be868d838abf646eb8702c9713a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427166"
---
# <a name="install-server-components-for-lync-server-2013"></a><span data-ttu-id="70a27-103">Installieren von Serverkomponenten für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70a27-103">Install server components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70a27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70a27-104">

<span> </span></span></span>

<span data-ttu-id="70a27-105">_**Letztes Änderungsdatum des Themas:** 2014-05-05_</span><span class="sxs-lookup"><span data-stu-id="70a27-105">_**Topic Last Modified:** 2014-05-05_</span></span>

<span data-ttu-id="70a27-106">Bevor Sie diese Schritte ausführen, stellen Sie sicher, dass Sie bei dem Server mit einem Domänenbenutzerkonto angemeldet sind, das sowohl ein lokaler Administrator als auch ein Mitglied der RTCUniversalReadOnlyAdmins-Gruppe in Active Directory ist.</span><span class="sxs-lookup"><span data-stu-id="70a27-106">Before following these steps, make sure you’re logged onto the server with a domain user account that’s both a local administrator and a member of the RTCUniversalReadOnlyAdmins group in Active Directory.</span></span>

<span data-ttu-id="70a27-107">Der lync Server-Bereitstellungs-Assistent wird verwendet, um die erforderlichen Komponenten für jede lync-Serverrolle zu installieren und den Server zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="70a27-107">The Lync Server Deployment Wizard is used to install the needed components for each Lync server role and to activate the server.</span></span> <span data-ttu-id="70a27-108">Dieser Artikel führt Sie durch die Schritte zum Bereitstellen eines Standard Edition-Servers oder eines Front-End-Servers in ihrer lync-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="70a27-108">This article walks you through the steps of deploying a Standard Edition server or a Front End Server in your Lync infrastructure.</span></span>

<div>

## <a name="to-install-lync-server-components"></a><span data-ttu-id="70a27-109">So installieren Sie lync Server-Komponenten</span><span class="sxs-lookup"><span data-stu-id="70a27-109">To install Lync Server components</span></span>

1.  <span data-ttu-id="70a27-110">Wenn der lync Server-Bereitstellungs-Assistent nicht ausgeführt wird, starten Sie ihn auf dem Server, auf dem Sie lync installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="70a27-110">If the Lync Server Deployment Wizard isn’t running, start it on the server you want to install Lync onto.</span></span>

2.  <span data-ttu-id="70a27-111">Klicken Sie auf **lync Server System installieren oder aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="70a27-111">Click **Install or Update Lync Server System**.</span></span>

3.  <span data-ttu-id="70a27-112">Bestätigen Sie im Bereitstellungs-Assistenten, dass **Schritt 1: Installieren des lokalen Konfigurationsspeichers** ein grünes Häkchen aufweist, was bedeutet, dass dieser Server eine lokale Kopie des Stores erfolgreich installiert hat.</span><span class="sxs-lookup"><span data-stu-id="70a27-112">In the Deployment Wizard, confirm that **Step 1: Install Local Configuration Store** has a green check mark, which means that this server has a local copy of the store installed successfully.</span></span> <span data-ttu-id="70a27-113">Wenn das Kontrollkästchen nicht aktiviert ist, müssen Sie den lokalen Konfigurationsspeicher auf dem Server installieren.</span><span class="sxs-lookup"><span data-stu-id="70a27-113">If it’s not checked, you need to install the Local Configuration store on the server.</span></span> <span data-ttu-id="70a27-114">Führen Sie die Schritte unter [Installieren des lokalen Konfigurationsspeichers in lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) aus, und kehren Sie dann zurück.</span><span class="sxs-lookup"><span data-stu-id="70a27-114">Follow the steps at [Install the Local Configuration store in Lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) and then come back here.</span></span>

4.  <span data-ttu-id="70a27-115">Wenn Sie bereit sind, die lync Server 2013-Komponenten auf dem Server zu installieren, klicken Sie auf **Ausführen** neben **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="70a27-115">When you’re ready to install the Lync Server 2013 components on your server, click **Run** next to **Step 2: Setup or Remove Lync Server Components**.</span></span>

5.  <span data-ttu-id="70a27-116">Klicken Sie auf der Seite **lync Server-Komponenten einrichten** auf **weiter** , um Komponenten gemäß der Definition in der veröffentlichten Topologie einzurichten.</span><span class="sxs-lookup"><span data-stu-id="70a27-116">On the **Set Up Lync Server Components** page, click **Next** to set up components as defined in your published topology.</span></span>

6.  <span data-ttu-id="70a27-117">Auf der Seite " **Befehle ausführen** " wird eine Zusammenfassung der Befehle und Installationsinformationen angezeigt, wenn die Einrichtung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="70a27-117">The **Executing Commands** page will display a summary of commands and installation information as the set up takes place.</span></span> <span data-ttu-id="70a27-118">Nach Abschluss des Vorgangs können Sie in der angezeigten Liste ein Protokoll auswählen und auf **Protokoll anzeigen** klicken.</span><span class="sxs-lookup"><span data-stu-id="70a27-118">When it’s done, you can use the list to select a log to view, and then click **View Log**.</span></span>

7.  <span data-ttu-id="70a27-119">Wenn das Setup von lync Server 2013-Komponenten abgeschlossen ist und Sie die Protokolle nach Bedarf überprüft haben, klicken Sie auf **Fertig stellen** , um diesen Schritt in der Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="70a27-119">When Lync Server 2013 components setup is done, and you’ve reviewed the logs as needed, click **Finish** to complete this step in the installation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="70a27-120">Wenn Sie aufgefordert werden, den Server neu zu starten (was möglicherweise der Fall ist, wenn die Windows-Desktop Umgebung installiert werden muss), tun Sie dies unbedingt.</span><span class="sxs-lookup"><span data-stu-id="70a27-120">If you’re prompted to restart the server (which might happen if Windows Desktop Experience needed to be installed), definitely do that.</span></span> <span data-ttu-id="70a27-121">Wenn der Computer wieder in Betrieb ist, müssen Sie diese Schritte wiederholen, beginnend mit Schritt 3, der oben aufgeführt ist (im Grunde Schritt 2 im Bereitstellungs-Assistenten ausführen).</span><span class="sxs-lookup"><span data-stu-id="70a27-121">When the computer is back up and running, you need to do these steps over again, starting from step three listed above (basically run Step 2 in the Deployment Wizard one more time).</span></span>

    
    <span data-ttu-id="70a27-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70a27-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

