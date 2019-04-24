---
title: CommentEntry_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334947"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="88116-102">CommentEntry_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="88116-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="88116-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="88116-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88116-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88116-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="88116-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="88116-105">**Schema file**</span></span> <br/> |<span data-ttu-id="88116-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="88116-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="88116-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="88116-107">**Extension base**</span></span> <br/> |<span data-ttu-id="88116-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="88116-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88116-109">Definición</span><span class="sxs-lookup"><span data-stu-id="88116-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="88116-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="88116-110">Elements and attributes</span></span>

<span data-ttu-id="88116-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="88116-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88116-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88116-112">Child elements</span></span>

<span data-ttu-id="88116-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="88116-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88116-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="88116-114">Attributes</span></span>

|<span data-ttu-id="88116-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="88116-115">**Attribute**</span></span>|<span data-ttu-id="88116-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="88116-116">**Type**</span></span>|<span data-ttu-id="88116-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="88116-117">**Required**</span></span>|<span data-ttu-id="88116-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88116-118">**Description**</span></span>|<span data-ttu-id="88116-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="88116-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88116-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="88116-120">AuthorID</span></span>  <br/> |<span data-ttu-id="88116-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88116-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88116-122">necesario</span><span class="sxs-lookup"><span data-stu-id="88116-122">required</span></span>  <br/> ||<span data-ttu-id="88116-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88116-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88116-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="88116-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="88116-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88116-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88116-126">opcional</span><span class="sxs-lookup"><span data-stu-id="88116-126">optional</span></span>  <br/> ||<span data-ttu-id="88116-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88116-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88116-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="88116-128">CommentID</span></span>  <br/> |<span data-ttu-id="88116-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88116-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88116-130">necesario</span><span class="sxs-lookup"><span data-stu-id="88116-130">required</span></span>  <br/> ||<span data-ttu-id="88116-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88116-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88116-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="88116-132">Date</span></span>  <br/> |<span data-ttu-id="88116-133">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="88116-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="88116-134">necesario</span><span class="sxs-lookup"><span data-stu-id="88116-134">required</span></span>  <br/> ||<span data-ttu-id="88116-135">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="88116-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="88116-136">Done</span><span class="sxs-lookup"><span data-stu-id="88116-136">Done</span></span>  <br/> |<span data-ttu-id="88116-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="88116-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="88116-138">opcional</span><span class="sxs-lookup"><span data-stu-id="88116-138">optional</span></span>  <br/> ||<span data-ttu-id="88116-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="88116-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="88116-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="88116-140">EditDate</span></span>  <br/> |<span data-ttu-id="88116-141">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="88116-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="88116-142">opcional</span><span class="sxs-lookup"><span data-stu-id="88116-142">optional</span></span>  <br/> ||<span data-ttu-id="88116-143">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="88116-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="88116-144">PageID</span><span class="sxs-lookup"><span data-stu-id="88116-144">PageID</span></span>  <br/> |<span data-ttu-id="88116-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88116-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88116-146">necesario</span><span class="sxs-lookup"><span data-stu-id="88116-146">required</span></span>  <br/> ||<span data-ttu-id="88116-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88116-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="88116-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="88116-148">ShapeID</span></span>  <br/> |<span data-ttu-id="88116-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="88116-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="88116-150">opcional</span><span class="sxs-lookup"><span data-stu-id="88116-150">optional</span></span>  <br/> ||<span data-ttu-id="88116-151">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="88116-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

