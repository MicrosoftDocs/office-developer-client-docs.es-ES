---
title: Elemento de conjuntos de elementos (Validation_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a0201e6-9a93-83ae-8a0a-47630ed291ce
description: Incluye un elemento RuleSet para cada conjunto de reglas de validación en el documento.
ms.openlocfilehash: 8c770de80a841a452908ae1a9f77a6dee25aad4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319050"
---
# <a name="rulesets-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="a26fa-103">Elemento de conjuntos de elementos (Validation_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="a26fa-103">RuleSets element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a26fa-104">Incluye un elemento **ruleset** para cada conjunto de reglas de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="a26fa-104">Includes a **RuleSet** element for each validation rule set in the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a26fa-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a26fa-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a26fa-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a26fa-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a26fa-107">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="a26fa-107">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a26fa-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a26fa-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a26fa-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a26fa-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a26fa-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a26fa-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a26fa-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a26fa-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a26fa-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="a26fa-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a26fa-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a26fa-113">Definition</span></span>

```XML
< xs:element name="RuleSets" type="RuleSets_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a26fa-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a26fa-114">Elements and attributes</span></span>

<span data-ttu-id="a26fa-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="a26fa-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a26fa-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a26fa-116">Parent elements</span></span>

|<span data-ttu-id="a26fa-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a26fa-117">**Element**</span></span>|<span data-ttu-id="a26fa-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a26fa-118">**Type**</span></span>|<span data-ttu-id="a26fa-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a26fa-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a26fa-120">Validation</span><span class="sxs-lookup"><span data-stu-id="a26fa-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="a26fa-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="a26fa-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a26fa-122">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="a26fa-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a26fa-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a26fa-123">Child elements</span></span>

|<span data-ttu-id="a26fa-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a26fa-124">**Element**</span></span>|<span data-ttu-id="a26fa-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a26fa-125">**Type**</span></span>|<span data-ttu-id="a26fa-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a26fa-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a26fa-127">RuleSet</span><span class="sxs-lookup"><span data-stu-id="a26fa-127">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a26fa-128">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="a26fa-128">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a26fa-129">Representa un conjunto de reglas de validación de diagrama.</span><span class="sxs-lookup"><span data-stu-id="a26fa-129">Represents one set of diagram-validation rules.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a26fa-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="a26fa-130">Attributes</span></span>

<span data-ttu-id="a26fa-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a26fa-131">None.</span></span>
  

