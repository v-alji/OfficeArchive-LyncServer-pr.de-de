---
title: 'Lync Server 2013: IP Phone-Inventurbericht'
description: 'Lync Server 2013: IP Phone-Inventurbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP Phone Inventory Report
ms:assetid: aa7d6b31-cb09-4e68-b020-aa5dd0081c20
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615027(v=OCS.15)
ms:contentKeyID: 48185044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3bc05017775ad64e0e18f876215aa2c6b3882bd7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426739"
---
# <a name="ip-phone-inventory-report-in-lync-server-2013"></a><span data-ttu-id="6619a-103">Bericht zum IP Phone-Inventar in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6619a-103">IP Phone Inventory Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6619a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6619a-104">

<span> </span></span></span>

<span data-ttu-id="6619a-105">_**Letztes Änderungsdatum des Themas:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="6619a-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="6619a-p101">Der Bericht für den IP-Telefonbestand enthält Informationen zu den IP-Telefonen, die derzeit in der Organisation verwendet werden. Er umfasst eine detaillierte Liste der IP-Telefone, die während des angegebenen Berichtszeitraums tatsächlich verwendet wurden. Mithilfe dieses Berichts können Administratoren unter anderem Informationen dazu erhalten, ob alte oder veraltete Telefone vorhanden sind, die ausgetauscht werden sollten. Zudem können Administratoren darauf hingewiesen werden, dass in der Organisation teure Telefone existieren, die kaum verwendet werden. Solche Informationen können außerordentlich wertvoll sein, wenn es darum geht, neue Telefone zu kaufen oder vorhandene Telefone neu zu verteilen. (Ein Benutzer, der sein teures Telefon selten nutzt, kann beispielsweise gebeten werden, sein Telefon mit einem Benutzer zu tauschen, der sein Telefon häufiger verwendet.)</span><span class="sxs-lookup"><span data-stu-id="6619a-p101">The IP Phone Inventory Report reports information about the IP phones currently in use in your organization. The IP Inventory Report provides a detailed list of the IP phones that were actually used during the specified reporting period. Among other things, this report lets administrators know if there are any old, outdated phones still in use that should be replaced; it can also alert administrators to the fact that there are expensive phones in the organization that are rarely being used. That type of information can be invaluable when it comes time to purchase new phones or to redistribute existing phones. (For example, a user who rarely uses his or her expensive phone might be asked to swap phones with a user who uses his or her phone much more frequently.)</span></span>

<span data-ttu-id="6619a-111">Es sollte beachtet werden, dass dieser Bericht einige Einschränkungen hat, wenn er als echter Inventarbericht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6619a-111">It should be noted that this report does have a few limitations when it comes to being used as a true inventory report.</span></span> <span data-ttu-id="6619a-112">Zum einen listet der Bericht IP Phone einfach alle Telefone auf, die sich während des angegebenen Zeitraums bei lync Server angemeldet haben, sortiert nach der letzten Anmeldezeit.</span><span class="sxs-lookup"><span data-stu-id="6619a-112">For one thing, the IP Phone Report simply lists all the phones that logged on to Lync Server during the specified time period, sorted by their last logon time.</span></span> <span data-ttu-id="6619a-113">Wenn sich ein Telefon während des angegebenen Zeitraums nicht anmeldet, wird es im Inventurbericht nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6619a-113">If a phone did not log on during the specified time period then it will not be listed in the inventory report.</span></span> <span data-ttu-id="6619a-114">Dazu gehören Telefone, die sich vor dem Start des Zeitraums anmeldeten und noch während des angegebenen Zeitintervalls angemeldet waren.</span><span class="sxs-lookup"><span data-stu-id="6619a-114">That includes phones that logged on before the time period started and were still logged on during the specified time interval.</span></span> <span data-ttu-id="6619a-115">Angenommen, Sie möchten die gesamte Telefon Inventur für Juli, 2012, sehen.</span><span class="sxs-lookup"><span data-stu-id="6619a-115">For example, suppose you wanted to look at all the phone inventory for July, 2012.</span></span> <span data-ttu-id="6619a-116">Angenommen, dass mehrere Telefone am lync Server am 30. Juni 2012 angemeldet und noch am 1. Juli angemeldet waren.</span><span class="sxs-lookup"><span data-stu-id="6619a-116">Suppose, as well, that several phones logged on to Lync Server on June 30, 2012 and were still logged on as of July 1st.</span></span> <span data-ttu-id="6619a-117">Diese Telefone werden im Inventarbericht für den 1. Juli nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6619a-117">Those phones will not show up on the inventory report for July 1st.</span></span>

