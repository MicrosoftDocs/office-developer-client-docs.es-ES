---
title: Propiedad canónica PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397369"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="48db8-103">Propiedad canónica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="48db8-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="48db8-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48db8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48db8-105">Representa el estado de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="48db8-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48db8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="48db8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="48db8-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="48db8-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="48db8-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="48db8-108">Property set:</span></span>  <br/> |<span data-ttu-id="48db8-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="48db8-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="48db8-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="48db8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="48db8-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="48db8-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="48db8-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="48db8-112">Data type:</span></span>  <br/> |<span data-ttu-id="48db8-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="48db8-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="48db8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="48db8-114">Area:</span></span>  <br/> |<span data-ttu-id="48db8-115">Marcar</span><span class="sxs-lookup"><span data-stu-id="48db8-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="48db8-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48db8-116">Remarks</span></span>

<span data-ttu-id="48db8-117">En Microsoft Office Outlook, una convocatoria de reunión es un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="48db8-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="48db8-118">Esta propiedad contiene texto puede especificar el usuario que se asociará con la marca y se debería establecer, si el objeto de mensaje se marcan o completado, pero no debe existir para un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="48db8-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="48db8-119">Los clientes pueden elegir no admite esta propiedad y escribir siempre "Seguimiento" (traducido para el idioma del usuario si es necesario) como el valor de la cadena cuando se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="48db8-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="48db8-120">Esta propiedad se debe omitir condicionalmente en función de los valores de las propiedades de **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) y **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48db8-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="48db8-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="48db8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="48db8-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="48db8-122">Protocol specifications</span></span>

<span data-ttu-id="48db8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48db8-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48db8-124">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="48db8-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="48db8-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="48db8-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="48db8-126">Especifica las propiedades y las operaciones relacionadas con marcas.</span><span class="sxs-lookup"><span data-stu-id="48db8-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="48db8-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="48db8-127">Header files</span></span>

<span data-ttu-id="48db8-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48db8-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="48db8-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="48db8-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="48db8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="48db8-130">See also</span></span>



[<span data-ttu-id="48db8-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="48db8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="48db8-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="48db8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="48db8-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="48db8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="48db8-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="48db8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

