---
title: 'Lync Server 2013: Telefone im öffentlichen Bereich'
description: 'Lync Server 2013: Telefone im öffentlichen Bereich.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Common area phones
ms:assetid: d63bb3de-154e-4347-9251-9fa94e7d593a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994076(v=OCS.15)
ms:contentKeyID: 51803987
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af8a68f875bba1d43a91e5a252259841d7a6bbda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395242"
---
# <a name="common-area-phones-in-lync-server-2013"></a><span data-ttu-id="045c0-103">Telefone im öffentlichen Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="045c0-103">Common area phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="045c0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="045c0-104">

<span> </span></span></span>

<span data-ttu-id="045c0-105">_**Letztes Änderungsdatum des Themas:** 2013-02-20_</span><span class="sxs-lookup"><span data-stu-id="045c0-105">_**Topic Last Modified:** 2013-02-20_</span></span>

<span data-ttu-id="045c0-106">Telefone im öffentlichen Bereich sind IP-Telefone, die keinem einzelnen Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="045c0-106">Common area phones are IP phones that are not associated with an individual user.</span></span> <span data-ttu-id="045c0-107">Statt sich im Büro einer anderen Person zu befinden, befinden sich die Telefone im öffentlichen Bereich in der Regel in Gebäude-Lobbies, Cafeterias, Mitarbeiter-Lounges, Besprechungsräumen und anderen Orten, an denen sich eine große Anzahl von Personen wahrscheinlich versammeln wird.</span><span class="sxs-lookup"><span data-stu-id="045c0-107">Instead of being located in someone’s office, common area phones are typically located in building lobbies, cafeterias, employee lounges, meeting rooms, and other locations where a large number of people are likely to gather.</span></span> <span data-ttu-id="045c0-108">Im Gegensatz zu anderen Telefonen in lync Server, die in der Regel mithilfe von VoIP-Richtlinien und Wählplänen verwaltet werden, die einzelnen Benutzern zugewiesen sind, sind für Telefone im öffentlichen Bereich keine einzelnen Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="045c0-108">Unlike other phones in Lync Server, which are typically maintained by using voice policies and dial plans that are assigned to individual users, common area phones do not have individual users assigned to them.</span></span> <span data-ttu-id="045c0-109">Das bedeutet, dass Sie anders als Ihre anderen Telefone verwaltet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="045c0-109">This means that they must be managed differently than your other phones.</span></span>

<span data-ttu-id="045c0-110">Zum Verwalten von Telefonen im allgemeinen Bereich erstellen Sie für alle Ihre Telefone im öffentlichen Bereich Active Directory-Domänendienste, denen wie Benutzerkonten Richtlinien und sprach Pläne zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="045c0-110">To manage common area phones, you create Active Directory Domain Services contact objects for all your common area phones that, like user accounts, can be assigned policies and voice plans.</span></span> <span data-ttu-id="045c0-111">Dieser Ansatz ermöglicht Ihnen, die Kontrolle über Telefone im öffentlichen Bereich zu behalten, auch wenn diese Telefone keinem einzelnen Benutzer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="045c0-111">This approach enables you to maintain control over common area phones, even though those phones are not associated with an individual user.</span></span>

<span data-ttu-id="045c0-112">Verwenden Sie die Themen in diesem Abschnitt, um zu erfahren, wie Sie Kontaktobjekte für Telefone im allgemeinen Bereich erstellen, diese ändern und löschen sowie Konfigurationsinformationen zu den Telefonen im öffentlichen Bereich in Ihrer Bereitstellung konfigurieren und anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="045c0-112">Use the topics in this section to learn how to create contact objects for common area phones, modify and delete them, and configure and view configuration information about the common area phones in your deployment.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="045c0-113">Sie haben drei Optionen für Telefone im öffentlichen Bereich: das allgemeine Bereichs Telefon Aastra 6721ip, das HP 4110 IP-Telefon und das Polycom CX500 IP-Telefon mit gemeinsamem Bereich.</span><span class="sxs-lookup"><span data-stu-id="045c0-113">You have three options for common area phones: the Aastra 6721ip common area phone, the HP 4110 IP Phone, and the Polycom CX500 IP common area phone.</span></span> <span data-ttu-id="045c0-114">Das Polycom CX3000 IP-Konferenztelefon ist ein weiteres Variant-Telefon im öffentlichen Bereich.</span><span class="sxs-lookup"><span data-stu-id="045c0-114">The Polycom CX3000 IP conferencing phone is another variant common area phone.</span></span> <span data-ttu-id="045c0-115">Sie ist jedoch für die Verwendung in Konferenzräumen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="045c0-115">However, it is intended for use in conference rooms.</span></span> <span data-ttu-id="045c0-116">Ausführliche Informationen zu Telefonen im öffentlichen Bereich finden Sie im Abschnitt Telefone im allgemeinen Bereich unter <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Auswählen neuer Geräte</A>.</span><span class="sxs-lookup"><span data-stu-id="045c0-116">For details about common area phones, see the Common Area Phones section of <A href="https://technet.microsoft.com/library/gg398958(v=ocs.14).aspx">Choosing New Devices</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="045c0-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="045c0-117">In This Section</span></span>

  - [<span data-ttu-id="045c0-118">Anzeigen von allgemeinen Telefon Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="045c0-118">View common area phone information in Lync Server 2013</span></span>](lync-server-2013-view-common-area-phone-information.md)

  - [<span data-ttu-id="045c0-119">Erstellen oder Ändern eines Telefon Kontaktobjekts in einem gemeinsamen Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="045c0-119">Create or modify a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="045c0-120">Aktivieren oder Deaktivieren von Hot Desking in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="045c0-120">Enable or disable hot desking in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-hot-desking.md)

  - [<span data-ttu-id="045c0-121">Löschen eines Kontaktobjekts für einen öffentlichen Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="045c0-121">Delete a common area phone Contact object in Lync Server 2013</span></span>](lync-server-2013-delete-a-common-area-phone-contact-object.md)

  - [<span data-ttu-id="045c0-122">Zuweisen von Richtlinien in lync Server 2013 zu einem Telefon im öffentlichen Bereich</span><span class="sxs-lookup"><span data-stu-id="045c0-122">Assign policies in Lync Server 2013 to a common area phone</span></span>](lync-server-2013-assign-policies-to-a-common-area-phone.md)

<span data-ttu-id="045c0-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="045c0-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

