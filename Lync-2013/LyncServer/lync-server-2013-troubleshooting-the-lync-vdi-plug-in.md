---
title: 'Lync Server 2013: Problembehandlung beim lync VDI-Plug-in'
description: 'Lync Server 2013: Problembehandlung beim lync VDI-Plug-in.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Troubleshooting the Lync VDI plug-in
ms:assetid: 183c9449-b907-409c-b5ed-b02af3bd93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204713(v=OCS.15)
ms:contentKeyID: 48183525
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cd2c0e3c8a47225f00ce280706dea2287e4dc8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394315"
---
# <a name="troubleshooting-the-lync-vdi-plug-in-in-lync-server-2013"></a><span data-ttu-id="9f7d6-103">Problembehandlung beim lync VDI-Plug-in in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f7d6-103">Troubleshooting the Lync VDI plug-in in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f7d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f7d6-104">

<span> </span></span></span>

<span data-ttu-id="9f7d6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="9f7d6-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<div>

## <a name="troubleshooting-issues-with-installing-the-lync-vdi-plug-in-on-a-thin-client"></a><span data-ttu-id="9f7d6-106">Behandeln von Problemen bei der Installation des lync VDI-Plug-Ins auf einem Thin Client</span><span class="sxs-lookup"><span data-stu-id="9f7d6-106">Troubleshooting Issues with Installing the Lync VDI Plug-in on a Thin Client</span></span>

<span data-ttu-id="9f7d6-107">Wenn Probleme beim Installieren des VDI-Plug-Ins auf einem Thin Client auftreten, überprüfen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9f7d6-107">If there are issues with installing the VDI plug-in on a thin client, check the following:</span></span>

  - <span data-ttu-id="9f7d6-108">Stellen Sie sicher, dass in dem Ordner, den Sie in den Systemvariablen „TEMP“ und „TMP“ angegeben haben, ausreichend Speicherplatz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-108">Ensure that there is sufficient space in the folder that you specified in the TEMP and TMP system variables.</span></span>

  - <span data-ttu-id="9f7d6-p101">Stellen Sie sicher, dass der Schreibschutz deaktiviert ist. Entsprechende Anweisungen finden Sie in der Dokumentation des Geräteherstellers.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-p101">Ensure that write-protect is turned off. Refer to your device manufacturer’s documentation for instructions.</span></span>

</div>

<div>

## <a name="troubleshooting-issues-with-pairing"></a><span data-ttu-id="9f7d6-111">Problembehandlung für die Kopplung</span><span class="sxs-lookup"><span data-stu-id="9f7d6-111">Troubleshooting Issues with Pairing</span></span>

<span data-ttu-id="9f7d6-112">Wenn die VDI-Plug-in-Kopplung fehlschlägt, wird das Kopplungs Symbol in der unteren rechten Ecke als rotes "X" angezeigt:</span><span class="sxs-lookup"><span data-stu-id="9f7d6-112">When VDI plug-in pairing fails, the pairing icon in the lower right displays as a red “X” as shown:</span></span>

