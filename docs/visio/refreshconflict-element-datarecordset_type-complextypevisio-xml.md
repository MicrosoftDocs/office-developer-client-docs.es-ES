---
title: Elemento de RefreshConflict (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica una fila en el conjunto de registros de datos vinculada a una forma que está en conflicto después de actualiza el conjunto de registros de datos.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397404"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="ade97-103">Elemento de RefreshConflict (DataRecordSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ade97-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ade97-104">Indica una fila en el conjunto de registros de datos vinculada a una forma que está en conflicto después de actualiza el conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="ade97-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ade97-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ade97-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ade97-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ade97-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ade97-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="ade97-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ade97-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ade97-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ade97-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ade97-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ade97-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ade97-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ade97-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ade97-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ade97-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="ade97-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ade97-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ade97-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ade97-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ade97-114">Elements and attributes</span></span>

<span data-ttu-id="ade97-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ade97-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ade97-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ade97-116">Parent elements</span></span>

|<span data-ttu-id="ade97-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ade97-117">**Element**</span></span>|<span data-ttu-id="ade97-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ade97-118">**Type**</span></span>|<span data-ttu-id="ade97-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ade97-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ade97-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="ade97-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ade97-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="ade97-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ade97-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="ade97-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ade97-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ade97-123">Child elements</span></span>

<span data-ttu-id="ade97-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ade97-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ade97-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="ade97-125">Attributes</span></span>

|<span data-ttu-id="ade97-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ade97-126">**Attribute**</span></span>|<span data-ttu-id="ade97-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ade97-127">**Type**</span></span>|<span data-ttu-id="ade97-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ade97-128">**Required**</span></span>|<span data-ttu-id="ade97-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ade97-129">**Description**</span></span>|<span data-ttu-id="ade97-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ade97-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ade97-131">PageID</span><span class="sxs-lookup"><span data-stu-id="ade97-131">PageID</span></span>  <br/> |<span data-ttu-id="ade97-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ade97-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ade97-133">necesario</span><span class="sxs-lookup"><span data-stu-id="ade97-133">required</span></span>  <br/> |<span data-ttu-id="ade97-134">Identificador de página de la forma implica en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="ade97-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="ade97-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ade97-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ade97-136">RowID</span><span class="sxs-lookup"><span data-stu-id="ade97-136">RowID</span></span>  <br/> |<span data-ttu-id="ade97-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ade97-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ade97-138">necesario</span><span class="sxs-lookup"><span data-stu-id="ade97-138">required</span></span>  <br/> |<span data-ttu-id="ade97-139">El identificador de fila original de la fila ahora en conflicto después de que se actualizan los datos.</span><span class="sxs-lookup"><span data-stu-id="ade97-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="ade97-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ade97-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ade97-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ade97-141">ShapeID</span></span>  <br/> |<span data-ttu-id="ade97-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ade97-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ade97-143">necesario</span><span class="sxs-lookup"><span data-stu-id="ade97-143">required</span></span>  <br/> |<span data-ttu-id="ade97-144">Identificador de la forma de la forma implica en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="ade97-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="ade97-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ade97-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

