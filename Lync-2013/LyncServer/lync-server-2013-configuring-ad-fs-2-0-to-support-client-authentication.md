---
title: 'Lync Server 2013: Konfigurieren von AD FS 2,0 zur Unterstützung der Clientauthentifizierung'
description: 'Lync Server 2013: Konfigurieren von AD FS 2,0 zur Unterstützung der Clientauthentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring AD FS 2.0 to support client authentication
ms:assetid: 4d93d400-ccaa-4da8-a71b-d05d7ba79d93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn308565(v=OCS.15)
ms:contentKeyID: 54973687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 156eb6d7e8af85dec04601ab8f88c55181db20d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433395"
---
# <a name="configuring-ad-fs-20-to-support-client-authentication-in-lync-server-2013"></a><span data-ttu-id="f9b73-103">Konfigurieren von AD FS 2,0 zur Unterstützung der Clientauthentifizierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9b73-103">Configuring AD FS 2.0 to support client authentication in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9b73-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9b73-104">

<span> </span></span></span>

<span data-ttu-id="f9b73-105">_**Letztes Änderungsdatum des Themas:** 2013-07-03_</span><span class="sxs-lookup"><span data-stu-id="f9b73-105">_**Topic Last Modified:** 2013-07-03_</span></span>

<span data-ttu-id="f9b73-106">Es gibt zwei mögliche Authentifizierungstypen, die so konfiguriert werden können, dass AD FS 2.0 Authentifizierung über Smartcards unterstützen kann:</span><span class="sxs-lookup"><span data-stu-id="f9b73-106">There are two possible authentication types that can be configured to allow AD FS 2.0 to support authentication using smart cards:</span></span>

  - <span data-ttu-id="f9b73-107">Formularbasierte Authentifizierung (FBA)</span><span class="sxs-lookup"><span data-stu-id="f9b73-107">Forms-based authentication (FBA)</span></span>

  - <span data-ttu-id="f9b73-108">Transport Layer Security-Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="f9b73-108">Transport Layer Security Client Authentication</span></span>

<span data-ttu-id="f9b73-109">Wenn Sie formularbasierte Authentifizierung verwenden, können Sie eine Webseite entwickeln, die es Benutzern ermöglicht, sich entweder mit der Kombination aus Benutzername und Kennwort oder mit Smartcard und PIN zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="f9b73-109">Using forms-based authentication, you can develop a web page that allows users to authenticate either by using their username/password or by using their smart card and PIN.</span></span> <span data-ttu-id="f9b73-110">Im vorliegenden Thema wird beschrieben, wie Transport Layer Security-Clientauthentifizierung mit AD FS 2.0 implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="f9b73-110">This topic focuses on how to implement Transport Layer Security Client Authentication with AD FS 2.0.</span></span> <span data-ttu-id="f9b73-111">Weitere Informationen zu den AD FS 2,0-Authentifizierungstypen finden Sie unter AD FS 2,0: Ändern des lokalen Authentifizierungstyps unter [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384) .</span><span class="sxs-lookup"><span data-stu-id="f9b73-111">For more information about AD FS 2.0 authentication types, see AD FS 2.0: How to Change the Local Authentication Type at [https://go.microsoft.com/fwlink/p/?LinkId=313384](https://go.microsoft.com/fwlink/p/?linkid=313384).</span></span>

<div>


<span data-ttu-id="f9b73-112">**So konfigurieren Sie AD FS 2.0, sodass Clientauthentifizierung unterstützt wird**</span><span class="sxs-lookup"><span data-stu-id="f9b73-112">**To Configure AD FS 2.0 to Support Client Authentication**</span></span>

1.  <span data-ttu-id="f9b73-113">Melden Sie sich beim AD FS 2.0-Computer über ein Domänenadministratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="f9b73-113">Log in to the AD FS 2.0 computer using a Domain Admin account.</span></span>

2.  <span data-ttu-id="f9b73-114">Starten Sie Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="f9b73-114">Launch Windows Explorer.</span></span>

3.  <span data-ttu-id="f9b73-115">Navigieren Sie zu C: \\ Inetpub \\ ADFS \\ ls</span><span class="sxs-lookup"><span data-stu-id="f9b73-115">Browse to C:\\inetpub\\adfs\\ls</span></span>

4.  <span data-ttu-id="f9b73-116">Erstellen Sie eine Sicherungskopie von der vorhandenen Datei „web.config“.</span><span class="sxs-lookup"><span data-stu-id="f9b73-116">Make a backup copy of the existing web.config file.</span></span>

5.  <span data-ttu-id="f9b73-117">Öffnen Sie die vorhandene Datei „web.config“ im Editor.</span><span class="sxs-lookup"><span data-stu-id="f9b73-117">Open the existing web.config file using Notepad.</span></span>

6.  <span data-ttu-id="f9b73-118">Wählen Sie in der Menüleiste das Menü **Bearbeiten** und anschließend **Suchen** aus.</span><span class="sxs-lookup"><span data-stu-id="f9b73-118">From the Menu bar, select **Edit** and then select **Find**.</span></span>

7.  <span data-ttu-id="f9b73-119">Suchen nach **\<localAuthenticationTypes\>** .</span><span class="sxs-lookup"><span data-stu-id="f9b73-119">Search for **\<localAuthenticationTypes\>**.</span></span>
    
    <span data-ttu-id="f9b73-120">Es werden vier Authentifizierungstypen aufgelistet (je ein Typ pro Zeile).</span><span class="sxs-lookup"><span data-stu-id="f9b73-120">Note that there are four authentication types listed, one per line.</span></span>

8.  <span data-ttu-id="f9b73-121">Verschieben Sie die Zeile, die den Authentifizierungstyp „TLSClient“ enthält, an den Anfang der Liste im Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="f9b73-121">Move the line containing the TLSClient authentication type to the top of the list in the section.</span></span>

9.  <span data-ttu-id="f9b73-122">Speichern Sie die Datei „web.config“ und beenden Sie den Editor.</span><span class="sxs-lookup"><span data-stu-id="f9b73-122">Save and Close the web.config file.</span></span>

10. <span data-ttu-id="f9b73-123">Starten Sie eine Eingabeaufforderung mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="f9b73-123">Launch a Command Prompt with elevated privileges.</span></span>

11. <span data-ttu-id="f9b73-124">Starten Sie IIS neu, indem Sie folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="f9b73-124">Restart IIS by running the following command:</span></span>
    
        IISReset /Restart /NoForce

<span data-ttu-id="f9b73-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9b73-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

