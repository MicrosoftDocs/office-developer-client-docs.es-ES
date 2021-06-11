---
title: Elemento RefreshConflict (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542838"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="a178a-103">Elemento RefreshConflict (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a178a-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a178a-104">Indica una fila del conjunto de registros de datos vinculada a una forma que está en conflicto después de actualizar el conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="a178a-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a178a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a178a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a178a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a178a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a178a-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="a178a-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a178a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a178a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a178a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a178a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a178a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a178a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a178a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a178a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a178a-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="a178a-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a178a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a178a-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a178a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a178a-114">Elements and attributes</span></span>

<span data-ttu-id="a178a-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a178a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a178a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a178a-116">Parent elements</span></span>

|<span data-ttu-id="a178a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a178a-117">**Element**</span></span>|<span data-ttu-id="a178a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a178a-118">**Type**</span></span>|<span data-ttu-id="a178a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a178a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a178a-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="a178a-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a178a-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="a178a-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a178a-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a178a-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a178a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a178a-123">Child elements</span></span>

<span data-ttu-id="a178a-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a178a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a178a-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="a178a-125">Attributes</span></span>

|<span data-ttu-id="a178a-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a178a-126">**Attribute**</span></span>|<span data-ttu-id="a178a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a178a-127">**Type**</span></span>|<span data-ttu-id="a178a-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="a178a-128">**Required**</span></span>|<span data-ttu-id="a178a-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a178a-129">**Description**</span></span>|<span data-ttu-id="a178a-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="a178a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a178a-131">PageID</span><span class="sxs-lookup"><span data-stu-id="a178a-131">PageID</span></span>  <br/> |<span data-ttu-id="a178a-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a178a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a178a-133">necesario</span><span class="sxs-lookup"><span data-stu-id="a178a-133">required</span></span>  <br/> |<span data-ttu-id="a178a-134">Identificador de página de la forma implicada en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="a178a-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="a178a-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a178a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a178a-136">RowID</span><span class="sxs-lookup"><span data-stu-id="a178a-136">RowID</span></span>  <br/> |<span data-ttu-id="a178a-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a178a-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a178a-138">necesario</span><span class="sxs-lookup"><span data-stu-id="a178a-138">required</span></span>  <br/> |<span data-ttu-id="a178a-139">El identificador de fila original de la fila ahora en conflicto después de actualizar los datos .</span><span class="sxs-lookup"><span data-stu-id="a178a-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="a178a-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a178a-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a178a-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="a178a-141">ShapeID</span></span>  <br/> |<span data-ttu-id="a178a-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a178a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a178a-143">necesario</span><span class="sxs-lookup"><span data-stu-id="a178a-143">required</span></span>  <br/> |<span data-ttu-id="a178a-144">Identificador de forma de la forma implicada en el conflicto.</span><span class="sxs-lookup"><span data-stu-id="a178a-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="a178a-145">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a178a-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

