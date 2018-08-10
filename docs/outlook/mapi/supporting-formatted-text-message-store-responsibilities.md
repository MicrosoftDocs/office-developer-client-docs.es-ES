---
title: Compatibilidad con las responsabilidades del almacén de mensajes con formato de texto
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820780"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a><span data-ttu-id="80d21-103">Admitir texto con formato: responsabilidades de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="80d21-103">Supporting Formatted Text: Message Store Responsibilities</span></span>

  
  
<span data-ttu-id="80d21-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="80d21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="80d21-105">Los proveedores de almacén de mensajes usar la propiedad **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para publicar o no puede controlar el formato de texto enriquecido (RTF), texto HTML y, si son compatible con RTF, si se almacenan el texto con formato en un formato comprimido o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="80d21-105">Message store providers use the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to publish whether or not they can handle Rich Text Format (RTF), HTML text and, if they are RTF-aware, whether they store the formatted text in a compressed or uncompressed format.</span></span> <span data-ttu-id="80d21-106">Los proveedores de almacén de mensajes indican que son conscientes de RTF estableciendo el bit STORE_RTF_OK y que contienen el texto con formato en un formulario sin comprimir estableciendo el bit STORE_UNCOMPRESSED_RTF.</span><span class="sxs-lookup"><span data-stu-id="80d21-106">Message store providers indicate that they are RTF-aware by setting the STORE_RTF_OK bit and that they store the formatted text in an uncompressed form by setting the STORE_UNCOMPRESSED_RTF bit.</span></span> <span data-ttu-id="80d21-107">Los proveedores de almacén de mensajes indican que son compatibles con HTML estableciendo el bit STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="80d21-107">Message store providers indicate they are HTML-aware by setting the STORE_HTML_OK bit.</span></span>
  
<span data-ttu-id="80d21-108">Aunque es importante para un cliente compatible con RTF comprobar si la STORE_RTF_OK de bit para determinar si admite o no un almacén de mensajes RTF, no es necesario para que un cliente afectados con el formato de texto con formato de un almacén de tener en cuenta RTF.</span><span class="sxs-lookup"><span data-stu-id="80d21-108">While it is important for an RTF-aware client to check for the STORE_RTF_OK bit to determine whether or not a message store supports RTF, it is not necessary for a client to be concerned with the format of an RTF-aware store's formatted text.</span></span> 
  
<span data-ttu-id="80d21-109">Todos los almacenes de mensaje deben admitir a clientes ajenos a RTF.</span><span class="sxs-lookup"><span data-stu-id="80d21-109">All message stores must support non-RTF-aware clients.</span></span> <span data-ttu-id="80d21-110">Un almacén de mensajes RTF reconozca debe eliminar la propiedad **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) durante una llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) del mensaje, si un cliente ha cambiado **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) sin actualización de **PR_RTF_IN_SYNC** o **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="80d21-110">A non-RTF-aware message store must delete the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property during a call to the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method if a client has changed **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) without updating either **PR_RTF_IN_SYNC** or **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> <span data-ttu-id="80d21-111">Eliminación de **PR_RTF_IN_SYNC** hace que la propiedad **PR_RTF_COMPRESSED** que volver a calcularse la próxima vez que llama a un cliente compatible con RTF [RTFSync](rtfsync.md)desde la propiedad **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="80d21-111">Deleting **PR_RTF_IN_SYNC** causes the **PR_RTF_COMPRESSED** property to be recomputed from the **PR_BODY** property the next time an RTF-aware client calls [RTFSync](rtfsync.md).</span></span> 
  
<span data-ttu-id="80d21-112">Almacenes de mensaje compatibles con RTF mayoría no se le proporciona el texto del mensaje por los clientes; se debe calcular en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80d21-112">Most RTF-aware message stores are not given the message text by clients; it must be computed on request.</span></span> <span data-ttu-id="80d21-113">Dado que este cálculo es largo y costoso, los clientes deben usar **PR_RTF_COMPRESSED** siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="80d21-113">Because this computation is time consuming and expensive, clients should use **PR_RTF_COMPRESSED** whenever possible.</span></span> <span data-ttu-id="80d21-114">Para calcular la propiedad **PR_BODY** , el proveedor de almacén de mensajes debe descomprimir el contenido de la propiedad **PR_RTF_COMPRESSED** y quitar el formato de texto enriquecido.</span><span class="sxs-lookup"><span data-stu-id="80d21-114">To compute the **PR_BODY** property, the message store provider must uncompress the contents of the **PR_RTF_COMPRESSED** property and remove the rich text formatting.</span></span> <span data-ttu-id="80d21-115">Los clientes que no admiten la propiedad **PR_RTF_COMPRESSED** requieren este cálculo tengan lugar para todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="80d21-115">Clients that do not support the **PR_RTF_COMPRESSED** property require this computation to take place for every message.</span></span> 
  
<span data-ttu-id="80d21-116">Cuando se copian los mensajes, los proveedores que no usan los métodos **IMAPISupport::DoCopyProps** o **IMAPISupport::DoCopyTo** , corre el riesgo de la creación de un mensaje sin contenido si su implementación excluye la **PR_BODY** del almacén de mensajes propiedad y se basa en **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="80d21-116">When copying messages, message store providers that do not use the **IMAPISupport::DoCopyProps** or **IMAPISupport::DoCopyTo** methods run the risk of creating a message with no content if their implementation excludes the **PR_BODY** property and relies on **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="80d21-117">Es posible que los datos de la propiedad **PR_RTF_COMPRESSED** esté dañado.</span><span class="sxs-lookup"><span data-stu-id="80d21-117">It is possible for the data in the **PR_RTF_COMPRESSED** property to be corrupt.</span></span> <span data-ttu-id="80d21-118">Antes de exclusión de cualquiera de estas propiedades de contenido de mensaje en la operación de copia, compruebe daños en la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="80d21-118">Before excluding either of these message content properties in the copy operation, check for corruption as follows:</span></span> 
  
