---
title: ComplexType CommentEntry_Type (XML de Visio)
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
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="0a33f-102">ComplexType CommentEntry_Type (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="0a33f-102">CommentEntry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0a33f-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="0a33f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a33f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0a33f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a33f-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0a33f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a33f-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="0a33f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a33f-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="0a33f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a33f-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="0a33f-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a33f-109">Definición</span><span class="sxs-lookup"><span data-stu-id="0a33f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a33f-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0a33f-110">Elements and attributes</span></span>

<span data-ttu-id="0a33f-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0a33f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a33f-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0a33f-112">Child elements</span></span>

<span data-ttu-id="0a33f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0a33f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a33f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0a33f-114">Attributes</span></span>

|<span data-ttu-id="0a33f-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0a33f-115">**Attribute**</span></span>|<span data-ttu-id="0a33f-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0a33f-116">**Type**</span></span>|<span data-ttu-id="0a33f-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0a33f-117">**Required**</span></span>|<span data-ttu-id="0a33f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a33f-118">**Description**</span></span>|<span data-ttu-id="0a33f-119">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0a33f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0a33f-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="0a33f-120">AuthorID</span></span>  <br/> |<span data-ttu-id="0a33f-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a33f-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a33f-122">necesario</span><span class="sxs-lookup"><span data-stu-id="0a33f-122">required</span></span>  <br/> ||<span data-ttu-id="0a33f-123">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a33f-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="0a33f-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="0a33f-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a33f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a33f-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0a33f-126">optional</span></span>  <br/> ||<span data-ttu-id="0a33f-127">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a33f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="0a33f-128">CommentID</span></span>  <br/> |<span data-ttu-id="0a33f-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a33f-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a33f-130">necesario</span><span class="sxs-lookup"><span data-stu-id="0a33f-130">required</span></span>  <br/> ||<span data-ttu-id="0a33f-131">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a33f-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="0a33f-132">Date</span></span>  <br/> |<span data-ttu-id="0a33f-133">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="0a33f-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0a33f-134">necesario</span><span class="sxs-lookup"><span data-stu-id="0a33f-134">required</span></span>  <br/> ||<span data-ttu-id="0a33f-135">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="0a33f-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-136">Done</span><span class="sxs-lookup"><span data-stu-id="0a33f-136">Done</span></span>  <br/> |<span data-ttu-id="0a33f-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="0a33f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0a33f-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0a33f-138">optional</span></span>  <br/> ||<span data-ttu-id="0a33f-139">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0a33f-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="0a33f-140">EditDate</span></span>  <br/> |<span data-ttu-id="0a33f-141">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="0a33f-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="0a33f-142">opcional</span><span class="sxs-lookup"><span data-stu-id="0a33f-142">optional</span></span>  <br/> ||<span data-ttu-id="0a33f-143">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="0a33f-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-144">PageID</span><span class="sxs-lookup"><span data-stu-id="0a33f-144">PageID</span></span>  <br/> |<span data-ttu-id="0a33f-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a33f-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a33f-146">necesario</span><span class="sxs-lookup"><span data-stu-id="0a33f-146">required</span></span>  <br/> ||<span data-ttu-id="0a33f-147">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a33f-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0a33f-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="0a33f-148">ShapeID</span></span>  <br/> |<span data-ttu-id="0a33f-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0a33f-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0a33f-150">opcional</span><span class="sxs-lookup"><span data-stu-id="0a33f-150">optional</span></span>  <br/> ||<span data-ttu-id="0a33f-151">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0a33f-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

