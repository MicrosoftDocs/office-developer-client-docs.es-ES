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
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359573"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="8df70-103">Propiedad canónica PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="8df70-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="8df70-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8df70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8df70-105">Especifica el nombre con el que se archivó el contacto al mostrar una lista de contactos.</span><span class="sxs-lookup"><span data-stu-id="8df70-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8df70-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="8df70-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8df70-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="8df70-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="8df70-108">Conjunto de propiedades:</span><span class="sxs-lookup"><span data-stu-id="8df70-108">Property set:</span></span>  <br/> |<span data-ttu-id="8df70-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="8df70-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="8df70-110">IDENTIFICADOR largo (LID):</span><span class="sxs-lookup"><span data-stu-id="8df70-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8df70-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="8df70-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="8df70-112">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="8df70-112">Data type:</span></span>  <br/> |<span data-ttu-id="8df70-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8df70-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8df70-114">Área:</span><span class="sxs-lookup"><span data-stu-id="8df70-114">Area:</span></span>  <br/> |<span data-ttu-id="8df70-115">Contact</span><span class="sxs-lookup"><span data-stu-id="8df70-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8df70-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8df70-116">Remarks</span></span>

<span data-ttu-id="8df70-117">La aplicación debe tratar esta propiedad como un PT_UNICODE vacío si falta en el contacto.</span><span class="sxs-lookup"><span data-stu-id="8df70-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8df70-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8df70-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8df70-119">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="8df70-119">Protocol specifications</span></span>

<span data-ttu-id="8df70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df70-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df70-121">Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="8df70-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8df70-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8df70-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8df70-123">Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.</span><span class="sxs-lookup"><span data-stu-id="8df70-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8df70-124">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="8df70-124">Header files</span></span>

<span data-ttu-id="8df70-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8df70-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8df70-126">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="8df70-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8df70-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8df70-127">See also</span></span>



[<span data-ttu-id="8df70-128">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8df70-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8df70-129">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="8df70-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8df70-130">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="8df70-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8df70-131">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="8df70-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

