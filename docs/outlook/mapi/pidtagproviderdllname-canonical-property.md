---
title: Propiedad canónica PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286491"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="2fb73-103">Propiedad canónica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="2fb73-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="2fb73-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fb73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fb73-105">Contiene el nombre de archivo base de la biblioteca de vínculos dinámicos (DLL) del proveedor de servicios MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fb73-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2fb73-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2fb73-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fb73-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="2fb73-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="2fb73-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2fb73-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fb73-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="2fb73-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="2fb73-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2fb73-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fb73-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2fb73-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2fb73-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2fb73-112">Area:</span></span>  <br/> |<span data-ttu-id="2fb73-113">MAPI común</span><span class="sxs-lookup"><span data-stu-id="2fb73-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fb73-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2fb73-114">Remarks</span></span>

<span data-ttu-id="2fb73-115">MAPI usa una convención de nomenclatura de archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="2fb73-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="2fb73-116">Anexa la cadena 32 al nombre de DLL base para identificar la versión que se ejecuta en plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2fb73-116">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="2fb73-117">Por ejemplo, cuando se especifica MAPI.DLL nombre, MAPI construye el nombre MAPI32.DLL para representar la versión de 32 bits correspondiente de la DLL.</span><span class="sxs-lookup"><span data-stu-id="2fb73-117">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="2fb73-118">Estas propiedades deben especificar el nombre base.</span><span class="sxs-lookup"><span data-stu-id="2fb73-118">These properties should specify the base name.</span></span> <span data-ttu-id="2fb73-119">MAPI anexa la cadena 32 según corresponda.</span><span class="sxs-lookup"><span data-stu-id="2fb73-119">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="2fb73-120">Si se incluye la cadena 32 como parte de esta propiedad, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="2fb73-120">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2fb73-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fb73-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2fb73-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2fb73-122">Header files</span></span>

<span data-ttu-id="2fb73-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fb73-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fb73-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2fb73-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fb73-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2fb73-125">Mapitags.h</span></span>
  
> <span data-ttu-id="2fb73-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2fb73-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fb73-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fb73-127">See also</span></span>



[<span data-ttu-id="2fb73-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2fb73-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fb73-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2fb73-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fb73-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2fb73-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fb73-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2fb73-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

