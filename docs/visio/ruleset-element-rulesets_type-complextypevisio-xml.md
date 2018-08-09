---
title: Elemento RuleSet (RuleSets_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación del diagrama.
ms.openlocfilehash: ae8fc52dd665e51f38c7eeae2f12ff778937d565
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823085"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="de56f-103">Elemento RuleSet (RuleSets_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="de56f-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="de56f-104">Representa un conjunto de reglas de validación del diagrama.</span><span class="sxs-lookup"><span data-stu-id="de56f-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de56f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="de56f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de56f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="de56f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="de56f-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="de56f-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="de56f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="de56f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="de56f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="de56f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="de56f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="de56f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="de56f-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="de56f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="de56f-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="de56f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de56f-113">Definición</span><span class="sxs-lookup"><span data-stu-id="de56f-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="de56f-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="de56f-114">Elements and attributes</span></span>

<span data-ttu-id="de56f-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="de56f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="de56f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="de56f-116">Parent elements</span></span>

|<span data-ttu-id="de56f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="de56f-117">**Element**</span></span>|<span data-ttu-id="de56f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="de56f-118">**Type**</span></span>|<span data-ttu-id="de56f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de56f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de56f-120">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="de56f-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de56f-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="de56f-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de56f-122">Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="de56f-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="de56f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="de56f-123">Child elements</span></span>

|<span data-ttu-id="de56f-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="de56f-124">**Element**</span></span>|<span data-ttu-id="de56f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="de56f-125">**Type**</span></span>|<span data-ttu-id="de56f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de56f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de56f-127">Rule</span><span class="sxs-lookup"><span data-stu-id="de56f-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de56f-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="de56f-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de56f-129">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="de56f-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="de56f-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="de56f-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de56f-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="de56f-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de56f-132">Especifica las propiedades del conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="de56f-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="de56f-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="de56f-133">Attributes</span></span>

|<span data-ttu-id="de56f-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="de56f-134">**Attribute**</span></span>|<span data-ttu-id="de56f-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="de56f-135">**Type**</span></span>|<span data-ttu-id="de56f-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="de56f-136">**Required**</span></span>|<span data-ttu-id="de56f-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="de56f-137">**Description**</span></span>|<span data-ttu-id="de56f-138">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="de56f-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="de56f-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="de56f-139">Description</span></span>  <br/> |<span data-ttu-id="de56f-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="de56f-140">xsd:string</span></span>  <br/> |<span data-ttu-id="de56f-141">opcional</span><span class="sxs-lookup"><span data-stu-id="de56f-141">optional</span></span>  <br/> |<span data-ttu-id="de56f-142">Especifica la descripción que aparece en la interfaz de usuario para el conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="de56f-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="de56f-143">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="de56f-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="de56f-144">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="de56f-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="de56f-145">Habilitado</span><span class="sxs-lookup"><span data-stu-id="de56f-145">Enabled</span></span>  <br/> |<span data-ttu-id="de56f-146">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="de56f-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="de56f-147">opcional</span><span class="sxs-lookup"><span data-stu-id="de56f-147">optional</span></span>  <br/> |<span data-ttu-id="de56f-148">Especifica si se comprueban las reglas en el conjunto de reglas de validación especificado cuando se desencadena la validación para el documento actual.</span><span class="sxs-lookup"><span data-stu-id="de56f-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="de56f-149">Valor predeterminado es True.</span><span class="sxs-lookup"><span data-stu-id="de56f-149">Default is True.</span></span>  <br/> |<span data-ttu-id="de56f-150">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="de56f-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="de56f-151">ID</span><span class="sxs-lookup"><span data-stu-id="de56f-151">ID</span></span>  <br/> |<span data-ttu-id="de56f-152">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="de56f-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="de56f-153">necesario</span><span class="sxs-lookup"><span data-stu-id="de56f-153">required</span></span>  <br/> |<span data-ttu-id="de56f-154">Especifica el identificador único del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="de56f-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="de56f-155">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="de56f-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="de56f-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="de56f-156">Name</span></span>  <br/> |<span data-ttu-id="de56f-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="de56f-157">xsd:string</span></span>  <br/> |<span data-ttu-id="de56f-158">opcional</span><span class="sxs-lookup"><span data-stu-id="de56f-158">optional</span></span>  <br/> |<span data-ttu-id="de56f-159">Especifica el nombre local del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="de56f-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="de56f-160">El valor predeterminado es el valor del atributo de NameU.</span><span class="sxs-lookup"><span data-stu-id="de56f-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="de56f-161">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="de56f-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="de56f-162">NameU</span><span class="sxs-lookup"><span data-stu-id="de56f-162">NameU</span></span>  <br/> |<span data-ttu-id="de56f-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="de56f-163">xsd:string</span></span>  <br/> |<span data-ttu-id="de56f-164">necesario</span><span class="sxs-lookup"><span data-stu-id="de56f-164">required</span></span>  <br/> |<span data-ttu-id="de56f-165">Especifica el nombre universal del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="de56f-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="de56f-166">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="de56f-166">Values of the xsd:string type.</span></span>  <br/> |
   

