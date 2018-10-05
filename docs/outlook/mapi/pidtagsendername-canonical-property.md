---
title: Propiedad canónica PidTagSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398461"
---
# <a name="pidtagsendername-canonical-property"></a><span data-ttu-id="96c4c-103">Propiedad canónica PidTagSenderName</span><span class="sxs-lookup"><span data-stu-id="96c4c-103">PidTagSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="96c4c-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96c4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96c4c-105">Contiene el nombre para mostrar del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="96c4c-105">Contains the message sender's display name.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96c4c-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="96c4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96c4c-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="96c4c-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="96c4c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="96c4c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96c4c-109">0x0C1A</span><span class="sxs-lookup"><span data-stu-id="96c4c-109">0x0C1A</span></span>  <br/> |
|<span data-ttu-id="96c4c-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="96c4c-110">Data type:</span></span>  <br/> |<span data-ttu-id="96c4c-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="96c4c-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="96c4c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="96c4c-112">Area:</span></span>  <br/> |<span data-ttu-id="96c4c-113">Address</span><span class="sxs-lookup"><span data-stu-id="96c4c-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96c4c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96c4c-114">Remarks</span></span>

<span data-ttu-id="96c4c-115">Estas propiedades son ejemplos de las propiedades de direcciones para el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="96c4c-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="96c4c-116">Se debe establecer por el proveedor de transporte saliente, que nunca se debe propagar los valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="96c4c-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="96c4c-117">Si no hay proveedor de transporte ha proporcionado las propiedades de dirección del remitente, la cola MAPI intenta rellenar llamando al método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para obtener un identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="96c4c-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="96c4c-118">Si se han proporcionado sin los identificadores de entrada, la cola MAPI almacena a "Unknown" en todas las propiedades de dirección de remitente del tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="96c4c-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="96c4c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96c4c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96c4c-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="96c4c-120">Protocol specifications</span></span>

<span data-ttu-id="96c4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="96c4c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96c4c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-124">Describe el formato de los mensajes que se utiliza para enviar información relacionada con el uso compartido de carpetas en el cliente.</span><span class="sxs-lookup"><span data-stu-id="96c4c-124">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
<span data-ttu-id="96c4c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-126">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="96c4c-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="96c4c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-128">Controla el orden y el flujo para las transferencias de datos entre un cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="96c4c-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="96c4c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-130">Convierte entre RFC2445 IETF, RFC2446 y RFC2447 y una cita y objetos de la reunión.</span><span class="sxs-lookup"><span data-stu-id="96c4c-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="96c4c-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-132">Especifica las propiedades y operaciones que se permiten para registrar objetos.</span><span class="sxs-lookup"><span data-stu-id="96c4c-132">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="96c4c-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-134">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="96c4c-134">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="96c4c-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96c4c-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96c4c-136">Codifica y descodifica los objetos de mensaje y datos adjuntos a una representación de secuencia eficaz.</span><span class="sxs-lookup"><span data-stu-id="96c4c-136">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96c4c-137">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="96c4c-137">Header files</span></span>

<span data-ttu-id="96c4c-138">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96c4c-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="96c4c-139">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="96c4c-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="96c4c-140">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96c4c-140">Mapitags.h</span></span>
  
> <span data-ttu-id="96c4c-141">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="96c4c-141">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96c4c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="96c4c-142">See also</span></span>



[<span data-ttu-id="96c4c-143">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96c4c-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96c4c-144">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="96c4c-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96c4c-145">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="96c4c-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96c4c-146">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="96c4c-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

