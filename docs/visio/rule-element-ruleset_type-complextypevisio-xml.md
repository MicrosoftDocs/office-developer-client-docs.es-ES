---
title: Elemento rule (RuleSet_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
ms.openlocfilehash: feae283c624bdece98dbc1136b0fe8765d911e12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823065"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="9cd25-103">Elemento rule (RuleSet_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="9cd25-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9cd25-104">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="9cd25-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9cd25-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9cd25-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cd25-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9cd25-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9cd25-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="9cd25-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9cd25-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9cd25-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9cd25-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9cd25-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9cd25-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9cd25-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9cd25-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9cd25-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9cd25-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="9cd25-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9cd25-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9cd25-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9cd25-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9cd25-114">Elements and attributes</span></span>

<span data-ttu-id="9cd25-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="9cd25-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9cd25-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9cd25-116">Parent elements</span></span>

|<span data-ttu-id="9cd25-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9cd25-117">**Element**</span></span>|<span data-ttu-id="9cd25-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9cd25-118">**Type**</span></span>|<span data-ttu-id="9cd25-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9cd25-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9cd25-120">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="9cd25-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9cd25-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9cd25-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9cd25-122">Representa un conjunto de reglas de validación del diagrama.</span><span class="sxs-lookup"><span data-stu-id="9cd25-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9cd25-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9cd25-123">Child elements</span></span>

|<span data-ttu-id="9cd25-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9cd25-124">**Element**</span></span>|<span data-ttu-id="9cd25-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9cd25-125">**Type**</span></span>|<span data-ttu-id="9cd25-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9cd25-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9cd25-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="9cd25-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9cd25-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="9cd25-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9cd25-129">Especifica la expresión lógica que determina si se debe aplicar la regla de validación para un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="9cd25-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="9cd25-130">RuleTest</span><span class="sxs-lookup"><span data-stu-id="9cd25-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9cd25-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="9cd25-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9cd25-132">Especifica la expresión lógica que determina si el objeto de destino satisface la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="9cd25-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9cd25-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="9cd25-133">Attributes</span></span>

|<span data-ttu-id="9cd25-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9cd25-134">**Attribute**</span></span>|<span data-ttu-id="9cd25-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9cd25-135">**Type**</span></span>|<span data-ttu-id="9cd25-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9cd25-136">**Required**</span></span>|<span data-ttu-id="9cd25-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9cd25-137">**Description**</span></span>|<span data-ttu-id="9cd25-138">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="9cd25-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9cd25-139">Category</span><span class="sxs-lookup"><span data-stu-id="9cd25-139">Category</span></span>  <br/> |<span data-ttu-id="9cd25-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9cd25-140">xsd:string</span></span>  <br/> |<span data-ttu-id="9cd25-141">opcional</span><span class="sxs-lookup"><span data-stu-id="9cd25-141">optional</span></span>  <br/> |<span data-ttu-id="9cd25-142">Especifica el texto que aparece en la columna de **categoría** de la ventana problemas.</span><span class="sxs-lookup"><span data-stu-id="9cd25-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="9cd25-143">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="9cd25-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="9cd25-144">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9cd25-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cd25-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cd25-145">Description</span></span>  <br/> |<span data-ttu-id="9cd25-146">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9cd25-146">xsd:string</span></span>  <br/> |<span data-ttu-id="9cd25-147">opcional</span><span class="sxs-lookup"><span data-stu-id="9cd25-147">optional</span></span>  <br/> |<span data-ttu-id="9cd25-148">Especifica la descripción de la regla de validación que aparece en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9cd25-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="9cd25-149">Valor predeterminado es "Unknown".</span><span class="sxs-lookup"><span data-stu-id="9cd25-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="9cd25-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9cd25-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cd25-151">id.</span><span class="sxs-lookup"><span data-stu-id="9cd25-151">ID</span></span>  <br/> |<span data-ttu-id="9cd25-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9cd25-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9cd25-153">necesario</span><span class="sxs-lookup"><span data-stu-id="9cd25-153">required</span></span>  <br/> |<span data-ttu-id="9cd25-154">Especifica el identificador único para la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="9cd25-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="9cd25-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9cd25-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9cd25-156">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="9cd25-156">Ignored</span></span>  <br/> |<span data-ttu-id="9cd25-157">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="9cd25-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9cd25-158">opcional</span><span class="sxs-lookup"><span data-stu-id="9cd25-158">optional</span></span>  <br/> |<span data-ttu-id="9cd25-159">Especifica si la regla de validación actualmente se omite.</span><span class="sxs-lookup"><span data-stu-id="9cd25-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="9cd25-160">Valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="9cd25-160">Default is False.</span></span>  <br/> |<span data-ttu-id="9cd25-161">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="9cd25-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9cd25-162">NameU</span><span class="sxs-lookup"><span data-stu-id="9cd25-162">NameU</span></span>  <br/> |<span data-ttu-id="9cd25-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9cd25-163">xsd:string</span></span>  <br/> |<span data-ttu-id="9cd25-164">necesario</span><span class="sxs-lookup"><span data-stu-id="9cd25-164">required</span></span>  <br/> |<span data-ttu-id="9cd25-165">Especifica el nombre universal de la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="9cd25-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="9cd25-166">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="9cd25-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9cd25-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="9cd25-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="9cd25-168">xsd: int</span><span class="sxs-lookup"><span data-stu-id="9cd25-168">xsd:int</span></span>  <br/> |<span data-ttu-id="9cd25-169">opcional</span><span class="sxs-lookup"><span data-stu-id="9cd25-169">optional</span></span>  <br/> |<span data-ttu-id="9cd25-170">Especifica el tipo de objeto al que se aplica la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="9cd25-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="9cd25-171">Valores del tipo XSD: int.</span><span class="sxs-lookup"><span data-stu-id="9cd25-171">Values of the xsd:int type.</span></span>  <br/> |
   

