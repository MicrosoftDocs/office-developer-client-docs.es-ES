---
title: Elemento RuleSets (Validation_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Incluye un elemento de conjunto de reglas para cada regla de validación establecida en el documento.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399644"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="083e6-103">Elemento RuleSets (Validation_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="083e6-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="083e6-104">Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="083e6-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="083e6-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="083e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="083e6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="083e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="083e6-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="083e6-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="083e6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="083e6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="083e6-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="083e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="083e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="083e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="083e6-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="083e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="083e6-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="083e6-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="083e6-113">Definición</span><span class="sxs-lookup"><span data-stu-id="083e6-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="083e6-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="083e6-114">Elements and attributes</span></span>

<span data-ttu-id="083e6-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="083e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="083e6-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="083e6-116">Parent elements</span></span>

|<span data-ttu-id="083e6-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="083e6-117">**Element**</span></span>|<span data-ttu-id="083e6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="083e6-118">**Type**</span></span>|<span data-ttu-id="083e6-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="083e6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="083e6-120">Validación</span><span class="sxs-lookup"><span data-stu-id="083e6-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="083e6-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="083e6-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="083e6-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="083e6-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="083e6-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="083e6-123">Child elements</span></span>

|<span data-ttu-id="083e6-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="083e6-124">**Element**</span></span>|<span data-ttu-id="083e6-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="083e6-125">**Type**</span></span>|<span data-ttu-id="083e6-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="083e6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="083e6-127">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="083e6-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="083e6-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="083e6-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="083e6-129">Representa un conjunto de reglas de validación del diagrama.</span><span class="sxs-lookup"><span data-stu-id="083e6-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="083e6-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="083e6-130">Attributes</span></span>

<span data-ttu-id="083e6-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="083e6-131">None.</span></span>
  

