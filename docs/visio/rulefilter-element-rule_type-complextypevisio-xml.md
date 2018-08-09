---
title: Elemento de RuleFilter (Rule_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica la expresión lógica que determina si se debe aplicar la regla de validación para un objeto de destino.
ms.openlocfilehash: f2862fe4f4b6a644d80ca0393270594766d940be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823060"
---
# <a name="rulefilter-element-ruletype-complextype-visio-xml"></a><span data-ttu-id="b5212-103">Elemento de RuleFilter (Rule_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b5212-103">RuleFilter element (Rule_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b5212-104">Especifica la expresión lógica que determina si se debe aplicar la regla de validación para un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="b5212-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5212-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5212-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5212-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b5212-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5212-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="b5212-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5212-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b5212-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5212-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b5212-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5212-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b5212-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5212-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="b5212-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5212-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="b5212-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5212-113">Definición</span><span class="sxs-lookup"><span data-stu-id="b5212-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5212-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b5212-114">Elements and attributes</span></span>

<span data-ttu-id="b5212-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b5212-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5212-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5212-116">Parent elements</span></span>

|<span data-ttu-id="b5212-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b5212-117">**Element**</span></span>|<span data-ttu-id="b5212-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5212-118">**Type**</span></span>|<span data-ttu-id="b5212-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5212-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5212-120">Rule</span><span class="sxs-lookup"><span data-stu-id="b5212-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5212-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="b5212-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5212-122">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="b5212-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5212-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5212-123">Child elements</span></span>

<span data-ttu-id="b5212-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5212-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5212-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5212-125">Attributes</span></span>

|<span data-ttu-id="b5212-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b5212-126">**Attribute**</span></span>|<span data-ttu-id="b5212-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b5212-127">**Type**</span></span>|<span data-ttu-id="b5212-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="b5212-128">**Required**</span></span>|<span data-ttu-id="b5212-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b5212-129">**Description**</span></span>|<span data-ttu-id="b5212-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="b5212-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5212-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="b5212-131">Formula</span></span>  <br/> |<span data-ttu-id="b5212-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="b5212-132">xsd:string</span></span>  <br/> |<span data-ttu-id="b5212-133">opcional</span><span class="sxs-lookup"><span data-stu-id="b5212-133">optional</span></span>  <br/> |<span data-ttu-id="b5212-134">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="b5212-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="b5212-135">Valores de la xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b5212-135">Values of the xsd:string.</span></span>  <br/> |
   

