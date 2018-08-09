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
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819720"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="57ac9-103">Propiedad canónica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="57ac9-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="57ac9-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57ac9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57ac9-105">Contiene una cadena de texto que identifica la clase de mensaje definido por el remitente, como IPM. Tenga en cuenta.</span><span class="sxs-lookup"><span data-stu-id="57ac9-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57ac9-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="57ac9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57ac9-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="57ac9-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="57ac9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="57ac9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57ac9-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="57ac9-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="57ac9-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="57ac9-110">Data type:</span></span>  <br/> |<span data-ttu-id="57ac9-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="57ac9-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="57ac9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="57ac9-112">Area:</span></span>  <br/> |<span data-ttu-id="57ac9-113">Common</span><span class="sxs-lookup"><span data-stu-id="57ac9-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57ac9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57ac9-114">Remarks</span></span>

<span data-ttu-id="57ac9-115">La clase de mensaje especifica el tipo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="57ac9-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="57ac9-116">Determina el conjunto de propiedades definidas para el mensaje, el tipo de información del mensaje se transmite y cómo controlar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="57ac9-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="57ac9-117">Estas propiedades contienen las cadenas que se concatena con períodos.</span><span class="sxs-lookup"><span data-stu-id="57ac9-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="57ac9-118">Cada cadena representa un nivel de creación de subclases.</span><span class="sxs-lookup"><span data-stu-id="57ac9-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="57ac9-119">Por ejemplo, IPM. Nota es una subclase de IPM y una superclase de IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="57ac9-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="57ac9-120">Estas propiedades deben constar de los caracteres ASCII 32 a 127 y no deben terminar con un punto (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="57ac9-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="57ac9-121">Las operaciones de ordenación y comparación deben tratar como una cadena entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="57ac9-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="57ac9-122">La longitud máxima permitida es de 255 caracteres, pero con el fin de permitir la sala MAPI anexar calificadores se recomienda que la longitud original mantenerse por debajo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="57ac9-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="57ac9-123">Cada mensaje es necesario para proporcionar estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="57ac9-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="57ac9-124">Normalmente, la aplicación cliente de creación de un nuevo mensaje establece tan pronto como [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) devuelve correctamente.</span><span class="sxs-lookup"><span data-stu-id="57ac9-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="57ac9-125">Pero si no se ha establecido la propiedad cuando el cliente llama a [IMAPIProp::SaveChanges](imapiprop-savechanges.md), el almacén de mensajes debe establecer para IPM.</span><span class="sxs-lookup"><span data-stu-id="57ac9-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="57ac9-126">Los valores definidos por MAPI son:</span><span class="sxs-lookup"><span data-stu-id="57ac9-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="57ac9-127">IPM y IPC están diseñados para ser solo superclase, y un mensaje debe tener al menos un calificador de subclase anexado antes de que se almacenan o enviado.</span><span class="sxs-lookup"><span data-stu-id="57ac9-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="57ac9-128">Para obtener más información sobre el uso de la clase de mensaje, vea [Las clases de mensajes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="57ac9-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="57ac9-129">Para las listas de propiedades opcionales y obligatorios para las clases de mensajes, vea los temas secundarios de [Acerca de propiedades del mensaje](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57ac9-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="57ac9-130">Una clase de mensaje personalizada puede definir propiedades en un intervalo reservado para su uso con sólo esa clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="57ac9-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="57ac9-131">Para obtener más información, vea [Acerca de identificadores de propiedad](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="57ac9-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="57ac9-132">Control de clases de mensaje que recibe un mensaje entrante de la carpeta se almacena en.</span><span class="sxs-lookup"><span data-stu-id="57ac9-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="57ac9-133">Para obtener más información, vea el método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="57ac9-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="57ac9-134">Para obtener más información sobre el uso de las clases de mensajes con servidores de formulario y formularios, vea [Elegir una clase de mensaje](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="57ac9-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="57ac9-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="57ac9-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="57ac9-136">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="57ac9-136">Protocol specifications</span></span>

<span data-ttu-id="57ac9-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57ac9-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57ac9-138">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="57ac9-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="57ac9-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57ac9-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57ac9-140">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="57ac9-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="57ac9-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57ac9-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57ac9-142">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="57ac9-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="57ac9-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="57ac9-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="57ac9-144">Especifica las propiedades y operaciones que se permiten para que representa los mensajes de fax y correo de voz.</span><span class="sxs-lookup"><span data-stu-id="57ac9-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="57ac9-145">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="57ac9-145">Header files</span></span>

<span data-ttu-id="57ac9-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57ac9-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="57ac9-147">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="57ac9-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="57ac9-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57ac9-148">Mapitags.h</span></span>
  
> <span data-ttu-id="57ac9-149">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="57ac9-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57ac9-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="57ac9-150">See also</span></span>



[<span data-ttu-id="57ac9-151">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="57ac9-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57ac9-152">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="57ac9-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57ac9-153">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="57ac9-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57ac9-154">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="57ac9-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

