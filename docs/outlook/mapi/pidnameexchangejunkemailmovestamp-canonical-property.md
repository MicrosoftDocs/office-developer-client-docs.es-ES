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
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="4d705-103">Propiedad canónica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="4d705-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="4d705-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d705-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d705-105">Contiene el valor de mensaje persistente que indica que un filtro de correo no deseado no debe procesar el mensaje porque el mensaje ya se ha procesado o es seguro.</span><span class="sxs-lookup"><span data-stu-id="4d705-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d705-106">Nombres descriptivos:</span><span class="sxs-lookup"><span data-stu-id="4d705-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="4d705-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4d705-107">None</span></span>  <br/> |
|<span data-ttu-id="4d705-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="4d705-108">Property set:</span></span>  <br/> |<span data-ttu-id="4d705-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="4d705-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="4d705-110">Nombre de la propiedad:</span><span class="sxs-lookup"><span data-stu-id="4d705-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="4d705-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4d705-111">Data type:</span></span>  <br/> |<span data-ttu-id="4d705-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4d705-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4d705-113">Área:</span><span class="sxs-lookup"><span data-stu-id="4d705-113">Area:</span></span>  <br/> |<span data-ttu-id="4d705-114">Mensajería segura</span><span class="sxs-lookup"><span data-stu-id="4d705-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d705-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d705-115">Remarks</span></span>

<span data-ttu-id="4d705-116">Esta propiedad se marca en todos los mensajes que se mueven mediante la regla de correo electrónico no deseado o que son contenido de confianza.</span><span class="sxs-lookup"><span data-stu-id="4d705-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d705-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d705-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d705-118">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="4d705-118">Protocol specifications</span></span>

<span data-ttu-id="4d705-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d705-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d705-120">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="4d705-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d705-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d705-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d705-122">Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.</span><span class="sxs-lookup"><span data-stu-id="4d705-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="4d705-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d705-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d705-124">Especifica las propiedades y las operaciones que representan elementos RSS.</span><span class="sxs-lookup"><span data-stu-id="4d705-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d705-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4d705-125">Header files</span></span>

<span data-ttu-id="4d705-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d705-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d705-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4d705-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d705-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d705-128">See also</span></span>



[<span data-ttu-id="4d705-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d705-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d705-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4d705-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d705-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4d705-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d705-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4d705-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

