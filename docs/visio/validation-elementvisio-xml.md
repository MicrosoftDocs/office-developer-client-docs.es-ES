---
title: Elemento de validación ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db6292c7-9f4c-c287-803b-64fa41c0a269
description: Almacena información sobre la validación del diagrama para el documento.
ms.openlocfilehash: 7e40cd3a79922b56800cbb566a0d88de23829cc0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382361"
---
# <a name="validation-element-visio-xml"></a><span data-ttu-id="f7677-103">Elemento de validación ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="f7677-103">Validation element ('Visio XML')</span></span>

<span data-ttu-id="f7677-104">Almacena información sobre la validación del diagrama para el documento.</span><span class="sxs-lookup"><span data-stu-id="f7677-104">Stores information about diagram validation for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7677-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f7677-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7677-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f7677-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f7677-107">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="f7677-107">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f7677-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f7677-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f7677-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f7677-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f7677-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f7677-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f7677-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="f7677-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f7677-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="f7677-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f7677-113">Definición</span><span class="sxs-lookup"><span data-stu-id="f7677-113">Definition</span></span>

```XML
< xs:element name="Validation" type="Validation_Type" > </xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f7677-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="f7677-114">Elements and attributes</span></span>

<span data-ttu-id="f7677-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="f7677-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f7677-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f7677-116">Parent elements</span></span>

<span data-ttu-id="f7677-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f7677-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7677-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f7677-118">Child elements</span></span>

|<span data-ttu-id="f7677-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7677-119">**Element**</span></span>|<span data-ttu-id="f7677-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f7677-120">**Type**</span></span>|<span data-ttu-id="f7677-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7677-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f7677-122">Problemas</span><span class="sxs-lookup"><span data-stu-id="f7677-122">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7677-123">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="f7677-123">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7677-124">Contiene todos los elementos de **problema** para el documento.</span><span class="sxs-lookup"><span data-stu-id="f7677-124">Contains all the **Issue** elements for the document.</span></span>  <br/> |
|[<span data-ttu-id="f7677-125">Conjuntos de reglas</span><span class="sxs-lookup"><span data-stu-id="f7677-125">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7677-126">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="f7677-126">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7677-127">Incluye un elemento de **conjunto de reglas** para cada regla de validación establecida en el documento.</span><span class="sxs-lookup"><span data-stu-id="f7677-127">Includes a **RuleSet** element for each validation rule set in the document.</span></span>  <br/> |
|[<span data-ttu-id="f7677-128">Propiedadesla</span><span class="sxs-lookup"><span data-stu-id="f7677-128">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f7677-129">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="f7677-129">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f7677-130">Encapsula las propiedades que están relacionadas con la validación del documento.</span><span class="sxs-lookup"><span data-stu-id="f7677-130">Encapsulates the properties that are related to the document's validation.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f7677-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="f7677-131">Attributes</span></span>

<span data-ttu-id="f7677-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f7677-132">None.</span></span>
  