<span data-ttu-id="6619a-118">Beachten Sie auch, dass der Inventurbericht Telefone enthalten kann, die in Ihrer Organisation nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6619a-118">It's also important to note that the inventory report could include phones that your organization no longer uses.</span></span> <span data-ttu-id="6619a-119">Nehmen wir beispielsweise an, dass eine Reihe von Fabrikam-Telefonen am System am 1. Juli 2012 angemeldet sind. fünf Tage später hat Ihre Organisation alle diese Fabrikam-Telefone entfernt und durch ein neues Contoso-Modell ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6619a-119">For example, suppose a number of Fabrikam phones logged on to the system on July 1, 2012; 5 days later your organization got rid of all those Fabrikam phones and replaced them with a newer Contoso model.</span></span> <span data-ttu-id="6619a-120">Die Fabrikam-Telefone werden nach wie vor im Bericht "Inventar" angezeigt, nur weil Sie sich im Laufe des Monats Juli am System angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="6619a-120">The Fabrikam phones will still appear on the "inventory" report simply because they logged on to the system during the month of July.</span></span>

<span data-ttu-id="6619a-p104">Darüber hinaus werden im Bericht für den IP-Telefonbestand keine zusammenfassenden Gesamtzahlen für die verschiedenen Telefontypen angegeben. Nehmen wir beispielsweise an, Sie besitzen 105 Telefone vom Typ Polycom CX600. Aus dem Bericht wird nicht ersichtlich, dass Sie 105 solcher Telefone haben. Stattdessen sehen Sie lediglich 105 separate Einträge für das Modell Polycom Cx600. Die einzige Möglichkeit, um herauszufinden, dass für das Modell Polycom Cx600 105 Einträge vorliegen, besteht darin, diese Einträge manuell zu zählen.</span><span class="sxs-lookup"><span data-stu-id="6619a-p104">In addition, the IP Phone Inventory Report does not report summary totals for the different types of phones. For example, suppose you have 105 Polycom CX600 phones. The report will not tell you that you have 105 of these phones; instead, you will simply see 105 separate entries for the Polycom Cx600. The only way to know that there are 105 entries for the Polycom Cx600 would be to count each of those entries manually.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="6619a-125">Alternativ dazu können Sie die Daten exportieren und die Zählung in Microsoft Excel oder Windows PowerShell vornehmen.</span><span class="sxs-lookup"><span data-stu-id="6619a-125">Or, export the data and use Microsoft Excel or Windows PowerShell to do that counting for you.</span></span>



</div>

<div>

## <a name="accessing-the-ip-phone-inventory-report"></a><span data-ttu-id="6619a-126">Zugreifen auf den Bericht für den IP-Telefonbestand</span><span class="sxs-lookup"><span data-stu-id="6619a-126">Accessing the IP Phone Inventory Report</span></span>

