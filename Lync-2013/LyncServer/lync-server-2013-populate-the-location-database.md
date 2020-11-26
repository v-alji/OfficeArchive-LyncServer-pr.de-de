---
title: 'Lync Server 2013: Auffüllen der Standortdatenbank'
description: 'Lync Server 2013: füllen Sie die Standortdatenbank auf.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Populate the location database
ms:assetid: fb84f5b6-c991-4893-bdbf-f195b4b7d28e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413069(v=OCS.15)
ms:contentKeyID: 48185939
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6cf3204795ae2c4f8248517b84d7a5ac1bad0d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442845"
---
# <a name="populate-the-location-database-in-lync-server-2013"></a><span data-ttu-id="6dc09-103">Auffüllen der Standortdatenbank in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6dc09-103">Populate the location database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6dc09-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6dc09-104">

<span> </span></span></span>

<span data-ttu-id="6dc09-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="6dc09-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="6dc09-p101">Zum automatischen Suchen nach Clients in einem Netzwerk müssen Sie zunächst die Standortdatenbank mithilfe einer Netzwerk-*Wiremap* auffüllen, die Netzwerkelemente physischen Adressen (d. h. Postanschriften) zuordnet. Sie können Subnetze, drahtlose Zugriffspunkte, Switches und Ports verwenden, um die Wiremap zu definieren.</span><span class="sxs-lookup"><span data-stu-id="6dc09-p101">To automatically locate clients within a network, you first need to populate the location database with a network *wiremap*, which maps network elements to civic (that is, street) addresses. You can use subnets, wireless access points, switches, and ports to define the wiremap.</span></span>

<span data-ttu-id="6dc09-108">Sie können der Standortdatenbank Adressen einzeln oder unter Verwendung einer CSV-Datei per Massenvorgang hinzufügen. Die CSV-Datei muss dabei die in der folgenden Tabelle beschriebenen Spaltenformate aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-108">You can add addresses to the location database individually, or in bulk by using a CSV file that contains the column formats described in the following table.</span></span>

<span data-ttu-id="6dc09-p102">Wenn Sie ein ELIN-Gateway (Emergency Location Identification Number) verwenden, schließen Sie für jeden Standort die ELIN in das Feld **Unternehmensname** ein. Sie können für jeden Standort mehrere ELINs eingeben, jeweils durch ein Semikolon voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="6dc09-p102">If you use an Emergency Location Identification Number (ELIN) gateway, include the ELIN in the **CompanyName** field for each location. You can include multiple ELINs for each location, each separated by a semicolon.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dc09-111">Netzwerkelement</span><span class="sxs-lookup"><span data-stu-id="6dc09-111">Network Element</span></span></th>
<th><span data-ttu-id="6dc09-112">Erforderliche Spalten</span><span class="sxs-lookup"><span data-stu-id="6dc09-112">Required Columns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6dc09-113"><strong>Drahtloser Zugriffspunkt</strong></span><span class="sxs-lookup"><span data-stu-id="6dc09-113"><strong>Wireless access point</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc09-114">&lt;BSSID &gt; , &lt; Description &gt; , &lt; Location &gt; , &lt; CompanyName &gt; , &lt; Hausnummer &gt; , &lt; HouseNumberSuffix &gt; , &lt; &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6dc09-114">&lt;BSSID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6dc09-115">&lt;... Straßennamen &gt; , &lt; "streetsuffix" &gt; , &lt; postdirectional &gt; , &lt; Ort &gt; , &lt; Bundes &gt; &lt; Land, PLZ &gt; , &lt; Land&gt;</span><span class="sxs-lookup"><span data-stu-id="6dc09-115">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc09-116"><strong>Subnetz</strong></span><span class="sxs-lookup"><span data-stu-id="6dc09-116"><strong>Subnet</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc09-117">&lt;Subnet &gt; , &lt; Description &gt; , &lt; Location &gt; , &lt; CompanyName &gt; , &lt; Hausnummer &gt; , &lt; HouseNumberSuffix &gt; , &lt; &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6dc09-117">&lt;Subnet&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6dc09-118">&lt;... Straßennamen &gt; , &lt; "streetsuffix" &gt; , &lt; postdirectional &gt; , &lt; Ort &gt; , &lt; Bundes &gt; &lt; Land, PLZ &gt; , &lt; Land&gt;</span><span class="sxs-lookup"><span data-stu-id="6dc09-118">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6dc09-119"><strong>Port</strong></span><span class="sxs-lookup"><span data-stu-id="6dc09-119"><strong>Port</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc09-120">&lt;Chassis-PortIDSubType, Port-Nr, &gt; &lt; &gt; &lt; &gt; &lt; Description &gt; , &lt; Location &gt; , &lt; CompanyName &gt; , &lt; Hausnummer &gt; , &lt; HouseNumberSuffix &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6dc09-120">&lt;ChassisID&gt;,&lt;PortIDSubType&gt;,&lt;PortID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,…</span></span></p>
<p><span data-ttu-id="6dc09-121">&lt;... Richtungs- &gt; , &lt; Straßennamen &gt; -, &lt; "streetsuffix" &gt; -, &lt; postdirectional &gt; -, &lt; Stadt-, Bundesland-, &gt; &lt; &gt; &lt; PLZ &gt; -, &lt; Land&gt;</span><span class="sxs-lookup"><span data-stu-id="6dc09-121">…&lt;PreDirectional&gt;,&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6dc09-122"><strong>Switch</strong></span><span class="sxs-lookup"><span data-stu-id="6dc09-122"><strong>Switch</strong></span></span></p></td>
<td><p><span data-ttu-id="6dc09-123">&lt;Chassis-Nr, &gt; &lt; Description &gt; , &lt; Location &gt; , &lt; CompanyName &gt; , &lt; Hausnummer &gt; , &lt; HouseNumberSuffix &gt; , &lt; &gt; ,...</span><span class="sxs-lookup"><span data-stu-id="6dc09-123">&lt;ChassisID&gt;,&lt;Description&gt;,&lt;Location&gt;,&lt;CompanyName&gt;,&lt;HouseNumber&gt;,&lt;HouseNumberSuffix&gt;,&lt;PreDirectional&gt;,…</span></span></p>
<p><span data-ttu-id="6dc09-124">&lt;... Straßennamen &gt; , &lt; "streetsuffix" &gt; , &lt; postdirectional &gt; , &lt; Ort &gt; , &lt; Bundes &gt; &lt; Land, PLZ &gt; , &lt; Land&gt;</span><span class="sxs-lookup"><span data-stu-id="6dc09-124">…&lt;StreetName&gt;,&lt;StreetSuffix&gt;,&lt;PostDirectional&gt;,&lt;City&gt;,&lt;State&gt;,&lt;PostalCode&gt;,&lt;Country&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6dc09-125">Wenn Sie die Standortdatenbank nicht auffüllen und die Eigenschaft **Standort erforderlich** in der Standortrichtlinie auf **Ja** oder **Haftungsausschluss** festgelegt ist, wird der Benutzer vom Client aufgefordert, den Standort manuell einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6dc09-125">If you do not populate the location database, and the **Location Required** in the Location Policy is set to **Yes** or **Disclaimer**, the client will prompt the user to enter a location manually.</span></span>

