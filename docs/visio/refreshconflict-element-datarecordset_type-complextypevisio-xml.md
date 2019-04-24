---
title: Elemento RefreshConflict (complexType DataRecordSet_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360140"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="6da59-103">Elemento RefreshConflict (complexType DataRecordSet_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="6da59-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6da59-104">Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="6da59-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6da59-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6da59-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6da59-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6da59-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6da59-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="6da59-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6da59-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6da59-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6da59-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6da59-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6da59-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6da59-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6da59-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6da59-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6da59-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="6da59-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6da59-113">Definición</span><span class="sxs-lookup"><span data-stu-id="6da59-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6da59-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6da59-114">Elements and attributes</span></span>

<span data-ttu-id="6da59-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6da59-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6da59-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6da59-116">Parent elements</span></span>

|<span data-ttu-id="6da59-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6da59-117">**Element**</span></span>|<span data-ttu-id="6da59-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6da59-118">**Type**</span></span>|<span data-ttu-id="6da59-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6da59-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6da59-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="6da59-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6da59-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="6da59-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6da59-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6da59-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6da59-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6da59-123">Child elements</span></span>

<span data-ttu-id="6da59-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6da59-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6da59-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="6da59-125">Attributes</span></span>

|<span data-ttu-id="6da59-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6da59-126">**Attribute**</span></span>|<span data-ttu-id="6da59-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6da59-127">**Type**</span></span>|<span data-ttu-id="6da59-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6da59-128">**Required**</span></span>|<span data-ttu-id="6da59-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6da59-129">**Description**</span></span>|<span data-ttu-id="6da59-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="6da59-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6da59-131">PageID</span><span class="sxs-lookup"><span data-stu-id="6da59-131">PageID</span></span>  <br/> |<span data-ttu-id="6da59-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6da59-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6da59-133">necesario</span><span class="sxs-lookup"><span data-stu-id="6da59-133">required</span></span>  <br/> |<span data-ttu-id="6da59-134">IDENTIFICADOR de página de la forma implicada en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="6da59-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="6da59-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6da59-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6da59-136">Pseudocolumna</span><span class="sxs-lookup"><span data-stu-id="6da59-136">RowID</span></span>  <br/> |<span data-ttu-id="6da59-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6da59-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6da59-138">necesario</span><span class="sxs-lookup"><span data-stu-id="6da59-138">required</span></span>  <br/> |<span data-ttu-id="6da59-139">El identificador de fila original de la fila ahora está en conflicto después de actualizar los datos.</span><span class="sxs-lookup"><span data-stu-id="6da59-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="6da59-140">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6da59-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6da59-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="6da59-141">ShapeID</span></span>  <br/> |<span data-ttu-id="6da59-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6da59-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6da59-143">necesario</span><span class="sxs-lookup"><span data-stu-id="6da59-143">required</span></span>  <br/> |<span data-ttu-id="6da59-144">IDENTIFICADOR de la forma implicada en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="6da59-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="6da59-145">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6da59-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

