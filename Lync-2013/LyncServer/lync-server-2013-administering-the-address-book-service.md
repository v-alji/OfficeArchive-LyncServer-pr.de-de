---
title: 'Lync Server 2013: Verwalten des Adressbuchdiensts'
description: 'Lync Server 2013: Verwalten des Adressbuchdiensts'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Administering the Address Book Service
ms:assetid: 801e4243-9670-4477-aa2f-88b61ecf5351
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429711(v=OCS.15)
ms:contentKeyID: 48184649
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 86d549b06b5c6ac1c450edf9e7edb0b902ef9adf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440696"
---
# <a name="administering-the-address-book-service-in-lync-server-2013"></a><span data-ttu-id="aa671-103">Verwalten des Adressbuchdiensts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa671-103">Administering the Address Book Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa671-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa671-104">

<span> </span></span></span>

<span data-ttu-id="aa671-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="aa671-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="aa671-106">Als Teil der Bereitstellung von lync Server, Enterprise Edition oder Standard Edition-Server wird der Adressbuchdienst standardmäßig installiert.</span><span class="sxs-lookup"><span data-stu-id="aa671-106">As a part of the deployment of Lync Server, Enterprise Edition or Standard Edition server, the Address Book Service is installed by default.</span></span> <span data-ttu-id="aa671-107">Die vom Adressbuchdienst – RTCab – verwendete Datenbank wird auf dem SQL Server erstellt (für Enterprise Edition, dies ist der Back-End-SQL-Server; für den Standard Edition-Server, den zusammengefassten SQL Server).</span><span class="sxs-lookup"><span data-stu-id="aa671-107">The database used by the Address Book Service – RTCab – is created on the SQL Server (for Enterprise Edition, this is the back-end SQL Server; for Standard Edition server, the collocated SQL Server).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="aa671-108">Informationen zur Verwendung der <STRONG>ADSI-Bearbeitung</STRONG> zum Bearbeiten von Active Directory-Objektattributen finden Sie unter <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI-Bearbeitung</A>.</span><span class="sxs-lookup"><span data-stu-id="aa671-108">For information about using <STRONG>ADSI Edit</STRONG> to edit Active Directory Domain Services object attributes, see <A href="https://go.microsoft.com/fwlink/?linkid=330427">ADSI Edit</A>.</span></span> <span data-ttu-id="aa671-109">Informationen zu einem Tool im Resource Kit speziell für den Adressbuchdienst finden Sie unter <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft lync Server 2013 Resource Kit-Tools</A>.</span><span class="sxs-lookup"><span data-stu-id="aa671-109">For information about a tool in the Resource Kit specifically for the Address Book service, see <A href="https://go.microsoft.com/fwlink/?linkid=330429">Microsoft Lync Server 2013 Resource Kit Tools</A>.</span></span>



</div>

<div>

## <a name="address-book-server-phone-number-normalization"></a><span data-ttu-id="aa671-110">Telefonnummernnormalisierung des Adressbuchservers</span><span class="sxs-lookup"><span data-stu-id="aa671-110">Address Book Server Phone Number Normalization</span></span>

<span data-ttu-id="aa671-111">Lync Server erfordert standardisierte RFC 3966/E. 164-Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="aa671-111">Lync Server requires standardized RFC 3966/E.164 phone numbers.</span></span> <span data-ttu-id="aa671-112">Um Telefonnummern zu verwenden, die nicht strukturiert oder inkonsistent formatiert sind, verwendet lync Server den Adressbuchserver, um Telefonnummern vorverarbeiten, bevor Sie an die Normalisierungsregeln übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa671-112">To use phone numbers that are unstructured or inconsistently formatted, Lync Server relies on the Address Book Server to preprocess phone numbers before they are handed off to the normalization rules.</span></span> <span data-ttu-id="aa671-113">Wenn eine Telefonnummer aus dem Adressbuch verwendet wird und die Normalisierungsregel angewendet wird, können Clients wie lync Phone Edition und lync Mobile diese normalisierten Nummern verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa671-113">When a phone number is used from the address book and the normalization rule is applied, clients, such as Lync Phone Edition and Lync Mobile, can use these normalized numbers.</span></span>

<span data-ttu-id="aa671-114">Die Normalisierungsregeln, die in früheren Versionen verwendet wurden, funktionieren möglicherweise ohne Anpassungen nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="aa671-114">The normalization rules that were used in previous versions may not work properly without some adjustments.</span></span> <span data-ttu-id="aa671-115">Da die Leerzeichen und nicht obligatorischen Zeichen vor den Normalisierungsregeln entfernt werden, wenn Ihr Regex-Ausdruck speziell nach einem Strich oder einem anderen Zeichen sucht, das entfernt wurde, schlägt die Normalisierungsregel möglicherweise fehl.</span><span class="sxs-lookup"><span data-stu-id="aa671-115">Because the white space and non-mandatory characters are removed prior to the normalization rules, if your regex expression is specifically looking for a dash or other character that was removed, your normalization rule might fail.</span></span> <span data-ttu-id="aa671-116">Überprüfen Sie Ihre Normalisierungsregeln, um sicherzustellen, dass Sie nicht nach diesen nicht obligatorischen Zeichen suchen, oder dass die Regel ordnungsgemäß fehlschlägt und fortgesetzt werden kann, wenn das Zeichen nicht vorhanden ist, wenn es von der Regel erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="aa671-116">You should review your normalization rules to ensure that either they are not looking for these non-mandatory characters, or that the rule can fail gracefully and continue in the event that the character is not present where the rule anticipates it will be.</span></span>

</div>

<div>

## <a name="user-replicator-and-address-book-server"></a><span data-ttu-id="aa671-117">Benutzer-Replikator und Adressbuch Server</span><span class="sxs-lookup"><span data-stu-id="aa671-117">User Replicator and Address Book Server</span></span>

