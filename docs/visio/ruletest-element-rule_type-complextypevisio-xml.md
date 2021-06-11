---
title: Elemento RuleTest (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cb95b34-3ce0-07a5-5d57-8ac9b0570b9a
description: Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.
ms.openlocfilehash: bb1f0cf9b3f712903f6e45d6d09f96607089f920
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541522"
---
# <a name="ruletest-element-rule_type-complextype-visio-xml"></a><span data-ttu-id="fb659-103">Elemento RuleTest (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fb659-103">RuleTest element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fb659-104">Especifica la expresión lógica que determina si el objeto de destino cumple la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="fb659-104">Specifies the logical expression that determines whether the target object satisfies the validation rule.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb659-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fb659-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb659-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fb659-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fb659-107">RuleTest_Type</span><span class="sxs-lookup"><span data-stu-id="fb659-107">RuleTest_Type</span></span>](ruletest_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fb659-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb659-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fb659-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fb659-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fb659-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fb659-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fb659-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="fb659-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fb659-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="fb659-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb659-113">Definición</span><span class="sxs-lookup"><span data-stu-id="fb659-113">Definition</span></span>

```XML
< xs:element name="RuleTest" type="RuleTest_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fb659-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="fb659-114">Elements and attributes</span></span>

<span data-ttu-id="fb659-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="fb659-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fb659-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fb659-116">Parent elements</span></span>

|<span data-ttu-id="fb659-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fb659-117">**Element**</span></span>|<span data-ttu-id="fb659-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb659-118">**Type**</span></span>|<span data-ttu-id="fb659-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb659-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb659-120">Rule</span><span class="sxs-lookup"><span data-stu-id="fb659-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb659-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="fb659-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb659-122">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="fb659-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb659-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fb659-123">Child elements</span></span>

<span data-ttu-id="fb659-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb659-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb659-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb659-125">Attributes</span></span>

|<span data-ttu-id="fb659-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="fb659-126">**Attribute**</span></span>|<span data-ttu-id="fb659-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb659-127">**Type**</span></span>|<span data-ttu-id="fb659-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="fb659-128">**Required**</span></span>|<span data-ttu-id="fb659-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fb659-129">**Description**</span></span>|<span data-ttu-id="fb659-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="fb659-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fb659-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="fb659-131">Formula</span></span>  <br/> |<span data-ttu-id="fb659-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="fb659-132">xsd:string</span></span>  <br/> |<span data-ttu-id="fb659-133">opcional</span><span class="sxs-lookup"><span data-stu-id="fb659-133">optional</span></span>  <br/> |<span data-ttu-id="fb659-134">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="fb659-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="fb659-135">Valores de xsd:string.</span><span class="sxs-lookup"><span data-stu-id="fb659-135">Values of the xsd:string.</span></span>  <br/> |
   

