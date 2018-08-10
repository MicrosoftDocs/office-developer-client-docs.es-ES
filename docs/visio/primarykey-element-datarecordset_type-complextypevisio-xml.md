---
title: Elemento ClavePrincipal (DataRecordSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Identifica una o más columnas de clave principal en el conjunto de registros de datos.
ms.openlocfilehash: f720636bbdf2c55baca6d98aa7d0761607e53ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822873"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="8f250-103">Elemento ClavePrincipal (DataRecordSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="8f250-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8f250-104">Identifica una o más columnas de clave principal en el conjunto de registros de datos.</span><span class="sxs-lookup"><span data-stu-id="8f250-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8f250-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8f250-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f250-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8f250-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8f250-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="8f250-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8f250-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8f250-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8f250-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8f250-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8f250-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8f250-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8f250-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8f250-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8f250-112">Recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="8f250-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8f250-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8f250-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8f250-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8f250-114">Elements and attributes</span></span>

<span data-ttu-id="8f250-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="8f250-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8f250-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8f250-116">Parent elements</span></span>

|<span data-ttu-id="8f250-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f250-117">**Element**</span></span>|<span data-ttu-id="8f250-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f250-118">**Type**</span></span>|<span data-ttu-id="8f250-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f250-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f250-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f250-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f250-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="8f250-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f250-122">Almacena, actualiza, expone y da formato a los datos consultados en una base de datos de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8f250-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8f250-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8f250-123">Child elements</span></span>

|<span data-ttu-id="8f250-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f250-124">**Element**</span></span>|<span data-ttu-id="8f250-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f250-125">**Type**</span></span>|<span data-ttu-id="8f250-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f250-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8f250-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="8f250-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8f250-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="8f250-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8f250-129">Especifica el valor de este componente de la clave principal de una fila individual de un objeto recordset.</span><span class="sxs-lookup"><span data-stu-id="8f250-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="8f250-130">DEBE haber al menos una repetición de este elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="8f250-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8f250-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="8f250-131">Attributes</span></span>

|<span data-ttu-id="8f250-132">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8f250-132">**Attribute**</span></span>|<span data-ttu-id="8f250-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8f250-133">**Type**</span></span>|<span data-ttu-id="8f250-134">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8f250-134">**Required**</span></span>|<span data-ttu-id="8f250-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8f250-135">**Description**</span></span>|<span data-ttu-id="8f250-136">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="8f250-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8f250-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="8f250-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="8f250-138">xsd: String</span><span class="sxs-lookup"><span data-stu-id="8f250-138">xsd:string</span></span>  <br/> |<span data-ttu-id="8f250-139">opcional</span><span class="sxs-lookup"><span data-stu-id="8f250-139">optional</span></span>  <br/> |<span data-ttu-id="8f250-140">Especifica el nombre de un campo que es un componente de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="8f250-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="8f250-141">DEBE ser el valor del atributo **ColumnNameID** de un elemento descendiente DataColumn_Type de la DataRecordSet_Type se especifica cuya clave principal.</span><span class="sxs-lookup"><span data-stu-id="8f250-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="8f250-142">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="8f250-142">Values of the xsd:string type.</span></span>  <br/> |
   
