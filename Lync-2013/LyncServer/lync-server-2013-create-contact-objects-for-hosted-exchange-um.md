---
title: 'Lync Server 2013: Erstellen von Kontaktobjekten für gehostete Exchange UM-Dienste'
description: 'Lync Server 2013: Erstellen von Kontaktobjekten für gehostete Exchange um.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create contact objects for hosted Exchange UM
ms:assetid: a39be52f-488a-4523-ad5f-ce1f0d681959
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412765(v=OCS.15)
ms:contentKeyID: 48185045
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9760e2a39b5182f9b5194e364e059bddc6a63d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431974"
---
# <a name="create-contact-objects-for-hosted-exchange-um-in-lync-server-2013"></a><span data-ttu-id="d704c-103">Erstellen von Kontaktobjekten für gehostete Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d704c-103">Create contact objects for hosted Exchange UM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d704c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d704c-104">

<span> </span></span></span>

<span data-ttu-id="d704c-105">_**Letztes Änderungsdatum des Themas:** 2012-09-24_</span><span class="sxs-lookup"><span data-stu-id="d704c-105">_**Topic Last Modified:** 2012-09-24_</span></span>

<span data-ttu-id="d704c-106">Im folgenden Verfahren wird erläutert, wie Sie die Kontaktobjekte der automatischen Telefonzentrale (AA) oder des Abonnenten Zugriffs (SA) für gehostete Exchange Unified Messaging (um) erstellen.</span><span class="sxs-lookup"><span data-stu-id="d704c-106">The following procedure explains how to create Auto Attendant (AA) or Subscriber Access (SA) contact objects for hosted Exchange Unified Messaging (UM).</span></span>

