---
title: CommentList_Type complexType ('XML de Visio')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393099"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="b751b-102">CommentList_Type complexType ('XML de Visio')</span><span class="sxs-lookup"><span data-stu-id="b751b-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b751b-103">Información de tipos</span><span class="sxs-lookup"><span data-stu-id="b751b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b751b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b751b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b751b-105">**Archivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b751b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b751b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b751b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b751b-107">**Base de extensión**</span><span class="sxs-lookup"><span data-stu-id="b751b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b751b-108">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b751b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b751b-109">Definición</span><span class="sxs-lookup"><span data-stu-id="b751b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b751b-110">Elementos y atributos</span><span class="sxs-lookup"><span data-stu-id="b751b-110">Elements and attributes</span></span>

<span data-ttu-id="b751b-111">Si el esquema define requisitos específicos, como **sequence**, **minOccurs**, **maxOccurs**y **choice**, consulte la sección definición.</span><span class="sxs-lookup"><span data-stu-id="b751b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b751b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b751b-112">Child elements</span></span>

|<span data-ttu-id="b751b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b751b-113">**Element**</span></span>|<span data-ttu-id="b751b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b751b-114">**Type**</span></span>|<span data-ttu-id="b751b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b751b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b751b-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="b751b-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b751b-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="b751b-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b751b-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="b751b-118">Attributes</span></span>

<span data-ttu-id="b751b-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b751b-119">None.</span></span>
  

