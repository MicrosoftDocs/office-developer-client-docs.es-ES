---
title: Elemento de RuleInfo (Issue_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aec47b43-adbe-3344-fbac-29554f244c99
description: Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.
ms.openlocfilehash: f0cf726f0c5d6943ef72669aa92f361a7367459c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394751"
---
# <a name="ruleinfo-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="4279c-103">Elemento de RuleInfo (Issue_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="4279c-103">RuleInfo element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4279c-104">Especifica información acerca de la regla de validación que el problema de validación primario pertenece a.</span><span class="sxs-lookup"><span data-stu-id="4279c-104">Specifies information about the validation rule that the parent validation issue pertains to.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4279c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4279c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4279c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4279c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4279c-107">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="4279c-107">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4279c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4279c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4279c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4279c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4279c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4279c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4279c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4279c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4279c-112">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="4279c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4279c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="4279c-113">Definition</span></span>

```XML
< xs:element name="RuleInfo" type="RuleInfo_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4279c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4279c-114">Elements and attributes</span></span>

<span data-ttu-id="4279c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="4279c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4279c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4279c-116">Parent elements</span></span>

|<span data-ttu-id="4279c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4279c-117">**Element**</span></span>|<span data-ttu-id="4279c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4279c-118">**Type**</span></span>|<span data-ttu-id="4279c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4279c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4279c-120">Problema</span><span class="sxs-lookup"><span data-stu-id="4279c-120">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4279c-121">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="4279c-121">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4279c-122">Representa un problema de validación único en el documento.</span><span class="sxs-lookup"><span data-stu-id="4279c-122">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4279c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4279c-123">Child elements</span></span>

<span data-ttu-id="4279c-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4279c-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4279c-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="4279c-125">Attributes</span></span>

|<span data-ttu-id="4279c-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4279c-126">**Attribute**</span></span>|<span data-ttu-id="4279c-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4279c-127">**Type**</span></span>|<span data-ttu-id="4279c-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4279c-128">**Required**</span></span>|<span data-ttu-id="4279c-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4279c-129">**Description**</span></span>|<span data-ttu-id="4279c-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="4279c-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4279c-131">Identificador de regla</span><span class="sxs-lookup"><span data-stu-id="4279c-131">RuleID</span></span>  <br/> |<span data-ttu-id="4279c-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4279c-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4279c-133">necesario</span><span class="sxs-lookup"><span data-stu-id="4279c-133">required</span></span>  <br/> |<span data-ttu-id="4279c-134">Especifica el identificador único de la regla de validación que el problema primario pertenece a.</span><span class="sxs-lookup"><span data-stu-id="4279c-134">Specifies the unique identifier of the validation rule that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="4279c-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4279c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4279c-136">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="4279c-136">RuleSetID</span></span>  <br/> |<span data-ttu-id="4279c-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4279c-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4279c-138">necesario</span><span class="sxs-lookup"><span data-stu-id="4279c-138">required</span></span>  <br/> |<span data-ttu-id="4279c-139">Especifica el identificador único del conjunto de reglas de validación que el problema primario pertenece a.</span><span class="sxs-lookup"><span data-stu-id="4279c-139">Specifies the unique identifier of the validation rule set that the parent issue pertains to.</span></span>  <br/> |<span data-ttu-id="4279c-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4279c-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

