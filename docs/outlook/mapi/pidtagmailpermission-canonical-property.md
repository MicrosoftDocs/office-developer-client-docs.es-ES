---
title: Propiedad canónica PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430178"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="4f567-103">Propiedad canónica PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="4f567-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="4f567-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f567-105">Contiene TRUE si el usuario de mensajería tiene permiso para enviar y recibir mensajes.</span><span class="sxs-lookup"><span data-stu-id="4f567-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f567-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="4f567-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f567-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="4f567-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="4f567-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4f567-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f567-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="4f567-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="4f567-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="4f567-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f567-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4f567-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4f567-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4f567-112">Area:</span></span>  <br/> |<span data-ttu-id="4f567-113">Address</span><span class="sxs-lookup"><span data-stu-id="4f567-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f567-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f567-114">Remarks</span></span>

<span data-ttu-id="4f567-115">Si no se establece esta propiedad, MAPI la trata como si fuera un valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="4f567-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="4f567-116">Establezca esta propiedad en FALSE en un directorio corporativo donde algunas de las entradas no están habilitadas para correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4f567-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f567-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f567-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f567-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="4f567-118">Header files</span></span>

<span data-ttu-id="4f567-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4f567-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f567-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="4f567-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f567-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4f567-121">Mapitags.h</span></span>
  
> <span data-ttu-id="4f567-122">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="4f567-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f567-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4f567-123">See also</span></span>



[<span data-ttu-id="4f567-124">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f567-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f567-125">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="4f567-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f567-126">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="4f567-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f567-127">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="4f567-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

