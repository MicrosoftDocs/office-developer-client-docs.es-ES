---
title: EnviarCorreoElectrónico (acción de macro)
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314654"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="26881-102">EnviarCorreoElectrónico (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="26881-102">SendEmail macro action</span></span>

<span data-ttu-id="26881-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26881-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26881-104">La acción **sendEmail** envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="26881-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="26881-105">La acción **EnviarCorreoElectrónico** solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="26881-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="26881-106">Configuración</span><span class="sxs-lookup"><span data-stu-id="26881-106">Setting</span></span>

<span data-ttu-id="26881-107">La acción **EnviarCorreoElectrónico** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="26881-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26881-108">Argument</span><span class="sxs-lookup"><span data-stu-id="26881-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="26881-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="26881-109">Required</span></span></p></th>
<th><p><span data-ttu-id="26881-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="26881-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26881-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="26881-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="26881-112">Sí</span><span class="sxs-lookup"><span data-stu-id="26881-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="26881-113">Destinatarios del mensaje cuyos nombres desea poner en la línea <strong>para</strong> del mensaje. Separe los nombres de los destinatarios que especifique en este argumento (y en los argumentos <em>CC</em> y <em>BCC</em> ) con un punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="26881-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26881-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="26881-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="26881-115">No</span><span class="sxs-lookup"><span data-stu-id="26881-115">No</span></span></p></td>
<td><p><span data-ttu-id="26881-116">Destinatarios del mensaje cuyos nombres desee indicar en la línea CC (&quot;copia&quot;carbón) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="26881-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26881-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="26881-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="26881-118">No</span><span class="sxs-lookup"><span data-stu-id="26881-118">No</span></span></p></td>
<td><p><span data-ttu-id="26881-119">Destinatarios del mensaje cuyos nombres desee indicar en la línea CCO (&quot;copia&quot;carbón oculta) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="26881-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26881-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="26881-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="26881-121">No</span><span class="sxs-lookup"><span data-stu-id="26881-121">No</span></span></p></td>
<td><p><span data-ttu-id="26881-p101">Asunto del mensaje. Este texto aparece en la línea <strong>Asunto</strong> del mensaje.</span><span class="sxs-lookup"><span data-stu-id="26881-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26881-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="26881-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="26881-125">No</span><span class="sxs-lookup"><span data-stu-id="26881-125">No</span></span></p></td>
<td><p><span data-ttu-id="26881-p102">El texto que desea incluir en el cuerpo principal del mensaje de correo. Si deja en blanco este argumento, no se incluirá ningún texto adicional en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="26881-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="26881-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26881-128">Remarks</span></span>

<span data-ttu-id="26881-129">La acción **EnviarCorreoElectrónico** solo está disponible en los eventos de macro **[Después de eliminar](after-delete-macro-event.md)**, **[Después de insertar](after-insert-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="26881-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="26881-130">La acción **EnviarCorreoElectrónico** no muestra el mensaje para su edición.</span><span class="sxs-lookup"><span data-stu-id="26881-130">The **SendEmail** action does not display the message for editing.</span></span>

