---
title: Benutzerprofil konfigurieren
description: Benutzerprofil konfigurieren.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure User Profile
ms:assetid: 52713245-e502-4539-a238-66ff1aca26b1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945594(v=OCS.15)
ms:contentKeyID: 51541419
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 682297da43797dd2d774094e85e8688ef3c64d98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443699"
---
# <a name="configure-user-profile"></a><span data-ttu-id="558e1-103">Benutzerprofil konfigurieren</span><span class="sxs-lookup"><span data-stu-id="558e1-103">Configure User Profile</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="558e1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="558e1-104">

<span> </span></span></span>

<span data-ttu-id="558e1-105">_**Letztes Änderungsdatum des Themas:** 2018-10-11_</span><span class="sxs-lookup"><span data-stu-id="558e1-105">_**Topic Last Modified:** 2018-10-11_</span></span>

<span data-ttu-id="558e1-106">Die im lync Server 2013-Tool für Stress und Leistung enthaltenen Tools ermöglichen es Ihnen, Testbenutzerkonten zu erstellen und zu konfigurieren, die Sie zum Ausführen von Auslastungssimulationen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="558e1-106">The tools included in the Lync Server 2013 Stress and Performance Tool package enable you to create and configure test user accounts that you can use to run load simulations.</span></span> <span data-ttu-id="558e1-107">Verwenden Sie das Benutzer Erstellungs Tool von lync Server 2013, um die Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="558e1-107">Use the Lync Server 2013 User Creation Tool to create the users.</span></span> <span data-ttu-id="558e1-108">(Weitere Informationen finden Sie unter [Erstellen von Benutzern und Kontakten](create-users-and-contacts.md).) Nachdem Benutzer erstellt wurden, konfigurieren Sie die Benutzerprofile mithilfe des lync Server 2013 Load Configuration-Tools.</span><span class="sxs-lookup"><span data-stu-id="558e1-108">(For details, see [Create Users and Contacts](create-users-and-contacts.md).) After users are created, configure the user profiles by using the Lync Server 2013 Load Configuration Tool.</span></span>

<div>

## <a name="running-the-lync-server-2013-load-configuration-tool"></a><span data-ttu-id="558e1-109">Ausführen des lync Server 2013 Load Configuration Tools</span><span class="sxs-lookup"><span data-stu-id="558e1-109">Running the Lync Server 2013 Load Configuration Tool</span></span>

<span data-ttu-id="558e1-110">Wenn Sie Benutzerprofile konfigurieren möchten, führen Sie das lync Server 2013 Load Configuration Tool (UserProfileGenerator.exe) aus, und füllen Sie die einzelnen Registerkarten aus.</span><span class="sxs-lookup"><span data-stu-id="558e1-110">To configure user profiles, run the Lync Server 2013 Load Configuration Tool (UserProfileGenerator.exe) and fill out each of the tabs.</span></span> <span data-ttu-id="558e1-111">UserProfileGenerator.exe generiert ein Verzeichnis für jeden Clientcomputer, den Sie zum Ausführen der Simulation benötigen.</span><span class="sxs-lookup"><span data-stu-id="558e1-111">UserProfileGenerator.exe generates a directory for each of the client computers that you need to run the simulation.</span></span> <span data-ttu-id="558e1-112">Jedes Clientverzeichnis enthält auch ein Skript, mit dem alle Instanzen des lync Server 2013-Stress-und-Leistungstools (LyncPerfTool.exe) gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="558e1-112">Each client directory also comes with a script to start all the instances of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="558e1-113">Die in UserProfileGenerator angegebenen benutzerspezifischen Werte müssen mit den Werten übereinstimmen, die im lync Server 2013-Benutzer Erstellungs Tool (UserProvisioningTool) für den Pool angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="558e1-113">The user-specific values specified in UserProfileGenerator must match the values specified in the Lync Server 2013 User Creation Tool (UserProvisioningTool) for the pool.</span></span>



</div>

<span data-ttu-id="558e1-114">Füllen Sie die Felder auf jeder Registerkarte des lync Server 2013 Load Configuration-Tools aus, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="558e1-114">Fill in the fields on each tab of the Lync Server 2013 Load Configuration Tool, as described in the following sections.</span></span>

<div>

## <a name="common-configuration"></a><span data-ttu-id="558e1-115">Allgemeine Konfiguration</span><span class="sxs-lookup"><span data-stu-id="558e1-115">Common Configuration</span></span>

<span data-ttu-id="558e1-116">Die folgende Abbildung zeigt die Registerkarte " **Allgemeine Konfiguration** " im lync Server 2013 Load Configuration Tool.</span><span class="sxs-lookup"><span data-stu-id="558e1-116">The **Common Configuration** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span> <span data-ttu-id="558e1-117">Füllen Sie die Felder auf der Registerkarte **Allgemeine Konfiguration** aus, wie in den folgenden Schritten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="558e1-117">Fill in the fields of the **Common Configuration** tab, as described in the following steps.</span></span>