<span data-ttu-id="9f7d6-113">![Lync-VDI-Symbol mit erfolgreicher Kopplung](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync-VDI-Symbol mit erfolgreicher Kopplung")</span><span class="sxs-lookup"><span data-stu-id="9f7d6-113">![Lync VDI icon showing successful pairing](images/JJ204948.303d618c-4bc8-41c4-8553-2475de0d395e(OCS.15).png "Lync VDI icon showing successful pairing")</span></span>

<span data-ttu-id="9f7d6-114">Im folgenden sind mögliche Ursachen für Fehler und die erforderlichen Korrekturmaßnahmen zu finden.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-114">The following are possible reasons for failures and the corrective actions you can take.</span></span>

  - <span data-ttu-id="9f7d6-115">**Die Benutzer haben bei der Anmeldung falsche Anmeldeinformationen eingegeben.**</span><span class="sxs-lookup"><span data-stu-id="9f7d6-115">**The user entered incorrect credentials during sign-in.**</span></span>
    
    <span data-ttu-id="9f7d6-116">Der Benutzer sollte sich bei lync abmelden und sich erneut mit den korrekten Anmeldeinformationen anmelden.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-116">The user should sign out of Lync and sign in again with the correct credentials.</span></span> <span data-ttu-id="9f7d6-117">Das Kopplungsdialogfeld wird erneut angezeigt und gibt an, ob die Kopplung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-117">The pairing dialog box will reappear and show whether pairing is successful.</span></span>

  - <span data-ttu-id="9f7d6-118">**Eine andere Instanz des Remotedesktopclients wird bereits ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="9f7d6-118">**Another instance of the remote desktop client is running.**</span></span>
    
    <span data-ttu-id="9f7d6-119">Wenn Sie in Windows die Remote Desktop Verbindung verwenden, sollten die Benutzer die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="9f7d6-119">If they are using Remote Desktop Connection in Windows, users should do the following:</span></span>
    
    1.  <span data-ttu-id="9f7d6-120">Starten Sie den Task-Manager: Drücken Sie **ALT+STRG+ENTF**, und klicken Sie dann auf **Task-Manager starten**.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-120">Start Task Manager: Press **Alt+Ctrl+Delete**, and then click **Start Task Manager**.</span></span>
    
    2.  <span data-ttu-id="9f7d6-121">Klicken Sie auf die Registerkarte **Prozesse**, und suchen Sie in der Liste nach allen Prozessen mit dem Namen **mstsc.exe**.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-121">Click the **Processes** tab and look for all processes named **mstsc.exe** in the list.</span></span>
    
    3.  <span data-ttu-id="9f7d6-122">Markieren Sie alle **mstsc.exe**-Prozesse, und klicken Sie dann auf **Prozess beenden**. </span><span class="sxs-lookup"><span data-stu-id="9f7d6-122">Highlight each **mstsc.exe** process and then click **End Process**.</span></span>
    
    4.  <span data-ttu-id="9f7d6-123">Starten Sie eine neue Remotedesktopsitzung, und versuchen Sie erneut, eine Verbindung herzustellen. </span><span class="sxs-lookup"><span data-stu-id="9f7d6-123">Start a new remote desktop session and try connecting again.</span></span>

  - <span data-ttu-id="9f7d6-124">**Die erforderlichen Dateien wurden nicht ordnungsgemäß installiert.**</span><span class="sxs-lookup"><span data-stu-id="9f7d6-124">**The necessary files did not install correctly.**</span></span>
    
    <span data-ttu-id="9f7d6-125">Nachdem das Plug-in auf dem lokalen Computer installiert wurde, sollten die folgenden Dateien unter C: \\ Programmdateien \\ Microsoft Office \\ Ordner office15 (oder der entsprechende Laufwerkbuchstabe) vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="9f7d6-125">After the plug-in is installed on the local computer, the following files should be present under C:\\Program Files\\Microsoft Office\\Office15 (or the appropriate drive letter):</span></span>
    
      - <span data-ttu-id="9f7d6-126">LyncVdiPlugin.dll</span><span class="sxs-lookup"><span data-stu-id="9f7d6-126">LyncVdiPlugin.dll</span></span>
    
      - <span data-ttu-id="9f7d6-127">UcVdi.dll</span><span class="sxs-lookup"><span data-stu-id="9f7d6-127">UcVdi.dll</span></span>
    
    <span data-ttu-id="9f7d6-128">Wenn Probleme mit der VDI-Kopplung auftreten, stellen Sie sicher, dass diese Dateien auf dem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-128">If there are any issues with VDI pairing, check to make sure that these files are present on the local computer.</span></span>

  - <span data-ttu-id="9f7d6-129">**Der lync-Client wird auf dem lokalen Computer ausgeführt.**</span><span class="sxs-lookup"><span data-stu-id="9f7d6-129">**The Lync client is running on the local computer.**</span></span>
    
    <span data-ttu-id="9f7d6-130">Wenn Sie das lync-VDI-Plug-in verwenden möchten, muss ein lync-Client nicht auf dem lokalen Computer ausgeführt werden, da andernfalls die Kopplung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-130">To use the Lync VDI plugin, a Lync client must not be running on the local computer, otherwise pairing will fail.</span></span> <span data-ttu-id="9f7d6-131">Als bewährte Methode sollte der Benutzer keinen lync-Client auf dem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-131">As a best practice, the user should not install a Lync client on the local computer.</span></span>

<span data-ttu-id="9f7d6-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f7d6-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

