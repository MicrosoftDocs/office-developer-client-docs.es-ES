---
title: Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821543"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a><span data-ttu-id="1fdef-103">Elemento de AuthorEntry (AuthorList_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="1fdef-103">AuthorEntry element (AuthorList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1fdef-104">Especifica propiedades que se usan para identificar al autor de un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="1fdef-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1fdef-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1fdef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fdef-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1fdef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1fdef-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1fdef-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1fdef-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1fdef-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1fdef-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1fdef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1fdef-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1fdef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1fdef-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="1fdef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1fdef-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="1fdef-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1fdef-113">Definición</span><span class="sxs-lookup"><span data-stu-id="1fdef-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1fdef-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="1fdef-114">Elements and attributes</span></span>

<span data-ttu-id="1fdef-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="1fdef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1fdef-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1fdef-116">Parent elements</span></span>

|<span data-ttu-id="1fdef-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1fdef-117">**Element**</span></span>|<span data-ttu-id="1fdef-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1fdef-118">**Type**</span></span>|<span data-ttu-id="1fdef-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fdef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1fdef-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="1fdef-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1fdef-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="1fdef-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1fdef-122">Especifica a los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="1fdef-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1fdef-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1fdef-123">Child elements</span></span>

<span data-ttu-id="1fdef-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1fdef-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1fdef-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="1fdef-125">Attributes</span></span>

|<span data-ttu-id="1fdef-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1fdef-126">**Attribute**</span></span>|<span data-ttu-id="1fdef-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1fdef-127">**Type**</span></span>|<span data-ttu-id="1fdef-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="1fdef-128">**Required**</span></span>|<span data-ttu-id="1fdef-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1fdef-129">**Description**</span></span>|<span data-ttu-id="1fdef-130">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="1fdef-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1fdef-131">ID</span><span class="sxs-lookup"><span data-stu-id="1fdef-131">ID</span></span>  <br/> |<span data-ttu-id="1fdef-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1fdef-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1fdef-133">necesario</span><span class="sxs-lookup"><span data-stu-id="1fdef-133">required</span></span>  <br/> |<span data-ttu-id="1fdef-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="1fdef-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="1fdef-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1fdef-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1fdef-136">Initials</span><span class="sxs-lookup"><span data-stu-id="1fdef-136">Initials</span></span>  <br/> |<span data-ttu-id="1fdef-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1fdef-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1fdef-138">opcional</span><span class="sxs-lookup"><span data-stu-id="1fdef-138">optional</span></span>  <br/> |<span data-ttu-id="1fdef-139">Las iniciales del autor.</span><span class="sxs-lookup"><span data-stu-id="1fdef-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="1fdef-140">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="1fdef-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1fdef-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="1fdef-141">Name</span></span>  <br/> |<span data-ttu-id="1fdef-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1fdef-142">xsd:string</span></span>  <br/> |<span data-ttu-id="1fdef-143">opcional</span><span class="sxs-lookup"><span data-stu-id="1fdef-143">optional</span></span>  <br/> |<span data-ttu-id="1fdef-144">El nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="1fdef-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="1fdef-145">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="1fdef-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1fdef-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="1fdef-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="1fdef-147">xsd: String</span><span class="sxs-lookup"><span data-stu-id="1fdef-147">xsd:string</span></span>  <br/> |<span data-ttu-id="1fdef-148">opcional</span><span class="sxs-lookup"><span data-stu-id="1fdef-148">optional</span></span>  <br/> |<span data-ttu-id="1fdef-149">Un identificador único para el autor.</span><span class="sxs-lookup"><span data-stu-id="1fdef-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="1fdef-150">Valores del tipo XSD: String.</span><span class="sxs-lookup"><span data-stu-id="1fdef-150">Values of the xsd:string type.</span></span>  <br/> |
   

