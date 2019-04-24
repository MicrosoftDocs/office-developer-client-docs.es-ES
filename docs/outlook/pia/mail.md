---
title: Correo
TOCTitle: Mail
ms:assetid: 7eddd53c-a598-4dc1-b555-fd3af1236402
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184619(v=office.15)
ms:contentKeyID: 55119864
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 871acb6d9b3905653a382e6548d74f0105d5a186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303426"
---
# <a name="mail"></a><span data-ttu-id="ddca9-102">Correo</span><span class="sxs-lookup"><span data-stu-id="ddca9-102">Mail</span></span>

<span data-ttu-id="ddca9-p101">Esta sección proporciona tareas de ejemplo que implican elementos de correo. Un elemento de correo representa un mensaje de correo en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ddca9-p101">This section provides sample tasks that involve mail items. A mail item represents a mail message in a folder.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ddca9-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ddca9-105">In this section</span></span>

|<span data-ttu-id="ddca9-106">Tema</span><span class="sxs-lookup"><span data-stu-id="ddca9-106">Topic</span></span>|<span data-ttu-id="ddca9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddca9-107">Description</span></span>|
|:----|:----------|
|[<span data-ttu-id="ddca9-108">Crear un elemento de correo con una plantilla de mensaje</span><span class="sxs-lookup"><span data-stu-id="ddca9-108">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)  |<span data-ttu-id="ddca9-109">Crea un elemento de correo mediante el método [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ddca9-109">Creates a mail item by using the [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)) method.</span></span>|
|<span data-ttu-id="ddca9-110">[Create a mail item, attach a report, and send the mail item to the user's manager](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md) (Crear un elemento de correo, adjuntar un informe y enviar el elemento de correo al jefe del usuario)</span><span class="sxs-lookup"><span data-stu-id="ddca9-110">[Create a mail item, attach a report, and send the mail item to the user's manager](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)</span></span>  |<span data-ttu-id="ddca9-111">Crea un elemento de correo que tiene datos adjuntos y se lo envía al administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="ddca9-111">Creates a mail item that has an attachment, and then sends the mail item to the user's manager.</span></span>|
|<span data-ttu-id="ddca9-112">[Send an email given the SMTP address of an account](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md) (Enviar un correo electrónico según la dirección SMTP de una cuenta)</span><span class="sxs-lookup"><span data-stu-id="ddca9-112">[Send an email given the SMTP address of an account](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)</span></span> |<span data-ttu-id="ddca9-113">Crea un mensaje de correo electrónico y lo envía desde una cuenta de Microsoft Outlook, dada la dirección de Protocolo simple de transferencia de correo (SMTP) de esa cuenta. </span><span class="sxs-lookup"><span data-stu-id="ddca9-113">Creates an email and sends it from a Microsoft Outlook account, given the Simple Mail Transfer Protocol (SMTP) address of that account.</span></span>|
|[<span data-ttu-id="ddca9-114">Agregar opciones de votación a un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="ddca9-114">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md) |<span data-ttu-id="ddca9-115">Usa la propiedad [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) del objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) para agregar opciones de votación a un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ddca9-115">Uses the [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an email message.</span></span>|
|<span data-ttu-id="ddca9-116">[Add a custom action as a response to a mail item](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md) (Agregar una acción personalizada como respuesta a un elemento de correo)</span><span class="sxs-lookup"><span data-stu-id="ddca9-116">[Add a custom action as a response to a mail item](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)</span></span>  |<span data-ttu-id="ddca9-117">Agrega acciones personalizadas como respuesta a un elemento de correo electrónico mediante el método [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) de la colección [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ddca9-117">Adds custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>|
|<span data-ttu-id="ddca9-118">[Get the SMTP address of the sender of a mail item](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md) (Obtener la dirección SMTP del remitente de un elemento de correo)</span><span class="sxs-lookup"><span data-stu-id="ddca9-118">[Get the SMTP address of the sender of a mail item](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)</span></span>  |<span data-ttu-id="ddca9-119">Obtiene la dirección del Protocolo simple de transferencia de correo (SMTP) de un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="ddca9-119">Gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>|
|[<span data-ttu-id="ddca9-120">Especificar diferentes tipos de destinatarios de un elemento de correo</span><span class="sxs-lookup"><span data-stu-id="ddca9-120">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md) |<span data-ttu-id="ddca9-121">Establece mediante programación diferentes tipos de destinatarios (Para, CC o CCO) para un elemento de correo.</span><span class="sxs-lookup"><span data-stu-id="ddca9-121">Programmatically sets different recipient types (To, Cc, or Bcc) for a mail item.</span></span>|

## <a name="see-also"></a><span data-ttu-id="ddca9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddca9-122">See also</span></span>

- <span data-ttu-id="ddca9-123">[Accounts](accounts.md) (Cuentas)</span><span class="sxs-lookup"><span data-stu-id="ddca9-123">[Accounts](accounts.md)</span></span>
- <span data-ttu-id="ddca9-124">[Attachments](attachments.md) (Archivos adjuntos)</span><span class="sxs-lookup"><span data-stu-id="ddca9-124">[Attachments](attachments.md)</span></span>
- <span data-ttu-id="ddca9-125">[Folders](folders.md) (Carpetas)</span><span class="sxs-lookup"><span data-stu-id="ddca9-125">[Folders](folders.md)</span></span>
- [<span data-ttu-id="ddca9-126">Destinatarios</span><span class="sxs-lookup"><span data-stu-id="ddca9-126">Recipients</span></span>](recipients.md)
- <span data-ttu-id="ddca9-127">[How do I... (Outlook 2013 PIA reference)](how-do-i-outlook-2013-pia-reference.md) (¿Cómo se puede... [Referencia a PIA de Outlook 2013])</span><span class="sxs-lookup"><span data-stu-id="ddca9-127">[How do I... (Outlook 2013 PIA reference)](how-do-i-outlook-2013-pia-reference.md)</span></span>

