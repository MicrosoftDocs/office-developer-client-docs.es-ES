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
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="ca62d-102">CommentEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="ca62d-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ca62d-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="ca62d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca62d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ca62d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ca62d-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ca62d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ca62d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ca62d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ca62d-107">**Base de la extensión**</span><span class="sxs-lookup"><span data-stu-id="ca62d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ca62d-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ca62d-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca62d-109">Definición</span><span class="sxs-lookup"><span data-stu-id="ca62d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ca62d-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ca62d-110">Elements and attributes</span></span>

<span data-ttu-id="ca62d-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="ca62d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ca62d-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ca62d-112">Child elements</span></span>

<span data-ttu-id="ca62d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ca62d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca62d-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="ca62d-114">Attributes</span></span>

|<span data-ttu-id="ca62d-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ca62d-115">**Attribute**</span></span>|<span data-ttu-id="ca62d-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ca62d-116">**Type**</span></span>|<span data-ttu-id="ca62d-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="ca62d-117">**Required**</span></span>|<span data-ttu-id="ca62d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca62d-118">**Description**</span></span>|<span data-ttu-id="ca62d-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="ca62d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca62d-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="ca62d-120">AuthorID</span></span>  <br/> |<span data-ttu-id="ca62d-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca62d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca62d-122">necesario</span><span class="sxs-lookup"><span data-stu-id="ca62d-122">required</span></span>  <br/> ||<span data-ttu-id="ca62d-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca62d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="ca62d-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="ca62d-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca62d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca62d-126">opcional</span><span class="sxs-lookup"><span data-stu-id="ca62d-126">optional</span></span>  <br/> ||<span data-ttu-id="ca62d-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca62d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="ca62d-128">CommentID</span></span>  <br/> |<span data-ttu-id="ca62d-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca62d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca62d-130">necesario</span><span class="sxs-lookup"><span data-stu-id="ca62d-130">required</span></span>  <br/> ||<span data-ttu-id="ca62d-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca62d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="ca62d-132">Date</span></span>  <br/> |<span data-ttu-id="ca62d-133">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="ca62d-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ca62d-134">necesario</span><span class="sxs-lookup"><span data-stu-id="ca62d-134">required</span></span>  <br/> ||<span data-ttu-id="ca62d-135">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="ca62d-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-136">Terminado</span><span class="sxs-lookup"><span data-stu-id="ca62d-136">Done</span></span>  <br/> |<span data-ttu-id="ca62d-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="ca62d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ca62d-138">opcional</span><span class="sxs-lookup"><span data-stu-id="ca62d-138">optional</span></span>  <br/> ||<span data-ttu-id="ca62d-139">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="ca62d-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="ca62d-140">EditDate</span></span>  <br/> |<span data-ttu-id="ca62d-141">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="ca62d-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="ca62d-142">opcional</span><span class="sxs-lookup"><span data-stu-id="ca62d-142">optional</span></span>  <br/> ||<span data-ttu-id="ca62d-143">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="ca62d-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-144">PageID</span><span class="sxs-lookup"><span data-stu-id="ca62d-144">PageID</span></span>  <br/> |<span data-ttu-id="ca62d-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca62d-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca62d-146">necesario</span><span class="sxs-lookup"><span data-stu-id="ca62d-146">required</span></span>  <br/> ||<span data-ttu-id="ca62d-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca62d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca62d-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="ca62d-148">ShapeID</span></span>  <br/> |<span data-ttu-id="ca62d-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca62d-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca62d-150">opcional</span><span class="sxs-lookup"><span data-stu-id="ca62d-150">optional</span></span>  <br/> ||<span data-ttu-id="ca62d-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca62d-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

