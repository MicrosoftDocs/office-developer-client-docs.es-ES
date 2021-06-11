---
title: Elemento RuleSets (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Incluye un elemento RuleSet para cada regla de validación establecida en el documento.
ms.openlocfilehash: 0aca3f52bd8b201d1afc2ab7d647757452ff8899
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541578"
---
# <a name="rulesets-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="4763f-103">Elemento RuleSets (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4763f-103">RuleSets element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4763f-104">Incluye un **elemento RuleSet** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="4763f-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4763f-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4763f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4763f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4763f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4763f-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="4763f-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4763f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4763f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4763f-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4763f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4763f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4763f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4763f-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4763f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4763f-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="4763f-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4763f-113">Definición</span><span class="sxs-lookup"><span data-stu-id="4763f-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4763f-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4763f-114">Elements and attributes</span></span>

<span data-ttu-id="4763f-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4763f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4763f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4763f-116">Parent elements</span></span>

|<span data-ttu-id="4763f-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4763f-117">**Element**</span></span>|<span data-ttu-id="4763f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4763f-118">**Type**</span></span>|<span data-ttu-id="4763f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4763f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4763f-120">Validation</span><span class="sxs-lookup"><span data-stu-id="4763f-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="4763f-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="4763f-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4763f-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="4763f-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4763f-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4763f-123">Child elements</span></span>

|<span data-ttu-id="4763f-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4763f-124">**Element**</span></span>|<span data-ttu-id="4763f-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4763f-125">**Type**</span></span>|<span data-ttu-id="4763f-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4763f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4763f-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="4763f-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4763f-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="4763f-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4763f-129">Representa un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="4763f-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4763f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="4763f-130">Attributes</span></span>

<span data-ttu-id="4763f-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4763f-131">None.</span></span>
  

