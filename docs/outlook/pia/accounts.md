---
title: Cuentas
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: eb7c56a8a261f36628c3b440c1aeec31c7aec46e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406823"
---
# <a name="accounts"></a><span data-ttu-id="e5e5e-102">Cuentas</span><span class="sxs-lookup"><span data-stu-id="e5e5e-102">Accounts</span></span> 

<span data-ttu-id="e5e5e-103">En esta sección se proporcionan tareas de ejemplo relacionadas con las cuentas de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="e5e5e-103">This section provides sample tasks that involve group sharing.</span></span> <span data-ttu-id="e5e5e-104">Las cuentas de correo electrónico pueden ser, por ejemplo, cuentas de Microsoft Exchange Server, Protocolo de oficina de correo 3 (POP3), Protocolo de acceso a mensajes de Internet (IMAP) y Protocolo de transferencia de hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="e5e5e-104">This section provides sample tasks that involve e-mail accounts. Examples of e-mail accounts are Microsoft Exchange Server, Post Office Protocol 3 (POP3), Internet Message Access Protocol (IMAP), and Hypertext Transfer Protocol (HTTP) accounts. An account for the current profile is represented by an T:Microsoft.Office.Interop.Outlook.Account object.</span></span> <span data-ttu-id="e5e5e-105">Una cuenta del perfil actual se representa con un objeto [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="e5e5e-105">An account for the current profile is represented by an [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia) object.</span></span>


|<span data-ttu-id="e5e5e-106">Tema</span><span class="sxs-lookup"><span data-stu-id="e5e5e-106">Topic</span></span>|<span data-ttu-id="e5e5e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e5e-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="e5e5e-108">Obtener información de la cuenta</span><span class="sxs-lookup"><span data-stu-id="e5e5e-108">Get account information</span></span>](how-to-get-account-information.md) | <span data-ttu-id="e5e5e-109">Toma como argumento de entrada un objeto [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) de Microsoft Outlook de confianza y usa el objeto **Account** para mostrar los detalles de cada cuenta que está disponible para el perfil actual de Outlook.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-109">Takes as an input argument a trusted Microsoft Outlook [T:Microsoft.Office.Interop.Outlook.Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>|
|[<span data-ttu-id="e5e5e-110">Crear un elemento que puede enviarse para una cuenta específica basándose en la carpeta actual</span><span class="sxs-lookup"><span data-stu-id="e5e5e-110">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | <span data-ttu-id="e5e5e-111">Contiene dos ejemplos de código que muestran cómo crear un elemento de correo electrónico que se pueda enviar y una convocatoria de reunión y, a continuación, enviarlos usando una cuenta específica basada en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-111">Contains two code examples that show how to create a sendable e-mail item and meeting request, and then to send them by using a specific account that is based on the current folder.</span></span>|
|[<span data-ttu-id="e5e5e-112">Obtener la cuenta de una carpeta</span><span class="sxs-lookup"><span data-stu-id="e5e5e-112">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md) | <span data-ttu-id="e5e5e-113">Obtiene la cuenta que está asociada a una carpeta en la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-113">Gets the account that is associated with a folder in the current session.</span></span>|
|[<span data-ttu-id="e5e5e-114">Obtener información de varias cuentas</span><span class="sxs-lookup"><span data-stu-id="e5e5e-114">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md) | <span data-ttu-id="e5e5e-115">Obtiene y muestra información diversa sobre cada cuenta del perfil actual.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-115">Obtains and displays miscellaneous information about each account in the current profile.</span></span>|
|[<span data-ttu-id="e5e5e-116">Enviar un elemento de correo con una cuenta de Hotmail</span><span class="sxs-lookup"><span data-stu-id="e5e5e-116">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | <span data-ttu-id="e5e5e-117">Usa la propiedad [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) para enviar un elemento de correo mediante una cuenta de Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-117">Uses the [P:Microsoft.Office.Interop.Outlook._MailItem.SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) property to send a mail item by using a Windows Live Hotmail account.</span></span>|

## <a name="see-also"></a><span data-ttu-id="e5e5e-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5e5e-118">See also</span></span>

- [<span data-ttu-id="e5e5e-119">Usuarios de Exchange</span><span class="sxs-lookup"><span data-stu-id="e5e5e-119">exchange users</span></span>](exchange-users.md)
- [<span data-ttu-id="e5e5e-120">Correo</span><span class="sxs-lookup"><span data-stu-id="e5e5e-120">Mail</span></span>](mail.md)
- [<span data-ttu-id="e5e5e-121">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="e5e5e-121">Recipients</span></span>](recipients.md)
- [<span data-ttu-id="e5e5e-122">¿Cómo se puede... (Referencia a PIA de Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="e5e5e-122">How do I... (Outlook 2013 PIA reference)</span></span>](how-do-i-outlook-2013-pia-reference.md)

