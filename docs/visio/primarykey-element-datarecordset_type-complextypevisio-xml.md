---
title: Elemento PrimaryKey (complexType DataRecordSet_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifica una o más columnas de clave principal del conjunto de registros de datos.
ms.openlocfilehash: bd77b1d18490695dc2b0cb43520f42bb845e91ab
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537713"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="b4f82-103">Elemento PrimaryKey (complexType DataRecordSet_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="b4f82-103">PrimaryKey element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b4f82-104">Identifica una o más columnas de clave principal del conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="b4f82-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4f82-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4f82-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4f82-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b4f82-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b4f82-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="b4f82-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b4f82-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b4f82-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b4f82-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b4f82-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b4f82-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b4f82-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b4f82-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b4f82-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b4f82-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="b4f82-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4f82-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b4f82-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b4f82-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b4f82-114">Elements and attributes</span></span>

<span data-ttu-id="b4f82-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="b4f82-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b4f82-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4f82-116">Parent elements</span></span>

|<span data-ttu-id="b4f82-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b4f82-117">**Element**</span></span>|<span data-ttu-id="b4f82-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4f82-118">**Type**</span></span>|<span data-ttu-id="b4f82-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4f82-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4f82-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="b4f82-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4f82-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="b4f82-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b4f82-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="b4f82-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b4f82-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4f82-123">Child elements</span></span>

|<span data-ttu-id="b4f82-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b4f82-124">**Element**</span></span>|<span data-ttu-id="b4f82-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4f82-125">**Type**</span></span>|<span data-ttu-id="b4f82-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4f82-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4f82-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="b4f82-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4f82-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="b4f82-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b4f82-129">Especifica el valor de este componente de la clave principal para una fila individual de un objeto Recordset.</span><span class="sxs-lookup"><span data-stu-id="b4f82-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="b4f82-130">DEBE haber al menos una ocurrencia de este elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="b4f82-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b4f82-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4f82-131">Attributes</span></span>

|<span data-ttu-id="b4f82-132">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b4f82-132">**Attribute**</span></span>|<span data-ttu-id="b4f82-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b4f82-133">**Type**</span></span>|<span data-ttu-id="b4f82-134">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b4f82-134">**Required**</span></span>|<span data-ttu-id="b4f82-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4f82-135">**Description**</span></span>|<span data-ttu-id="b4f82-136">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="b4f82-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4f82-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="b4f82-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="b4f82-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b4f82-138">xsd:string</span></span>  <br/> |<span data-ttu-id="b4f82-139">opcional</span><span class="sxs-lookup"><span data-stu-id="b4f82-139">optional</span></span>  <br/> |<span data-ttu-id="b4f82-140">Especifica el nombre de un campo que es un componente de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="b4f82-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="b4f82-141">DEBE ser el valor del atributo **ColumnNameID** de un elemento descendiente de DataColumn_Type de la DataRecordSet_Type cuya clave principal se especifica.</span><span class="sxs-lookup"><span data-stu-id="b4f82-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="b4f82-142">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b4f82-142">Values of the xsd:string type.</span></span>  <br/> |
   

