---
title: Elemento CommentEntry (complexType CommentList_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica las propiedades que se usan para identificar un Comentario en un dibujo.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329543"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a><span data-ttu-id="8db1d-103">Elemento CommentEntry (complexType CommentList_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="8db1d-103">CommentEntry element (CommentList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="8db1d-104">Especifica las propiedades que se usan para identificar un Comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="8db1d-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8db1d-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8db1d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8db1d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="8db1d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8db1d-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="8db1d-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8db1d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="8db1d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8db1d-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="8db1d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8db1d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8db1d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8db1d-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="8db1d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8db1d-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="8db1d-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8db1d-113">Definición</span><span class="sxs-lookup"><span data-stu-id="8db1d-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8db1d-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="8db1d-114">Elements and attributes</span></span>

<span data-ttu-id="8db1d-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="8db1d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8db1d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8db1d-116">Parent elements</span></span>

|<span data-ttu-id="8db1d-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8db1d-117">**Element**</span></span>|<span data-ttu-id="8db1d-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8db1d-118">**Type**</span></span>|<span data-ttu-id="8db1d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8db1d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8db1d-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="8db1d-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8db1d-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="8db1d-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8db1d-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="8db1d-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8db1d-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8db1d-123">Child elements</span></span>

<span data-ttu-id="8db1d-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8db1d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8db1d-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="8db1d-125">Attributes</span></span>

|<span data-ttu-id="8db1d-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="8db1d-126">**Attribute**</span></span>|<span data-ttu-id="8db1d-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="8db1d-127">**Type**</span></span>|<span data-ttu-id="8db1d-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="8db1d-128">**Required**</span></span>|<span data-ttu-id="8db1d-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8db1d-129">**Description**</span></span>|<span data-ttu-id="8db1d-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="8db1d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8db1d-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="8db1d-131">AuthorID</span></span>  <br/> |<span data-ttu-id="8db1d-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8db1d-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8db1d-133">necesario</span><span class="sxs-lookup"><span data-stu-id="8db1d-133">required</span></span>  <br/> |<span data-ttu-id="8db1d-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="8db1d-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="8db1d-135">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8db1d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="8db1d-136">CommentID</span></span>  <br/> |<span data-ttu-id="8db1d-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8db1d-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8db1d-138">necesario</span><span class="sxs-lookup"><span data-stu-id="8db1d-138">required</span></span>  <br/> |<span data-ttu-id="8db1d-139">Un valor único que identifica el comentario en una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8db1d-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="8db1d-140">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8db1d-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-141">Fecha</span><span class="sxs-lookup"><span data-stu-id="8db1d-141">Date</span></span>  <br/> |<span data-ttu-id="8db1d-142">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="8db1d-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8db1d-143">necesario</span><span class="sxs-lookup"><span data-stu-id="8db1d-143">required</span></span>  <br/> |<span data-ttu-id="8db1d-144">Especifica cuándo se creó un comentario.</span><span class="sxs-lookup"><span data-stu-id="8db1d-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="8db1d-145">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="8db1d-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-146">Done</span><span class="sxs-lookup"><span data-stu-id="8db1d-146">Done</span></span>  <br/> |<span data-ttu-id="8db1d-147">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="8db1d-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8db1d-148">opcional</span><span class="sxs-lookup"><span data-stu-id="8db1d-148">optional</span></span>  <br/> |<span data-ttu-id="8db1d-149">Especifica el estado actual del comentario.</span><span class="sxs-lookup"><span data-stu-id="8db1d-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="8db1d-150">Valores del tipo xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8db1d-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="8db1d-151">EditDate</span></span>  <br/> |<span data-ttu-id="8db1d-152">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="8db1d-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="8db1d-153">opcional</span><span class="sxs-lookup"><span data-stu-id="8db1d-153">optional</span></span>  <br/> |<span data-ttu-id="8db1d-154">Especifica cuándo se modificó por última vez un comentario.</span><span class="sxs-lookup"><span data-stu-id="8db1d-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="8db1d-155">Valores del tipo xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="8db1d-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-156">PageID</span><span class="sxs-lookup"><span data-stu-id="8db1d-156">PageID</span></span>  <br/> |<span data-ttu-id="8db1d-157">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8db1d-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8db1d-158">necesario</span><span class="sxs-lookup"><span data-stu-id="8db1d-158">required</span></span>  <br/> |<span data-ttu-id="8db1d-159">Un valor que identifica la página de dibujo en la que se encuentra el comentario.</span><span class="sxs-lookup"><span data-stu-id="8db1d-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="8db1d-160">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8db1d-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8db1d-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="8db1d-161">ShapeID</span></span>  <br/> |<span data-ttu-id="8db1d-162">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="8db1d-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8db1d-163">opcional</span><span class="sxs-lookup"><span data-stu-id="8db1d-163">optional</span></span>  <br/> |<span data-ttu-id="8db1d-164">Un valor que identifica la forma en que se encuentra el comentario.</span><span class="sxs-lookup"><span data-stu-id="8db1d-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="8db1d-165">Si no se especifica ningún ShapeID, el comentario hace referencia a la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="8db1d-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="8db1d-166">Valores del tipo xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="8db1d-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

