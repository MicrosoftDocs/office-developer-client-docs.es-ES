---
title: CommentEntry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821790"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="28b4a-102">CommentEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="28b4a-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="28b4a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="28b4a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28b4a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="28b4a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="28b4a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="28b4a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="28b4a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="28b4a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="28b4a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="28b4a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="28b4a-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="28b4a-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="28b4a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="28b4a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="28b4a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="28b4a-110">Elements and attributes</span></span>

<span data-ttu-id="28b4a-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="28b4a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="28b4a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28b4a-112">Child elements</span></span>

<span data-ttu-id="28b4a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28b4a-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28b4a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="28b4a-114">Attributes</span></span>

|<span data-ttu-id="28b4a-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="28b4a-115">**Attribute**</span></span>|<span data-ttu-id="28b4a-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="28b4a-116">**Type**</span></span>|<span data-ttu-id="28b4a-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="28b4a-117">**Required**</span></span>|<span data-ttu-id="28b4a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28b4a-118">**Description**</span></span>|<span data-ttu-id="28b4a-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="28b4a-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="28b4a-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="28b4a-120">AuthorID</span></span>  <br/> |<span data-ttu-id="28b4a-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28b4a-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28b4a-122">necesario</span><span class="sxs-lookup"><span data-stu-id="28b4a-122">required</span></span>  <br/> ||<span data-ttu-id="28b4a-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28b4a-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="28b4a-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="28b4a-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28b4a-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28b4a-126">opcional</span><span class="sxs-lookup"><span data-stu-id="28b4a-126">optional</span></span>  <br/> ||<span data-ttu-id="28b4a-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28b4a-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="28b4a-128">CommentID</span></span>  <br/> |<span data-ttu-id="28b4a-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28b4a-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28b4a-130">necesario</span><span class="sxs-lookup"><span data-stu-id="28b4a-130">required</span></span>  <br/> ||<span data-ttu-id="28b4a-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28b4a-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="28b4a-132">Date</span></span>  <br/> |<span data-ttu-id="28b4a-133">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="28b4a-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="28b4a-134">necesario</span><span class="sxs-lookup"><span data-stu-id="28b4a-134">required</span></span>  <br/> ||<span data-ttu-id="28b4a-135">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="28b4a-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-136">Terminado</span><span class="sxs-lookup"><span data-stu-id="28b4a-136">Done</span></span>  <br/> |<span data-ttu-id="28b4a-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="28b4a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="28b4a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="28b4a-138">optional</span></span>  <br/> ||<span data-ttu-id="28b4a-139">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="28b4a-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="28b4a-140">EditDate</span></span>  <br/> |<span data-ttu-id="28b4a-141">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="28b4a-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="28b4a-142">opcional</span><span class="sxs-lookup"><span data-stu-id="28b4a-142">optional</span></span>  <br/> ||<span data-ttu-id="28b4a-143">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="28b4a-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-144">PageID</span><span class="sxs-lookup"><span data-stu-id="28b4a-144">PageID</span></span>  <br/> |<span data-ttu-id="28b4a-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28b4a-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28b4a-146">necesario</span><span class="sxs-lookup"><span data-stu-id="28b4a-146">required</span></span>  <br/> ||<span data-ttu-id="28b4a-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28b4a-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="28b4a-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="28b4a-148">ShapeID</span></span>  <br/> |<span data-ttu-id="28b4a-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="28b4a-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="28b4a-150">opcional</span><span class="sxs-lookup"><span data-stu-id="28b4a-150">optional</span></span>  <br/> ||<span data-ttu-id="28b4a-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="28b4a-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

