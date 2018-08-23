---
title: Propiedad canónica PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d2917f2119fde38686397b65956113bc430b2e31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570817"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="1642a-103">Propiedad canónica PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="1642a-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="1642a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1642a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1642a-105">Contiene el nombre de archivo del archivo DLL que contiene la función de punto de entrada de mensaje servicio proveedor para llamar a para la configuración.</span><span class="sxs-lookup"><span data-stu-id="1642a-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1642a-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1642a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1642a-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1642a-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="1642a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1642a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1642a-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="1642a-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="1642a-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1642a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1642a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1642a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1642a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1642a-112">Area:</span></span>  <br/> |<span data-ttu-id="1642a-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1642a-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1642a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1642a-114">Remarks</span></span>

<span data-ttu-id="1642a-115">Cuando el nombre de la función de punto de entrada aparece en el método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), indica que existe el punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1642a-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="1642a-116">MAPI utiliza una convención de nomenclatura del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="1642a-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="1642a-117">El nombre de archivo base contiene hasta seis caracteres que identifican el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="1642a-117">The base filename contains up to six characters that uniquely identify the DLL.</span></span> <span data-ttu-id="1642a-118">MAPI anexa la cadena 32 para el nombre base del archivo DLL para identificar la versión que se ejecuta en plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1642a-118">MAPI appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="1642a-119">Por ejemplo, cuando el nombre de MAPI. Se especifica el archivo DLL, el nombre MAPI32 las construcciones de MAPI. DLL para representar la versión de 32 bits correspondiente de la DLL.</span><span class="sxs-lookup"><span data-stu-id="1642a-119">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="1642a-120">Estas propiedades deben especificar el nombre base.</span><span class="sxs-lookup"><span data-stu-id="1642a-120">These properties should specify the base name.</span></span> <span data-ttu-id="1642a-121">MAPI anexa la cadena 32 según corresponda.</span><span class="sxs-lookup"><span data-stu-id="1642a-121">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="1642a-122">Por ejemplo, la cadena de 32 como parte de estos resultados de las propiedades de un error.</span><span class="sxs-lookup"><span data-stu-id="1642a-122">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1642a-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1642a-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1642a-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1642a-124">Header files</span></span>

<span data-ttu-id="1642a-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1642a-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1642a-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1642a-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="1642a-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1642a-127">Mapitags.h</span></span>
  
> <span data-ttu-id="1642a-128">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1642a-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1642a-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1642a-129">See also</span></span>



[<span data-ttu-id="1642a-130">Propiedad canónica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="1642a-130">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="1642a-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1642a-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1642a-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1642a-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1642a-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1642a-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1642a-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1642a-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

