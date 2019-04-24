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
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330068"
---
# <a name="pidtagservicedllname-canonical-property"></a><span data-ttu-id="77318-103">Propiedad canónica PidTagServiceDllName</span><span class="sxs-lookup"><span data-stu-id="77318-103">PidTagServiceDllName Canonical Property</span></span>

  
  
<span data-ttu-id="77318-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77318-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77318-105">Contiene el nombre de archivo del archivo DLL que contiene la función de punto de entrada del proveedor de servicios de mensajes para llamar para la configuración.</span><span class="sxs-lookup"><span data-stu-id="77318-105">Contains the filename of the DLL containing the message service provider entry point function to call for configuration.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77318-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="77318-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77318-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span><span class="sxs-lookup"><span data-stu-id="77318-107">PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W</span></span>  <br/> |
|<span data-ttu-id="77318-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="77318-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77318-109">0x3D0A</span><span class="sxs-lookup"><span data-stu-id="77318-109">0x3D0A</span></span>  <br/> |
|<span data-ttu-id="77318-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="77318-110">Data type:</span></span>  <br/> |<span data-ttu-id="77318-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="77318-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="77318-112">Área:</span><span class="sxs-lookup"><span data-stu-id="77318-112">Area:</span></span>  <br/> |<span data-ttu-id="77318-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="77318-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77318-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77318-114">Remarks</span></span>

<span data-ttu-id="77318-115">Cuando el nombre de la función de punto de entrada aparece en el método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), indica que existe el punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="77318-115">When the entry point function name appears in the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) method, it indicates that the entry point exists.</span></span>
  
<span data-ttu-id="77318-116">MAPI utiliza una Convención de nomenclatura de archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="77318-116">MAPI uses a DLL file naming convention.</span></span> <span data-ttu-id="77318-117">Anexa la cadena 32 al nombre de la DLL base para identificar la versión que se ejecuta en las plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="77318-117">It appends the string 32 to the base DLL name to identify the version that runs on 32-bit platforms.</span></span> <span data-ttu-id="77318-118">Por ejemplo, cuando el nombre MAPI. DLL, MAPI crea el nombre MAPI32. DLL para representar la versión de 32 bits correspondiente del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="77318-118">For example, when the name MAPI.DLL is specified, MAPI constructs the name MAPI32.DLL to represent the corresponding 32-bit version of the DLL.</span></span>
  
<span data-ttu-id="77318-119">Estas propiedades deben especificar el nombre base.</span><span class="sxs-lookup"><span data-stu-id="77318-119">These properties should specify the base name.</span></span> <span data-ttu-id="77318-120">MAPI anexa la cadena 32 según corresponda.</span><span class="sxs-lookup"><span data-stu-id="77318-120">MAPI appends the string 32 as appropriate.</span></span> <span data-ttu-id="77318-121">La inclusión de la cadena 32 como parte de estas propiedades da como resultado un error.</span><span class="sxs-lookup"><span data-stu-id="77318-121">Including the string 32 as part of these properties result in an error.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="77318-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="77318-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="77318-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="77318-123">Header files</span></span>

<span data-ttu-id="77318-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="77318-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="77318-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="77318-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="77318-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="77318-126">Mapitags.h</span></span>
  
> <span data-ttu-id="77318-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="77318-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77318-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="77318-128">See also</span></span>



[<span data-ttu-id="77318-129">Propiedad canónica PidTagProviderDllName</span><span class="sxs-lookup"><span data-stu-id="77318-129">PidTagProviderDllName Canonical Property</span></span>](pidtagproviderdllname-canonical-property.md)


[<span data-ttu-id="77318-130">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="77318-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77318-131">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="77318-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77318-132">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="77318-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77318-133">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="77318-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

