---
title: Propiedad canónica PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401506"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="f7d29-103">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="f7d29-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="f7d29-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7d29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7d29-105">Contiene un número que identifica de forma exclusiva los datos adjuntos en su mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="f7d29-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7d29-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="f7d29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7d29-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="f7d29-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="f7d29-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f7d29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7d29-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="f7d29-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="f7d29-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="f7d29-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7d29-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f7d29-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f7d29-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f7d29-112">Area:</span></span>  <br/> |<span data-ttu-id="f7d29-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="f7d29-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7d29-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f7d29-114">Remarks</span></span>

<span data-ttu-id="f7d29-115">Almacenes de mensaje generan y mantienen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f7d29-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="f7d29-116">El número de datos adjuntos es el criterio de ordenación secundario, después de la posición de representación, en la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f7d29-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="f7d29-117">**PR_ATTACH_NUM** se usa para abrir los datos adjuntos con el método [IMessage::OpenAttach](imessage-openattach.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d29-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="f7d29-118">Dentro de la sesión de la aplicación de cliente, la propiedad **PR_ATTACH_NUM** de datos adjuntos del mensaje permanece constante mientras está abierta en la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f7d29-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="f7d29-119">El almacén de mensajes propaga los cambios a la tabla con los métodos **IMessage::CreateAttach** y **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="f7d29-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="f7d29-120">En su opción del almacén de mensajes puede generar notificaciones de tabla en las tablas de datos adjuntos abiertos para que los clientes pueden volver a sincronizar a esos cambios.</span><span class="sxs-lookup"><span data-stu-id="f7d29-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f7d29-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7d29-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7d29-122">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="f7d29-122">Protocol specifications</span></span>

<span data-ttu-id="f7d29-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7d29-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7d29-124">Controla los objetos de mensaje y los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="f7d29-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7d29-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="f7d29-125">Header files</span></span>

<span data-ttu-id="f7d29-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7d29-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7d29-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="f7d29-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7d29-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f7d29-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f7d29-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="f7d29-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7d29-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7d29-130">See also</span></span>



[<span data-ttu-id="f7d29-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d29-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7d29-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="f7d29-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7d29-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="f7d29-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7d29-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="f7d29-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