<span data-ttu-id="6619a-p105">Der Zugriff auf den Bericht für den IP-Telefonbestand erfolgt über die Startseite der Überwachungsberichte. Wenn Sie auf die Metrik „Benutzer-URI“ klicken, können Sie auf den Benutzeraktivitätsbericht für den jeweiligen Benutzer zugreifen. Wenn Sie für einen Peer-to-Peer-Anruf auf die Metrik „Letzte Aktivität“ klicken, gelangen Sie zum Detailbericht über Peer-to-Peer-Sitzungen. Wenn Sie für eine Konferenz auf dieselbe Metrik klicken, gelangen Sie zum detaillierten Konferenzbericht.</span><span class="sxs-lookup"><span data-stu-id="6619a-p105">The IP Phone Inventory Report is accessed from the Monitoring Reports home page. If you click the User URI metric you can access the User Activity Report for that user. Clicking the Last activity metric for a peer-to-peer call will take you to the Peer-to-Peer Session Detail Report; clicking that same metric for a conference will take you to the Conference Detail Report.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-ip-phone-inventory-report"></a><span data-ttu-id="6619a-130">Optimale Nutzung des Berichts für den IP-Telefonbestand</span><span class="sxs-lookup"><span data-stu-id="6619a-130">Making the Best Use of the IP Phone Inventory Report</span></span>

<span data-ttu-id="6619a-131">Wenn Sie nur an Nutzungsinformationen für eine bestimmte Art von Telefon interessiert sind (beispielsweise: "wie oft verwenden Benutzer ein Polycom CX600-Telefon?"), können Sie diese Informationen direkt aus dem Inventarbericht für IP-Telefone abrufen, indem Sie für diese bestimmte Art von Telefon filtern.</span><span class="sxs-lookup"><span data-stu-id="6619a-131">If you're only interested in usage information for one particular kind of phone (for example, "How often are users using a Polycom CX600 phone?") you can get that information directly from the IP Phone Inventory Report by filtering for that particular kind of phone.</span></span> <span data-ttu-id="6619a-132">Wenn Sie jedoch Zusammenfassungsinformationen für alle ihre Smartphones (wie viele Personen eine Polycom CX600 verwenden, wie viele eine LG-Nortel-IP8540 verwenden usw.) möchten, müssen Sie die Daten exportieren und eine andere Anwendung (wie Windows PowerShell) verwenden, um diese Art der Analyse durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="6619a-132">However, if you want summary information for all your phones (how many people are using a Polycom CX600, how many are using an LG-Nortel IP8540, etc.) then you will need to export the data and use another application (such as Windows PowerShell) to do that type of analysis.</span></span> <span data-ttu-id="6619a-133">Angenommen, Sie exportieren die Daten in eine Datei mit Komma getrennten Werten (C: \\ Data \\ IP \_ Phone \_ Inventory \_Report.csv).</span><span class="sxs-lookup"><span data-stu-id="6619a-133">For example, suppose you export the data to a comma-separated values file (C:\\Data\\IP\_Phone\_Inventory\_Report.csv).</span></span> <span data-ttu-id="6619a-134">In diesem Fall können Sie mit diesen beiden Befehlen Zusammenfassungsdaten für alle Ihre Telefone bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="6619a-134">In that case, you could use these two commands to provide summary data for all your phones:</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones |Group-Object Manufacturer, "Hardware version" | Select-Object Count, Name | Sort-Object Count -Descending

<span data-ttu-id="6619a-135">Die zurückgegebenen Daten sehen so ähnlich aus, wie diese:</span><span class="sxs-lookup"><span data-stu-id="6619a-135">That will return data similar to this:</span></span>

    Count    Name
    -----    ----
      267    POLYCOM, CX700
      267    POLYCOM, CX600
      166    POLYCOM, C
       68    Microsoft, CPE
       64    LG-Nortel, IP8540
       59    Aastra, 6725ip
       37    LG-Nortel, IP
       22    POLYCOM, CX3000
       11    Microsoft, CPE_A
        9    POLYCOM, CX500
        7    Aastra, 6721ip

