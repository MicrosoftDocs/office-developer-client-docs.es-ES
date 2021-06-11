---
title: Propiedad canónica PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319708"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="3cf49-103">Propiedad canónica PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="3cf49-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="3cf49-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cf49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cf49-105">Especifica el conjunto de caracteres usado para este contacto.</span><span class="sxs-lookup"><span data-stu-id="3cf49-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3cf49-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="3cf49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cf49-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="3cf49-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="3cf49-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="3cf49-108">Property set:</span></span>  <br/> |<span data-ttu-id="3cf49-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3cf49-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3cf49-110">Id. largo (LID):</span><span class="sxs-lookup"><span data-stu-id="3cf49-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3cf49-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="3cf49-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="3cf49-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="3cf49-112">Data type:</span></span>  <br/> |<span data-ttu-id="3cf49-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3cf49-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3cf49-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3cf49-114">Area:</span></span>  <br/> |<span data-ttu-id="3cf49-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="3cf49-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cf49-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cf49-116">Remarks</span></span>

<span data-ttu-id="3cf49-117">Las aplicaciones pueden usar esta propiedad para ayudar a generar una lista dependiente del conjunto de caracteres de opciones para las propiedades **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) y **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3cf49-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="3cf49-118">Si el valor de la propiedad es "0x00000000" o "0x00000001", las aplicaciones deben tratar la propiedad como no establecida.</span><span class="sxs-lookup"><span data-stu-id="3cf49-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3cf49-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3cf49-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cf49-120">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="3cf49-120">Protocol specifications</span></span>

<span data-ttu-id="3cf49-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf49-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf49-122">Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="3cf49-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3cf49-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cf49-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cf49-124">Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="3cf49-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cf49-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="3cf49-125">Header files</span></span>

<span data-ttu-id="3cf49-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cf49-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cf49-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="3cf49-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cf49-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cf49-128">See also</span></span>



[<span data-ttu-id="3cf49-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf49-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cf49-130">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf49-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cf49-131">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="3cf49-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cf49-132">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="3cf49-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

