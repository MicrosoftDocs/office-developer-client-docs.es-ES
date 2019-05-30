---
title: Elemento IssueTarget (complexType Issue_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd9a5d5f-16fe-29b4-5af0-913b14d2be16
description: Según el destino del problema de validación principal, especifica la página, o bien la página y la forma, asociadas con el problema de validación principal. Si el destino del problema de validación principal es un documento, IssueTarget no especifica ni una página ni una forma.
ms.openlocfilehash: 686f37afee43d9cee3f58979d5856602f571eec8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542957"
---
# <a name="issuetarget-element-issuetype-complextype-visio-xml"></a><span data-ttu-id="4aba5-104">Elemento IssueTarget (complexType Issue_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="4aba5-104">IssueTarget element (Issue_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4aba5-105">Según el destino del problema de validación principal, especifica la página, o bien la página y la forma, asociadas con el problema de validación principal.</span><span class="sxs-lookup"><span data-stu-id="4aba5-105">Depending on the target of the parent validation issue, specifies either the page, or both the page and the shape, associated with the parent validation issue.</span></span> <span data-ttu-id="4aba5-106">Si el destino del problema de validación principal es un documento, **IssueTarget** no especifica ni una página ni una forma.</span><span class="sxs-lookup"><span data-stu-id="4aba5-106">If the target of the parent validation issue is a document, **IssueTarget** specifes neither a page nor a shape.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4aba5-107">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4aba5-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4aba5-108">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4aba5-108">**Element type**</span></span> <br/> |[<span data-ttu-id="4aba5-109">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="4aba5-109">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4aba5-110">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4aba5-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4aba5-111">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4aba5-111">**Schema file**</span></span> <br/> |<span data-ttu-id="4aba5-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4aba5-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4aba5-113">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="4aba5-113">**Document parts**</span></span> <br/> |<span data-ttu-id="4aba5-114">Validation. XML</span><span class="sxs-lookup"><span data-stu-id="4aba5-114">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4aba5-115">Definición</span><span class="sxs-lookup"><span data-stu-id="4aba5-115">Definition</span></span>

```XML
< xs:element name="IssueTarget" type="IssueTarget_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4aba5-116">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="4aba5-116">Elements and attributes</span></span>

<span data-ttu-id="4aba5-117">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="4aba5-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4aba5-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4aba5-118">Parent elements</span></span>

|<span data-ttu-id="4aba5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4aba5-119">**Element**</span></span>|<span data-ttu-id="4aba5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4aba5-120">**Type**</span></span>|<span data-ttu-id="4aba5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4aba5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4aba5-122">Problema</span><span class="sxs-lookup"><span data-stu-id="4aba5-122">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4aba5-123">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="4aba5-123">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4aba5-124">Representa un único problema de validación en el documento.</span><span class="sxs-lookup"><span data-stu-id="4aba5-124">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4aba5-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4aba5-125">Child elements</span></span>

<span data-ttu-id="4aba5-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4aba5-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4aba5-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="4aba5-127">Attributes</span></span>

|<span data-ttu-id="4aba5-128">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4aba5-128">**Attribute**</span></span>|<span data-ttu-id="4aba5-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4aba5-129">**Type**</span></span>|<span data-ttu-id="4aba5-130">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="4aba5-130">**Required**</span></span>|<span data-ttu-id="4aba5-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4aba5-131">**Description**</span></span>|<span data-ttu-id="4aba5-132">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="4aba5-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4aba5-133">PageID</span><span class="sxs-lookup"><span data-stu-id="4aba5-133">PageID</span></span>  <br/> |<span data-ttu-id="4aba5-134">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4aba5-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4aba5-135">necesario</span><span class="sxs-lookup"><span data-stu-id="4aba5-135">required</span></span>  <br/> |<span data-ttu-id="4aba5-136">Especifica el identificador único de la página que está asociado con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="4aba5-136">Specifies the unique identifier of the page that is associated with the parent validation issue.</span></span> <span data-ttu-id="4aba5-137">Si el destino es el documento, el valor de PageID puede ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4aba5-137">If the target is the document, the PageID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="4aba5-138">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4aba5-138">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4aba5-139">ShapeID</span><span class="sxs-lookup"><span data-stu-id="4aba5-139">ShapeID</span></span>  <br/> |<span data-ttu-id="4aba5-140">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4aba5-140">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4aba5-141">necesario</span><span class="sxs-lookup"><span data-stu-id="4aba5-141">required</span></span>  <br/> |<span data-ttu-id="4aba5-142">Especifica el identificador único de la forma asociada con el problema de validación primario.</span><span class="sxs-lookup"><span data-stu-id="4aba5-142">Specifies the unique identifier of the shape that is associated with the parent validation issue.</span></span> <span data-ttu-id="4aba5-143">Si el destino es el documento o una página, el valor de ShapeID puede ser 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4aba5-143">If the target is the document or a page, the ShapeID value can be 0xFFFFFFFF.</span></span>  <br/> |<span data-ttu-id="4aba5-144">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4aba5-144">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

