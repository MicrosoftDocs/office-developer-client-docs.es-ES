---
title: Elemento RuleSet (RuleSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación de diagramas.
ms.openlocfilehash: c6fc8df6d9c84f44496d69207dfb9cfb878659e3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541641"
---
# <a name="ruleset-element-rulesets_type-complextype-visio-xml"></a><span data-ttu-id="c1801-103">Elemento RuleSet (RuleSets_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c1801-103">RuleSet element (RuleSets_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c1801-104">Representa un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="c1801-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1801-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1801-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1801-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c1801-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1801-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="c1801-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1801-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c1801-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1801-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c1801-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1801-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c1801-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1801-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="c1801-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1801-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="c1801-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1801-113">Definición</span><span class="sxs-lookup"><span data-stu-id="c1801-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1801-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="c1801-114">Elements and attributes</span></span>

<span data-ttu-id="c1801-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="c1801-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1801-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1801-116">Parent elements</span></span>

|<span data-ttu-id="c1801-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1801-117">**Element**</span></span>|<span data-ttu-id="c1801-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1801-118">**Type**</span></span>|<span data-ttu-id="c1801-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1801-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1801-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="c1801-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1801-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="c1801-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1801-122">Incluye un **elemento RuleSet** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="c1801-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1801-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1801-123">Child elements</span></span>

|<span data-ttu-id="c1801-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c1801-124">**Element**</span></span>|<span data-ttu-id="c1801-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1801-125">**Type**</span></span>|<span data-ttu-id="c1801-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1801-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1801-127">Rule</span><span class="sxs-lookup"><span data-stu-id="c1801-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1801-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="c1801-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1801-129">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="c1801-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="c1801-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="c1801-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1801-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="c1801-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1801-132">Especifica las propiedades del conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="c1801-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1801-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1801-133">Attributes</span></span>

|<span data-ttu-id="c1801-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c1801-134">**Attribute**</span></span>|<span data-ttu-id="c1801-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c1801-135">**Type**</span></span>|<span data-ttu-id="c1801-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="c1801-136">**Required**</span></span>|<span data-ttu-id="c1801-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c1801-137">**Description**</span></span>|<span data-ttu-id="c1801-138">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="c1801-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c1801-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1801-139">Description</span></span>  <br/> |<span data-ttu-id="c1801-140">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1801-140">xsd:string</span></span>  <br/> |<span data-ttu-id="c1801-141">opcional</span><span class="sxs-lookup"><span data-stu-id="c1801-141">optional</span></span>  <br/> |<span data-ttu-id="c1801-142">Especifica la descripción que aparece en la interfaz de usuario del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="c1801-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="c1801-143">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c1801-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="c1801-144">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c1801-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1801-145">Habilitado</span><span class="sxs-lookup"><span data-stu-id="c1801-145">Enabled</span></span>  <br/> |<span data-ttu-id="c1801-146">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c1801-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c1801-147">opcional</span><span class="sxs-lookup"><span data-stu-id="c1801-147">optional</span></span>  <br/> |<span data-ttu-id="c1801-148">Especifica si las reglas del conjunto de reglas de validación especificado se comprueban cuando se desencadena la validación para el documento actual.</span><span class="sxs-lookup"><span data-stu-id="c1801-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="c1801-149">El valor predeterminado es TrueTrue.</span><span class="sxs-lookup"><span data-stu-id="c1801-149">Default is True.</span></span>  <br/> |<span data-ttu-id="c1801-150">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c1801-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c1801-151">ID</span><span class="sxs-lookup"><span data-stu-id="c1801-151">ID</span></span>  <br/> |<span data-ttu-id="c1801-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c1801-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c1801-153">necesario</span><span class="sxs-lookup"><span data-stu-id="c1801-153">required</span></span>  <br/> |<span data-ttu-id="c1801-154">Especifica el identificador único del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="c1801-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="c1801-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c1801-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c1801-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1801-156">Name</span></span>  <br/> |<span data-ttu-id="c1801-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1801-157">xsd:string</span></span>  <br/> |<span data-ttu-id="c1801-158">opcional</span><span class="sxs-lookup"><span data-stu-id="c1801-158">optional</span></span>  <br/> |<span data-ttu-id="c1801-159">Especifica el nombre local del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="c1801-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="c1801-160">El valor predeterminado es NameU attribute value.</span><span class="sxs-lookup"><span data-stu-id="c1801-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="c1801-161">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c1801-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c1801-162">NameU</span><span class="sxs-lookup"><span data-stu-id="c1801-162">NameU</span></span>  <br/> |<span data-ttu-id="c1801-163">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c1801-163">xsd:string</span></span>  <br/> |<span data-ttu-id="c1801-164">necesario</span><span class="sxs-lookup"><span data-stu-id="c1801-164">required</span></span>  <br/> |<span data-ttu-id="c1801-165">Especifica el nombre universal del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="c1801-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="c1801-166">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c1801-166">Values of the xsd:string type.</span></span>  <br/> |
   

