---
title: 'Lync Server 2013: Verwenden von Setup-Befehlszeilenoptionen'
description: 'Lync Server 2013: Verwenden der Befehlszeilenoptionen für Setup.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Setup command-line options
ms:assetid: 99878c3c-ff31-48e2-8424-580d7b07a7bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205129(v=OCS.15)
ms:contentKeyID: 48184957
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15c3490ead090766462ce83cb13ffe62355032cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393898"
---
# <a name="using-setup-command-line-options-in-lync-server-2013"></a><span data-ttu-id="9173e-103">Verwenden von Setup-Befehlszeilenoptionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9173e-103">Using Setup command-line options in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9173e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9173e-104">

<span> </span></span></span>

<span data-ttu-id="9173e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="9173e-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="9173e-p101">Die Befehlszeile von "Setup.exe" wird nur für wenige Vorgänge des Office-Setups verwendet. Anstelle der Setup-Befehlszeilenoptionen benutzen Sie in der Regel das Office-Anpassungstool und die Datei "Config.xml", um Produkte einzurichten und Funktionen anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9173e-p101">The Setup.exe command line is used for very few operations in Office setup. Instead of using the Setup command-line options, you’ll typically use the Office Customization Tool and the Config.xml file for product setup and feature customization.</span></span>

<span data-ttu-id="9173e-108">Die Befehlszeile der Office "Setup.exe" erkennt die in der folgenden Tabelle beschriebenen Befehlzeilenoptionen.</span><span class="sxs-lookup"><span data-stu-id="9173e-108">The Office Setup.exe command line recognizes the command-line options described in the following table.</span></span>

### <a name="office-setup-command-line-options"></a><span data-ttu-id="9173e-109">Optionen der Office Setup-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9173e-109">Office Setup Command-Line Options</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9173e-110">Option der Office Setup-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9173e-110">Setup Command-Line Option</span></span></th>
<th><span data-ttu-id="9173e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9173e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9173e-112">/admin</span><span class="sxs-lookup"><span data-stu-id="9173e-112">/admin</span></span></p></td>
<td><p><span data-ttu-id="9173e-113">Führt das Office-Anpassungstool aus, um eine Setupanpassungsdatei (.msp-Datei) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9173e-113">Runs the Office Customization Tool to create a Setup customization file (.msp file).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9173e-114">/adminfile [Pfad]</span><span class="sxs-lookup"><span data-stu-id="9173e-114">/adminfile [path]</span></span></p></td>
<td><p><span data-ttu-id="9173e-p102">Wendet die angegebene Setupanpassungsdatei auf die Installation an. Sie können einen Pfad zu einer bestimmten Anpassungsdatei (.msp-Datei) oder zu dem Ordner angeben, in dem Sie Anpassungsdateien speichern.</span><span class="sxs-lookup"><span data-stu-id="9173e-p102">Applies the specified Setup customization file to the installation. You can specify a path of a specific customization file (.msp file) or to the folder where you store customization files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9173e-117">/config [Pfad]</span><span class="sxs-lookup"><span data-stu-id="9173e-117">/config [path]</span></span></p></td>
<td><p><span data-ttu-id="9173e-118">Gibt die Config.xml Datei an, die von Setup während der Installation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9173e-118">Specifies the Config.xml file that Setup uses during the installation.</span></span> <span data-ttu-id="9173e-119">Verwenden Sie die/config-Option, um die Config.xml Datei anzugeben, die Sie für lync 2013-Installationen angepasst haben, beispielsweise: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span><span class="sxs-lookup"><span data-stu-id="9173e-119">Use the /config option to specify the Config.xml file you customized for Lync 2013 installations, for example: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9173e-120">/Modify lync</span><span class="sxs-lookup"><span data-stu-id="9173e-120">/modify Lync</span></span></p></td>
<td><p><span data-ttu-id="9173e-121">Wird mit einer geänderten config.xml-Datei verwendet, um Setup im Wartungsmodus auszuführen und Änderungen an einer vorhandenen Office-Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="9173e-121">Used with a modified Config.xml file to run Setup in maintenance mode and make changes to an existing Office installation.</span></span> <span data-ttu-id="9173e-122">So können Sie beispielsweise die Option/MODIFY verwenden, um lync-Features hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9173e-122">For example, you can use the /modify option to add or remove Lync features.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9173e-123">/Repair lync</span><span class="sxs-lookup"><span data-stu-id="9173e-123">/repair Lync</span></span></p></td>
<td><p><span data-ttu-id="9173e-124">Führt das Setup auf dem Computer des Benutzers aus, um lync zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="9173e-124">Runs Setup from the user’s computer to repair Lync.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9173e-125">/Uninstall lync</span><span class="sxs-lookup"><span data-stu-id="9173e-125">/uninstall Lync</span></span></p></td>
<td><p><span data-ttu-id="9173e-126">Führt das Setup aus, um lync vom Computer des Benutzers zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9173e-126">Runs Setup to remove Lync from the user’s computer.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9173e-127">Ausführliche Informationen zur Verwendung der Befehlszeilenoptionen für Setup finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=267515> .</span><span class="sxs-lookup"><span data-stu-id="9173e-127">For details about using the setup command-line options, see <https://go.microsoft.com/fwlink/p/?linkid=267515>.</span></span>

<span data-ttu-id="9173e-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9173e-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

