---
title: Bereitstellen eines nicht standardmäßigen SQL Server-Ports und -Alias in Lync Server 2013
description: Bereitstellen eines nicht standardmäßigen SQL Server-Ports und-Alias in lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying a SQL Server nonstandard port and alias in Lync Server 2013
ms:assetid: 2da92c1f-250e-407a-8651-fb2aec76aeb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn776290(v=OCS.15)
ms:contentKeyID: 62634609
ms.date: 09/17/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da76db2b946a47e13fe3549d7184b0b12894a83a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394035"
---
# <a name="deploying-a-sql-server-nonstandard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b0a48-103">Bereitstellen eines nicht standardmäßigen SQL Server-Ports und -Alias in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0a48-103">Deploying a SQL Server nonstandard port and alias in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0a48-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0a48-104">

<span> </span></span></span>

<span data-ttu-id="b0a48-105">_**Letztes Änderungsdatum des Themas:** 2015-09-16_</span><span class="sxs-lookup"><span data-stu-id="b0a48-105">_**Topic Last Modified:** 2015-09-16_</span></span>

<span data-ttu-id="b0a48-106">Microsoft lync Server 2013 unterstützt die Verwendung eines nicht standardmäßigen Ports und Alias in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b0a48-106">Microsoft Lync Server 2013 supports using a non-standard port and alias in SQL Server.</span></span> <span data-ttu-id="b0a48-107">Mit einem nicht standardmäßigen SQL Server-Port und einem Alias wird die Sicherheit erhöht und eine flexiblere Umgebung für die lync-Bereitstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-107">Using a SQL Server non-standard port and an alias increases security and creates a more flexible environment for the Lync deployment.</span></span> <span data-ttu-id="b0a48-108">Diese Schritte stellen nur einen einzigen Schritt bei der ordnungsgemäßen Sicherung ihrer lync Server 2013-Umgebung dar.</span><span class="sxs-lookup"><span data-stu-id="b0a48-108">These steps are only a single step in properly securing your Lync Server 2013 environment.</span></span> <span data-ttu-id="b0a48-109">Es sollten zusätzliche Schritte unternommen werden, um die Angriffsfläche einer lync Server 2013-Implementierung zu verringern.</span><span class="sxs-lookup"><span data-stu-id="b0a48-109">Additional steps should be taken to reduce the attack surface of a Lync Server 2013 implementation.</span></span>

<span data-ttu-id="b0a48-110">Im folgenden Artikel werden die Schritte beschrieben, die erforderlich sind, um einen nicht standardmäßigen SQL Server-Port und-Alias in lync Server 2013 einzurichten.</span><span class="sxs-lookup"><span data-stu-id="b0a48-110">The following article describes the steps required to setup a SQL Server non-standard port and alias in Lync Server 2013.</span></span>

<div>

## <a name="deploying-a-sql-server-non-standard-port-and-alias-in-lync-server-2013"></a><span data-ttu-id="b0a48-111">Bereitstellen eines nicht Standard mäßigen SQL Server-Ports und-Alias in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0a48-111">Deploying a SQL Server Non-Standard Port and Alias in Lync Server 2013</span></span>

<span data-ttu-id="b0a48-112">Der lync Server 2013-Topologie-Generator unterstützt die Verwendung eines SQL Server-Alias als vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) anstelle des eigentlichen SQL Server-FQDN beim Konfigurieren von lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0a48-112">Lync Server 2013 Topology Builder supports using a SQL Server alias as the Fully Qualified Domain Name (FQDN) instead of the actual SQL Server FQDN when configuring Lync Server 2013.</span></span> <span data-ttu-id="b0a48-113">Dadurch kann der tatsächliche SQL Server-FQDN vor böswilligen Angreifern verborgen werden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-113">This allows the actual SQL Server FQDN to be hidden from any malicious attacker.</span></span> <span data-ttu-id="b0a48-114">Darüber hinaus verdeckt die Verwendung eines nicht standardmäßigen Ports den tatsächlichen Port von einem beliebigen Angreifer, der versucht, die Datenbank auf dem Standard Port 1433 anzugreifen, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-114">In addition, using a non-standard port obscures the actual port from any would be attacker attempting to attack the database on the standard port 1433, as shown in the following figure.</span></span>

