---
title: Elemento de problema (Issues_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5c4d07bf-4edc-e241-7827-017f96c11957
description: Representa un problema de validación único en el documento.
ms.openlocfilehash: 904b42c969bdf97fcfa1e34bad97f73242b17cc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822387"
---
# <a name="issue-element-issuestype-complextype-visio-xml"></a><span data-ttu-id="ebd26-103">Elemento de problema (Issues_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ebd26-103">Issue element (Issues_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ebd26-104">Representa un problema de validación único en el documento.</span><span class="sxs-lookup"><span data-stu-id="ebd26-104">Represents a single validation issue in the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebd26-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ebd26-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebd26-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ebd26-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ebd26-107">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="ebd26-107">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ebd26-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ebd26-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ebd26-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ebd26-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ebd26-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ebd26-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ebd26-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ebd26-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ebd26-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="ebd26-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ebd26-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ebd26-113">Definition</span></span>

```XML
< xs:element name="Issue" type="Issue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ebd26-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ebd26-114">Elements and attributes</span></span>

<span data-ttu-id="ebd26-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ebd26-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ebd26-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ebd26-116">Parent elements</span></span>

|<span data-ttu-id="ebd26-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebd26-117">**Element**</span></span>|<span data-ttu-id="ebd26-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ebd26-118">**Type**</span></span>|<span data-ttu-id="ebd26-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebd26-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ebd26-120">Problemas</span><span class="sxs-lookup"><span data-stu-id="ebd26-120">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ebd26-121">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="ebd26-121">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ebd26-122">Contiene todos los elementos de **problema** para el documento.</span><span class="sxs-lookup"><span data-stu-id="ebd26-122">Contains all the **Issue** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ebd26-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ebd26-123">Child elements</span></span>

|<span data-ttu-id="ebd26-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebd26-124">**Element**</span></span>|<span data-ttu-id="ebd26-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ebd26-125">**Type**</span></span>|<span data-ttu-id="ebd26-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebd26-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ebd26-127">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="ebd26-127">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ebd26-128">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="ebd26-128">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ebd26-129">Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="ebd26-129">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span>  <br/> |
|[<span data-ttu-id="ebd26-130">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="ebd26-130">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ebd26-131">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="ebd26-131">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ebd26-132">Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.</span><span class="sxs-lookup"><span data-stu-id="ebd26-132">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ebd26-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebd26-133">Attributes</span></span>

|<span data-ttu-id="ebd26-134">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ebd26-134">**Attribute**</span></span>|<span data-ttu-id="ebd26-135">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ebd26-135">**Type**</span></span>|<span data-ttu-id="ebd26-136">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ebd26-136">**Required**</span></span>|<span data-ttu-id="ebd26-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ebd26-137">**Description**</span></span>|<span data-ttu-id="ebd26-138">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ebd26-138">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ebd26-139">ID</span><span class="sxs-lookup"><span data-stu-id="ebd26-139">ID</span></span>  <br/> |<span data-ttu-id="ebd26-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ebd26-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ebd26-141">necesario</span><span class="sxs-lookup"><span data-stu-id="ebd26-141">required</span></span>  <br/> |<span data-ttu-id="ebd26-142">Especifica el identificador único del problema de validación.</span><span class="sxs-lookup"><span data-stu-id="ebd26-142">Specifies the unique identifier of the validation issue.</span></span>  <br/> |<span data-ttu-id="ebd26-143">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ebd26-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ebd26-144">Pasa por alto</span><span class="sxs-lookup"><span data-stu-id="ebd26-144">Ignored</span></span>  <br/> |<span data-ttu-id="ebd26-145">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="ebd26-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ebd26-146">opcional</span><span class="sxs-lookup"><span data-stu-id="ebd26-146">optional</span></span>  <br/> |<span data-ttu-id="ebd26-147">Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.</span><span class="sxs-lookup"><span data-stu-id="ebd26-147">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>  <br/> |<span data-ttu-id="ebd26-148">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="ebd26-148">Values of the xsd:boolean type.</span></span>  <br/> |
   

