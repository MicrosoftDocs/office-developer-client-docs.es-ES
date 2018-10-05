---
title: Propiedad canónica PidNameExchangeJunkEmailMoveStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 07acfd8715dccad8833ee14ac8e573fb995539ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399707"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="8f776-103">Propiedad canónica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="8f776-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="8f776-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f776-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f776-105">Contiene el valor conservado de mensaje que indica que el mensaje no se debe procesar mediante un filtro de spam debido a que el mensaje fue ya procesan o no es seguro.</span><span class="sxs-lookup"><span data-stu-id="8f776-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f776-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="8f776-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="8f776-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8f776-107">None</span></span>  <br/> |
|<span data-ttu-id="8f776-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8f776-108">Property set:</span></span>  <br/> |<span data-ttu-id="8f776-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="8f776-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="8f776-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="8f776-110">Property name:</span></span>  <br/> |https://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="8f776-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8f776-111">Data type:</span></span>  <br/> |<span data-ttu-id="8f776-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8f776-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8f776-113">Área:</span><span class="sxs-lookup"><span data-stu-id="8f776-113">Area:</span></span>  <br/> |<span data-ttu-id="8f776-114">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="8f776-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f776-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f776-115">Remarks</span></span>

<span data-ttu-id="8f776-116">Esta propiedad se mostrará en todos los mensajes que se desplaza por la regla de correo electrónico no deseado o es en caso contrario, el contenido de confianza.</span><span class="sxs-lookup"><span data-stu-id="8f776-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f776-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f776-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f776-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8f776-118">Protocol specifications</span></span>

<span data-ttu-id="8f776-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f776-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f776-120">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8f776-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f776-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f776-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f776-122">Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="8f776-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="8f776-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f776-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f776-124">Especifica las propiedades y operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="8f776-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f776-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8f776-125">Header files</span></span>

<span data-ttu-id="8f776-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f776-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f776-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8f776-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f776-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f776-128">See also</span></span>



[<span data-ttu-id="8f776-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8f776-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f776-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="8f776-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f776-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8f776-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f776-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="8f776-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

