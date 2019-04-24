---
title: Elemento RuleInfo (complexType Issue_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica información sobre la regla de validación a la que se refiere el problema de validación primario.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356990"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="d2968-103">Elemento RuleInfo (complexType Issue_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="d2968-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d2968-104">Especifica información sobre la regla de validación a la que se refiere el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="d2968-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2968-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d2968-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2968-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d2968-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d2968-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="d2968-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d2968-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d2968-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d2968-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d2968-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d2968-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d2968-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d2968-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="d2968-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d2968-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="d2968-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d2968-113">Definición</span><span class="sxs-lookup"><span data-stu-id="d2968-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d2968-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d2968-114">Elements and attributes</span></span>

<span data-ttu-id="d2968-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d2968-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d2968-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d2968-116">Parent elements</span></span>

|<span data-ttu-id="d2968-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d2968-117">**Element**</span></span>|<span data-ttu-id="d2968-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d2968-118">**Type**</span></span>|<span data-ttu-id="d2968-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2968-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d2968-120">Problema</span><span class="sxs-lookup"><span data-stu-id="d2968-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d2968-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="d2968-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d2968-122">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="d2968-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d2968-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d2968-123">Child elements</span></span>

<span data-ttu-id="d2968-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2968-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2968-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2968-125">Attributes</span></span>

|<span data-ttu-id="d2968-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d2968-126">**Attribute**</span></span>|<span data-ttu-id="d2968-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d2968-127">**Type**</span></span>|<span data-ttu-id="d2968-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d2968-128">**Required**</span></span>|<span data-ttu-id="d2968-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2968-129">**Description**</span></span>|<span data-ttu-id="d2968-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d2968-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d2968-131">RuleID</span><span class="sxs-lookup"><span data-stu-id="d2968-131">RuleID</span></span>  <br/> |<span data-ttu-id="d2968-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d2968-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d2968-133">necesario</span><span class="sxs-lookup"><span data-stu-id="d2968-133">required</span></span>  <br/> |<span data-ttu-id="d2968-134">Especifica el identificador único de la regla de validación a la que se refiere el problema primario.</span><span class="sxs-lookup"><span data-stu-id="d2968-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="d2968-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d2968-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d2968-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="d2968-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="d2968-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d2968-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d2968-138">necesario</span><span class="sxs-lookup"><span data-stu-id="d2968-138">required</span></span>  <br/> |<span data-ttu-id="d2968-139">Especifica el identificador único del conjunto de reglas de validación al que se refiere el problema primario.</span><span class="sxs-lookup"><span data-stu-id="d2968-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="d2968-140">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d2968-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

