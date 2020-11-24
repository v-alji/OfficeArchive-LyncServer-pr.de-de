---
title: 'Lync Server 2013: Einrichten eines Sicherungsspeicherorts'
description: 'Lync Server 2013: Einrichten eines Sicherungsspeicherorts.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up a backup location
ms:assetid: 006732eb-3d44-414d-8010-227a855caa93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202158(v=OCS.15)
ms:contentKeyID: 51541440
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 344baea1b7e51454bb28d31d88451d29fd6aa3a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394962"
---
# <a name="setting-up-a-backup-location-for-lync-server-2013"></a><span data-ttu-id="da88c-103">Einrichten eines Sicherungsspeicherorts für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="da88c-103">Setting up a backup location for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="da88c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="da88c-104">

<span> </span></span></span>

<span data-ttu-id="da88c-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="da88c-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="da88c-106">Bevor Sie die erste Sicherung von lync Server durchführen, richten Sie die Hardware und Software ein, die Sie benötigen, um die Sicherungen zu speichern und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="da88c-106">Before you take your first backup of Lync Server, set up the hardware and software that you need in order to store and maintain the backups.</span></span> <span data-ttu-id="da88c-107">Sie müssen je nach Bedarf Zugriff auf die Medien und Inhalte erhalten und die Netzwerkkonnektivität zwischen den einzelnen zu sichernden Servern und den Sicherungsmedien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="da88c-107">You need to obtain access to the media and content, as appropriate, and provide network connectivity between each server to be backed up and the backup media.</span></span> <span data-ttu-id="da88c-108">Die von Ihnen verwendeten Medien und Standorte sollten in ihrer Sicherungs-und Wiederherstellungsstrategie definiert werden.</span><span class="sxs-lookup"><span data-stu-id="da88c-108">The media and location that you use should be defined in your backup and restoration strategy.</span></span> <span data-ttu-id="da88c-109">Der Speicherort, den Sie für reguläre Sicherungen verwenden, kann lokal oder Remote sein, aber er muss sicher sein, und er muss für die Sicherung und Wiederherstellung zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="da88c-109">The location that you use for regular backups can be local or remote, but it must be secure, and it must be accessible for both backup and restoration.</span></span> <span data-ttu-id="da88c-110">Wir empfehlen, einen Remotestandort zu verwenden, um vor einem katastrophalen Ereignis an Ihrem primären Standort zu schützen.</span><span class="sxs-lookup"><span data-stu-id="da88c-110">We recommend using a remote location to protect against a catastrophic event at your primary site.</span></span>

<span data-ttu-id="da88c-111">Nachdem Sie die einzelnen Komponenten eingerichtet und getestet haben, überprüfen Sie die Barrierefreiheit der Sicherungen auf den einzelnen Servern.</span><span class="sxs-lookup"><span data-stu-id="da88c-111">After you set up and test the individual components, verify accessibility to the backups from each server.</span></span>

<span data-ttu-id="da88c-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="da88c-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

