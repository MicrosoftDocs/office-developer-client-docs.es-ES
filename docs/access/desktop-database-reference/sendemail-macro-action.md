---
title: EnviarCorreoElectrónico (acción de macro)
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb2624a00ed2fdbe4a2b24a1f052e19217a4c1a9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871944"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="797a1-102">EnviarCorreoElectrónico (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="797a1-102">SendEmail Macro Action</span></span>


<span data-ttu-id="797a1-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="797a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="797a1-104">La acción **EnviarCorreoElectrónico** envía un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="797a1-104">The **SendEmail** action sends an e-mail message.</span></span>


> [!NOTE]
> <P><span data-ttu-id="797a1-105">[!NOTA] La acción <STRONG>EnviarCorreoElectrónico</STRONG> solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="797a1-105">The <STRONG>SendEmail</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="797a1-106">Valores</span><span class="sxs-lookup"><span data-stu-id="797a1-106">Setting</span></span>

<span data-ttu-id="797a1-107">La acción **EnviarCorreoElectrónico** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="797a1-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="797a1-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="797a1-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="797a1-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="797a1-109">Required</span></span></p></th>
<th><p><span data-ttu-id="797a1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="797a1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="797a1-111"><strong>To</strong></span><span class="sxs-lookup"><span data-stu-id="797a1-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="797a1-112">Sí</span><span class="sxs-lookup"><span data-stu-id="797a1-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="797a1-113">Los destinatarios del mensaje cuyos nombres desee indicar en la línea <strong>para</strong> del mensaje. Separe los nombres de los destinatarios que especifique en este argumento (y en los argumentos <em>Cc</em> y <em>CCO</em> ) con un punto y coma (;).</span><span class="sxs-lookup"><span data-stu-id="797a1-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="797a1-114"><strong>CC</strong></span><span class="sxs-lookup"><span data-stu-id="797a1-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="797a1-115">No</span><span class="sxs-lookup"><span data-stu-id="797a1-115">No</span></span></p></td>
<td><p><span data-ttu-id="797a1-116">Los destinatarios del mensaje cuyos nombres desee indicar en el campo Cc (&quot;copia carbón&quot;) línea del mensaje.</span><span class="sxs-lookup"><span data-stu-id="797a1-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="797a1-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="797a1-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="797a1-118">No</span><span class="sxs-lookup"><span data-stu-id="797a1-118">No</span></span></p></td>
<td><p><span data-ttu-id="797a1-119">Los destinatarios del mensaje cuyos nombres desee indicar en la CCO (&quot;copia carbón oculta&quot;) línea del mensaje.</span><span class="sxs-lookup"><span data-stu-id="797a1-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="797a1-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="797a1-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="797a1-121">No</span><span class="sxs-lookup"><span data-stu-id="797a1-121">No</span></span></p></td>
<td><p><span data-ttu-id="797a1-p101">Asunto del mensaje. Este texto aparece en la línea <strong>Asunto</strong> del mensaje.</span><span class="sxs-lookup"><span data-stu-id="797a1-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="797a1-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="797a1-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="797a1-125">No</span><span class="sxs-lookup"><span data-stu-id="797a1-125">No</span></span></p></td>
<td><p><span data-ttu-id="797a1-p102">El texto que desea incluir en el cuerpo principal del mensaje de correo. Si deja en blanco este argumento, no se incluirá ningún texto adicional en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="797a1-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="797a1-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="797a1-128">Remarks</span></span>

<span data-ttu-id="797a1-129">La acción **EnviarCorreoElectrónico** solo está disponible en los eventos de macro **[Después de eliminar](after-delete-macro-event.md)**, **[Después de insertar](after-insert-macro-event.md)** y **[Después de actualizar](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="797a1-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="797a1-130">La acción **EnviarCorreoElectrónico** no muestra el mensaje para su edición.</span><span class="sxs-lookup"><span data-stu-id="797a1-130">The **SendEmail** action does not display the message for editing.</span></span>

