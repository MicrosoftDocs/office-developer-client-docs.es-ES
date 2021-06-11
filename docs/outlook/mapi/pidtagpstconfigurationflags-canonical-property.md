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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408946"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="e40c0-103">Propiedad canónica PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="e40c0-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="e40c0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e40c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e40c0-105">Especifica las marcas de configuración de una tabla de almacenamiento personal (archivo .pst).</span><span class="sxs-lookup"><span data-stu-id="e40c0-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e40c0-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e40c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e40c0-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="e40c0-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e40c0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e40c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e40c0-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="e40c0-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="e40c0-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e40c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="e40c0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e40c0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e40c0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e40c0-112">Area:</span></span>  <br/> |<span data-ttu-id="e40c0-113">Tabla de almacenamiento personal (.pst) interna</span><span class="sxs-lookup"><span data-stu-id="e40c0-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e40c0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e40c0-114">Remarks</span></span>

<span data-ttu-id="e40c0-115">Los siguientes son valores válidos para esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="e40c0-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="e40c0-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e40c0-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="e40c0-117">Indica un archivo .pst Unicode.</span><span class="sxs-lookup"><span data-stu-id="e40c0-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="e40c0-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="e40c0-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="e40c0-119">Cuando se establece de las marcas de cliente al método [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) **trata ConfigureMsgService** como una llamada [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) y omite la advertencia "Este servicio de información no se ha configurado".</span><span class="sxs-lookup"><span data-stu-id="e40c0-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="e40c0-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="e40c0-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="e40c0-121">Indica **a ConfigureMsgService** que no cambie el valor de la propiedad **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), aunque se haya proporcionado.</span><span class="sxs-lookup"><span data-stu-id="e40c0-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="e40c0-122">En ese caso, solo se suministró para los nuevos archivos .pst.</span><span class="sxs-lookup"><span data-stu-id="e40c0-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="e40c0-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="e40c0-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="e40c0-124">Indica al código de configuración que primero muestre un cuadro de diálogo para confirmar si se encontró un archivo de carpeta sin conexión (.ost) y, según la respuesta del usuario, use la carpeta sin conexión encontrada o habilite al usuario para buscar otra carpeta sin conexión.</span><span class="sxs-lookup"><span data-stu-id="e40c0-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="e40c0-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="e40c0-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="e40c0-126">Copia el archivo .ost con un nuevo nombre único y descarta el nombre actual.</span><span class="sxs-lookup"><span data-stu-id="e40c0-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="e40c0-127">El archivo .ost existente permanece en el equipo, pero ya no se usa en este perfil.</span><span class="sxs-lookup"><span data-stu-id="e40c0-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="e40c0-128">Esto suele ocurrir cuando Microsoft Outlook permite un archivo .ost determinado y las directivas del Registro no permiten al usuario cambiar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="e40c0-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="e40c0-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e40c0-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e40c0-130">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="e40c0-130">Protocol specifications</span></span>

<span data-ttu-id="e40c0-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="e40c0-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="e40c0-132">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="e40c0-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e40c0-133">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e40c0-133">Header files</span></span>

<span data-ttu-id="e40c0-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e40c0-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="e40c0-135">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e40c0-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="e40c0-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e40c0-136">Mapitags.h</span></span>
  
> <span data-ttu-id="e40c0-137">Contiene definiciones de propiedades enumeradas como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="e40c0-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e40c0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e40c0-138">See also</span></span>



[<span data-ttu-id="e40c0-139">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e40c0-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e40c0-140">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e40c0-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e40c0-141">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e40c0-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e40c0-142">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="e40c0-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

