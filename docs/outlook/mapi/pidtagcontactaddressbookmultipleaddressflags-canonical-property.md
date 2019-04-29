---
title: Propiedad canónica PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429253"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="4a277-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="4a277-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="4a277-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a277-105">Contiene marcadores que indican si los proveedores admitirán varias direcciones de correo electrónico por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="4a277-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a277-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4a277-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a277-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4a277-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="4a277-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a277-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a277-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="4a277-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="4a277-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4a277-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a277-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="4a277-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="4a277-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a277-112">Area:</span></span>  <br/> |<span data-ttu-id="4a277-113">Libreta de direcciones de contacto</span><span class="sxs-lookup"><span data-stu-id="4a277-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a277-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a277-114">Remarks</span></span>

<span data-ttu-id="4a277-115">Si los indicadores de esta propiedad son TRUE, el proveedor no incluye los contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4a277-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="4a277-116">Solo se respetará la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="4a277-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="4a277-117">Se trata de una propiedad de una sección de Perfil de la libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="4a277-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a277-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a277-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4a277-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4a277-119">Header files</span></span>

<span data-ttu-id="4a277-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a277-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a277-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4a277-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a277-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4a277-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4a277-123">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4a277-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a277-124">Ver también</span><span class="sxs-lookup"><span data-stu-id="4a277-124">See also</span></span>



[<span data-ttu-id="4a277-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a277-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a277-126">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4a277-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a277-127">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4a277-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a277-128">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4a277-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

