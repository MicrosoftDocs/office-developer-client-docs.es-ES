---
title: Propiedad canónico PidTagProviderDllName
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819965"
---
# <a name="pidtagproviderdllname-canonical-property"></a><span data-ttu-id="ad779-103">Propiedad canónico PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="ad779-103">PidTagProviderDllName Canonical Property</span></span>

  
  
<span data-ttu-id="ad779-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad779-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad779-105">Contiene el nombre de archivo de base de la biblioteca de vínculos dinámicos de proveedor de servicio MAPI (DLL).</span><span class="sxs-lookup"><span data-stu-id="ad779-105">Contains the base file name of the MAPI service provider dynamic-link library (DLL).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad779-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="ad779-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad779-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="ad779-107">PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="ad779-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad779-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad779-109">0x300A</span><span class="sxs-lookup"><span data-stu-id="ad779-109">0x300A</span></span>  <br/> |
|<span data-ttu-id="ad779-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ad779-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad779-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad779-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ad779-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad779-112">Area:</span></span>  <br/> |<span data-ttu-id="ad779-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="ad779-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad779-114">Notas</span><span class="sxs-lookup"><span data-stu-id="ad779-114">Remarks</span></span>

<span data-ttu-id="ad779-115">MAPI utiliza una convención de nomenclatura del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="ad779-115">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="ad779-116">El nombre de archivo base contiene hasta seis caracteres que identifican el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="ad779-116">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="ad779-117">MAPI anexa la cadena 32 para el nombre base del archivo DLL para identificar la versión que se ejecuta en plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ad779-117">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="ad779-118">Por ejemplo, cuando el nombre de MAPI. Se especifica el archivo DLL, el nombre MAPI32 las construcciones de MAPI. DLL para representar la versión de 32 bits correspondiente de la DLL.</span><span class="sxs-lookup"><span data-stu-id="ad779-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="ad779-119">Estas propiedades deben especificar el nombre base.</span><span class="sxs-lookup"><span data-stu-id="ad779-119">These properties should specify the base name.</span></span> <span data-ttu-id="ad779-120">MAPI anexa la cadena 32 según corresponda.</span><span class="sxs-lookup"><span data-stu-id="ad779-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="ad779-121">Por ejemplo, la cadena de 32 como parte de este los resultados de la propiedad en un error.</span><span class="sxs-lookup"><span data-stu-id="ad779-121">Including the string 32 as part of this property results in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ad779-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad779-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ad779-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="ad779-123">Header files</span></span>

<span data-ttu-id="ad779-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ad779-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad779-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ad779-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad779-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ad779-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ad779-127">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="ad779-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad779-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="ad779-128">See also</span></span>



[<span data-ttu-id="ad779-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad779-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad779-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="ad779-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad779-131">Asignación de nombres de propiedad canónico a nombres de MAPI</span><span class="sxs-lookup"><span data-stu-id="ad779-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad779-132">Asignación de nombres MAPI para nombres canónicos (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ad779-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

