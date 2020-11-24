---
title: 'Lync Server 2013: Verwenden des Office-Anpassungstools (OAT)'
description: 'Lync Server 2013: Verwenden des Office-Anpassungstools (OAT)'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Office Customization Tool (OCT)
ms:assetid: 26647cb6-ba84-4ba7-8b6f-2cf86818e530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204748(v=OCS.15)
ms:contentKeyID: 48183654
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 602502ba4579ed6c640eee909d4c6b056ce247d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395274"
---
# <a name="using-the-office-customization-tool-oct-in-lync-server-2013"></a><span data-ttu-id="d3b2f-103">Verwenden des Office-Anpassungstools (OAT) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3b2f-103">Using the Office Customization Tool (OCT) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3b2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3b2f-104">

<span> </span></span></span>

<span data-ttu-id="d3b2f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="d3b2f-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="d3b2f-106">Das Office-Anpassungstool (OAT) ist Teil des Setup-Programms und wird als Tool für viele Anpassungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-106">The Office Customization Tool (OCT) is part of the Setup program and is the recommended tool for many customizations.</span></span> <span data-ttu-id="d3b2f-107">Wenn Sie das OAT verwenden, passen Sie Office an, und speichern Sie Ihre Anpassungen in einer MSP-Datei für die Setup Anpassung.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-107">By using the OCT, you customize Office and save your customizations in a Setup customization .msp file.</span></span> <span data-ttu-id="d3b2f-108">Sie fügen die Datei im Ordner Updates auf dem Netzwerkinstallationspfad ein.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-108">You place the file in the Updates folder on the network installation point.</span></span> <span data-ttu-id="d3b2f-109">Wenn Sie Office installieren, sucht Setup im Ordner Updates nach einer Setupanpassungsdatei und wendet die Anpassungen an.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-109">When you install Office, Setup looks for a Setup customization file in the Updates folder and applies the customizations.</span></span> <span data-ttu-id="d3b2f-110">Der Ordner Updates kann nur zum Bereitstellen von Softwareupdates während einer Erstinstallation von Office 2013 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-110">The Updates folder can be used only to deploy software updates during an initial installation of Office 2013.</span></span>

<span data-ttu-id="d3b2f-111">Das OAT ist Teil des Setups und in Volumenlizenzversionen des Produkts enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-111">The OCT is part of setup and it is included in volume license versions of the product.</span></span> <span data-ttu-id="d3b2f-112">Sie führen das OAT durch Eingabe über `setup.exe /admin` die Befehlszeile aus dem Stammverzeichnis des Netzwerkinstallationspfads, der die Office 2013-Quelldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-112">You run the OCT by typing `setup.exe /admin` at the command line from the root of the network installation point that contains the Office 2013 source files.</span></span> <span data-ttu-id="d3b2f-113">Verwenden Sie beispielsweise folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="d3b2f-113">For example, use the following:</span></span>

`\\server\share\Office15\setup.exe /admin`

<span data-ttu-id="d3b2f-114">Administratoren verwenden das OAT zum Erstellen einer Setupanpassungsdatei (MSP-Datei).</span><span class="sxs-lookup"><span data-stu-id="d3b2f-114">Administrators use the OCT to create a setup customization .msp file.</span></span> <span data-ttu-id="d3b2f-115">Wie im Microsoft Office 2010 Oct können Administratoren die folgenden Bereiche anpassen:</span><span class="sxs-lookup"><span data-stu-id="d3b2f-115">As in the Microsoft Office 2010 OCT, administrators can customize the following areas:</span></span>

  - <span data-ttu-id="d3b2f-116">**Einrichtung** Dient zum Angeben des Standard Installationsspeicherorts auf dem Client und dem Standard Organisationsnamen, zusätzliche Netzwerkinstallationsquellen, Product Key, Endbenutzer-Lizenzvertrag, Anzeigeebene, zu entfernende frühere Versionen von Office, benutzerdefinierte Programme, die während der Installation, Sicherheitseinstellungen und Setup Eigenschaften ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-116">**Setup** Used to specify default installation location on the client and default organization name, additional network installation sources, product key, end-user license agreement, display level, earlier versions of Office to remove, custom programs to run during installation, security settings, and Setup properties.</span></span>

  - <span data-ttu-id="d3b2f-117">**Funktionen** Wird verwendet, um Benutzereinstellungen zu konfigurieren und die Installation von Office-Features anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-117">**Features** Used to configure user settings and to customize how Office features are installed.</span></span> <span data-ttu-id="d3b2f-118">Administratoren können das OAT verwenden, um anfängliche Standardwerte für die Office-Anwendungseinstellungen für Benutzer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-118">Administrators can use the OCT to specify initial default values of Office application settings for users.</span></span> <span data-ttu-id="d3b2f-119">Benutzer können die meisten Einstellungen nach der Installation ändern.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-119">Users can modify most of the settings after the installation.</span></span>

  - <span data-ttu-id="d3b2f-120">**Zusätzlicher Inhalt** Wird zum Hinzufügen oder Entfernen von Dateien, hinzufügen oder Entfernen von Registrierungseinträgen und Konfigurieren von Tastenkombinationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-120">**Additional content** Used to add or remove files, add or remove registry entries, and configure shortcuts.</span></span>

  - <span data-ttu-id="d3b2f-121">**Outlook** Wird verwendet, um das standardmäßige Outlook-Profil eines Benutzers anzupassen, Exchange-Einstellungen anzugeben, Konten hinzuzufügen, Konten zu entfernen und Einstellungen zu exportieren sowie Senden von \\ Empfangs Gruppen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d3b2f-121">**Outlook** Used to customize a user's default Outlook profile, specify Exchange settings, add accounts, remove accounts and export settings, and specify Send\\Receive groups.</span></span>

<span data-ttu-id="d3b2f-122">Informationen zum OAT finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=267516> .</span><span class="sxs-lookup"><span data-stu-id="d3b2f-122">For information about the OCT, see <https://go.microsoft.com/fwlink/p/?linkid=267516>.</span></span>

<span data-ttu-id="d3b2f-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3b2f-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

