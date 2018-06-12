---
title: Elemento de CommentList (Comments_Type complexType) ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica los comentarios de un dibujo.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821802"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="3f51c-103">Elemento de CommentList (Comments_Type complexType) ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="3f51c-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3f51c-104">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="3f51c-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f51c-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3f51c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f51c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="3f51c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3f51c-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="3f51c-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3f51c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3f51c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3f51c-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3f51c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3f51c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3f51c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3f51c-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="3f51c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3f51c-112">Comments.Xml</span><span class="sxs-lookup"><span data-stu-id="3f51c-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3f51c-113">Definición</span><span class="sxs-lookup"><span data-stu-id="3f51c-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3f51c-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="3f51c-114">Elements and attributes</span></span>

<span data-ttu-id="3f51c-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="3f51c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3f51c-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3f51c-116">Parent elements</span></span>

|<span data-ttu-id="3f51c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f51c-117">**Element**</span></span>|<span data-ttu-id="3f51c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3f51c-118">**Type**</span></span>|<span data-ttu-id="3f51c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f51c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f51c-120">Comments</span><span class="sxs-lookup"><span data-stu-id="3f51c-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f51c-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="3f51c-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3f51c-122">Especifica propiedades que se usan para identificar los autores y los comentarios en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="3f51c-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3f51c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f51c-123">Child elements</span></span>

|<span data-ttu-id="3f51c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3f51c-124">**Element**</span></span>|<span data-ttu-id="3f51c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3f51c-125">**Type**</span></span>|<span data-ttu-id="3f51c-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3f51c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f51c-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="3f51c-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f51c-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="3f51c-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3f51c-129">Especifica las propiedades que se usa para identificar un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="3f51c-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3f51c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="3f51c-130">Attributes</span></span>

<span data-ttu-id="3f51c-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f51c-131">None.</span></span>
  

