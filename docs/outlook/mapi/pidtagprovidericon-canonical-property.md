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
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819969"
---
# <a name="pidtagprovidericon-canonical-property"></a><span data-ttu-id="de146-103">Propiedad canónica PidTagProviderIcon</span><span class="sxs-lookup"><span data-stu-id="de146-103">PidTagProviderIcon Canonical Property</span></span>

  
  
<span data-ttu-id="de146-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de146-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de146-105">Contiene una cadena Unicode que especifica un icono personalizado o los iconos que se mostrará para un proveedor de MAPI en la barra de estado de Microsoft Office Outlook en Estados en línea y sin conexión.</span><span class="sxs-lookup"><span data-stu-id="de146-105">Contains a Unicode string that specifies a custom icon or icons to be displayed for a MAPI provider in the Microsoft Office Outlook status bar in both online and offline states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de146-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="de146-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de146-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span><span class="sxs-lookup"><span data-stu-id="de146-107">PR_PROVIDER_ICON, PR_PROVIDER_ICON_W</span></span>  <br/> |
|<span data-ttu-id="de146-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="de146-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de146-109">0x3417</span><span class="sxs-lookup"><span data-stu-id="de146-109">0x3417</span></span>  <br/> |
|<span data-ttu-id="de146-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="de146-110">Data type:</span></span>  <br/> |<span data-ttu-id="de146-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de146-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="de146-112">Área:</span><span class="sxs-lookup"><span data-stu-id="de146-112">Area:</span></span>  <br/> |<span data-ttu-id="de146-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="de146-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de146-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de146-114">Remarks</span></span>

<span data-ttu-id="de146-115">Estas propiedades especifican el archivo de recursos que contiene un icono personalizado que representa un proveedor de MAPI en un estado en línea, y, opcionalmente, otro icono personalizado en el estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="de146-115">These properties specify the resource file that contains a custom icon that represents a MAPI provider in an online state, and optionally, another custom icon in the offline state.</span></span> <span data-ttu-id="de146-116">Outlook siempre solicita estas propiedades en la representación Unicode.</span><span class="sxs-lookup"><span data-stu-id="de146-116">Outlook always requests these properties in Unicode representation.</span></span> 
  
<span data-ttu-id="de146-117">Por ejemplo, el valor de la propiedad siguiente indica a Outlook a cargar icono identificador 1001 desde el módulo mymod32.dll y usar ese icono para el estado en línea: `mymod32.dll,#1001`.</span><span class="sxs-lookup"><span data-stu-id="de146-117">For example, the following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state:  `mymod32.dll,#1001`.</span></span> <span data-ttu-id="de146-118">Dado que no hay ningún icono específicas del proveedor para el estado sin conexión, en este caso, se utiliza el icono estándar de sin conexión de Outlook en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="de146-118">Since there is no provider-specific icon for the offline state, in this case, the standard Outlook offline icon is used in the status bar.</span></span> 
  
<span data-ttu-id="de146-119">El valor de la propiedad siguiente indica a Outlook para cargar el icono identificador 1001 desde el módulo mymod32.dll y usar ese icono para el estado en línea y también cargar icono identificador 1002 desde este mismo módulo que se usará para el estado sin conexión: `mymod32.dll,#1001,#1002`.</span><span class="sxs-lookup"><span data-stu-id="de146-119">The following property value instructs Outlook to load icon ID 1001 from the module mymod32.dll and use that icon for the online state, and to also load icon ID 1002 from this same module to be used for the offline state:  `mymod32.dll,#1001,#1002`.</span></span> <span data-ttu-id="de146-120">No hay icono de Outlook se usa en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="de146-120">No Outlook icon is used in the status bar.</span></span> 
  
<span data-ttu-id="de146-121">De forma predeterminada, si no se especifican ningún iconos personalizados, el proveedor está representado por los iconos de Outlook predeterminado para el estado en línea y el estado sin conexión.</span><span class="sxs-lookup"><span data-stu-id="de146-121">By default, if no custom icons are specified, the provider is represented by the Outlook default icons for the online state and the offline state.</span></span> <span data-ttu-id="de146-122">El proveedor, opcionalmente, puede especificar un nombre para mostrar que se debe mostrar junto al icono en la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="de146-122">The provider can optionally specify a display name to be shown adjacent to the icon in the status bar.</span></span> <span data-ttu-id="de146-123">Para obtener más información, vea **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="de146-123">For more information, see **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de146-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="de146-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="de146-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="de146-125">Header files</span></span>

<span data-ttu-id="de146-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de146-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="de146-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="de146-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="de146-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="de146-128">Mapitags.h</span></span>
  
> <span data-ttu-id="de146-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="de146-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de146-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="de146-130">See also</span></span>



[<span data-ttu-id="de146-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="de146-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de146-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="de146-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de146-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="de146-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de146-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="de146-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
