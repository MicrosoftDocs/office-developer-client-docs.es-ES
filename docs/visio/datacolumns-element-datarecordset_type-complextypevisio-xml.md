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
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="eefa0-103">Elemento DataColumns (DataRecordSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="eefa0-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="eefa0-104">Contiene todos los elementos de **DataColumn** de un conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="eefa0-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="eefa0-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eefa0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eefa0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="eefa0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="eefa0-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="eefa0-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="eefa0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eefa0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="eefa0-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="eefa0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="eefa0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="eefa0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="eefa0-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="eefa0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="eefa0-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="eefa0-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eefa0-113">Definición</span><span class="sxs-lookup"><span data-stu-id="eefa0-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eefa0-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="eefa0-114">Elements and attributes</span></span>

<span data-ttu-id="eefa0-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="eefa0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="eefa0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eefa0-116">Parent elements</span></span>

|<span data-ttu-id="eefa0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="eefa0-117">**Element**</span></span>|<span data-ttu-id="eefa0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eefa0-118">**Type**</span></span>|<span data-ttu-id="eefa0-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eefa0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eefa0-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="eefa0-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eefa0-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="eefa0-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eefa0-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="eefa0-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eefa0-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eefa0-123">Child elements</span></span>

|<span data-ttu-id="eefa0-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="eefa0-124">**Element**</span></span>|<span data-ttu-id="eefa0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eefa0-125">**Type**</span></span>|<span data-ttu-id="eefa0-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eefa0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eefa0-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="eefa0-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eefa0-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="eefa0-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eefa0-129">Define cómo aparece una columna de datos en la ventana **Datos externos** en la interfaz de usuario de Visio y califica los datos en la columna mediante la definición de su tipo de datos y el formato.</span><span class="sxs-lookup"><span data-stu-id="eefa0-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="eefa0-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="eefa0-130">Attributes</span></span>

|<span data-ttu-id="eefa0-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="eefa0-131">**Attribute**</span></span>|<span data-ttu-id="eefa0-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="eefa0-132">**Type**</span></span>|<span data-ttu-id="eefa0-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="eefa0-133">**Required**</span></span>|<span data-ttu-id="eefa0-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eefa0-134">**Description**</span></span>|<span data-ttu-id="eefa0-135">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="eefa0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eefa0-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="eefa0-136">SortAsc</span></span>  <br/> |<span data-ttu-id="eefa0-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="eefa0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="eefa0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="eefa0-138">optional</span></span>  <br/> |<span data-ttu-id="eefa0-139">La columna en la que se va a ordenar los datos.</span><span class="sxs-lookup"><span data-stu-id="eefa0-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="eefa0-140">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="eefa0-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="eefa0-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="eefa0-141">SortColumn</span></span>  <br/> |<span data-ttu-id="eefa0-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="eefa0-142">xsd:string</span></span>  <br/> |<span data-ttu-id="eefa0-143">opcional</span><span class="sxs-lookup"><span data-stu-id="eefa0-143">optional</span></span>  <br/> |<span data-ttu-id="eefa0-144">Si desea ordenar la columna **SortColumn** (1) de forma ascendente o descendente (0).</span><span class="sxs-lookup"><span data-stu-id="eefa0-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="eefa0-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="eefa0-145">Values of the xsd:string type.</span></span>  <br/> |
   