<span data-ttu-id="aa671-118">Der Adressbuch Server verwendet die vom Benutzerreplikationsdienst zur Verfügung gestellten Daten, um die Informationen zu aktualisieren, die er ursprünglich aus der globalen Adressliste (Global Address List, GAL) erhält.</span><span class="sxs-lookup"><span data-stu-id="aa671-118">The Address Book Server uses data provided by User Replicator to update the information that it initially obtains from the global address list (GAL).</span></span> <span data-ttu-id="aa671-119">Der Benutzerreplikationsdienst schreibt die Attribute der Active Directory-Domänendienste für jeden Benutzer, Kontakt und jede Gruppe in die Tabelle AbUserEntry-Tabelle in der Datenbank, und der Adressbuchserver synchronisiert die Benutzerdaten aus der Datenbank in Dateien im Dateispeicher des Adressbuchservers und in die Adressbuchdatenbank-RTCab.</span><span class="sxs-lookup"><span data-stu-id="aa671-119">User Replicator writes the Active Directory Domain Services attributes for each user, contact, and group into the AbUserEntry table in the database and the Address Book Server syncs the user data from the database into files in the Address Book Server file store and into the Address Book database RTCab.</span></span> <span data-ttu-id="aa671-120">Das Schema für die Tabelle AbUserEntry-Tabelle verwendet zwei Spalten, **UserGuid** und **UserData**.</span><span class="sxs-lookup"><span data-stu-id="aa671-120">The schema for the AbUserEntry table uses two columns, **UserGuid** and **UserData**.</span></span> <span data-ttu-id="aa671-121">**UserGuid** ist die Indexspalte und enthält die 16-Byte-GUID des Active Directory-Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa671-121">**UserGuid** is the index column and contains the 16-byte GUID of the Active Directory object.</span></span> <span data-ttu-id="aa671-122">**UserData** ist eine Bildspalte, die alle zuvor erwähnten Attribute für Active Directory-Domänendienste für diesen Kontakt enthält.</span><span class="sxs-lookup"><span data-stu-id="aa671-122">**UserData** is an image column which contains all of the previously mentioned Active Directory Domain Services attributes for that contact.</span></span>

<span data-ttu-id="aa671-123">Der Benutzerreplikationsdienst bestimmt, welche Active Directory-Attribute geschrieben werden sollen, indem Sie eine Konfigurationstabelle lesen, die sich in derselben SQL Server-basierten Instanz wie die Tabelle AbUserEntry-Tabelle befindet.</span><span class="sxs-lookup"><span data-stu-id="aa671-123">User Replicator determines which Active Directory attributes to write by reading a configuration table located in the same SQL Server-based instance as the AbUserEntry table.</span></span> <span data-ttu-id="aa671-124">Die AbAttribute-Tabelle enthält drei Spalten, **ID**, **Name**, **Flags** und **enable**.</span><span class="sxs-lookup"><span data-stu-id="aa671-124">The AbAttribute table contains three columns, **ID**, **Name**, **Flags**, and **Enable**.</span></span> <span data-ttu-id="aa671-125">Die Tabelle wird beim Einrichten der Datenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa671-125">The table is created during database setup.</span></span> <span data-ttu-id="aa671-126">Wenn die AbAttribute-Tabelle leer ist, überspringt der Benutzerreplikationsdienst die Tabelle AbUserEntry-Tabellen Verarbeitungslogik.</span><span class="sxs-lookup"><span data-stu-id="aa671-126">If the AbAttribute table is empty, User Replicator skips its AbUserEntry table processing logic.</span></span> <span data-ttu-id="aa671-127">Adressbuchserver Attribute sind dynamisch und werden aus der AbAttribute-Tabelle abgerufen, die zunächst vom Adressbuchserver geschrieben wird, wenn der Adressbuchserver aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="aa671-127">Address Book Server attributes are dynamic and are retrieved from the AbAttribute table, which is initially written by the Address Book Server when the Address Book Server is activated.</span></span>

