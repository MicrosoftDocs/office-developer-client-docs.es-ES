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
# <a name="commententry_type-complextype-visio-xml"></a><span data-ttu-id="cc464-102">CommentEntry_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cc464-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="cc464-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="cc464-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc464-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc464-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc464-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc464-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc464-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cc464-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc464-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="cc464-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc464-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cc464-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc464-109">Definición</span><span class="sxs-lookup"><span data-stu-id="cc464-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cc464-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cc464-110">Elements and attributes</span></span>

<span data-ttu-id="cc464-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cc464-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc464-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc464-112">Child elements</span></span>

<span data-ttu-id="cc464-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc464-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc464-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc464-114">Attributes</span></span>

|<span data-ttu-id="cc464-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cc464-115">**Attribute**</span></span>|<span data-ttu-id="cc464-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc464-116">**Type**</span></span>|<span data-ttu-id="cc464-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="cc464-117">**Required**</span></span>|<span data-ttu-id="cc464-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc464-118">**Description**</span></span>|<span data-ttu-id="cc464-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="cc464-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc464-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="cc464-120">AuthorID</span></span>  <br/> |<span data-ttu-id="cc464-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc464-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc464-122">necesario</span><span class="sxs-lookup"><span data-stu-id="cc464-122">required</span></span>  <br/> ||<span data-ttu-id="cc464-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc464-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc464-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="cc464-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="cc464-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc464-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc464-126">opcional</span><span class="sxs-lookup"><span data-stu-id="cc464-126">optional</span></span>  <br/> ||<span data-ttu-id="cc464-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc464-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc464-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="cc464-128">CommentID</span></span>  <br/> |<span data-ttu-id="cc464-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc464-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc464-130">necesario</span><span class="sxs-lookup"><span data-stu-id="cc464-130">required</span></span>  <br/> ||<span data-ttu-id="cc464-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc464-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc464-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="cc464-132">Date</span></span>  <br/> |<span data-ttu-id="cc464-133">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="cc464-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="cc464-134">necesario</span><span class="sxs-lookup"><span data-stu-id="cc464-134">required</span></span>  <br/> ||<span data-ttu-id="cc464-135">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="cc464-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="cc464-136">Hecho</span><span class="sxs-lookup"><span data-stu-id="cc464-136">Done</span></span>  <br/> |<span data-ttu-id="cc464-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cc464-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cc464-138">opcional</span><span class="sxs-lookup"><span data-stu-id="cc464-138">optional</span></span>  <br/> ||<span data-ttu-id="cc464-139">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cc464-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cc464-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="cc464-140">EditDate</span></span>  <br/> |<span data-ttu-id="cc464-141">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="cc464-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="cc464-142">opcional</span><span class="sxs-lookup"><span data-stu-id="cc464-142">optional</span></span>  <br/> ||<span data-ttu-id="cc464-143">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="cc464-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="cc464-144">PageID</span><span class="sxs-lookup"><span data-stu-id="cc464-144">PageID</span></span>  <br/> |<span data-ttu-id="cc464-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc464-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc464-146">necesario</span><span class="sxs-lookup"><span data-stu-id="cc464-146">required</span></span>  <br/> ||<span data-ttu-id="cc464-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc464-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc464-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="cc464-148">ShapeID</span></span>  <br/> |<span data-ttu-id="cc464-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc464-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc464-150">opcional</span><span class="sxs-lookup"><span data-stu-id="cc464-150">optional</span></span>  <br/> ||<span data-ttu-id="cc464-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc464-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

