---
title: 'Lync Server 2013: Zuweisen eines Kerberos-Authentifizierungskontos zu einem Standort'
description: 'Lync Server 2013: Zuweisen eines Kerberos-Authentifizierungs Kontos zu einer Website'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assign a Kerberos authentication account to a site
ms:assetid: 3d9c587c-c8b8-4f81-8ed9-1458a31fc292
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425901(v=OCS.15)
ms:contentKeyID: 48183929
ms.date: 04/18/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: edcd80ef3ae15ae91dfab73ee8789054d897fe5c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439842"
---
# <a name="assign-a-kerberos-authentication-account-to-a-site-in-lync-server-2013"></a><span data-ttu-id="01bb9-103">Zuweisen eines Kerberos-Authentifizierungskontos zu einem Standort in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01bb9-103">Assign a Kerberos authentication account to a site in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01bb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01bb9-104">

<span> </span></span></span>

<span data-ttu-id="01bb9-105">_**Letztes Änderungsdatum des Themas:** 2017-04-18_</span><span class="sxs-lookup"><span data-stu-id="01bb9-105">_**Topic Last Modified:** 2017-04-18_</span></span>

<span data-ttu-id="01bb9-106">Um dieses Verfahren erfolgreich abzuschließen, sollten Sie als Benutzer angemeldet sein, der Mitglied der RTCUniversalServerAdmins-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="01bb9-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="01bb9-107">Nachdem Sie das Kerberos-Konto erstellt haben, müssen Sie es einer Website zuweisen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-107">After creating the Kerberos account, you must assign it to a site.</span></span> <span data-ttu-id="01bb9-108">Hierbei handelt es sich um eine lync Server 2013-Website, nicht um einen Active Directory-Standort.</span><span class="sxs-lookup"><span data-stu-id="01bb9-108">This is a Lync Server 2013 site, not an Active Directory site.</span></span> <span data-ttu-id="01bb9-109">Sie können pro Bereitstellung mehrere Kerberos-Authentifizierungs Konten erstellen, aber Sie können einer Website nur ein Konto zuweisen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-109">You can create multiple Kerberos authentication accounts per deployment, but you can assign only one account to a site.</span></span> <span data-ttu-id="01bb9-110">Gehen Sie wie folgt vor, um einer Website ein zuvor erstelltes Kerberos-Authentifizierungs Konto zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-110">Use the following procedure to assign a previously created Kerberos authentication account to a site.</span></span> <span data-ttu-id="01bb9-111">Details zum Erstellen des Kerberos-Kontos finden Sie unter [Erstellen eines Kerberos-Authentifizierungs Kontos in lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span><span class="sxs-lookup"><span data-stu-id="01bb9-111">For details about creating the Kerberos account, see [Create a Kerberos authentication account in Lync Server 2013](lync-server-2013-create-a-kerberos-authentication-account.md).</span></span>

<div>

## <a name="to-assign-a-kerberos-authentication-account-to-a-site"></a><span data-ttu-id="01bb9-112">So weisen Sie einer Website ein Kerberos-Authentifizierungs Konto zu</span><span class="sxs-lookup"><span data-stu-id="01bb9-112">To assign a Kerberos authentication account to a site</span></span>

1.  <span data-ttu-id="01bb9-113">Melden Sie sich als Mitglied der RTCUniversalServerAdmins-Gruppe an einem Computer in der Domäne mit lync Server 2013 oder auf einem Computer an, auf dem die Verwaltungstools installiert sind.</span><span class="sxs-lookup"><span data-stu-id="01bb9-113">As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.</span></span>

2.  <span data-ttu-id="01bb9-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="01bb9-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="01bb9-115">Führen Sie in der Befehlszeile die beiden folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="01bb9-115">From the command line, run the following two commands:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "Domain\UserAccount"
                  -Identity "site:SiteName"
       ```          
    
       ```powershell
        Enable-CsTopology
       ```
    
    <span data-ttu-id="01bb9-116">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="01bb9-116">For example:</span></span>
    
       ```powershell
        New-CsKerberosAccountAssignment -UserAccount "contoso\kerbauth"
                  -Identity "site:redmond"
       ```
    
       ```powershell
        Enable-CsTopology
       ```
    
    <div class="">
    

    > [!NOTE]  
    > <span data-ttu-id="01bb9-117">Sie müssen den Benutzerkonto-Parameter unter Verwendung des Formats Domäne \ Benutzer angeben.</span><span class="sxs-lookup"><span data-stu-id="01bb9-117">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="01bb9-118">Das User@Domain. Extension-Format wird nicht unterstützt, um auf die für die Kerberos-Authentifizierung erstellten Computerobjekte zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-118">The User@Domain.extension format is not supported for referring to the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>

4.  <span data-ttu-id="01bb9-119">**Optional**: Sie haben möglicherweise einen überschreiben-FQDN (Fully Qualified Domain Name, vollständig qualifizierter Domänenname) für Ihre Webdienste konfiguriert, wie pro [Änderung der URL für Webdienste in lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span><span class="sxs-lookup"><span data-stu-id="01bb9-119">**OPTIONAL**: You may have configured an override FQDN (fully qualified domain name) for your WebServices, as per [Change the Web Services URL in Lync Server 2013](lync-server-2013-change-the-web-services-url.md).</span></span> <span data-ttu-id="01bb9-120">Wenn dies der Fall ist, müssen Sie auch einen SPN für diesen FQDN hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-120">If that's the case, you'll need to add a SPN for this FQDN as well.</span></span> <span data-ttu-id="01bb9-121">Wenn der FQDN beispielsweise Webservices. contoso. local lautete, würden Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="01bb9-121">For example, if the FQDN was webservices.contoso.local, you would run:</span></span>
    
    ```console
    setspn -S http/webservices.contoso.local kerbauth
    ```
5.     
    <div class="">
    

    > [!IMPORTANT]  
    > <span data-ttu-id="01bb9-122">Nachdem Sie die Kerberos-Authentifizierung geändert haben, beispielsweise ein Konto hinzugefügt oder ein Konto entfernt haben, müssen Sie <STRONG>enable-CsTopology</STRONG> über die Eingabeaufforderung der lync Server-Verwaltungsshell ausführen.</span><span class="sxs-lookup"><span data-stu-id="01bb9-122">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="01bb9-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01bb9-123"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