<span data-ttu-id="aa671-128">Bei der Aktivierung des Adressbuchservers wird die AbAttribute-Tabelle mit den in der folgenden Tabelle dargestellten Werten gefüllt.</span><span class="sxs-lookup"><span data-stu-id="aa671-128">Address Book Server activation populates the AbAttribute table with the values shown in the following table.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa671-129">ID</span><span class="sxs-lookup"><span data-stu-id="aa671-129">ID</span></span></th>
<th><span data-ttu-id="aa671-130">Name</span><span class="sxs-lookup"><span data-stu-id="aa671-130">Name</span></span></th>
<th><span data-ttu-id="aa671-131">Kennzeichnungen</span><span class="sxs-lookup"><span data-stu-id="aa671-131">Flags</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa671-132">1</span><span class="sxs-lookup"><span data-stu-id="aa671-132">1</span></span></p></td>
<td><p><span data-ttu-id="aa671-133">givenName</span><span class="sxs-lookup"><span data-stu-id="aa671-133">givenName</span></span></p></td>
<td><p><span data-ttu-id="aa671-134">0x01400000</span><span class="sxs-lookup"><span data-stu-id="aa671-134">0x01400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-135">2</span><span class="sxs-lookup"><span data-stu-id="aa671-135">2</span></span></p></td>
<td><p><span data-ttu-id="aa671-136">SN</span><span class="sxs-lookup"><span data-stu-id="aa671-136">Sn</span></span></p></td>
<td><p><span data-ttu-id="aa671-137">0x02400000</span><span class="sxs-lookup"><span data-stu-id="aa671-137">0x02400000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-138">3</span><span class="sxs-lookup"><span data-stu-id="aa671-138">3</span></span></p></td>
<td><p><span data-ttu-id="aa671-139">DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa671-139">displayName</span></span></p></td>
<td><p><span data-ttu-id="aa671-140">0x03420000</span><span class="sxs-lookup"><span data-stu-id="aa671-140">0x03420000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-141">4</span><span class="sxs-lookup"><span data-stu-id="aa671-141">4</span></span></p></td>
<td><p><span data-ttu-id="aa671-142">Titel</span><span class="sxs-lookup"><span data-stu-id="aa671-142">Title</span></span></p></td>
<td><p><span data-ttu-id="aa671-143">0x04000000</span><span class="sxs-lookup"><span data-stu-id="aa671-143">0x04000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-144">5</span><span class="sxs-lookup"><span data-stu-id="aa671-144">5</span></span></p></td>
<td><p><span data-ttu-id="aa671-145">mailNickname</span><span class="sxs-lookup"><span data-stu-id="aa671-145">mailNickname</span></span></p></td>
<td><p><span data-ttu-id="aa671-146">0x05400000</span><span class="sxs-lookup"><span data-stu-id="aa671-146">0x05400000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-147">6</span><span class="sxs-lookup"><span data-stu-id="aa671-147">6</span></span></p></td>
<td><p><span data-ttu-id="aa671-148">Unternehmen</span><span class="sxs-lookup"><span data-stu-id="aa671-148">Company</span></span></p></td>
<td><p><span data-ttu-id="aa671-149">0x06000000</span><span class="sxs-lookup"><span data-stu-id="aa671-149">0x06000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-150">7</span><span class="sxs-lookup"><span data-stu-id="aa671-150">7</span></span></p></td>
<td><p><span data-ttu-id="aa671-151">physicalDeliveryOfficeName</span><span class="sxs-lookup"><span data-stu-id="aa671-151">physicalDeliveryOfficeName</span></span></p></td>
<td><p><span data-ttu-id="aa671-152">0x07000000</span><span class="sxs-lookup"><span data-stu-id="aa671-152">0x07000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-153">8</span><span class="sxs-lookup"><span data-stu-id="aa671-153">8</span></span></p></td>
<td><p><span data-ttu-id="aa671-154">msRTCSIP-PrimaryUserAddress</span><span class="sxs-lookup"><span data-stu-id="aa671-154">msRTCSIP-PrimaryUserAddress</span></span></p></td>
<td><p><span data-ttu-id="aa671-155">0x08520C00</span><span class="sxs-lookup"><span data-stu-id="aa671-155">0x08520C00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-156">9</span><span class="sxs-lookup"><span data-stu-id="aa671-156">9</span></span></p></td>
<td><p><span data-ttu-id="aa671-157">telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="aa671-157">telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="aa671-158">0x09022800</span><span class="sxs-lookup"><span data-stu-id="aa671-158">0x09022800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-159">10</span><span class="sxs-lookup"><span data-stu-id="aa671-159">10</span></span></p></td>
<td><p><span data-ttu-id="aa671-160">homePhone</span><span class="sxs-lookup"><span data-stu-id="aa671-160">homePhone</span></span></p></td>
<td><p><span data-ttu-id="aa671-161">0x0A302800</span><span class="sxs-lookup"><span data-stu-id="aa671-161">0x0A302800</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-162">11</span><span class="sxs-lookup"><span data-stu-id="aa671-162">11</span></span></p></td>
<td><p><span data-ttu-id="aa671-163">Mobil</span><span class="sxs-lookup"><span data-stu-id="aa671-163">Mobile</span></span></p></td>
<td><p><span data-ttu-id="aa671-164">0x0B622800</span><span class="sxs-lookup"><span data-stu-id="aa671-164">0x0B622800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-165">12</span><span class="sxs-lookup"><span data-stu-id="aa671-165">12</span></span></p></td>
<td><p><span data-ttu-id="aa671-166">otherTelephone</span><span class="sxs-lookup"><span data-stu-id="aa671-166">otherTelephone</span></span></p></td>
<td><p><span data-ttu-id="aa671-167">0x0C302000</span><span class="sxs-lookup"><span data-stu-id="aa671-167">0x0C302000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-168">13</span><span class="sxs-lookup"><span data-stu-id="aa671-168">13</span></span></p></td>
<td><p><span data-ttu-id="aa671-169">ipPhone</span><span class="sxs-lookup"><span data-stu-id="aa671-169">ipPhone</span></span></p></td>
<td><p><span data-ttu-id="aa671-170">0x0D302000</span><span class="sxs-lookup"><span data-stu-id="aa671-170">0x0D302000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-171">14</span><span class="sxs-lookup"><span data-stu-id="aa671-171">14</span></span></p></td>
<td><p><span data-ttu-id="aa671-172">Mail</span><span class="sxs-lookup"><span data-stu-id="aa671-172">Mail</span></span></p></td>
<td><p><span data-ttu-id="aa671-173">0x0E500000</span><span class="sxs-lookup"><span data-stu-id="aa671-173">0x0E500000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-174">15</span><span class="sxs-lookup"><span data-stu-id="aa671-174">15</span></span></p></td>
<td><p><span data-ttu-id="aa671-175">GroupType</span><span class="sxs-lookup"><span data-stu-id="aa671-175">groupType</span></span></p></td>
<td><p><span data-ttu-id="aa671-176">0x0F010800</span><span class="sxs-lookup"><span data-stu-id="aa671-176">0x0F010800</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-177">16</span><span class="sxs-lookup"><span data-stu-id="aa671-177">16</span></span></p></td>
<td><p><span data-ttu-id="aa671-178">Abteilung</span><span class="sxs-lookup"><span data-stu-id="aa671-178">Department</span></span></p></td>
<td><p><span data-ttu-id="aa671-179">0x10000000</span><span class="sxs-lookup"><span data-stu-id="aa671-179">0x10000000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-180">17</span><span class="sxs-lookup"><span data-stu-id="aa671-180">17</span></span></p></td>
<td><p><span data-ttu-id="aa671-181">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa671-181">Description</span></span></p></td>
<td><p><span data-ttu-id="aa671-182">0x11000100</span><span class="sxs-lookup"><span data-stu-id="aa671-182">0x11000100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-183">18</span><span class="sxs-lookup"><span data-stu-id="aa671-183">18</span></span></p></td>
<td><p><span data-ttu-id="aa671-184">Manager</span><span class="sxs-lookup"><span data-stu-id="aa671-184">Manager</span></span></p></td>
<td><p><span data-ttu-id="aa671-185">0x12040001</span><span class="sxs-lookup"><span data-stu-id="aa671-185">0x12040001</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-186">19</span><span class="sxs-lookup"><span data-stu-id="aa671-186">19</span></span></p></td>
<td><p><span data-ttu-id="aa671-187">ProxyAddress</span><span class="sxs-lookup"><span data-stu-id="aa671-187">proxyAddress</span></span></p></td>
<td><p><span data-ttu-id="aa671-188">0x00500105</span><span class="sxs-lookup"><span data-stu-id="aa671-188">0x00500105</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-189">20</span><span class="sxs-lookup"><span data-stu-id="aa671-189">20</span></span></p></td>
<td><p><span data-ttu-id="aa671-190">msExchHideFromAddressLists</span><span class="sxs-lookup"><span data-stu-id="aa671-190">msExchHideFromAddressLists</span></span></p></td>
<td><p><span data-ttu-id="aa671-191">0xFF000003</span><span class="sxs-lookup"><span data-stu-id="aa671-191">0xFF000003</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-192">99</span><span class="sxs-lookup"><span data-stu-id="aa671-192">99</span></span></p></td>
<td><p><span data-ttu-id="aa671-193">entryID</span><span class="sxs-lookup"><span data-stu-id="aa671-193">entryID</span></span></p></td>
<td><p><span data-ttu-id="aa671-194">0x99000000</span><span class="sxs-lookup"><span data-stu-id="aa671-194">0x99000000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa671-195">Die Zahlen in der Spalte " **ID** " müssen eindeutig sein und nie wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa671-195">The numbers in the **ID** column must be unique and should never be reused.</span></span> <span data-ttu-id="aa671-196">Außerdem wird durch das aufrecht erhalten der ID-Werte unter 256 Platz in den vom Adressbuch Server geschriebenen Ausgabedateien gespart.</span><span class="sxs-lookup"><span data-stu-id="aa671-196">Also, keeping the ID values under 256 saves space in the output files written by the Address Book Server.</span></span> <span data-ttu-id="aa671-197">Der maximale ID-Wert ist jedoch 65535.</span><span class="sxs-lookup"><span data-stu-id="aa671-197">However, the maximum ID value is 65535.</span></span> <span data-ttu-id="aa671-198">Die Spalte **Name** entspricht dem Active Directory-Attributnamen, den der Benutzerreplikationsdienst in die Tabelle AbUserEntry-Tabelle für jeden Kontakt aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="aa671-198">The **Name** column corresponds to the Active Directory attribute name that User Replicator should put in the AbUserEntry table for each contact.</span></span> <span data-ttu-id="aa671-199">Der Wert in der Spalte **Flags** wird verwendet, um den Typ des Attributs zu definieren.</span><span class="sxs-lookup"><span data-stu-id="aa671-199">The value in the **Flags** column is used to define the type of attribute.</span></span> <span data-ttu-id="aa671-200">Die folgenden Typen von Adressbuch Server Attributen werden vom Benutzerreplikationsdienst erkannt, der durch das niedrige Byte des Werts in der Spalte **Flags** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa671-200">The following types of Address Book Server attributes are recognized by User Replicator, indicated by the low byte of the value in the **Flags** column.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa671-201">Attribut</span><span class="sxs-lookup"><span data-stu-id="aa671-201">Attribute</span></span></th>
<th><span data-ttu-id="aa671-202">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa671-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa671-203">0x0</span><span class="sxs-lookup"><span data-stu-id="aa671-203">0x0</span></span></p></td>
<td><p><span data-ttu-id="aa671-204">Ein Zeichenfolgenattribut.</span><span class="sxs-lookup"><span data-stu-id="aa671-204">A string attribute.</span></span> <span data-ttu-id="aa671-205">Der Benutzerreplikationsdienst wandelt diesen Typ in UTF-8 um, bevor er ihn in der Tabelle AbUserEntry-Tabelle speichert.</span><span class="sxs-lookup"><span data-stu-id="aa671-205">User Replicator converts this type to UTF-8 before storing it in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-206">0x1</span><span class="sxs-lookup"><span data-stu-id="aa671-206">0x1</span></span></p></td>
<td><p><span data-ttu-id="aa671-207">Ein binäres Attribut.</span><span class="sxs-lookup"><span data-stu-id="aa671-207">A binary attribute.</span></span> <span data-ttu-id="aa671-208">Der Benutzerreplikationsdienst speichert diese ohne Konvertierung im BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa671-208">User Replicator stores this in the blob without any conversion.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-209">0x2</span><span class="sxs-lookup"><span data-stu-id="aa671-209">0x2</span></span></p></td>
<td><p><span data-ttu-id="aa671-210">Ein Zeichenfolgenattribut, wird aber nur berücksichtigt, wenn der Attributwert mit &quot; Tel: beginnt &quot; .</span><span class="sxs-lookup"><span data-stu-id="aa671-210">A string attribute, but is included only if the attribute value begins with &quot;tel:&quot;.</span></span> <span data-ttu-id="aa671-211">Dies gilt in erster Linie für mehrwertige Zeichenfolgenattribute, insbesondere für <strong>proxyAddresses</strong>.</span><span class="sxs-lookup"><span data-stu-id="aa671-211">This is primarily for multi-valued string attributes, specifically <strong>proxyAddresses</strong>.</span></span> <span data-ttu-id="aa671-212">In diesem Fall ist der Adressbuch Server nur an <strong>proxyAddresses</strong> -Einträgen interessiert, die mit &quot; Tel: beginnen &quot; .</span><span class="sxs-lookup"><span data-stu-id="aa671-212">In this case, Address Book Server is interested only in <strong>proxyAddresses</strong> entries that begin with &quot;tel:&quot;.</span></span> <span data-ttu-id="aa671-213">Aus diesem Grund speichert der Benutzerreplikationsdienst im Interesse des Speicherplatzes nur die Einträge, die mit &quot; Tel: beginnen &quot; .</span><span class="sxs-lookup"><span data-stu-id="aa671-213">Therefore, in the interest of saving space, User Replicator stores only the entries that begin with &quot;tel:&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-214">0x3</span><span class="sxs-lookup"><span data-stu-id="aa671-214">0x3</span></span></p></td>
<td><p><span data-ttu-id="aa671-215">Ein boolesches Zeichenfolgenattribut, das bei true bewirkt, dass der Benutzer Replicator diesen Kontakt nicht in die Tabelle AbUserEntry-Tabelle einfügt.</span><span class="sxs-lookup"><span data-stu-id="aa671-215">A Boolean string attribute, which if TRUE causes User Replicator to not include this contact in the AbUserEntry table.</span></span> <span data-ttu-id="aa671-216">Ist der Wert false, wird der Benutzerreplikationsdienst dazu veranlasst, die Attribute für diesen Kontakt in die Tabelle AbUserEntry-Tabelle einzubeziehen, jedoch nicht das jeweilige Attribut mit diesem Flag.</span><span class="sxs-lookup"><span data-stu-id="aa671-216">If FALSE, it causes User Replicator to include the attributes for this contact in the AbUserEntry table, but not the particular attribute with this flag.</span></span> <span data-ttu-id="aa671-217">Dies ist ein weiterer spezieller Case-Typ, der in erster Linie für das <strong>msExchHideFromAddressLists</strong> -Attribut steht.</span><span class="sxs-lookup"><span data-stu-id="aa671-217">This is another special case type that is primarily for the <strong>msExchHideFromAddressLists</strong> attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-218">0x4</span><span class="sxs-lookup"><span data-stu-id="aa671-218">0x4</span></span></p></td>
<td><p><span data-ttu-id="aa671-219">Ein Zeichenfolgenattribut, wird aber nur berücksichtigt, wenn der Attributwert mit &quot; SMTP beginnt: &quot; und das &quot; @ &quot; Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="aa671-219">A string attribute, but is included only if the attribute value begins with &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-220">0x5</span><span class="sxs-lookup"><span data-stu-id="aa671-220">0x5</span></span></p></td>
<td><p><span data-ttu-id="aa671-221">Ein Zeichenfolgenattribut, wird aber nur berücksichtigt, wenn der Attributwert entweder mit &quot; "Tel:" &quot; oder &quot; "SMTP:" beginnt &quot; und das &quot; @ &quot; Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="aa671-221">A string attribute, but is included only if the attribute value begins with either &quot;tel:&quot; or &quot;smtp:&quot; and includes the &quot;@&quot; symbol.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-222">0x100</span><span class="sxs-lookup"><span data-stu-id="aa671-222">0x100</span></span></p></td>
<td><p><span data-ttu-id="aa671-223">Wenn festzulegen, handelt es sich um ein mehrwertiges Attribut, das für jeden Kontakt mehrmals angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="aa671-223">If set, this is a multi-valued attribute that can appear more than once for each contact.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-224">0x400</span><span class="sxs-lookup"><span data-stu-id="aa671-224">0x400</span></span></p></td>
<td><p><span data-ttu-id="aa671-225">Wenn diese Einstellung festgesetzt ist, wird das Attribut "e-Mail-Benutzerkontoname" für einen Kontakt angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-225">If set, this identifies the email user account name attribute for a contact.</span></span> <span data-ttu-id="aa671-226">Der Adressbuch Server verwendet dieses Flag, um zu ermitteln, welcher Attributwert im Ereignisprotokolleintrag für die Telefon Normalisierung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa671-226">Address Book Server uses this flag to identify which attribute value to show in the phone normalization event log entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-227">0x800</span><span class="sxs-lookup"><span data-stu-id="aa671-227">0x800</span></span></p></td>
<td><p><span data-ttu-id="aa671-228">Wenn festzulegen, wird ein erforderliches Attribut für einen Kontakt angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-228">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="aa671-229">Der Adressbuch Server enthält nur dann einen Benutzer in der Tabelle AbUserEntry-Tabelle, wenn ein Wert für dieses Attribut in Active Directory vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aa671-229">Address Book Server includes a user in the AbUserEntry table only if there is a value for this attribute in Active Directory.</span></span> <span data-ttu-id="aa671-230">Wenn mehr als ein erforderliches Attribut vorhanden ist, muss nur einer von Ihnen über einen Wert verfügen, um den Benutzer in die Tabelle AbUserEntry-Tabelle einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="aa671-230">If there is more than one required attribute, only one of them is required to have a value to include the user in the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-231">0x1000</span><span class="sxs-lookup"><span data-stu-id="aa671-231">0x1000</span></span></p></td>
<td><p><span data-ttu-id="aa671-232">Wenn der Wert für Address Book Server gesetzt ist, wird der Wert dieses Attributs immer normalisiert.</span><span class="sxs-lookup"><span data-stu-id="aa671-232">If set, Address Book Server always normalizes the value of this attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-233">0x2000</span><span class="sxs-lookup"><span data-stu-id="aa671-233">0x2000</span></span></p></td>
<td><p><span data-ttu-id="aa671-234">Ist der Wert festgelegt, verwendet der Adressbuch Server die normalisierte Zahl von <strong>proxyAddresses</strong>, wenn die <strong>UseNormalizationRules</strong> -CMS-Einstellung falsch ist. Andernfalls verhält es sich wie beim Flag-Bit 0x1000.</span><span class="sxs-lookup"><span data-stu-id="aa671-234">If set, Address Book Server uses the normalized number from <strong>proxyAddresses</strong>, if the <strong>UseNormalizationRules</strong> CMS setting is FALSE; otherwise it behaves the same as when the flag bit is 0x1000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-235">0x4000</span><span class="sxs-lookup"><span data-stu-id="aa671-235">0x4000</span></span></p></td>
<td><p><span data-ttu-id="aa671-236">Wenn festgelegt, enthält der Adressbuch Server keine Objekte in der Tabelle AbUserEntry-Tabelle, die diesen Wert für das angegebene Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aa671-236">If set, Address Book Server does not include objects in the AbUserEntry table that have this value for the specified attribute.</span></span> <span data-ttu-id="aa671-237">Wenn beispielsweise für das <strong>Attribut msRTCSIP-PrimaryUserAddress-</strong> Attribut dieses Flag-Bit festgesetzt ist, werden Kontakte mit diesem Attribut nicht in die Datenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa671-237">For example, if the <strong>msRTCSIP-PrimaryUserAddress</strong> attribute has this flag bit set, then contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-238">0X8000</span><span class="sxs-lookup"><span data-stu-id="aa671-238">0x8000</span></span></p></td>
<td><p><span data-ttu-id="aa671-239">Wenn festgelegt, enthält der Adressbuch Server keine Objekte in der Tabelle AbUserEntry-Tabelle, die diesen Wert für das angegebene Attribut nicht aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aa671-239">If set, Address Book Server does not include objects in the AbUserEntry table that do not have this value for the specified attribute.</span></span> <span data-ttu-id="aa671-240">Wenn sowohl die 0x4000-als auch die 0X8000-Flag-Bits für ein Objekt gesetzt sind, hat das Attribut mit dem Flag-Bit-Wert, der auf 0x4000 gesetzt ist, Vorrang, und das Objekt wird aus der Tabelle AbUserEntry-Tabelle ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aa671-240">If both the 0x4000 and 0x8000 flag bits are set on an object, the attribute with the flag bit value set to 0x4000 takes precedence, and the object is excluded from the AbUserEntry table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-241">0x10000</span><span class="sxs-lookup"><span data-stu-id="aa671-241">0x10000</span></span></p></td>
<td><p><span data-ttu-id="aa671-242">Wenn diese Einstellung eingestellt ist, stellt dies ein Group-Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="aa671-242">If set, this represents a group object.</span></span> <span data-ttu-id="aa671-243">Der Benutzerreplikationsdienst verwendet dieses Flag-Bit, um Kontakte mit dem <strong>GroupType</strong> -Attribut einzubeziehen, deren Anwesenheitsstatus auf eine Gruppe (beispielsweise eine Verteilerliste oder eine Sicherheitsgruppe) hinweist.</span><span class="sxs-lookup"><span data-stu-id="aa671-243">User Replicator uses this flag bit to include contacts with the <strong>groupType</strong> attribute whose presence indicates a group (for example, a distribution list or security group).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-244">0x20000</span><span class="sxs-lookup"><span data-stu-id="aa671-244">0x20000</span></span></p></td>
<td><p><span data-ttu-id="aa671-245">Ist dieser Wert festzulegen, verwendet der Benutzerreplikationsdienst dieses Flag-Bit, um dieses Attribut in gerätespezifische Adressbuch Server Dateien (also Dateien mit der Erweiterung ". kleckse") einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="aa671-245">If set, User Replicator uses this flag bit to include this attribute in device-specific Address Book Server files (that is, files with a .dabs extension).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aa671-246">In früheren Versionen von lync Server musste der Administrator beim Anwenden einer Änderung an Active Directory die Windows PowerShell-Cmdlets **Update-CSUserDatabase** und **Update – CSAddressBook** ausführen, um die Änderung an der lync Server-Benutzerdatenbank und der RTCab-Datenbank sofort beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="aa671-246">In previous versions of Lync Server, when applying a change to Active Directory, the administrator would be required to run **Update -CSUserDatabase** and **Update –CSAddressBook** Windows PowerShell cmdlets to persist the change to the Lync Server user database and RTCab database immediately.</span></span> <span data-ttu-id="aa671-247">In lync Server 2013 wird der lync Server-Benutzerreplikationsdienst die Änderungen aus Active Directory aufnehmen und die lync Server-Benutzerdatenbank basierend auf einem konfigurierten Intervall aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="aa671-247">In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval.</span></span> <span data-ttu-id="aa671-248">Der lync Server-Benutzerreplikationsdienst gibt die Änderungen auch schnell an die RTCab-Datenbank weiter, ohne dass der Administrator Update-CSAddressBook ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="aa671-248">Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook.</span></span> <span data-ttu-id="aa671-249">Wenn die Adressbuch-Webabfrage aktiviert ist, werden die Änderungen in den Suchergebnissen von lync-Clients wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-249">If Address Book Web query is enabled, then the changes will be reflected in search results by Lync clients.</span></span> <span data-ttu-id="aa671-250">Administratoren müssen nur Update-CSAddressBook ausführen, wenn der Download der Adressbuchdatei aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="aa671-250">Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="aa671-251">Standardmäßig wird der lync Server-Benutzerreplikationsdienst automatisch alle 5 Minuten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa671-251">By default Lync Server User Replicator runs automatically every 5 minutes.</span></span> <span data-ttu-id="aa671-252">Sie können dieses Intervall mithilfe von "Satz-CSUserReplicatorConfiguration-ReplicationCycleInterval" konfigurieren &lt; &gt; .</span><span class="sxs-lookup"><span data-stu-id="aa671-252">You can configure this interval by using Set -CSUserReplicatorConfiguration -ReplicationCycleInterval &lt;&gt;.</span></span>



