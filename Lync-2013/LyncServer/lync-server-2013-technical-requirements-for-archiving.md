---
title: 'Lync Server 2013: Technische Voraussetzungen für die Archivierung'
description: 'Lync Server 2013: Technische Voraussetzungen für die Archivierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Archiving
ms:assetid: 896d60e2-be4b-462d-8357-4cd307ab7304
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205059(v=OCS.15)
ms:contentKeyID: 48184732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6100753ad2c62424eb68c8c258094ba51848170e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423386"
---
# <a name="technical-requirements-for-archiving-in-lync-server-2013"></a><span data-ttu-id="5f1f1-103">Technische Voraussetzungen für die Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1f1-103">Technical requirements for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f1f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f1f1-104">

<span> </span></span></span>

<span data-ttu-id="5f1f1-105">_**Letztes Änderungsdatum des Themas:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="5f1f1-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="5f1f1-106">Die technischen Voraussetzungen für lync Server 2013 umfassen die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5f1f1-106">Lync Server 2013 technical requirements include the following:</span></span>

  - <span data-ttu-id="5f1f1-107">Infrastrukturanforderungen.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-107">Infrastructure requirements.</span></span>

  - <span data-ttu-id="5f1f1-108">Erforderliche Software, die für die Archivierung installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-108">Prerequisite software that must be installed for Archiving.</span></span>

  - <span data-ttu-id="5f1f1-109">Datenspeicheranforderungen für die Archivierung</span><span class="sxs-lookup"><span data-stu-id="5f1f1-109">Data storage requirements for Archiving.</span></span>

  - <span data-ttu-id="5f1f1-110">Skalierungsanforderungen und Überlegungen für die Archivierungs Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-110">Scaling requirements and considerations for your Archiving deployment.</span></span>

  - <span data-ttu-id="5f1f1-111">Leistungsanforderungen und Überlegungen für Ihre Archivierungsdatenbanken.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-111">Performance requirements and considerations for your Archiving databases.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5f1f1-112">Skalierungs-und Leistungsinformationen stehen in dieser lync Server 2013-Version nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-112">Scaling and performance information is not available in this Lync Server 2013 release.</span></span>



</div>

<div>

## <a name="infrastructure-requirements"></a><span data-ttu-id="5f1f1-113">Infrastrukturanforderungen</span><span class="sxs-lookup"><span data-stu-id="5f1f1-113">Infrastructure Requirements</span></span>