<span data-ttu-id="558e1-118">![Registerkarte "Allgemeine Konfiguration"](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "Registerkarte "Allgemeine Konfiguration"")</span><span class="sxs-lookup"><span data-stu-id="558e1-118">![Common Configuration tab.](images/JJ945594.c68dcc8f-10f2-499e-95a2-fccbcc206c2f(OCS.15).jpg "Common Configuration tab.")</span></span>

1.  <span data-ttu-id="558e1-119">Geben Sie unter **Anzahl der verfügbaren** Computer die Anzahl der Computer ein, die Sie zum Ausführen von LyncPerfTool.exe verwenden möchten, oder klicken Sie darauf.</span><span class="sxs-lookup"><span data-stu-id="558e1-119">In **Number of Available Machines**, type or click the number of computers that you want to use to run LyncPerfTool.exe.</span></span> <span data-ttu-id="558e1-120">Wir empfehlen, dass Sie über einen Computer für alle 4.500-Benutzer verfügen, die Sie simulieren werden.</span><span class="sxs-lookup"><span data-stu-id="558e1-120">We recommend that you have one computer for every 4,500 users that you will be simulating.</span></span> <span data-ttu-id="558e1-121">Diese Nummer kann variieren, wenn Sie den Ladebereich verringern oder nur einen Teil der verfügbaren Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="558e1-121">That number may vary if you reduce the load level or if you use only a subset of the available features.</span></span> <span data-ttu-id="558e1-122">(Die Ladestufen werden auf der Registerkarte **Allgemeine Szenarien** eingestellt.)</span><span class="sxs-lookup"><span data-stu-id="558e1-122">(Load levels are set on the **General Scenarios** tab.)</span></span>

2.  <span data-ttu-id="558e1-123">Geben Sie in **Prefix für Benutzernamen** das Präfix für den Benutzernamen der Benutzer ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-123">In **Prefix for User Names**, type the prefix for the user name of the users.</span></span> <span data-ttu-id="558e1-124">Um sich anzumelden, wird der Uniform Resource Identifier (URI) wie folgt angegeben: UserPrefix \[ User Start Index... (Anzahl der Benutzer-1) \] @User Domäne.</span><span class="sxs-lookup"><span data-stu-id="558e1-124">To log in, the Uniform Resource Identifier (URI) will be: UserPrefix\[User Start Index…(Number Of Users-1)\]@User Domain.</span></span>

3.  <span data-ttu-id="558e1-125">Geben Sie unter **Kennwort für alle Benutzer** das Kennwort ein, das zum Erstellen der Benutzer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="558e1-125">In **Password for All Users**, enter the password that was used for creating the users.</span></span> <span data-ttu-id="558e1-126">Wenn Sie dieses Feld leer lassen, wird der Benutzername als Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="558e1-126">If you leave this field empty, the username will be used as the password.</span></span>

4.  <span data-ttu-id="558e1-127">Klicken Sie im **Start Index des Benutzers** auf den Index des ersten Benutzers, den Sie konfigurieren möchten, oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-127">In **User Start Index**, click or type the index of the first user to be configured.</span></span> <span data-ttu-id="558e1-128">Sie können unterschiedliche Bereiche für verschiedene Typen oder lade Ebenen konfigurieren, Sie müssen jedoch UserProfileGenerator.exe einmal pro Bereich ausführen, den Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="558e1-128">You can configure different ranges for different types or levels of load, but you must run UserProfileGenerator.exe once per the range that you want to configure.</span></span>

5.  <span data-ttu-id="558e1-129">Klicken Sie unter **Anzahl der Benutzer** auf die Gesamtzahl der Benutzer, die Sie konfigurieren möchten, oder geben Sie Sie ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-129">In **Number of Users**, click or type the total number of users you are going to configure.</span></span>

6.  <span data-ttu-id="558e1-130">Geben Sie in **Benutzerdomäne** die Domäne ein, die für den SIP-URI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="558e1-130">In **User Domain**, type the domain used for the SIP URI.</span></span> <span data-ttu-id="558e1-131">Diese wird verwendet, um den SIP-URI jedes Benutzers zu erstellen, der sich am lync Server 2013-Front-End-Server oder Standard Edition-Server anmeldet.</span><span class="sxs-lookup"><span data-stu-id="558e1-131">This is used to construct the SIP URI of each user to log on to the Lync Server 2013 Front End Server or Standard Edition server.</span></span> <span data-ttu-id="558e1-132">Sie kann sich von der Kontodomäne unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="558e1-132">It can be different from the account domain.</span></span>

7.  <span data-ttu-id="558e1-133">Geben Sie in **Kontodomäne** die Domänenanmeldung für Active Directory-Domänendienste ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-133">In **Account Domain**, type the Active Directory Domain Services domain logon.</span></span>

8.  <span data-ttu-id="558e1-134">Geben Sie die maximale Anzahl von gleichzeitigen Endpunkten in **Anmeldung pro Sekunde (pro Instanz)** ein, für die Sie das Tool an allen Endpunkten/Benutzern protokollieren möchten.</span><span class="sxs-lookup"><span data-stu-id="558e1-134">Enter the maximum number of concurrent endpoints in **Sign In Per Second (per instance)** for which you want the tool to log in all the endpoints/users.</span></span> <span data-ttu-id="558e1-135">Die empfohlene Gebühr ist \< = 2 pro Sekunde/Standard SKU Fe.</span><span class="sxs-lookup"><span data-stu-id="558e1-135">The recommended rate is \<=2 per second/standard SKU FE.</span></span>

