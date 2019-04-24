---
title: Elemento AuthorList (complexType Comments_Type) ("XML" de Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica los autores de comentarios en un dibujo.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338419"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="5910a-103">Elemento AuthorList (complexType Comments_Type) ("XML" de Visio)</span><span class="sxs-lookup"><span data-stu-id="5910a-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5910a-104">Especifica los autores de comentarios en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5910a-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5910a-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5910a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5910a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5910a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5910a-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="5910a-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5910a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5910a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5910a-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5910a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5910a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="5910a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5910a-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="5910a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5910a-112">comments. XML</span><span class="sxs-lookup"><span data-stu-id="5910a-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5910a-113">Definición</span><span class="sxs-lookup"><span data-stu-id="5910a-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5910a-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="5910a-114">Elements and attributes</span></span>

<span data-ttu-id="5910a-115">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="5910a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5910a-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5910a-116">Parent elements</span></span>

|<span data-ttu-id="5910a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5910a-117">**Element**</span></span>|<span data-ttu-id="5910a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5910a-118">**Type**</span></span>|<span data-ttu-id="5910a-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5910a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5910a-120">Comments</span><span class="sxs-lookup"><span data-stu-id="5910a-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5910a-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="5910a-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5910a-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5910a-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5910a-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5910a-123">Child elements</span></span>

|<span data-ttu-id="5910a-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5910a-124">**Element**</span></span>|<span data-ttu-id="5910a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5910a-125">**Type**</span></span>|<span data-ttu-id="5910a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5910a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5910a-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="5910a-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5910a-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="5910a-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5910a-129">Especifica las propiedades que identifican al autor de un Comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="5910a-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5910a-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="5910a-130">Attributes</span></span>

<span data-ttu-id="5910a-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5910a-131">None.</span></span>
  

