---
title: Konfigurieren der AutoErmittlung für Mobilität mit hybriden Bereitstellungen
description: Konfigurieren der AutoErmittlung für Mobilität mit hybridbereitstellungen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Autodiscover for mobility with hybrid deployments
ms:assetid: f838af79-d8b4-4122-b81c-7889573d143e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215885(v=OCS.15)
ms:contentKeyID: 48706012
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a66f0045ec1fce65b8e21b6a6f4494b96c93912
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433262"
---
# <a name="configuring-autodiscover-in-lync-server-2013-for-mobility-with-hybrid-deployments"></a><span data-ttu-id="5bd24-103">Konfigurieren der AutoErmittlung in Lync Server 2013 für Mobilität mit hybriden Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="5bd24-103">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5bd24-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5bd24-104">

<span> </span></span></span>

<span data-ttu-id="5bd24-105">_**Letztes Änderungsdatum des Themas:** 2014-06-18_</span><span class="sxs-lookup"><span data-stu-id="5bd24-105">_**Topic Last Modified:** 2014-06-18_</span></span>

<span data-ttu-id="5bd24-106">Hybrid Bereitstellungen sind Konfigurationen, die sowohl den Microsoft lync Online-clouddienst als auch die lokale Bereitstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5bd24-106">Hybrid Deployments are configurations that use both the Microsoft Lync Online cloud service and the on premises deployment.</span></span> <span data-ttu-id="5bd24-107">Bei dieser Art von Konfiguration muss der AutoErmittlungsdienst in der Lage sein, zu ermitteln, wo sich der Benutzer gerade befindet.</span><span class="sxs-lookup"><span data-stu-id="5bd24-107">In this type of configuration, the Autodiscover service must be able to locate where the user is actually located.</span></span> <span data-ttu-id="5bd24-108">Das heißt, die AutoErmittlung unterstützt Sie bei der Suche nach dem Benutzerkonto und dem Server, auf dem sich das Konto des Benutzers befindet, unabhängig davon, ob es sich um die lokale Bereitstellung oder die lync Online-Bereitstellung handelt.</span><span class="sxs-lookup"><span data-stu-id="5bd24-108">That is to say, Autodiscover aids in finding the user account and where the server that hosts the user’s account is, regardless if it is in the on premises deployment or in the Lync Online deployment.</span></span>

<span data-ttu-id="5bd24-109">Wenn beispielsweise das Konto eines Benutzers auf einem Server in lync online gehostet wird, erfolgt der Versuch, den Benutzer zu finden, in einem Vorgang, der als *Auffindbarkeit* bekannt ist, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5bd24-109">For example, if a user’s account is hosted on a server in Lync Online, the attempt to locate the user will happen as follows, in a process known as *discoverability*:</span></span>

  - <span data-ttu-id="5bd24-110">Der Benutzer initiiert einen Verbindungsversuch mit der lokalen Bereitstellung, **contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="5bd24-110">User initiates a connection attempt to the on premises deployment, **contoso.com**.</span></span>

  - <span data-ttu-id="5bd24-111">Der Versuch wird an lyncdiscover.contoso.com gesendet, dem DNS-Namen, der dem AutoErmittlungsdienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5bd24-111">The attempt is sent to lyncdiscover.contoso.com, the DNS name associated with the Autodiscover service.</span></span>

  - <span data-ttu-id="5bd24-112">Die AutoErmittlung bezieht sich auf den angenommenen Registrierungspool bei der contoso.com-Bereitstellung und erhält Informationen über den tatsächlichen Stammserver des Benutzers, der in lync online gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd24-112">Autodiscover refers to the assumed registrar pool at the contoso.com on premises deployment and is given information on the user’s actual home server hosted in Lync Online.</span></span> <span data-ttu-id="5bd24-113">Der AutoErmittlungsdienst sendet dem Benutzer dann einen Verweis an den **lync.com** Online-AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5bd24-113">Autodiscover then sends the user a referral to the **lync.com** online Autodiscover service.</span></span>

  - <span data-ttu-id="5bd24-114">Der Benutzer initiiert einen Verbindungsversuch mit dem lync.com Online-AutoErmittlungsdienst und kann das Konto des Benutzers und den Stammserver des Benutzers finden.</span><span class="sxs-lookup"><span data-stu-id="5bd24-114">The user initiates a connection attempt to the lync.com online Autodiscover service and is able to locate the user’s account and the user’s home server.</span></span>

<span data-ttu-id="5bd24-115">Damit Mobile Clients die Bereitstellung ermitteln können, auf der sich der Benutzerstamm Server befindet, müssen Sie den AutoErmittlungsdienst mit einem neuen URL (Uniform Resource Locator) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5bd24-115">To enable mobile clients to discover the deployment where the user home server is located, you must configure the Autodiscover service with a new uniform resource locator (URL).</span></span> <span data-ttu-id="5bd24-116">Gehen Sie wie folgt vor, um den AutoErmittlungsdienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5bd24-116">Do the following to configure the Autodiscover service.</span></span>

<div>

## <a name="configuring-autodiscover-for-hybrid-deployments"></a><span data-ttu-id="5bd24-117">Konfigurieren der AutoErmittlung für Hybrid Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="5bd24-117">Configuring Autodiscover for Hybrid Deployments</span></span>

1.  <span data-ttu-id="5bd24-118">Sie verwenden Get-CsHostingProvider, um den Wert des Attributs ProxyFQDN abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5bd24-118">You use Get-CsHostingProvider to retrieve the value of the attribute ProxyFQDN.</span></span>

2.  <span data-ttu-id="5bd24-119">Geben Sie in der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="5bd24-119">From the Lync Server Management Shell, type</span></span>
    
        Set-CsHostingProvider -Identity [identity] -AutodiscoverUrl https://webdir.online.lync.com/autodiscover/autodiscoverservice.svc/root
    
    <span data-ttu-id="5bd24-120">Wobei \[ Identity \] durch den Domänennamen des freigegebenen SIP-Adressraums ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd24-120">Where \[identity\] is replaced with the domain name of the shared SIP address space.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5bd24-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd24-121">See Also</span></span>


<span data-ttu-id="5bd24-122">[Get-CsHostingProvider](https://technet.microsoft.com/library/Gg413078(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5bd24-122">[Get-CsHostingProvider](https://technet.microsoft.com/library/Gg413078(v=OCS.15))</span></span>  
<span data-ttu-id="5bd24-123">[Satz-CsHostingProvider](https://technet.microsoft.com/library/Gg398532(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="5bd24-123">[Set-CsHostingProvider](https://technet.microsoft.com/library/Gg398532(v=OCS.15))</span></span>  
  

<span data-ttu-id="5bd24-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5bd24-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

