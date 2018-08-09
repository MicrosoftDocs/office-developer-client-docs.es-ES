---
title: Elemento de RowMap (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Asigna una fila del conjunto de registros de datos a una forma.
ms.openlocfilehash: aefae8c625f35feacd6d0fdf04f128c423db299b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823075"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="687bb-103">Elemento de RowMap (DataRecordSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="687bb-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="687bb-104">Asigna una fila del conjunto de registros de datos a una forma.</span><span class="sxs-lookup"><span data-stu-id="687bb-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="687bb-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="687bb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="687bb-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="687bb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="687bb-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="687bb-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="687bb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="687bb-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="687bb-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="687bb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="687bb-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="687bb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="687bb-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="687bb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="687bb-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="687bb-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="687bb-113">Definición</span><span class="sxs-lookup"><span data-stu-id="687bb-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="687bb-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="687bb-114">Elements and attributes</span></span>

<span data-ttu-id="687bb-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="687bb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="687bb-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="687bb-116">Parent elements</span></span>

****

|<span data-ttu-id="687bb-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="687bb-117">**Element**</span></span>|<span data-ttu-id="687bb-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="687bb-118">**Type**</span></span>|<span data-ttu-id="687bb-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="687bb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="687bb-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="687bb-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="687bb-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="687bb-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="687bb-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="687bb-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="687bb-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="687bb-123">Child elements</span></span>

<span data-ttu-id="687bb-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="687bb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="687bb-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="687bb-125">Attributes</span></span>

|<span data-ttu-id="687bb-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="687bb-126">**Attribute**</span></span>|<span data-ttu-id="687bb-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="687bb-127">**Type**</span></span>|<span data-ttu-id="687bb-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="687bb-128">**Required**</span></span>|<span data-ttu-id="687bb-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="687bb-129">**Description**</span></span>|<span data-ttu-id="687bb-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="687bb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="687bb-131">PageID</span><span class="sxs-lookup"><span data-stu-id="687bb-131">PageID</span></span>  <br/> |<span data-ttu-id="687bb-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="687bb-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="687bb-133">necesario</span><span class="sxs-lookup"><span data-stu-id="687bb-133">required</span></span>  <br/> |<span data-ttu-id="687bb-134">Identificador de página de la forma vinculada a los datos en la fila del conjunto de registros de datos identificada por **RowID**.</span><span class="sxs-lookup"><span data-stu-id="687bb-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="687bb-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="687bb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="687bb-136">RowID</span><span class="sxs-lookup"><span data-stu-id="687bb-136">RowID</span></span>  <br/> |<span data-ttu-id="687bb-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="687bb-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="687bb-138">necesario</span><span class="sxs-lookup"><span data-stu-id="687bb-138">required</span></span>  <br/> |<span data-ttu-id="687bb-139">Identificador de la fila, única en el conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="687bb-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="687bb-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="687bb-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="687bb-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="687bb-141">ShapeID</span></span>  <br/> |<span data-ttu-id="687bb-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="687bb-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="687bb-143">necesario</span><span class="sxs-lookup"><span data-stu-id="687bb-143">required</span></span>  <br/> |<span data-ttu-id="687bb-144">Identificador de la forma de la forma vinculada a los datos en la fila del conjunto de registros de datos identificada por **RowID**.</span><span class="sxs-lookup"><span data-stu-id="687bb-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="687bb-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="687bb-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

