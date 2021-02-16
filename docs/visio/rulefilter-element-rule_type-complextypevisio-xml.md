---
title: Elemento RuleFilter (Rule_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b05497e6-722f-9203-e03c-0f14a712cddb
description: Especifica la expresión lógica que determina si se debe aplicar la regla de validación a un objeto de destino.
ms.openlocfilehash: 3abcd7e2dd093fa8e2321052e73835db22c150db
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541683"
---
# <a name="rulefilter-element-rule_type-complextype-visio-xml"></a><span data-ttu-id="7b9e6-103">Elemento RuleFilter (Rule_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="7b9e6-103">RuleFilter element (Rule_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7b9e6-104">Especifica la expresión lógica que determina si se debe aplicar la regla de validación a un objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-104">Specifies the logical expression that determines whether the validation rule should be applied to a target object.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b9e6-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7b9e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b9e6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7b9e6-107">RuleFilter_Type</span><span class="sxs-lookup"><span data-stu-id="7b9e6-107">RuleFilter_Type</span></span>](rulefilter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7b9e6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7b9e6-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7b9e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7b9e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7b9e6-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7b9e6-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="7b9e6-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b9e6-113">Definición</span><span class="sxs-lookup"><span data-stu-id="7b9e6-113">Definition</span></span>

```XML
< xs:element name="RuleFilter" type="RuleFilter_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7b9e6-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="7b9e6-114">Elements and attributes</span></span>

<span data-ttu-id="7b9e6-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7b9e6-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7b9e6-116">Parent elements</span></span>

|<span data-ttu-id="7b9e6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-117">**Element**</span></span>|<span data-ttu-id="7b9e6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-118">**Type**</span></span>|<span data-ttu-id="7b9e6-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b9e6-120">Rule</span><span class="sxs-lookup"><span data-stu-id="7b9e6-120">Rule</span></span>](rule-element-ruleset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7b9e6-121">Rule_Type</span><span class="sxs-lookup"><span data-stu-id="7b9e6-121">Rule_Type</span></span>](rule_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7b9e6-122">Representa una regla de validación única en un conjunto de reglas de validación de diagramas.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-122">Represents a single validation rule in a diagram validation rule set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b9e6-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b9e6-123">Child elements</span></span>

<span data-ttu-id="7b9e6-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b9e6-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b9e6-125">Attributes</span></span>

|<span data-ttu-id="7b9e6-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-126">**Attribute**</span></span>|<span data-ttu-id="7b9e6-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-127">**Type**</span></span>|<span data-ttu-id="7b9e6-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-128">**Required**</span></span>|<span data-ttu-id="7b9e6-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-129">**Description**</span></span>|<span data-ttu-id="7b9e6-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="7b9e6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7b9e6-131">Fórmula</span><span class="sxs-lookup"><span data-stu-id="7b9e6-131">Formula</span></span>  <br/> |<span data-ttu-id="7b9e6-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="7b9e6-132">xsd:string</span></span>  <br/> |<span data-ttu-id="7b9e6-133">opcional</span><span class="sxs-lookup"><span data-stu-id="7b9e6-133">optional</span></span>  <br/> |<span data-ttu-id="7b9e6-134">Representa la fórmula del elemento.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-134">Represents the element's formula.</span></span>  <br/> |<span data-ttu-id="7b9e6-135">Valores de xsd:string.</span><span class="sxs-lookup"><span data-stu-id="7b9e6-135">Values of the xsd:string.</span></span>  <br/> |
   

