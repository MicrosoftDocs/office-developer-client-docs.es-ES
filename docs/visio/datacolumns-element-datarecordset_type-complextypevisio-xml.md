---
title: Elemento DataColumns (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contiene todos los elementos de DataColumn de un conjunto de registros de datos.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821914"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="67067-103">Elemento DataColumns (DataRecordSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="67067-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="67067-104">Contiene todos los elementos de **DataColumn** de un conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="67067-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="67067-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="67067-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67067-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="67067-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67067-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="67067-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67067-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="67067-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67067-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="67067-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67067-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="67067-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67067-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="67067-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67067-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="67067-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67067-113">Definición</span><span class="sxs-lookup"><span data-stu-id="67067-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67067-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="67067-114">Elements and attributes</span></span>

<span data-ttu-id="67067-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="67067-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67067-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="67067-116">Parent elements</span></span>

|<span data-ttu-id="67067-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="67067-117">**Element**</span></span>|<span data-ttu-id="67067-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67067-118">**Type**</span></span>|<span data-ttu-id="67067-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67067-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67067-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="67067-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67067-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="67067-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67067-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="67067-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67067-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67067-123">Child elements</span></span>

|<span data-ttu-id="67067-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="67067-124">**Element**</span></span>|<span data-ttu-id="67067-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67067-125">**Type**</span></span>|<span data-ttu-id="67067-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67067-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67067-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="67067-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67067-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="67067-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67067-129">Define cómo aparece una columna de datos en la ventana **Datos externos** en la interfaz de usuario de Visio y califica los datos en la columna mediante la definición de su tipo de datos y el formato.</span><span class="sxs-lookup"><span data-stu-id="67067-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="67067-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="67067-130">Attributes</span></span>

|<span data-ttu-id="67067-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="67067-131">**Attribute**</span></span>|<span data-ttu-id="67067-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="67067-132">**Type**</span></span>|<span data-ttu-id="67067-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="67067-133">**Required**</span></span>|<span data-ttu-id="67067-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67067-134">**Description**</span></span>|<span data-ttu-id="67067-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="67067-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67067-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="67067-136">SortAsc</span></span>  <br/> |<span data-ttu-id="67067-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="67067-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67067-138">opcional</span><span class="sxs-lookup"><span data-stu-id="67067-138">optional</span></span>  <br/> |<span data-ttu-id="67067-139">La columna en la que se va a ordenar los datos.</span><span class="sxs-lookup"><span data-stu-id="67067-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="67067-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="67067-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67067-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="67067-141">SortColumn</span></span>  <br/> |<span data-ttu-id="67067-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="67067-142">xsd:string</span></span>  <br/> |<span data-ttu-id="67067-143">opcional</span><span class="sxs-lookup"><span data-stu-id="67067-143">optional</span></span>  <br/> |<span data-ttu-id="67067-144">Si desea ordenar la columna **SortColumn** (1) de forma ascendente o descendente (0).</span><span class="sxs-lookup"><span data-stu-id="67067-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="67067-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="67067-145">Values of the xsd:string type.</span></span>  <br/> |
   

