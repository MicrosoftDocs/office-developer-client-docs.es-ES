---
title: CommentList_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359419"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="2968a-102">CommentList_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2968a-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2968a-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="2968a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2968a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2968a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2968a-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2968a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2968a-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="2968a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2968a-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="2968a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2968a-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2968a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2968a-109">Definición</span><span class="sxs-lookup"><span data-stu-id="2968a-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2968a-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="2968a-110">Elements and attributes</span></span>

<span data-ttu-id="2968a-111">Si el esquema define requisitos específicos, como **Sequence**, **minOccurs**, **maxOccurs**y **Choice**, consulte la sección de definición.</span><span class="sxs-lookup"><span data-stu-id="2968a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2968a-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2968a-112">Child elements</span></span>

|<span data-ttu-id="2968a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2968a-113">**Element**</span></span>|<span data-ttu-id="2968a-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2968a-114">**Type**</span></span>|<span data-ttu-id="2968a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2968a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2968a-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="2968a-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2968a-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2968a-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2968a-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="2968a-118">Attributes</span></span>

<span data-ttu-id="2968a-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2968a-119">None.</span></span>
  

