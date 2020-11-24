---
title: Konfigurieren der Seite für den Besprechungsbeitritt
description: Konfigurieren der Besprechungsteilnahme Seite
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure the meeting join page
ms:assetid: 036c9d03-ad95-4d63-a3d8-6cae1a8ad530
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204635(v=OCS.15)
ms:contentKeyID: 48183260
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af49a57a6844c59bf6f6631d996d8efe12152c52
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394435"
---
# <a name="configure-the-meeting-join-page"></a><span data-ttu-id="4bbac-103">Konfigurieren der Seite für den Besprechungsbeitritt</span><span class="sxs-lookup"><span data-stu-id="4bbac-103">Configure the meeting join page</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4bbac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4bbac-104">

<span> </span></span></span>

<span data-ttu-id="4bbac-105">_**Letztes Änderungsdatum des Themas:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="4bbac-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="4bbac-106">Wenn ein Benutzer in einer Besprechungsanfrage auf einen Besprechungslink klickt, erkennt die Seite "Besprechungsteilnahme", ob ein lync 2013-Client bereits auf dem Computer des Benutzers installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4bbac-106">When a user clicks a meeting link in a meeting request, the meeting join page detects whether a Lync 2013 client is already installed on the user’s computer.</span></span> <span data-ttu-id="4bbac-107">Wenn ein Client bereits installiert ist, wird dieser Client geöffnet und der Besprechung beitreten.</span><span class="sxs-lookup"><span data-stu-id="4bbac-107">If a client is already installed, that client opens and joins the meeting.</span></span> <span data-ttu-id="4bbac-108">Wenn ein Client nicht installiert ist, wird standardmäßig die 2013-Version von lync Web App geöffnet.</span><span class="sxs-lookup"><span data-stu-id="4bbac-108">If a client is not installed, by default the 2013 version of Lync Web App opens.</span></span>

<span data-ttu-id="4bbac-109">Sie können das Verhalten der Besprechungsteilnahme Seite ändern, wenn Sie Benutzern die Teilnahme an Besprechungen mit Office Communicator 2007 R2 oder lync 2010 Attendant gestatten möchten.</span><span class="sxs-lookup"><span data-stu-id="4bbac-109">You can modify the behavior of the meeting join page if you want to allow users to join meetings with Office Communicator 2007 R2 or Lync 2010 Attendant.</span></span> <span data-ttu-id="4bbac-110">Diese Konfigurationsoptionen wurden aus der Systemsteuerung von lync Server 2013 entfernt, aber Sie werden mithilfe des CsWebServiceConfiguration-Cmdlets konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4bbac-110">These configuration options have been removed from the Lync Server 2013 Control Panel, but you configure them by using the CsWebServiceConfiguration cmdlet.</span></span>

### <a name="meeting-join-page-cswebserviceconfiguration-parameters"></a><span data-ttu-id="4bbac-111">CsWebServiceConfiguration-Parameter für Besprechungsteilnehmer Seite</span><span class="sxs-lookup"><span data-stu-id="4bbac-111">Meeting Join Page CsWebServiceConfiguration Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4bbac-112">CsWebServiceConfiguration-Parameter</span><span class="sxs-lookup"><span data-stu-id="4bbac-112">CsWebServiceConfiguration Parameter</span></span></th>
<th><span data-ttu-id="4bbac-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bbac-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bbac-114">ShowJoinUsingLegacyClientLink</span><span class="sxs-lookup"><span data-stu-id="4bbac-114">ShowJoinUsingLegacyClientLink</span></span></p></td>
<td><p><span data-ttu-id="4bbac-115">Wenn die Einstellung auf "true" festgelegt ist, wird Benutzern, die mit einer anderen Clientanwendung als lync an einer Besprechung teilnehmen, die Möglichkeit gegeben, mit Office Communicator 2007 R2 an der Besprechung teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="4bbac-115">If set to True, users joining a meeting by using a client application other than Lync will be given the opportunity to join the meeting by using Office Communicator 2007 R2.</span></span> <span data-ttu-id="4bbac-116">Der Standardwert lautet "False".</span><span class="sxs-lookup"><span data-stu-id="4bbac-116">The default value is False.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bbac-117">ShowAlternateJoinOptionsExpanded</span><span class="sxs-lookup"><span data-stu-id="4bbac-117">ShowAlternateJoinOptionsExpanded</span></span></p></td>
<td><p><span data-ttu-id="4bbac-118">Wenn Sie auf true festgelegt ist, werden alternative Optionen für die Teilnahme an einer Onlinekonferenz (wie Office Communicator 2007 R2) automatisch erweitert und Benutzern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bbac-118">When set to True then alternate options for joining an online conference (such as Office Communicator 2007 R2) will automatically be expanded and shown to users.</span></span> <span data-ttu-id="4bbac-119">Wenn auf "false" (der Standardwert) festgelegt ist, sind diese Optionen verfügbar, der Benutzer muss jedoch die Liste der Optionen für sich selbst anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4bbac-119">When set to False (the default value) these options will be available, but the user will have to display the list of options for themselves.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-configure-the-meeting-join-page-by-using-lync-server-2013-management-shell"></a><span data-ttu-id="4bbac-120">So konfigurieren Sie die Seite "Besprechungsteilnahme" mithilfe der lync Server 2013-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="4bbac-120">To configure the meeting join page by using Lync Server 2013 Management Shell</span></span>

1.  <span data-ttu-id="4bbac-121">Starten Sie die lync Server 2013-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4bbac-121">Start the Lync Server 2013 Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4bbac-122">Führen Sie das folgende Cmdlet aus:</span><span class="sxs-lookup"><span data-stu-id="4bbac-122">Run the following cmdlet:</span></span>
    
        Get-CsWebServiceConfiguration
    
    <span data-ttu-id="4bbac-123">Dieses Cmdlet gibt die Konfigurationseinstellungen des Webdiensts zurück.</span><span class="sxs-lookup"><span data-stu-id="4bbac-123">This cmdlet returns the web service configuration settings.</span></span>

3.  <span data-ttu-id="4bbac-124">Führen Sie den folgenden Befehl aus, wobei die Parameter je nach ihrer Einstellung auf "true" oder "false" festgelegt sind (Einzelheiten zu den Parametern für dieses Cmdlet finden Sie in der Dokumentation zur lync Server 2013-Verwaltungsshell):</span><span class="sxs-lookup"><span data-stu-id="4bbac-124">Run the following command, with the parameters set to True or False, depending on your preference (for details about the parameters for this cmdlet, see the Lync Server 2013 Management Shell documentation):</span></span>
    
        Set-CsWebServiceConfiguration -Identity global -ShowJoinUsingLegacyClientLink $True

<span data-ttu-id="4bbac-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4bbac-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

