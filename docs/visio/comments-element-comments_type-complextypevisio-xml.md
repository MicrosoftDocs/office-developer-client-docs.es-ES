---
title: Elemento Comments (Comments_Type complexType) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica las propiedades que se usan para identificar los autores y los comentarios de un dibujo.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359398"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="ba714-103">Elemento Comments (Comments_Type complexType) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="ba714-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ba714-104">Especifica las propiedades que se usan para identificar los autores y los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ba714-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba714-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba714-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba714-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ba714-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ba714-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="ba714-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ba714-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ba714-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ba714-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ba714-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ba714-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ba714-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ba714-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ba714-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ba714-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="ba714-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ba714-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ba714-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ba714-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ba714-114">Elements and attributes</span></span>

<span data-ttu-id="ba714-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ba714-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ba714-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba714-116">Parent elements</span></span>

<span data-ttu-id="ba714-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba714-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba714-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba714-118">Child elements</span></span>

|<span data-ttu-id="ba714-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ba714-119">**Element**</span></span>|<span data-ttu-id="ba714-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ba714-120">**Type**</span></span>|<span data-ttu-id="ba714-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba714-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ba714-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="ba714-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ba714-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="ba714-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ba714-124">Especifica los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ba714-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="ba714-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="ba714-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ba714-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="ba714-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ba714-127">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ba714-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ba714-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba714-128">Attributes</span></span>

<span data-ttu-id="ba714-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba714-129">None.</span></span>
  

