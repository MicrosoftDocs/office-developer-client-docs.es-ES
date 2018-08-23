---
title: Propiedad canónica PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a315f1564f2980ad16ce2ba3da2308960f7d4b88
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578895"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="5a147-103">Propiedad canónica PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a147-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="5a147-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a147-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a147-105">Contiene TRUE si un perfil de usuario de mensajería es el perfil predeterminado MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a147-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a147-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5a147-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5a147-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="5a147-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="5a147-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5a147-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5a147-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="5a147-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="5a147-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5a147-110">Data type:</span></span>  <br/> |<span data-ttu-id="5a147-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5a147-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5a147-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5a147-112">Area:</span></span>  <br/> |<span data-ttu-id="5a147-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="5a147-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a147-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a147-114">Remarks</span></span>

<span data-ttu-id="5a147-115">Esta propiedad no aparece como una propiedad de cualquier objeto, pero sólo como una columna de una tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="5a147-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="5a147-116">Una aplicación cliente puede usar el método [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) para designar el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5a147-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5a147-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a147-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5a147-118">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5a147-118">Header files</span></span>

<span data-ttu-id="5a147-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a147-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5a147-120">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5a147-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5a147-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5a147-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5a147-122">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="5a147-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a147-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5a147-123">See also</span></span>



[<span data-ttu-id="5a147-124">Propiedad canónica PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="5a147-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="5a147-125">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5a147-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5a147-126">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="5a147-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5a147-127">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5a147-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5a147-128">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="5a147-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

