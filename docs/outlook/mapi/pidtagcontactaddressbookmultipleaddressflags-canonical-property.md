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
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588674"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="57296-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="57296-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="57296-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57296-105">Contiene los indicadores que indica si los proveedores de será compatible con correo electrónico varias direcciones por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="57296-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57296-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="57296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="57296-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="57296-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="57296-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="57296-108">Identifier:</span></span>  <br/> |<span data-ttu-id="57296-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="57296-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="57296-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="57296-110">Data type:</span></span>  <br/> |<span data-ttu-id="57296-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="57296-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="57296-112">Área:</span><span class="sxs-lookup"><span data-stu-id="57296-112">Area:</span></span>  <br/> |<span data-ttu-id="57296-113">Libreta de direcciones de contacto</span><span class="sxs-lookup"><span data-stu-id="57296-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57296-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57296-114">Remarks</span></span>

<span data-ttu-id="57296-115">Si las marcas de esta propiedad están TRUE, el proveedor no incluye contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="57296-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="57296-116">Tendrá en cuenta sólo la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="57296-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="57296-117">Se trata de una propiedad en una sección de perfil de la libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="57296-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="57296-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="57296-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="57296-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="57296-119">Header files</span></span>

<span data-ttu-id="57296-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="57296-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="57296-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="57296-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="57296-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="57296-122">Mapitags.h</span></span>
  
> <span data-ttu-id="57296-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="57296-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57296-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="57296-124">See also</span></span>



[<span data-ttu-id="57296-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="57296-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="57296-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="57296-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="57296-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="57296-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="57296-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="57296-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

