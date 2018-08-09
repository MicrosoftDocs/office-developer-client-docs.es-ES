---
title: Propiedad canónica PidLidFileUnder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aa0a7f958ed1a5ed4140e87e25bd540123616568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818726"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="a3185-103">Propiedad canónica PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="a3185-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="a3185-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a3185-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a3185-105">Especifica el nombre en la que se archiva el contacto al mostrar una lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="a3185-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3185-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="a3185-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3185-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="a3185-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="a3185-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="a3185-108">Property set:</span></span>  <br/> |<span data-ttu-id="a3185-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a3185-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a3185-110">Identificador de tipo Long (LID):</span><span class="sxs-lookup"><span data-stu-id="a3185-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a3185-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="a3185-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="a3185-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="a3185-112">Data type:</span></span>  <br/> |<span data-ttu-id="a3185-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a3185-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a3185-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a3185-114">Area:</span></span>  <br/> |<span data-ttu-id="a3185-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="a3185-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3185-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3185-116">Remarks</span></span>

<span data-ttu-id="a3185-117">La aplicación debe tratar esta propiedad como un PT_UNICODE vacía si se encuentra el contacto.</span><span class="sxs-lookup"><span data-stu-id="a3185-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3185-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3185-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3185-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="a3185-119">Protocol specifications</span></span>

<span data-ttu-id="a3185-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3185-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3185-121">Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a3185-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3185-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3185-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3185-123">Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.</span><span class="sxs-lookup"><span data-stu-id="a3185-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3185-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="a3185-124">Header files</span></span>

<span data-ttu-id="a3185-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3185-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3185-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a3185-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3185-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3185-127">See also</span></span>



[<span data-ttu-id="a3185-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a3185-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3185-129">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="a3185-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3185-130">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="a3185-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3185-131">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="a3185-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