<span data-ttu-id="5f1f1-114">Die Anforderungen der Archivierungsinfrastruktur für lync Server 2013 sind identisch mit der Bereitstellung von lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-114">Lync Server 2013 Archiving infrastructure requirements are the same as for deployment of Lync Server 2013.</span></span> <span data-ttu-id="5f1f1-115">Ausführliche Informationen finden Sie unter [Ermitteln der Infrastrukturanforderungen für lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-115">For details, see [Determining your infrastructure requirements for Lync Server 2013](lync-server-2013-determining-your-infrastructure-requirements.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-prerequisites"></a><span data-ttu-id="5f1f1-116">Archivierungs Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5f1f1-116">Archiving Prerequisites</span></span>

<span data-ttu-id="5f1f1-117">Lync Server 2013 optimiert die Voraussetzungen für die Archivierung aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="5f1f1-117">Lync Server 2013 streamlines prerequisites for Archiving because of the following:</span></span>

  - <span data-ttu-id="5f1f1-118">Der Archivierungsserver ist keine Serverrolle mehr.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-118">Archiving Server is no longer a server role.</span></span> <span data-ttu-id="5f1f1-119">Stattdessen werden Unified Data Collection-Agents auf den Front-End-Servern in einem Pool und auf Standard Edition-Servern ausgeführt, um Daten für die Archivierung zu erfassen, sodass Sie keine separaten Systemplattformen für die Archivierung einrichten.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-119">Instead, Unified Data Collection Agents run on the Front End Servers in a pool and Standard Edition servers to capture data for Archiving, so you do not set up separate system platforms for Archiving.</span></span>

  - <span data-ttu-id="5f1f1-120">Bei der Archivierung wird der lync Server 2013-Dateispeicher zur temporären Speicherung von Besprechungsinhalts Dateien verwendet, sodass Sie keinen separaten Dateispeicher für die Archivierung einrichten.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-120">Archiving uses the Lync Server 2013 file storage for temporary storage of meeting content files, so you do not set up a separate file store for archiving.</span></span>

  - <span data-ttu-id="5f1f1-121">In lync Server 2013 ist Message Queuing nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-121">In Lync Server 2013, Message Queuing is not required.</span></span>

</div>

<div>

## <a name="data-storage-requirements-for-archiving"></a><span data-ttu-id="5f1f1-122">Datenspeicheranforderungen für die Archivierung</span><span class="sxs-lookup"><span data-stu-id="5f1f1-122">Data Storage Requirements for Archiving</span></span>

<span data-ttu-id="5f1f1-123">Darüber hinaus müssen Sie die Infrastruktur für die Archivierung von Speicher einrichten.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-123">Additionally, you need to set up the infrastructure for Archiving storage.</span></span> <span data-ttu-id="5f1f1-124">Dazu gehören eine oder beide der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="5f1f1-124">This includes one or both of the following:</span></span>

  - <span data-ttu-id="5f1f1-125">**Microsoft Exchange-Speicher**.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-125">**Microsoft Exchange storage**.</span></span> <span data-ttu-id="5f1f1-126">Besprechungsinhalts Dateien wie PowerPoint-Präsentationen werden als Anlagen archiviert.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-126">Meeting content files, such as PowerPoint presentations, are archived as attachments.</span></span> <span data-ttu-id="5f1f1-127">Wenn Sie die Microsoft Exchange-Integration verwenden möchten, damit lync-Archivdaten mit Exchange-Kompatibilitätsdaten gespeichert werden, müssen Sie Exchange 2013 für Ihre Exchange-Bereitstellung verwenden und sicherstellen, dass die maximale Speichergröße die Speicherung der Besprechungsinhalts Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-127">If you want to use Microsoft Exchange integration so that Lync archive data is stored with Exchange compliance data, you must use Exchange 2013 for your Exchange deployment and ensure that the maximum storage size supports storage of the meeting content files.</span></span> <span data-ttu-id="5f1f1-128">Wenn Sie die Archivierung mithilfe der Microsoft Exchange-Integrations Option bereitstellen, werden lync-Archivdaten nur für die Benutzer, die auf Ihren Exchange 2013-Servern gehostet werden, mit Exchange 2013-Kompatibilitätsdaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-128">If you deploy Archiving using the Microsoft Exchange integration option, Lync archive data is stored with Exchange 2013 compliance data only for the users who are homed on your Exchange 2013 servers.</span></span> <span data-ttu-id="5f1f1-129">Sie müssen Exchange 2013 vor der Bereitstellung und Aktivierung der Archivierung mithilfe der Microsoft Exchange-Integrations Option bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-129">You must deploy Exchange 2013 prior to deploying and enabling Archiving using the Microsoft Exchange integration option.</span></span> <span data-ttu-id="5f1f1-130">Wenn Sie Exchange 2013-Speicher verwenden, müssen Sie keine separaten SQL Server-Datenbanken für die Archivierung bereitstellen, es sei denn, Sie verfügen über lync-Benutzer, die nicht auf Ihren Exchange 2013-Servern gehostet sind.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-130">If you choose to use Exchange 2013 storage, you do not need to deploy separate SQL Server databases for Archiving, unless you have Lync users who are not homed on your Exchange 2013 servers.</span></span>

  - <span data-ttu-id="5f1f1-131">**SQL Server-Datenbankspeicher für die Archivierung**.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-131">**SQL Server database storage for Archiving**.</span></span> <span data-ttu-id="5f1f1-132">Wenn Sie Benutzer unterstützen möchten, die nicht auf Exchange 2013-Servern gehostet werden, oder wenn Sie die Microsoft Exchange-Integrations Option nicht verwenden möchten, müssen Sie den Archivierungsspeicher mithilfe einer SQL Server-Datenbank bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-132">To support users who are not homed on Exchange 2013 servers, or if you do not want to use the Microsoft Exchange integration option, you must deploy Archiving storage using a SQL Server database.</span></span> <span data-ttu-id="5f1f1-133">Lync Server 2013 unterstützt die folgenden 64-Bit-Versionen von SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f1f1-133">Lync Server 2013 supports the following 64-bit versions of SQL Server:</span></span>
    
      - <span data-ttu-id="5f1f1-134">Microsoft SQL Server 2008 R2 Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f1f1-134">Microsoft SQL Server 2008 R2 Enterprise</span></span>
    
      - <span data-ttu-id="5f1f1-135">Microsoft SQL Server 2008 R2 Standard</span><span class="sxs-lookup"><span data-stu-id="5f1f1-135">Microsoft SQL Server 2008 R2 Standard</span></span>
    
      - <span data-ttu-id="5f1f1-136">Microsoft SQL Server 2012 Enterprise</span><span class="sxs-lookup"><span data-stu-id="5f1f1-136">Microsoft SQL Server 2012 Enterprise</span></span>
    
      - <span data-ttu-id="5f1f1-137">Microsoft SQL Server 2012 Standard</span><span class="sxs-lookup"><span data-stu-id="5f1f1-137">Microsoft SQL Server 2012 Standard</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5f1f1-138">Microsoft SQL Server 2008 R2 Express und Microsoft SQL Server 2012 Express werden für die Archivierung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-138">Microsoft SQL Server 2008 R2 Express and Microsoft SQL Server 2012 Express are not supported for Archiving.</span></span> <span data-ttu-id="5f1f1-139">32-Bit-Versionen von SQL Server werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-139">32-bit versions of SQL Server are not supported.</span></span> <span data-ttu-id="5f1f1-140">Weitere SQL Server-Anforderungen und-Einschränkungen finden Sie unter unter <A href="lync-server-2013-database-software-support.md">Stützung von Datenbanksoftware in lync Server 2013</A> in der Planungsdokumentation oder in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-140">For additional SQL Server requirements and restrictions, see <A href="lync-server-2013-database-software-support.md">Database software support in Lync Server 2013</A> in the Planning documentation or in the Supportability documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="5f1f1-141">Sie müssen die SQL Server-Plattformen einrichten, bevor Sie die Archivierung bereitstellen und aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-141">You must set up the SQL Server platforms prior to deploying and enabling Archiving.</span></span> <span data-ttu-id="5f1f1-142">Wenn das Konto, das zum Veröffentlichen der Topologie verwendet werden soll, mit den erforderlichen Administratorrechten und -berechtigungen ausgestattet ist, können Sie die Archivierungsdatenbank (LcsLog) beim Veröffentlichen der Topologie erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-142">If the account to be used to publish the topology has the appropriate administrator rights and permissions, you can create the Archiving database (LcsLog) when you publish your topology.</span></span> <span data-ttu-id="5f1f1-143">Sie können die Datenbank auch später erstellen, auch als Teil des Installationsvorgangs.</span><span class="sxs-lookup"><span data-stu-id="5f1f1-143">You can also create the database later, including as part of the installation procedure.</span></span> <span data-ttu-id="5f1f1-144">Ausführliche Informationen zu SQL Server finden Sie im SQL Server TechCenter unter [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045) .</span><span class="sxs-lookup"><span data-stu-id="5f1f1-144">For details about SQL Server, see the SQL Server TechCenter at [https://go.microsoft.com/fwlink/p/?linkID=129045](https://go.microsoft.com/fwlink/p/?linkid=129045).</span></span>

<span data-ttu-id="5f1f1-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f1f1-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

