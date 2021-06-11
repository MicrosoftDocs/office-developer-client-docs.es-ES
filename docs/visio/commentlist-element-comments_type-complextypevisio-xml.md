---
title: Elemento CommentList (Comments_Type complexType) (Visio XML)
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
# <a name="commentlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="ef754-103">Elemento CommentList (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ef754-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ef754-104">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ef754-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef754-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef754-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef754-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="ef754-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ef754-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="ef754-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ef754-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ef754-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ef754-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ef754-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ef754-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ef754-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ef754-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="ef754-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ef754-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="ef754-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ef754-113">Definición</span><span class="sxs-lookup"><span data-stu-id="ef754-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ef754-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="ef754-114">Elements and attributes</span></span>

<span data-ttu-id="ef754-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="ef754-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ef754-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef754-116">Parent elements</span></span>

|<span data-ttu-id="ef754-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef754-117">**Element**</span></span>|<span data-ttu-id="ef754-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ef754-118">**Type**</span></span>|<span data-ttu-id="ef754-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef754-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef754-120">Comments</span><span class="sxs-lookup"><span data-stu-id="ef754-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef754-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="ef754-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef754-122">Especifica las propiedades usadas para identificar los autores y los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ef754-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ef754-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef754-123">Child elements</span></span>

|<span data-ttu-id="ef754-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ef754-124">**Element**</span></span>|<span data-ttu-id="ef754-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ef754-125">**Type**</span></span>|<span data-ttu-id="ef754-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef754-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ef754-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="ef754-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ef754-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="ef754-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ef754-129">Especifica las propiedades usadas para identificar un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="ef754-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ef754-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef754-130">Attributes</span></span>

<span data-ttu-id="ef754-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ef754-131">None.</span></span>
  

