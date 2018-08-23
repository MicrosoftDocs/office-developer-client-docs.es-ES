---
title: Propiedad canónica PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b79b40a59a2bf7b68c58bffbccca04034b853a15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570208"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="b5d11-103">Propiedad canónica PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="b5d11-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="b5d11-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5d11-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5d11-105">Especifica los indicadores de configuración para una tabla de almacenamiento de información personal (archivos .pst).</span><span class="sxs-lookup"><span data-stu-id="b5d11-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5d11-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="b5d11-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5d11-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="b5d11-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b5d11-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b5d11-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5d11-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="b5d11-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="b5d11-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="b5d11-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5d11-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5d11-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5d11-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b5d11-112">Area:</span></span>  <br/> |<span data-ttu-id="b5d11-113">Tabla de almacenamiento personal (.pst) interno</span><span class="sxs-lookup"><span data-stu-id="b5d11-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5d11-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b5d11-114">Remarks</span></span>

<span data-ttu-id="b5d11-115">Las siguientes son valores válidos para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="b5d11-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="b5d11-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b5d11-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="b5d11-117">Indica un archivo .pst Unicode.</span><span class="sxs-lookup"><span data-stu-id="b5d11-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="b5d11-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="b5d11-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="b5d11-119">Cuando set desde el cliente de marcas para el método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , **ConfigureMsgService** la trata como una llamada de [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) y omite la "este servicio de información no se ha configurado" advertencia.</span><span class="sxs-lookup"><span data-stu-id="b5d11-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="b5d11-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="b5d11-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="b5d11-121">Indica a **ConfigureMsgService** para no cambiar el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), incluso aunque lo suministró.</span><span class="sxs-lookup"><span data-stu-id="b5d11-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="b5d11-122">En ese caso, que ha proporcionado únicamente para los nuevos archivos pst.</span><span class="sxs-lookup"><span data-stu-id="b5d11-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="b5d11-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="b5d11-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="b5d11-124">Indica el código de configuración al primer para mostrar un cuadro de diálogo para confirmar si un archivo de carpetas sin conexión (.ost) se ha encontrado y, según la respuesta del usuario, o bien usar la carpeta que se encuentra sin conexión o habilitar al usuario para buscar otra carpeta sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b5d11-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="b5d11-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="b5d11-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="b5d11-126">Copia el archivo .ost con un nuevo nombre único y descarta el nombre actual.</span><span class="sxs-lookup"><span data-stu-id="b5d11-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="b5d11-127">El archivo .ost existente permanece en el equipo, pero ya no se usa en este perfil.</span><span class="sxs-lookup"><span data-stu-id="b5d11-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="b5d11-128">Normalmente, esto se produce cuando Microsoft Outlook ya no se permite un archivo .ost determinado y las directivas del registro no permitir al usuario que cambie el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="b5d11-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="b5d11-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5d11-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5d11-130">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="b5d11-130">Protocol specifications</span></span>

<span data-ttu-id="b5d11-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="b5d11-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b5d11-132">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b5d11-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5d11-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="b5d11-133">Header files</span></span>

<span data-ttu-id="b5d11-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5d11-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5d11-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="b5d11-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5d11-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5d11-136">Mapitags.h</span></span>
  
> <span data-ttu-id="b5d11-137">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="b5d11-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5d11-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b5d11-138">See also</span></span>



[<span data-ttu-id="b5d11-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d11-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5d11-140">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="b5d11-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5d11-141">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="b5d11-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5d11-142">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="b5d11-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

