---
title: Elemento AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define una regla que compara una columna del elemento DataRecordset primario con un elemento de datos de formas de la última acción de vinculación automática realizada correctamente en la interfaz de usuario.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537874"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="6e4e8-103">Elemento AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6e4e8-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6e4e8-104">Define una regla que compara una columna del elemento **DataRecordset** primario con un elemento de datos de formas de la última acción de vinculación automática realizada correctamente en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6e4e8-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6e4e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e4e8-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6e4e8-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="6e4e8-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6e4e8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6e4e8-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6e4e8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6e4e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6e4e8-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6e4e8-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="6e4e8-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e4e8-113">Definición</span><span class="sxs-lookup"><span data-stu-id="6e4e8-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e4e8-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="6e4e8-114">Elements and attributes</span></span>

<span data-ttu-id="6e4e8-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e4e8-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6e4e8-116">Parent elements</span></span>

|<span data-ttu-id="6e4e8-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-117">**Element**</span></span>|<span data-ttu-id="6e4e8-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-118">**Type**</span></span>|<span data-ttu-id="6e4e8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e4e8-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="6e4e8-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e4e8-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="6e4e8-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e4e8-122">Especifica un conjunto de registros y el enlace de datos entre ese conjunto de registros y las formas de las páginas de dibujo.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e4e8-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e4e8-123">Child elements</span></span>

<span data-ttu-id="6e4e8-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e4e8-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e4e8-125">Attributes</span></span>

|<span data-ttu-id="6e4e8-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-126">**Attribute**</span></span>|<span data-ttu-id="6e4e8-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-127">**Type**</span></span>|<span data-ttu-id="6e4e8-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-128">**Required**</span></span>|<span data-ttu-id="6e4e8-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-129">**Description**</span></span>|<span data-ttu-id="6e4e8-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="6e4e8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6e4e8-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="6e4e8-131">ColumnName</span></span>  <br/> |<span data-ttu-id="6e4e8-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6e4e8-132">xsd:string</span></span>  <br/> |<span data-ttu-id="6e4e8-133">necesario</span><span class="sxs-lookup"><span data-stu-id="6e4e8-133">required</span></span>  <br/> |<span data-ttu-id="6e4e8-134">Corresponde a un nombre de columna en el conjunto de registros de ADO.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="6e4e8-135">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6e4e8-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="6e4e8-136">ContextType</span></span>  <br/> |<span data-ttu-id="6e4e8-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6e4e8-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6e4e8-138">necesario</span><span class="sxs-lookup"><span data-stu-id="6e4e8-138">required</span></span>  <br/> |<span data-ttu-id="6e4e8-139">Especifica las propiedades del grupo o la forma que se usará para la comparación.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="6e4e8-140">Los valores posibles se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="6e4e8-141">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6e4e8-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="6e4e8-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="6e4e8-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6e4e8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6e4e8-144">opcional</span><span class="sxs-lookup"><span data-stu-id="6e4e8-144">optional</span></span>  <br/> |<span data-ttu-id="6e4e8-145">Si el valor ContextType es 2 o 3, este atributo es necesario para definir una comparación.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="6e4e8-146">Para ContextType = 2, ContextTypeLabel debe ser la etiqueta del elemento de datos de forma y, si **ContextType** = 3, ContextTypeLabel debe ser el nombre de fila local.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="6e4e8-147">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6e4e8-147">Values of the xsd:string type.</span></span>  <br/> |
   

