---
title: Elemento CommentEntry (CommentList_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Especifica las propiedades usadas para identificar un comentario en un dibujo.
ms.openlocfilehash: 6b4f20d632b54e7c96ef8181310e8ffab1abbd0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540115"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a><span data-ttu-id="64377-103">Elemento CommentEntry (CommentList_Type complexType) (VISIO XML)</span><span class="sxs-lookup"><span data-stu-id="64377-103">CommentEntry element (CommentList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="64377-104">Especifica las propiedades usadas para identificar un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="64377-104">Specifies properties used to identify a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64377-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="64377-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64377-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="64377-106">**Element type**</span></span> <br/> |[<span data-ttu-id="64377-107">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="64377-107">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="64377-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64377-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="64377-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="64377-109">**Schema file**</span></span> <br/> |<span data-ttu-id="64377-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="64377-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="64377-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="64377-111">**Document parts**</span></span> <br/> |<span data-ttu-id="64377-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="64377-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64377-113">Definición</span><span class="sxs-lookup"><span data-stu-id="64377-113">Definition</span></span>

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="64377-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="64377-114">Elements and attributes</span></span>

<span data-ttu-id="64377-115">Si el esquema define requisitos específicos, como **secuencia**, **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="64377-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="64377-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64377-116">Parent elements</span></span>

|<span data-ttu-id="64377-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64377-117">**Element**</span></span>|<span data-ttu-id="64377-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64377-118">**Type**</span></span>|<span data-ttu-id="64377-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64377-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64377-120">CommentList</span><span class="sxs-lookup"><span data-stu-id="64377-120">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="64377-121">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="64377-121">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="64377-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="64377-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="64377-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64377-123">Child elements</span></span>

<span data-ttu-id="64377-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="64377-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64377-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="64377-125">Attributes</span></span>

|<span data-ttu-id="64377-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="64377-126">**Attribute**</span></span>|<span data-ttu-id="64377-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64377-127">**Type**</span></span>|<span data-ttu-id="64377-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="64377-128">**Required**</span></span>|<span data-ttu-id="64377-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64377-129">**Description**</span></span>|<span data-ttu-id="64377-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="64377-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64377-131">AuthorID</span><span class="sxs-lookup"><span data-stu-id="64377-131">AuthorID</span></span>  <br/> |<span data-ttu-id="64377-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64377-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64377-133">necesario</span><span class="sxs-lookup"><span data-stu-id="64377-133">required</span></span>  <br/> |<span data-ttu-id="64377-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="64377-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="64377-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64377-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64377-136">CommentID</span><span class="sxs-lookup"><span data-stu-id="64377-136">CommentID</span></span>  <br/> |<span data-ttu-id="64377-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64377-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64377-138">necesario</span><span class="sxs-lookup"><span data-stu-id="64377-138">required</span></span>  <br/> |<span data-ttu-id="64377-139">Valor único que identifica el comentario en una página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="64377-139">A unique value that identifies the comment in a drawing page.</span></span>  <br/> |<span data-ttu-id="64377-140">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64377-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64377-141">Fecha</span><span class="sxs-lookup"><span data-stu-id="64377-141">Date</span></span>  <br/> |<span data-ttu-id="64377-142">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="64377-142">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="64377-143">necesario</span><span class="sxs-lookup"><span data-stu-id="64377-143">required</span></span>  <br/> |<span data-ttu-id="64377-144">Especifica cuándo se creó un comentario.</span><span class="sxs-lookup"><span data-stu-id="64377-144">Specifies when a comment was created.</span></span>  <br/> |<span data-ttu-id="64377-145">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="64377-145">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="64377-146">Hecho</span><span class="sxs-lookup"><span data-stu-id="64377-146">Done</span></span>  <br/> |<span data-ttu-id="64377-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="64377-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64377-148">opcional</span><span class="sxs-lookup"><span data-stu-id="64377-148">optional</span></span>  <br/> |<span data-ttu-id="64377-149">Especifica el estado actual del comentario.</span><span class="sxs-lookup"><span data-stu-id="64377-149">Specifies the current state of the comment.</span></span>  <br/> |<span data-ttu-id="64377-150">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="64377-150">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64377-151">EditDate</span><span class="sxs-lookup"><span data-stu-id="64377-151">EditDate</span></span>  <br/> |<span data-ttu-id="64377-152">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="64377-152">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="64377-153">opcional</span><span class="sxs-lookup"><span data-stu-id="64377-153">optional</span></span>  <br/> |<span data-ttu-id="64377-154">Especifica cuándo se modificó un comentario por última vez.</span><span class="sxs-lookup"><span data-stu-id="64377-154">Specifies when a comment was last changed.</span></span>  <br/> |<span data-ttu-id="64377-155">Valores del tipo xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="64377-155">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="64377-156">PageID</span><span class="sxs-lookup"><span data-stu-id="64377-156">PageID</span></span>  <br/> |<span data-ttu-id="64377-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64377-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64377-158">necesario</span><span class="sxs-lookup"><span data-stu-id="64377-158">required</span></span>  <br/> |<span data-ttu-id="64377-159">Valor que identifica la página de dibujo en la que se encuentra el comentario.</span><span class="sxs-lookup"><span data-stu-id="64377-159">A value that identifies the drawing page the comment is on.</span></span>  <br/> |<span data-ttu-id="64377-160">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64377-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64377-161">ShapeID</span><span class="sxs-lookup"><span data-stu-id="64377-161">ShapeID</span></span>  <br/> |<span data-ttu-id="64377-162">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64377-162">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64377-163">opcional</span><span class="sxs-lookup"><span data-stu-id="64377-163">optional</span></span>  <br/> |<span data-ttu-id="64377-164">Valor que identifica la forma en la que se encuentra el comentario.</span><span class="sxs-lookup"><span data-stu-id="64377-164">A value that identifies the shape the comment is on.</span></span> <span data-ttu-id="64377-165">Si no se especifica ningún ShapeID, el comentario hace referencia a la página de dibujo.</span><span class="sxs-lookup"><span data-stu-id="64377-165">If no ShapeID is specified, the comment refers to the drawing page.</span></span>  <br/> |<span data-ttu-id="64377-166">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64377-166">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

