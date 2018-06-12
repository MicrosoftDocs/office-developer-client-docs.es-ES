---
title: Elemento de IssueTarget (Issue_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario. Si el destino del problema de validación primario es un documento, IssueTarget especifica una página ni una forma.
ms.openlocfilehash: 72789782a37b29daa48cd01adb0b8eda4ebf73ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822404"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="65a34-104">Elemento de IssueTarget (Issue_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="65a34-104">IssueTarget element (Issue_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="65a34-105">Según el destino del elemento primario problema de validación, especifica la página, o la página y la forma, asociado con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="65a34-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="65a34-106">Si el destino del problema de validación primario es un documento, **IssueTarget** especifica una página ni una forma.</span><span class="sxs-lookup"><span data-stu-id="65a34-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="65a34-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65a34-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65a34-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="65a34-108">**Element type**</span></span> <br/> |[<span data-ttu-id="65a34-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="65a34-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="65a34-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="65a34-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="65a34-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="65a34-111">**Schema file**</span></span> <br/> |<span data-ttu-id="65a34-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="65a34-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="65a34-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="65a34-113">**Document parts**</span></span> <br/> |<span data-ttu-id="65a34-114">Validation.Xml</span><span class="sxs-lookup"><span data-stu-id="65a34-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65a34-115">Definición</span><span class="sxs-lookup"><span data-stu-id="65a34-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="65a34-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="65a34-116">Elements and attributes</span></span>

<span data-ttu-id="65a34-117">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="65a34-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="65a34-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65a34-118">Parent elements</span></span>

|<span data-ttu-id="65a34-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="65a34-119">**Element**</span></span>|<span data-ttu-id="65a34-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65a34-120">**Type**</span></span>|<span data-ttu-id="65a34-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65a34-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65a34-122">Problema</span><span class="sxs-lookup"><span data-stu-id="65a34-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="65a34-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="65a34-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="65a34-124">Representa un problema de validación único en el documento.</span><span class="sxs-lookup"><span data-stu-id="65a34-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="65a34-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65a34-125">Child elements</span></span>

<span data-ttu-id="65a34-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="65a34-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65a34-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="65a34-127">Attributes</span></span>

|<span data-ttu-id="65a34-128">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="65a34-128">**Attribute**</span></span>|<span data-ttu-id="65a34-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="65a34-129">**Type**</span></span>|<span data-ttu-id="65a34-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="65a34-130">**Required**</span></span>|<span data-ttu-id="65a34-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65a34-131">**Description**</span></span>|<span data-ttu-id="65a34-132">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="65a34-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="65a34-133">PageID</span><span class="sxs-lookup"><span data-stu-id="65a34-133">PageID</span></span>  <br/> |<span data-ttu-id="65a34-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65a34-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65a34-135">necesario</span><span class="sxs-lookup"><span data-stu-id="65a34-135">required</span></span>  <br/> |<span data-ttu-id="65a34-136">Especifica el identificador único de la página que está asociada con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="65a34-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="65a34-137">Si el destino es el documento, el valor de PageID puede ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="65a34-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="65a34-138">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65a34-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="65a34-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="65a34-139">ShapeID</span></span>  <br/> |<span data-ttu-id="65a34-140">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="65a34-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="65a34-141">necesario</span><span class="sxs-lookup"><span data-stu-id="65a34-141">required</span></span>  <br/> |<span data-ttu-id="65a34-142">Especifica el identificador único de la forma que está asociada con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="65a34-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="65a34-143">Si el destino es una página o el documento, el valor de ShapeID puede ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="65a34-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="65a34-144">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="65a34-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

