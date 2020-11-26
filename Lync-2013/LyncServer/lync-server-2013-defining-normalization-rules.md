---
title: 'Lync Server 2013: Definieren von Normalisierungsregeln'
description: 'Lync Server 2013: Definieren von Normalisierungsregeln'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a123e17b1d3256781ff34e4cade2b344ba8fe14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430994"
---
# <a name="defining-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="e7812-103">Definieren von Normalisierungsregeln in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7812-103">Defining normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7812-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7812-104">

<span> </span></span></span>

<span data-ttu-id="e7812-105">_**Letztes Änderungsdatum des Themas:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="e7812-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="e7812-106">Lync Server 2013-Normalisierungsregeln verwenden reguläre .NET Framework-Ausdrücke, um gewählte Telefonnummern in das E. 164-Format zu übersetzen. mit anderen Worten: Normalisierungsregeln nehmen die von einem Benutzer gewählte Telefonnummer an und wandeln diese Zahl in das von lync Server intern verwendete Format um.</span><span class="sxs-lookup"><span data-stu-id="e7812-106">Lync Server 2013 normalization rules use .NET Framework regular expressions to translate dialed phone numbers to E.164 format; in other words, normalization rules take the phone number dialed by a user and convert that number to the format used internally by Lync Server.</span></span> <span data-ttu-id="e7812-107">Jedem Wählplan muss mindestens eine Normalisierungsregel zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="e7812-107">Each dial plan must be assigned one or more normalization rules.</span></span>

<span data-ttu-id="e7812-108">Details zu Normalisierungsregeln finden Sie unter [Wählpläne und Normalisierungsregeln in lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="e7812-108">For details about normalization rules, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.</span></span>

<span data-ttu-id="e7812-109">Ausführliche Informationen zum Schreiben regulärer Ausdrücke finden Sie unter ".NET Framework-reguläre Ausdrücke" unter [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927) .</span><span class="sxs-lookup"><span data-stu-id="e7812-109">For details about how to write regular expressions, see ".NET Framework Regular Expressions" at [https://go.microsoft.com/fwlink/p/?linkId=140927](https://go.microsoft.com/fwlink/p/?linkid=140927).</span></span>

<span data-ttu-id="e7812-110">Mithilfe einer der folgenden Methoden können Sie eine Normalisierungsregel definieren oder bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="e7812-110">You can use either of the following methods to define or edit a normalization rule:</span></span>

  - <span data-ttu-id="e7812-111">Verwenden Sie das Tool **Normalisierungsregel erstellen** , um Werte für die Anfangsziffern, die Länge, die zu entfernenden Ziffern und die zu addierenden Ziffern anzugeben, und lassen Sie dann die lync Server-Systemsteuerung das entsprechende Übereinstimmungsmuster und die entsprechende Übersetzungsregel generieren.</span><span class="sxs-lookup"><span data-stu-id="e7812-111">Use the **Build a Normalization Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.</span></span>

  - <span data-ttu-id="e7812-112">Schreiben Sie reguläre Ausdrücke manuell, um das übereinstimmende Muster und die Übersetzungsregel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e7812-112">Write regular expressions manually to define the matching pattern and translation rule.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e7812-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e7812-113">In This Section</span></span>

  - [<span data-ttu-id="e7812-114">Erstellen oder Ändern einer Normalisierungsregel mithilfe der Regel zum Erstellen einer Normalisierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7812-114">Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [<span data-ttu-id="e7812-115">Manuelles Erstellen oder Ändern einer Normalisierungsregel in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7812-115">Create or modify a normalization rule manually in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e7812-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7812-116">See Also</span></span>


[<span data-ttu-id="e7812-117">Erstellen eines Wählplans in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7812-117">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="e7812-118">Ändern eines Wählplans in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7812-118">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="e7812-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7812-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

