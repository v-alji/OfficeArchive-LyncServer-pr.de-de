---
title: 'Lync Server 2013: Kontaktobjektverwaltung für gehostete Exchange-Dienste'
description: 'Lync Server 2013: Hosted Exchange Contact-Objektverwaltung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Contact object management
ms:assetid: eead9d76-bc4f-4c1c-9779-683cb7a88410
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412978(v=OCS.15)
ms:contentKeyID: 48185748
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 691bcea10d3a4f8b523c6565f384d6c4c9a2a2a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427621"
---
# <a name="hosted-exchange-contact-object-management-in-lync-server-2013"></a><span data-ttu-id="f9da1-103">Kontaktobjektverwaltung für gehostete Exchange-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9da1-103">Hosted Exchange Contact object management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9da1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9da1-104">

<span> </span></span></span>

<span data-ttu-id="f9da1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="f9da1-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="f9da1-106">Sie müssen ein Kontaktobjekt für jede Nummer der automatischen Telefonzentrale und die Teilnehmerzugriffsnummer in Ihrer standortübergreifenden Bereitstellung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f9da1-106">You need to configure a Contact object for each auto-attendant number and subscriber access number in your cross-premises deployment.</span></span>

<span data-ttu-id="f9da1-107">Zur Integration in den Hosted Exchange um können ocsumutil.exe keine Kontaktobjekte verwalten, da dies von den Active Directory Exchange um-Einstellungen abhängt.</span><span class="sxs-lookup"><span data-stu-id="f9da1-107">For integration with hosted Exchange UM, ocsumutil.exe cannot be used to manage Contact objects, because it depends on Active Directory Exchange UM settings.</span></span> <span data-ttu-id="f9da1-108">In einer standortübergreifenden Bereitstellung werden lync Server 2013 und gehostete Exchange um in getrennten Gesamtstrukturen installiert, ohne dass Sie vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="f9da1-108">In a cross-premises deployment, Lync Server 2013 and hosted Exchange UM are installed in separate forests with no trust between them.</span></span> <span data-ttu-id="f9da1-109">Aus Sicherheitsgründen haben lync Server 2013-Administratoren keinen direkten Zugriff auf Exchange um-Active Directory-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="f9da1-109">For security reasons, Lync Server 2013 administrators have no direct access to Exchange UM Active Directory settings.</span></span> <span data-ttu-id="f9da1-110">Daher bietet lync Server 2013 ein anderes Modell für die Verwaltung von Kontaktobjekten in einem *freigegebenen SIP-Adressraum* , auf den sowohl lync Server 2013 als auch der gehostete Exchange um-Dienst zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="f9da1-110">As a result, Lync Server 2013 provides a different model for managing Contact objects in a *shared SIP address space* that is accessible to both Lync Server 2013 and the hosted Exchange UM service.</span></span>

<div>

## <a name="hosted-contact-object-workflow"></a><span data-ttu-id="f9da1-111">Workflow für gehostete Kontaktobjekte</span><span class="sxs-lookup"><span data-stu-id="f9da1-111">Hosted Contact Object Workflow</span></span>

<span data-ttu-id="f9da1-112">Im folgenden finden Sie die allgemeinen Schritte für die Zusammenarbeit mit Ihrem Hosted Exchange-mandantenadministrator zum Verwalten von Kontaktobjekten:</span><span class="sxs-lookup"><span data-stu-id="f9da1-112">The following are the general steps for working with your hosted Exchange tenant administrator to manage contact objects:</span></span>

1.  <span data-ttu-id="f9da1-113">Der Exchange-Administrator fordert Telefonnummern für den Exchange um-Abonnenten Zugriff und die automatischen Telefonzentralen-Kontaktobjekte an.</span><span class="sxs-lookup"><span data-stu-id="f9da1-113">The Exchange administrator requests phone numbers for the Exchange UM subscriber access and auto-attendant Contact objects.</span></span>

2.  <span data-ttu-id="f9da1-114">Der lync Server 2013-Administrator erstellt für jede Telefonnummer ein Kontaktobjekt und weist jedem Kontaktobjekt eine Richtlinie für gehostete Voicemail zu.</span><span class="sxs-lookup"><span data-stu-id="f9da1-114">The Lync Server 2013 administrator creates a Contact object for each phone number and assigns a hosted voice mail policy to each Contact object.</span></span>

3.  <span data-ttu-id="f9da1-115">Der lync Server 2013-Administrator stellt die Telefonnummern dem Exchange-Administrator zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f9da1-115">The Lync Server 2013 administrator provides the phone numbers to the Exchange administrator.</span></span>

4.  <span data-ttu-id="f9da1-116">Der Exchange-Administrator ordnet die Telefonnummern den entsprechenden Exchange um-Wählplänen für automatische Telefonzentralen und den Abonnenten Zugriff zu.</span><span class="sxs-lookup"><span data-stu-id="f9da1-116">The Exchange administrator assigns the phone numbers to appropriate Exchange UM dial plans for auto attendants and subscriber access.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f9da1-117">Es ist nicht erforderlich, die Einstellungen für den Wählplan von lync Server 2013 für die Kontaktobjekte so zu konfigurieren, wie dies bei lokalen Bereitstellungen der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="f9da1-117">There is no need to configure any Lync Server 2013 dial plan settings on the Contact objects as there is with on-premises deployments.</span></span>



