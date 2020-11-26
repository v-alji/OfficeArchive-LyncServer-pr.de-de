---
title: Die Skype for Business Online-Bericht Erstellungs-Cmdlets und der übrige Web Service
description: Die Skype for Business Online-Berichterstattungs-Cmdlets und der restliche Webdienst.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: The Skype for Business Online reporting cmdlets and REST web service
ms:assetid: cadd73a7-c08a-4102-b73a-ccb3ad4987bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362845(v=OCS.15)
ms:contentKeyID: 56563409
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f2160e0910d42f811ec8b03fa50450d5f73c59b1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423407"
---
# <a name="the-skype-for-business-online-reporting-cmdlets-and-rest-web-service"></a><span data-ttu-id="77a56-103">Die Skype for Business Online-Bericht Erstellungs-Cmdlets und der übrige Web Service</span><span class="sxs-lookup"><span data-stu-id="77a56-103">The Skype for Business Online reporting cmdlets and REST web service</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77a56-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77a56-104">

<span> </span></span></span>

<span data-ttu-id="77a56-105">_**Letztes Änderungsdatum des Themas:** 2014-09-05_</span><span class="sxs-lookup"><span data-stu-id="77a56-105">_**Topic Last Modified:** 2014-09-05_</span></span>

<span data-ttu-id="77a56-106">In Verbindung mit den Berichterstellungsfeatures bietet Skype for Business Online Zugriff auf fünf Windows PowerShell-Cmdlets, die dazu beitragen, diese Berichte zu generieren, und Sie können auch von Administratoren verwendet werden, um angepasste Berichtsdaten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="77a56-106">In conjunction with the reporting features, Skype for Business Online provides access to five Windows PowerShell cmdlets that help generate those reports and are also can be used by administrators to return customized reporting data.</span></span> <span data-ttu-id="77a56-107">Skype for Business Online enthält auch den anderen (Repräsentations Status Transfer), der von Entwicklern zum Abrufen von benutzerdefinierten Bericht Erstellungsinformationen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="77a56-107">Skype for Business Online also includes the REST (Representational State Transfer), which can be used by developers to retrieve customized reporting information.</span></span>

<span data-ttu-id="77a56-108">Zu den für Administratoren verfügbaren Berichterstattungs-Cmdlets gehören:</span><span class="sxs-lookup"><span data-stu-id="77a56-108">The reporting cmdlets available to administrators include:</span></span>

  - <span data-ttu-id="77a56-109">Get-CsActiveUserReport, das Informationen über die Anzahl aktiver Benutzer enthält (also Benutzer, die sich bei Skype for Business Online angemeldet haben und an mindestens einer Konferenz oder Peer-to-Peer-Kommunikationssitzung teilgenommen haben).</span><span class="sxs-lookup"><span data-stu-id="77a56-109">Get-CsActiveUserReport, which provides information about the number of active users (that is, users who have logged on to Skype for Business Online and participated in at least one conference or peer-to-peer communication session).</span></span>

  - <span data-ttu-id="77a56-110">Get-CsAVConferenceTimeReport bietet Informationen über die Zeitdauer (in Minuten), die Benutzer in Audio-und Videokonferenzen verbracht haben.</span><span class="sxs-lookup"><span data-stu-id="77a56-110">Get-CsAVConferenceTimeReport, which provides information about the amount of time (in minutes) users spent in audio/video conferences.</span></span>

  - <span data-ttu-id="77a56-111">Get-CsConferenceReport, das Informationen über die Anzahl und die Art der Konferenzen enthält, an denen Benutzer teilgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="77a56-111">Get-CsConferenceReport, which provides information about the number and type of conferences that users participated in.</span></span>

  - <span data-ttu-id="77a56-112">Get-CsP2PAVTimeReport bietet Informationen über die Zeitdauer (in Minuten), die Benutzer in Peer-to-Peer-Sitzungen mit Audio und/oder Video verbracht haben.</span><span class="sxs-lookup"><span data-stu-id="77a56-112">Get-CsP2PAVTimeReport, which provides information about the amount of time (in minutes) users spent in peer-to-peer sessions that included audio and/or video.</span></span>

  - <span data-ttu-id="77a56-113">Get-CsP2PSessionReport, das Informationen über die Anzahl und den Typ der Peer-to-Peer-Sitzungen enthält, an denen Benutzer teilgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="77a56-113">Get-CsP2PSessionReport, which provides information about the number and type of peer-to-peer sessions that users participated in.</span></span>