9.  <span data-ttu-id="558e1-136">Geben Sie in **Access-Proxy oder Pool-FQDN** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Servers ein, mit dem die Clients eine Verbindung herstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="558e1-136">In **Access Proxy or Pool FQDN**, type the fully qualified domain name (FQDN) of the server that you want the clients to connect to.</span></span> <span data-ttu-id="558e1-137">Wenn sich die Benutzer extern anmelden, geben Sie den Zugriffsproxy an.</span><span class="sxs-lookup"><span data-stu-id="558e1-137">If the users are logging on externally, specify the access proxy.</span></span> <span data-ttu-id="558e1-138">Wenn die Benutzer intern sind, geben Sie den FQDN Ihres Pools oder Standard Edition-Servers an.</span><span class="sxs-lookup"><span data-stu-id="558e1-138">If the users are internal, specify the FQDN of their pool or Standard Edition server.</span></span>

10. <span data-ttu-id="558e1-139">Klicken oder geben Sie in **Port** den Port ein, den Benutzer für SIP verwenden sollen (der Standardwert ist 5061).</span><span class="sxs-lookup"><span data-stu-id="558e1-139">In **Port**, click or type the port that you want users to use for SIP (the default is 5061).</span></span>

<span data-ttu-id="558e1-140">Geben Sie für externe Netzwerk Server Einstellungen den **Zugriffs Proxy oder den Pool-FQDN** und den **Port** an.</span><span class="sxs-lookup"><span data-stu-id="558e1-140">For External Network Server Settings, specify the **Access Proxy or Pool FQDN** and the **Port**.</span></span> <span data-ttu-id="558e1-141">Diese Einstellungen werden nur für die Auslastungssimulation externer Endpunkte verwendet.</span><span class="sxs-lookup"><span data-stu-id="558e1-141">These settings are used only for External endpoints load simulation.</span></span>

</div>

<div>

## <a name="general-scenarios"></a><span data-ttu-id="558e1-142">Allgemeine Szenarien</span><span class="sxs-lookup"><span data-stu-id="558e1-142">General Scenarios</span></span>

<span data-ttu-id="558e1-143">Die Registerkarte " **Allgemeine Szenarien** " im lync Server 2013 Load Configuration Tool ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="558e1-143">The **General Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="558e1-144">Konfigurieren Sie die Auslastungsstufen und Parameter für die einzelnen allgemeinen Szenarien, die Sie ausführen möchten, oder lassen Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="558e1-144">Configure the load levels and parameters for each of the general scenarios that you want to run, or leave disabled.</span></span>

<span data-ttu-id="558e1-145">![Registerkarte "allgemeine Szenarien"](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "Registerkarte "allgemeine Szenarien"")</span><span class="sxs-lookup"><span data-stu-id="558e1-145">![General Scenarios tab.](images/JJ945594.4f046d39-b532-4baf-99a6-c89d1d6d1fcc(OCS.15).jpg "General Scenarios tab.")</span></span>

1.  <span data-ttu-id="558e1-146">Geben Sie in **Instant Messaging**, das Peer-to-Peer und Konferenzen umfasst, den entsprechenden Wert für die Auslastungsstufe an.</span><span class="sxs-lookup"><span data-stu-id="558e1-146">In **Instant Messaging**, which includes peer-to-peer and conferencing, specify the appropriate value for the Load Level.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="558e1-147">Die Werte für die Auslastungsstufe für alle Felder (mit Ausnahme von Standort Informationsdiensten) sind <STRONG>deaktiviert</STRONG>, <STRONG>gering</STRONG>, <STRONG>Mittel</STRONG>, <STRONG>hoch</STRONG>und <STRONG>Benutzerdefiniert</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="558e1-147">Load level values for all fields (except Location Information Services) are <STRONG>Disabled</STRONG>, <STRONG>Low</STRONG>, <STRONG>Medium</STRONG>, <STRONG>High</STRONG>, and <STRONG>Custom</STRONG>.</span></span> <span data-ttu-id="558e1-148">Wenn "Low", "Mittel", "hoch" oder "Benutzerdefiniert" ausgewählt ist, werden für jede Modalität und jeden Clientkonfigurationen generiert.</span><span class="sxs-lookup"><span data-stu-id="558e1-148">When Low, Medium, High, or Custom is selected, configurations will be generated for each modality and client.</span></span> <span data-ttu-id="558e1-149">"Hoch" führt zu der maximalen unterstützten Last, die für den Server generiert wird, das Medium entspricht 60 Prozent der Last, und "Low" entspricht 30 Prozent der Auslastung.</span><span class="sxs-lookup"><span data-stu-id="558e1-149">High will result in the maximum supported load to be generated for the server, Medium corresponds to 60 percent of the load, and Low corresponds to 30 percent of the load.</span></span>

    
    </div>