</div>

</div>

<div>

## <a name="filtering-the-address-book"></a><span data-ttu-id="aa671-253">Filtern des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="aa671-253">Filtering the Address Book</span></span>

<span data-ttu-id="aa671-254">Die in den Adressbuch Server Dateien aufgefüllten Benutzer können basierend auf bestimmten Active Directory-Domänendienst Attributen, die in der AbAttribute-Tabelle aufgelistet sind, gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="aa671-254">The users populated in the Address Book Server files can be controlled based on certain Active Directory Domain Services attributes listed in the AbAttribute table.</span></span> <span data-ttu-id="aa671-255">Ein solches Attribut, das für die Filterung verwendet wird, ist das **msExchangeHideFromAddressBook** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="aa671-255">One such attribute used for filtering is the **msExchangeHideFromAddressBook** attribute.</span></span> <span data-ttu-id="aa671-256">Hierbei handelt es sich um ein vom Exchange-Schema hinzugefügtes Benutzerattribut.</span><span class="sxs-lookup"><span data-stu-id="aa671-256">This is a user attribute added by the Exchange schema.</span></span> <span data-ttu-id="aa671-257">Wenn der Wert dieses Attributs wahr ist, verwendet Exchange Server dieses Attribut zum Ausblenden des Kontakts aus der globalen Outlook-Adressliste (GAL).</span><span class="sxs-lookup"><span data-stu-id="aa671-257">If the value of this attribute is TRUE, Exchange Server uses this attribute to hide the contact from the Outlook Global Address List (GAL).</span></span> <span data-ttu-id="aa671-258">Wenn der Wert dieses Attributs auf "true" festgelegt ist, enthält der Benutzerreplikationsdienst diesen Benutzer in der Tabelle AbUserEntry-Tabelle nicht, und dieser Benutzer befindet sich nicht in den Adressbuch Server Dateien.</span><span class="sxs-lookup"><span data-stu-id="aa671-258">Similarly, if the value of this attribute is TRUE, User Replicator does not include that user in the AbUserEntry table and this user will not be in the Address Book Server files.</span></span>

