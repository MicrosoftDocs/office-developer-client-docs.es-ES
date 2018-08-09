---
title: Elemento Comments (Comments_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica propiedades que se usan para identificar los autores y los comentarios en un dibujo.
ms.openlocfilehash: 77695fb32aa88cb6c2b6ac5e9bff99fa12e262bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821798"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="a0226-103">Elemento Comments (Comments_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="a0226-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a0226-104">Especifica propiedades que se usan para identificar los autores y los comentarios en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="a0226-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0226-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a0226-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0226-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="a0226-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a0226-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="a0226-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a0226-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a0226-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a0226-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="a0226-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a0226-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a0226-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a0226-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="a0226-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a0226-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="a0226-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a0226-113">Definición</span><span class="sxs-lookup"><span data-stu-id="a0226-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a0226-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="a0226-114">Elements and attributes</span></span>

<span data-ttu-id="a0226-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="a0226-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a0226-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a0226-116">Parent elements</span></span>

<span data-ttu-id="a0226-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a0226-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0226-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a0226-118">Child elements</span></span>

|<span data-ttu-id="a0226-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0226-119">**Element**</span></span>|<span data-ttu-id="a0226-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a0226-120">**Type**</span></span>|<span data-ttu-id="a0226-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0226-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a0226-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="a0226-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0226-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="a0226-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a0226-124">Especifica a los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="a0226-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="a0226-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="a0226-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a0226-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="a0226-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a0226-127">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="a0226-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a0226-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="a0226-128">Attributes</span></span>

<span data-ttu-id="a0226-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a0226-129">None.</span></span>
  

