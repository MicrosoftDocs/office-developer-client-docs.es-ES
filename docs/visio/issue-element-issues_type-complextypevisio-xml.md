---
title: Elemento Issue (Issues_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa un único problema de validación en el documento.
ms.openlocfilehash: 73c83fe47ebf9921686ea7b35c5f94a06b803623
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541130"
---
# <a name="issue-element-issues_type-complextype-visio-xml"></a><span data-ttu-id="13598-103">Elemento Issue (Issues_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="13598-103">Issue element (Issues_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="13598-104">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="13598-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13598-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13598-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13598-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="13598-106">**Element type**</span></span> <br/> |[<span data-ttu-id="13598-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="13598-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="13598-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13598-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="13598-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="13598-109">**Schema file**</span></span> <br/> |<span data-ttu-id="13598-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="13598-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="13598-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="13598-111">**Document parts**</span></span> <br/> |<span data-ttu-id="13598-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="13598-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13598-113">Definición</span><span class="sxs-lookup"><span data-stu-id="13598-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="13598-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="13598-114">Elements and attributes</span></span>

<span data-ttu-id="13598-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="13598-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="13598-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13598-116">Parent elements</span></span>

|<span data-ttu-id="13598-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13598-117">**Element**</span></span>|<span data-ttu-id="13598-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13598-118">**Type**</span></span>|<span data-ttu-id="13598-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13598-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13598-120">Issues</span><span class="sxs-lookup"><span data-stu-id="13598-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13598-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="13598-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="13598-122">Contiene todos los **elementos Issue** del documento.</span><span class="sxs-lookup"><span data-stu-id="13598-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13598-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13598-123">Child elements</span></span>

|<span data-ttu-id="13598-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13598-124">**Element**</span></span>|<span data-ttu-id="13598-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13598-125">**Type**</span></span>|<span data-ttu-id="13598-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13598-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13598-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="13598-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13598-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="13598-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="13598-129">Según el destino del problema de validación principal, especifica la página o la página y la forma asociadas con el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="13598-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="13598-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="13598-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="13598-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="13598-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="13598-132">Especifica información sobre la regla de validación a la que pertenece el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="13598-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="13598-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="13598-133">Attributes</span></span>

|<span data-ttu-id="13598-134">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="13598-134">**Attribute**</span></span>|<span data-ttu-id="13598-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13598-135">**Type**</span></span>|<span data-ttu-id="13598-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="13598-136">**Required**</span></span>|<span data-ttu-id="13598-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13598-137">**Description**</span></span>|<span data-ttu-id="13598-138">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="13598-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13598-139">ID</span><span class="sxs-lookup"><span data-stu-id="13598-139">ID</span></span>  <br/> |<span data-ttu-id="13598-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13598-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13598-141">necesario</span><span class="sxs-lookup"><span data-stu-id="13598-141">required</span></span>  <br/> |<span data-ttu-id="13598-142">Especifica el identificador único del problema de validación.</span><span class="sxs-lookup"><span data-stu-id="13598-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="13598-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13598-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13598-144">Omitido</span><span class="sxs-lookup"><span data-stu-id="13598-144">Ignored</span></span>  <br/> |<span data-ttu-id="13598-145">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="13598-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13598-146">opcional</span><span class="sxs-lookup"><span data-stu-id="13598-146">optional</span></span>  <br/> |<span data-ttu-id="13598-147">Especifica información sobre la regla de validación a la que pertenece el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="13598-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="13598-148">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="13598-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