<span data-ttu-id="aa671-259">Sie können einige Flag-Bits verwenden, um einen Filter für die Verwendung in Adressbuch Server Attributen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="aa671-259">You can use some flag bits to define a filter to use on Address Book Server attributes.</span></span> <span data-ttu-id="aa671-260">So kann beispielsweise das vorhanden sein bestimmter kennzeichenbits ein Attribut als Include-Attribut oder Exclude-Attribut identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aa671-260">For example, the presence of certain flag bits can identify an attribute as an include attribute or an exclude attribute.</span></span> <span data-ttu-id="aa671-261">Der Benutzerreplikationsdienst filtert Kontakte aus, die ein Exclude-Attribut enthalten, und filtert Contains, die kein Include-Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa671-261">User Replicator filters out contacts that contain an exclude attribute and filters out contains that do not contain an include attribute.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="aa671-262">Weitere Informationen zum Filtern des Adressbuchs finden Sie unter <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Adressbuch Server-Cmdlets in lync Server 2013</A>und <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filtern des lync 2013-Adressbuchs</A> .</span><span class="sxs-lookup"><span data-stu-id="aa671-262">For more information about filtering the Address Book, see <A href="https://technet.microsoft.com/library/gg415643(v=ocs.15)">Address Book Server cmdlets in Lync Server 2013</A>, and <A href="https://go.microsoft.com/fwlink/?linkid=330430">Filter Lync 2013 address book</A></span></span>