<span data-ttu-id="6dc09-126">Details zum Auffüllen der Standortdatenbank finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6dc09-126">For details about populating the location database, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="6dc09-127">**Get-CsLisSubnet**</span><span class="sxs-lookup"><span data-stu-id="6dc09-127">**Get-CsLisSubnet**</span></span>

  - <span data-ttu-id="6dc09-128">**Satz-CsLisSubnet**</span><span class="sxs-lookup"><span data-stu-id="6dc09-128">**Set-CsLisSubnet**</span></span>

  - <span data-ttu-id="6dc09-129">Remove-CsLisSubnet</span><span class="sxs-lookup"><span data-stu-id="6dc09-129">Remove-CsLisSubnet</span></span>

  - <span data-ttu-id="6dc09-130">**Get-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6dc09-130">**Get-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6dc09-131">**Satz-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6dc09-131">**Set-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6dc09-132">**Remove-CsLisWirelessAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="6dc09-132">**Remove-CsLisWirelessAccessPoint**</span></span>

  - <span data-ttu-id="6dc09-133">**Get-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6dc09-133">**Get-CsLisSwitch**</span></span>

  - <span data-ttu-id="6dc09-134">**Satz-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6dc09-134">**Set-CsLisSwitch**</span></span>

  - <span data-ttu-id="6dc09-135">**Remove-CsLisSwitch**</span><span class="sxs-lookup"><span data-stu-id="6dc09-135">**Remove-CsLisSwitch**</span></span>

  - <span data-ttu-id="6dc09-136">**Get-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6dc09-136">**Get-CsLisPort**</span></span>

  - <span data-ttu-id="6dc09-137">**Satz-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6dc09-137">**Set-CsLisPort**</span></span>

  - <span data-ttu-id="6dc09-138">**Remove-CsLisPort**</span><span class="sxs-lookup"><span data-stu-id="6dc09-138">**Remove-CsLisPort**</span></span>

<div>

## <a name="to-add-network-elements-to-the-location-database"></a><span data-ttu-id="6dc09-139">So fügen Sie der Standortdatenbank Netzwerkelemente hinzu</span><span class="sxs-lookup"><span data-stu-id="6dc09-139">To add network elements to the location database</span></span>

