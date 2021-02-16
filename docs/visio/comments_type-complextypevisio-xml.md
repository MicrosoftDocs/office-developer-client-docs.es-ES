---
title: Comments_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542019"
---
# <a name="comments_type-complextype-visio-xml"></a><span data-ttu-id="e0700-102">Comments_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e0700-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e0700-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e0700-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0700-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0700-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0700-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e0700-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0700-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0700-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0700-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e0700-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0700-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e0700-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0700-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e0700-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0700-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e0700-110">Elements and attributes</span></span>

<span data-ttu-id="e0700-111">Si el esquema define requisitos específicos, como **secuencia,** **minOccurs**, **maxOccurs** y **elección,** vea la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="e0700-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0700-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0700-112">Child elements</span></span>

|<span data-ttu-id="e0700-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0700-113">**Element**</span></span>|<span data-ttu-id="e0700-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0700-114">**Type**</span></span>|<span data-ttu-id="e0700-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0700-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0700-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="e0700-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0700-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="e0700-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0700-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="e0700-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e0700-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="e0700-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0700-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0700-120">Attributes</span></span>

|<span data-ttu-id="e0700-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e0700-121">**Attribute**</span></span>|<span data-ttu-id="e0700-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0700-122">**Type**</span></span>|<span data-ttu-id="e0700-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e0700-123">**Required**</span></span>|<span data-ttu-id="e0700-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0700-124">**Description**</span></span>|<span data-ttu-id="e0700-125">**Posibles valores**</span><span class="sxs-lookup"><span data-stu-id="e0700-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0700-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="e0700-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="e0700-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e0700-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0700-128">opcional</span><span class="sxs-lookup"><span data-stu-id="e0700-128">optional</span></span>  <br/> ||<span data-ttu-id="e0700-129">Valores del tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e0700-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

