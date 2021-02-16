---
title: Elemento AuthorEntry (AuthorList_Type complexType) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Especifica las propiedades usadas para identificar al autor de un comentario en un dibujo.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537909"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a><span data-ttu-id="0adb2-103">Elemento AuthorEntry (AuthorList_Type complexType) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="0adb2-103">AuthorEntry element (AuthorList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="0adb2-104">Especifica las propiedades usadas para identificar al autor de un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="0adb2-104">Specifies properties used to identify the author of a comment in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0adb2-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0adb2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0adb2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0adb2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0adb2-107">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="0adb2-107">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0adb2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0adb2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0adb2-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0adb2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0adb2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0adb2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0adb2-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="0adb2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0adb2-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="0adb2-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0adb2-113">Definición</span><span class="sxs-lookup"><span data-stu-id="0adb2-113">Definition</span></span>

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0adb2-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="0adb2-114">Elements and attributes</span></span>

<span data-ttu-id="0adb2-115">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="0adb2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0adb2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0adb2-116">Parent elements</span></span>

|<span data-ttu-id="0adb2-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0adb2-117">**Element**</span></span>|<span data-ttu-id="0adb2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0adb2-118">**Type**</span></span>|<span data-ttu-id="0adb2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0adb2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0adb2-120">AuthorList</span><span class="sxs-lookup"><span data-stu-id="0adb2-120">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0adb2-121">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="0adb2-121">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0adb2-122">Especifica los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="0adb2-122">Specifies the authors in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0adb2-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0adb2-123">Child elements</span></span>

<span data-ttu-id="0adb2-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0adb2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0adb2-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="0adb2-125">Attributes</span></span>

|<span data-ttu-id="0adb2-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0adb2-126">**Attribute**</span></span>|<span data-ttu-id="0adb2-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0adb2-127">**Type**</span></span>|<span data-ttu-id="0adb2-128">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="0adb2-128">**Required**</span></span>|<span data-ttu-id="0adb2-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0adb2-129">**Description**</span></span>|<span data-ttu-id="0adb2-130">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="0adb2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0adb2-131">ID</span><span class="sxs-lookup"><span data-stu-id="0adb2-131">ID</span></span>  <br/> |<span data-ttu-id="0adb2-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0adb2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0adb2-133">necesario</span><span class="sxs-lookup"><span data-stu-id="0adb2-133">required</span></span>  <br/> |<span data-ttu-id="0adb2-134">Un valor basado en uno que identifica al autor.</span><span class="sxs-lookup"><span data-stu-id="0adb2-134">A one-based value that identifies the author.</span></span>  <br/> |<span data-ttu-id="0adb2-135">Valores del tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0adb2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0adb2-136">Initials</span><span class="sxs-lookup"><span data-stu-id="0adb2-136">Initials</span></span>  <br/> |<span data-ttu-id="0adb2-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0adb2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0adb2-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0adb2-138">optional</span></span>  <br/> |<span data-ttu-id="0adb2-139">Iniciales del autor.</span><span class="sxs-lookup"><span data-stu-id="0adb2-139">The initials of the author.</span></span>  <br/> |<span data-ttu-id="0adb2-140">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0adb2-140">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0adb2-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="0adb2-141">Name</span></span>  <br/> |<span data-ttu-id="0adb2-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0adb2-142">xsd:string</span></span>  <br/> |<span data-ttu-id="0adb2-143">opcional</span><span class="sxs-lookup"><span data-stu-id="0adb2-143">optional</span></span>  <br/> |<span data-ttu-id="0adb2-144">Nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="0adb2-144">The name of the author.</span></span>  <br/> |<span data-ttu-id="0adb2-145">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0adb2-145">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0adb2-146">ResolutionID</span><span class="sxs-lookup"><span data-stu-id="0adb2-146">ResolutionID</span></span>  <br/> |<span data-ttu-id="0adb2-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0adb2-147">xsd:string</span></span>  <br/> |<span data-ttu-id="0adb2-148">opcional</span><span class="sxs-lookup"><span data-stu-id="0adb2-148">optional</span></span>  <br/> |<span data-ttu-id="0adb2-149">Identificador único del autor.</span><span class="sxs-lookup"><span data-stu-id="0adb2-149">A unique identifier for the author.</span></span>  <br/> |<span data-ttu-id="0adb2-150">Valores del tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0adb2-150">Values of the xsd:string type.</span></span>  <br/> |
   

