---
title: Propiedad canónica PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286463"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="2bdfb-103">Propiedad canónica PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="2bdfb-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="2bdfb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bdfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bdfb-105">Contiene una cadena Unicode que especifica un icono o iconos personalizados que se mostrarán para un proveedor MAPI en la barra de estado de Microsoft Office Outlook en los Estados en línea y sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2bdfb-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="2bdfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2bdfb-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="2bdfb-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="2bdfb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2bdfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2bdfb-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="2bdfb-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="2bdfb-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="2bdfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="2bdfb-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2bdfb-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2bdfb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2bdfb-112">Area:</span></span>  <br/> |<span data-ttu-id="2bdfb-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfb-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2bdfb-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2bdfb-114">Remarks</span></span>

<span data-ttu-id="2bdfb-115">Estas propiedades especifican el archivo de recursos que contiene un icono personalizado que representa un proveedor MAPI en un estado en línea y, opcionalmente, otro icono personalizado en el estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="2bdfb-116">Outlook siempre solicita estas propiedades en representación Unicode.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="2bdfb-117">Por ejemplo, el siguiente valor de propiedad indica a Outlook que debe cargar el identificador de icono 1001 desde el módulo mymod32. dll y usar dicho icono para `mymod32.dll,#1001`el estado de conexión:.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="2bdfb-118">Dado que no hay ningún icono específico del proveedor para el estado sin conexión, en este caso, se usa el icono estándar de Outlook sin conexión en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="2bdfb-119">El siguiente valor de propiedad indica a Outlook que debe cargar el identificador de icono 1001 desde el módulo mymod32. dll y usar dicho icono para el estado en línea, así como cargar el icono identificador 1002 desde el mismo módulo que se va `mymod32.dll,#1001,#1002`a usar para el estado sin conexión:.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="2bdfb-120">No se usa ningún icono de Outlook en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="2bdfb-121">De forma predeterminada, si no se especifican iconos personalizados, el proveedor se representa mediante los iconos predeterminados de Outlook para el estado de conexión y el estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="2bdfb-122">De manera opcional, el proveedor puede especificar un nombre para mostrar que se mostrará junto al icono en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="2bdfb-123">Para obtener más información, vea **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2bdfb-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2bdfb-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2bdfb-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2bdfb-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="2bdfb-125">Header files</span></span>

<span data-ttu-id="2bdfb-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2bdfb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2bdfb-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2bdfb-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2bdfb-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2bdfb-129">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="2bdfb-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2bdfb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bdfb-130">See also</span></span>



[<span data-ttu-id="2bdfb-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2bdfb-132">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2bdfb-133">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="2bdfb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2bdfb-134">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="2bdfb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

