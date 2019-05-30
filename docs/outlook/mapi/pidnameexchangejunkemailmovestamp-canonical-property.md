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
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540948"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="fdbc0-103">Propiedad canónica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="fdbc0-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="fdbc0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdbc0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdbc0-105">Contiene el valor del mensaje persistente que indica que el mensaje no debe ser procesado por un filtro de correo no deseado porque el mensaje ya se ha procesado o es seguro.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fdbc0-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="fdbc0-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="fdbc0-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fdbc0-107">None</span></span>  <br/> |
|<span data-ttu-id="fdbc0-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="fdbc0-108">Property set:</span></span>  <br/> |<span data-ttu-id="fdbc0-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="fdbc0-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="fdbc0-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="fdbc0-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="fdbc0-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="fdbc0-111">Data type:</span></span>  <br/> |<span data-ttu-id="fdbc0-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fdbc0-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fdbc0-113">Área:</span><span class="sxs-lookup"><span data-stu-id="fdbc0-113">Area:</span></span>  <br/> |<span data-ttu-id="fdbc0-114">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="fdbc0-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fdbc0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdbc0-115">Remarks</span></span>

<span data-ttu-id="fdbc0-116">Esta propiedad se marca en todos los mensajes movidos por la regla de correo electrónico no deseado o en contenido de confianza.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fdbc0-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdbc0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fdbc0-118">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="fdbc0-118">Protocol specifications</span></span>

<span data-ttu-id="fdbc0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdbc0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdbc0-120">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fdbc0-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdbc0-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdbc0-122">Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="fdbc0-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fdbc0-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fdbc0-124">Especifica las propiedades y las operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fdbc0-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="fdbc0-125">Header files</span></span>

<span data-ttu-id="fdbc0-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fdbc0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fdbc0-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="fdbc0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fdbc0-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdbc0-128">See also</span></span>



[<span data-ttu-id="fdbc0-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fdbc0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fdbc0-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="fdbc0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fdbc0-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="fdbc0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fdbc0-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="fdbc0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

