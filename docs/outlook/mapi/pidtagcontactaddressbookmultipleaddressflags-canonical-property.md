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
ms.openlocfilehash: fbe955d3e7a509edf6ba10678e1e2538c9185193
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819316"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a><span data-ttu-id="63f9a-103">Propiedad canónica PidTagContactAddressBookMultipleAddressFlags</span><span class="sxs-lookup"><span data-stu-id="63f9a-103">PidTagContactAddressBookMultipleAddressFlags Canonical Property</span></span>

  
  
<span data-ttu-id="63f9a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63f9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63f9a-105">Contiene los indicadores que indica si los proveedores de será compatible con correo electrónico varias direcciones por elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="63f9a-105">Contains flags that indicating whether the providers will support multiple email addresses per contact item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63f9a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="63f9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63f9a-107">PR_CONTAB_MULTI_ADDR_FLAGS</span><span class="sxs-lookup"><span data-stu-id="63f9a-107">PR_CONTAB_MULTI_ADDR_FLAGS</span></span>  <br/> |
|<span data-ttu-id="63f9a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="63f9a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63f9a-109">0x6625</span><span class="sxs-lookup"><span data-stu-id="63f9a-109">0x6625</span></span>  <br/> |
|<span data-ttu-id="63f9a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="63f9a-110">Data type:</span></span>  <br/> |<span data-ttu-id="63f9a-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="63f9a-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="63f9a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="63f9a-112">Area:</span></span>  <br/> |<span data-ttu-id="63f9a-113">Libreta de direcciones de contacto</span><span class="sxs-lookup"><span data-stu-id="63f9a-113">Contact address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63f9a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63f9a-114">Remarks</span></span>

<span data-ttu-id="63f9a-115">Si las marcas de esta propiedad están TRUE, el proveedor no incluye contactos sin direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="63f9a-115">If the flags in this property are TRUE, the provider does not include contacts without email addresses.</span></span> <span data-ttu-id="63f9a-116">Tendrá en cuenta sólo la dirección de correo electrónico principal.</span><span class="sxs-lookup"><span data-stu-id="63f9a-116">Only the primary email address will be honored.</span></span> <span data-ttu-id="63f9a-117">Se trata de una propiedad en una sección de perfil de la libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="63f9a-117">This is a property on a Contact Address Book profile section.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="63f9a-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="63f9a-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="63f9a-119">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="63f9a-119">Header files</span></span>

<span data-ttu-id="63f9a-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63f9a-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="63f9a-121">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="63f9a-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="63f9a-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63f9a-122">Mapitags.h</span></span>
  
> <span data-ttu-id="63f9a-123">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="63f9a-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63f9a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="63f9a-124">See also</span></span>



[<span data-ttu-id="63f9a-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="63f9a-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63f9a-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="63f9a-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63f9a-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="63f9a-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63f9a-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="63f9a-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

