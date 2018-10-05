---
title: Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386337"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="d425a-103">Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="d425a-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d425a-104">Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d425a-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d425a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d425a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d425a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="d425a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d425a-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d425a-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d425a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d425a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d425a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d425a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d425a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d425a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d425a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="d425a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d425a-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="d425a-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d425a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="d425a-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d425a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="d425a-114">Elements and attributes</span></span>

<span data-ttu-id="d425a-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="d425a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d425a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d425a-116">Parent elements</span></span>

|<span data-ttu-id="d425a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d425a-117">**Element**</span></span>|<span data-ttu-id="d425a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d425a-118">**Type**</span></span>|<span data-ttu-id="d425a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d425a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d425a-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="d425a-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d425a-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="d425a-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d425a-122">Especifica a los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="d425a-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d425a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d425a-123">Child elements</span></span>

<span data-ttu-id="d425a-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d425a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d425a-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="d425a-125">Attributes</span></span>

|<span data-ttu-id="d425a-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d425a-126">**Attribute**</span></span>|<span data-ttu-id="d425a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d425a-127">**Type**</span></span>|<span data-ttu-id="d425a-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d425a-128">**Required**</span></span>|<span data-ttu-id="d425a-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d425a-129">**Description**</span></span>|<span data-ttu-id="d425a-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="d425a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d425a-131">ID</span><span class="sxs-lookup"><span data-stu-id="d425a-131">ID</span></span>  <br/> |<span data-ttu-id="d425a-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d425a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d425a-133">necesario</span><span class="sxs-lookup"><span data-stu-id="d425a-133">required</span></span>  <br/> |<span data-ttu-id="d425a-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="d425a-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="d425a-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d425a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d425a-136">Initials</span><span class="sxs-lookup"><span data-stu-id="d425a-136">Initials</span></span>  <br/> |<span data-ttu-id="d425a-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d425a-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d425a-138">opcional</span><span class="sxs-lookup"><span data-stu-id="d425a-138">optional</span></span>  <br/> |<span data-ttu-id="d425a-139">Las iniciales del autor.</span><span class="sxs-lookup"><span data-stu-id="d425a-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="d425a-140">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d425a-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d425a-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="d425a-141">Name</span></span>  <br/> |<span data-ttu-id="d425a-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d425a-142">xsd:string</span></span>  <br/> |<span data-ttu-id="d425a-143">opcional</span><span class="sxs-lookup"><span data-stu-id="d425a-143">optional</span></span>  <br/> |<span data-ttu-id="d425a-144">El nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="d425a-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="d425a-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d425a-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d425a-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="d425a-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="d425a-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="d425a-147">xsd:string</span></span>  <br/> |<span data-ttu-id="d425a-148">opcional</span><span class="sxs-lookup"><span data-stu-id="d425a-148">optional</span></span>  <br/> |<span data-ttu-id="d425a-149">Un identificador único para el autor.</span><span class="sxs-lookup"><span data-stu-id="d425a-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="d425a-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="d425a-150">Values of the xsd:string type.</span></span>  <br/> |
   

