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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336326"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="78832-103">Propiedad canónica PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="78832-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="78832-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78832-105">Contiene una cadena Unicode que se consulta en el contenido de los datos adjuntos del almacén.</span><span class="sxs-lookup"><span data-stu-id="78832-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="78832-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="78832-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78832-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="78832-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="78832-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="78832-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78832-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="78832-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="78832-110">Tipo de propiedad:</span><span class="sxs-lookup"><span data-stu-id="78832-110">Property type:</span></span>  <br/> |<span data-ttu-id="78832-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78832-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="78832-112">Área:</span><span class="sxs-lookup"><span data-stu-id="78832-112">Area:</span></span>  <br/> |<span data-ttu-id="78832-113">Buscar </span><span class="sxs-lookup"><span data-stu-id="78832-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="78832-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="78832-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="78832-115">Esta etiqueta de restricción de MAPI, que se usa cuando se busca contenido de datos adjuntos, puede que no esté definida en el archivo de encabezado descargable que tiene actualmente.</span><span class="sxs-lookup"><span data-stu-id="78832-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="78832-116">Puede agregarlo al código con el siguiente valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="78832-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="78832-117">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="78832-117">Protocol specifications</span></span>

<span data-ttu-id="78832-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78832-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78832-119">Proporciona referencias a especificaciones del Protocolo de Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="78832-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="78832-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="78832-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="78832-121">Especifica las propiedades y operaciones para manipular una configuración de lista de carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="78832-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="78832-122">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="78832-122">Header files</span></span>

<span data-ttu-id="78832-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="78832-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="78832-124">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="78832-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="78832-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="78832-125">Mapitags.h</span></span>
  
> <span data-ttu-id="78832-126">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="78832-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78832-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="78832-127">See also</span></span>



[<span data-ttu-id="78832-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="78832-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78832-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="78832-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78832-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="78832-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78832-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="78832-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

