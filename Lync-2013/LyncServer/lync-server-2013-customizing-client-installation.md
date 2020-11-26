---
title: 'Lync Server 2013: Anpassen der Clientinstallation'
description: 'Lync Server 2013: Anpassen der Clientinstallation'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Customizing client installation
ms:assetid: 5c1a85f1-5ebb-48fb-acb7-3bf46decbf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204934(v=OCS.15)
ms:contentKeyID: 48184254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8dd1942c298ccbc8b6a2950baf4f24cc2f797a92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431372"
---
# <a name="customizing-client-installation-in-lync-server-2013"></a><span data-ttu-id="83437-103">Anpassen der Clientinstallation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="83437-103">Customizing client installation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="83437-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="83437-104">

<span> </span></span></span>

<span data-ttu-id="83437-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="83437-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="83437-106">Unternehmensadministratoren können die Windows Installer-basierte Installation (MSI) von Office 2013 mithilfe der in diesem Abschnitt beschriebenen Methoden anpassen.</span><span class="sxs-lookup"><span data-stu-id="83437-106">Enterprise administrators can customize the Office 2013 Windows Installer-based (.msi) installation by using the methods discussed in this section.</span></span> <span data-ttu-id="83437-107">Da kein einzelnes Tool alle Anpassungsoptionen bereitstellt, verwenden Sie wahrscheinlich eine Kombination dieser Methoden in ihrer lync 2013-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="83437-107">Because no single tool provides all customization options, you’ll likely use a combination of these methods in your Lync 2013 deployment.</span></span> <span data-ttu-id="83437-108">Sie können die in den folgenden Abschnitten beschriebenen Tools mindestens verwenden:</span><span class="sxs-lookup"><span data-stu-id="83437-108">At a minimum, you might use the tools described in the following sections:</span></span>

  - <span data-ttu-id="83437-109">[Verwenden Sie das Office-Anpassungs Tool (OAT) in lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) , um die Setupoptionen und Features für lync und andere Office-Programme anzupassen.</span><span class="sxs-lookup"><span data-stu-id="83437-109">[Using the Office Customization Tool (OCT) in Lync Server 2013](lync-server-2013-using-the-office-customization-tool-oct.md) to customize setup options and features for Lync and other Office programs.</span></span>

  - <span data-ttu-id="83437-110">[Verwenden von Config.xml zum Ausführen von Installationsaufgaben in lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) , um den Pfad des Netzwerkinstallationspunkts anzugeben und eine unbeaufsichtigte Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="83437-110">[Using Config.xml to perform installation tasks in Lync Server 2013](lync-server-2013-using-config-xml-to-perform-installation-tasks.md) to specify the path of the network installation point and perform silent installation.</span></span>

  - <span data-ttu-id="83437-111">[Verwenden Sie die Setup-Befehlszeilenoptionen in lync Server 2013](lync-server-2013-using-setup-command-line-options.md) , um die Config.xml Datei anzugeben, die während der Installation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="83437-111">[Using Setup command-line options in Lync Server 2013](lync-server-2013-using-setup-command-line-options.md) to specify the Config.xml file to use during installation.</span></span>

  - <span data-ttu-id="83437-112">[Konfigurieren von Client-Trap Ping-Richtlinien in lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) mithilfe des MMC-Snap-Ins "Gruppenrichtlinienobjekt-Editor".</span><span class="sxs-lookup"><span data-stu-id="83437-112">[Configuring client bootstrapping policies in Lync Server 2013](lync-server-2013-configuring-client-bootstrapping-policies.md) by using the Group Policy Object Editor MMC snap-in.</span></span>

<span data-ttu-id="83437-113">Bei der Bereitstellung der Office-Produktsuite passen Sie wahrscheinlich noch weitere Optionen für Ihre Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="83437-113">There will probably be other options you’ll want to configure as you deploy the Office suite of products.</span></span> <span data-ttu-id="83437-114">Die Themen in diesem Abschnitt enthalten eine Übersicht über diese Anpassungstools und erläutern lync-spezifische Aspekte.</span><span class="sxs-lookup"><span data-stu-id="83437-114">The topics in this section give an overview of these customization tools and discuss Lync-specific considerations.</span></span> <span data-ttu-id="83437-115">Außerdem finden Sie dort Links zu detaillierter Office-Hilfe für die einzelnen Tools.</span><span class="sxs-lookup"><span data-stu-id="83437-115">Included are links to detailed Office help for each tool.</span></span>

<span data-ttu-id="83437-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="83437-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

