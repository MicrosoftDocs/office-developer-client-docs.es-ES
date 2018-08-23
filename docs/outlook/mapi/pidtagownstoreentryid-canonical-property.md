---
title: Propiedad canónica PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 54014ab25d268c161465349b4e33c6a1df19f140
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591704"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="f7152-103">Propiedad canónica PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="f7152-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f7152-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7152-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7152-105">Contiene el identificador de entrada acoplado de un transporte almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f7152-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7152-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7152-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7152-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f7152-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f7152-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7152-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7152-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="f7152-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="f7152-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7152-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7152-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f7152-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f7152-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7152-112">Area:</span></span>  <br/> |<span data-ttu-id="f7152-113">Propiedades de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="f7152-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7152-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7152-114">Remarks</span></span>

<span data-ttu-id="f7152-115">Esta propiedad especifica el identificador de entrada para el almacén de acoplamiento ajustado, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="f7152-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="f7152-116">Por ejemplo, un proveedor de transporte puede especificar la carpeta privada almacenar el identificador de entrada para que la cola MAPI puede conectar el proveedor de transporte para el almacén.</span><span class="sxs-lookup"><span data-stu-id="f7152-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f7152-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7152-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f7152-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7152-118">Header files</span></span>

<span data-ttu-id="f7152-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7152-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7152-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7152-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7152-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7152-121">Mapitags.h</span></span>
  
> <span data-ttu-id="f7152-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="f7152-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7152-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f7152-123">See also</span></span>



[<span data-ttu-id="f7152-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7152-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7152-125">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f7152-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7152-126">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7152-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7152-127">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f7152-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