</div>

<span data-ttu-id="aa671-263">Derzeit gibt es drei verschiedene Filter.</span><span class="sxs-lookup"><span data-stu-id="aa671-263">Currently, there are three different filters.</span></span> <span data-ttu-id="aa671-264">In der folgenden Tabelle sind diese Filter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="aa671-264">The following table lists these filters.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa671-265">Attribut</span><span class="sxs-lookup"><span data-stu-id="aa671-265">Attribute</span></span></th>
<th><span data-ttu-id="aa671-266">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa671-266">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa671-267">0x800</span><span class="sxs-lookup"><span data-stu-id="aa671-267">0x800</span></span></p></td>
<td><p><span data-ttu-id="aa671-268">Wenn festzulegen, wird ein erforderliches Attribut für einen Kontakt angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-268">If set, this identifies a required attribute for a contact.</span></span> <span data-ttu-id="aa671-269">Der Benutzerreplikationsdienst verwendet dieses Flag-Bit, um Kontakte zu filtern, die nicht mindestens ein erforderliches Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa671-269">User Replicator uses this flag bit to filter out contacts that do not contain at least one required attribute.</span></span> <span data-ttu-id="aa671-270">OuPathId ist ein erforderliches Attribut, das immer gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="aa671-270">The OuPathId is a required attribute, which is always set.</span></span> <span data-ttu-id="aa671-271">Daher sollte mindestens eines der anderen erforderlichen Attribute festzulegen sein.</span><span class="sxs-lookup"><span data-stu-id="aa671-271">So at least one of other required attributes should be set.</span></span> <span data-ttu-id="aa671-272">Andernfalls wird der Kontakt (mit dem Wert des required-Attributs OuPathId) immer noch nicht in die Datenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa671-272">Otherwise, contact (that is, with value of required attribute OuPathId) will still not be written to database.</span></span> <span data-ttu-id="aa671-273">Wenn beispielsweise <strong>telephoneNumber</strong> und <strong>homePhone</strong> als erforderliche Attribute definiert sind, werden nur die Kontakte, die mindestens eines dieser Attribute aufweisen, in die Datenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa671-273">For example, if <strong>telephoneNumber</strong> and <strong>homePhone</strong> are defined as required attributes, only the contacts that have at least one of these attributes are written to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa671-274">0x4000</span><span class="sxs-lookup"><span data-stu-id="aa671-274">0x4000</span></span></p></td>
<td><p><span data-ttu-id="aa671-275">Wenn festzulegen, wird ein Exclude-Attribut identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa671-275">If set, this identifies an exclude attribute.</span></span> <span data-ttu-id="aa671-276">Der Benutzerreplikationsdienst verwendet dieses Flag-Bit, um Kontakte zu filtern, die dieses Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa671-276">User Replicator uses this flag bit to filter out contacts that contain this attribute.</span></span> <span data-ttu-id="aa671-277">Wenn beispielsweise <strong>Attribut msRTCSIP-PrimaryUserAddress</strong> als Exclude-Attribut definiert ist, werden Kontakte mit diesem Attribut nicht in die Datenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa671-277">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an exclude attribute, contacts that have this attribute are not written to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa671-278">0X8000</span><span class="sxs-lookup"><span data-stu-id="aa671-278">0x8000</span></span></p></td>
<td><p><span data-ttu-id="aa671-279">Wenn festzulegen, wird ein Include-Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-279">If set, this identifies an include attribute.</span></span> <span data-ttu-id="aa671-280">Der Benutzerreplikationsdienst verwendet dieses Flag-Bit, um Kontakte zu filtern, die dieses Attribut nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa671-280">User Replicator uses this flag bit to filter out contacts that do not contain this attribute.</span></span> <span data-ttu-id="aa671-281">Wenn beispielsweise <strong>Attribut msRTCSIP-PrimaryUserAddress</strong> als Include-Attribut definiert ist, werden nur die Kontakte, die dieses Attribut aufweisen, in die Datenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa671-281">For example, if <strong>msRTCSIP-PrimaryUserAddress</strong> is defined as an include attribute, only the contacts that have this attribute are written to the database.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="aa671-282">Wenn sowohl das 0x4000 (Exclude-Attribut) als auch das 0X8000 (Include-Attribut)-Flag-Bits gesetzt sind, überschreibt das 0x4000-Bit das 0X8000-Bit, und der Kontakt wird ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="aa671-282">If both the 0x4000 (exclude attribute) and 0x8000 (include attribute) flag bits are set, the 0x4000 bit overrides the 0x8000 bit and the contact is excluded.</span></span>



