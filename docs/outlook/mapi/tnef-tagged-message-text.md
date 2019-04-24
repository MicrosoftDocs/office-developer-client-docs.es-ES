---
title: Texto del mensaje etiquetado con TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339595"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="07859-103">Texto del mensaje etiquetado con TNEF</span><span class="sxs-lookup"><span data-stu-id="07859-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="07859-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07859-105">TNEF utiliza el texto del mensaje etiquetado para resolver las posiciones de los datos adjuntos en el mensaje principal.</span><span class="sxs-lookup"><span data-stu-id="07859-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="07859-106">Esto se realiza agregando un marcador de posición en el texto del mensaje en la posición de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="07859-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="07859-107">Este marcador de posición, o etiqueta de datos adjuntos, describe los datos adjuntos de tal manera que TNEF sabe cómo resolver los datos adjuntos y su posición.</span><span class="sxs-lookup"><span data-stu-id="07859-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="07859-108">Las etiquetas tienen el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="07859-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="07859-109">**El título\> del objeto y el nombre de archivo son variables que contienen valores de los datos adjuntos en sí. \<** \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="07859-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="07859-110">En los casos en los que estos valores no están disponibles, el título es el predeterminado en formato TNEF en función del tipo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="07859-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="07859-111">La \*\* \<variable\> KeyNum\*\* contiene la representación textual de la clave de datos adjuntos asignada a los datos adjuntos por TNEF.</span><span class="sxs-lookup"><span data-stu-id="07859-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="07859-112">El valor base de la clave se pasa a la llamada [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="07859-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="07859-113">El valor base no debe ser cero y no debe ser el mismo para cada llamada a **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="07859-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="07859-114">Debe bastar con usar números pseudoaleatorios en función de la hora del sistema, desde cualquier generador de números aleatorios que proporcione la biblioteca en tiempo de ejecución, siempre que se garantice que nunca son cero.</span><span class="sxs-lookup"><span data-stu-id="07859-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="07859-115">La \*\* \<variable de\> nombre de transporte\*\* contiene el nombre de la secuencia que se ha pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="07859-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="07859-116">La propiedad **PR_ATTACH_TRANSPORT_NAME** y la \*\* \<variable de\> nombre de transporte\*\* de una etiqueta de texto de mensaje no tienen nada que saber con el nombre del proveedor de transporte que se está implementando.</span><span class="sxs-lookup"><span data-stu-id="07859-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="07859-117">Estos elementos representan el nombre de los datos adjuntos del proveedor de transporte y el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="07859-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="07859-118">El texto del mensaje se etiqueta cuando un proveedor de transporte solicita el texto del mensaje etiquetado llamando al método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="07859-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="07859-119">Al leer de la secuencia de texto etiquetada, TNEF reemplaza el carácter único que estaba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) con la etiqueta adecuada.</span><span class="sxs-lookup"><span data-stu-id="07859-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="07859-120">Al escribir en la secuencia de texto etiquetada, TNEF comprueba las etiquetas de los datos entrantes, busca los datos adjuntos asociados y reemplaza la etiqueta con un solo carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="07859-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="07859-121">Tenga en cuenta que, al usar el texto del mensaje etiquetado, un proveedor de transporte puede conservar la posición de los datos adjuntos independientemente de la mayoría de los cambios realizados en el texto del mensaje por sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="07859-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