1.  <span data-ttu-id="6dc09-140">Führen Sie das folgende Cmdlet aus, um der Standortdatenbank einen Subnetzstandort hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-140">Run the following cmdlet to add a subnet location to the location database.</span></span>
    
        Set-CsLisSubnet -Subnet 157.56.66.0 -Description "Subnet 1" -Location Location1 -CompanyName "Litware" -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6dc09-p103">Für ELIN-Gateways geben Sie die ELIN in das Feld „Unternehmensname“ ein. Sie können mehrere ELINs eingeben. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6dc09-p103">For ELIN gateways, put the ELIN in the CompanyName field. You can include more than one ELIN. For example:</span></span>
    
        Set-CsLisSubnet -Subnet 157.56.66.0 -Description "Subnet 1" -Location Location1 -CompanyName 425-555-0100; 425-555-0200; 425-555-0300 -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6dc09-144">Alternativ dazu können Sie auch folgende Cmdlets ausführen und eine Datei namens „subnets.csv“ verwenden, um Subnetzstandorte per Massenvorgang zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6dc09-144">Alternately, you can run the following cmdlets and use a file named "subnets.csv" to bulk update subnet locations.</span></span>
    
        $g = Import-Csv subnets.csv
        $g | Set-CsLisSubnet

2.  <span data-ttu-id="6dc09-145">Führen Sie das folgende Cmdlet aus, um der Standortdatenbank drahtlose Standorte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-145">Run the following cmdlet to add wireless locations to the location database.</span></span>
    
        Set-CsLisWirelessAccessPoint -BSSID 0A-23-CD-16-AA-2E -Description "Wireless1" -Location Location2 -CompanyName "Litware" -HouseNumber 2345 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Bellevue -State WA -PostalCode 99234 -Country US
    
    <span data-ttu-id="6dc09-146">Alternativ dazu können Sie auch folgende Cmdlets ausführen und eine Datei namens „waps.csv“ verwenden, um drahtlose Standorte per Massenvorgang zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6dc09-146">Alternately, you can run the following cmdlets and use a file named "waps.csv" to bulk update wireless locations.</span></span>
    
        $g = Import-Csv waps.csv
        $g | Set-CsLisWirelessAccessPoint

3.  <span data-ttu-id="6dc09-147">Führen Sie das folgende Cmdlet aus, um der Standortdatenbank Switchstandorte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-147">Run the following cmdlet to add switch locations to the location database.</span></span>
    
        Set-CsLisSwitch-ChassisID 0B-23-CD-16-AA-BB -Description "Switch1" -Location Location1 -CompanyName "Litware" -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Redmond -State WA -PostalCode 99123 -Country US
    
    <span data-ttu-id="6dc09-148">Alternativ dazu können Sie auch folgende Cmdlets ausführen und eine Datei namens „switches.csv“ verwenden, um Switchstandorte per Massenvorgang zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6dc09-148">Alternately, you can run the following cmdlets and use a file named "switches.csv" to bulk update switch locations.</span></span>
    
        $g = Import-Csv switches.csv
        $g | Set-CsLisSwitch

4.  <span data-ttu-id="6dc09-149">Führen Sie das folgende Cmdlet aus, um der Standortdatenbank Portstandorte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-149">Run the following cmdlet to add port locations to the location database</span></span>
    
        Set-CsLisPort -ChassisID 0C-23-CD-16-AA-CC -PortID 0A-abcd -Description "Port1" -Location Location2 -CompanyName "Litware" -HouseNumber 2345 -HouseNumberSuffix "" -PreDirectional "" -StreetName 163rd -StreetSuffix Ave -PostDirectional NE -City Bellevue -State WA -PostalCode 99234 -Country US
    
    <span data-ttu-id="6dc09-p104">Der Standardwert für PortIDSubType lautet LocallyAssigned. Sie können den Wert auch auf InterfaceAlias oder InterfaceName festlegen.</span><span class="sxs-lookup"><span data-stu-id="6dc09-p104">The default for PortIDSubType is LocallyAssigned. You can also set it to InterfaceAlias or InterfaceName</span></span>
    
    <span data-ttu-id="6dc09-152">Alternativ dazu können Sie auch folgende Cmdlets ausführen und eine Datei namens „ports.csv“ verwenden, um Portstandorte per Massenvorgang zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6dc09-152">Alternately, you can run the following cmdlets and use a file named "ports.csv" to bulk update port locations.</span></span>
    
        $g = Import-Csv ports.csv
        $g | Set-CsLisPort

<span data-ttu-id="6dc09-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6dc09-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