<span data-ttu-id="6619a-136">Gleichermaßen erhalten Sie mithilfe dieser beiden Befehle Informationen dazu, welche Telefone zwar beim System angemeldet, aber tatsächlich nie zum Telefonieren genutzt wurden (der Wert der Metrik „Letzte Aktivität“ ist leer und gibt somit an, dass es keine letzte Aktivität gab):</span><span class="sxs-lookup"><span data-stu-id="6619a-136">Similarly, these two commands tell you which phones logged on to the system but were never actually used to make a call (the value of the Last activity metric is blank, indicating that there hasn't been any last activity):</span></span>

    $phones = Import-Csv "C:\Data\IP_Phone_Inventory_Report.csv"
    $phones | Where-Object {$_."Last activity" -eq ""}

<span data-ttu-id="6619a-137">Dabei werden für alle nicht verwendeten Telefone Daten zurückgegeben, die den Folgenden ähneln:</span><span class="sxs-lookup"><span data-stu-id="6619a-137">That returns data similar to this for each phone that has not been used:</span></span>

    Manufacturer     : POLYCOM
    Hardware version : CX600
    MAC address      : 00-04-F2-00-01-76
    User URI         : 422
    User agent       : CPE/4.0.7423.1 OCPhone/4.0.7423.1 (Microsoft Lync 2010 (Beta) Phone Edition)
    Last logon time  : 8/30/2010 4:44:48 PM
    Last logoff time : 8/30/2010 5:59:07 PM
    Last activity    :

<span data-ttu-id="6619a-138">Eine weitere interessante Möglichkeit zur Verwendung des Inventarberichts für IP-Telefone: Wenn Sie über die Mac-Adresse eines IP-Telefons verfügen, können Sie den Benutzer, der das Telefon zuletzt verwendet hat, einfach über die Adresse in das Textfeld Mac-Adresse eingeben.</span><span class="sxs-lookup"><span data-stu-id="6619a-138">Another interesting way to use the IP Phone Inventory Report is this: if you have the MAC address of an IP Phone you can find out the user who last used that phone simply by entering that address in the MAC address text box.</span></span> <span data-ttu-id="6619a-139">Der Bericht IP Phone Inventory meldet dann (unter anderem) die SIP-Adresse des Benutzers, der sich zuletzt mit diesem Telefon angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="6619a-139">The IP Phone Inventory report will then report back (among other things) the SIP address of the user who last logged on with that phone.</span></span> <span data-ttu-id="6619a-140">Sie können auch eine SIP-Adresse des Benutzers (im Feld Benutzer-URI-Präfix) eingeben, um alle Telefone festzustellen, die von diesem Benutzer verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="6619a-140">Alternatively, you can enter a user SIP address (in the User URI prefix box) to find out all the phones that have been used by that user.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="6619a-141">Filter</span><span class="sxs-lookup"><span data-stu-id="6619a-141">Filters</span></span>

<span data-ttu-id="6619a-p108">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Der IP-Telefonbestand ermöglicht Ihnen beispielsweise das Anzeigen von Telefonen eines bestimmten Herstellers oder sogar einer bestimmten Version dieser Telefone. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden Registrierungen nach Stunde, Tag, Woche oder Monat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="6619a-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the IP Phone Inventory enables you to view only the phones manufactured by a specific company, or even a specific version of those phones. You can also choose how data should be grouped. In this case, registrations are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="6619a-146">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Bericht für den IP-Telefonbestand verwenden können.</span><span class="sxs-lookup"><span data-stu-id="6619a-146">The following table lists the filters that you can use with the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-filters"></a><span data-ttu-id="6619a-147">Bericht für den IP-Telefonbestand - Filter</span><span class="sxs-lookup"><span data-stu-id="6619a-147">IP Phone Inventory Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6619a-148">Name</span><span class="sxs-lookup"><span data-stu-id="6619a-148">Name</span></span></th>
<th><span data-ttu-id="6619a-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6619a-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6619a-150"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-p109">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="6619a-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="6619a-153">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="6619a-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="6619a-p110">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="6619a-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="6619a-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="6619a-156">7/7/2012</span></span></p>
<p><span data-ttu-id="6619a-157">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="6619a-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="6619a-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="6619a-158">7/3/2012</span></span></p>
<p><span data-ttu-id="6619a-159">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="6619a-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-160"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-p111">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="6619a-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="6619a-163">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="6619a-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="6619a-p112">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="6619a-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="6619a-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="6619a-166">7/7/2012</span></span></p>
<p><span data-ttu-id="6619a-167">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="6619a-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="6619a-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="6619a-168">7/3/2012</span></span></p>
<p><span data-ttu-id="6619a-169">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="6619a-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-170"><strong>Hersteller</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-170"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-p113">Name des Herstellers des IP-Telefons. Die Werte für diesen Filter werden basierend auf den in der Datenbank vorhandenen IP-Telefonen automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6619a-p113">Name of the company that manufactured the IP phone. The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-173"><strong>Hardwareversion</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-173"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-174">Versionsnummer des IP-Telefons; mit den Filtern für den Hersteller und die Hardwareversion können Sie einen bestimmten Telefontyp eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6619a-174">Version number of the IP phone; by using the Manufacturer and the Hardware version filters you can uniquely identity a particular type of phone.</span></span> <span data-ttu-id="6619a-175">Die Werte für diesen Filter werden basierend auf den in der Datenbank vorhandenen IP-Telefonen automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6619a-175">The values for this filter are automatically populated for you based on the IP phones that are currently in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-176"><strong>Benutzer-Agent</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-176"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-p115">ID für die vom IP-Telefon verwendete Software. Die Werte für diesen Filter werden basierend auf den in der Datenbank vorhandenen IP-Telefonen automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6619a-p115">Identifier for the software used by the IP phone. The values for this filter are automatically populated for you based on the IP phones currently in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-179"><strong>MAC-Adresse</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-179"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-p116">Eindeutige ID für die Netzwerkschnittstelle auf dem IP-Telefon. Die MAC-Adresse (Media Access Control) wird in der Regel bei der Herstellung des Telefons zugewiesen und fest in der Gerätehardware verdrahtet.</span><span class="sxs-lookup"><span data-stu-id="6619a-p116">Unique identifier for the network interface on the IP phone. The Media Access Control (MAC) address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p>
<p><span data-ttu-id="6619a-p117">Zum Suchen nach Datensätzen mit einer bestimmten MAC-Adresse geben Sie einfach diese Adresse ein, z. B.:</span><span class="sxs-lookup"><span data-stu-id="6619a-p117">To search for records pertaining to a specific MAC address simply enter that address. For example:</span></span></p>
<p><span data-ttu-id="6619a-184">00-08-5D-16-16-48</span><span class="sxs-lookup"><span data-stu-id="6619a-184">00-08-5D-16-16-48</span></span></p>
<p><span data-ttu-id="6619a-p118">Die Adresse muss vollständig eingegeben werden. Ein Teil einer Adresse (z. B. 00-08-5D) gibt keine Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="6619a-p118">You must enter the complete address. A partial address (for example 00-08-5D) does not return any data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-187"><strong>Letzte Aktivität vor (Tage)</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-187"><strong>Last activity before days</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-188">Wählen Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="6619a-188">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="6619a-189">[Alle]</span><span class="sxs-lookup"><span data-stu-id="6619a-189">[All]</span></span></p></li>
<li><p><span data-ttu-id="6619a-190">10</span><span class="sxs-lookup"><span data-stu-id="6619a-190">10</span></span></p></li>
<li><p><span data-ttu-id="6619a-191">20</span><span class="sxs-lookup"><span data-stu-id="6619a-191">20</span></span></p></li>
<li><p><span data-ttu-id="6619a-192">30</span><span class="sxs-lookup"><span data-stu-id="6619a-192">30</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-193"><strong>Zuletzt abgemeldet vor (Tage):</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-193"><strong>Last logoff time before days</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-194">Wählen Sie einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="6619a-194">Select one of the following values:</span></span></p>
<ul>
<li><p><span data-ttu-id="6619a-195">[Alle]</span><span class="sxs-lookup"><span data-stu-id="6619a-195">[All]</span></span></p></li>
<li><p><span data-ttu-id="6619a-196">10</span><span class="sxs-lookup"><span data-stu-id="6619a-196">10</span></span></p></li>
<li><p><span data-ttu-id="6619a-197">20</span><span class="sxs-lookup"><span data-stu-id="6619a-197">20</span></span></p></li>
<li><p><span data-ttu-id="6619a-198">30</span><span class="sxs-lookup"><span data-stu-id="6619a-198">30</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-199"><strong>Präfix des Benutzer-URI</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-199"><strong>User URI prefix</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-200">SIP-Adresse des Benutzers, der das IP-Telefon verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="6619a-200">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="6619a-201">Metriken</span><span class="sxs-lookup"><span data-stu-id="6619a-201">Metrics</span></span>

<span data-ttu-id="6619a-202">In der folgenden Tabelle werden Metriken aufgelistet, die im Bericht für den IP-Telefonbestand angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6619a-202">The following table lists the information provided in the IP Phone Inventory Report.</span></span>

### <a name="ip-phone-inventory-report-metrics"></a><span data-ttu-id="6619a-203">Bericht für den IP-Telefonbestand - Metriken</span><span class="sxs-lookup"><span data-stu-id="6619a-203">IP Phone Inventory Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6619a-204">Name</span><span class="sxs-lookup"><span data-stu-id="6619a-204">Name</span></span></th>
<th><span data-ttu-id="6619a-205">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="6619a-205">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6619a-206">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6619a-206">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6619a-207"><strong>Hersteller</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-207"><strong>Manufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-208">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-209">Name des Herstellers des IP-Telefons.</span><span class="sxs-lookup"><span data-stu-id="6619a-209">Name of the company that manufactured the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-210"><strong>Hardwareversion</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-210"><strong>Hardware version</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-211">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-212">Versionsnummer des IP-Telefons.</span><span class="sxs-lookup"><span data-stu-id="6619a-212">Version number of the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-213"><strong>MAC-Adresse</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-213"><strong>MAC address</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-214">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-p119">Eindeutige ID für die Netzwerkschnittstelle auf dem IP-Telefon. Die MAC-Adresse wird in der Regel bei der Herstellung des Telefons zugewiesen und fest in der Gerätehardware verdrahtet.</span><span class="sxs-lookup"><span data-stu-id="6619a-p119">Unique identifier for the network interface on the IP phone. The MAC address is typically assigned at the time the phone is manufactured and is hard-wired into the device hardware.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-217"><strong>Benutzer-URI</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-217"><strong>User URI</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-218">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-218">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-219">SIP-Adresse des Benutzers, der das IP-Telefon verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="6619a-219">SIP address of the user who used the IP phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-220"><strong>Benutzer-Agent</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-220"><strong>User agent</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-221">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-222">ID für die vom IP-Telefon verwendete Software.</span><span class="sxs-lookup"><span data-stu-id="6619a-222">Identifier for the software used by the IP phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-223"><strong>Zuletzt angemeldet um:</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-223"><strong>Last logon time</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-224">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-225">Datum und Uhrzeit der letzten Anmeldung des IP-Telefons bei lync Server.</span><span class="sxs-lookup"><span data-stu-id="6619a-225">Date and time that the IP phone last logged on to Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6619a-226"><strong>Zuletzt abgemeldet um:</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-226"><strong>Last logoff time</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-227">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-228">Datum und Uhrzeit, zu dem das IP-Telefon zuletzt von lync Server abgemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="6619a-228">Date and time that the IP phone last logged off from Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6619a-229"><strong>Letzte Aktivität</strong></span><span class="sxs-lookup"><span data-stu-id="6619a-229"><strong>Last activity</strong></span></span></p></td>
<td><p><span data-ttu-id="6619a-230">Ja</span><span class="sxs-lookup"><span data-stu-id="6619a-230">Yes</span></span></p></td>
<td><p><span data-ttu-id="6619a-231">Datum und Uhrzeit der letzten Verwendung des IP-Telefons.</span><span class="sxs-lookup"><span data-stu-id="6619a-231">Date and time that the IP phone was last used.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6619a-232">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6619a-232">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

