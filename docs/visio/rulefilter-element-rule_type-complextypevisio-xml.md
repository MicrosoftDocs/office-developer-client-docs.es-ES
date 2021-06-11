---
title: Elemento RuleFilter (Rule_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica la expresión lógica que determina si la regla de validación debe aplicarse a un objeto de destino.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541683"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a><span data-ttu-id="7e271-103">Elemento RuleFilter (Rule_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7e271-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7e271-104">Especifica la expresión lógica que determina si la regla de validación debe aplicarse a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="7e271-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e271-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7e271-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e271-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7e271-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7e271-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="7e271-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7e271-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7e271-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7e271-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7e271-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7e271-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7e271-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7e271-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7e271-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7e271-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="7e271-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7e271-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7e271-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7e271-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7e271-114">Elements and attributes</span></span>

<span data-ttu-id="7e271-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7e271-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7e271-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7e271-116">Parent elements</span></span>

|<span data-ttu-id="7e271-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7e271-117">**Element**</span></span>|<span data-ttu-id="7e271-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7e271-118">**Type**</span></span>|<span data-ttu-id="7e271-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e271-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7e271-120">Rule</span><span class="sxs-lookup"><span data-stu-id="7e271-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7e271-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="7e271-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7e271-122">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="7e271-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7e271-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7e271-123">Child elements</span></span>

<span data-ttu-id="7e271-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7e271-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e271-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="7e271-125">Attributes</span></span>

|<span data-ttu-id="7e271-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7e271-126">**Attribute**</span></span>|<span data-ttu-id="7e271-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7e271-127">**Type**</span></span>|<span data-ttu-id="7e271-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7e271-128">**Required**</span></span>|<span data-ttu-id="7e271-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e271-129">**Description**</span></span>|<span data-ttu-id="7e271-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7e271-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7e271-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="7e271-131">Formula</span></span>  <br/> |<span data-ttu-id="7e271-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7e271-132">xsd:string</span></span>  <br/> |<span data-ttu-id="7e271-133">opcional</span><span class="sxs-lookup"><span data-stu-id="7e271-133">optional</span></span>  <br/> |<span data-ttu-id="7e271-134">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="7e271-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="7e271-135">Valores de xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7e271-135">Values of the xsd:string.</span></span>  <br/> |
   

