---
title: CommentEntry_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384797"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="000e0-102">CommentEntry_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="000e0-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="000e0-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="000e0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="000e0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="000e0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="000e0-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="000e0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="000e0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="000e0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="000e0-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="000e0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="000e0-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="000e0-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="000e0-109">Definición</span><span class="sxs-lookup"><span data-stu-id="000e0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="000e0-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="000e0-110">Elements and attributes</span></span>

<span data-ttu-id="000e0-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="000e0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="000e0-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="000e0-112">Child elements</span></span>

<span data-ttu-id="000e0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="000e0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="000e0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="000e0-114">Attributes</span></span>

|<span data-ttu-id="000e0-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="000e0-115">**Attribute**</span></span>|<span data-ttu-id="000e0-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="000e0-116">**Type**</span></span>|<span data-ttu-id="000e0-117">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="000e0-117">**Required**</span></span>|<span data-ttu-id="000e0-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="000e0-118">**Description**</span></span>|<span data-ttu-id="000e0-119">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="000e0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="000e0-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="000e0-120">AuthorID</span></span>  <br/> |<span data-ttu-id="000e0-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="000e0-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="000e0-122">necesario</span><span class="sxs-lookup"><span data-stu-id="000e0-122">required</span></span>  <br/> ||<span data-ttu-id="000e0-123">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="000e0-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="000e0-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="000e0-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="000e0-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="000e0-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="000e0-126">opcional</span><span class="sxs-lookup"><span data-stu-id="000e0-126">optional</span></span>  <br/> ||<span data-ttu-id="000e0-127">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="000e0-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="000e0-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="000e0-128">CommentID</span></span>  <br/> |<span data-ttu-id="000e0-129">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="000e0-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="000e0-130">necesario</span><span class="sxs-lookup"><span data-stu-id="000e0-130">required</span></span>  <br/> ||<span data-ttu-id="000e0-131">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="000e0-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="000e0-132">Fecha</span><span class="sxs-lookup"><span data-stu-id="000e0-132">Date</span></span>  <br/> |<span data-ttu-id="000e0-133">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="000e0-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="000e0-134">necesario</span><span class="sxs-lookup"><span data-stu-id="000e0-134">required</span></span>  <br/> ||<span data-ttu-id="000e0-135">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="000e0-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="000e0-136">Terminado</span><span class="sxs-lookup"><span data-stu-id="000e0-136">Done</span></span>  <br/> |<span data-ttu-id="000e0-137">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="000e0-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="000e0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="000e0-138">optional</span></span>  <br/> ||<span data-ttu-id="000e0-139">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="000e0-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="000e0-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="000e0-140">EditDate</span></span>  <br/> |<span data-ttu-id="000e0-141">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="000e0-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="000e0-142">opcional</span><span class="sxs-lookup"><span data-stu-id="000e0-142">optional</span></span>  <br/> ||<span data-ttu-id="000e0-143">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="000e0-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="000e0-144">PageID</span><span class="sxs-lookup"><span data-stu-id="000e0-144">PageID</span></span>  <br/> |<span data-ttu-id="000e0-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="000e0-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="000e0-146">necesario</span><span class="sxs-lookup"><span data-stu-id="000e0-146">required</span></span>  <br/> ||<span data-ttu-id="000e0-147">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="000e0-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="000e0-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="000e0-148">ShapeID</span></span>  <br/> |<span data-ttu-id="000e0-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="000e0-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="000e0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="000e0-150">optional</span></span>  <br/> ||<span data-ttu-id="000e0-151">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="000e0-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

