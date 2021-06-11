---
title: Propiedad canónica PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358514"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="d3e23-103">Propiedad canónica PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="d3e23-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="d3e23-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3e23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3e23-105">Contiene un valor que identifica de forma única una fila de una tabla.</span><span class="sxs-lookup"><span data-stu-id="d3e23-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3e23-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d3e23-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3e23-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="d3e23-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="d3e23-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d3e23-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d3e23-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="d3e23-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="d3e23-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d3e23-110">Data type:</span></span>  <br/> |<span data-ttu-id="d3e23-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d3e23-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d3e23-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d3e23-112">Area:</span></span>  <br/> |<span data-ttu-id="d3e23-113">Tabla</span><span class="sxs-lookup"><span data-stu-id="d3e23-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3e23-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3e23-114">Remarks</span></span>

<span data-ttu-id="d3e23-115">Esta propiedad es un valor binario que identifica de forma única una fila en una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="d3e23-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="d3e23-116">Es una columna necesaria en la mayoría de las tablas.</span><span class="sxs-lookup"><span data-stu-id="d3e23-116">It is a required column in most tables.</span></span> <span data-ttu-id="d3e23-117">Si una fila se incluye en dos vistas, hay dos claves de instancia diferentes.</span><span class="sxs-lookup"><span data-stu-id="d3e23-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="d3e23-118">La clave de instancia de una fila puede diferir cada vez que se abre la tabla, pero permanece constante mientras la tabla está abierta.</span><span class="sxs-lookup"><span data-stu-id="d3e23-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="d3e23-119">Las filas agregadas mientras se usa una tabla no reutilizan una clave de instancia que se usó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d3e23-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="d3e23-120">Use las **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) o **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para correlacionar todas las filas de una expansión.</span><span class="sxs-lookup"><span data-stu-id="d3e23-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="d3e23-121">Use **PR_INSTANCE_KEY** para localizar una instancia determinada dentro de la expansión.</span><span class="sxs-lookup"><span data-stu-id="d3e23-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="d3e23-122">Cuando se expande una propiedad multivalor en una tabla, se crea una fila para cada instancia de la expansión, es decir, para cada valor de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3e23-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="d3e23-123">Cada fila tiene un valor único para la **propiedad PR_INSTANCE_KEY,** mientras que todas las demás columnas conservan sus valores originales a lo largo de la expansión.</span><span class="sxs-lookup"><span data-stu-id="d3e23-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="d3e23-124">En un tipo categorizado de una tabla, las filas que no corresponden a datos reales se pueden agregar al resultado de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="d3e23-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="d3e23-125">Cada fila de este tipo, como todas las filas de todas las tablas, tiene su propia clave de instancia única.</span><span class="sxs-lookup"><span data-stu-id="d3e23-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="d3e23-126">**PR_INSTANCE_KEY** también se usa en notificaciones de eventos de tabla.</span><span class="sxs-lookup"><span data-stu-id="d3e23-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="d3e23-127">Los **miembros propIndex** y **propPrior** de la [estructura TABLE_NOTIFICATION](table_notification.md) son estructuras [SPropValue](spropvalue.md) que **PR_INSTANCE_KEY** valores.</span><span class="sxs-lookup"><span data-stu-id="d3e23-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="d3e23-128">El **miembro propIndex** indica la fila que se agregó o cambió.</span><span class="sxs-lookup"><span data-stu-id="d3e23-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="d3e23-129">El **miembro propPrior** indica la fila antes de la fila agregada o modificada (**PR_NULL** indica un cambio en la primera fila).</span><span class="sxs-lookup"><span data-stu-id="d3e23-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="d3e23-130">Este valor no se copia como parte de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="d3e23-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="d3e23-131">**PR_INSTANCE_KEY** es una [estructura MAPIUID.](mapiuid.md)</span><span class="sxs-lookup"><span data-stu-id="d3e23-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="d3e23-132">Todas las claves de instancia se pueden comparar directamente como valores binarios.</span><span class="sxs-lookup"><span data-stu-id="d3e23-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d3e23-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3e23-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3e23-134">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="d3e23-134">Protocol specifications</span></span>

<span data-ttu-id="d3e23-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3e23-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3e23-136">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="d3e23-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3e23-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3e23-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3e23-138">Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="d3e23-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3e23-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d3e23-139">Header files</span></span>

<span data-ttu-id="d3e23-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3e23-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3e23-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d3e23-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="d3e23-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d3e23-142">Mapitags.h</span></span>
  
> <span data-ttu-id="d3e23-143">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d3e23-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3e23-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3e23-144">See also</span></span>



[<span data-ttu-id="d3e23-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d3e23-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3e23-146">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d3e23-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3e23-147">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d3e23-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3e23-148">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="d3e23-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

