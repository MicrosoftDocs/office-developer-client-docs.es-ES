---
title: Propiedad canónica PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331860"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a><span data-ttu-id="9f720-103">Propiedad canónica PidTagTransmittableDisplayName</span><span class="sxs-lookup"><span data-stu-id="9f720-103">PidTagTransmittableDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="9f720-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f720-105">Contiene el nombre para mostrar del destinatario en un formulario seguro que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="9f720-105">Contains a recipient's display name in a secure form that cannot be changed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9f720-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9f720-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9f720-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="9f720-107">PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W</span></span>  <br/> |
|<span data-ttu-id="9f720-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9f720-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9f720-109">0x3A20</span><span class="sxs-lookup"><span data-stu-id="9f720-109">0x3A20</span></span>  <br/> |
|<span data-ttu-id="9f720-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9f720-110">Data type:</span></span>  <br/> |<span data-ttu-id="9f720-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9f720-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9f720-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9f720-112">Area:</span></span>  <br/> |<span data-ttu-id="9f720-113">Address</span><span class="sxs-lookup"><span data-stu-id="9f720-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f720-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f720-114">Remarks</span></span>

<span data-ttu-id="9f720-115">Todos los proveedores de libreta de direcciones deben implementar estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9f720-115">These properties should be implemented by all address book providers.</span></span> <span data-ttu-id="9f720-116">Contienen la versión del nombre para mostrar del destinatario que se transmite con el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f720-116">They contain the version of the recipient's display name that is transmitted with the message.</span></span> <span data-ttu-id="9f720-117">Para la mayoría de los proveedores de libreta de direcciones, estas propiedades tienen el mismo valor que la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9f720-117">For most address book providers these properties have the same value as the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="9f720-118">Los proveedores que no tienen un nombre para mostrar seguro devuelven PT_ERROR y MAPI cambian el nombre para mostrar agregando comillas alrededor del nombre.</span><span class="sxs-lookup"><span data-stu-id="9f720-118">Providers that do not have a secure display name return PT_ERROR and MAPI changes the display name by adding quotation marks around the name.</span></span>
  
<span data-ttu-id="9f720-119">Una aplicación cliente puede usar esta propiedad para impedir la alteración o la "imitación" de las entradas.</span><span class="sxs-lookup"><span data-stu-id="9f720-119">A client application can use this property to prevent alteration or "spoofing" of entries.</span></span> <span data-ttu-id="9f720-120">Un ejemplo de suplantación es la transmisión de John Doe como Juan (un chico).</span><span class="sxs-lookup"><span data-stu-id="9f720-120">An example of spoofing is transmitting John Doe as John (What a Guy) Doe.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9f720-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f720-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9f720-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="9f720-122">Protocol specifications</span></span>

<span data-ttu-id="9f720-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f720-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f720-124">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="9f720-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9f720-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f720-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f720-126">Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="9f720-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="9f720-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f720-127">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f720-128">Controla las comunicaciones de un cliente con un servidor de interfaz del proveedor de servicios de nombres (NSPI).</span><span class="sxs-lookup"><span data-stu-id="9f720-128">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="9f720-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f720-129">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f720-130">Controla el orden y el flujo de transferencias de datos entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="9f720-130">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="9f720-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9f720-131">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9f720-132">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9f720-132">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9f720-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9f720-133">Header files</span></span>

<span data-ttu-id="9f720-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9f720-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="9f720-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9f720-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="9f720-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9f720-136">Mapitags.h</span></span>
  
> <span data-ttu-id="9f720-137">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="9f720-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f720-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f720-138">See also</span></span>



[<span data-ttu-id="9f720-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9f720-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9f720-140">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="9f720-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9f720-141">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9f720-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9f720-142">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9f720-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

