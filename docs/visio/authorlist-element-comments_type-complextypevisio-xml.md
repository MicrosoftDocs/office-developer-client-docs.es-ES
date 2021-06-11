---
title: Elemento AuthorList (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Especifica los autores de los comentarios de un dibujo.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537860"
---
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="cc3e5-103">Elemento AuthorList (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cc3e5-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="cc3e5-104">Especifica los autores de los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc3e5-105">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc3e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc3e5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc3e5-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="cc3e5-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cc3e5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cc3e5-109">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc3e5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cc3e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cc3e5-111">**Elementos de documento**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cc3e5-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="cc3e5-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc3e5-113">Definición</span><span class="sxs-lookup"><span data-stu-id="cc3e5-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc3e5-114">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="cc3e5-114">Elements and attributes</span></span>

<span data-ttu-id="cc3e5-115">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs** y **choice**, vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc3e5-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc3e5-116">Parent elements</span></span>

|<span data-ttu-id="cc3e5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-117">**Element**</span></span>|<span data-ttu-id="cc3e5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-118">**Type**</span></span>|<span data-ttu-id="cc3e5-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc3e5-120">Comments</span><span class="sxs-lookup"><span data-stu-id="cc3e5-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc3e5-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="cc3e5-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc3e5-122">Especifica los comentarios de un dibujo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cc3e5-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc3e5-123">Child elements</span></span>

|<span data-ttu-id="cc3e5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-124">**Element**</span></span>|<span data-ttu-id="cc3e5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-125">**Type**</span></span>|<span data-ttu-id="cc3e5-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc3e5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc3e5-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="cc3e5-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc3e5-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="cc3e5-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc3e5-129">Especifica las propiedades que identifican al autor de un comentario en un dibujo.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cc3e5-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc3e5-130">Attributes</span></span>

<span data-ttu-id="cc3e5-131">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cc3e5-131">None.</span></span>
  

