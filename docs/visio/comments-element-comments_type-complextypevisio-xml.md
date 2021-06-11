---
title: Elemento Comments (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Especifica las propiedades usadas para identificar los autores y los comentarios de un dibujo.
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539223"
---
# <a name="comments-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="70d50-103">Elemento Comments (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="70d50-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="70d50-104">Especifica las propiedades usadas para identificar los autores y los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="70d50-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70d50-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="70d50-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70d50-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="70d50-106">**Element type**</span></span> <br/> |[<span data-ttu-id="70d50-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="70d50-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="70d50-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="70d50-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="70d50-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="70d50-109">**Schema file**</span></span> <br/> |<span data-ttu-id="70d50-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="70d50-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="70d50-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="70d50-111">**Document parts**</span></span> <br/> |<span data-ttu-id="70d50-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="70d50-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70d50-113">Definición</span><span class="sxs-lookup"><span data-stu-id="70d50-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="70d50-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="70d50-114">Elements and attributes</span></span>

<span data-ttu-id="70d50-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="70d50-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="70d50-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="70d50-116">Parent elements</span></span>

<span data-ttu-id="70d50-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="70d50-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70d50-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70d50-118">Child elements</span></span>

|<span data-ttu-id="70d50-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="70d50-119">**Element**</span></span>|<span data-ttu-id="70d50-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="70d50-120">**Type**</span></span>|<span data-ttu-id="70d50-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70d50-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70d50-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="70d50-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70d50-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="70d50-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70d50-124">Especifica los autores de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="70d50-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="70d50-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="70d50-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70d50-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="70d50-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="70d50-127">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="70d50-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="70d50-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="70d50-128">Attributes</span></span>

<span data-ttu-id="70d50-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="70d50-129">None.</span></span>
  

