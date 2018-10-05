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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384867"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="51838-103">Propiedad canónica PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="51838-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="51838-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51838-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51838-105">Especifica el juego de caracteres utilizado para este contacto.</span><span class="sxs-lookup"><span data-stu-id="51838-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51838-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="51838-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51838-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="51838-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="51838-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="51838-108">Property set:</span></span>  <br/> |<span data-ttu-id="51838-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="51838-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="51838-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="51838-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51838-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="51838-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="51838-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="51838-112">Data type:</span></span>  <br/> |<span data-ttu-id="51838-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51838-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51838-114">Área:</span><span class="sxs-lookup"><span data-stu-id="51838-114">Area:</span></span>  <br/> |<span data-ttu-id="51838-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="51838-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51838-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51838-116">Remarks</span></span>

<span data-ttu-id="51838-117">Las aplicaciones pueden usar esta propiedad para facilitar la generación de una lista dependiente de juego de caracteres de opciones de **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) y \*\*dispidFileUnderId \*\*Propiedades ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="51838-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="51838-118">Si el valor de la propiedad es "0 x 00000000" o "0 x 00000001", las aplicaciones deben tratar la propiedad como no está establecido.</span><span class="sxs-lookup"><span data-stu-id="51838-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51838-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="51838-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51838-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="51838-120">Protocol specifications</span></span>

<span data-ttu-id="51838-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51838-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51838-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="51838-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51838-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51838-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51838-124">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="51838-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51838-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="51838-125">Header files</span></span>

<span data-ttu-id="51838-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51838-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="51838-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="51838-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51838-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="51838-128">See also</span></span>



[<span data-ttu-id="51838-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="51838-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51838-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="51838-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51838-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="51838-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51838-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="51838-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

