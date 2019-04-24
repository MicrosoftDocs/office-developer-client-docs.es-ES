---
title: Elemento DataColumns (DataRecordSet_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contiene todos los elementos DataColumn de un conjunto de registros de datos.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345251"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="7d76e-103">Elemento DataColumns (DataRecordSet_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="7d76e-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7d76e-104">Contiene todos los elementos **DataColumn** de un conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="7d76e-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7d76e-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7d76e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d76e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7d76e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7d76e-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="7d76e-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7d76e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7d76e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7d76e-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7d76e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7d76e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7d76e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7d76e-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7d76e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7d76e-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="7d76e-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d76e-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7d76e-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7d76e-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7d76e-114">Elements and attributes</span></span>

<span data-ttu-id="7d76e-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7d76e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7d76e-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7d76e-116">Parent elements</span></span>

|<span data-ttu-id="7d76e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d76e-117">**Element**</span></span>|<span data-ttu-id="7d76e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d76e-118">**Type**</span></span>|<span data-ttu-id="7d76e-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d76e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d76e-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="7d76e-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d76e-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7d76e-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7d76e-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="7d76e-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7d76e-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7d76e-123">Child elements</span></span>

|<span data-ttu-id="7d76e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7d76e-124">**Element**</span></span>|<span data-ttu-id="7d76e-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d76e-125">**Type**</span></span>|<span data-ttu-id="7d76e-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d76e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d76e-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="7d76e-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d76e-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="7d76e-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7d76e-129">Define cómo aparece una columna de datos en la ventana **datos externos** de la interfaz de usuario de Visio y califica los datos de la columna mediante la definición de su formato y tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="7d76e-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7d76e-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7d76e-130">Attributes</span></span>

|<span data-ttu-id="7d76e-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7d76e-131">**Attribute**</span></span>|<span data-ttu-id="7d76e-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7d76e-132">**Type**</span></span>|<span data-ttu-id="7d76e-133">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7d76e-133">**Required**</span></span>|<span data-ttu-id="7d76e-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d76e-134">**Description**</span></span>|<span data-ttu-id="7d76e-135">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7d76e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d76e-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="7d76e-136">SortAsc</span></span>  <br/> |<span data-ttu-id="7d76e-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="7d76e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7d76e-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7d76e-138">optional</span></span>  <br/> |<span data-ttu-id="7d76e-139">Columna en la que se van a ordenar los datos.</span><span class="sxs-lookup"><span data-stu-id="7d76e-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="7d76e-140">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7d76e-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7d76e-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="7d76e-141">SortColumn</span></span>  <br/> |<span data-ttu-id="7d76e-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7d76e-142">xsd:string</span></span>  <br/> |<span data-ttu-id="7d76e-143">opcional</span><span class="sxs-lookup"><span data-stu-id="7d76e-143">optional</span></span>  <br/> |<span data-ttu-id="7d76e-144">Si se va a ordenar la columna **SortColumn** en orden ascendente (1) o descendente (0).</span><span class="sxs-lookup"><span data-stu-id="7d76e-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="7d76e-145">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7d76e-145">Values of the xsd:string type.</span></span>  <br/> |
   

