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
ms.openlocfilehash: 53772fca5e8137dfd602d4c7d6f5e6ad40f9c50f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573435"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="66b28-103">Propiedad canónica PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="66b28-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="66b28-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66b28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66b28-105">Contiene un valor que identifica de forma exclusiva una fila en una tabla.</span><span class="sxs-lookup"><span data-stu-id="66b28-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="66b28-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="66b28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66b28-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="66b28-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="66b28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="66b28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66b28-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="66b28-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="66b28-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="66b28-110">Data type:</span></span>  <br/> |<span data-ttu-id="66b28-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="66b28-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="66b28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="66b28-112">Area:</span></span>  <br/> |<span data-ttu-id="66b28-113">Tabla</span><span class="sxs-lookup"><span data-stu-id="66b28-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66b28-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66b28-114">Remarks</span></span>

<span data-ttu-id="66b28-115">Esta propiedad es un valor binario que identifica de forma exclusiva una fila en una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="66b28-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="66b28-116">Es una columna necesaria en la mayoría de las tablas.</span><span class="sxs-lookup"><span data-stu-id="66b28-116">It is a required column in most tables.</span></span> <span data-ttu-id="66b28-117">Si se incluye una fila en dos vistas, hay dos claves de instancia diferente.</span><span class="sxs-lookup"><span data-stu-id="66b28-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="66b28-118">La clave de instancia de una fila puede diferir cada vez que se abre en la tabla, pero permanece constante mientras la tabla está abierto.</span><span class="sxs-lookup"><span data-stu-id="66b28-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="66b28-119">Filas agregadas mientras una tabla está en uso no volver a usar una clave de instancia que se usó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="66b28-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="66b28-120">Utilice las propiedades de **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) o la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para correlacionar todas las filas de una expansión.</span><span class="sxs-lookup"><span data-stu-id="66b28-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="66b28-121">Use **PR_INSTANCE_KEY** para buscar una instancia determinada dentro de la expansión.</span><span class="sxs-lookup"><span data-stu-id="66b28-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="66b28-122">Cuando se expande una propiedad multivalor en una tabla, se crea una fila para cada instancia de la expansión, es decir, para cada valor de dicha propiedad.</span><span class="sxs-lookup"><span data-stu-id="66b28-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="66b28-123">Cada fila tiene un valor único para la propiedad **PR_INSTANCE_KEY** , mientras que todas las demás columnas conservan sus valores originales en toda la expansión.</span><span class="sxs-lookup"><span data-stu-id="66b28-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="66b28-124">En una ordenación por categorías de una tabla, se pueden agregar filas no correspondiente a los datos reales en el resultado de la ordenación.</span><span class="sxs-lookup"><span data-stu-id="66b28-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="66b28-125">Cada fila, al igual que todas las filas de todas las tablas, tiene su propia clave de instancia única.</span><span class="sxs-lookup"><span data-stu-id="66b28-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="66b28-126">**PR_INSTANCE_KEY** también se usa en las notificaciones de eventos de tabla.</span><span class="sxs-lookup"><span data-stu-id="66b28-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="66b28-127">Los miembros **propIndex** y **propPrior** de la estructura [TABLE_NOTIFICATION](table_notification.md) son estructuras [SPropValue](spropvalue.md) contienen valores **PR_INSTANCE_KEY** .</span><span class="sxs-lookup"><span data-stu-id="66b28-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="66b28-128">El miembro **propIndex** indica la fila que se ha agregado o modificado.</span><span class="sxs-lookup"><span data-stu-id="66b28-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="66b28-129">El miembro **propPrior** indica la fila antes de la fila se ha agregado o modificada (**PR_NULL** indica un cambio en la primera fila).</span><span class="sxs-lookup"><span data-stu-id="66b28-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="66b28-130">Este valor no se copia como parte de la tabla para mostrar.</span><span class="sxs-lookup"><span data-stu-id="66b28-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="66b28-131">**PR_INSTANCE_KEY** es una estructura [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="66b28-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="66b28-132">Todas las claves de la instancia se pueden comparar directamente como valores binarios.</span><span class="sxs-lookup"><span data-stu-id="66b28-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="66b28-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="66b28-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66b28-134">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="66b28-134">Protocol specifications</span></span>

<span data-ttu-id="66b28-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66b28-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66b28-136">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="66b28-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66b28-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66b28-137">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66b28-138">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="66b28-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66b28-139">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="66b28-139">Header files</span></span>

<span data-ttu-id="66b28-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66b28-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="66b28-141">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="66b28-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="66b28-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="66b28-142">Mapitags.h</span></span>
  
> <span data-ttu-id="66b28-143">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="66b28-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66b28-144">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="66b28-144">See also</span></span>



[<span data-ttu-id="66b28-145">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="66b28-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66b28-146">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="66b28-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66b28-147">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="66b28-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66b28-148">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="66b28-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