<span data-ttu-id="77a56-114">Die meisten Administratoren verwenden die im Microsoft 365 Admin Center verfügbaren Berichte: Diese Berichte werden nicht nur automatisch generiert, sondern auch eine grafische Darstellung der Daten bereitgestellt, die häufig einfacher zu interpretieren sind als die von den Berichterstattungs-Cmdlets zurückgegebenen unformatierten Zahlenwerte.</span><span class="sxs-lookup"><span data-stu-id="77a56-114">Most administrators will use the reports available in the Microsoft 365 admin center: not only are those reports auto-generated, but they also provide a graphical representation of the data that is often easier to interpret than the raw number values returned by the reporting cmdlets.</span></span> <span data-ttu-id="77a56-115">Administratoren, die mit Windows PowerShell vertraut sind, können jedoch mithilfe der Berichterstattungs-Cmdlets Daten zurückgeben, die in den lync Online-Berichten nicht ohne weiteres verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="77a56-115">However, administrators familiar with Windows PowerShell can use the reporting cmdlets to return data that is not readily available from the Lync Online reports.</span></span> <span data-ttu-id="77a56-116">Beispielsweise geben die Berichterstattungs-Cmdlets Informationen zur Sitzungsdauer zurück (die Zeitdauer in Minuten, zu der jede Sitzung dauerte).</span><span class="sxs-lookup"><span data-stu-id="77a56-116">For example, the reporting cmdlets return information about session duration (the amount of time, in minutes, that each session lasted).</span></span> <span data-ttu-id="77a56-117">Die einzelnen Sitzungs dauern sind mithilfe der lync Online-Berichte nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77a56-117">Individual session durations are not available using the Lync Online reports.</span></span> <span data-ttu-id="77a56-118">In der täglichen Ansicht werden in den lync Online-berichten ebenfalls Informationen nur für die vorhergehenden 14 Tage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77a56-118">Likewise, in daily view the Lync Online reports display information only for the preceding 14 days.</span></span> <span data-ttu-id="77a56-119">Wenn Sie die Tagesergebnisse für einen anderen Tag überprüfen möchten (beispielsweise ein Datum vor vier Monaten), können Sie dies mithilfe der Berichterstattungs-Cmdlets tun.</span><span class="sxs-lookup"><span data-stu-id="77a56-119">If you would like to review the daily totals for a different day (for example, a date from four months ago) you can do so by using the reporting cmdlets.</span></span>

