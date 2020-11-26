---
title: 'Lync Server 2013: Konfigurieren des persönlichen Kontaktspeichers auf Clientcomputern'
description: 'Lync Server 2013: Konfigurieren des persönlichen Kontaktspeichers auf Clientcomputern'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring the personal contacts store on client computers
ms:assetid: ec69a6cb-07f2-4057-9544-55035f83eeae
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721922(v=OCS.15)
ms:contentKeyID: 49733857
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1040b3eb9aa38e3e0c537d690b9292ab8f1ead2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432520"
---
# <a name="configuring-the-personal-contacts-store-on-client-computers-for-lync-server-2013"></a><span data-ttu-id="b8ea8-103">Konfigurieren des Speichers für persönliche Kontakte auf Clientcomputern für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8ea8-103">Configuring the personal contacts store on client computers for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8ea8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8ea8-104">

<span> </span></span></span>

<span data-ttu-id="b8ea8-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="b8ea8-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="b8ea8-106">Wenn Sie Microsoft lync Server 2013 und Microsoft Exchange Server 2013 integrieren, wird empfohlen, den persönlichen Kontaktspeicher auf allen Clientcomputern zu konfigurieren, auf denen Microsoft lync 2010 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-106">If you are integrating Microsoft Lync Server 2013 and Microsoft Exchange Server 2013 then it is recommended that you configure the personal contact store on any client computers running Microsoft Lync 2010.</span></span> <span data-ttu-id="b8ea8-107">Insbesondere sollten Sie lync so konfigurieren, dass Exchange als persönlicher Kontaktspeicher verwendet wird, und gleichzeitig sicherstellen, dass Benutzer diese Entscheidung nicht außer Kraft setzen können.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-107">In particular, you should configure Lync to use Exchange as the personal contact store, and, at the same time, ensure that users are not able to override that decision.</span></span> <span data-ttu-id="b8ea8-108">Dies ist nur dann möglich, wenn Sie auf jedem Clientcomputer einen Registrierungswert erstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-108">This can be done by creating and configuring a Registry value on each client computer.</span></span>

<span data-ttu-id="b8ea8-109">Beachten Sie, dass dies auf Computern, auf denen lync 2013 ausgeführt wird, nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-109">Note that this is not required on computers running Lync 2013.</span></span>

<span data-ttu-id="b8ea8-110">Zum Konfigurieren dieses Werts auf einem einzelnen Computer führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b8ea8-110">To configure this value on a single computer, complete the following procedure:</span></span>

1.  <span data-ttu-id="b8ea8-111">Klicken Sie auf dem Clientcomputer im Menü **Start** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-111">On the client computer, click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="b8ea8-112">Geben Sie im Dialogfeld **Ausführen** den Befehl regedit ein und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-112">In the **Run** dialog box, type regedit and then press ENTER.</span></span>

3.  <span data-ttu-id="b8ea8-113">Erweitern Sie im Registrierungs-Editor **HKEY \_ lokaler \_ Computer**, erweitern Sie **Software**, erweitern Sie **Richtlinien**, erweitern Sie **Microsoft**, und erweitern Sie dann **Communicator**.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-113">In Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **Software**, expand **Policies**, expand **Microsoft**, and then expand **Communicator**.</span></span>

4.  <span data-ttu-id="b8ea8-114">Klicken Sie mit der rechten Maustaste auf **Communicator**, zeigen Sie auf **Neu** und klicken Sie auf **DWORD-Wert (32-Bit)**.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-114">Right-click **Communicator**, point to **New**, and then click **DWORD (32-bit) Value**.</span></span>

5.  <span data-ttu-id="b8ea8-115">Geben Sie nach dem Erstellen des neuen Werts **PersonalContactStoreOverride** ein und drücken Sie die EINGABETASTE, um den Wert umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-115">After the new value is created, type **PersonalContactStoreOverride** and then press ENTER to rename the value.</span></span>

6.  <span data-ttu-id="b8ea8-116">Stellen Sie sicher, dass der Wert von PersonalContactStoreOverride 0 ist, und schließen Sie dann den Registrierungs-Editor.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-116">Verify that the value of PersonalContactStoreOverride is set to 0 and then close Registry Editor.</span></span>

<span data-ttu-id="b8ea8-117">Wenn Sie die gleiche Änderung auf mehreren Computern durchführen müssen, können Sie dazu ein benutzerdefiniertes Gruppenrichtlinienobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8ea8-117">If you need to make this same change on multiple computers you can do so by creating a custom Group Policy object.</span></span> <span data-ttu-id="b8ea8-118">Ausführliche Informationen finden Sie in der Gruppenrichtlinien-Dokumentation unter [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543) .</span><span class="sxs-lookup"><span data-stu-id="b8ea8-118">For details, see the Group Policy documentation at [https://go.microsoft.com/fwlink/p/?LinkId=268543](https://go.microsoft.com/fwlink/p/?linkid=268543).</span></span>

<span data-ttu-id="b8ea8-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8ea8-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

