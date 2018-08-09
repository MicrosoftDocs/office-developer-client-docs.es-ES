---
title: Propiedad canónica PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820322"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="13753-103">Propiedad canónica PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="13753-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="13753-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13753-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13753-105">Contiene una lista de los archivos que pertenecen al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13753-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13753-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="13753-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13753-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="13753-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="13753-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13753-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13753-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="13753-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="13753-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="13753-110">Data type:</span></span>  <br/> |<span data-ttu-id="13753-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="13753-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="13753-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13753-112">Area:</span></span>  <br/> |<span data-ttu-id="13753-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="13753-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13753-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13753-114">Remarks</span></span>

<span data-ttu-id="13753-115">Uso de un cuadro de diálogo en el applet de panel de control, un usuario puede obtener la lista de archivos que pertenecen al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13753-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="13753-116">Por ejemplo, el usuario puede obtener los nombres de todas las bibliotecas de vínculos dinámicos (DLL) que pertenecen al servicio.</span><span class="sxs-lookup"><span data-stu-id="13753-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="13753-117">El usuario, a continuación, puede buscar detalles adicionales acerca de los archivos especificados, como los nombres y números de versión de todos los archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="13753-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="13753-118">MAPI utiliza estas propiedades para crear una lista de archivos de soporte técnico en un cuadro de diálogo para la selección del usuario de mensajería.</span><span class="sxs-lookup"><span data-stu-id="13753-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="13753-119">MAPI sólo funciona con los nombres de archivo y otras cadenas pasan a ella, en el juego de caracteres de Interfaces de servicio de Active Directory (ANSI).</span><span class="sxs-lookup"><span data-stu-id="13753-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="13753-120">Las aplicaciones de cliente que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos a ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="13753-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13753-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13753-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="13753-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="13753-122">Header files</span></span>

<span data-ttu-id="13753-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13753-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="13753-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="13753-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="13753-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="13753-125">Mapitags.h</span></span>
  
> <span data-ttu-id="13753-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="13753-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13753-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="13753-127">See also</span></span>



[<span data-ttu-id="13753-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13753-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13753-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="13753-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13753-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="13753-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13753-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="13753-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

