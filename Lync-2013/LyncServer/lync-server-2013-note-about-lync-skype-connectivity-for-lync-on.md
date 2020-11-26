---
title: 'Lync Server 2013: Hinweis zu Lync-Skype Konnektivität für lync auf'
description: 'Lync Server 2013: Hinweis zu Lync-Skype Konnektivität für lync auf.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Note about Lync-Skype connectivity for Lync On
ms:assetid: 1d0f5c1a-74c6-468f-9877-ad2b1ddf355f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440169(v=OCS.15)
ms:contentKeyID: 57793359
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f7d9758f277f2f987677c2c0ffa0a4447ba31d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424975"
---
# <a name="note-about-lync-skype-connectivity-in-lync-server-2013-for-lync-online-customers"></a><span data-ttu-id="faf4a-103">Hinweis zu Lync-Skype Konnektivität in lync Server 2013 für lync Online-Kunden</span><span class="sxs-lookup"><span data-stu-id="faf4a-103">Note about Lync-Skype connectivity in Lync Server 2013 for Lync Online customers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faf4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faf4a-104">

<span> </span></span></span>

<span data-ttu-id="faf4a-105">_**Letztes Änderungsdatum des Themas:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="faf4a-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="faf4a-106">Dieses Dokument wurde geschrieben, um lync Server-Administratoren bei der Einrichtung Lync-Skype Konnektivität zu helfen.</span><span class="sxs-lookup"><span data-stu-id="faf4a-106">This document was written to help Lync Server on-premise administrators set up Lync-Skype connectivity.</span></span>  <span data-ttu-id="faf4a-107">Lync-Skype Konnektivität ist auch eine Funktion von lync Online, die Bestandteil von Office 365 und Microsoft 365 ist.</span><span class="sxs-lookup"><span data-stu-id="faf4a-107">Lync-Skype connectivity is also a feature of Lync Online, which is part of Office 365 and Microsoft 365.</span></span> <span data-ttu-id="faf4a-108">Sie können das Feature Lync-Skype Konnektivität über die lync-Verwaltungskonsole innerhalb des Admin Centers aktivieren.</span><span class="sxs-lookup"><span data-stu-id="faf4a-108">You can enable the Lync-Skype connectivity feature from the Lync Administration Center within the admin center.</span></span>

<span data-ttu-id="faf4a-109">Für Microsoft 365 mittelständische Unternehmen, Office 365 Enterprise, Microsoft 365 Education und Office 365 für Government: Sie können sich beim Office 365-Portal oder im Microsoft 365 Admin Center anmelden und zur **lync-Verwaltungskonsole** navigieren.</span><span class="sxs-lookup"><span data-stu-id="faf4a-109">For Microsoft 365 Midsize Business, Office 365 Enterprise, Microsoft 365 Education, and Office 365 for Government: Sign in to the Office 365 portal or Microsoft 365 admin center and navigate to the **Lync Administration Center**.</span></span> <span data-ttu-id="faf4a-110">Wechseln Sie zu **externe Kommunikation**.</span><span class="sxs-lookup"><span data-stu-id="faf4a-110">Go to **External Communications**.</span></span> <span data-ttu-id="faf4a-111">Klicken Sie unter **Dienstanbieter für öffentliche Chats** auf **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="faf4a-111">Under **Public IM Service Providers**, click **Enable**.</span></span> <span data-ttu-id="faf4a-112">Wenn Sie den Zugriff einzelner Benutzer auf Lync-Skype Konnektivität steuern möchten, können Sie dies tun, indem Sie die Einstellungen für die externe Kommunikation einzelner Benutzer bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="faf4a-112">If you want to control individual user access to Lync-Skype Connectivity, you can do so by editing individual users’ External Communications settings.</span></span>

<span data-ttu-id="faf4a-113">Für Microsoft 365 Small Business Premium: Anmelden bei Microsoft 365 und wechseln zu den **Administrator \> Diensteinstellungen \> Chat, Besprechungen und Konferenzen**.</span><span class="sxs-lookup"><span data-stu-id="faf4a-113">For Microsoft 365 Small Business Premium: Sign in to Microsoft 365, and go to **Admin \> Service Settings \> Instant messaging, meetings and conferencing**.</span></span> <span data-ttu-id="faf4a-114">Aktivieren Sie „Externe Kommunikation“.</span><span class="sxs-lookup"><span data-stu-id="faf4a-114">Turn on External communications.</span></span> <span data-ttu-id="faf4a-115">Der Schalter für externe Kommunikation aktiviert sowohl die Lync-Skype Konnektivität als auch die Kommunikation mit anderen Organisationen, die lync verwenden.</span><span class="sxs-lookup"><span data-stu-id="faf4a-115">The External communications switch turns on both Lync-Skype connectivity and communications with other organizations that use Lync.</span></span> <span data-ttu-id="faf4a-116">Je nachdem, wann Sie mit der Verwendung von lync Online begonnen haben, kann der Schalter für externe Kommunikation in einem "ein"-Zustand zunächst nur angeben, dass die Kommunikation mit anderen lync-Organisationen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="faf4a-116">Depending on when you started using Lync Online, the External communications switch in an "on" state may initially indicate only that communications with other Lync organizations is activated.</span></span> <span data-ttu-id="faf4a-117">Wenn Sie Lync-Skype Konnektivität aktivieren möchten, schalten Sie den Schalter einfach aus und wieder ein.</span><span class="sxs-lookup"><span data-stu-id="faf4a-117">To turn on Lync-Skype Connectivity, simply toggle the switch off and then back on again.</span></span>

<span data-ttu-id="faf4a-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faf4a-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

