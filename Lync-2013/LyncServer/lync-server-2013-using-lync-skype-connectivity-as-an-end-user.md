---
title: 'Lync Server 2013: Verwenden von Lync-Skype-Konnektivität als Endbenutzer'
description: 'Lync Server 2013: Verwenden von Lync-Skype Konnektivität als Endbenutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Lync-Skype connectivity as an end user
ms:assetid: ad22f731-118c-4349-8790-b1a72941cbdd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440175(v=OCS.15)
ms:contentKeyID: 57793365
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd669a5cf0b15f7fb2d411e4456553f5469d9f96
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438918"
---
# <a name="using-lync-skype-connectivity-in-lync-server-2013-as-an-end-user"></a><span data-ttu-id="441b9-103">Verwenden von Lync-Skype-Konnektivität als Endbenutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="441b9-103">Using Lync-Skype connectivity in Lync Server 2013 as an end user</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="441b9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="441b9-104">

<span> </span></span></span>

<span data-ttu-id="441b9-105">_**Letztes Änderungsdatum des Themas:** 2016-12-27_</span><span class="sxs-lookup"><span data-stu-id="441b9-105">_**Topic Last Modified:** 2016-12-27_</span></span>

<span data-ttu-id="441b9-106">Lync-Skype Konnektivität ermöglicht es Skype-Benutzern und lync-Benutzern, sich gegenseitig als Kontakte hinzuzufügen, Sofortnachrichten auszutauschen und Audio-und Videoanrufe zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="441b9-106">Lync-Skype Connectivity enables Skype users and Lync users to add each other as contacts, exchange instant messages and make audio and video calls.</span></span> <span data-ttu-id="441b9-107">Wenn ein Skype-Nutzer einen lync-Nutzer hinzufügt, wird ein Skype-Nutzer einen Kontakt in Skype erstellen, der den SIP-Uniform Resource Identifier (Session Initiation Protocol) des lync-Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="441b9-107">When a Skype user adds a Lync user, a Skype user will create a contact in Skype containing the session initiation protocol (SIP) uniform resource identifier (URI) of the Lync user.</span></span> <span data-ttu-id="441b9-108">Wenn ein lync-Benutzer einen Skype-Kontakt hinzufügt, erstellt der lync-Benutzer umgekehrt einen Kontakt in lync, der das Microsoft-Konto (MSA) des Skype-Benutzers und nicht den Skype-Nutzernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="441b9-108">Conversely, when a Lync user adds a Skype contact, the Lync user will create a contact in Lync that will contain the Microsoft Account (MSA) of the Skype user, and not the Skype user name.</span></span>

