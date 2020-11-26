---
title: 'Lync Server 2013: Konfigurieren der Tabelle nicht zugewiesener Nummern'
description: 'Lync Server 2013: Konfigurieren der Tabelle "nicht zugewiesene Nummern"'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the unassigned number table
ms:assetid: eaa01986-e92f-4328-acf6-4e46c4306a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399053(v=OCS.15)
ms:contentKeyID: 48185908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ed8ba6c709311dab791b711d6ba69aaff72a630
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433598"
---
# <a name="configure-the-unassigned-number-table-in-lync-server-2013"></a><span data-ttu-id="18a41-103">Konfigurieren der Tabelle nicht zugewiesener Nummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="18a41-103">Configure the unassigned number table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="18a41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="18a41-104">

<span> </span></span></span>

<span data-ttu-id="18a41-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="18a41-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="18a41-106">In lync Server 2013 können Sie angeben, was mit eingehenden Anrufen von Telefonnummern geschieht, die für Ihre Organisation gültig sind, aber keinem Benutzer oder Telefon zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="18a41-106">In Lync Server 2013, you can specify what happens to incoming calls to phone numbers that are valid for your organization, but are not assigned to a user or phone.</span></span> <span data-ttu-id="18a41-107">Anrufer können eine Nachricht hören oder an ein anderes Ziel oder beides weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="18a41-107">Callers can hear a message, or can be routed to another destination, or both.</span></span>

<span data-ttu-id="18a41-p102">Wie Sie die Tabelle nicht zugewiesener Rufnummern konfigurieren, richtet sich danach, wie Sie diese verwenden möchten. Sie können die Tabelle mit allen gültigen Durchwahlnummern für Ihre Organisation konfigurieren, nur mit nicht zugewiesenen Durchwahlnummern oder als eine Kombination beider Nummerntypen. Die Tabelle nicht zugewiesener Rufnummern kann sowohl zugewiesene als auch nicht zugewiesene Rufnummern enthalten, wird jedoch nur ausgelöst, wenn ein Anrufer eine derzeit nicht zugewiesene Rufnummer wählt. Wenn Sie alle gültigen Durchwahlnummern in die Tabelle nicht zugewiesener Nummern aufnehmen, können Sie eine Aktion angeben, die bei Ausscheiden eines Mitarbeiters aus der Organisation ausgeführt werden soll. In diesem Fall ist eine Neukonfiguration der Tabelle nicht erforderlich. Wenn Sie nicht zugewiesene Durchwahlnummern in die Tabelle aufnehmen, können Sie die Aktion anpassen, die für bestimmte Nummern ausgeführt wird. Wenn Sie beispielsweise die Durchwahlnummer für Ihren Kundendienst ändern, können Sie die alte Rufnummer des Kundendiensts in die Tabelle aufnehmen und ihr dann eine Ansage zuweisen, in der die neue Rufnummer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="18a41-p102">How you configure the unassigned number table depends on how you want to use it. You can configure the table with all the valid extensions for your organization, with only unassigned extensions, or with a combination of both types of numbers. The unassigned number table can include both assigned and unassigned numbers, but it is invoked only when a caller dials a number that is not currently assigned. If you include all the valid extensions in the unassigned number table, you can specify the action that occurs whenever someone leaves your organization, without needing to reconfigure the table. If you include unassigned extensions in the table, you can modify the action that occurs for specific numbers. For example, if you change the extension for your customer service desk, you can include the old customer service number in the table and then assign it to an announcement that provides the new number.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="18a41-114">Bevor Sie die Tabelle "nicht zugewiesene Nummern" konfigurieren, muss Ihr System bereits Ankündigungen definiert haben oder eine automatische UM-Telefonzentrale (Exchange Unified Messaging) eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="18a41-114">Before you configure the unassigned number table, your system must already either have Announcements defined or an Exchange Unified Messaging (UM) Auto Attendant set up.</span></span>



</div>

<div>


> [!TIP]  
> <span data-ttu-id="18a41-115">Wenn jemand eine nicht zugewiesene Nummer anruft, durchsucht lync Server die Tabelle nicht zugewiesene Nummern von oben nach unten und verwendet den ersten übereinstimmenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="18a41-115">When someone calls an unassigned number, Lync Server searches the unassigned number table from top to bottom and uses the first matching range.</span></span> <span data-ttu-id="18a41-116">Sie sollten also als letzte Lösungsmöglichkeit eine Aktion definieren, die für den letzten Bereich in der Tabelle ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="18a41-116">Therefore, an action that you want to be performed as a last resort should be specified for the last range in the table.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="18a41-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="18a41-117">In This Section</span></span>

<span data-ttu-id="18a41-118">[Erstellen oder Ändern eines nicht zugewiesenen Nummernbereichs in lync Server 2013](lync-server-2013-create-or-modify-an-unassigned-number-range.md) [Erstellen einer Ankündigung in lync Server 2013](lync-server-2013-create-an-announcement.md)</span><span class="sxs-lookup"><span data-stu-id="18a41-118">[Create or modify an unassigned number range in Lync Server 2013](lync-server-2013-create-or-modify-an-unassigned-number-range.md) [Create an announcement in Lync Server 2013](lync-server-2013-create-an-announcement.md)</span></span>

<span data-ttu-id="18a41-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="18a41-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

