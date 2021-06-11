---
title: Propiedad canónica PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359270"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="05ad7-103">Propiedad canónica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="05ad7-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="05ad7-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05ad7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05ad7-105">Contiene una cadena de texto que identifica la clase de mensaje definida por el remitente, como IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="05ad7-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05ad7-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="05ad7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05ad7-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="05ad7-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="05ad7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="05ad7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05ad7-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="05ad7-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="05ad7-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="05ad7-110">Data type:</span></span>  <br/> |<span data-ttu-id="05ad7-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="05ad7-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="05ad7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="05ad7-112">Area:</span></span>  <br/> |<span data-ttu-id="05ad7-113">Común</span><span class="sxs-lookup"><span data-stu-id="05ad7-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05ad7-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05ad7-114">Remarks</span></span>

<span data-ttu-id="05ad7-115">La clase message especifica el tipo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="05ad7-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="05ad7-116">Determina el conjunto de propiedades definidas para el mensaje, el tipo de información que transmite el mensaje y cómo controlar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="05ad7-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="05ad7-117">Estas propiedades contienen cadenas concatenadas con puntos.</span><span class="sxs-lookup"><span data-stu-id="05ad7-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="05ad7-118">Cada cadena representa un nivel de subclase.</span><span class="sxs-lookup"><span data-stu-id="05ad7-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="05ad7-119">Por ejemplo, IPM. Nota es una subclase de IPM y una superclase de IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="05ad7-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="05ad7-120">Estas propiedades deben estar formadas por los caracteres ASCII 32 a 127 y no deben terminar con un punto (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="05ad7-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="05ad7-121">Las operaciones de ordenación y comparación deben tratarse como una cadena que no diferencia mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="05ad7-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="05ad7-122">La longitud máxima posible es de 255 caracteres, pero para permitir que el salón MAPI anexe calificadores, se recomienda mantener la longitud original por debajo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="05ad7-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="05ad7-123">Cada mensaje es necesario para proporcionar estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="05ad7-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="05ad7-124">Normalmente, la aplicación cliente que crea un mensaje nuevo lo establece tan pronto [como IMAPIFolder::CreateMessage](imapifolder-createmessage.md) devuelve correctamente.</span><span class="sxs-lookup"><span data-stu-id="05ad7-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="05ad7-125">Pero si la propiedad no se ha establecido cuando el cliente llama a [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)el almacén de mensajes debe establecerlo en IPM.</span><span class="sxs-lookup"><span data-stu-id="05ad7-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="05ad7-126">Los valores definidos por MAPI son:</span><span class="sxs-lookup"><span data-stu-id="05ad7-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="05ad7-127">IPM e IPC están diseñados para ser superclases solamente y un mensaje debe tener al menos un calificador de subclase anexado antes de almacenarse o enviarse.</span><span class="sxs-lookup"><span data-stu-id="05ad7-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="05ad7-128">Para obtener más información sobre el uso de clases de mensaje, vea [Clases de mensaje](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="05ad7-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="05ad7-129">Para obtener listas de propiedades obligatorias y opcionales para las clases de mensaje, vea los subtemas de [Acerca de las propiedades del mensaje](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="05ad7-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="05ad7-130">Una clase de mensaje personalizada puede definir propiedades en un intervalo reservado para su uso solo con esa clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="05ad7-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="05ad7-131">Para obtener más información, vea [About Property Identifiers](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="05ad7-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="05ad7-132">Las clases de mensaje controlan en qué carpeta de recepción se almacena un mensaje entrante.</span><span class="sxs-lookup"><span data-stu-id="05ad7-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="05ad7-133">Para obtener más información, vea el [método IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="05ad7-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="05ad7-134">Para obtener más información sobre el uso de clases de mensaje con formularios y servidores de formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="05ad7-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="05ad7-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="05ad7-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="05ad7-136">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="05ad7-136">Protocol specifications</span></span>

<span data-ttu-id="05ad7-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05ad7-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05ad7-138">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="05ad7-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="05ad7-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05ad7-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05ad7-140">Controla objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="05ad7-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="05ad7-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05ad7-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05ad7-142">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="05ad7-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="05ad7-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="05ad7-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="05ad7-144">Especifica las propiedades y las operaciones permitidas para representar mensajes de correo de voz y fax.</span><span class="sxs-lookup"><span data-stu-id="05ad7-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="05ad7-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="05ad7-145">Header files</span></span>

<span data-ttu-id="05ad7-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05ad7-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="05ad7-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="05ad7-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="05ad7-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="05ad7-148">Mapitags.h</span></span>
  
> <span data-ttu-id="05ad7-149">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="05ad7-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05ad7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="05ad7-150">See also</span></span>



[<span data-ttu-id="05ad7-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="05ad7-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05ad7-152">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="05ad7-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05ad7-153">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="05ad7-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05ad7-154">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="05ad7-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

