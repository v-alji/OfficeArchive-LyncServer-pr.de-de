---
title: 'Lync Server 2013: Adressen überprüfen'
description: 'Lync Server 2013: Überprüfen von Adressen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validate addresses
ms:assetid: aae557c9-e6f5-4d23-8af1-1d4cd7968c54
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412808(v=OCS.15)
ms:contentKeyID: 48185108
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bcbb8789912b3bcbcfb60dd79807f06c2957c1f6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446318"
---
# <a name="validate-addresses-in-lync-server-2013"></a><span data-ttu-id="26145-103">Überprüfen von Adressen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="26145-103">Validate addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="26145-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="26145-104">

<span> </span></span></span>

<span data-ttu-id="26145-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="26145-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="26145-106">Bevor Sie die Standortdatenbank veröffentlichen, müssen Sie neue Speicherorte für den Master Street Address Guide (MSAG) überprüfen, der von Ihrem SIP-Stamm oder dem öffentlichen Telefonnetz (PSTN) E9-1-1 Service Provider verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="26145-106">Before publishing the location database, you must validate new locations against the Master Street Address Guide (MSAG) that is maintained by your SIP trunk or public switched telephone network (PSTN) E9-1-1 service provider.</span></span>

<span data-ttu-id="26145-107">Ausführliche Informationen zu SIP Trunk E9-1-1 Serviceanbietern finden Sie unter [Auswählen eines E9-1-1-Dienstanbieters für lync Server 2013](lync-server-2013-choosing-an-e9-1-1-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="26145-107">For details about SIP trunk E9-1-1 service providers, see [Choosing an E9-1-1 service provider for Lync Server 2013](lync-server-2013-choosing-an-e9-1-1-service-provider.md).</span></span>

<span data-ttu-id="26145-108">Details zur Überprüfung von Adressen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="26145-108">For details about validating addresses, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - <span data-ttu-id="26145-109">**Get-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="26145-109">**Get-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="26145-110">**Satz-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="26145-110">**Set-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="26145-111">**Remove-CsLisServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="26145-111">**Remove-CsLisServiceProvider**</span></span>

  - <span data-ttu-id="26145-112">**Get-CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="26145-112">**Get-CsLisCivicAddress**</span></span>

  - <span data-ttu-id="26145-113">**Test-CsLisCivicAddress**</span><span class="sxs-lookup"><span data-stu-id="26145-113">**Test-CsLisCivicAddress**</span></span>

<div>

## <a name="to-validate-addresses-located-in-the-location-database"></a><span data-ttu-id="26145-114">So überprüfen Sie Adressen in der Standortdatenbank auf Gültigkeit</span><span class="sxs-lookup"><span data-stu-id="26145-114">To validate addresses located in the location database</span></span>

1.  <span data-ttu-id="26145-115">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="26145-115">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="26145-116">Führen Sie die folgenden Cmdlets zum Konfigurieren der Verbindung mit dem Anbieter für die Notrufunterstützung aus.</span><span class="sxs-lookup"><span data-stu-id="26145-116">Run the following cmdlets to configure the emergency service provider connection.</span></span>
    
        $pwd = Read-Host -AsSecureString <password>
        Set-CsLisServiceProvider -ServiceProviderName Provider1 -ValidationServiceUrl <URL provided by provider> -CertFileName <location of certificate provided by provider> -Password $pwd

3.  <span data-ttu-id="26145-117">Führen das folgende Cmdlet zum Überprüfen der Gültigkeit von Adressen in der Standortdatenbank aus.</span><span class="sxs-lookup"><span data-stu-id="26145-117">Run the following cmdlet to validate the addresses in the location database.</span></span>
    
        Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus
    
    <span data-ttu-id="26145-118">Einzelne Adressen können Sie auch mit dem Cmdlet **Test-CsLisCivicAddress** validieren.</span><span class="sxs-lookup"><span data-stu-id="26145-118">You can also use the **Test-CsLisCivicAddress** cmdlet to validate individual addresses.</span></span>

<span data-ttu-id="26145-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="26145-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