<span data-ttu-id="d704c-107">Ausführliche Informationen finden Sie unter [gehostete Exchange-Kontaktobjekt Verwaltung in lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="d704c-107">For details, see [Hosted Exchange Contact object management in Lync Server 2013](lync-server-2013-hosted-exchange-contact-object-management.md) in the Planning documentation.</span></span>

<span data-ttu-id="d704c-108">Details zum Konfigurieren von Kontaktobjekten finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d704c-108">For details about configuring contact objects, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="d704c-109">New-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="d704c-109">New-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsExUmContact)

  - [<span data-ttu-id="d704c-110">Set-CsExUmContact</span><span class="sxs-lookup"><span data-stu-id="d704c-110">Set-CsExUmContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsExUmContact)

<div class=" ">


> [!IMPORTANT]  
> <span data-ttu-id="d704c-111">Bevor lync Server 2013-Kontaktobjekte für gehostete Exchange um aktiviert werden können, muss eine für Sie geltende gehostete Voicemail-Richtlinie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d704c-111">Before Lync Server 2013 contact objects can be enabled for hosted Exchange UM, a hosted voice mail policy that applies to them must be deployed.</span></span> <span data-ttu-id="d704c-112">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-hosted-voice-mail-policies.md">Richtlinien für gehostete Voicemail in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="d704c-112">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-create-aa-or-sa-contact-objects-for-hosted-exchange-um"></a><span data-ttu-id="d704c-113">So erstellen Sie AA-oder SA-Kontaktobjekte für gehostete Exchange um</span><span class="sxs-lookup"><span data-stu-id="d704c-113">To create AA or SA contact objects for hosted Exchange UM</span></span>

1.  <span data-ttu-id="d704c-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="d704c-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d704c-115">Führen Sie das New-CsExUmContact-Cmdlet aus, um alle für Ihre Bereitstellung erforderlichen Kontaktobjekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d704c-115">Run the New-CsExUmContact cmdlet to create any contact objects required for your deployment.</span></span> <span data-ttu-id="d704c-116">Führen Sie beispielsweise die folgenden Schritte aus, um ein AA-und ein SA-Kontaktobjekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="d704c-116">For example, run the following to create an AA and an SA contact object:</span></span>
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumaa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101" -AutoAttendant $True
       ```
    
       ```powershell
        New-CsExUmContact -SipAddress "sip:exumsa1@fabrikam.com" -RegistrarPool "RedmondPool.litwareinc.com" -OU "HostedExUM Integration" -DisplayNumber "+14255550101"
       ```
    
    <span data-ttu-id="d704c-117">In diesen Beispielen werden die folgenden Parameter angegeben:</span><span class="sxs-lookup"><span data-stu-id="d704c-117">These examples set the following parameters:</span></span>
    
      - <span data-ttu-id="d704c-118">**SipAddress** gibt die SIP-Adresse des Contact-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="d704c-118">**SipAddress** specifies the SIP address of the contact object.</span></span> <span data-ttu-id="d704c-119">Hierbei muss es sich um eine Adresse handeln, die noch nicht verwendet wurde, um einen Benutzer oder ein Kontaktobjekt in den Active Directory-Domänendiensten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d704c-119">This must be an address that has not already been used to configure a user or contact object in Active Directory Domain Services.</span></span> <span data-ttu-id="d704c-120">Dieser Wert muss das Format "SIP:" aufweisen \<*SIP address*\> , wie in den vorherigen Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d704c-120">This value must be in the format “sip:\<*SIP address*\>“ as shown in the previous examples.</span></span>
    
      - <span data-ttu-id="d704c-121">**RegistrarPool** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Pools an, auf dem der Registrierungsdienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d704c-121">**RegistrarPool** specifies the fully qualified domain name (FQDN) of the pool on which the Registrar service is running.</span></span>
        
        <div class=" ">
        

        > [!NOTE]  
        > <span data-ttu-id="d704c-122">Exchange um-Kontaktobjekte können nicht in Pools verschoben werden, die Bestandteil von lync Server 2013-Bereitstellungen vor lync Server 2013 sind.</span><span class="sxs-lookup"><span data-stu-id="d704c-122">Exchange UM contact objects cannot be moved to pools that are part of Lync Server 2013 deployments prior to Lync Server 2013.</span></span>

        
        </div>
    
      - <span data-ttu-id="d704c-123">**OU** gibt die Active Directory-Organisationseinheit an, in der sich dieses Kontaktobjekt befindet.</span><span class="sxs-lookup"><span data-stu-id="d704c-123">**OU** specifies the Active Directory organizational unit where this contact object will be located.</span></span>
    
      - <span data-ttu-id="d704c-124">**DisplayNumber** gibt die Telefonnummer des Kontaktobjekts an.</span><span class="sxs-lookup"><span data-stu-id="d704c-124">**DisplayNumber** specifies the telephone number of the contact object.</span></span> <span data-ttu-id="d704c-125">Die Telefonnummer für jedes Kontaktobjekt muss eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d704c-125">The phone number for each contact object must be unique.</span></span>
    
      - <span data-ttu-id="d704c-126">**Autoattender** gibt an, ob es sich bei dem Kontaktobjekt um eine automatische Telefonzentrale handelt.</span><span class="sxs-lookup"><span data-stu-id="d704c-126">**AutoAttendant** specifies whether the Contact object is an Auto Attendant.</span></span> <span data-ttu-id="d704c-127">Die automatische Telefonzentrale bietet eine Reihe von Sprachansagen, mit denen Anrufer in das Telefonsystem navigieren und die Partei erreichen können, mit der Sie Kontakt aufnehmen möchten.</span><span class="sxs-lookup"><span data-stu-id="d704c-127">Auto Attendant provides a set of voice prompts that allow callers to navigate the phone system and reach the party that they want to contact.</span></span> <span data-ttu-id="d704c-128">Der Wert **false** (Standardeinstellung) für diesen Parameter gibt ein Kontaktobjekt für den Abonnenten Zugriff an.</span><span class="sxs-lookup"><span data-stu-id="d704c-128">A value of **False** (the default) for this parameter indicates a Subscriber Access contact object.</span></span>

<span data-ttu-id="d704c-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d704c-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

