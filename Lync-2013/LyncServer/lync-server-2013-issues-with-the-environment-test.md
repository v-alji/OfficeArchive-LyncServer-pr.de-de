---
title: 'Lync Server 2013: Probleme mit dem Umgebungs Test'
description: 'Lync Server 2013: Probleme mit dem Umgebungs Test.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Issues with the environment test
ms:assetid: ff1fe0d3-35b2-41ef-87e7-6a61e9e1d2ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205421(v=OCS.15)
ms:contentKeyID: 48185970
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 551d7e914480e178e0558c1d17eefcf060c0688e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426718"
---
# <a name="issues-with-the-environment-test-in-lync-server-2013"></a><span data-ttu-id="c13cd-103">Probleme mit dem Umgebungs Test in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c13cd-103">Issues with the environment test in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c13cd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c13cd-104">

<span> </span></span></span>

<span data-ttu-id="c13cd-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="c13cd-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="c13cd-106">Bewährte Methoden Analyzer bietet eine Möglichkeit, um zu überprüfen, ob Ihre lync Server 2013-Umgebung eine unterstützte Konfiguration ist.</span><span class="sxs-lookup"><span data-stu-id="c13cd-106">Best Practices Analyzer provides a way for you to verify that your Lync Server 2013 environment is a supported configuration.</span></span> <span data-ttu-id="c13cd-107">Im Rahmen der Active Directory-Domänendienst Überprüfung führt Best Practices Analyzer folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="c13cd-107">As part of the Active Directory Domain Services check, Best Practices Analyzer does the following:</span></span>

  - <span data-ttu-id="c13cd-108">Überprüft die Active Directory-Domänendienste-Gesamtstruktur und die Schemavorbereitung.</span><span class="sxs-lookup"><span data-stu-id="c13cd-108">Verifies the Active Directory Domain Services forest and schema preparation.</span></span>

  - <span data-ttu-id="c13cd-109">Gibt die Anzahl der Active Directory-Domänendienste-Websites und-Domänen in der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="c13cd-109">Identifies the number of Active Directory Domain Services sites and domains in the deployment.</span></span>

  - <span data-ttu-id="c13cd-110">Überprüft die Gesamtstruktur und die Domänenebenen.</span><span class="sxs-lookup"><span data-stu-id="c13cd-110">Checks the forest and domain levels.</span></span>

  - <span data-ttu-id="c13cd-111">Überprüft die Version des Domänencontrollers.</span><span class="sxs-lookup"><span data-stu-id="c13cd-111">Checks the domain controller version.</span></span>

  - <span data-ttu-id="c13cd-112">Identifiziert den Domänen-, Konfigurations-und Schemanamenskontext.</span><span class="sxs-lookup"><span data-stu-id="c13cd-112">Identifies the domain, configuration, and schema naming context.</span></span>

  - <span data-ttu-id="c13cd-113">Gibt die Anzahl der aktivierten Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="c13cd-113">Identifies the number of enabled users.</span></span>

  - <span data-ttu-id="c13cd-114">Überprüft, wo die globalen Einstellungen für Active Directory-Domänendienste gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c13cd-114">Checks where the global Active Directory Domain Services settings are stored.</span></span>

  - <span data-ttu-id="c13cd-115">Überprüft, ob die Dienstverbindungspunkte für lync Server SKP sind.</span><span class="sxs-lookup"><span data-stu-id="c13cd-115">Checks for the service connection points (SCPs) for Lync Server.</span></span>

  - <span data-ttu-id="c13cd-116">Identifiziert die Datenbankversion.</span><span class="sxs-lookup"><span data-stu-id="c13cd-116">Identifies the database version.</span></span>

<div>

## <a name="resolving-issues-with-the-environment"></a><span data-ttu-id="c13cd-117">Beheben von Problemen mit der Umgebung</span><span class="sxs-lookup"><span data-stu-id="c13cd-117">Resolving Issues with the Environment</span></span>

<span data-ttu-id="c13cd-118">Wenn der Umgebungs Test Probleme mit Ihrer Umgebung gefunden hat, werden diese Probleme wahrscheinlich durch Probleme mit Ihrer Active Directory-Konfiguration oder der Softwareebene verursacht, die auf bestimmten Servern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c13cd-118">If the environment test found problems with your environment, these problems are probably caused by issues with your Active Directory configuration or the level of software running on specific servers.</span></span> <span data-ttu-id="c13cd-119">Wenn beispielsweise Best Practices Analyzer alle Domänencontroller in Ihrer Umgebung identifiziert, die Windows Server 2000 ausführen, wird eine Warnung ausgegeben, und Sie müssen diese Domänencontroller auf eine unterstützte Version von Windows Server aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c13cd-119">For example, if Best Practices Analyzer identifies any domain controllers in your environment that are running Windows Server 2000, it will issue a warning and you will need to upgrade those domain controllers to a supported version of Windows Server.</span></span>

<span data-ttu-id="c13cd-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c13cd-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

