---
title: Propiedad canónica PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382837"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="cb48e-103">Propiedad canónica PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="cb48e-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="cb48e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb48e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb48e-105">Contiene una cadena Unicode que se va a consultar en el contenido de los datos adjuntos en el almacén.</span><span class="sxs-lookup"><span data-stu-id="cb48e-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="cb48e-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="cb48e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb48e-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="cb48e-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="cb48e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb48e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cb48e-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="cb48e-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="cb48e-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="cb48e-110">Property type:</span></span>  <br/> |<span data-ttu-id="cb48e-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb48e-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cb48e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="cb48e-112">Area:</span></span>  <br/> |<span data-ttu-id="cb48e-113">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="cb48e-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cb48e-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb48e-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="cb48e-115">Esta etiqueta de restricción MAPI, que se usa cuando se busca el contenido de los datos adjuntos, no puede definirse en el archivo de encabezado descargables que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="cb48e-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="cb48e-116">Puede agregar a su código con el siguiente valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="cb48e-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="cb48e-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="cb48e-117">Protocol specifications</span></span>

<span data-ttu-id="cb48e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb48e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb48e-119">Proporciona referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="cb48e-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb48e-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb48e-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb48e-121">Especifica las propiedades y operaciones para manipular la configuración de la lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cb48e-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb48e-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="cb48e-122">Header files</span></span>

<span data-ttu-id="cb48e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb48e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb48e-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="cb48e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="cb48e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cb48e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="cb48e-126">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="cb48e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb48e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb48e-127">See also</span></span>



[<span data-ttu-id="cb48e-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cb48e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb48e-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="cb48e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb48e-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="cb48e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb48e-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="cb48e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

