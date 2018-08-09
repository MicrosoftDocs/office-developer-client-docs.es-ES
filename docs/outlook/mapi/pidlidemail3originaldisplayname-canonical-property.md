---
title: Propiedad canónica PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ac90910e143d05c17b73aa6a1062cd0999b0d3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818660"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="e1fd2-103">Propiedad canónica PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="e1fd2-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="e1fd2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1fd2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1fd2-105">Especifica el nombre para mostrar de terceros que corresponde a la dirección de correo electrónico que se especifica para el contacto.</span><span class="sxs-lookup"><span data-stu-id="e1fd2-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1fd2-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="e1fd2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1fd2-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="e1fd2-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="e1fd2-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="e1fd2-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1fd2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="e1fd2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="e1fd2-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="e1fd2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e1fd2-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="e1fd2-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="e1fd2-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="e1fd2-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1fd2-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1fd2-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e1fd2-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e1fd2-114">Area:</span></span>  <br/> |<span data-ttu-id="e1fd2-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="e1fd2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1fd2-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1fd2-116">Remarks</span></span>

<span data-ttu-id="e1fd2-117">Si el valor de la propiedad **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) es "SMTP", el valor de la propiedad respectivos **dispidEmail3OriginalDisplayName** debe ser igual que el valor de la **respectivos dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1fd2-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="e1fd2-118">El propósito de esta propiedad es mostrar una dirección alternativa fáciles de usar que es equivalente a la de la **dispidEmail3EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="e1fd2-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e1fd2-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1fd2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1fd2-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="e1fd2-120">Protocol specifications</span></span>

<span data-ttu-id="e1fd2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1fd2-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1fd2-122">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e1fd2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1fd2-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1fd2-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1fd2-124">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="e1fd2-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1fd2-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="e1fd2-125">Header files</span></span>

<span data-ttu-id="e1fd2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1fd2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1fd2-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="e1fd2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1fd2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1fd2-128">See also</span></span>



[<span data-ttu-id="e1fd2-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e1fd2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1fd2-130">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="e1fd2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1fd2-131">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="e1fd2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1fd2-132">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="e1fd2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