<span data-ttu-id="77a56-120">Administratoren sind möglicherweise auch an dem Artikel [mit Excel zum Abrufen von Office 365-Berichtsdaten](https://msdn.microsoft.com/library/dn781442.aspx)interessiert, in dem erläutert wird, wie Sie das Feature "OData-Datenabfrage" in Microsoft Excel verwenden, um einen benutzerdefinierten Office 365-Bericht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77a56-120">Administrators might also be interested in the article [Using Excel to Retrieve Office 365 Reporting Data](https://msdn.microsoft.com/library/dn781442.aspx), which explains how to use the OData data querying feature in Microsoft Excel to create custom office 365 report.</span></span> <span data-ttu-id="77a56-121">Benutzerdefinierte Berichte bieten Ihnen die Möglichkeit, zu diktieren, welche Daten (und wie viele Daten) vom Office 365-Berichterstattungsdienst zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77a56-121">Custom reports give you the ability to dictate which data (and how much data) is returned from the Office 365 reporting service.</span></span> <span data-ttu-id="77a56-122">Benutzerdefinierte Berichte ermöglichen Ihnen auch, wie Sie angeben, wie die Daten sortiert und gruppiert werden sollen, und bieten Zugriff auf Informationen, die nicht im Admin Center angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77a56-122">Custom reports also enable you to do such things as specify how the data should be sorted and grouped, and provide access to information that is not displayed in the admin center.</span></span>

<span data-ttu-id="77a56-123">Administratoren mit einem Entwicklungshintergrund können mithilfe des RESTful-Webdiensts Informationen abrufen, die nicht im Skype for Business Online Admin Center angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77a56-123">Administrators with a development background can use the REST web service to obtain information not displayed in the Skype for Business Online admin center.</span></span> <span data-ttu-id="77a56-124">Der restliche Dienst ist mit dem SOAP-Dienst vergleichbar, da jede Technologie eine Möglichkeit bietet, XML-Daten zwischen einem Client und einem Server zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="77a56-124">The REST service is similar to the SOAP service, in that each technology provides a way to transfer XML data between a client and a server.</span></span> <span data-ttu-id="77a56-125">Der Service für den Ruhezustand hat jedoch mindestens zwei Vorteile gegenüber dem SOAP-Dienst.</span><span class="sxs-lookup"><span data-stu-id="77a56-125">However, the REST service has at least two advantages over the SOAP service.</span></span> <span data-ttu-id="77a56-126">Zum einen führt Ruhe XML-Datenübertragungen mit einem standardisierten Format aus, das als Atom-Syndication-Format bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="77a56-126">For one, REST performs XML data transfers using a standardized format known as the ATOM syndication format.</span></span> <span data-ttu-id="77a56-127">Im Gegensatz dazu wird SOAP beim Übertragen von Daten mit einem nicht standardmäßigen Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="77a56-127">By contrast, SOAP using a non-standard format when transferring data.</span></span> <span data-ttu-id="77a56-128">Darüber hinaus ist "Ruhe" in der Lage, Daten über Netzwerke zu übertragen, die andere HTTP-Verben als "abrufen" und "Posten" blockieren.</span><span class="sxs-lookup"><span data-stu-id="77a56-128">In addition, REST is able to transfer data across networks that block HTTP verbs other than GET and POST.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="77a56-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77a56-129">See Also</span></span>


<span data-ttu-id="77a56-130">[Lync Online-Berichterstellung](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="77a56-130">[Lync Online reporting](https://technet.microsoft.com/library/dn362827\(v=ocs.15\))</span></span>  


[<span data-ttu-id="77a56-131">Der Office 365-Berichterstellungsdienst</span><span class="sxs-lookup"><span data-stu-id="77a56-131">The Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984325.aspx)  
[<span data-ttu-id="77a56-132">Kennenlernen des Office 365-Berichts-Webdiensts</span><span class="sxs-lookup"><span data-stu-id="77a56-132">Learning About the Office 365 Reporting Web Service</span></span>](https://msdn.microsoft.com/library/office/jj984321.aspx)  
<span data-ttu-id="77a56-133">[Die Exchange Online-Berichterstattungs-Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span><span class="sxs-lookup"><span data-stu-id="77a56-133">[The Exchange Online Reporting Cmdlets](https://technet.microsoft.com/library/jj200780\(v=exchg.150\).aspx)</span></span>  
[<span data-ttu-id="77a56-134">Verwenden von Excel zum Abrufen von Office 365-Berichtsdaten</span><span class="sxs-lookup"><span data-stu-id="77a56-134">Using Excel to Retrieve Office 365 Reporting Data</span></span>](https://msdn.microsoft.com/library/dn781442.aspx)  
  

<span data-ttu-id="77a56-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77a56-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

