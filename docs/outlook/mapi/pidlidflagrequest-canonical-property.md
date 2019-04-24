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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357809"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="67eb4-103">Propiedad canónica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="67eb4-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="67eb4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67eb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67eb4-105">Representa el estado de una convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="67eb4-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67eb4-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="67eb4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67eb4-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="67eb4-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="67eb4-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="67eb4-108">Property set:</span></span>  <br/> |<span data-ttu-id="67eb4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="67eb4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="67eb4-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="67eb4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="67eb4-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="67eb4-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="67eb4-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="67eb4-112">Data type:</span></span>  <br/> |<span data-ttu-id="67eb4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="67eb4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="67eb4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="67eb4-114">Area:</span></span>  <br/> |<span data-ttu-id="67eb4-115">Marcar</span><span class="sxs-lookup"><span data-stu-id="67eb4-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67eb4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67eb4-116">Remarks</span></span>

<span data-ttu-id="67eb4-117">En Microsoft Office Outlook, una convocatoria de reunión es un elemento de cita.</span><span class="sxs-lookup"><span data-stu-id="67eb4-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="67eb4-118">Esta propiedad contiene texto especificable por el usuario que debe asociarse con la marca y debe establecerse si el objeto de mensaje está marcado o completado, pero no debe existir para un objeto relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="67eb4-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="67eb4-119">Los clientes pueden elegir no admitir esta propiedad y escribir siempre "seguimiento" (convertido en el idioma del usuario si corresponde) como valor de la cadena cuando se debe establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="67eb4-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="67eb4-120">Esta propiedad se debe omitir condicionalmente en función de los valores de las propiedades **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="67eb4-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="67eb4-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="67eb4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67eb4-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="67eb4-122">Protocol specifications</span></span>

<span data-ttu-id="67eb4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67eb4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67eb4-124">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="67eb4-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67eb4-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67eb4-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67eb4-126">Especifica las propiedades y operaciones relacionadas con la marcación.</span><span class="sxs-lookup"><span data-stu-id="67eb4-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67eb4-127">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="67eb4-127">Header files</span></span>

<span data-ttu-id="67eb4-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="67eb4-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="67eb4-129">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="67eb4-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67eb4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="67eb4-130">See also</span></span>



[<span data-ttu-id="67eb4-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67eb4-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67eb4-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="67eb4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67eb4-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="67eb4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