</div>

<span data-ttu-id="aa671-283">Zwar können Sie das Adressbuch so filtern, dass nur bestimmte Benutzer eingeschlossen werden, aber das Einschränken von Einträgen schränkt nicht die Möglichkeit anderer Benutzer ein, die gefilterten Benutzer zu kontaktieren oder Ihren Anwesenheitsstatus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aa671-283">Although you can filter the Address Book to include only certain users, limiting entries does not limit other users' ability to contact the filtered users or to see their presence status.</span></span> <span data-ttu-id="aa671-284">Benutzer können jederzeit Sofortnachrichten suchen, manuell senden oder Anrufe an Benutzer, die sich nicht im Adressbuch befinden, manuell initiieren, indem Sie den vollständigen Anmeldenamen eines Benutzers eingeben.</span><span class="sxs-lookup"><span data-stu-id="aa671-284">Users can always find, manually send instant messages, or manually initiate calls to users not in the Address Book by entering a user's complete sign-in name.</span></span> <span data-ttu-id="aa671-285">Auch Kontaktinformationen für einen Benutzer finden Sie in Outlook.</span><span class="sxs-lookup"><span data-stu-id="aa671-285">Also, contact information for a user could also be found in Outlook.</span></span>

<span data-ttu-id="aa671-286">Wenn Sie mit den vollständigen Kontaktdatensätzen in den Adressbuchdateien die Verwendung von lync Server zum Initiieren von e-Mail-Nachrichten, Telefonen oder Enterprise-VoIP-Anrufen (Wenn Enterprise-VoIP auf dem Server aktiviert ist) mit Benutzern ermöglichen, die nicht für SIP (Session Initiation Protocol) konfiguriert sind, möchten einige Organisationen nur SIP-fähige Benutzer in Ihre</span><span class="sxs-lookup"><span data-stu-id="aa671-286">While having full contact records in the Address Book files enables you to use Lync Server to initiate email, telephone, or Enterprise Voice calls (that is, if Enterprise Voice is enabled on the server) with users that are not configured for Session Initiation Protocol (SIP), some organizations prefer to include only SIP-enabled users in their Address Book Server entries.</span></span> <span data-ttu-id="aa671-287">Sie können das Adressbuch so filtern, dass nur SIP-fähige Benutzer eingeschlossen werden, indem Sie das 0x800-Bit in der Spalte **Flags** der folgenden erforderlichen Attribute löschen: **mailNickname**, **telephoneNumber**, **homePhone** und **Handy**.</span><span class="sxs-lookup"><span data-stu-id="aa671-287">You can filter the Address Book to include only SIP-enabled users by clearing the 0x800 bit in the **Flags** column of the following required attributes: **mailNickname**, **telephoneNumber**, **homePhone**, and **mobile**.</span></span> <span data-ttu-id="aa671-288">Sie können das Adressbuch auch filtern, um nur SIP-fähige Benutzer einzubeziehen, indem Sie das 0X8000 (Include-Attribut) in der Spalte **Flags** des **Attribut msRTCSIP-PrimaryUserAddress-** Attributs festlegen.</span><span class="sxs-lookup"><span data-stu-id="aa671-288">You can also filter the Address Book to include only SIP-enabled users by setting the 0x8000 (include attribute) in the **Flags** column of the **msRTCSIP-PrimaryUserAddress** attribute.</span></span> <span data-ttu-id="aa671-289">Dadurch können auch Dienstkonten aus den Adressbuchdateien ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="aa671-289">This also helps to exclude service accounts from the Address Book files.</span></span>