</div>

</div>

<div>

## <a name="configuring-hosted-contact-objects"></a><span data-ttu-id="f9da1-118">Konfigurieren von gehosteten Kontaktobjekten</span><span class="sxs-lookup"><span data-stu-id="f9da1-118">Configuring Hosted Contact Objects</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f9da1-119">Bevor lync Server 2013-Kontaktobjekte für gehostete Exchange um aktiviert werden können, muss eine für Sie geltende gehostete Voicemail-Richtlinie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9da1-119">Before Lync Server 2013 Contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="f9da1-120">Die Richtlinie kann globaler, Website ebener oder benutzerbezogener Bereich sein, sofern Sie auf das zu aktivierende Kontaktobjekt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9da1-120">The policy can be of global, site-level, or per-user scope, as long as it applies to the contact object you want to enable.</span></span> <span data-ttu-id="f9da1-121">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-hosted-voice-mail-policies.md">Richtlinien für gehostete Voicemail in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f9da1-121">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="f9da1-122">Zum Konfigurieren der in einer lokalen Bereitstellung gehosteten Kontaktobjekte für die automatische Telefonzentrale und den Abonnenten Zugriff müssen Sie die folgenden Cmdlets verwenden:</span><span class="sxs-lookup"><span data-stu-id="f9da1-122">To configure hosted auto-attendant and subscriber access Contact objects in a cross-premises deployment, you must use the following cmdlets:</span></span>

  - <span data-ttu-id="f9da1-123">**New-CsExUmContact** erstellt ein neues Kontaktobjekt für gehostete um.</span><span class="sxs-lookup"><span data-stu-id="f9da1-123">**New-CsExUmContact** creates a new Contact object for hosted UM.</span></span>

  - <span data-ttu-id="f9da1-124">Mit " **CsExUmContact** " wird ein vorhandenes Kontaktobjekt für gehostete Exchange um geändert.</span><span class="sxs-lookup"><span data-stu-id="f9da1-124">**Set-CsExUmContact** modifies an existing Contact object for hosted Exchange UM.</span></span>

<span data-ttu-id="f9da1-125">Im folgenden Beispiel wird ein Kontaktobjekt der automatischen Telefonzentrale erstellt:</span><span class="sxs-lookup"><span data-stu-id="f9da1-125">The following example creates an auto-attendant Contact object:</span></span>

    New-CsExUmContact -SipAddress sip:exumaa1@fabrikam.com -RegistrarPool RedmondPool.litwareinc.com -OU "OU=ExUmContacts,DC=litwareinc,DC=com" -DisplayNumber 2065559876 -AutoAttendant $True

<span data-ttu-id="f9da1-126">In diesem Beispiel wird ein neues Exchange um-Kontaktobjekt mit der SIP-Adresse SIP:exumaa1@fabrikam.com erstellt.</span><span class="sxs-lookup"><span data-stu-id="f9da1-126">This example creates a new Exchange UM Contact object with the SIP address sip:exumaa1@fabrikam.com.</span></span> <span data-ttu-id="f9da1-127">Der Name des Pools, in dem der lync Server 2013-Registrierungsdienst ausgeführt wird, lautet RedmondPool.litwareinc.com.</span><span class="sxs-lookup"><span data-stu-id="f9da1-127">The name of the pool where the Lync Server 2013 Registrar service is running is RedmondPool.litwareinc.com.</span></span> <span data-ttu-id="f9da1-128">Die Active Directory-Organisationseinheit, in der diese Informationen gespeichert werden, ist ou = ExUmContacts, DC = "litwareinc, DC = com.</span><span class="sxs-lookup"><span data-stu-id="f9da1-128">The Active Directory organizational unit where this information will be stored is OU=ExUmContacts,DC=litwareinc,DC=com.</span></span> <span data-ttu-id="f9da1-129">Die Telefonnummer des Kontaktobjekts ist 2065554567.</span><span class="sxs-lookup"><span data-stu-id="f9da1-129">The phone number of the Contact object is 2065554567.</span></span> <span data-ttu-id="f9da1-130">Der Parameter optional – autoattende $true gibt an, dass dieses Objekt ein Kontaktobjekt der automatischen Telefonzentrale ist.</span><span class="sxs-lookup"><span data-stu-id="f9da1-130">The optional -AutoAttendant $True parameter specifies that this object is an auto-attendant Contact object.</span></span> <span data-ttu-id="f9da1-131">Wenn der-autoattender-Parameter auf "false" festgelegt wird (der Standardwert), wird ein Kontaktobjekt des Teilnehmerzugriffs angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9da1-131">Setting the -AutoAttendant parameter to False (the default) specifies a subscriber access Contact object.</span></span>

<span data-ttu-id="f9da1-132">Details zu den New-CsExUmContact-und Set-CsExUmContact-Cmdlets finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="f9da1-132">For details about the New-CsExUmContact and Set-CsExUmContact cmdlets, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="f9da1-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9da1-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