2.  <span data-ttu-id="558e1-150">Geben Sie in **Audiokonferenzen**, bei denen es sich nur um Audiokonferenzen handelt, den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-150">In **Audio Conferencing**, which is audio conferencing only, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="558e1-151">Peer-zu-Peer-Anrufe werden im Abschnitt VoIP-Szenarien weiter unten in diesem Thema behandelt.</span><span class="sxs-lookup"><span data-stu-id="558e1-151">Peer-to-peer calls are covered in the Voice Scenarios section later in this topic.</span></span> <span data-ttu-id="558e1-152">Um MultiView zu aktivieren, öffnen Sie die Registerkarte **erweitert** für diese Modalität.</span><span class="sxs-lookup"><span data-stu-id="558e1-152">To enable MultiView, open the **Advanced** tab for that modality.</span></span>

3.  <span data-ttu-id="558e1-153">Geben Sie in **Anwendungsfreigabe** den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-153">In **Application Sharing**, specify the appropriate value for Load Level.</span></span>

4.  <span data-ttu-id="558e1-154">Geben Sie in der **Datenzusammenarbeit**, die Datenkonferenzen umfasst, den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-154">In **Data Collaboration**, which includes data conferencing, specify the appropriate value for Load Level.</span></span>

5.  <span data-ttu-id="558e1-155">Geben Sie in **Expansion der Verteilerliste** den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-155">In **Distribution List Expansion**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="558e1-156">Sie müssen auch auf die Schaltfläche **erweitert** klicken, und füllen Sie dann die Felder mit den gleichen Werten aus, die Sie auf der Registerkarte **Verteilerliste** des lync Server-Benutzer Erstellungstools (UserProvisioningTool.exe) konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="558e1-156">You must also click the **Advanced** button, and then fill in the fields with the same values that you configured on the **Distribution List** tab of the Lync Server User Creation Tool (UserProvisioningTool.exe).</span></span> <span data-ttu-id="558e1-157">Details zu diesen Feldern finden Sie unter [Erstellen von Benutzern und Kontakten](create-users-and-contacts.md) .</span><span class="sxs-lookup"><span data-stu-id="558e1-157">For details about these fields, see [Create Users and Contacts](create-users-and-contacts.md)</span></span>

6.  <span data-ttu-id="558e1-158">Geben Sie in der **Adressbuch-Webabfrage**, bei der es sich um den Adressbuch-Suchdienst (nicht den Adressbuchdatei-Download) handelt, den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-158">In **Address Book Web Query**, which is the address book lookup service (not the address book file download), specify the appropriate value for Load Level.</span></span> <span data-ttu-id="558e1-159">Um Adressbuch Downloads zu aktivieren, klicken Sie auf die entsprechende Schaltfläche **erweitert** , und legen Sie **EnableABSDownload** auf true fest.</span><span class="sxs-lookup"><span data-stu-id="558e1-159">To enable address book downloads, click the corresponding **Advanced** button, and then set **EnableABSDownload** to true.</span></span>

7.  <span data-ttu-id="558e1-160">Geben Sie im **Reaktionsgruppendienst** den entsprechenden Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-160">In **Response Group Service**, specify the appropriate value for Load Level.</span></span> <span data-ttu-id="558e1-161">Sie müssen auch auf die entsprechende Schaltfläche **erweitert** klicken und dann die URIs der Reaktionsgruppen angeben, die Sie bereits beim Bereitstellen von Reaktionsgruppen-Service-Agents erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="558e1-161">You must also click the corresponding **Advanced** button, and then specify the URIs of the response groups you have already created when provisioning Response Group Service agents.</span></span> <span data-ttu-id="558e1-162">Sie müssen mindestens eine Reaktionsgruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="558e1-162">You must specify at least one response group.</span></span> <span data-ttu-id="558e1-163">Verwenden Sie Semikolons, um mehrere Antwortgruppen voneinander zu trennen.</span><span class="sxs-lookup"><span data-stu-id="558e1-163">Use semicolons to separate multiple response groups.</span></span> <span data-ttu-id="558e1-164">Aktualisieren Sie RGSUriSuffixStartIndex und RGSUriSuffixEndIndex auf die tatsächlichen Werte.</span><span class="sxs-lookup"><span data-stu-id="558e1-164">Update RGSUriSuffixStartIndex and RGSUriSuffixEndIndex to the actual values.</span></span>

