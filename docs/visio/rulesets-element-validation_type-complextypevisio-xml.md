---
title: Elemento RuleSets (Validation_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Incluye un elemento de conjunto de reglas para cada regla de validación establecida en el documento.
ms.openlocfilehash: 84d64a8539f1b83c16a96a61ea68e9b2660c9036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823091"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="9038d-103">Elemento RuleSets (Validation_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="9038d-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9038d-104">Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="9038d-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9038d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9038d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9038d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="9038d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9038d-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="9038d-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9038d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9038d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9038d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9038d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9038d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9038d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9038d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="9038d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9038d-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="9038d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9038d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="9038d-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9038d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="9038d-114">Elements and attributes</span></span>

<span data-ttu-id="9038d-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="9038d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9038d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9038d-116">Parent elements</span></span>

|<span data-ttu-id="9038d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9038d-117">**Element**</span></span>|<span data-ttu-id="9038d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9038d-118">**Type**</span></span>|<span data-ttu-id="9038d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9038d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9038d-120">Validación</span><span class="sxs-lookup"><span data-stu-id="9038d-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="9038d-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="9038d-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9038d-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="9038d-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9038d-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9038d-123">Child elements</span></span>

|<span data-ttu-id="9038d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9038d-124">**Element**</span></span>|<span data-ttu-id="9038d-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9038d-125">**Type**</span></span>|<span data-ttu-id="9038d-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9038d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9038d-127">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="9038d-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9038d-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="9038d-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9038d-129">Representa un conjunto de reglas de validación del diagrama.</span><span class="sxs-lookup"><span data-stu-id="9038d-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="9038d-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="9038d-130">Attributes</span></span>

<span data-ttu-id="9038d-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9038d-131">None.</span></span>
  