1. <span data-ttu-id="80d21-119">Si el valor de **PR_RTF_COMPRESSED** no es mayor que el comprimido RTF, la propiedad está dañada.</span><span class="sxs-lookup"><span data-stu-id="80d21-119">If the value of **PR_RTF_COMPRESSED** is not larger than the compressed RTF, the property is corrupt.</span></span> 
    
2. <span data-ttu-id="80d21-120">Si el valor de magia en el encabezado RTF no es _dwMagicCompressedRTF_ o _dwMagicUncompressedRTF_, la propiedad está dañado.</span><span class="sxs-lookup"><span data-stu-id="80d21-120">If the magic value in the RTF header is not  _dwMagicCompressedRTF_ or  _dwMagicUncompressedRTF_, the property is corrupt.</span></span>
    
<span data-ttu-id="80d21-121">Mediante los métodos necesitan a no ser que se trate con la implementación de una comprobación de posibles daños **PR_RTF_COMPRESSED** ; la compatibilidad con los proveedores del almacén de mensajes MAPI se asegura de que las propiedades adecuadas existen y son válidas.</span><span class="sxs-lookup"><span data-stu-id="80d21-121">Message store providers using the support methods need not be concerned with implementing a check for **PR_RTF_COMPRESSED** corruption; MAPI ensures that the appropriate properties exist and are valid.</span></span> 
  
<span data-ttu-id="80d21-122">Hay tres niveles diferentes de compatibilidad RTF que se pueden implementar los proveedores de almacén de mensajes; MAPI, se recomienda que los proveedores de almacén de mensajes RTF para implementan su compatibilidad en el nivel intermedio o más alto.</span><span class="sxs-lookup"><span data-stu-id="80d21-122">There are three different levels of RTF support that message store providers can implement; MAPI recommends that RTF-aware message store providers implement their support at the middle or highest level.</span></span> <span data-ttu-id="80d21-123">Todos los compatible con RTF almacén de mensajes proveedores se encargan de generar **PR_BODY** a partir de los datos incluidos en **PR_RTF_COMPRESSED** en los mensajes salientes y realizar una llamada a **RTFSync** para sincronizar el formato de texto y en los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="80d21-123">All RTF-aware message store providers take care of generating **PR_BODY** from the data included in **PR_RTF_COMPRESSED** on outgoing messages and make a call to **RTFSync** to synchronize text and formatting on incoming messages.</span></span> 
  
<span data-ttu-id="80d21-124">Las diferencias entre estos tres niveles se describen en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="80d21-124">The differences between these three levels are described in the following table.</span></span> 
  
|<span data-ttu-id="80d21-125">**Nivel de compatibilidad**</span><span class="sxs-lookup"><span data-stu-id="80d21-125">**Level of support**</span></span>|<span data-ttu-id="80d21-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80d21-126">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80d21-127">Low</span><span class="sxs-lookup"><span data-stu-id="80d21-127">Low</span></span>  <br/> |<span data-ttu-id="80d21-128">Mensaje de almacenar las llamadas de proveedor **RTFSync** cada vez que se guardan los cambios en un mensaje y extrae los datos para la propiedad **PR_BODY** **PR_RTF_COMPRESSED** en lugar de los clientes que requieren para establecerla.</span><span class="sxs-lookup"><span data-stu-id="80d21-128">Message store provider calls **RTFSync** whenever changes are saved to a message and extracts the data for the **PR_BODY** property from **PR_RTF_COMPRESSED** rather than requiring clients to set it.</span></span> <span data-ttu-id="80d21-129">**PR_BODY** y **PR_RTF_COMPRESSED** se almacenan.</span><span class="sxs-lookup"><span data-stu-id="80d21-129">Both **PR_BODY** and **PR_RTF_COMPRESSED** are stored.</span></span>  <br/> |
|<span data-ttu-id="80d21-130">En medio</span><span class="sxs-lookup"><span data-stu-id="80d21-130">Middle</span></span>  <br/> |<span data-ttu-id="80d21-131">Almacén de mensajes almacenes proveedor sólo la propiedad **PR_RTF_COMPRESSED** , los sistemas **PR_BODY** cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="80d21-131">Message store provider stores only the **PR_RTF_COMPRESSED** property, computing **PR_BODY** when necessary.</span></span>  <br/> |
|<span data-ttu-id="80d21-132">High</span><span class="sxs-lookup"><span data-stu-id="80d21-132">High</span></span>  <br/> |<span data-ttu-id="80d21-133">Almacenes de proveedor de almacén de mensajes ni **PR_BODY** o las propiedades RTF auxiliares.</span><span class="sxs-lookup"><span data-stu-id="80d21-133">Message store provider stores neither **PR_BODY** or the auxiliary RTF properties.</span></span> <span data-ttu-id="80d21-134">**RTFSync** se llama cuando se ha cambiado el texto del mensaje y el formato permanece inalterado o cuando se descarga un nuevo mensaje de un proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="80d21-134">**RTFSync** is called when the message text has changed and the formatting remains unchanged or when a new message is downloaded by a transport provider.</span></span>  <br/> |
   
