---
title: 'Lync Server 2013: Überprüfen des Zugriffs über den Reverseproxy'
description: 'Lync Server 2013: Überprüfen des Zugriffs über den Reverse-Proxy'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593aac5574f0dcf683351f12a6392f6116480ac5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443475"
---
# <a name="verify-access-through-your-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="6f1fa-103">Überprüfen des Zugriffs über den Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f1fa-103">Verify access through your reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f1fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f1fa-104">

<span> </span></span></span>

<span data-ttu-id="6f1fa-105">_**Letztes Änderungsdatum des Themas:** 2013-03-29_</span><span class="sxs-lookup"><span data-stu-id="6f1fa-105">_**Topic Last Modified:** 2013-03-29_</span></span>

<span data-ttu-id="6f1fa-106">Gehen Sie wie folgt vor, um zu überprüfen, ob Ihre Benutzer auf Informationen auf dem Reverse-Proxy zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-106">Use the following procedure to verify that your users can access information on the reverse proxy.</span></span> <span data-ttu-id="6f1fa-107">Möglicherweise müssen Sie die Firewall-Konfiguration und DNS-Konfiguration (Domain Name System) durchführen, bevor Access ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-107">You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.</span></span>

<div>

## <a name="to-verify-that-you-can-access-the-website-through-the-internet"></a><span data-ttu-id="6f1fa-108">So überprüfen Sie, ob Sie über das Internet auf die Website zugreifen können</span><span class="sxs-lookup"><span data-stu-id="6f1fa-108">To verify that you can access the website through the Internet</span></span>

  - <span data-ttu-id="6f1fa-109">Öffnen Sie einen Webbrowser, und geben Sie die URLs in der **Adress** Leiste ein, die Clients für den Zugriff auf die Adressbuchdateien und die Website für Konferenzen wie folgt verwenden:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-109">Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:</span></span>
    
      - <span data-ttu-id="6f1fa-110">Geben Sie für den Adressbuch Server eine URL ein, die der folgenden ähnelt: **https://externalwebfarmFQDN/abs** wobei externalwebfarmFQDN der externe FQDN der externen Webdienste ist, der Adressbuchdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-110">For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services.</span></span> <span data-ttu-id="6f1fa-111">Der Benutzer sollte eine HTTP-Abfrage erhalten, da die Verzeichnissicherheit im Ordner "Adressbuch Server" standardmäßig für die Windows-Authentifizierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-111">The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="6f1fa-112">Geben Sie für Konferenzen eine URL ein, die der folgenden ähnelt: **https://externalwebfarmFQDN/meet** wobei externalwebfarmFQDN der externe FQDN der Webfarm ist, die Besprechungsinhalte hostet.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-112">For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content.</span></span> <span data-ttu-id="6f1fa-113">Diese URL sollte die Seite zur Problembehandlung für Konferenzen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-113">This URL should display the troubleshooting page for conferencing.</span></span> <span data-ttu-id="6f1fa-114">Sie können aber auch sicherstellen, dass Ihre einfache URL für Konferenzfunktionen ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-114">Alternatively, confirm that your Simple URL for conferencing functions correctly.</span></span> <span data-ttu-id="6f1fa-115">Eine einfache URL für die Konferenzteilnahme ist möglicherweise https://meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6f1fa-115">An example Simple URL for the conference join might be https://meet.contoso.com</span></span>
    
      - <span data-ttu-id="6f1fa-116">Geben Sie für die Erweiterung der Verteilergruppe eine URL ein, die der folgenden **https://externalwebfarmFQDN/GroupExpansion/service.svc** ähnelt:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-116">For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**.</span></span> <span data-ttu-id="6f1fa-117">Der Benutzer sollte eine HTTP-Challenge erhalten, da die Verzeichnissicherheit des Verteilergruppen-Erweiterungs Diensts standardmäßig für die Windows-Authentifizierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-117">The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.</span></span>
    
      - <span data-ttu-id="6f1fa-118">Geben Sie für Einwahl die einfache URL ein, die der folgenden ähnelt, **https://externalwebfarmFQDN/dialin** wobei externalwebfarmFQDN der externe FQDN der Webfarm ist, die die Einwahlseite für Einwahlkonferenzen hostet.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-118">For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing.</span></span> <span data-ttu-id="6f1fa-119">Der Benutzer sollte an die Einwahlseite weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-119">The user should be directed to the dial-in page.</span></span> <span data-ttu-id="6f1fa-120">Sie können aber auch sicherstellen, dass Ihre einfache URL-Einwahlfunktion ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-120">Alternatively, confirm that your Simple URL dial-in functions correctly.</span></span> <span data-ttu-id="6f1fa-121">Ein Beispiel für eine einfache URL für die Einwahl ist möglicherweise https://dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="6f1fa-121">An example Simple URL for dial-in might be https://dialin.contoso.com</span></span>
    
      - <span data-ttu-id="6f1fa-122">Um zu bestätigen, dass die Auto Ermittlungs-URL funktioniert, geben Sie https://lyncdiscover .</span><span class="sxs-lookup"><span data-stu-id="6f1fa-122">To confirm that the autodiscover URL is working, type https://lyncdiscover.</span></span> <span data-ttu-id="6f1fa-123">externaldomainFQDN.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-123">externaldomainFQDN.</span></span> <span data-ttu-id="6f1fa-124">Der Browser sollte Sie dazu auffordern, eine Datei zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-124">The browser should prompt you to open a file.</span></span> <span data-ttu-id="6f1fa-125">Wählen Sie Editor aus, um ihn zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6f1fa-125">Select Notepad to open it.</span></span> <span data-ttu-id="6f1fa-126">Eine typische Antwort wäre ähnlich wie bei:</span><span class="sxs-lookup"><span data-stu-id="6f1fa-126">A typical response would be similar to:</span></span>
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

<span data-ttu-id="6f1fa-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f1fa-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

