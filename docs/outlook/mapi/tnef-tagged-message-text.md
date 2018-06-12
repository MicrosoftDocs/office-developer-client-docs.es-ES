---
title: Texto del mensaje con etiqueta TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820870"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="1e95c-103">Texto del mensaje con etiqueta TNEF</span><span class="sxs-lookup"><span data-stu-id="1e95c-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="1e95c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e95c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e95c-105">Texto del mensaje con etiqueta se usa en TNEF para resolver las posiciones de los datos adjuntos en el mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="1e95c-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="1e95c-106">Esto se realiza mediante la adición de un marcador de posición en el texto del mensaje en la posición de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1e95c-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="1e95c-107">Este marcador de posición o etiqueta de datos adjuntos, se describe los datos adjuntos de forma que TNEF sabe cómo resolver los datos adjuntos y su posición.</span><span class="sxs-lookup"><span data-stu-id="1e95c-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="1e95c-108">Las etiquetas tienen el formato de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1e95c-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="1e95c-109">** \<Objeto título\> ** y ** \<nombre de archivo\> ** son variables que contiene los valores que se toman de los datos adjuntos del propio.</span><span class="sxs-lookup"><span data-stu-id="1e95c-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="1e95c-110">En los casos en que estos valores no están disponibles, el título es el predeterminado por TNEF en función del tipo de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="1e95c-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="1e95c-111">La ** \<KeyNum\> ** variable contiene la representación textual de la clave de datos adjuntos que se ha asignado a los datos adjuntos TNEF.</span><span class="sxs-lookup"><span data-stu-id="1e95c-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="1e95c-112">El valor de base de la clave se pasa a la llamada de [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="1e95c-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="1e95c-113">El valor de base no debe ser cero y no debe ser el mismo para todas las llamadas a **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="1e95c-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="1e95c-114">Debe ser suficiente para usar números aleatorios ficticio según la hora del sistema desde cualquier generador de números aleatorios que proporciona la biblioteca de tiempo de ejecución, siempre y cuando se garantiza que nunca son cero.</span><span class="sxs-lookup"><span data-stu-id="1e95c-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="1e95c-115">La ** \<nombre del transporte\> ** variable contiene el nombre de secuencia pasado a la llamada [OpenTnefStreamEx](opentnefstreamex.md) o el valor de la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1e95c-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1e95c-116">La propiedad **PR_ATTACH_TRANSPORT_NAME** y el ** \<nombre del transporte\> ** variable en una etiqueta de texto del mensaje no tienen nada que ver con el nombre del proveedor de transporte que va a implementar.</span><span class="sxs-lookup"><span data-stu-id="1e95c-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="1e95c-117">Estos elementos representan el nombre de datos adjuntos para el proveedor de transporte y el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1e95c-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="1e95c-118">El texto del mensaje está etiquetado cuando un proveedor de transporte solicita un mensaje con etiqueta de texto llamando al método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="1e95c-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="1e95c-119">Al leer de la secuencia de texto con etiqueta, TNEF reemplaza el carácter único que se encontraba en el texto del mensaje en el índice proporcionado en la propiedad **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) con la etiqueta adecuada.</span><span class="sxs-lookup"><span data-stu-id="1e95c-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="1e95c-120">Al escribir en la secuencia de texto con etiqueta, TNEF comprueba los datos entrantes para las etiquetas, los datos adjuntos asociados no encuentra y reemplaza la etiqueta con un único carácter de espacio.</span><span class="sxs-lookup"><span data-stu-id="1e95c-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="1e95c-121">Tenga en cuenta que, mediante el uso de texto del mensaje con etiqueta, un proveedor de transporte puede conservar la colocación de los datos adjuntos, independientemente de la mayoría de los cambios realizado en el texto del mensaje por sistemas de mensajería.</span><span class="sxs-lookup"><span data-stu-id="1e95c-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

