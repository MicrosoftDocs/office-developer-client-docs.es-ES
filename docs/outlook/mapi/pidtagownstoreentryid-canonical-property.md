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
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427377"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="acb70-103">Propiedad canónica PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="acb70-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="acb70-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acb70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acb70-105">Contiene el identificador de entrada del almacén de mensajes estrechamente acoplado de un transporte.</span><span class="sxs-lookup"><span data-stu-id="acb70-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="acb70-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="acb70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acb70-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="acb70-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="acb70-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="acb70-108">Identifier:</span></span>  <br/> |<span data-ttu-id="acb70-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="acb70-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="acb70-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="acb70-110">Data type:</span></span>  <br/> |<span data-ttu-id="acb70-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="acb70-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="acb70-112">Área:</span><span class="sxs-lookup"><span data-stu-id="acb70-112">Area:</span></span>  <br/> |<span data-ttu-id="acb70-113">Propiedades del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="acb70-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb70-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="acb70-114">Remarks</span></span>

<span data-ttu-id="acb70-115">Esta propiedad especifica el identificador de entrada del almacén estrechamente acoplado, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="acb70-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="acb70-116">Por ejemplo, un proveedor de transporte puede especificar el identificador de entrada del almacén de carpetas privadas para que la cola MAPI pueda conectar el proveedor de transporte al almacén.</span><span class="sxs-lookup"><span data-stu-id="acb70-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="acb70-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="acb70-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="acb70-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="acb70-118">Header files</span></span>

<span data-ttu-id="acb70-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acb70-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="acb70-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="acb70-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="acb70-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="acb70-121">Mapitags.h</span></span>
  
> <span data-ttu-id="acb70-122">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="acb70-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acb70-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="acb70-123">See also</span></span>



[<span data-ttu-id="acb70-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="acb70-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="acb70-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="acb70-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="acb70-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="acb70-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="acb70-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="acb70-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

