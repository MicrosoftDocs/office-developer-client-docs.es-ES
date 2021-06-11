---
title: TNEF-Tagged texto del mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419922"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="3bb16-103">TNEF-Tagged texto del mensaje</span><span class="sxs-lookup"><span data-stu-id="3bb16-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="3bb16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bb16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bb16-105">TNEF usa el texto del mensaje etiquetado para resolver las posiciones de datos adjuntos en el mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="3bb16-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="3bb16-106">Para ello, agregue un soporte de posición en el texto del mensaje en la posición de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3bb16-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="3bb16-107">Este soporte de posición, o etiqueta de datos adjuntos, describe los datos adjuntos de forma que TNEF sepa cómo resolver los datos adjuntos y su posición.</span><span class="sxs-lookup"><span data-stu-id="3bb16-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="3bb16-108">Las etiquetas tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="3bb16-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="3bb16-109">**\< Título \> del objeto** y **\< Nombre de \> archivo** son variables que contienen valores que se toman de los datos adjuntos en sí.</span><span class="sxs-lookup"><span data-stu-id="3bb16-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="3bb16-110">En los casos en los que estos valores no están disponibles, TNEF tiene el título predeterminado en función del tipo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3bb16-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="3bb16-111">La **\< variable \> KeyNum** contiene la representación textual de la clave de datos adjuntos asignada a los datos adjuntos por TNEF.</span><span class="sxs-lookup"><span data-stu-id="3bb16-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="3bb16-112">El valor base de la clave se pasa a la [llamada OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="3bb16-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="3bb16-113">El valor base no debe ser cero y no debe ser el mismo para cada llamada a **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="3bb16-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="3bb16-114">Debe bastar con usar números pseudo aleatorios en función del tiempo del sistema desde cualquier generador de números aleatorios que la biblioteca de tiempo de ejecución proporciona, siempre y cuando se garantice que nunca son cero.</span><span class="sxs-lookup"><span data-stu-id="3bb16-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="3bb16-115">La variable **\< Transport \> Name** contiene el nombre de secuencia pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb16-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3bb16-116">La **PR_ATTACH_TRANSPORT_NAME** y la variable **\< Transport Name \>** de una etiqueta de texto de mensaje no tienen nada que ver con el nombre del proveedor de transporte que está implementando.</span><span class="sxs-lookup"><span data-stu-id="3bb16-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="3bb16-117">Estos elementos representan el nombre de un archivo adjunto para el proveedor de transporte y el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3bb16-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="3bb16-118">El texto del mensaje se etiqueta cuando un proveedor de transporte solicita un texto de mensaje etiquetado llamando al [método ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="3bb16-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="3bb16-119">Al leer desde la secuencia de texto etiquetada, TNEF reemplaza el carácter único que estaba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) por la etiqueta adecuada.</span><span class="sxs-lookup"><span data-stu-id="3bb16-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="3bb16-120">Al escribir en la secuencia de texto etiquetada, TNEF comprueba las etiquetas de los datos entrantes, busca los datos adjuntos asociados y reemplaza la etiqueta por un solo carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="3bb16-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="3bb16-121">Tenga en cuenta que al usar texto de mensaje etiquetado, un proveedor de transporte puede conservar el posicionamiento de los datos adjuntos independientemente de la mayoría de los cambios realizados en el texto del mensaje por los sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="3bb16-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

