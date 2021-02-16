---
title: Elemento RuleInfo (Issue_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica información sobre la regla de validación a la que pertenece el problema de validación principal.
ms.openlocfilehash: 29454fdb82d9e12d46fa9eedf73f8a31e8befd95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541690"
---
# <a name="ruleinfo-element-issue_type-complextype-visio-xml"></a><span data-ttu-id="f6276-103">Elemento RuleInfo (Issue_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="f6276-103">RuleInfo element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f6276-104">Especifica información sobre la regla de validación a la que pertenece el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="f6276-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6276-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f6276-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6276-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f6276-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f6276-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="f6276-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6276-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f6276-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6276-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f6276-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f6276-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f6276-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6276-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f6276-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f6276-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="f6276-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f6276-113">Definición</span><span class="sxs-lookup"><span data-stu-id="f6276-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6276-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f6276-114">Elements and attributes</span></span>

<span data-ttu-id="f6276-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="f6276-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6276-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f6276-116">Parent elements</span></span>

|<span data-ttu-id="f6276-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f6276-117">**Element**</span></span>|<span data-ttu-id="f6276-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f6276-118">**Type**</span></span>|<span data-ttu-id="f6276-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6276-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6276-120">Problema</span><span class="sxs-lookup"><span data-stu-id="f6276-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f6276-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="f6276-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6276-122">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="f6276-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6276-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f6276-123">Child elements</span></span>

<span data-ttu-id="f6276-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f6276-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6276-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="f6276-125">Attributes</span></span>

|<span data-ttu-id="f6276-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f6276-126">**Attribute**</span></span>|<span data-ttu-id="f6276-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f6276-127">**Type**</span></span>|<span data-ttu-id="f6276-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="f6276-128">**Required**</span></span>|<span data-ttu-id="f6276-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6276-129">**Description**</span></span>|<span data-ttu-id="f6276-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="f6276-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6276-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="f6276-131">RuleID</span></span>  <br/> |<span data-ttu-id="f6276-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f6276-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f6276-133">necesario</span><span class="sxs-lookup"><span data-stu-id="f6276-133">required</span></span>  <br/> |<span data-ttu-id="f6276-134">Especifica el identificador único de la regla de validación a la que pertenece el problema primario.</span><span class="sxs-lookup"><span data-stu-id="f6276-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="f6276-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f6276-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f6276-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="f6276-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="f6276-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f6276-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f6276-138">necesario</span><span class="sxs-lookup"><span data-stu-id="f6276-138">required</span></span>  <br/> |<span data-ttu-id="f6276-139">Especifica el identificador único del conjunto de reglas de validación al que pertenece el problema principal.</span><span class="sxs-lookup"><span data-stu-id="f6276-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="f6276-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f6276-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

