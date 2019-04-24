---
title: Elemento AutoLinkComparison (complexType DataRecordSet_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Define una regla que compara una columna del elemento DataRecordset principal con un elemento de datos de formas de la última acción de vinculación automática correcta realizada en la interfaz de usuario.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338321"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="2bcea-103">Elemento AutoLinkComparison (complexType DataRecordSet_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="2bcea-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2bcea-104">Define una regla que compara una columna del elemento **DataRecordset** principal con un elemento de datos de formas de la última acción de vinculación automática correcta realizada en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2bcea-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2bcea-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2bcea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2bcea-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2bcea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2bcea-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="2bcea-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2bcea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2bcea-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2bcea-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2bcea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2bcea-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="2bcea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2bcea-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="2bcea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2bcea-112">Recordsets. XML</span><span class="sxs-lookup"><span data-stu-id="2bcea-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2bcea-113">Definición</span><span class="sxs-lookup"><span data-stu-id="2bcea-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2bcea-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2bcea-114">Elements and attributes</span></span>

<span data-ttu-id="2bcea-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2bcea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2bcea-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2bcea-116">Parent elements</span></span>

|<span data-ttu-id="2bcea-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2bcea-117">**Element**</span></span>|<span data-ttu-id="2bcea-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2bcea-118">**Type**</span></span>|<span data-ttu-id="2bcea-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bcea-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2bcea-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="2bcea-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2bcea-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="2bcea-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2bcea-122">Especifica un conjunto de registros y el enlace de datos entre ese conjunto de registros y formas en las páginas del dibujo.</span><span class="sxs-lookup"><span data-stu-id="2bcea-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2bcea-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2bcea-123">Child elements</span></span>

<span data-ttu-id="2bcea-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2bcea-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2bcea-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="2bcea-125">Attributes</span></span>

|<span data-ttu-id="2bcea-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2bcea-126">**Attribute**</span></span>|<span data-ttu-id="2bcea-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2bcea-127">**Type**</span></span>|<span data-ttu-id="2bcea-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="2bcea-128">**Required**</span></span>|<span data-ttu-id="2bcea-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2bcea-129">**Description**</span></span>|<span data-ttu-id="2bcea-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="2bcea-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2bcea-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="2bcea-131">ColumnName</span></span>  <br/> |<span data-ttu-id="2bcea-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2bcea-132">xsd:string</span></span>  <br/> |<span data-ttu-id="2bcea-133">necesario</span><span class="sxs-lookup"><span data-stu-id="2bcea-133">required</span></span>  <br/> |<span data-ttu-id="2bcea-134">Corresponde a un nombre de columna en el objeto Recordset de ADO.</span><span class="sxs-lookup"><span data-stu-id="2bcea-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="2bcea-135">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2bcea-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2bcea-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="2bcea-136">ContextType</span></span>  <br/> |<span data-ttu-id="2bcea-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2bcea-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2bcea-138">necesario</span><span class="sxs-lookup"><span data-stu-id="2bcea-138">required</span></span>  <br/> |<span data-ttu-id="2bcea-139">Especifica las propiedades del grupo o la forma que se va a usar para la comparación.</span><span class="sxs-lookup"><span data-stu-id="2bcea-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="2bcea-140">Los valores posibles se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2bcea-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="2bcea-141">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2bcea-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2bcea-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="2bcea-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="2bcea-143">xsd: String</span><span class="sxs-lookup"><span data-stu-id="2bcea-143">xsd:string</span></span>  <br/> |<span data-ttu-id="2bcea-144">opcional</span><span class="sxs-lookup"><span data-stu-id="2bcea-144">optional</span></span>  <br/> |<span data-ttu-id="2bcea-145">Si el valor de ContextType es 2 o 3, este atributo es necesario para definir una comparación.</span><span class="sxs-lookup"><span data-stu-id="2bcea-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="2bcea-146">Para ContextType = 2, ContextTypeLabel debe ser la etiqueta del elemento de datos de formas y si **ContextType** = 3, ContextTypeLabel debe ser el nombre de fila local.</span><span class="sxs-lookup"><span data-stu-id="2bcea-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="2bcea-147">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2bcea-147">Values of the xsd:string type.</span></span>  <br/> |
   

