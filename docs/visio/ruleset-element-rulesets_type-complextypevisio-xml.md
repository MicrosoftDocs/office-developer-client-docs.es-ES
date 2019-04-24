---
title: Elemento RuleSet (RuleSets_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ca63b8a-782e-211f-be7a-8e177b61d8fc
description: Representa un conjunto de reglas de validación de diagrama.
ms.openlocfilehash: 1231e8cdb3c8781dc47f470c0477b4585b1331c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318917"
---
# <a name="ruleset-element-rulesetstype-complextype-visio-xml"></a><span data-ttu-id="34d94-103">Elemento RuleSet (RuleSets_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="34d94-103">RuleSet element (RuleSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="34d94-104">Representa un conjunto de reglas de validación de diagrama.</span><span class="sxs-lookup"><span data-stu-id="34d94-104">Represents one set of diagram-validation rules.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34d94-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="34d94-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34d94-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="34d94-106">**Element type**</span></span> <br/> |[<span data-ttu-id="34d94-107">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="34d94-107">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="34d94-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="34d94-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="34d94-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="34d94-109">**Schema file**</span></span> <br/> |<span data-ttu-id="34d94-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="34d94-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="34d94-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="34d94-111">**Document parts**</span></span> <br/> |<span data-ttu-id="34d94-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="34d94-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="34d94-113">Definición</span><span class="sxs-lookup"><span data-stu-id="34d94-113">Definition</span></span>

```XML
< xs:element name="RuleSet" type="RuleSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="34d94-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="34d94-114">Elements and attributes</span></span>

<span data-ttu-id="34d94-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="34d94-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="34d94-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="34d94-116">Parent elements</span></span>

|<span data-ttu-id="34d94-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="34d94-117">**Element**</span></span>|<span data-ttu-id="34d94-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34d94-118">**Type**</span></span>|<span data-ttu-id="34d94-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34d94-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34d94-120">RuleSets</span><span class="sxs-lookup"><span data-stu-id="34d94-120">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34d94-121">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="34d94-121">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34d94-122">Incluye un elemento **ruleset** para cada conjunto de reglas de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="34d94-122">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="34d94-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34d94-123">Child elements</span></span>

|<span data-ttu-id="34d94-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="34d94-124">**Element**</span></span>|<span data-ttu-id="34d94-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34d94-125">**Type**</span></span>|<span data-ttu-id="34d94-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34d94-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="34d94-127">Rule</span><span class="sxs-lookup"><span data-stu-id="34d94-127">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34d94-128">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="34d94-128">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34d94-129">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="34d94-129">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
|[<span data-ttu-id="34d94-130">RuleSetFlags</span><span class="sxs-lookup"><span data-stu-id="34d94-130">RuleSetFlags</span></span>](rulesetflags-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="34d94-131">RuleSetFlags_Type</span><span class="sxs-lookup"><span data-stu-id="34d94-131">RuleSetFlags_Type</span></span>](rulesetflags_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="34d94-132">Especifica las propiedades del conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="34d94-132">Specifies rule-set properties.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="34d94-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="34d94-133">Attributes</span></span>

|<span data-ttu-id="34d94-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="34d94-134">**Attribute**</span></span>|<span data-ttu-id="34d94-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="34d94-135">**Type**</span></span>|<span data-ttu-id="34d94-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="34d94-136">**Required**</span></span>|<span data-ttu-id="34d94-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34d94-137">**Description**</span></span>|<span data-ttu-id="34d94-138">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="34d94-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="34d94-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="34d94-139">Description</span></span>  <br/> |<span data-ttu-id="34d94-140">xsd: String</span><span class="sxs-lookup"><span data-stu-id="34d94-140">xsd:string</span></span>  <br/> |<span data-ttu-id="34d94-141">opcional</span><span class="sxs-lookup"><span data-stu-id="34d94-141">optional</span></span>  <br/> |<span data-ttu-id="34d94-142">Especifica la descripción que aparece en la interfaz de usuario del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="34d94-142">Specifies the description that appears in the user interface for the validation rule set.</span></span> <span data-ttu-id="34d94-143">El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="34d94-143">Default is an empty string.</span></span>  <br/> |<span data-ttu-id="34d94-144">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34d94-144">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34d94-145">Habilitado</span><span class="sxs-lookup"><span data-stu-id="34d94-145">Enabled</span></span>  <br/> |<span data-ttu-id="34d94-146">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="34d94-146">xsd:boolean</span></span>  <br/> |<span data-ttu-id="34d94-147">opcional</span><span class="sxs-lookup"><span data-stu-id="34d94-147">optional</span></span>  <br/> |<span data-ttu-id="34d94-148">Especifica si se activan las reglas del conjunto de reglas de validación especificado cuando se desencadena la validación para el documento actual.</span><span class="sxs-lookup"><span data-stu-id="34d94-148">Specifies whether the rules in the specified validation rule set are checked when validation is triggered for the current document.</span></span> <span data-ttu-id="34d94-149">El valor predeterminado es TrueTrue.</span><span class="sxs-lookup"><span data-stu-id="34d94-149">Default is True.</span></span>  <br/> |<span data-ttu-id="34d94-150">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="34d94-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="34d94-151">ID</span><span class="sxs-lookup"><span data-stu-id="34d94-151">ID</span></span>  <br/> |<span data-ttu-id="34d94-152">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="34d94-152">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="34d94-153">necesario</span><span class="sxs-lookup"><span data-stu-id="34d94-153">required</span></span>  <br/> |<span data-ttu-id="34d94-154">Especifica el identificador único del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="34d94-154">Specifies the unique identifier of the validation rule set.</span></span>  <br/> |<span data-ttu-id="34d94-155">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="34d94-155">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="34d94-156">Nombre</span><span class="sxs-lookup"><span data-stu-id="34d94-156">Name</span></span>  <br/> |<span data-ttu-id="34d94-157">xsd: String</span><span class="sxs-lookup"><span data-stu-id="34d94-157">xsd:string</span></span>  <br/> |<span data-ttu-id="34d94-158">opcional</span><span class="sxs-lookup"><span data-stu-id="34d94-158">optional</span></span>  <br/> |<span data-ttu-id="34d94-159">Especifica el nombre local del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="34d94-159">Specifies the local name of the validation rule set.</span></span> <span data-ttu-id="34d94-160">El valor predeterminado del atributo NameU es.</span><span class="sxs-lookup"><span data-stu-id="34d94-160">Defaults to NameU attribute value.</span></span>  <br/> |<span data-ttu-id="34d94-161">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34d94-161">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="34d94-162">NameU</span><span class="sxs-lookup"><span data-stu-id="34d94-162">NameU</span></span>  <br/> |<span data-ttu-id="34d94-163">xsd: String</span><span class="sxs-lookup"><span data-stu-id="34d94-163">xsd:string</span></span>  <br/> |<span data-ttu-id="34d94-164">necesario</span><span class="sxs-lookup"><span data-stu-id="34d94-164">required</span></span>  <br/> |<span data-ttu-id="34d94-165">Especifica el nombre universal del conjunto de reglas de validación.</span><span class="sxs-lookup"><span data-stu-id="34d94-165">Specifies the universal name of the validation rule set.</span></span>  <br/> |<span data-ttu-id="34d94-166">Valores del tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="34d94-166">Values of the xsd:string type.</span></span>  <br/> |
   