8.  <span data-ttu-id="558e1-165">Wählen Sie in **Standort Informationsdienste** den geeigneten Wert für Auslastungsgrad aus.</span><span class="sxs-lookup"><span data-stu-id="558e1-165">In **Location Information Services**, select the appropriate value for Load Level.</span></span> <span data-ttu-id="558e1-166">Die Auslastungsstufe für Standort Informationsdienste muss **aktiviert** oder **deaktiviert** sein.</span><span class="sxs-lookup"><span data-stu-id="558e1-166">The load level for Location Information Services must be **Enabled** or **Disabled**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="558e1-167">In jedem der Szenarien befindet sich neben der Schaltfläche " <STRONG>erweitert</STRONG> " und eine Reihe von Kontrollkästchen, die Variationen der Szenarien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="558e1-167">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it, and a set of check boxes that enable variations of the scenarios.</span></span> <span data-ttu-id="558e1-168"><STRONG>Ad-hoc-</STRONG> Mittel zur Simulation von Konferenzen, die während der gesamten Stunde erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="558e1-168"><STRONG>Ad-hoc</STRONG> means to generate simulation of conferences that will be created throughout the hour.</span></span> <span data-ttu-id="558e1-169"><STRONG>Große conf</STRONG> bedeutet, dass große Konferenzszenarien simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="558e1-169"><STRONG>Large Conf</STRONG> means that Large Conference Scenario will be simulated.</span></span> <span data-ttu-id="558e1-170"><STRONG>Externe</STRONG> Mittel, um auch externe Benutzer zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-170"><STRONG>External</STRONG> means to also simulate external users.</span></span><BR><span data-ttu-id="558e1-171">Diese Schaltflächen und Kontrollkästchen ermöglichen den Zugriff auf Werte, die für jedes Szenario spezifisch sind, das das Verhalten des lync Server 2013-Stress-und-Leistungstools (LyncPerfTool) ändert und die Anpassung möglich macht.</span><span class="sxs-lookup"><span data-stu-id="558e1-171">These buttons and check boxes allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and make customization possible.</span></span> <span data-ttu-id="558e1-172">Bei jedem Szenario auf der Registerkarte <STRONG>Allgemeine Szenarien</STRONG> (mit Ausnahme von Standort Informationsdiensten) wird die Konversations Rate mithilfe des entsprechenden Felds im Dialogfeld <STRONG>erweitert</STRONG> berechnet, wenn der Wert der Auslastungsstufe <STRONG>Benutzerdefiniert</STRONG>ist.</span><span class="sxs-lookup"><span data-stu-id="558e1-172">For each scenario on the <STRONG>General Scenarios</STRONG> tab (except for Location Information Services), if the value of Load Level is <STRONG>Custom</STRONG>, then the conversation rate will be calculated using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="558e1-173">Der Feldname unterscheidet sich je nach Szenario, aber die Feld Beschreibung gibt an, "Hinweis: Diese Nummer wird nur verwendet, wenn im Dropdownmenü" Benutzerdefiniert "ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="558e1-173">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span> <span data-ttu-id="558e1-174">Im allgemeinen ändern die Werte " <STRONG>hoch</STRONG>", " <STRONG>Mittel</STRONG>" und " <STRONG>tief</STRONG> " die Konversations Raten pro Modalwert entsprechend dem Benutzermodell, bei dem es sich um ein Gleichgewicht aller Szenarien handelt.</span><span class="sxs-lookup"><span data-stu-id="558e1-174">In general, the values <STRONG>High</STRONG>, <STRONG>Medium</STRONG>, and <STRONG>Low</STRONG> will alter the conversation rates per modality in line with the User Model that is a balance of all the scenarios.</span></span> <span data-ttu-id="558e1-175">Wenn es erforderlich ist, den Auslastungsgrad pro Modalwert aufgrund einer unterschiedlichen erwarteten Nutzung zu ändern, empfehlen wir die Verwendung einer <STRONG>benutzerdefinierten</STRONG> Konversations Gebühr.</span><span class="sxs-lookup"><span data-stu-id="558e1-175">If there is a need to change the load level per modality due to a difference in expected usage, we recommend using a <STRONG>Custom</STRONG> conversation rate.</span></span><BR>



</div>

</div>

<div>

## <a name="voice-scenarios"></a><span data-ttu-id="558e1-176">Sprachszenarien</span><span class="sxs-lookup"><span data-stu-id="558e1-176">Voice Scenarios</span></span>

<span data-ttu-id="558e1-177">Die Registerkarte " **VoIP-Szenarien** " im lync Server 2013 Load Configuration Tool ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="558e1-177">The **Voice Scenarios** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="558e1-178">Verwenden Sie die Registerkarte **VoIP-Szenarien** , um alle sprachbezogenen Szenarien zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-178">Use the **Voice Scenarios** tab to configure all of the voice-related scenarios.</span></span>

<span data-ttu-id="558e1-179">![Registerkarte "Sprachszenarien"](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "Registerkarte "Sprachszenarien"")</span><span class="sxs-lookup"><span data-stu-id="558e1-179">![Voice Scenarios tab.](images/JJ945594.28edf664-da59-40b0-9a0e-196f01e9ca86(OCS.15).jpg "Voice Scenarios tab.")</span></span>

1.  <span data-ttu-id="558e1-180">Klicken Sie in **VoIP** auf die Schaltfläche **erweitert** , und geben Sie dann Werte für die Felder **PhoneAreaCode** und **LocationProfile** (Wählplan) ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-180">In **VoIP**, click the **Advanced** button, and then provide values for the **PhoneAreaCode** and **LocationProfile** (dial plan) fields.</span></span> <span data-ttu-id="558e1-181">Außerdem müssen Sie einen Wert für **Load Level** angeben.</span><span class="sxs-lookup"><span data-stu-id="558e1-181">You must also specify a value for **Load Level**.</span></span> <span data-ttu-id="558e1-182">Wenn Load Level für **VoIP** und **UC/PSTN-Gateway** aktiviert ist, wird immer ein öffentliches Switched Telephone Network (PSTN) zur Unified Communications (UC)-Konfigurationsdatei generiert, die externe Anrufe simuliert.</span><span class="sxs-lookup"><span data-stu-id="558e1-182">If Load Level for **VoIP** and **UC/PSTN Gateway** is Enabled, then a public switched telephone network (PSTN) to unified communications (UC) configuration file will always be generated that will simulate external calls.</span></span>

