---
title: Propiedad canónica PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a8810b6c39b909ebaa612496824150499cd15165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584845"
---
# <a name="pidtagidentityentryid-canonical-property"></a><span data-ttu-id="4f047-103">Propiedad canónica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="4f047-103">PidTagIdentityEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4f047-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f047-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f047-105">Contiene el identificador de entrada para la identidad de un proveedor de servicios, tal como se define dentro de un sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4f047-105">Contains the entry identifier for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f047-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4f047-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f047-107">PR_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4f047-107">PR_IDENTITY_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4f047-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4f047-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f047-109">0x3E01</span><span class="sxs-lookup"><span data-stu-id="4f047-109">0x3E01</span></span>  <br/> |
|<span data-ttu-id="4f047-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4f047-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f047-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4f047-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4f047-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4f047-112">Area:</span></span>  <br/> |<span data-ttu-id="4f047-113">Estado MAPI</span><span class="sxs-lookup"><span data-stu-id="4f047-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f047-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f047-114">Remarks</span></span>

<span data-ttu-id="4f047-115">Esta propiedad no aparece como una propiedad en cualquier objeto sino sólo como una columna de una tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="4f047-115">This property does not appear as a property on any object but only as a column in a status table.</span></span> <span data-ttu-id="4f047-116">Forma parte de la identidad de la exposición de la fila de la tabla de estado de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="4f047-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="4f047-117">Identidad del proveedor normalmente hace referencia a su cuenta en el servidor, pero puede hacer referencia a cualquier representación que el proveedor define dentro del sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="4f047-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="4f047-118">Esta propiedad se establece normalmente en el identificador de entrada de la libreta de direcciones adecuado.</span><span class="sxs-lookup"><span data-stu-id="4f047-118">This proprerty is commonly set to the appropriate address book entry identifier.</span></span> 
  
<span data-ttu-id="4f047-119">Debe proporcionar un proveedor de servicios de suministro de cualquiera de las propiedades de identidad todos ellos.</span><span class="sxs-lookup"><span data-stu-id="4f047-119">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="4f047-120">Los proveedores que pertenecen al mismo servicio de mensajes deben exponer los mismos valores para las propiedades de identidad.</span><span class="sxs-lookup"><span data-stu-id="4f047-120">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f047-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f047-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f047-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4f047-122">Header files</span></span>

<span data-ttu-id="4f047-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f047-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f047-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4f047-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f047-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f047-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4f047-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="4f047-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f047-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="4f047-127">See also</span></span>



[<span data-ttu-id="4f047-128">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="4f047-128">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="4f047-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f047-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f047-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="4f047-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f047-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4f047-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f047-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="4f047-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

