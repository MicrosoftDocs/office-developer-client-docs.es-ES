---
title: Elemento Validation ("XML de Visio")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Almacena información sobre la validación del diagrama para el documento.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329088"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="95a1d-103">Elemento Validation ("XML de Visio")</span><span class="sxs-lookup"><span data-stu-id="95a1d-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="95a1d-104">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="95a1d-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95a1d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="95a1d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95a1d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="95a1d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95a1d-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="95a1d-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95a1d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95a1d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95a1d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="95a1d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95a1d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="95a1d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95a1d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="95a1d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95a1d-112">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="95a1d-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95a1d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="95a1d-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95a1d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="95a1d-114">Elements and attributes</span></span>

<span data-ttu-id="95a1d-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="95a1d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95a1d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="95a1d-116">Parent elements</span></span>

<span data-ttu-id="95a1d-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95a1d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95a1d-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="95a1d-118">Child elements</span></span>

|<span data-ttu-id="95a1d-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95a1d-119">**Element**</span></span>|<span data-ttu-id="95a1d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95a1d-120">**Type**</span></span>|<span data-ttu-id="95a1d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95a1d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95a1d-122">Issues</span><span class="sxs-lookup"><span data-stu-id="95a1d-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95a1d-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="95a1d-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95a1d-124">Contiene todos los elementos **Issue** del documento.</span><span class="sxs-lookup"><span data-stu-id="95a1d-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="95a1d-125">RuleSets</span><span class="sxs-lookup"><span data-stu-id="95a1d-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95a1d-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="95a1d-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95a1d-127">Incluye un elemento **ruleset** para cada conjunto de reglas de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="95a1d-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="95a1d-128">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="95a1d-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95a1d-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="95a1d-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95a1d-130">Encapsula las propiedades que están relacionadas con la validación del documento.</span><span class="sxs-lookup"><span data-stu-id="95a1d-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95a1d-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="95a1d-131">Attributes</span></span>

<span data-ttu-id="95a1d-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="95a1d-132">None.</span></span>
  