2.  <span data-ttu-id="558e1-183">Geben Sie in **UC/PSTN-Gateway** einen Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-183">In **UC/PSTN Gateway**, specify a value for Load Level.</span></span> <span data-ttu-id="558e1-184">Wenn Sie eine andere Ladeebene als **deaktiviert** auswählen, müssen Sie einen Wert für die **PSTN-Vorwahl** angeben, indem Sie unter Mediation Server und PSTN auf die Schaltfläche **Hinzufügen** klicken.</span><span class="sxs-lookup"><span data-stu-id="558e1-184">If you select a load level other than **Disabled**, you must supply a value for **PSTN Area Code** by clicking the **Add** button under Mediation Server and PSTN.</span></span> <span data-ttu-id="558e1-185">Stellen Sie sicher, dass für diese Ortsvorwahl eine Route konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="558e1-185">Verify that you have a route configured for that area code.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="558e1-186">Sie können entweder die lync Server-Systemsteuerung oder die lync Server-Verwaltungsshell verwenden, um die Konfiguration der VoIP-Route zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="558e1-186">You can use either the Lync Server Control Panel or the Lync Server Management Shell to verify voice route configuration.</span></span>

    
    </div>

3.  <span data-ttu-id="558e1-187">Geben Sie in **Conferencing Attendant** einen Wert für Load Level an.</span><span class="sxs-lookup"><span data-stu-id="558e1-187">In **Conferencing Attendant**, specify a value for Load Level.</span></span> <span data-ttu-id="558e1-188">Wenn Sie einen Ladebereich (außer **disabled**) auswählen, wird das Feld **Telefonnummer** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="558e1-188">Selecting a load level (other than **Disabled**) will enable the **Telephone Number** field.</span></span> <span data-ttu-id="558e1-189">Geben Sie die Telefonnummer der automatischen Telefonzentrale ein, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="558e1-189">Enter the telephone number of the Auto Attendant that you want to use.</span></span> <span data-ttu-id="558e1-190">Klicken Sie auch auf die Schaltfläche **erweitert** , und geben Sie dann einen Wert für das **LocationProfile** -Feld ein.</span><span class="sxs-lookup"><span data-stu-id="558e1-190">Also, click the **Advanced** button, and then specify a value for the **LocationProfile** field.</span></span>

4.  <span data-ttu-id="558e1-191">Geben Sie im Dienst für das **Parken von Anrufen** den entsprechenden Wert für **Auslastungsgrad** an.</span><span class="sxs-lookup"><span data-stu-id="558e1-191">In **Call Park Service**, specify the appropriate value for **Load Level**.</span></span>

5.  <span data-ttu-id="558e1-192">In **Mediation Server und PSTN** müssen Sie für jeden Vermittlungsserver, den Sie verwenden möchten, über einen separaten PSTN-Simulator verfügen.</span><span class="sxs-lookup"><span data-stu-id="558e1-192">In **Mediation Server and PSTN**, for each Mediation Server that you want to use, you must have a separate PSTN simulator.</span></span> <span data-ttu-id="558e1-193">Nachdem Sie festgestellt haben, welchen Client Sie als Simulator verwenden möchten, müssen Sie Ihren Vermittlungs Server so konfigurieren, dass Anrufe an diesen Computer auf dem von Ihnen konfigurierten PSTN-Simulator-Port weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="558e1-193">After you have determined which client you are going to use as the simulator, you need to configure your Mediation Server to route calls to that computer on the PSTN Simulator port that you configured.</span></span> <span data-ttu-id="558e1-194">Klicken Sie auf **Hinzufügen** , um den Wert für den Vermittlungs Server zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-194">Click **Add** to configure the value for the Mediation Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="558e1-195">In jedem der Szenarien befindet sich daneben eine Schaltfläche " <STRONG>erweitert</STRONG> ".</span><span class="sxs-lookup"><span data-stu-id="558e1-195">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="558e1-196">Diese Schaltflächen ermöglichen den Zugriff auf Werte, die für jedes Szenario spezifisch sind, das das Verhalten des lync Server 2013 Stress and Performance Tool (LyncPerfTool) ändert und die Anpassung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="558e1-196">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="558e1-197">Bei jedem Szenario auf der Registerkarte <STRONG>VoIP-Szenarien</STRONG> , wenn der Wert der <STRONG>Auslastungsstufe</STRONG> <STRONG>Benutzerdefiniert</STRONG>ist, wird die Konversations Rate mithilfe des entsprechenden Felds im Dialogfeld <STRONG>erweitert</STRONG> berechnet.</span><span class="sxs-lookup"><span data-stu-id="558e1-197">For each scenario on the <STRONG>Voice Scenarios</STRONG> tab, if the value of <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the conversation rate will be calculated by using the corresponding field in the <STRONG>Advanced</STRONG> dialog box.</span></span> <span data-ttu-id="558e1-198">Der Feldname unterscheidet sich je nach Szenario, aber die Feld Beschreibung gibt an, "Hinweis: Diese Nummer wird nur verwendet, wenn im Dropdownmenü" Benutzerdefiniert "ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="558e1-198">The field name differs, depending on the scenario, but the field description will state, "NOTE: This number will only be used if Custom is selected from the drop-down menu."</span></span>



