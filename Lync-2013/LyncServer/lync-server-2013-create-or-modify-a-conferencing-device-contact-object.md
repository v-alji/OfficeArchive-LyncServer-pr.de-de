---
title: 'Lync Server 2013: Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte'
description: 'Lync Server 2013: Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 853ee1c7dfda2fda99431b8cc1a5210a51f39a4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394378"
---
# <a name="create-or-modify-a-conferencing-device-contact-object-in-lync-server-2013"></a><span data-ttu-id="c412f-103">Erstellen oder Ändern eines Kontaktobjekts für Konferenzgeräte in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c412f-103">Create or modify a conferencing device Contact object in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c412f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c412f-104">

<span> </span></span></span>

<span data-ttu-id="c412f-105">_**Letztes Änderungsdatum des Themas:** 2013-10-02_</span><span class="sxs-lookup"><span data-stu-id="c412f-105">_**Topic Last Modified:** 2013-10-02_</span></span>

<span data-ttu-id="c412f-106">Zum Erstellen eines Konferenzraum Objekts erstellen Sie zunächst ein Active Directory-Benutzerkonto, um das Gerät darzustellen.</span><span class="sxs-lookup"><span data-stu-id="c412f-106">To create a conferencing room object, first create an Active Directory user account to represent the device.</span></span> <span data-ttu-id="c412f-107">Verwenden Sie dann das Cmdlet **enable-CsMeetingRoom** , damit dieses Konto als Konferenzgerät funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c412f-107">Then, use the **Enable-CsMeetingRoom** cmdlet to enable that account to function as a conferencing device.</span></span> <span data-ttu-id="c412f-108">Wenn Sie die Eigenschaften eines vorhandenen Konferenz Geräts ändern müssen, verwenden Sie das Cmdlet " **Satz-CsMeetingRoom** ".</span><span class="sxs-lookup"><span data-stu-id="c412f-108">If you need to change the properties of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span>

<span data-ttu-id="c412f-109">Diese Cmdlets können entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c412f-109">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c412f-110">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="c412f-110">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="creating-a-conferencing-device"></a><span data-ttu-id="c412f-111">Erstellen eines Konferenz Geräts</span><span class="sxs-lookup"><span data-stu-id="c412f-111">Creating a Conferencing Device</span></span>

  - <span data-ttu-id="c412f-112">Nachdem Sie das Active Directory-Benutzerkonto erstellt haben, das das neue Konferenzgerät darstellt, aktivieren Sie es mithilfe des Cmdlets **enable-CsMeetingRoom** .</span><span class="sxs-lookup"><span data-stu-id="c412f-112">After you create the Active Directory user account that represents the new conferencing device, enable it by using the **Enable-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="c412f-113">Stellen Sie sicher, dass Sie a) die Konferenzgeräte Identität, b) den Registrar-Pool, in dem das Raumkonto verwaltet wird, und c) die SIP-Adresse einbeziehen, die diesem Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c412f-113">Be sure to include a) the conferencing device identity, b) the registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account.</span></span> <span data-ttu-id="c412f-114">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c412f-114">For example:</span></span>
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

</div>

<div>

## <a name="modifying-a-conferencing-device"></a><span data-ttu-id="c412f-115">Ändern eines Konferenz Geräts</span><span class="sxs-lookup"><span data-stu-id="c412f-115">Modifying a Conferencing Device</span></span>

  - <span data-ttu-id="c412f-116">Verwenden Sie das Cmdlet " **CsMeetingRoom** ", um die Eigenschaftswerte eines vorhandenen Konferenz Geräts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c412f-116">To modify the property values of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.</span></span> <span data-ttu-id="c412f-117">Mit dem folgenden Befehl wird beispielsweise die Telefonnummer (LineUri) aktualisiert, die einem Konferenzgerät zugeordnet ist:</span><span class="sxs-lookup"><span data-stu-id="c412f-117">For example, the following command updates the phone number (LineUri) associated with a conferencing device:</span></span>
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

</div>

<span data-ttu-id="c412f-118">Ausführliche Informationen finden Sie in den Hilfethemen zum Cmdlet [enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) und dem Cmdlet " [Satz-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) ".</span><span class="sxs-lookup"><span data-stu-id="c412f-118">For details, see the Help topics for the [Enable-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Enable-CsMeetingRoom) cmdlet and the [Set-CsMeetingRoom](https://docs.microsoft.com/powershell/module/skype/Set-CsMeetingRoom) cmdlet.</span></span>

<span data-ttu-id="c412f-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c412f-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