<span data-ttu-id="aa671-290">Nachdem Sie die AbAttribute-Tabelle geändert haben, können Sie die Daten in der Tabelle AbUserEntry-Tabelle aktualisieren, indem Sie den Befehl Cmdlet **Update-CsUserDatabase** ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa671-290">After you modify the AbAttribute table, you can refresh the data in the AbUserEntry table by running the cmdlet **Update-CsUserDatabase** command.</span></span> <span data-ttu-id="aa671-291">Nach Abschluss der ur-Replikation können Sie die Datei im Dateispeicher des Adressbuchservers aktualisieren, indem Sie den Befehl Cmdlet **UpdateCsAddressBook** manuell ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa671-291">After UR replication completes, you can update the file in the Address Book Server file store by manually running the cmdlet **UpdateCsAddressBook** command.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="aa671-292">Der Front-End-Server, auf dem der Adressbuchserver gespeichert ist, kann nicht administrativ konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="aa671-292">The Front End Server that the Address Book Server is placed is not administratively configurable.</span></span> <span data-ttu-id="aa671-293">Eine wird während der Bereitstellung ausgewählt – in der Regel der erste bereitgestellte Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="aa671-293">One is chosen during deployment—typically, the first Front End Server deployed.</span></span> <span data-ttu-id="aa671-294">Bei einem Fehler wechselt der Adressbuchdienst zu einem anderen Front-End-Server und erfordert keine administrative Beachtung.</span><span class="sxs-lookup"><span data-stu-id="aa671-294">In the event of failure, the Address Book Service will move to another Front End Server, and requires no administrative attention.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="aa671-295">Wenn Sie Ihre Infrastruktur von einer Bereitstellung mit mehreren Gesamtstrukturen oder von einer übergeordneten/untergeordneten Bereitstellung konsolidiert oder anderweitig geändert haben (wie etwa das Konsolidieren Ihrer Infrastruktur vor dem Wechsel zu lync Server), stellen Sie möglicherweise fest, dass der Download des Adressbuchdiensts und die Adressbuch-Webabfrage für einige Benutzer fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="aa671-295">If you have consolidated or otherwise modified your infrastructure from a multi-forest deployment or a parent/child deployment (such as consolidating your infrastructure before moving to Lync Server), you may find that the Address Book service download and the Address Book Web Query fails for some users.</span></span> <span data-ttu-id="aa671-296">Bei einer Bereitstellung mit mehreren Domänen oder Gesamtstrukturen wird das Attribut <STRONG>Attribut msRTCSIP-OriginatorSid</STRONG> für die Benutzerobjekte aufgefüllt, die das Problem aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aa671-296">When in a deployment that had multiple domains or forests, the attribute <STRONG>MsRTCSIP-OriginatorSid</STRONG> is populated on the user objects that are exhibiting the issue.</span></span> <span data-ttu-id="aa671-297">Das <STRONG>Attribut msRTCSIP-OriginatorSid-</STRONG> Attribut muss für diese Objekte auf Null festgesetzt werden, um das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="aa671-297">The <STRONG>MsRTCSIP-OriginatorSid</STRONG> attribute must be set to NULL on these objects to resolve the issue.</span></span>



<span data-ttu-id="aa671-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa671-298"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

