---
title: 'Lync Server 2013: Wiederherstellen von Konferenzinhalten mithilfe des Sicherungsdiensts'
description: 'Lync Server 2013: Wiederherstellen von Konferenz Inhalten mithilfe des Sicherungsdiensts'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring conference contents using the Backup Service
ms:assetid: 3e0f18ec-7319-4c07-a59b-2938e7787bc9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688030(v=OCS.15)
ms:contentKeyID: 49733620
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3a0037af711948c008e74c5444373ed995f0e6e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442544"
---
# <a name="restoring-conference-contents-using-the-backup-service-in-lync-server-2013"></a><span data-ttu-id="57ab2-103">Wiederherstellen von Konferenzinhalten mithilfe des Sicherungsdiensts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="57ab2-103">Restoring conference contents using the Backup Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="57ab2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="57ab2-104">

<span> </span></span></span>

<span data-ttu-id="57ab2-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="57ab2-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="57ab2-106">Wenn die Konferenz Informationen, die im Dateispeicher eines Front-End-Pools gespeichert sind, nicht mehr zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="57ab2-106">If the conference information stored in the file store of a Front End pool becomes unavailable.</span></span> <span data-ttu-id="57ab2-107">Sie müssen diese Informationen so wiederherstellen, dass Benutzer, die im Pool verwaltet werden, ihre Konferenzdaten beibehalten.</span><span class="sxs-lookup"><span data-stu-id="57ab2-107">you must restore this information so that users homed on the pool retain their conference data.</span></span> <span data-ttu-id="57ab2-108">Wenn der Front-End-Pool, in dem Konferenzdaten verloren gegangen sind, mit einem anderen Front-End-Pool gekoppelt ist, können Sie die Daten mithilfe des Sicherungsdiensts wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="57ab2-108">If the Front End pool which has lost conference data is paired with another Front End pool, you can use the Backup Service to restore the data.</span></span>

<span data-ttu-id="57ab2-109">Sie müssen diese Aufgabe auch ausführen, wenn ein gesamter Pool fehlgeschlagen ist und Sie die Benutzer nicht mit einem Sicherungspool durchführen müssen.</span><span class="sxs-lookup"><span data-stu-id="57ab2-109">You must also perform this task if an entire pool has failed and you have to fail over its users to a backup pool.</span></span> <span data-ttu-id="57ab2-110">Wenn diese Benutzer wieder in ihren ursprünglichen Pool zurückgekehrt sind, müssen Sie diese Vorgehensweise verwenden, um Ihre Konferenzinhalte wieder in ihren ursprünglichen Pool zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="57ab2-110">When these users are failed back over to their original pool, you must use this procedure to copy their conference content back to their original pool as well.</span></span>

<span data-ttu-id="57ab2-111">Gehen Sie davon aus, dass pool1 mit Pool2 gekoppelt ist und die Konferenzdaten in pool1 verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="57ab2-111">Assume that Pool1 is paired with Pool2, and the conference data in Pool1 is lost.</span></span> <span data-ttu-id="57ab2-112">Sie können das folgende Cmdlet verwenden, um den Sicherungsdienst aufzurufen, um den Inhalt wiederherzustellen:</span><span class="sxs-lookup"><span data-stu-id="57ab2-112">You can use the following cmdlet to invoke the Backup Service to restore the contents:</span></span>

    Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="57ab2-113">Das Wiederherstellen der Konferenzinhalte kann je nach Größe einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="57ab2-113">Restoring the conference contents may take some time, depending on their size.</span></span> <span data-ttu-id="57ab2-114">Sie können das folgende Cmdlet verwenden, um den Prozessstatus zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="57ab2-114">You can use the following cmdlet to check the process status:</span></span>

    Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN> -BackupModule ConfServices.DataConf

<span data-ttu-id="57ab2-115">Der Vorgang erfolgt, wenn dieses Cmdlet den Wert des Steady-State-Werts für das Datenkonferenz Modul zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="57ab2-115">The process is done when this cmdlet returns a value of Steady State for the data conference module.</span></span>

<span data-ttu-id="57ab2-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="57ab2-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