</div>

</div>

<div>

## <a name="reach"></a><span data-ttu-id="558e1-199">Erreichen</span><span class="sxs-lookup"><span data-stu-id="558e1-199">Reach</span></span>

<span data-ttu-id="558e1-200">REACH ist eine neue Erfahrung in lync Server 2013, die Konferenzszenarien über den Unified Communications Web API-Server (UCWA) unterstützt, der auf dem Front-End-Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="558e1-200">Reach is a new experience in Lync Server 2013 that supports conferencing scenarios through the Unified Communications Web API (UCWA) server that is installed on the Front-End server.</span></span> <span data-ttu-id="558e1-201">Die Registerkarte " **REACH** " des lync Server 2013 Load Configuration-Tools ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="558e1-201">The **Reach** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="558e1-202">Verwenden Sie die Registerkarte **REACH** , um alle REACH-bezogenen Szenarien zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-202">Use the **Reach** tab to configure all the reach-related scenarios.</span></span>

<span data-ttu-id="558e1-203">![Registerkarte "REACH"](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "Registerkarte "REACH"")</span><span class="sxs-lookup"><span data-stu-id="558e1-203">![Reach tab.](images/JJ945594.65ccf6de-0e8d-47ba-93f3-9dcb39d3fd62(OCS.15).jpg "Reach tab.")</span></span>

1.  <span data-ttu-id="558e1-204">Klicken Sie auf die Schaltfläche **erweitert** neben **Allgemeine Einstellungen für REACH**.</span><span class="sxs-lookup"><span data-stu-id="558e1-204">Click the **Advanced** button next to **General Reach Settings**.</span></span> <span data-ttu-id="558e1-205">Legen Sie das Feld **UcwaTargetServerUrl** auf den Director Pool Virtual IP (VIP) oder den Front-End-Pool VIP.</span><span class="sxs-lookup"><span data-stu-id="558e1-205">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="558e1-206">Wählen Sie in **Anwendungsfreigabe**, **Datenzusammenarbeit** und **Chat** den entsprechenden Wert für **Load Level** aus.</span><span class="sxs-lookup"><span data-stu-id="558e1-206">In **Application Sharing**, **Data Collaboration**, and **IM**, select the appropriate value for **Load Level**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="558e1-207">In jedem der Szenarien befindet sich daneben eine Schaltfläche " <STRONG>erweitert</STRONG> ".</span><span class="sxs-lookup"><span data-stu-id="558e1-207">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="558e1-208">Diese Schaltflächen ermöglichen den Zugriff auf Werte, die für jedes Szenario spezifisch sind, das das Verhalten des lync Server 2013 Stress and Performance Tool (LyncPerfTool) ändert und die Anpassung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="558e1-208">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="558e1-209">Bei jedem der REACH-Szenarien wird, wenn die <STRONG>Auslastungsstufe</STRONG> <STRONG>Benutzerdefiniert</STRONG>ist, der im Feld <STRONG>ConversationsPerHour</STRONG> angegebene Wert anstelle des Standardwerts verwendet.</span><span class="sxs-lookup"><span data-stu-id="558e1-209">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default</span></span>



</div>

<span data-ttu-id="558e1-210">Verwenden Sie die Registerkarte **Mobilität** , um alle mobilitätsbezogenen Szenarien zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-210">Use the **Mobility** tab to configure all of the mobility-related scenarios.</span></span>

<span data-ttu-id="558e1-211">![Reiter Mobilität.](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "Reiter Mobilität.")</span><span class="sxs-lookup"><span data-stu-id="558e1-211">![Mobility tab.](images/JJ945594.4dd8f3e0-921c-48a5-8b23-2a0330d3c334(OCS.15).jpg "Mobility tab.")</span></span>

1.  <span data-ttu-id="558e1-212">Klicken Sie auf die Schaltfläche **erweitert** neben **Mobilität (UCWA)**.</span><span class="sxs-lookup"><span data-stu-id="558e1-212">Click the **Advanced** button next to **Mobility (UCWA)**.</span></span> <span data-ttu-id="558e1-213">Legen Sie das Feld **UcwaTargetServerUrl** auf den Director Pool Virtual IP (VIP) oder den Front-End-Pool VIP.</span><span class="sxs-lookup"><span data-stu-id="558e1-213">Set the field **UcwaTargetServerUrl** to the Director pool virtual IP (VIP) or the Front End pool VIP.</span></span>

