---
title: Elemento rule (RuleSet_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fcd22f3a-c8e8-1133-160c-fe26e612a15d
description: Representa una regla de validación única en un conjunto de reglas de validación de diagramas.
ms.openlocfilehash: 92d52456164b89ff2aad31fa8d8f02f818c8bd1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358803"
---
# <a name="rule-element-rulesettype-complextype-visio-xml"></a><span data-ttu-id="477e5-103">Elemento rule (RuleSet_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="477e5-103">Rule element (RuleSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="477e5-104">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="477e5-104">Represents a single validation rule in a diagram validation rule set.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="477e5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="477e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="477e5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="477e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="477e5-107">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="477e5-107">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="477e5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="477e5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="477e5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="477e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="477e5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="477e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="477e5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="477e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="477e5-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="477e5-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="477e5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="477e5-113">Definition</span></span>

```XML
< xs:element name="Rule" type="Rule_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="477e5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="477e5-114">Elements and attributes</span></span>

<span data-ttu-id="477e5-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="477e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="477e5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="477e5-116">Parent elements</span></span>

|<span data-ttu-id="477e5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="477e5-117">**Element**</span></span>|<span data-ttu-id="477e5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="477e5-118">**Type**</span></span>|<span data-ttu-id="477e5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="477e5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="477e5-120">RuleSet</span><span class="sxs-lookup"><span data-stu-id="477e5-120">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="477e5-121">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="477e5-121">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="477e5-122">Representa un conjunto de reglas de validación de diagrama.</span><span class="sxs-lookup"><span data-stu-id="477e5-122">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="477e5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="477e5-123">Child elements</span></span>

|<span data-ttu-id="477e5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="477e5-124">**Element**</span></span>|<span data-ttu-id="477e5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="477e5-125">**Type**</span></span>|<span data-ttu-id="477e5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="477e5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="477e5-127">RuleFilter</span><span class="sxs-lookup"><span data-stu-id="477e5-127">RuleFilter</span></span>](rulefilter-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="477e5-128">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="477e5-128">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="477e5-129">Especifica la expresión lógica que determina si la regla de validación debe aplicarse a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="477e5-129">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>  <br/> |
|[<span data-ttu-id="477e5-130">Msdnprobar</span><span class="sxs-lookup"><span data-stu-id="477e5-130">RuleTest</span></span>](ruletest-element-rule_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="477e5-131">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="477e5-131">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="477e5-132">Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="477e5-132">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="477e5-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="477e5-133">Attributes</span></span>

|<span data-ttu-id="477e5-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="477e5-134">**Attribute**</span></span>|<span data-ttu-id="477e5-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="477e5-135">**Type**</span></span>|<span data-ttu-id="477e5-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="477e5-136">**Required**</span></span>|<span data-ttu-id="477e5-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="477e5-137">**Description**</span></span>|<span data-ttu-id="477e5-138">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="477e5-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="477e5-139">Categoría</span><span class="sxs-lookup"><span data-stu-id="477e5-139">Category</span></span>  <br/> |<span data-ttu-id="477e5-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="477e5-140">xsd:string</span></span>  <br/> |<span data-ttu-id="477e5-141">opcional</span><span class="sxs-lookup"><span data-stu-id="477e5-141">optional</span></span>  <br/> |<span data-ttu-id="477e5-142">Especifica el texto que se muestra en la columna **categoría** de la ventana problemas.</span><span class="sxs-lookup"><span data-stu-id="477e5-142">Specifies the text displayed in the **Category** column of the Issues window.</span></span> <span data-ttu-id="477e5-143">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="477e5-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="477e5-144">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="477e5-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="477e5-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="477e5-145">Description</span></span>  <br/> |<span data-ttu-id="477e5-146">xsd: String</span><span class="sxs-lookup"><span data-stu-id="477e5-146">xsd:string</span></span>  <br/> |<span data-ttu-id="477e5-147">opcional</span><span class="sxs-lookup"><span data-stu-id="477e5-147">optional</span></span>  <br/> |<span data-ttu-id="477e5-148">Especifica la descripción de la regla de validación que aparece en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="477e5-148">Specifies the description of the validation rule that appears in the user interface.</span></span> <span data-ttu-id="477e5-149">El valor predeterminado es "Unknown".</span><span class="sxs-lookup"><span data-stu-id="477e5-149">Default is "Unknown".</span></span>  <br/> |<span data-ttu-id="477e5-150">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="477e5-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="477e5-151">ID</span><span class="sxs-lookup"><span data-stu-id="477e5-151">ID</span></span>  <br/> |<span data-ttu-id="477e5-152">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="477e5-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="477e5-153">necesario</span><span class="sxs-lookup"><span data-stu-id="477e5-153">required</span></span>  <br/> |<span data-ttu-id="477e5-154">Especifica el identificador único para la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="477e5-154">Specifies the unique identifier for the validation rule.</span></span>  <br/> |<span data-ttu-id="477e5-155">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="477e5-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="477e5-156">Ignored</span><span class="sxs-lookup"><span data-stu-id="477e5-156">Ignored</span></span>  <br/> |<span data-ttu-id="477e5-157">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="477e5-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="477e5-158">opcional</span><span class="sxs-lookup"><span data-stu-id="477e5-158">optional</span></span>  <br/> |<span data-ttu-id="477e5-159">Especifica si la regla de validación se ignora actualmente.</span><span class="sxs-lookup"><span data-stu-id="477e5-159">Specifies whether the validation rule is currently ignored.</span></span> <span data-ttu-id="477e5-160">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="477e5-160">Default is False.</span></span>  <br/> |<span data-ttu-id="477e5-161">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="477e5-161">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="477e5-162">NameU</span><span class="sxs-lookup"><span data-stu-id="477e5-162">NameU</span></span>  <br/> |<span data-ttu-id="477e5-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="477e5-163">xsd:string</span></span>  <br/> |<span data-ttu-id="477e5-164">necesario</span><span class="sxs-lookup"><span data-stu-id="477e5-164">required</span></span>  <br/> |<span data-ttu-id="477e5-165">Especifica el nombre universal de la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="477e5-165">Specifies the universal name of the validation rule.</span></span>  <br/> |<span data-ttu-id="477e5-166">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="477e5-166">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="477e5-167">RuleTarget</span><span class="sxs-lookup"><span data-stu-id="477e5-167">RuleTarget</span></span>  <br/> |<span data-ttu-id="477e5-168">xsd: int</span><span class="sxs-lookup"><span data-stu-id="477e5-168">xsd:int</span></span>  <br/> |<span data-ttu-id="477e5-169">opcional</span><span class="sxs-lookup"><span data-stu-id="477e5-169">optional</span></span>  <br/> |<span data-ttu-id="477e5-170">Especifica el tipo de objeto al que se aplica la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="477e5-170">Specifies the type of object to which the validation rule applies.</span></span>  <br/> |<span data-ttu-id="477e5-171">Valores del tipo xsd: int.</span><span class="sxs-lookup"><span data-stu-id="477e5-171">Values of the xsd:int type.</span></span>  <br/> |
   

