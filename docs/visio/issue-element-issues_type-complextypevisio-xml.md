---
title: Elemento Issue (complexType Issues_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa un único problema de validación en el documento.
ms.openlocfilehash: 4ebe7d2d8b2b4627fb9c9e12113ef23ce19db52e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317909"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="9c6f5-103">Elemento Issue (complexType Issues_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="9c6f5-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9c6f5-104">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c6f5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9c6f5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c6f5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9c6f5-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="9c6f5-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9c6f5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9c6f5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9c6f5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="9c6f5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9c6f5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9c6f5-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="9c6f5-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9c6f5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9c6f5-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9c6f5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9c6f5-114">Elements and attributes</span></span>

<span data-ttu-id="9c6f5-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9c6f5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9c6f5-116">Parent elements</span></span>

|<span data-ttu-id="9c6f5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-117">**Element**</span></span>|<span data-ttu-id="9c6f5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-118">**Type**</span></span>|<span data-ttu-id="9c6f5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c6f5-120">Issues</span><span class="sxs-lookup"><span data-stu-id="9c6f5-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c6f5-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="9c6f5-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c6f5-122">Contiene todos los elementos **Issue** del documento.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c6f5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9c6f5-123">Child elements</span></span>

|<span data-ttu-id="9c6f5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-124">**Element**</span></span>|<span data-ttu-id="9c6f5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-125">**Type**</span></span>|<span data-ttu-id="9c6f5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9c6f5-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="9c6f5-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c6f5-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="9c6f5-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c6f5-129">Según el destino del problema de validación principal, especifica la página, o bien la página y la forma, asociadas con el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="9c6f5-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="9c6f5-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9c6f5-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="9c6f5-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9c6f5-132">Especifica información sobre la regla de validación a la que se refiere el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9c6f5-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="9c6f5-133">Attributes</span></span>

|<span data-ttu-id="9c6f5-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-134">**Attribute**</span></span>|<span data-ttu-id="9c6f5-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-135">**Type**</span></span>|<span data-ttu-id="9c6f5-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-136">**Required**</span></span>|<span data-ttu-id="9c6f5-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-137">**Description**</span></span>|<span data-ttu-id="9c6f5-138">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="9c6f5-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9c6f5-139">ID</span><span class="sxs-lookup"><span data-stu-id="9c6f5-139">ID</span></span>  <br/> |<span data-ttu-id="9c6f5-140">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9c6f5-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9c6f5-141">necesario</span><span class="sxs-lookup"><span data-stu-id="9c6f5-141">required</span></span>  <br/> |<span data-ttu-id="9c6f5-142">Especifica el identificador único del problema de validación.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="9c6f5-143">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9c6f5-144">Ignored</span><span class="sxs-lookup"><span data-stu-id="9c6f5-144">Ignored</span></span>  <br/> |<span data-ttu-id="9c6f5-145">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="9c6f5-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9c6f5-146">opcional</span><span class="sxs-lookup"><span data-stu-id="9c6f5-146">optional</span></span>  <br/> |<span data-ttu-id="9c6f5-147">Especifica información sobre la regla de validación a la que se refiere el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="9c6f5-148">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="9c6f5-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

