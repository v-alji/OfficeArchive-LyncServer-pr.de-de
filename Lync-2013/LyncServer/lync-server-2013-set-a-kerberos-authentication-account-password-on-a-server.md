---
title: 'Lync Server 2013: Festlegen eines Kennworts für das Kerberos-Authentifizierungskonto auf einem Server'
description: 'Lync Server 2013: Festlegen eines Kennworts für ein Kerberos-Authentifizierungs Konto auf einem Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set a Kerberos authentication account password on a server
ms:assetid: 902d3292-678d-4512-9248-586053cb638b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398734(v=OCS.15)
ms:contentKeyID: 48184787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 723392e670ca0b4bc9796cd62dab3b1a61f99dd1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444784"
---
# <a name="set-a-kerberos-authentication-account-password-on-a-server-in-lync-server-2013"></a><span data-ttu-id="e9906-103">Festlegen eines Kennworts für das Kerberos-Authentifizierungskonto auf einem Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9906-103">Set a Kerberos authentication account password on a server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9906-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9906-104">

<span> </span></span></span>

<span data-ttu-id="e9906-105">_**Letztes Änderungsdatum des Themas:** 2012-01-16_</span><span class="sxs-lookup"><span data-stu-id="e9906-105">_**Topic Last Modified:** 2012-01-16_</span></span>

<span data-ttu-id="e9906-106">Um dieses Verfahren erfolgreich abzuschließen, sollten Sie als Benutzer angemeldet sein, der Mitglied der RTCUniversalServerAdmins-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="e9906-106">To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.</span></span>

<span data-ttu-id="e9906-107">Sie müssen für jede Website mit Front-End-Servern, Standard Edition-Servern und Directors ein Kennwort für das Kerberos-Konto einrichten.</span><span class="sxs-lookup"><span data-stu-id="e9906-107">You must set up a password on the Kerberos account for each site that has Front End Servers, Standard Edition servers, and Directors.</span></span> <span data-ttu-id="e9906-108">Sie können das Kennwort einrichten, indem Sie das Windows PowerShell-Cmdlet " **CsKerberosAccountPassword** " auf einem Server auf der Website ausführen (beispielsweise ein Front-End-Server).</span><span class="sxs-lookup"><span data-stu-id="e9906-108">You can set up the password by running the **Set-CsKerberosAccountPassword** Windows PowerShell cmdlet on one server in the site (for example, one Front End Server).</span></span> <span data-ttu-id="e9906-109">Für jede Website müssen Sie das Cmdlet " **Satz-CsKerberosAccountPassword** " ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9906-109">For each site, you must run the **Set-CsKerberosAccountPassword** cmdlet.</span></span> <span data-ttu-id="e9906-110">Das Cmdlet konfiguriert Internet Informationsdienste (IIS) für den Webdienst Dienst und legt dann das Kennwort für das Computerkonto in den Active Directory-Domänendiensten fest.</span><span class="sxs-lookup"><span data-stu-id="e9906-110">The cmdlet configures Internet Information Services (IIS) for the Web Services service, and then sets the password on the computer account in Active Directory Domain Services.</span></span> <span data-ttu-id="e9906-111">Eine alternative Methode, basierend auf dem mit dem Cmdlet verwendeten Parameter, konfiguriert IIS auf einem Server, während ein anderer Server verwendet wird, der als Quelle des Kerberos-Kontokennworts konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="e9906-111">An alternate method, based on which parameter is used with the cmdlet, configures IIS on one server while using another server that has been configured as the source of the Kerberos account password.</span></span>

<span data-ttu-id="e9906-112">Wenn Sie das Cmdlet **Set-CsKerberosAccountPassword** verwenden, um ein Kennwort festzulegen, wird das Kennwort von Kerberos auf eine zufällig generierte Zeichenfolge festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9906-112">When you use the **Set-CsKerberosAccountPassword** cmdlet to set a password, Kerberos sets the password to a randomly generated string.</span></span> <span data-ttu-id="e9906-113">Dieses Cmdlet kontaktiert alle IIS-Instanzen in allen lync Server 2013 Central-Websites, denen dieses Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e9906-113">This cmdlet contacts all IIS instances in all Lync Server 2013 central sites to which this account is assigned.</span></span>

<div>

## <a name="to-set-a-password-for-a-kerberos-authentication-account"></a><span data-ttu-id="e9906-114">So legen Sie ein Kennwort für ein Kerberos-Authentifizierungs Konto ab</span><span class="sxs-lookup"><span data-stu-id="e9906-114">To set a password for a Kerberos authentication account</span></span>

1.  <span data-ttu-id="e9906-115">Melden Sie sich bei einem beliebigen Domänencomputer an, auf dem die lync Server-Verwaltungsshell als Mitglied der RTCUniversalServerAdmins-Gruppe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e9906-115">Log on to any domain computer with Lync Server Management Shell installed as a member of the RTCUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="e9906-116">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="e9906-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="e9906-117">Führen Sie in der Befehlszeile die beiden folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="e9906-117">From the command line, run the following two commands:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "Domain\UserAccount"
    
    <span data-ttu-id="e9906-118">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e9906-118">For example:</span></span>
    
        Set-CsKerberosAccountPassword -UserAccount "contoso\KerbAuth"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="e9906-119">Sie müssen den Benutzerkonto-Parameter unter Verwendung des Formats Domäne \ Benutzer angeben.</span><span class="sxs-lookup"><span data-stu-id="e9906-119">You must specify the UserAccount parameter by using the Domain\User format.</span></span> <span data-ttu-id="e9906-120">Das Format User@Domain. Extension wird für den Verweis auf die für die Kerberos-Authentifizierung erstellten Computerobjekte nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9906-120">The User@Domain.extension format is not supported for referencing the computer objects created for Kerberos authentication purposes.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="e9906-121">Nachdem Sie die Kerberos-Authentifizierung geändert haben, beispielsweise ein Konto hinzugefügt oder ein Konto entfernt haben, müssen Sie <STRONG>enable-CsTopology</STRONG> über die Eingabeaufforderung der lync Server-Verwaltungsshell ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9906-121">After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.</span></span>

    
    <span data-ttu-id="e9906-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9906-122"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

