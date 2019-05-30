---
title: Elemento CommentList (complexType Comments_Type) (XML de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Especifica los comentarios de un dibujo.
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539251"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="766d2-103">Elemento CommentList (complexType Comments_Type) (XML de Visio)</span><span class="sxs-lookup"><span data-stu-id="766d2-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="766d2-104">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="766d2-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="766d2-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="766d2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="766d2-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="766d2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="766d2-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="766d2-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="766d2-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="766d2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="766d2-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="766d2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="766d2-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="766d2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="766d2-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="766d2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="766d2-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="766d2-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="766d2-113">Definición</span><span class="sxs-lookup"><span data-stu-id="766d2-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="766d2-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="766d2-114">Elements and attributes</span></span>

<span data-ttu-id="766d2-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="766d2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="766d2-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="766d2-116">Parent elements</span></span>

|<span data-ttu-id="766d2-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="766d2-117">**Element**</span></span>|<span data-ttu-id="766d2-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="766d2-118">**Type**</span></span>|<span data-ttu-id="766d2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="766d2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="766d2-120">Comments</span><span class="sxs-lookup"><span data-stu-id="766d2-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="766d2-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="766d2-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="766d2-122">Especifica las propiedades que se usan para identificar los autores y los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="766d2-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="766d2-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="766d2-123">Child elements</span></span>

|<span data-ttu-id="766d2-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="766d2-124">**Element**</span></span>|<span data-ttu-id="766d2-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="766d2-125">**Type**</span></span>|<span data-ttu-id="766d2-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="766d2-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="766d2-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="766d2-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="766d2-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="766d2-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="766d2-129">Especifica las propiedades que se usan para identificar un Comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="766d2-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="766d2-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="766d2-130">Attributes</span></span>

<span data-ttu-id="766d2-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="766d2-131">None.</span></span>
  

