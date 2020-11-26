---
title: 'Lync Server 2013: Anzeigen von Zugriffsnummern für Einwahlkonferenzen'
description: 'Lync Server 2013: Anzeigen von Zugriffsnummern für Einwahlkonferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View dial-in conferencing access numbers
ms:assetid: 41a7dfb4-0c89-4650-b61b-0e1bf875c62b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688037(v=OCS.15)
ms:contentKeyID: 49733628
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad682a4da92b31fbadfe3a75903f8cb6b8e8b949
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446983"
---
# <a name="view-dial-in-conferencing-access-numbers-in-lync-server-2013"></a><span data-ttu-id="b506d-103">Anzeigen von Einwahlkonferenz-Zugriffsnummern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b506d-103">View dial-in conferencing access numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b506d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b506d-104">

<span> </span></span></span>

<span data-ttu-id="b506d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="b506d-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="b506d-106">In der lync Server 2013-Systemsteuerung stellen Sie die Einwahl Zugriffsnummern für Benutzer bereit, damit diese extern an einer Besprechung teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="b506d-106">In Lync Server 2013 Control Panel, you provide dial-in access numbers to users so that they can join a meeting externally.</span></span>

<div>

## <a name="to-view-dial-in-access-numbers"></a><span data-ttu-id="b506d-107">So zeigen Sie Einwahl Zugriffsnummern an</span><span class="sxs-lookup"><span data-stu-id="b506d-107">To view dial-in access numbers</span></span>

1.  <span data-ttu-id="b506d-108">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b506d-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="b506d-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b506d-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="b506d-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b506d-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="b506d-111">Klicken Sie in der linken Navigationsleiste auf **Konferenz** und dann auf **Einwahlnummer**.</span><span class="sxs-lookup"><span data-stu-id="b506d-111">In the left navigation bar, click **Conferencing** and then click **Dial-in Access Number**.</span></span>

4.  <span data-ttu-id="b506d-112">Klicken Sie auf der Seite **Zugriffsnummer für Einwahlkonferenz** auf die Zugriffsnummer, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="b506d-112">On the **Dial-in Access Number** page, click the access number that you would like to view.</span></span>

5.  <span data-ttu-id="b506d-113">Wählen Sie in **Bearbeiten** die Option **Details anzeigen aus.**</span><span class="sxs-lookup"><span data-stu-id="b506d-113">In **Edit**, select the **Show Details…**</span></span> <span data-ttu-id="b506d-114">Aktivieren Sie das Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="b506d-114">check box.</span></span>

</div>

<div>

## <a name="viewing-dial-in-conferencing-access-numbers-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="b506d-115">Anzeigen von Zugriffsnummern für Einwahlkonferenzen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b506d-115">Viewing Dial-in Conferencing Access Numbers by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="b506d-116">Zugriffsnummern für Einwahlkonferenzen können mithilfe von Windows PowerShell und dem Cmdlet Get-CsDialInConferencingAccessNumber angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b506d-116">Dial-in conferencing access numbers can be viewed by using Windows PowerShell and the Get-CsDialInConferencingAccessNumber cmdlet.</span></span> <span data-ttu-id="b506d-117">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b506d-117">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="b506d-118">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="b506d-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-dial-in-conferencing-access-numbers"></a><span data-ttu-id="b506d-119">So zeigen Sie Einwahlkonferenz-Zugriffsnummern an</span><span class="sxs-lookup"><span data-stu-id="b506d-119">To view dial-in conferencing access numbers</span></span>

  - <span data-ttu-id="b506d-120">Wenn Sie Informationen zu allen Access-Nummern für Einwahlkonferenzen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="b506d-120">To view information about all your dial-in conferencing access numbers, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsDialInConferencingAccessNumber
    
    <span data-ttu-id="b506d-121">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="b506d-121">That will return information similar to this:</span></span>
    
        Identity           : CN={20ca8dc8-5ff8-41f4-b5bb-22ba9972ae2e},
                             CN=Application Contacts,CN=RTCService=Services,
                             CN=Configuration,DC=litwareinc,DC=com
        PrimaryUri         : sip:testnumber@litwareinc.com
        DisplayName        : Test
        DisplayNumber      : 1-425-555-1019
        LineUri            : tel:+14255551019
        PrimaryLanguage    : en-US
        SecondaryLanguages : {}
        Pool               : atl-cs-001.litwareinc.com
        HostingProvider    :
        Regions            : {US}

</div>

<span data-ttu-id="b506d-122">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingAccessNumber) .</span><span class="sxs-lookup"><span data-stu-id="b506d-122">For more information, see the help topic for the [Get-CsDialInConferencingAccessNumber](https://docs.microsoft.com/powershell/module/skype/Get-CsDialInConferencingAccessNumber) cmdlet.</span></span>

<span data-ttu-id="b506d-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b506d-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

