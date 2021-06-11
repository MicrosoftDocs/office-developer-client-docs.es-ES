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
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417045"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="9af91-103">Propiedad canónica PidTagServiceSupportFiles</span><span class="sxs-lookup"><span data-stu-id="9af91-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="9af91-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9af91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9af91-105">Contiene una lista de los archivos que pertenecen al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9af91-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9af91-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="9af91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9af91-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="9af91-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="9af91-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9af91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9af91-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="9af91-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="9af91-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="9af91-110">Data type:</span></span>  <br/> |<span data-ttu-id="9af91-111">PT_MV_STRING8, PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9af91-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9af91-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9af91-112">Area:</span></span>  <br/> |<span data-ttu-id="9af91-113">Perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="9af91-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9af91-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9af91-114">Remarks</span></span>

<span data-ttu-id="9af91-115">Mediante un cuadro de diálogo en el applet del panel de control, un usuario puede obtener la lista de archivos que pertenecen al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9af91-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="9af91-116">Por ejemplo, el usuario puede obtener los nombres de todas las bibliotecas de vínculos dinámicos (DLL) que pertenecen al servicio.</span><span class="sxs-lookup"><span data-stu-id="9af91-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="9af91-117">A continuación, el usuario puede buscar detalles adicionales sobre los archivos especificados, como los nombres y los números de versión de todas las DLL.</span><span class="sxs-lookup"><span data-stu-id="9af91-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="9af91-118">MAPI usa estas propiedades para crear una lista de archivos de soporte técnico en un cuadro de diálogo para la selección de usuarios de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9af91-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="9af91-119">MAPI solo funciona con nombres de archivo y otras cadenas que se le pasan en el juego de caracteres interfaces de servicio (ANSI) de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9af91-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="9af91-120">Las aplicaciones cliente que usan nombres de archivo en un juego de caracteres del fabricante de equipos originales (OEM) deben convertirlos en ANSI antes de llamar a MAPI.</span><span class="sxs-lookup"><span data-stu-id="9af91-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9af91-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9af91-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9af91-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="9af91-122">Header files</span></span>

<span data-ttu-id="9af91-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9af91-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9af91-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="9af91-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9af91-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9af91-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9af91-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="9af91-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9af91-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9af91-127">See also</span></span>



[<span data-ttu-id="9af91-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9af91-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9af91-129">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9af91-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9af91-130">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="9af91-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9af91-131">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="9af91-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