2.  <span data-ttu-id="558e1-214">Wählen Sie in **Anwesenheits-und P2P-Instant Messaging \\ -Audio** den entsprechenden Wert für **Load Level** aus, um die Mobilitäts Szenario-Simulation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="558e1-214">In **Presence and P2P Instant Messaging\\Audio**, select the appropriate value for **Load Level** to enable Mobility Scenario simulation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="558e1-215">In jedem der Szenarien befindet sich daneben eine Schaltfläche " <STRONG>erweitert</STRONG> ".</span><span class="sxs-lookup"><span data-stu-id="558e1-215">Each of the scenarios has an <STRONG>Advanced</STRONG> button located next to it.</span></span> <span data-ttu-id="558e1-216">Diese Schaltflächen ermöglichen den Zugriff auf Werte, die für jedes Szenario spezifisch sind, das das Verhalten des lync Server 2013 Stress and Performance Tool (LyncPerfTool) ändert und die Anpassung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="558e1-216">These buttons allow access to values specific to each scenario that will change the behavior of the Lync Server 2013 Stress and Performance Tool (LyncPerfTool) and enable customization.</span></span> <span data-ttu-id="558e1-217">Bei jedem der REACH-Szenarien wird, wenn die <STRONG>Auslastungsstufe</STRONG> <STRONG>Benutzerdefiniert</STRONG>ist, der im Feld <STRONG>ConversationsPerHour</STRONG> angegebene Wert anstelle des Standardwerts verwendet.</span><span class="sxs-lookup"><span data-stu-id="558e1-217">For each of the Reach scenarios, if the <STRONG>Load Level</STRONG> is <STRONG>Custom</STRONG>, then the value specified in the <STRONG>ConversationsPerHour</STRONG> field is used instead of the default.</span></span>



</div>

</div>

<div>

## <a name="summary"></a><span data-ttu-id="558e1-218">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="558e1-218">Summary</span></span>

<span data-ttu-id="558e1-219">Die Registerkarte " **Zusammenfassung** " des lync Server 2013 Load Configuration-Tools ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="558e1-219">The **Summary** tab of the Lync Server 2013 Load Configuration Tool is shown in the following figure.</span></span>

<span data-ttu-id="558e1-220">![Registerkarte "Zusammenfassung"](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "Registerkarte "Zusammenfassung"")</span><span class="sxs-lookup"><span data-stu-id="558e1-220">![Summary tab.](images/JJ945594.c675e869-8ded-4195-8c2a-68d844fc96ad(OCS.15).jpg "Summary tab.")</span></span>

<span data-ttu-id="558e1-221">Die Registerkarte " **Zusammenfassung** " gibt an, welche Benutzer für die einzelnen Szenarien verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="558e1-221">The **Summary** tab indicates which users to use for each of the scenarios.</span></span> <span data-ttu-id="558e1-222">Es ist möglich, Benutzernummern Bereiche manuell zu konfigurieren, indem Sie das Kontrollkästchen Benutzer **definierte Benutzerbereichs Generierung aktivieren** auswählen und dann in der Tabelle mit dem **Benutzerbereich** , den Sie anpassen möchten, auf das Szenario doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="558e1-222">It is possible to manually configure user number ranges by selecting the **Enable Custom User Range Generation** check box, and then double-clicking the scenario in the table that has the **User Range** that you want to customize.</span></span> <span data-ttu-id="558e1-223">Überprüfen (RunClient.bat) beim Starten eine Anmelde Verzögerung hinzufügen, um Verzögerungen in den generierten Batchdateien einzubeziehen, damit Sie dem Anmelde Satz entsprechen.</span><span class="sxs-lookup"><span data-stu-id="558e1-223">Check (RunClient.bat) Add sign-in delay when starting, in order to include delays in the generated batch files to correspond with the sign-in rate.</span></span> <span data-ttu-id="558e1-224">Dies ist nützlich, um eine Serverüberlastung zu verhindern, wenn eine große Anzahl von Benutzern signiert wird.</span><span class="sxs-lookup"><span data-stu-id="558e1-224">This is useful to prevent server overload when signing in a large number of users.</span></span> <span data-ttu-id="558e1-225">Klicken Sie auf **Dateien generieren**, und wählen Sie den Ordner aus, in dem Sie die Konfiguration generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="558e1-225">Click **Generate Files**, and select the folder where you want to generate the configuration.</span></span> <span data-ttu-id="558e1-226">Wenn Ihre Dateien erfolgreich erstellt wurden, wird ein Dialogfeld angezeigt, das der folgenden Abbildung ähnelt.</span><span class="sxs-lookup"><span data-stu-id="558e1-226">A dialog box similar to the following figure will appear when your files have been successfully created.</span></span>

<span data-ttu-id="558e1-227">![Bestätigung, dass Dateien erstellt wurden.](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "Bestätigung, dass Dateien erstellt wurden.")</span><span class="sxs-lookup"><span data-stu-id="558e1-227">![Acknowledgement that files have been created.](images/JJ945594.00dc1e92-bfba-48e7-9568-b97ad864491e(OCS.15).jpg "Acknowledgement that files have been created.")</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="558e1-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="558e1-228">See Also</span></span>


[<span data-ttu-id="558e1-229">Erstellen von Benutzern und Kontakten</span><span class="sxs-lookup"><span data-stu-id="558e1-229">Create Users and Contacts</span></span>](create-users-and-contacts.md)  
</div>
</div>
<span></span>
</div>
</div>
</div>
