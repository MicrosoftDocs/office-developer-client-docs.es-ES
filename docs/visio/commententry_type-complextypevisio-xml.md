---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540129"
---
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="d9a38-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d9a38-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d9a38-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="d9a38-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9a38-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d9a38-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d9a38-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d9a38-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d9a38-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d9a38-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d9a38-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="d9a38-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d9a38-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d9a38-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9a38-109">Definición</span><span class="sxs-lookup"><span data-stu-id="d9a38-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d9a38-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d9a38-110">Elements and attributes</span></span>

<span data-ttu-id="d9a38-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="d9a38-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d9a38-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d9a38-112">Child elements</span></span>

<span data-ttu-id="d9a38-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9a38-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9a38-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9a38-114">Attributes</span></span>

|<span data-ttu-id="d9a38-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d9a38-115">**Attribute**</span></span>|<span data-ttu-id="d9a38-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d9a38-116">**Type**</span></span>|<span data-ttu-id="d9a38-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d9a38-117">**Required**</span></span>|<span data-ttu-id="d9a38-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9a38-118">**Description**</span></span>|<span data-ttu-id="d9a38-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="d9a38-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d9a38-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="d9a38-120">AuthorID</span></span>  <br/> |<span data-ttu-id="d9a38-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9a38-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9a38-122">necesario</span><span class="sxs-lookup"><span data-stu-id="d9a38-122">required</span></span>  <br/> ||<span data-ttu-id="d9a38-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9a38-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="d9a38-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="d9a38-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9a38-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9a38-126">opcional</span><span class="sxs-lookup"><span data-stu-id="d9a38-126">optional</span></span>  <br/> ||<span data-ttu-id="d9a38-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9a38-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="d9a38-128">CommentID</span></span>  <br/> |<span data-ttu-id="d9a38-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9a38-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9a38-130">necesario</span><span class="sxs-lookup"><span data-stu-id="d9a38-130">required</span></span>  <br/> ||<span data-ttu-id="d9a38-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9a38-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="d9a38-132">Date</span></span>  <br/> |<span data-ttu-id="d9a38-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="d9a38-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d9a38-134">necesario</span><span class="sxs-lookup"><span data-stu-id="d9a38-134">required</span></span>  <br/> ||<span data-ttu-id="d9a38-135">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="d9a38-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-136">Hecho</span><span class="sxs-lookup"><span data-stu-id="d9a38-136">Done</span></span>  <br/> |<span data-ttu-id="d9a38-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="d9a38-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d9a38-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d9a38-138">optional</span></span>  <br/> ||<span data-ttu-id="d9a38-139">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d9a38-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="d9a38-140">EditDate</span></span>  <br/> |<span data-ttu-id="d9a38-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="d9a38-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="d9a38-142">opcional</span><span class="sxs-lookup"><span data-stu-id="d9a38-142">optional</span></span>  <br/> ||<span data-ttu-id="d9a38-143">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="d9a38-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-144">PageID</span><span class="sxs-lookup"><span data-stu-id="d9a38-144">PageID</span></span>  <br/> |<span data-ttu-id="d9a38-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9a38-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9a38-146">necesario</span><span class="sxs-lookup"><span data-stu-id="d9a38-146">required</span></span>  <br/> ||<span data-ttu-id="d9a38-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9a38-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d9a38-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="d9a38-148">ShapeID</span></span>  <br/> |<span data-ttu-id="d9a38-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d9a38-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d9a38-150">opcional</span><span class="sxs-lookup"><span data-stu-id="d9a38-150">optional</span></span>  <br/> ||<span data-ttu-id="d9a38-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d9a38-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

