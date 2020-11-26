---
title: 'Lync Server 2013: Reduzieren von nicht angeforderten Chatnachrichten'
description: 'Lync Server 2013: Reduzieren unerwünschter Sofortnachrichten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reducing unsolicited IM for Lync Server 2013
ms:assetid: d2998708-e699-4465-a918-e1d9ea4c49c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn518335(v=OCS.15)
ms:contentKeyID: 62625493
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 294c53a6b82b4dc345fbb9afcf9983d5bd35893a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436671"
---
# <a name="reducing-unsolicited-im-for-lync-server-2013"></a><span data-ttu-id="f5d6e-103">Reduzieren von nicht angeforderten Chatnachrichten für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f5d6e-103">Reducing unsolicited IM for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f5d6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f5d6e-104">

<span> </span></span></span>

<span data-ttu-id="f5d6e-105">_**Letztes Änderungsdatum des Themas:** 2013-12-05_</span><span class="sxs-lookup"><span data-stu-id="f5d6e-105">_**Topic Last Modified:** 2013-12-05_</span></span>

<span data-ttu-id="f5d6e-106">Die intelligente Chat Filter-Anwendung schützt Ihre Microsoft lync Server 2013-Bereitstellung vor den häufigsten Viren mit minimaler Beeinträchtigung der Benutzererfahrung.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-106">The Intelligent IM Filter application helps protect your Microsoft Lync Server 2013 deployment against the most common viruses with minimal degradation to the user experience.</span></span> <span data-ttu-id="f5d6e-107">Der intelligente Chat-Filter bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f5d6e-107">The Intelligent IM Filter provides the following:</span></span>

  - <span data-ttu-id="f5d6e-108">Erweiterte URL-Filterung</span><span class="sxs-lookup"><span data-stu-id="f5d6e-108">Enhanced URL filtering</span></span>

  - <span data-ttu-id="f5d6e-109">Verbesserte Filter für die Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="f5d6e-109">Enhanced file transfer filtering</span></span>

<span data-ttu-id="f5d6e-110">Verwenden Sie den intelligenten Chatfilter, um Filter so zu konfigurieren, dass unerwünschte oder potenziell schädliche Sofortnachrichten von unbekannten Endpunkten außerhalb der Unternehmensfirewall blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-110">Use Intelligent IM Filter to configure filters to block unsolicited or potentially harmful instant messages from unknown endpoints outside the corporate firewall.</span></span> <span data-ttu-id="f5d6e-111">Sie konfigurieren Filter, indem Sie die Kriterien angeben, die verwendet werden sollen, um zu bestimmen, was blockiert werden soll, beispielsweise Sofortnachrichten mit Links und Dateien mit bestimmten Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-111">You configure filters by specifying the criteria to be used to determine what should be blocked, such as instant messages containing hyperlinks and files with specific extensions.</span></span>

<span data-ttu-id="f5d6e-112">Bevor Sie die intelligente Chat-Nachrichten Filter Anwendung bereitstellen, sollten Sie wissen, wie Filteroptionen angewendet werden, wenn Nachrichten von einem lync Server 2013-Server an einen anderen weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-112">Before you deploy the Intelligent IM Message Filter application, you should understand how filtering options are applied when messages are routed from one Lync Server 2013 server to another.</span></span> <span data-ttu-id="f5d6e-113">Die Art und Weise, wie diese Filteroptionen angewendet werden, ist konsistent, unabhängig davon, ob sich die Server in einer einzelnen Organisation oder unternehmensübergreifend befinden.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-113">The way these filtering options are applied is consistent, regardless of whether the servers are located in a single organization or across organizational boundaries.</span></span> <span data-ttu-id="f5d6e-114">Diese Konsistenz bezieht sich auf die Art und Weise, in der benutzerdefinierte Hinweise und Warnungstexte in Nachrichten eingefügt und serverübergreifend gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-114">This consistency applies to the way that the customized notice, and warning texts are inserted into messages and sent across servers.</span></span>

<span data-ttu-id="f5d6e-115">Die empfohlene Filteroption besteht darin, Sofortnachrichten mit Hyperlinks zuzulassen, aber den intelligenten Chat-Filter zum Deaktivieren der Verknüpfung zu erzwingen, indem Sie einen Unterstrich davor einfügen.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-115">The recommended filtering option is to allow instant messages with hyperlinks but require the Intelligent IM Filter to disable the link by inserting an underscore before it.</span></span> <span data-ttu-id="f5d6e-116">Wenn Sie diese Option auswählen, haben Sie die zusätzliche Möglichkeit, eine Benachrichtigung an Benutzer zu verfassen, die am Anfang jeder Chatnachricht angezeigt wird, die einen Link enthält.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-116">If you choose this option, you have the additional option of composing a notice to users that appears at the beginning of each instant message that contains a hyperlink.</span></span>

<span data-ttu-id="f5d6e-117">Eine zweite Filteroption besteht darin, Sofortnachrichten mit nicht geänderten Hyperlinks zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-117">A second filtering option is to allow instant messages with unmodified hyperlinks.</span></span> <span data-ttu-id="f5d6e-118">Wenn Sie diese Option auswählen, haben Sie die zusätzliche Option (empfohlen) zum Verfassen einer Warnung für Benutzer, die in jede Nachricht eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-118">If you choose this option, you have the additional option (recommended) of composing a warning to users that is inserted in each message.</span></span>

<span data-ttu-id="f5d6e-119">Eine dritte Möglichkeit besteht darin, alle Sofortnachrichten, die Links enthalten, zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-119">A third option is to block all instant messages that contain hyperlinks.</span></span> <span data-ttu-id="f5d6e-120">Wenn Sie diese Option auswählen, sendet der Server eine Warnung an den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-120">If you choose this option, the server sends a warning to the user.</span></span> <span data-ttu-id="f5d6e-121">Sie müssen diese Warnung schreiben.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-121">You must write this warning.</span></span>

<span data-ttu-id="f5d6e-122"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f5d6e-122"></div>

<span> </span>

</div>

</div>

</span></span></div>

