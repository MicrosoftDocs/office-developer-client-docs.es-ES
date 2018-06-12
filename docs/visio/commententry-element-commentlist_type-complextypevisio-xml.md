---
title: Elemento de CommentEntry (CommentList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica las propiedades que se usa para identificar un comentario en un dibujo.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821797"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="1b379-103">Elemento de CommentEntry (CommentList_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1b379-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1b379-104">Especifica las propiedades que se usa para identificar un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="1b379-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b379-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1b379-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b379-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1b379-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1b379-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1b379-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1b379-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b379-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1b379-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1b379-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1b379-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1b379-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1b379-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1b379-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1b379-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="1b379-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b379-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1b379-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b379-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1b379-114">Elements and attributes</span></span>

<span data-ttu-id="1b379-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1b379-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b379-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1b379-116">Parent elements</span></span>

|<span data-ttu-id="1b379-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b379-117">**Element**</span></span>|<span data-ttu-id="1b379-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b379-118">**Type**</span></span>|<span data-ttu-id="1b379-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b379-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b379-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="1b379-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b379-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="1b379-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1b379-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="1b379-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b379-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1b379-123">Child elements</span></span>

<span data-ttu-id="1b379-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1b379-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b379-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1b379-125">Attributes</span></span>

|<span data-ttu-id="1b379-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1b379-126">**Attribute**</span></span>|<span data-ttu-id="1b379-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1b379-127">**Type**</span></span>|<span data-ttu-id="1b379-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1b379-128">**Required**</span></span>|<span data-ttu-id="1b379-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b379-129">**Description**</span></span>|<span data-ttu-id="1b379-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="1b379-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1b379-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="1b379-131">AuthorID</span></span>  <br/> |<span data-ttu-id="1b379-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b379-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b379-133">necesario</span><span class="sxs-lookup"><span data-stu-id="1b379-133">required</span></span>  <br/> |<span data-ttu-id="1b379-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="1b379-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="1b379-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1b379-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b379-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="1b379-136">CommentID</span></span>  <br/> |<span data-ttu-id="1b379-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b379-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b379-138">necesario</span><span class="sxs-lookup"><span data-stu-id="1b379-138">required</span></span>  <br/> |<span data-ttu-id="1b379-139">Un valor único que identifica el comentario en una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1b379-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="1b379-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1b379-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b379-141">Fecha</span><span class="sxs-lookup"><span data-stu-id="1b379-141">Date</span></span>  <br/> |<span data-ttu-id="1b379-142">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="1b379-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="1b379-143">necesario</span><span class="sxs-lookup"><span data-stu-id="1b379-143">required</span></span>  <br/> |<span data-ttu-id="1b379-144">Especifica cuándo se creó un comentario.</span><span class="sxs-lookup"><span data-stu-id="1b379-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="1b379-145">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="1b379-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="1b379-146">Terminado</span><span class="sxs-lookup"><span data-stu-id="1b379-146">Done</span></span>  <br/> |<span data-ttu-id="1b379-147">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="1b379-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1b379-148">opcional</span><span class="sxs-lookup"><span data-stu-id="1b379-148">optional</span></span>  <br/> |<span data-ttu-id="1b379-149">Especifica el estado actual del comentario.</span><span class="sxs-lookup"><span data-stu-id="1b379-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="1b379-150">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="1b379-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1b379-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="1b379-151">EditDate</span></span>  <br/> |<span data-ttu-id="1b379-152">xsd: DateTime</span><span class="sxs-lookup"><span data-stu-id="1b379-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="1b379-153">opcional</span><span class="sxs-lookup"><span data-stu-id="1b379-153">optional</span></span>  <br/> |<span data-ttu-id="1b379-154">Especifica cuándo se modificó por última vez un comentario.</span><span class="sxs-lookup"><span data-stu-id="1b379-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="1b379-155">Valores del tipo XSD: DateTime.</span><span class="sxs-lookup"><span data-stu-id="1b379-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="1b379-156">PageID</span><span class="sxs-lookup"><span data-stu-id="1b379-156">PageID</span></span>  <br/> |<span data-ttu-id="1b379-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b379-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b379-158">necesario</span><span class="sxs-lookup"><span data-stu-id="1b379-158">required</span></span>  <br/> |<span data-ttu-id="1b379-159">Un valor que identifica la página de dibujo el comentario está en.</span><span class="sxs-lookup"><span data-stu-id="1b379-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="1b379-160">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1b379-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1b379-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1b379-161">ShapeID</span></span>  <br/> |<span data-ttu-id="1b379-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1b379-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1b379-163">opcional</span><span class="sxs-lookup"><span data-stu-id="1b379-163">optional</span></span>  <br/> |<span data-ttu-id="1b379-164">Un valor que identifica la forma el comentario está en.</span><span class="sxs-lookup"><span data-stu-id="1b379-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="1b379-165">Si no se especifica ningún ShapeID, el comentario hace referencia a la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="1b379-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="1b379-166">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1b379-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

