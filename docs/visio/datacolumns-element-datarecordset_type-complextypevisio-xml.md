---
title: Elemento DataColumns (DataRecordSet_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contiene todos los elementos DataColumn de un conjunto de registros de datos.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541200"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="c8e23-103">Elemento DataColumns (DataRecordSet_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="c8e23-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c8e23-104">Contiene todos los **elementos DataColumn** de un conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="c8e23-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c8e23-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8e23-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8e23-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c8e23-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c8e23-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="c8e23-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c8e23-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c8e23-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c8e23-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8e23-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c8e23-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c8e23-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c8e23-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c8e23-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c8e23-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="c8e23-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8e23-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c8e23-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c8e23-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c8e23-114">Elements and attributes</span></span>

<span data-ttu-id="c8e23-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c8e23-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c8e23-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8e23-116">Parent elements</span></span>

|<span data-ttu-id="c8e23-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8e23-117">**Element**</span></span>|<span data-ttu-id="c8e23-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8e23-118">**Type**</span></span>|<span data-ttu-id="c8e23-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8e23-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8e23-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="c8e23-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8e23-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="c8e23-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c8e23-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c8e23-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c8e23-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8e23-123">Child elements</span></span>

|<span data-ttu-id="c8e23-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8e23-124">**Element**</span></span>|<span data-ttu-id="c8e23-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8e23-125">**Type**</span></span>|<span data-ttu-id="c8e23-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8e23-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8e23-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="c8e23-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8e23-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="c8e23-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c8e23-129">Define cómo aparece una  columna de datos en la ventana Datos externos de la interfaz de usuario de Visio y clasifica los datos de la columna definiendo su tipo de datos y formato.</span><span class="sxs-lookup"><span data-stu-id="c8e23-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c8e23-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8e23-130">Attributes</span></span>

|<span data-ttu-id="c8e23-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c8e23-131">**Attribute**</span></span>|<span data-ttu-id="c8e23-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c8e23-132">**Type**</span></span>|<span data-ttu-id="c8e23-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c8e23-133">**Required**</span></span>|<span data-ttu-id="c8e23-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8e23-134">**Description**</span></span>|<span data-ttu-id="c8e23-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c8e23-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c8e23-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="c8e23-136">SortAsc</span></span>  <br/> |<span data-ttu-id="c8e23-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c8e23-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c8e23-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c8e23-138">optional</span></span>  <br/> |<span data-ttu-id="c8e23-139">Columna en la que se ordenarán los datos.</span><span class="sxs-lookup"><span data-stu-id="c8e23-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="c8e23-140">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c8e23-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c8e23-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="c8e23-141">SortColumn</span></span>  <br/> |<span data-ttu-id="c8e23-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c8e23-142">xsd:string</span></span>  <br/> |<span data-ttu-id="c8e23-143">opcional</span><span class="sxs-lookup"><span data-stu-id="c8e23-143">optional</span></span>  <br/> |<span data-ttu-id="c8e23-144">Si se ordena la **columna SortColumn** en orden ascendente (1) o descendente (0).</span><span class="sxs-lookup"><span data-stu-id="c8e23-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="c8e23-145">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c8e23-145">Values of the xsd:string type.</span></span>  <br/> |
   