<span data-ttu-id="441b9-109">**Was ist ein MSA?**</span><span class="sxs-lookup"><span data-stu-id="441b9-109">**What is an MSA?**</span></span> <span data-ttu-id="441b9-110">Skype-Nutzer müssen sich mit einem Microsoft-Konto (vormals als Windows Live ID bezeichnet) bei Skype anmelden, um mit lync-Kontakten zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="441b9-110">Skype users must sign in to Skype with a Microsoft account (previously called Windows Live ID) in order to communicate with Lync contacts.</span></span> <span data-ttu-id="441b9-111">Ein Microsoft-Konto besteht aus einer Kombination aus einer e-Mail-Adresse und einem Kennwort, mit der Sie sich auch bei Diensten wie Microsoft OneDrive-Speichertechnologie, Windows Phone, Microsoft Xbox Live Online-Spielservice und Microsoft Outlook-Messaging-und Zusammenarbeitsclient (und zuvor Microsoft Hotmail-webbasierter e-Mail-Dienst oder Windows Live Messenger) anmelden können.</span><span class="sxs-lookup"><span data-stu-id="441b9-111">A Microsoft account consists of the combination of an email address and a password, which you can also use to sign in to services such as Microsoft OneDrive storage technology, Windows Phone, Microsoft Xbox LIVE online game service, and Microsoft Outlook messaging and collaboration client (and, previously, Microsoft Hotmail web-based e-mail service or Windows Live Messenger).</span></span> <span data-ttu-id="441b9-112">Wenn Sie eine e-Mail-Adresse und ein Kennwort für die Anmeldung bei diesen oder anderen Diensten verwenden, verfügen Sie bereits über ein Microsoft-Konto.</span><span class="sxs-lookup"><span data-stu-id="441b9-112">If you use an email address and a password to sign in to these or other services, you already have a Microsoft account.</span></span> <span data-ttu-id="441b9-113">Details zum Erstellen eines Microsoft-Kontos finden Sie auf der Anmeldeseite des Microsoft-Kontos unter [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061) .</span><span class="sxs-lookup"><span data-stu-id="441b9-113">For details about creating a Microsoft Account, see the Microsoft account sign-up page at [https://go.microsoft.com/fwlink/p/?LinkId=306061](https://go.microsoft.com/fwlink/p/?linkid=306061).</span></span> <span data-ttu-id="441b9-114">Sie können Ihr vorhandenes Skype-Konto mit Ihrem Microsoft-Konto für einmaliges Anmelden in einer Vielzahl von Anwendungen und Diensten zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="441b9-114">You can merge your existing Skype account with your Microsoft account for single sign-on, across a variety of applications and services.</span></span> <span data-ttu-id="441b9-115">Nachdem das Konto zusammengeführt wurde, kann ein Skype-Nutzer eine Kontakt Anfrage an lync-Nutzer senden.</span><span class="sxs-lookup"><span data-stu-id="441b9-115">Once the account is merged a Skype user can send a contact request to Lync users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="441b9-116">Damit lync-und Skype-Benutzer vollständig miteinander kommunizieren können, müssen die folgenden Voraussetzungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="441b9-116">In order for Lync and Skype users to fully communicate with each other, the following requirements must be met:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="441b9-117">Skype-Nutzer müssen bei Ihrem Skype-Client mit einem Microsoft-Konto (MSA) angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="441b9-117">Skype users must be logged into their Skype client with a Microsoft Account (MSA).</span></span></P>
> <LI>
> <P><span data-ttu-id="441b9-118">Lync-Benutzer müssen für die Verbindung mit öffentlichen Chat Diensten durch ihren lync-Administrator aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="441b9-118">Lync users must be enabled for public IM connectivity by their Lync administrator.</span></span></P>
> <LI>
> <P><span data-ttu-id="441b9-119">Wenn ein Skype-Nutzer einen lync-Kontakt hinzufügt, stellen Sie sicher, dass das Wort lync unter dem Namen des Kontakts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="441b9-119">When a Skype user adds a Lync contact, verify that the word Lync appears below the contact’s name.</span></span> <span data-ttu-id="441b9-120">Dies zeigt an, dass ein lync-URI gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="441b9-120">This indicates that a Lync URI has been found.</span></span></P>
> <LI>
> <P><span data-ttu-id="441b9-121">Wenn ein Skype-Benutzer einen lync-Kontakt hinzufügt und für diese lync-Domäne keine Suchergebnisse zurückgegeben werden, ist der PIC-Bereitstellungsprozess möglicherweise nicht abgeschlossen, oder die lync-Domäne wurde noch nicht eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="441b9-121">When a Skype user adds a Lync contact and zero search results are returned for that Lync domain, the PIC provisioning process may not have completed, or the Lync domain has not yet been set up.</span></span></P>
> <LI>
> <P><span data-ttu-id="441b9-122">Je nach den Privatsphäre-Einstellungen der lync-und Skype-Nutzer funktionieren Chat, Video und Anwesenheitsinformationen möglicherweise erst, wenn die neuen Kontakte von jedem Benutzer akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="441b9-122">Depending on the privacy settings of the Lync and Skype users, IM, video, and presence may not work until the new contacts are accepted by each user.</span></span></P></LI></UL>



</div>

<span data-ttu-id="441b9-123">**So fügen Sie einen Skype-Kontakt zu lync 2013 hinzu**</span><span class="sxs-lookup"><span data-stu-id="441b9-123">**To add a Skype contact to Lync 2013**</span></span>

1.  <span data-ttu-id="441b9-124">Klicken Sie in lync auf **Kontakt hinzufügen, einen Kontakt hinzufügen, der sich nicht in meiner Organisation** befindet.</span><span class="sxs-lookup"><span data-stu-id="441b9-124">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="441b9-125">Wählen Sie in der Liste der verfügbaren Kontakt Anbieter **Skype** aus.</span><span class="sxs-lookup"><span data-stu-id="441b9-125">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="441b9-126">Geben Sie im Feld **Chat Adresse** das Microsoft-Konto (MSA) des Skype-Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="441b9-126">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user.</span></span>

4.  <span data-ttu-id="441b9-127">Wählen Sie im Dropdownfeld **zur Kontaktgruppe hinzufügen** eine Kontaktgruppe aus, der Sie den Benutzer hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="441b9-127">In the **Add to contact group** dropdown box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="441b9-128">Wählen Sie im Dropdownfeld **private Beziehung festlegen** die entsprechende Kontakteinstellung aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="441b9-128">In the **Set privacy relationship** dropdown box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="441b9-129">Der Benutzer wird nun in lync als Kontakt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="441b9-129">The user will now appear as a contact in Lync.</span></span> <span data-ttu-id="441b9-130">Wählen Sie den Benutzer aus, klicken Sie mit der rechten Maustaste auf den Benutzernamen, und klicken Sie auf **Visitenkarte** anzeigen, um die Benutzereigenschaften anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="441b9-130">Select the user, right-click the user name, and click **See Contact Card** to view the user properties.</span></span> <span data-ttu-id="441b9-131">Sie können jetzt mit dem neu hinzugefügten Skype-Nutzer einen Audio-oder Videoanruf einrichten.</span><span class="sxs-lookup"><span data-stu-id="441b9-131">You can now establish an audio or video call with the newly added Skype user.</span></span>

<span data-ttu-id="441b9-132">Weitere Informationen zur Unterstützung von Kontakten finden Sie unter [Hinzufügen eines Kontakts in lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span><span class="sxs-lookup"><span data-stu-id="441b9-132">For additional information on support for contacts, see [Add a contact in Lync](https://support.office.com/article/add-a-contact-ae55b88d-b9af-48da-bffe-7cc720a5059a).</span></span>

<span data-ttu-id="441b9-133">Wenn das Microsoft-Konto eines Skype-Benutzers einen benutzerdefinierten Domänennamen wie <strong>Bob@contoso.com</strong> verwendet, kann ein lync-Benutzer dieses Microsoft-Konto auf zwei Arten zu lync hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="441b9-133">When a Skype user’s Microsoft account uses a custom domain name, such as <strong>bob@contoso.com</strong> , a Lync user can add that Microsoft account to Lync in two ways:</span></span>

1.  <span data-ttu-id="441b9-134">Verwenden Sie das Symbol " **Kontakt hinzufügen** " oder</span><span class="sxs-lookup"><span data-stu-id="441b9-134">Use the **Add a Contact** icon, or</span></span>

2.  <span data-ttu-id="441b9-135">Verwenden Sie das Feld **jemanden suchen oder ein Zimmer oder ein Nummernfeld wählen** .</span><span class="sxs-lookup"><span data-stu-id="441b9-135">Use the **Find someone or a room, or a dial a number** field.</span></span>

<span data-ttu-id="441b9-136">In jedem Fall muss der lync-Benutzer die e-Mail-Adresse des Skype-Benutzers im folgenden Format eingeben: <strong>Benutzer (Domänenname) @MSN. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="441b9-136">In each instance, the Lync user must enter the Skype user’s email in the following format: <strong>user(domain name)@msn.com</strong> .</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="441b9-137">Dieser Schritt ist für Microsoft-Konten, die die folgenden Domänennamen verwenden, nicht erforderlich: <STRONG>@Live. com, @hotmail. com oder @Outlook. com</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="441b9-137">This step is not required for Microsoft accounts that use the following domain names: <STRONG>@live.com, @hotmail.com or @outlook.com</STRONG>.</span></span> <span data-ttu-id="441b9-138">Weitere Informationen zu unterstützten benutzerdefinierten Domänennamen finden Sie unter <A href="https://support.microsoft.com/kb/897567">Unterstützte öffentliche Chat-Domänen</A>.</span><span class="sxs-lookup"><span data-stu-id="441b9-138">For more information on supported custom domain names, see <A href="https://support.microsoft.com/kb/897567">Supported public IM domains</A>.</span></span>



</div>

<span data-ttu-id="441b9-139">**So fügen Sie einen Skype-Kontakt zu lync hinzu, wenn Sie einen benutzerdefinierten Domänennamen verwenden**</span><span class="sxs-lookup"><span data-stu-id="441b9-139">**To add a Skype contact to Lync when using a custom domain name**</span></span>

1.  <span data-ttu-id="441b9-140">Klicken Sie in lync auf **Kontakt hinzufügen, einen Kontakt hinzufügen, der sich nicht in meiner Organisation** befindet.</span><span class="sxs-lookup"><span data-stu-id="441b9-140">From Lync, click **Add a Contact, Add a Contact Not in My Organization**.</span></span>

2.  <span data-ttu-id="441b9-141">Wählen Sie in der Liste der verfügbaren Kontakt Anbieter **Skype** aus.</span><span class="sxs-lookup"><span data-stu-id="441b9-141">From the list of available contact providers, select **Skype**.</span></span>

3.  <span data-ttu-id="441b9-142">Geben Sie im Feld **Chat Adresse** das Microsoft-Konto (MSA) des Skype-Benutzers im Format <strong>User (Domain Name) @MSN. com</strong>ein.</span><span class="sxs-lookup"><span data-stu-id="441b9-142">In the **IM Address** field, enter the Microsoft Account (MSA) of the Skype user in the format <strong>user(domain name)@msn.com</strong>.</span></span> <span data-ttu-id="441b9-143">Für Benutzer Bob@contoso.com wäre der Eintrag also <strong> Bob (contoso. com) @MSN. com <strong> .</span><span class="sxs-lookup"><span data-stu-id="441b9-143">So for user bob@contoso.com, the entry would be <strong>bob(contoso.com)@msn.com<strong> .</span></span>

4.  <span data-ttu-id="441b9-144">Wählen Sie im Dropdown-Listenfeld **zu Kontaktgruppe hinzufügen** eine Kontaktgruppe aus, der Sie den Benutzer hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="441b9-144">In the **Add to contact group** drop-down list box, select a contact group to add the user to.</span></span>

5.  <span data-ttu-id="441b9-145">Wählen Sie im Dropdown-Listenfeld **private Beziehung festlegen** die entsprechende Kontakteinstellung aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="441b9-145">In the **Set privacy relationship** drop-down list box, select the appropriate contact setting and then click **OK**.</span></span>

6.  <span data-ttu-id="441b9-146">Ein lync-Benutzer kann auch das Feld **jemanden suchen oder einen Chatroom verwenden oder ein Nummern** Feld in lync wählen und eine Adresse hinzufügen, die dem folgenden <strong>Benutzer ähnelt (Domänenname) @MSN. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="441b9-146">A Lync user can also use the **Find someone or a room, or dial a number** field in Lync, and add an address that resembles the following <strong>user(domain name)@msn.com</strong> .</span></span> <span data-ttu-id="441b9-147">Für das Bob@contoso.com-Microsoft-Konto wäre der Eintrag also <strong>Bob (contoso. com) @MSN. com</strong> .</span><span class="sxs-lookup"><span data-stu-id="441b9-147">So for the bob@contoso.com Microsoft account, the entry would be <strong>bob(contoso.com)@msn.com</strong> .</span></span>

7.  <span data-ttu-id="441b9-148">Führen Sie die Schritte 4 und 5 weiter oben in diesem Verfahren aus, um den Kontakt einer Kontaktgruppe hinzuzufügen und die entsprechende Datenschutz Beziehung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="441b9-148">Follow steps 4 and 5 earlier in this procedure to add the contact to a contact group and to select the appropriate privacy relationship.</span></span>

<span data-ttu-id="441b9-149">**So fügen Sie einen lync-Kontakt zu Skype hinzu**</span><span class="sxs-lookup"><span data-stu-id="441b9-149">**To add a Lync contact to Skype**</span></span>

1.  <span data-ttu-id="441b9-150">Bei Skype anmelden.</span><span class="sxs-lookup"><span data-stu-id="441b9-150">Sign in to Skype.</span></span> <span data-ttu-id="441b9-151">Der Skype-Nutzer muss bei seinem Skype-Client mit einem Microsoft-Konto (MSA) angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="441b9-151">The Skype user must be logged into their Skype client with a Microsoft Account (MSA).</span></span>

2.  <span data-ttu-id="441b9-152">Wählen Sie das Symbol "Kontakte hinzufügen" aus.</span><span class="sxs-lookup"><span data-stu-id="441b9-152">Select the Add Contacts icon.</span></span>

3.  <span data-ttu-id="441b9-153">Geben Sie den SIP-URI des lync-Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="441b9-153">Enter the SIP URI of the Lync user.</span></span> <span data-ttu-id="441b9-154">Beispiel: Bob@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="441b9-154">For example, bob@contoso.com.</span></span>

4.  <span data-ttu-id="441b9-155">Wenn Skype die Übereinstimmung in den Suchergebnissen findet, suchen Sie nach dem Wort **lync** unter dem Namen des lync-Benutzers.</span><span class="sxs-lookup"><span data-stu-id="441b9-155">When Skype finds the match in the search results, look for the word **Lync** below the Lync user’s name.</span></span> <span data-ttu-id="441b9-156">Dies zeigt an, dass Skype den SIP-URI des lync-Clients erfolgreich gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="441b9-156">This indicates Skype successfully located the Lync client’s SIP URI.</span></span> <span data-ttu-id="441b9-157">Klicken Sie auf den Namen.</span><span class="sxs-lookup"><span data-stu-id="441b9-157">Click the name.</span></span>

5.  <span data-ttu-id="441b9-158">Klicken Sie in der oberen rechten Ecke des Fensters auf zu Kontakten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="441b9-158">In the top right corner of the window, click Add to Contacts.</span></span>

6.  <span data-ttu-id="441b9-159">Der neue Kontakt wird nun Ihrer Kontaktliste hinzugefügt, aber anstelle des Statussymbols wird ein Fragezeichen angezeigt, bis Sie Ihre Anfrage angenommen haben.</span><span class="sxs-lookup"><span data-stu-id="441b9-159">The new contact is now added to your contact list, but you’ll see a question mark instead of their status icon until they accept your request.</span></span> <span data-ttu-id="441b9-160">Wenn Ihr neuer Kontakt Ihre Anfrage akzeptiert, können Sie sehen, wann Sie online sind, Chat Unterhaltungen initiieren und Audio-und Videoanrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="441b9-160">When your new contact accepts your request, you will be able to see when they are online, initiate IM conversations, and make audio and video calls.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="441b9-161">Der lync Server-Administrator muss die Richtlinieneinstellungen des lync-Benutzers so konfigurieren, dass eingehende Anforderungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="441b9-161">The Lync Server administrator must configure the Lync user’s policy settings to allow incoming requests.</span></span> <span data-ttu-id="441b9-162">Wenn dies nicht der Fall ist, erhält der lync-Nutzer keine Kontaktanfragen vom Skype-Nutzer.</span><span class="sxs-lookup"><span data-stu-id="441b9-162">If not, the Lync user will not receive contact requests from the Skype user.</span></span> <span data-ttu-id="441b9-163">Je nach Konfiguration der Richtlinieneinstellungen des lync-Benutzers wird die Anforderung zum Hinzufügen des Skype-Benutzers auf der <STRONG>neuen</STRONG> Registerkarte des lync-Clients angezeigt. Um mit dem Skype-Nutzer kommunizieren zu können, muss der lync-Nutzer den Skype-Nutzer entweder der Favoritenliste oder einer Kontaktliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="441b9-163">Depending on the configuration of the Lync user’s policy settings, the request to add the Skype user will appear on the Lync client’s <STRONG>New</STRONG> tab. To begin communicating with the Skype user, the Lync user must add the Skype user to either the Favorites list or a contact list.</span></span> <span data-ttu-id="441b9-164">Die folgende Abbildung zeigt die Position der <STRONG>neuen</STRONG> Registerkarte im lync-Client.</span><span class="sxs-lookup"><span data-stu-id="441b9-164">The image below shows the location of the <STRONG>New</STRONG> tab in the Lync client.</span></span>

    
    </div>

<span data-ttu-id="441b9-165">Ein lync-Benutzer muss lync-Benachrichtigungen konfigurieren, um sicherzustellen, dass von einem Skype-Benutzer gesendete Anforderungen angezeigt werden und vom lync-Benutzer erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="441b9-165">A Lync user must configure Lync alerts to ensure that requests sent from a Skype user appear and are discoverable by the Lync user.</span></span> <span data-ttu-id="441b9-166">Führen Sie die folgenden Schritte aus, um lync-Benachrichtigungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="441b9-166">To configure Lync alerts, complete the procedure that follows.</span></span>

<span data-ttu-id="441b9-167">**So konfigurieren Sie lync-Benachrichtigungen**</span><span class="sxs-lookup"><span data-stu-id="441b9-167">**To configure Lync Alerts**</span></span>

1.  <span data-ttu-id="441b9-168">Klicken Sie im lync-Client auf das Symbol **Optionen** .</span><span class="sxs-lookup"><span data-stu-id="441b9-168">From the Lync client, click the **Options** icon.</span></span>

2.  <span data-ttu-id="441b9-169">Wählen Sie **Benachrichtigungen** aus.</span><span class="sxs-lookup"><span data-stu-id="441b9-169">Select **Alerts**.</span></span>

3.  <span data-ttu-id="441b9-170">Aktivieren Sie unter **Allgemeine Benachrichtigungen** das Kontrollkästchen **Wenn jemand mich zu seiner Kontaktliste hinzufügt**.</span><span class="sxs-lookup"><span data-stu-id="441b9-170">Under **General alerts**, check **Tell me when someone adds me to his or her contact list**.</span></span>

4.  <span data-ttu-id="441b9-171">Wählen Sie unter Kontakte, die **lync nicht verwenden** **die Option Einladungen zulassen, aber alle anderen Kommunikationen blockieren** aus.</span><span class="sxs-lookup"><span data-stu-id="441b9-171">Under **Contacts not using Lync**, select **Allow invites but block all other communications**.</span></span>

5.  <span data-ttu-id="441b9-172">Klicken Sie auf **OK** , um das Fenster Optionen zu schließen.</span><span class="sxs-lookup"><span data-stu-id="441b9-172">Click **OK** to close the Options window.</span></span>

<span data-ttu-id="441b9-173"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="441b9-173"></div>

<span> </span>

</div>

</div>

</span></span></div>

