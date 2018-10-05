---
title: Elemento de AuthorList (Comments_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica a los autores de comentarios en un dibujo.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387744"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="08ed3-103">Elemento de AuthorList (Comments_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="08ed3-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="08ed3-104">Especifica a los autores de comentarios en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="08ed3-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08ed3-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08ed3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08ed3-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="08ed3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="08ed3-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="08ed3-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="08ed3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="08ed3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="08ed3-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="08ed3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="08ed3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="08ed3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="08ed3-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="08ed3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="08ed3-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="08ed3-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="08ed3-113">Definición</span><span class="sxs-lookup"><span data-stu-id="08ed3-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="08ed3-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="08ed3-114">Elements and attributes</span></span>

<span data-ttu-id="08ed3-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="08ed3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="08ed3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08ed3-116">Parent elements</span></span>

|<span data-ttu-id="08ed3-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="08ed3-117">**Element**</span></span>|<span data-ttu-id="08ed3-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08ed3-118">**Type**</span></span>|<span data-ttu-id="08ed3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08ed3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08ed3-120">Comments</span><span class="sxs-lookup"><span data-stu-id="08ed3-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08ed3-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="08ed3-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="08ed3-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="08ed3-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="08ed3-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08ed3-123">Child elements</span></span>

|<span data-ttu-id="08ed3-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="08ed3-124">**Element**</span></span>|<span data-ttu-id="08ed3-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="08ed3-125">**Type**</span></span>|<span data-ttu-id="08ed3-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08ed3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="08ed3-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="08ed3-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="08ed3-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="08ed3-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="08ed3-129">Especifica las propiedades que identifican al autor de un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="08ed3-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="08ed3-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="08ed3-130">Attributes</span></span>

<span data-ttu-id="08ed3-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="08ed3-131">None.</span></span>
  

