---
title: 'Lync Server 2013: Übersicht über die lync Server-Hybridumgebung'
description: 'Lync Server 2013: Übersicht über die lync Server-Hybridumgebung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Lync Server 2013 hybrid environment
ms:assetid: 0d16ec3a-28f0-4483-96e7-8e68f30398fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204669(v=OCS.15)
ms:contentKeyID: 48183399
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 95b0ae433dafad349d7ef9b6328e43dbc308579c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445043"
---
# <a name="overview-of-the-lync-server-2013-hybrid-environment"></a><span data-ttu-id="05c0f-103">Übersicht über die lync Server 2013-Hybridumgebung</span><span class="sxs-lookup"><span data-stu-id="05c0f-103">Overview of the Lync Server 2013 hybrid environment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="05c0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="05c0f-104">

<span> </span></span></span>

<span data-ttu-id="05c0f-105">_**Letztes Änderungsdatum des Themas:** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="05c0f-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="05c0f-106">Die lync Server 2013-Hybridumgebung bezieht sich auf eine Bereitstellung, in der einige Benutzer mit dem lokalen lync Server 2013 und anderen Benutzern in lync Online vernetzt sind, Benutzer jedoch dieselbe Domäne wie user@contoso.com verwenden.</span><span class="sxs-lookup"><span data-stu-id="05c0f-106">Lync Server 2013 hybrid environment refers to a deployment in which there are some users homed to the on-premises Lync Server 2013 and other users homed to Lync Online, but users share the same domain, such as user@contoso.com.</span></span>

<div>

## <a name="about-this-guide"></a><span data-ttu-id="05c0f-107">Informationen zu diesem Leitfaden</span><span class="sxs-lookup"><span data-stu-id="05c0f-107">About this Guide</span></span>

<span data-ttu-id="05c0f-108">In diesem Leitfaden werden die Aufgaben beschrieben, die erforderlich sind, um Ihre lync Server 2013-Umgebung für die Interoperabilität mit lync online zu konfigurieren und dann Benutzer aus Ihrer lokalen Bereitstellung in die Verwendung von lync online zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="05c0f-108">This guide describes the tasks necessary to configure your Lync Server 2013 environment for interoperability with Lync Online, and then to move users from your on-premises deployment to use Lync Online.</span></span>

</div>

<div>

## <a name="prerequisites"></a><span data-ttu-id="05c0f-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="05c0f-109">Prerequisites</span></span>

<span data-ttu-id="05c0f-110">Sie müssen die folgenden Anwendungen und Dienstprogramme installiert haben, um die Aufgaben für die Konfiguration einer Bereitstellung für Hybrid abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="05c0f-110">You will need to have the following applications and utilities installed to complete the tasks for configuring a deployment for hybrid.</span></span> <span data-ttu-id="05c0f-111">Die Installationsprogramme für diese Dateien sind auf den für Ihre Bereitstellung bereitgestellten Installationsmedien sowie auf den Links in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="05c0f-111">The installers for these files are included on the installation media provided for your deployment, as well as at the links included in the following list.</span></span>

  - [<span data-ttu-id="05c0f-112">Active Directory-Verbunddienste (AD FS) 2,0</span><span class="sxs-lookup"><span data-stu-id="05c0f-112">Active Directory Federation Services (AD FS) 2.0</span></span>](https://go.microsoft.com/fwlink/p/?linkid=257305)

  - [<span data-ttu-id="05c0f-113">Microsoft-Verzeichnis Synchronisierungs Tool 9,1</span><span class="sxs-lookup"><span data-stu-id="05c0f-113">Microsoft Directory Synchronization Tool 9.1</span></span>](https://go.microsoft.com/fwlink/p/?linkid=257307)

  - [<span data-ttu-id="05c0f-114">Installieren von Windows PowerShell für einmaliges Anmelden mit AD FS</span><span class="sxs-lookup"><span data-stu-id="05c0f-114">Install Windows PowerShell for single sign-on with AD FS</span></span>](https://go.microsoft.com/fwlink/p/?linkid=398710)

  - <span data-ttu-id="05c0f-115">Der Microsoft Online Services-Anmelde Assistent (msoidcli-7.0.msi) ist im Desktop-Setup für Microsoft 365 enthalten, das über die Download Seite mit dem Microsoft 365 Admin Center abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="05c0f-115">Microsoft Online Services Sign-in Assistant (msoidcli-7.0.msi) is included with the Desktop Setup for Microsoft 365, which can be obtained from the Downloads page linked to from the Microsoft 365 admin center.</span></span>

</div>

<div>

## <a name="administrator-credentials"></a><span data-ttu-id="05c0f-116">Administrator Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="05c0f-116">Administrator Credentials</span></span>

<span data-ttu-id="05c0f-117">Wenn Sie aufgefordert werden, Ihre Administratoranmeldeinformationen anzugeben, verwenden Sie den Benutzernamen und das Kennwort für das Administratorkonto für Ihre Microsoft 365-oder Office 365-Organisation.</span><span class="sxs-lookup"><span data-stu-id="05c0f-117">When you are asked to provide your administrator credentials, use the username and password for the administrator account for your Microsoft 365 or Office 365 organization.</span></span> <span data-ttu-id="05c0f-118">Sie verwenden diese Anmeldeinformationen auch, wenn Sie Active Directory-Verbunddienste (AD FS) 2,0, Verzeichnissynchronisierung, einmaliges Anmelden, Föderation und Verschieben von Benutzern nach lync Online konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="05c0f-118">You will also use these credentials when you configure Active Directory Federation Services (AD FS) 2.0, Directory Synchronization, Single sign-on, federation, and moving users to Lync Online.</span></span>

</div>

<div>

## <a name="connecting-to-lync-online-powershell"></a><span data-ttu-id="05c0f-119">Herstellen einer Verbindung mit lync Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="05c0f-119">Connecting to Lync Online PowerShell</span></span>

<span data-ttu-id="05c0f-120">Administratoren haben jetzt die Möglichkeit, Windows PowerShell zum Verwalten von lync Online und ihren lync Online-Benutzerkonten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="05c0f-120">Administrators now have the ability to use Windows PowerShell to manage Lync Online and their Lync Online user accounts.</span></span> <span data-ttu-id="05c0f-121">Dazu müssen Sie zuerst das lync Online Connector-Modul aus dem Microsoft Download Center herunterladen und installieren ( https://go.microsoft.com/fwlink/?LinkId=294688) .</span><span class="sxs-lookup"><span data-stu-id="05c0f-121">To do this, you must first download and install the Lync Online Connector Module from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=294688).</span></span> <span data-ttu-id="05c0f-122">Weitere Informationen zum herunterladen, installieren und Verwenden des lync Online-Connector-Moduls sowie ausführliche Informationen zur Verwendung von Windows PowerShell zum Verwalten von lync Online finden Sie unter [Verwenden von Windows PowerShell zum Verwalten von lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="05c0f-122">For more information on downloading, installing, and using the Lync Online Connector Module, and for detailed information on using Windows PowerShell to manage Lync Online, see [Using Windows PowerShell to manage Lync Online](https://docs.microsoft.com/SkypeForBusiness/set-up-your-computer-for-windows-powershell/set-up-your-computer-for-windows-powershell).</span></span>

<span data-ttu-id="05c0f-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="05c0f-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