<span data-ttu-id="b0a48-115">![Ein Hacker weiß nicht, welche Portnummer angreifen soll.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "Ein Hacker weiß nicht, welche Portnummer angreifen soll.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-115">![A hacker doesn't know the port number to attack.](images/Dn776290.2f3923e0-2bdc-416b-a66b-bf56599eb14e(OCS.15).jpg "A hacker doesn't know the port number to attack.")</span></span>

<span data-ttu-id="b0a48-116">Um den Port zu ermitteln, der von lync Server 2013 für die Kommunikation mit SQL Server verwendet wird, muss der Angreifer alle Ports durchsuchen, um die Portinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b0a48-116">In order to be successful in determining the port Lync Server 2013 is using to communicate with SQL Server, the attacker would need to scan all ports to obtain the port information.</span></span> <span data-ttu-id="b0a48-117">Eine Portüberprüfung durch einen Angreifer erhöht die Wahrscheinlichkeit, dass die Sicherheit die Anweisung erkennen und beenden kann.</span><span class="sxs-lookup"><span data-stu-id="b0a48-117">A port scan by an attacker increases the chances that security can detect and stop the instruction.</span></span> <span data-ttu-id="b0a48-118">Zusätzlich zum Hinzufügen höherer Sicherheit mit einem nicht standardmäßigen Port können Sie auch einen SQL Server-Alias verwenden, um Flexibilität für die Bereitstellung zu bieten.</span><span class="sxs-lookup"><span data-stu-id="b0a48-118">In addition to adding increased security with a non-standard port, you can also use a SQL Server alias to provide flexibility for the deployment.</span></span> <span data-ttu-id="b0a48-119">Dies ist hilfreich, um Konfigurationsänderungen in Situationen zu verringern, in denen eine Änderung des SQL Server-namens erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b0a48-119">This is valuable in order to reduce configuration changes in situations where a SQL Server name change is required.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0a48-120">SQL Server bietet zwei Fehlertoleranz Methoden (Failover-Clustering und Spiegelung).</span><span class="sxs-lookup"><span data-stu-id="b0a48-120">SQL Server provides two fault tolerance methods (Failover Clustering and Mirroring).</span></span> <span data-ttu-id="b0a48-121">Beide SQL Server-Fehlertoleranz Methoden werden mit einem nicht standardmäßigen SQL Server-Port und-Alias mit lync Server 2013 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-121">Both SQL Server fault tolerance methods are supported using a SQL Server non-standard port and alias with Lync Server 2013.</span></span> <span data-ttu-id="b0a48-122">Wenn sich das vom Pool verwendete SQL Server-Back-End in einer gespiegelten Konfiguration befindet, sollte der SQL-Browserdienst auf den SQL Server-Back-End-Servern für Front-End-Server ausgeführt werden, um eine Verbindung mit der gespiegelten Datenbank herzustellen, wenn die Datenbanken auf den gespiegelten SQL Server übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-122">If the SQL Server backend used by the pool is in a mirrored configuration, then the SQL browser service on the SQL Server backend servers should be running for Front End servers to connect to the mirrored database when the databases are failed over to the mirrored SQL Server.</span></span>



</div>

<span data-ttu-id="b0a48-123">Wenn Sie die SQL Server-Datenbankverbindung in Topology Builder konfigurieren oder wenn Sie das Install-CsDatabase-Cmdlet verwenden, ist es nicht möglich, eine nicht standardmäßige SQL Server-Portnummer explizit zu definieren und Sie einer SQL-Instanz zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-123">When configuring SQL Server database connectivity from within Topology Builder, or when using the Install-CsDatabase cmdlet, it’s not possible to explicitly define a SQL Server non-standard port number and associate it with a SQL instance.</span></span> <span data-ttu-id="b0a48-124">Wenn Sie einen nicht standardmäßigen Port einrichten möchten, müssen Sie die SQL Server-und Windows Server-Dienstprogramme verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-124">To set a non-standard port, you’ll need to use SQL Server and Windows Server utilities.</span></span>

<span data-ttu-id="b0a48-125">Um einen nicht standardmäßigen SQL Server-Port und-Alias für die Verwendung mit lync Server 2013 einzurichten, müssen Sie drei primäre Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-125">To set up a SQL Server non-standard port and alias for use with Lync Server 2013, you will need to complete three primary steps.</span></span> <span data-ttu-id="b0a48-126">Diese Schritte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b0a48-126">These steps are:</span></span>

  - <span data-ttu-id="b0a48-127">Vergewissern Sie sich, dass lync Server 2013 die neuesten Updates installiert hat.</span><span class="sxs-lookup"><span data-stu-id="b0a48-127">Confirm that Lync Server 2013 has the Latest Updates Applied.</span></span>

  - <span data-ttu-id="b0a48-128">Richten Sie den SQL Server-Port und-Alias nicht Standard mäßig ein.</span><span class="sxs-lookup"><span data-stu-id="b0a48-128">Setup the SQL Server Non-Standard Port and Alias.</span></span>

  - <span data-ttu-id="b0a48-129">Konfigurieren Sie lync Server 2013 mit dem SQL Server-Alias mithilfe des Topologie-Generators.</span><span class="sxs-lookup"><span data-stu-id="b0a48-129">Configure Lync Server 2013 with the SQL Server alias using Topology Builder.</span></span>

  - <span data-ttu-id="b0a48-130">Veröffentlichen Sie die Topologie, und überprüfen Sie die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b0a48-130">Publish the Topology, and Verify the Database.</span></span>

<div>

## <a name="confirm-that-lync-server-2013-has-the-latest-updates-applied"></a><span data-ttu-id="b0a48-131">Überprüfen, ob lync Server 2013 die neuesten Updates angewendet hat</span><span class="sxs-lookup"><span data-stu-id="b0a48-131">Confirm that Lync Server 2013 has the Latest Updates Applied</span></span>

<span data-ttu-id="b0a48-132">Es ist wichtig, lync Server 2013 auf dem neuesten Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="b0a48-132">It is important to keep Lync Server 2013 up to date.</span></span> <span data-ttu-id="b0a48-133">Informationen zum Überprüfen der neuesten Updates und Informationen zur Anwendung finden Sie unter [Updates für lync Server 2013](https://support.microsoft.com/kb/2809243).</span><span class="sxs-lookup"><span data-stu-id="b0a48-133">To check for the most recent updates and information on how to apply them, see [Updates for Lync Server 2013](https://support.microsoft.com/kb/2809243).</span></span>

</div>

<div>

## <a name="setup-the-sql-server-non-standard-port-and-alias"></a><span data-ttu-id="b0a48-134">Einrichten des nicht Standard mäßigen SQL Server-Ports und-Alias</span><span class="sxs-lookup"><span data-stu-id="b0a48-134">Setup the SQL Server Non-Standard Port and Alias</span></span>

<span data-ttu-id="b0a48-135">Der SQL Server-Port und der nicht standardmäßige Alias müssen für die Datenbankinstanz eingerichtet werden, bevor Sie vom lync Server 2013-Topologie-Generator referenziert werden können.</span><span class="sxs-lookup"><span data-stu-id="b0a48-135">The SQL Server non-standard port and alias must be set up on the database instance before it can be referenced from Lync Server 2013 Topology Builder.</span></span> <span data-ttu-id="b0a48-136">Um einen nicht standardmäßigen SQL Server-Port und-Alias einzurichten, müssen Sie drei primäre Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-136">To set up a SQL Server non-standard port and alias, you will have to complete three primary steps.</span></span> <span data-ttu-id="b0a48-137">Diese Schritte sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b0a48-137">These steps are as follows:</span></span>

  - <span data-ttu-id="b0a48-138">Ändern Sie die Standardwerte für TCP/IP-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="b0a48-138">Change the Default TCP/IP Protocol Values.</span></span>

  - <span data-ttu-id="b0a48-139">Erstellen und konfigurieren Sie einen SQL Server-Alias.</span><span class="sxs-lookup"><span data-stu-id="b0a48-139">Create and Configure a SQL Server Alias.</span></span>

  - <span data-ttu-id="b0a48-140">Erstellen Sie einen CNAME-Ressourceneintrag (Domain Name System).</span><span class="sxs-lookup"><span data-stu-id="b0a48-140">Create a Domain Name System (DNS) Canonical Name (CNAME) Resource Record.</span></span>

<span data-ttu-id="b0a48-141">**Ändern der Standardwerte für TCP/IP-Protokolle**</span><span class="sxs-lookup"><span data-stu-id="b0a48-141">**Modify the Default TCP/IP Protocol Values**</span></span>

1.  <span data-ttu-id="b0a48-142">Wählen Sie **Start** aus, und wählen Sie **SQL Server-Konfigurations-Manager** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-142">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-143">![Das SQL Server Management Studio-Symbol](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Das SQL Server Management Studio-Symbol")</span><span class="sxs-lookup"><span data-stu-id="b0a48-143">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b0a48-144">Wählen Sie im Navigationsbereich aus, um die **SQL Server-Instanz** zu erweitern, wählen Sie aus, um die **SQL Server-Netzwerkkonfiguration** zu erweitern, und wählen Sie **Protokolle für aus \<instance name\>**, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-144">In the navigation pane, choose to expand the **SQL Server instance**, choose to expand **SQL Server Network Configuration**, and choose **Protocols for \<instance name\>**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-145">![Navigieren Sie zu den TCP/IP-Eigenschaften.](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigieren Sie zu den TCP/IP-Eigenschaften.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-145">![Navigate to TCP/IP Properties](images/Dn776290.3d7a964c-f17e-47fd-8f0c-535453da7fad(OCS.15).jpg "Navigate to TCP/IP Properties")</span></span>

3.  <span data-ttu-id="b0a48-146">Klicken Sie im rechten Bereich mit der rechten Maustaste auf **TCP/IP**, und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="b0a48-146">In the right pane, right-click **TCP/IP**, and select **Properties**.</span></span> <span data-ttu-id="b0a48-147">Das Dialogfeld TCP/IP-Eigenschaften wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-147">The TCP/IP Properties dialog box is displayed.</span></span>

4.  <span data-ttu-id="b0a48-148">Wählen Sie die Registerkarte **IP-Adressen** aus. Auf der Registerkarte IP-Adressen werden alle aktiven IP-Adressen auf dem Server angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-148">Select the **IP Addresses** tab. The IP Addresses tab shows all of the active IP addresses on the server.</span></span> <span data-ttu-id="b0a48-149">Diese befinden sich im Format IP1, IP2, bis zu IPAll, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-149">These are in the format IP1, IP2, up to IPAll, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-150">![Öffnen Sie die TCP/IP-Eigenschaften.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Öffnen Sie die TCP/IP-Eigenschaften.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-150">![Open TCP/IP properties.](images/Dn776290.ed2fd70d-1836-4ebf-80fe-09191d96585e(OCS.15).jpg "Open TCP/IP properties.")</span></span>

5.  <span data-ttu-id="b0a48-151">Deaktivieren Sie das Feld **TCP Dynamic Ports** für alle IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-151">Clear the **TCP Dynamic Ports** field for all IP addresses.</span></span> <span data-ttu-id="b0a48-152">Wenn das Feld ein Nullzeichen enthält, bedeutet dies, dass SQL Server dynamische Ports überwacht.</span><span class="sxs-lookup"><span data-stu-id="b0a48-152">If the field contains a zero character, then it means SQL Server is listening on dynamic ports.</span></span> <span data-ttu-id="b0a48-153">Stellen Sie sicher, dass diese Felder deaktiviert sind und keine 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0a48-153">Make sure these fields are cleared and do not contain a zero.</span></span>

6.  <span data-ttu-id="b0a48-154">Stellen Sie für die IP-Adresse, die von lync Server für die Verbindung mit der Datenbank verwendet wird, sicher, dass **Enabled** auf **Ja** festgesetzt ist, wie in der folgenden Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-154">For the IP address that Lync Server will be using to connect to the database, make sure that **Enabled** is set to **Yes**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-155">![Aktivieren Sie die richtige IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Aktivieren Sie die richtige IP.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-155">![Set enabled as Yes for the correct IP.](images/Dn776290.7f818b91-0793-4594-8932-90447270fad9(OCS.15).jpg "Set enabled as Yes for the correct IP.")</span></span>

7.  <span data-ttu-id="b0a48-156">Geben Sie im Abschnitt **IPAll** am unteren Rand des Dialogfelds den gewünschten Port im Feld **TCP-Port** ein, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-156">In the **IPAll** section at the bottom of the dialog, enter the desired port in the **TCP Port** field, as shown in the following figure.</span></span> <span data-ttu-id="b0a48-157">In diesem Beispiel verwenden wir Port 50062, Sie können jedoch einen beliebigen Port zwischen 49152 und 65535 verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-157">In this example, we use port 50062, but you can use any port between 49152 and 65535.</span></span> <span data-ttu-id="b0a48-158">Hierbei handelt es sich um die Ports, die der dynamischen und privaten Verwendung zugewiesen sind, und dadurch wird sichergestellt, dass Sie keinen Konflikt mit anderen in der lync Server 2013-Bereitstellung verwendeten Anschlüssen verursachen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-158">These are the ports assigned to dynamic and private use, and this ensures you won’t conflict with other ports being used in the Lync Server 2013 deployment.</span></span>
    
    <span data-ttu-id="b0a48-159">![Port im IPAll-Abschnitt einstellen.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Port im IPAll-Abschnitt einstellen.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-159">![Set port in IPAll section.](images/Dn776290.b5af53e2-7961-4664-b586-3ca8f3a17f06(OCS.15).jpg "Set port in IPAll section.")</span></span>

8.  <span data-ttu-id="b0a48-160">Wählen Sie **OK** aus, um das Dialogfeld TCP/IP-Eigenschaften zu beenden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-160">Choose **OK** to exit the TCP/IP Properties dialog.</span></span>

9.  <span data-ttu-id="b0a48-161">Starten Sie die SQL Server-Instanz neu, indem Sie im linken Bereich des SQL Server-Konfigurations-Managers **SQL Server-Dienste** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-161">Restart the SQL Server instance by selecting **SQL Server Services** in the left pane of SQL Server Configuration Manager.</span></span> <span data-ttu-id="b0a48-162">Klicken Sie dann im rechten Bereich mit der rechten Maustaste auf **SQL Server \<instance name\>** , und wählen Sie dann **neu starten** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-162">Then right-click **SQL Server \<instance name\>** in the right pane, and select **Restart**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-163">![Setzen Sie den SQL Server-Dienst zum Beispiel zurück.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Setzen Sie den SQL Server-Dienst zum Beispiel zurück.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-163">![Reset the SQL Server service for instance.](images/Dn776290.a965c8cf-f769-4b52-bb38-c48a438cf491(OCS.15).jpg "Reset the SQL Server service for instance.")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b0a48-164">Stellen Sie sicher, dass Sie Ihre Firewalleinstellungen so aktualisieren, dass Sie den neuen SQL Server-Port aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-164">Make sure you update your firewall settings to accommodate the new SQL Server port.</span></span>



</div>

<span data-ttu-id="b0a48-165">**Erstellen und Konfigurieren eines SQL Server-Alias**</span><span class="sxs-lookup"><span data-stu-id="b0a48-165">**Create and Configure a SQL Server Alias**</span></span>

1.  <span data-ttu-id="b0a48-166">Wählen Sie **Start** aus, und wählen Sie **SQL Server-Konfigurations-Manager** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-166">Select **Start**, and choose **SQL Server Configuration Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-167">![Das SQL Server Management Studio-Symbol](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "Das SQL Server Management Studio-Symbol")</span><span class="sxs-lookup"><span data-stu-id="b0a48-167">![The SQL Server Management Studio icon](images/Dn776290.6e811f27-cea9-4437-b44c-55bff013150f(OCS.15).png "The SQL Server Management Studio icon")</span></span>

2.  <span data-ttu-id="b0a48-168">Wählen Sie im linken Bereich die Option zum Erweitern der **SQL Server-Instanz** aus, wählen Sie aus, um die **SQL Native Client- \<version\> Konfiguration** zu erweitern, und wählen Sie dann **Aliase** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-168">In the left pane, choose to expand **SQL Server instance**, choose to expand **SQL Native Client \<version\> Configuration**, and then choose **Aliases**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-169">![Aliase im SQL Server-Konfigurations-Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliase im SQL Server-Konfigurations-Manager.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-169">![Aliases in SQL Server Configuration Manager.](images/Dn776290.95341826-55d7-425f-ae19-d47d6668c5d8(OCS.15).jpg "Aliases in SQL Server Configuration Manager.")</span></span>

3.  <span data-ttu-id="b0a48-170">Klicken Sie mit der rechten Maustaste auf **Aliase**, und wählen Sie **Neuer Alias** aus.</span><span class="sxs-lookup"><span data-stu-id="b0a48-170">Right-click **Aliases**, and select **New Alias…**.</span></span>

4.  <span data-ttu-id="b0a48-171">Geben Sie den **Alias Namen**, die **Port Nummer**, das **Protokoll** und den **Server** ein, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-171">Enter the **Alias Name**, **Port Number**, **Protocol**, and **Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-172">![Erstellen eines neuen Alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Erstellen eines neuen Alias")</span><span class="sxs-lookup"><span data-stu-id="b0a48-172">![Creating a new alias](images/Dn776290.03653588-aecf-4fdd-b58a-95f5b372d478(OCS.15).jpg "Creating a new alias")</span></span>
    
    <div>
    

    > [!CAUTION]  
    > <span data-ttu-id="b0a48-173">Stellen Sie sicher, dass Sie den gleichen nicht standardmäßigen Port eingeben, den Sie im vorherigen Schritt verwendet haben, da dies der Port ist, der von SQL Server überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="b0a48-173">Make sure to enter the same non-standard port you used in the previous step since that is the port SQL Server will be listening on.</span></span> <span data-ttu-id="b0a48-174">Wenn ein konfigurierter Alias eine Verbindung mit dem falschen SQL Server-FQDN oder-Beispiel herstellt, deaktivieren Sie das zugeordnete Netzwerkprotokoll, und aktivieren Sie es dann erneut.</span><span class="sxs-lookup"><span data-stu-id="b0a48-174">If a configured alias is connecting to the wrong SQL Server FQDN or Instance, disable and then re-enable the associated network protocol.</span></span> <span data-ttu-id="b0a48-175">Dadurch werden alle zwischengespeicherten Verbindungsinformationen gelöscht, und der Client kann eine ordnungsgemäße Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-175">Doing this clears any cached connection information and allows the client to connect correctly.</span></span>

    
    </div>

<span data-ttu-id="b0a48-176">**Erstellen eines DNS-CNAME-Ressourceneintrags**</span><span class="sxs-lookup"><span data-stu-id="b0a48-176">**Create a DNS CNAME Resource Record**</span></span>

1.  <span data-ttu-id="b0a48-177">Registrieren Sie sich beim Computer, der DNS verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b0a48-177">Sign into the computer managing DNS.</span></span>

2.  <span data-ttu-id="b0a48-178">Wählen Sie **Start** aus, und wählen Sie **Server-Manager** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-178">Select **Start**, and choose **Server Manager**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-179">![Öffnen des Server-Managers](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Öffnen des Server-Managers")</span><span class="sxs-lookup"><span data-stu-id="b0a48-179">![Opening Server Manager](images/Dn776290.3e4bd8ad-2a65-4a05-af40-c8dd3583bc8f(OCS.15).jpg "Opening Server Manager")</span></span>

3.  <span data-ttu-id="b0a48-180">Wählen Sie die Dropdownliste **Tools** aus, und wählen Sie **DNS** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-180">Choose the **Tools** drop-down, and select **DNS**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-181">![Öffnen von DNS im Server-Manager](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Öffnen von DNS im Server-Manager")</span><span class="sxs-lookup"><span data-stu-id="b0a48-181">![Opening DNS from Server Manager.](images/Dn776290.415e1da1-7c9a-4a4e-a896-ca34a76aaeff(OCS.15).jpg "Opening DNS from Server Manager.")</span></span>

4.  <span data-ttu-id="b0a48-182">Erweitern Sie im linken Bereich den Knoten Servername, erweitern Sie den Knoten Forward Lookup Zones, und wählen Sie die entsprechende Domäne aus.</span><span class="sxs-lookup"><span data-stu-id="b0a48-182">In the left pane, expand the server name node, expand the Forward Lookup Zones node, and choose the relevant domain.</span></span>

5.  <span data-ttu-id="b0a48-183">Klicken Sie mit der rechten Maustaste auf die Domäne, und wählen Sie **Neuer Alias (CNAME)...** aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-183">Right-click the domain, and select **New Alias (CNAME)…**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-184">![Auswählen der Option zum Erstellen eines neuen Alias-CNAMES](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Auswählen der Option zum Erstellen eines neuen Alias-CNAMES")</span><span class="sxs-lookup"><span data-stu-id="b0a48-184">![Selecting option to create a new alias CNAME](images/Dn776290.abe66cca-b53c-427a-9094-1a59dc6840ca(OCS.15).jpg "Selecting option to create a new alias CNAME")</span></span>

6.  <span data-ttu-id="b0a48-185">Geben Sie den **Alias Namen** und den **FQDN für SQL Server** ein, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-185">Enter the **Alias Name** and the **FQDN for SQL Server**, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-186">![Ausfüllen des neuen Alias-CNAME-Dialogfelds](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Ausfüllen des neuen Alias-CNAME-Dialogfelds")</span><span class="sxs-lookup"><span data-stu-id="b0a48-186">![Filling in the new alias CNAME dialog.](images/Dn776290.dd0ebd2d-3407-4459-8bd9-2b389a7bc440(OCS.15).jpg "Filling in the new alias CNAME dialog.")</span></span>

7.  <span data-ttu-id="b0a48-187">Wählen Sie **OK** aus, um den CNAME zu speichern und im DNS-Manager anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-187">Choose **OK** to save the CNAME and view it in DNS Manager.</span></span>

</div>

<div>

## <a name="validate-database-connectivity"></a><span data-ttu-id="b0a48-188">Überprüfen der Datenbankkonnektivität</span><span class="sxs-lookup"><span data-stu-id="b0a48-188">Validate Database Connectivity</span></span>

<span data-ttu-id="b0a48-189">Es gibt viele verschiedene Möglichkeiten, um sicherzustellen, dass es funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b0a48-189">There are many different ways to make sure it is working.</span></span> <span data-ttu-id="b0a48-190">Sie möchten sicherstellen, dass die SQL Server-Datenbank den angegebenen Port mithilfe des Alias abhört.</span><span class="sxs-lookup"><span data-stu-id="b0a48-190">You want to make sure that the SQL Server database is listening on the specified port using the alias.</span></span> <span data-ttu-id="b0a48-191">Eine Schnellüberprüfung kann mithilfe der Befehle **netstat** und **Telnet** ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-191">A quick check can be completed using the **netstat** and **telnet** commands.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b0a48-192">Der Telnet-Client ist ein Feature, das im Lieferumfang von Windows Server enthalten ist, aber installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b0a48-192">Telnet Client is a Feature that comes with Windows Server but that must be installed.</span></span> <span data-ttu-id="b0a48-193">Sie können ein Windows Server-Feature installieren, indem Sie Server-Manager öffnen und im Menü verwalten die Option Rollen und Features hinzufügen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-193">A Windows Server Feature can be installed by opening Server Manager and selecting Add Roles and Features from the Manage menu.</span></span>



</div>

<span data-ttu-id="b0a48-194">**Verwenden von netstat und Telnet zur Überprüfung der Datenbankkonnektivität**</span><span class="sxs-lookup"><span data-stu-id="b0a48-194">**Use netstat and telnet to verify database connectivity**</span></span>

1.  <span data-ttu-id="b0a48-195">Wählen Sie **Start** aus, und geben Sie **cmd** ein, um eine Eingabeaufforderung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-195">Select **Start**, and type **cmd** to open a command prompt.</span></span>

2.  <span data-ttu-id="b0a48-196">Geben Sie **netstat-a-f ein**, und vergewissern Sie sich, dass SQL Server mit dem richtigen Port ausgeführt wird, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0a48-196">Type **netstat -a -f**, and confirm that SQL Server is running with the correct port, as shown in the following figure.</span></span>
    
    <span data-ttu-id="b0a48-197">![Verwenden Sie netstat, um den Port zu überprüfen.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Verwenden Sie netstat, um den Port zu überprüfen.")</span><span class="sxs-lookup"><span data-stu-id="b0a48-197">![Using netstat to verify port.](images/Dn776290.4ff3a1b2-c5eb-4496-8be7-374c351fa027(OCS.15).jpg "Using netstat to verify port.")</span></span>

3.  <span data-ttu-id="b0a48-198">Geben **Sie \<alias name\> \<port \#\> Telnet** ein, um die Verbindung mit der SQL Server-Instanz zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-198">Type **telnet \<alias name\> \<port \#\>** to confirm the connection to the SQL Server instance.</span></span> <span data-ttu-id="b0a48-199">Wenn die Verbindung erfolgreich hergestellt wurde, stellt Telnet eine Verbindung her, und Sie sollten keinen Fehler sehen.</span><span class="sxs-lookup"><span data-stu-id="b0a48-199">If the connection is successful, telnet will connect and you shouldn’t see an error.</span></span> <span data-ttu-id="b0a48-200">Dies zeigt, dass die SQL Server-Instanz den richtigen Port mit dem richtigen Alias abhört.</span><span class="sxs-lookup"><span data-stu-id="b0a48-200">This shows that the SQL Server instance is listening on the correct port with the correct alias.</span></span> <span data-ttu-id="b0a48-201">Wenn beim Herstellen einer Verbindung mit der SQL Server-Datenbank ein Problem auftritt, zeigt Telnet einen Fehler an, dass die Verbindung nicht hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0a48-201">If there’s a problem connecting to the SQL Server database, then telnet shows an error that the connection cannot be made.</span></span> <span data-ttu-id="b0a48-202">Nachdem Sie nun die Datenbankkonnektivität auf dem Datenbankserver überprüft haben, können Sie das gleiche von lync Server (über das Netzwerk) durchführen und sicherstellen, dass keine Firewalls den Zugriff auf dem Weg blockieren.</span><span class="sxs-lookup"><span data-stu-id="b0a48-202">Now that you have checked database connectivity on the database server, you can do the same thing from Lync Server (over the network) and make sure there aren’t any firewalls blocking access along the way.</span></span>

</div>

<div>

## <a name="conclusion"></a><span data-ttu-id="b0a48-203">Fazit</span><span class="sxs-lookup"><span data-stu-id="b0a48-203">Conclusion</span></span>

<span data-ttu-id="b0a48-204">Nachdem der SQL Server-Alias konfiguriert wurde, können Sie ihn zum Erstellen einer lync Server 2013-Topologie im Tool Topologie-Generator verwenden.</span><span class="sxs-lookup"><span data-stu-id="b0a48-204">Once the SQL Server alias has been configured, you can use it to create a Lync Server 2013 topology in the Topology Builder tool.</span></span> <span data-ttu-id="b0a48-205">Weitere Informationen zu Topologien finden Sie unter [definieren und Konfigurieren der Topologie in lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span><span class="sxs-lookup"><span data-stu-id="b0a48-205">For more information about topologies, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b0a48-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a48-206">See Also</span></span>


<span data-ttu-id="b0a48-207">[Microsoft lync Server 2013](microsoft-lync-server-2013.md)  
 [Planen der Sicherheit in lync Server 2013](lync-server-2013-planning-for-security.md)</span><span class="sxs-lookup"><span data-stu-id="b0a48-207">[Microsoft Lync Server 2013](microsoft-lync-server-2013.md) 
[Planning for security in Lync Server 2013](lync-server-2013-planning-for-security.md)</span></span>  
[<span data-ttu-id="b0a48-208">Definieren und Konfigurieren der Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0a48-208">Defining and configuring the topology in Lync Server 2013</span></span>](lync-server-2013-defining-and-configuring-the-topology.md)  
[<span data-ttu-id="b0a48-209">Bereitstellen von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0a48-209">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="b0a48-210"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0a48-210"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

