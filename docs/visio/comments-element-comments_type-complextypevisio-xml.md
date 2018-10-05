---
title: Elemento Comments (Comments_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica propiedades que se usan para identificar los autores y los comentarios en un dibujo.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389648"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="87f68-103">Elemento Comments (Comments_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="87f68-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="87f68-104">Especifica propiedades que se usan para identificar los autores y los comentarios en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="87f68-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87f68-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="87f68-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87f68-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="87f68-106">**Element type**</span></span> <br/> |[<span data-ttu-id="87f68-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="87f68-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="87f68-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="87f68-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="87f68-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="87f68-109">**Schema file**</span></span> <br/> |<span data-ttu-id="87f68-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="87f68-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="87f68-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="87f68-111">**Document parts**</span></span> <br/> |<span data-ttu-id="87f68-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="87f68-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="87f68-113">Definición</span><span class="sxs-lookup"><span data-stu-id="87f68-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="87f68-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="87f68-114">Elements and attributes</span></span>

<span data-ttu-id="87f68-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="87f68-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="87f68-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="87f68-116">Parent elements</span></span>

<span data-ttu-id="87f68-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87f68-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87f68-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="87f68-118">Child elements</span></span>

|<span data-ttu-id="87f68-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="87f68-119">**Element**</span></span>|<span data-ttu-id="87f68-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="87f68-120">**Type**</span></span>|<span data-ttu-id="87f68-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87f68-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="87f68-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="87f68-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87f68-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="87f68-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87f68-124">Especifica a los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="87f68-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="87f68-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="87f68-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="87f68-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="87f68-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="87f68-127">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="87f68-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="87f68-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="87f68-128">Attributes</span></span>

<span data-ttu-id="87f68-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="87f68-129">None.</span></span>
  

