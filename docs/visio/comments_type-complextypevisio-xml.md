---
title: Comments_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393477"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="e92ae-102">Comments_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="e92ae-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e92ae-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="e92ae-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e92ae-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e92ae-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e92ae-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e92ae-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e92ae-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e92ae-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e92ae-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="e92ae-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e92ae-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e92ae-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e92ae-109">Definición</span><span class="sxs-lookup"><span data-stu-id="e92ae-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e92ae-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="e92ae-110">Elements and attributes</span></span>

<span data-ttu-id="e92ae-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="e92ae-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e92ae-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e92ae-112">Child elements</span></span>

|<span data-ttu-id="e92ae-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e92ae-113">**Element**</span></span>|<span data-ttu-id="e92ae-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e92ae-114">**Type**</span></span>|<span data-ttu-id="e92ae-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e92ae-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e92ae-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="e92ae-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e92ae-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="e92ae-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e92ae-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="e92ae-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e92ae-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="e92ae-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e92ae-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="e92ae-120">Attributes</span></span>

|<span data-ttu-id="e92ae-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e92ae-121">**Attribute**</span></span>|<span data-ttu-id="e92ae-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e92ae-122">**Type**</span></span>|<span data-ttu-id="e92ae-123">**Obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e92ae-123">**Required**</span></span>|<span data-ttu-id="e92ae-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e92ae-124">**Description**</span></span>|<span data-ttu-id="e92ae-125">**Valores posibles**</span><span class="sxs-lookup"><span data-stu-id="e92ae-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e92ae-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="e92ae-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="e92ae-127">Boolean con tipo</span><span class="sxs-lookup"><span data-stu-id="e92ae-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e92ae-128">opcional</span><span class="sxs-lookup"><span data-stu-id="e92ae-128">optional</span></span>  <br/> ||<span data-ttu-id="e92ae-129">Valores del tipo Boolean con tipo.</span><span class="sxs-lookup"><span data-stu-id="e92ae-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

