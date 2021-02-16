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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327254"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="89d69-103">Propiedad canónica PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="89d69-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="89d69-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89d69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89d69-105">Contiene un número que identifica de forma única los datos adjuntos dentro de su mensaje primario.</span><span class="sxs-lookup"><span data-stu-id="89d69-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89d69-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="89d69-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89d69-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="89d69-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="89d69-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89d69-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89d69-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="89d69-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="89d69-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="89d69-110">Data type:</span></span>  <br/> |<span data-ttu-id="89d69-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="89d69-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="89d69-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89d69-112">Area:</span></span>  <br/> |<span data-ttu-id="89d69-113">Datos adjuntos del mensaje</span><span class="sxs-lookup"><span data-stu-id="89d69-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89d69-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89d69-114">Remarks</span></span>

<span data-ttu-id="89d69-115">Los almacenes de mensajes generan y mantienen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="89d69-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="89d69-116">El número de datos adjuntos es la clave de ordenación secundaria, después de la posición de representación, en la tabla de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="89d69-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="89d69-117">**PR_ATTACH_NUM** se usa para abrir los datos adjuntos con el [método IMessage::OpenAttach.](imessage-openattach.md)</span><span class="sxs-lookup"><span data-stu-id="89d69-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="89d69-118">Dentro de la sesión de una aplicación cliente, la propiedad **PR_ATTACH_NUM** de datos adjuntos de un mensaje permanece constante mientras la tabla de datos adjuntos esté abierta.</span><span class="sxs-lookup"><span data-stu-id="89d69-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="89d69-119">El almacén de mensajes propaga los cambios a la tabla mediante los métodos **IMessage::CreateAttach** e **IMessage::D eleteAttach.**</span><span class="sxs-lookup"><span data-stu-id="89d69-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="89d69-120">En su opción, el almacén de mensajes puede generar notificaciones de tabla en tablas de datos adjuntos abiertas para que los clientes puedan volver a sincronizarse con esos cambios.</span><span class="sxs-lookup"><span data-stu-id="89d69-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="89d69-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89d69-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89d69-122">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="89d69-122">Protocol specifications</span></span>

<span data-ttu-id="89d69-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89d69-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89d69-124">Controla los objetos de mensaje y datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="89d69-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89d69-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="89d69-125">Header files</span></span>

<span data-ttu-id="89d69-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89d69-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="89d69-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="89d69-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="89d69-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89d69-128">Mapitags.h</span></span>
  
> <span data-ttu-id="89d69-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="89d69-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89d69-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89d69-130">See also</span></span>



[<span data-ttu-id="89d69-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89d69-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89d69-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="89d69-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89d69-133">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="89d69-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89d69-134">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="89d69-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

